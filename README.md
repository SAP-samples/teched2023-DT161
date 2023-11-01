

# DT161 - Simplified Selective Data Transition 

## Description

This repository contains the material for the SAP TechEd 2023 session called DT161 - Simplified Selective Data Transition.  

## Overview

This session introduces attendees to the SAP Business Transformation Center, a new solution to to accelerate the transition of our customers from SAP ECC to SAP S/4HANA Cloud, private edition, and SAP S/4HANA. SAP Business Transformation Center helps you to gain insights into your source SAP ECC System and provides a guided user experience to identify and scope relevant data.

## Requirements

The requirements to follow the exercises in this repository are low, nevertheless it’s an advantage to have domain knowledge about the organization structure of SAP ECC and or at least one SAP ECC application component (e.g., FI, CO, MM, SD, PP etc.).

## Exercises

- Getting Started
  
   You can logon to SAP Business Transformation Center using the following URL: [SAP Business Transformation Center](https://dt161-vygek9xc.eu10.alm.cloud.sap)

   As logon user and password please use the following username & password. Please replace “###” with your group id (displayed at your table):
   - User: DT161_###
   - Password: Acce$$teched23

   Within the launchpad app overview, select the section “SAP Business Transformation Center / Transformation” to navigate to the single apps of the SAP Business Transformation Center.


- Exercise 1 – Upload the SAP Readiness Check file for SAP ERP Usage and Data Profiling (UDP)
    - Step 1.1. – Download the SAP Readiness Check UDP example file [here](https://github.com/SAP-samples/teched2023-DT161/blob/main/PTP_920_15.zip)
    - Step 1.2. – Upload the zip file from the SAP Readiness Check UDP example file

      - Click on the fiori app “Manage Analysis File” and press the “Create” button to upload the zip analysis file from step 1.1.
      - Start the name of the analysis file with your group id followed by dash “###-“ and optionally provide a short description in the field “Notes” and hit the “Create” button
    - Q1: Once the file has been successfully uploaded, what´s the User ID who ran the analysis in the ECC source system?

- Exercise 2 – Create a Digital Blueprint 
    - Step 2.1. – Create your Digital Blueprint
      - Click on the fiori app “Manage Digital Blueprints” and press “Create”
      
      - Enter a name of the Digital Blueprint with your group id followed by dash “###-“
      
      - Maintain a free text in the description

      - choose the uploaded analysis file from step 1.2 out of the value help in the field “Analysis File” and hit the “Create” button

    - Step 2.2. – Have a first look at your Digital Blueprint Data
      - Once your Digital Blueprint is created, first Data are displayed in the Fiori App
      - Quickly browse through the 3 sections on the App 
    - Q2: What's the System ID and the client of the ECC source system?
      

 - Exercise 3 – Get an overview about the data profile of your ECC source system
     - Step 3.1. – Start Digital Blueprint Overview
       - Click on the fiori app “Digital Blueprint Overview” and select your Digital Blueprint name with your group ID created in Exercise 2 from the dropdown list
       - Navigate through the in total 5 Cards of the Digital Blueprint Overview and adjust their size & appearance according to your needs
       - Choose the “Open Help” icon on the upper right screen to learn about the card for system hints
       - Change the dropdown menu of the tiles for "Company Code Selection" and "Transformation Object Selection" based on the available dimensions. 
    - Q3: How many Company Codes do exist in the ECC source system?
    - Q4: How many transformation objects do exist for application component CO (Controlling)?
    - Q5: Which Application Component contains the highest data count in the ECC source system?

 - Exercise 4 – Choose your company codes in scope for the transition to SAP S/4HANA
    - Step 4.1. – Start the Digital Blueprint Overview
      - Click on the header of the card “Company Code Selection” to jump into the scoping app for the company codes 
      - Alternatively, choose the App “Select Company Codes” from the Launchpad overview and select your Digital Blueprint ID and press the "Go" button
    - Step 4.2 – Set company codes out of scope
      - Select only company codes with a last activity greater equal 2022 independent whether there are open items or not by utilizing the settings of the company code list view as well as filtering and sorting
      - Set all other company codes with a last activity smaller than 2022 or without any activity to “Out of Scope” by using the button “Mass Edit”. Enter a comment, that those company codes are not relevant anymore due to inactivity.
    - Step 4.3 – Check details of a company code
      - Click on the company code “BE01” to jump into the details of the company code
      - Browse through the details of the company code
    - Q6: Which fiscal year variant is maintained for the company code BE01?
    - Q7: How many purchase orders have been created in company code BE01 in the year 2021?
    - Q8: Does the company code BE01 contain open customer items?
      - Add a free defined comment in the details of the company code and return to the company code overview


- Exercise 5 – Review your first scoping decision and its data impact
   - Step 5.1. – Start the Digital Blueprint Overview
     - Click on the fiori app “Digital Blueprint Overview” and select your Digital Blueprint name with your Group ID created in Exercise 2 from the dropdown list
     - Navigate through the cards of the Digital Blueprint Overview and explore the results of you previously done scoping decision
   - Q9: How many percent is the overall data footprint reduction resulting from your scoping decisions?
     

- Exercise 6 – Choose your transformation objects in scope for the transition to SAP S/4HANA
   - Step 6.1. – Start the Digital Blueprint Overview
     - Click on the header of the card “Transformation Object Selection” to jump into the scoping app for the transformation objects 
     - Alternatively, choose the app “Select Transformation Objects” from the app overview and select your Digital Blueprint ID
     - Explore the app content by changing settings in the transformation object list view (e.g. setting filters or change grouping / sorting)
   - Q10: Within application component “MM”, which transformation object has the highest total data count and what is the number of records?
   - Step 6.2 – Check details of a single transformation object
     - Click on the transformation object “Sales Document – Order” and have a look at the details page of the transformation object
     - Have a look at the company codes where the transformation object has been used, the company code scoping status und its data count
     - Compare the sum of the data counts for all company codes marked as out of scope and the figure for “Total Data Count” and “Relevant Data Count” at the top of the details page for the transformation object
     - Optionally, press the “Go to Technical Details” on the upper right of the detailed page of the selected transformation object to get insights on the table structure of the transformation object
   - Q11: What is the Total Data Count for transformation object "Sales Document - Order" in company code BE01?
   -  Step 6.3 – Set transformation objects out of scope
      - For business purposes, the management of real estate processes shall not be done in SAP S/4HANA. It is not known if this component is used at all in the ECC source system
      - Check if the application component “RE” contains usage data at all by utilizing the given filtering capabilities
      - Set the whole application component “RE” out of scope by using the “mass edit” option in the list overview and set the status value to “Confirmed”. Enter a comment that application component "RE" is no longer used in the future SAP S/4HANA environment.

- Exercise 7 – Review your scoping decision and confirm the Digital Blueprint
    - Step 7.1. – Start the Digital Blueprint Overview
      - Click on the fiori app “Digital Blueprint Overview” and select your Digital Blueprint name with your Group ID created in Exercise 2 from the dropdown list
      - Navigate through the cards of the Digital Blueprint Overview and explore the results of you previously done scoping decision
    - Q12: How many percent is the overall data footprint reduction resulting from your scoping decision?   
    - Step 7.2. – Confirm the Digital Blueprint
      - As a last step, manifest your scoping activities within the Digital Blueprint by setting the status to “Completed”
      - Click on the fiori app “Manage Digital Blueprints” and select your Digital Blueprint name with your group ID created in Exercise 2 from the dropdown list to jump into the details view
      - Hit the “Confirm Digital Blueprint” button and press “Ok” in case a warning Pop Up appears indicating an open confirmation status on transformation object level
      - Navigate back to the list overview and compare the timestamps of your Digital Blueprint ID for the
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
