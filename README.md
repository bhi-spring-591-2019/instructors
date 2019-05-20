# Welcome to Hands on with FHIR and other Healthcare Data Standards

## Spring 2019 591 C
Mondays, 12:30pm - 1:20pm in HST T530

SLN: 11121

This class will provide a hands-on learning experience with current data standards and tools used today throughout healthcare, including FHIR and Genomics. Each colloquium will include a 15-minute topic primer, and 30 minutes of dedicated assisted development time. Students will have the option to explore possible applications for these technologies, choose an area of interest, and work on a project of their choice throughout the quarter while assisted by the instructors. Topics will include some pre-FHIR standards, FHIR, SMART on FHIR, CDS Hooks, the Bulk Data FHIR API, and Genomic data standards like VCF. Students will have an opportunity to learn about and use the new Microsoft Azure FHIR server.

## Instructors repository
This repository is meant to be a shared repository for the class.  Basic course info, like this readme, and shared code from the instructors or class members can be found here.

## Google Drive Folder
https://drive.google.com/drive/folders/0AA5q0Q88uzOtUk9PVA

## Slack Workspace
https://join.slack.com/t/bime591sp19/signup

## Class schedule
This is our current plan for the course and what we will cover each day.  If it changes we will update it here and let everyone know.

|Date|Topic|Led By|
|:-------|:--------|:-----|
| Apr 1 | [Course Intro](#apr-1) <ul><li>Tech Setup & Primer - git, Azure, node, visual code, jupyter notebook, etc.</li><li>Project Intro and Project Brainstorm/Ideation</li></ul>|Hannah, Jared, Piotr|
|Apr 8 | [Man Before FHIR](#apr-8) <ul><li>HL7 2.5, CCD, XDS.b, and related XML standards</li><li>Project Ideation/Design</li></ul>| Jared |
| Apr 15 | [Discovering FHIR #1](#apr-15)<ul><li>Introduce resources</li><li>Query a FHIR endpoint</li></ul> | Piotr |
| Apr 22 | [Discovering FHIR #2](#apr-22) <ul><li>Identify required resources<li>Build a BMI Calculator using FHIR data</li></ul> | Hannah |
| Apr 29 | SMART on FHIR - EHRs as Application Platforms  | Piotr |
| May 6 | [CDS Hooks](#may-6) <ul><li>EHR Integration of Simple and Flexible Clinical Decision Support</li></ul> | Hannah<br>Tom Lang, MD, ER Doc |
| May 13 | Guest Speaker -- Details and discussion of  the Azure FHIR server from the Microsoft team | Michael Hansen, Program Manager at Microsoft |
| May 20 | Bulk FHIR & Data Analysis Pipelines | Piotr |
| May 27 | Memorial Day | |
| June 3 | Genetic Data Standards - VCF files, Presentations & Closing Ceremonies | Piotr, Jared, Hannah|

## Class notes
### May 6
Lesson Plan

|  **Approx. Time (min)** | **Topic** | **Instructor(s)** |
| :---: | :---: | :---: |
|  5 | Recap and Class Intro | Jared |
|  20 | CDS Hooks Tutorial<br>Running a basic CDS Hooks application, Structure of a CDS Hooks application, Using patient context in CDS Hooks, Calling an external API to calculate BMI<br/>[CDS Hooks tutorial](https://github.com/uw-fhir/CDS-Hooks-Tutorial/blob/master/tutorial.md) | Hannah |
|  15 | Guest speaker: Tom Lang, MD |  |
|  10 | Project Time | Jared, Hannah |


### Apr 22
Lesson Plan

|  **Approx. Time (min)** | **Topic** | **Instructor(s)** |
| :---: | :---: | :---: |
|  5 | Recap and Class Intro | Piotr, Jared, Hannah |
|  20 | FHIR BMI Calculator Tutorial<br/>Identify req Information, Identify req FHIR resources, Query to get patient data, Query to get weight/height data, Calculate BMI<br>https://github.com/uw-fhir/fhir-api-tutorial/blob/master/fhir-calculator-notebook-level2-ANSWERS.ipynb | Hannah |
|  25 | Project Time!<br/>Daily Exercise: Level 3 FHIR Tutorial, Hannah: GA Tech Project Interest group, Piotr (remote): SMART on FHIR interest group, Jared: Microsoft interest group | Piotr, Jared, Hannah |

### Apr 15
Lesson Plan

|  **Approx. Time (min)** | **Topic** | **Instructor(s)** |
| :---: | :---: | :---: |
|  5 | Meetup Recap, Quick recap of class so far | Piotr, Jared, Hannah |
|  10 | Requirement List Activity:<br/>BrainstormingComparisons Features | Piotr |
|  10 | Exploring FHIR with ClinFHIR<br/>http://clinfhir.com/ https://github.com/uw-fhir/fhir-api-tutorial<br/>Additional Resources:<br/>https://drive.google.com/open?id=1O5dz2rY7JpSVN3XcRCIuJVyJ5jfhaGK5 https://drive.google.com/open?id=1ERDQiTyD1BKefbJxCeayRgnCpTOkt15L | Piotr |
|  25 | Project Activity<br/>Pitch Categories Pitch major opportunities 3-pronged approach: Piotr: Patient portal integration Hannah: GA Project Jared: Working with the Azure FHIR server | Piotr, Jared, Hannah |

### Apr 8
Lesson Plan
### Added a walkthrough page of what we did in class [here](https://github.com/bhi-spring-591-2019/instructors/blob/master/HL7%20and%20XDSToolkit%20walkthrough.md)
|Time|Topic|Notes|
|:-------|:--------|:-----|
|5|Quick Intro for new class members||
|10|Presentation/Discussion on HL7 2.5.1, CCD/CDA and IHE XDS/XCA/XDR|<ul><li>Sample messages available in the repo, also sample [CDA here](https://github.com/chb/sample_ccdas/blob/master/HL7%20Samples/CCD.sample.xml)</li><li>HL7 editors: [7edit](http://www.7edit.com/home/index.php) (very good, free trial, then pay for it), [Smart HL7](http://smarthl7.com/)(free)</li><li>[Interoperability Standards Advisory](https://www.healthit.gov/isa/sites/isa/files/inline-files/2019ISAReferenceEdition.pdf)</li><li>[XDSToolKit a reference implementation of the IHE standard](https://github.com/usnistgov/iheos-toolkit2)</li>
|15|Hands on with some sample messages and registry/repository simulators|
|20|Remainder open for project discussions, exploring HL7 messages, XDS queries, etc.|

### Apr 1
- To do:
  - join Slack channel
  - make sure you are part of the Github organization (Jared will invite you - please send a reminder if you have not received an invitation)
  - install anaconda (comes with git, jupyter notebook, vscode - make sure these work). Post on slack if you run into problems.
  - in a Canvas message, send us your details so we can activate your MSDN account (name, email address, maining address, and phone number). Remember, you will get $150 of *monthly* Azure credits and the full suite of Microsoft products for 1 year, a $6000 value. This is a major perk of being in this class :)
  - if you like, continue working on ideation for your project in the Ideation document (Google Drive)
  
  
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3Nzk5MTY5MDcsLTE3MjU2MjA3NDcsMT
MxNzA5NjY3XX0=
-->