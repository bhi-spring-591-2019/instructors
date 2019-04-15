
# How to deploy your Azure FHIR server and load it with data
We have mentioned several times about creating a FHIR server in Microsoft Azure and being able to use it a sandbox to store FHIR resources and connect a FHIR application to.  Here we want to give some more details about how to get that up and running.

While there are several options for deplying the FHIR API server, we will focus on a simple method that uses powershell to deploy the server in Azure, and will have authentication/authorization turned off by default.  This will make it much easier to access at the begining.
Microsoft has documentation on how to do this here: [https://github.com/Microsoft/fhir-server/blob/master/docs/DefaultDeployment.md](https://github.com/Microsoft/fhir-server/blob/master/docs/DefaultDeployment.md)
We are going to skip most of the steps and go straight to the section that starts with "To deploy without Authentication/Authorization:"
It lists two commands:

    $rg = New-AzureRmResourceGroup -Name "RG-NAME" -Location westus2
    New-AzureRmResourceGroupDeployment -TemplateUri "https://raw.githubusercontent.com/Microsoft/fhir-server/master/samples/templates/default-azuredeploy.json" -ResourceGroupName $rg.ResourceGroupName -serviceName $fhirServiceName

Because we skipped a few steps, we need to
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyMTA0MDU3NzcsNTU2NjY4MTY5XX0=
-->