# Walkthrough of HL7/XDS demo from class
We used a tool, [7edit](http://www.7edit.com/home/index.php) to view an HL7 message and understand the different parts.

The message we used is in this repo, in the SampleMessages folder [here](https://github.com/bhi-spring-591-2019/instructors/blob/master/SampleMessages/ADT_GREEN992.ADT).  It has a free trial period of 21 days.
In particular we looked at the PID segment which contains the patient identifier.
![7edit HL7 ADT message](https://github.com/bhi-spring-591-2019/instructors/raw/master/WalkthroughImages/7editCapture.PNG)

We also looked a reference implementation of the XDS/XCA standard called the [XdsToolkit](https://github.com/usnistgov/iheos-toolkit2)
There is an example running for the class to explore here:
[http://xdstoolkit3.westcentralus.cloudapp.azure.com:8080/xdstools7.2.5/](http://xdstoolkit3.westcentralus.cloudapp.azure.com:8080/xdstools7.2.5/)
With the XdsToolkit, we wanted to search for all documents about a patient and then find a specific document.
In order to do that, we first sent an HL7 v2.51 ADT message to the toolkit to register the patient.
You can do this 7edit.  First press the red "Sender" arrow in the top toolbar.  Then enter the information of the receiving system in to 7edit.  The server is: xdstoolkit3.westcentralus.cloudapp.azure.com, and the port is 5000.
![enter image description here](https://github.com/bhi-spring-591-2019/instructors/raw/master/WalkthroughImages/7editSendProfile.PNG)
You can then press the green send button.

Now you can go back to XdsToolkit and search for that patient.
![enter image description here](https://github.com/bhi-spring-591-2019/instructors/raw/master/WalkthroughImages/XdsToolsFindDocument.PNG)
Click on "Inspect Results" to find the document id.
![enter image description here](https://github.com/bhi-spring-591-2019/instructors/raw/master/WalkthroughImages/XdsToolsInspectResults.PNG)
Finally copy that document Id to run a Get Documents query.
![enter image description here](https://github.com/bhi-spring-591-2019/instructors/raw/master/WalkthroughImages/XdsToolsGetDocument.PNG)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQyNTQ1NDI1NCw1NDYyODU3NzBdfQ==
-->