[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/teched2023-DT161)](https://api.reuse.software/info/github.com/SAP-samples/teched2023-DT161)

# DT161 - Simplified Selective Data Transition 

## Description

This repository contains the material for the SAP TechEd 2022 session called DT161 - Simplified Selective Data Transition.  

## Overview

This session introduces attendees to the SAP Business Transformation Center, a solution to identify and move data from SAP ECC to SAP S/4HANA. 

## Requirements

The requirements to follow the exercises in this repository are low, nevertheless it’s an advantage to have domain knowledge about the organization structure of SAP ECC and or at least one SAP ECC application component (e.g., FI, CO, MM, SD, PP etc.).

## Exercises

- Getting Started
You can logon to SAP Business Transformation Center using the following URL: [SAP Business Transformation Center](https://dt161-vygek9xc.eu10.alm.cloud.sap)
As logon user and password please use the following username & password. Please replace “###” with your group id (displayed at your table):
   - User: DT161_###
   - Password: Acce$$teched23
     
   Within the Launchpad App Overview, select the Section “SAP Business Transformation Center” to navigate to the single Apps of the SAP Business Transformation Center


- Exercise 1 – Upload the SAP Readiness Check File for SAP ERP Usage and Data Profiling (UDP)
    - Step 1.1. – Download the SAP Readiness Check UDP example file [here](https://github.com/SAP-samples/teched2023-DT161/blob/main/PTP_920_15.zip)
    - Step 1.2. – Upload the Zip File from the SAP Readiness Check UDP example file
      Click on the Fiori App “Manage Analysis File” and press the “Create” Button to upload the Zip analysis file from step 1.1.
      Start the name of the analysis file with your group id followed by dash “###-“ and optionally provide a short description in the field “Notes” hit the “Create” button
    - Q1: Once the file has been successfully uploaded, what´s the User ID who run the Analysis in the ECC source system?

- Exercise 2 – Create a Digital Blueprint 
    - Step 2.1. – Create your Digital Blueprint
      Click on the Fiori App “Manage Digital Blueprints” and press “Create”
      Enter a name of the Digital Blueprint with your group id followed by dash “###-“
      Maintain a free text in the description
      choose the uploaded analysis file from step 1.2 out of the value help in the field “Analysis File” and hit the “Create” Button

    - Step 2.2. – Have a first look at your Digital Blueprint Data
      Once your Digital Blueprint is created, first Data are displayed in the Fiori App
      Quickly browse through the 3 sections on the App 
    - Q2: What's the System ID and the client of the ECC source system?
      

 - Exercise 3 – Get an Overview about the Data Profile of your ECC source system
     - Step 3.1. – Start the Digital Blueprint Overview
       Click on the Fiori App “Digital Blueprint Overview” and select your Digital Blueprint Name with your Group ID created in Exercise 2 from the dropdown list
       Navigate through the in total 5 Cards of the Digital Blueprint Overview and adjust their size & appearance according to your needs
       Choose the “Open Help” Icon on the upper right screen to learn about the Card for System Hints
    - Q3: How many Company Codes do exist in the ECC source system?
    - Q4: Which Application Component contains the most data sets in the ECC source system?

 - Exercise 4 – Choose your Company Codes in Scope for the Transition to SAP S/4HANA
    - Step 4.1. – Start the Digital Blueprint Overview
      Click on the header of the Card “Company Code Selection” to jump into the Scoping App for the Company Codes 
      Alternatively, choose the App “Select Company Codes” from the App Overview and select your Digital Blueprint ID
    - Step 4.2 – Set Company Codes out of Scope
      Select only company codes with a last activity greater equal 2022 independent whether they are open items or not by utilizing the settings of the company code list view as well as filtering and sorting
      Set all other Company Codes with a last activity smaller than 2022 to “Out of Scope” by using the button “Mass Edit”
    - Step 4.3 – Check Details of a Company Code
      Click on the Company Code “BE01” to jump into the Details Page of the Company Code
      Browse through the details of the Company Code
    - Q5: Which fiscal year variant is maintained for the Company Code BE01?
    - Q6: How many Purchase Orders have been created in Company Code BE01 in the year 2021?
    - Q7: Does the Company Code BE01 contain open Customer Items?
      Add a free defined comment in the details of the Company Code and leave the details of the Company Code BE01


- Exercise 5 – Review your first Scoping Decision and its Data impact
   - Step 5.1. – Start the Digital Blueprint Overview
     Click on the Fiori App “Digital Blueprint Overview” and select your Digital Blueprint Name with your Group ID created in Exercise 2 from the dropdown list
     Navigate through the Cards of the Digital Blueprint Overview and explore the results of you previously done scoping decision
   - Q8: How many percent is the overall data footprint reduction resulting from your scoping decision?
     

- Exercise 6 – Choose your Transformation Objects in Scope for the Transition to SAP S/4HANA
   - Step 6.1. – Start the Digital Blueprint Overview
     Click on the header of the Card “Transformation Object Selection” to jump into the Scoping App for the Transformation Objects 
     Alternatively, choose the App “Select Transformation Objects” from the App Overview and select your Digital Blueprint ID
     Explore the App Content by changing settings in the Transformation Object List view
   - Q9: Which Transformation Object contains the oldest Last Activity Date?
   - Q10: Within Application Component “SD”, which Transformation Object has the latest Last Activity Date and when?
   - Step 6.2 – Check Details of a single Transformation Object
     Click on the Transformation Object “Sales Document – Order” and have a look at the details page of the Transformation Object
     Have a look at the Company Codes where the Transformation Object has been used, the Company Code Scoping Status und its Data Count
     Compare the Sum of the Data Counts for all Company Codes marked as out of Scope and the Figure for “Total Data Count” and “Relevant Data Count” at the top of the details page for the Transformation Object
     Optionally, press the “Go to Technical Details” on the upper right of the detailed page of the selected Transformation Object to get insights on the table structure of the transformation object


   -  Step 6.3 – Set Transformation Objects out of Scope
      For business purposes, the management of real estate processes shall not be done in S/4HANA. It is not known if this component is used at all in the ECC source system
      Check if the Application Component “RE” contains usage data at all by utilizing the given filtering capabilities
      Set the whole Application Component “RE” out of Scope by using the “mass edit” option in the list overview and set the Status Value to “Confirmed”

- Exercise 7 – Review your Scoping Decision and Confirm the Digital Blueprint
    - Step 7.1. – Start the Digital Blueprint Overview
      Click on the Fiori App “Digital Blueprint Overview” and select your Digital Blueprint Name with your Group ID created in Exercise 2 from the dropdown list
      Navigate through the Cards of the Digital Blueprint Overview and explore the results of you previously done scoping decision
    - Q11: How many percent is the overall data footprint reduction resulting from your scoping decision?   
    - Step 7.2. – Confirm the Digital Blueprint
      As a last step, manifest your scoping activities within the Digital Blueprint by setting the status to “Completed”
      Click on the Fiori App “Manage Digital Blueprints” and select your Digital Blueprint Name with your Group ID created in Exercise 2 from the dropdown list to jump into the details view
      Hit the “Confirm Digital Blueprint” Button and Press “Ok” in case a warning Pop Up appears indicating an open confirmation status on transformation object level
      Navigate back to the list overview and compare the timestamps of your Digital Blueprint ID for the
      - analysis date & time
      - creation date & time
      - confirmation date & time



**IMPORTANT**

Your repo must contain the .reuse and LICENSES folder and the License section below. DO NOT REMOVE the section or folders/files. Also, remove all unused template assets(images, folders, etc) from the exercises folder. 

## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2023 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
