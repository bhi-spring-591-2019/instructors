
# How to deploy your Azure FHIR server and load it with data
We have mentioned several times about creating a FHIR server in Microsoft Azure and being able to use it a sandbox to store FHIR resources and connect a FHIR application to.  Here we want to give some more details about how to get that up and running.

While there are several options for deplying the FHIR API server, we will focus on a simple method that uses powershell to deploy the server in Azure, and will have authentication/authorization turned off by default.  This will make it much easier to access at the begining.
Microsoft has documentation on how to do this here: [https://github.com/Microsoft/fhir-server/blob/master/docs/DefaultDeployment.md](https://github.com/Microsoft/fhir-server/blob/master/docs/DefaultDeployment.md)
We are going to skip most of the steps and go straight to the section that starts with "To deploy without Authentication/Authorization:"
It lists two powershell commands:

    $rg = New-AzureRmResourceGroup -Name "RG-NAME" -Location westus2
    New-AzureRmResourceGroupDeployment -TemplateUri "https://raw.githubusercontent.com/Microsoft/fhir-server/master/samples/templates/default-azuredeploy.json" -ResourceGroupName $rg.ResourceGroupName -serviceName $fhirServiceName

Because we skipped a few steps, we need to add two previous commands:

    Connect-AzureRmAccount
    $fhirServiceName = "MyFhirServer"

Open powershell, run these two commands, and then the previous commands.  

Replace "RG-NAME" with a useful name for your new Azure resources.  This name is simply a friendly name that will group all the stuff you create in Azure for the FHIR Api together.
Replace "MyFhirServer" with a name that will be in the URL for your new server.

Once it is up and running, you will want to put some data in it.  It's no fun without some data!

A popular tool for generating "realistic" clinical data is [Synthea](https://github.com/synthetichealth/synthea).
This tool can generate FHIR resources which can be sent to a FHIR server.  These are generated as FHIR Bundle resources, a resource type which contains other resources.

To help load these into the Microsoft FHIR Server, we wrote a little tool which will send FHIR Bundles to a FHIR endpoint.  The code is in another repository in the same bhi-591 organization.
[https://github.com/bhi-spring-591-2019/SubmitFHIRBundle](https://github.com/bhi-spring-591-2019/SubmitFHIRBundle)

The code might also simply useful as a code example for accessing a FHIR server programmatically.

If you clone the repository you will get the source code, and also some already generated FHIR resources, so you don't need to use Synthea if you do not want to.

To run the tool to upload FHIR resources, you will need the [.Net Core Runtime](https://dotnet.microsoft.com/download).
Then download the tool from the github [releases](https://github.com/bhi-spring-591-2019/SubmitFHIRBundle/releases/download/v0.1/SubmitFHIRBundle.zip).

To run execute the following command

    dotnet SubmitFHIRBundle.dll -p patient1.json -s https://fhir591.azurewebsites.net
 


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzMTE2NTMyODcsLTEyMTAzMjE5NDksMT
A1NzY0MTc1MiwyMDQ3NzE2MTYyLDU1NjY2ODE2OV19
-->