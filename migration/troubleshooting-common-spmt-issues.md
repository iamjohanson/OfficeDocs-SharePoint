---
title: "Troubleshooting SharePoint Migration Tool"
ms.author: jhendr
author: JoanneHendrickson
manager: pamgreen
ms.audience: ITPro
ms.topic: article
ms.prod: sharepoint-server-itpro
localization_priority: Priority
ms.collection: 
- IT_Sharepoint_Server_Top
- Strat_SP_gtc
ms.custom: 

description: "How to troubleshoot common errors in the SharePoint Migration Tool."
---
## Troubleshooting common SPMT errors
|**Error Code**|**Error description and Recommendation**|
|:-----|:-----|
|0x0201000D|The list does not exist or cannot be accessed. </br>**Action** Check if the list exists or if you can access the list in source site and target site.|
|0x02050008|Failed to access local storage. . </br>**Action** Do not open, edit or delete the SPMT working folder %appdata%\Microsoft\MigrationToolStorage or its contents. Restart your migration.|
|0x02010023|Your source list template is not supported.  Please try another. . </br>**Action** The source list is not supported or with unsupported dependencies, such as unsupported taxonomy, the source list template is not supported, or that the lookup field reference is broken. Please check StructureReport_XX.csv for more details.  The StructureReport_XX.csv report is is under "*C:\Users\%user name%\AppData\Roaming\Microsoft\MigrationTool\admin@XXXX.onmicrosoft.com\WF_XXXXX\Report*" folder.|
|0x0201000C|Invalid credentials. Check if you can access the source sites and lists with your credentials. . </br>**Action** Make sure you are the site collection admin for source and target. Check if you can modify SPO target site.|
|0x02010017|You do not have sufficient permission. . </br>**Action** Make sure the user is site collection admin.|
|0x02060009|1. The site collection cannot be created because the URL is already in use or an invalid URL. **Action** The site collection cannot be created because the URL is already in use or an invalid URL.</br></br>2. The site collection cannot be created because the URL contains invalid character.</br> **Action** The site collection cannot be created because the URL contains invalid character. </br></br>3. The site collection cannot be created or updated. Make sure you are tenant admin. Check below items for potential failure reasons**Action** The site collection cannot be created or updated.| </br></br>
|0x02010018|1. Check your credentials and try again.</br>  Reason: Invalid credentials</br></br>2. A problem occurred accessing SharePoint.  Check your credentials and try again SharePoint access failure - SharePoint library was not found</br> .The list doesn't exist</br></br>3. A problem occurred accessing SharePoint.  Check your credentials and try again SharePoint access failure - Server cannot be connected </br> Network connection issue</br></br>4. A problem occurred accessing SharePoint.  Check your credentials and try again SharePoint access failure - Web issue</br> Invalid site URL</br></br>5. A problem occurred accessing SharePoint.  Check your credentials and try again SharePoint access failure - Invalid URL format</br> Wrong URL format</br></br>6. A problem occurred accessing SharePoint.  Check your credentials and try again SharePoint access failure - Unexpected failure</br> An unexpected error occurs. Please create a support case. </br></br>7. A problem occurred accessing SharePoint.  Check your credentials and try again SharePoint access failure - DNS resolving failure. Error occurs during data source scanning.  Check below for potential failure reasons.</br>. Check network for potential DNS resolving issue. Open the site in browser.|
|0x0204000A|Cannot create package file due to file being locked. </br> **Action** Check %appdata%\Microsoft\MigrationToolStorage and make sure all the files/folders are not opened during migration.|
|0x02030001|1. Query job status SharePoint access failure - I</br>**Action** Invalid credentials</br></br>2. Query job status SharePoint access failure - SharePoint library is not found</</br>**Action** Invalid credentials</br></br>3. Query job status SharePoint access failure - Server cannot be connected</br>**Action** The list doesn't exist</br></br>4. Query job status SharePoint access failure - Web issue</br>**Action** Network connection issue</br></br>5. Query job status SharePoint access failure - Invalid URL format</br>**Action** Invalid URL format </br></br>6. Query job status SharePoint access failure - Unexpected failure</br>**Action** An unexpected error occurred. Please create a support case. </br></br>7. Query job status SharePoint access failure - DNS resolving failure. This error occurs when submitting migration job to SPO. </br>**Action** Check network for potential DNS resolving issue. Open the site in browser.| </br></br>
|0x02010008|Invalid user mapping. Check your user mapping file for correct formatting and access.</br> **Action** Check to see if you have permission to access the user mapping .csv file and if the path and format of the  user mapping file is correct.|
|0x02050001|Local storage file is corrupted.</br> **Action** Do not open, edit or delete the SPMT working folder %appdata%\Microsoft\MigrationToolStorage or its contents. Restart your migration.
|0x02010002|Unable to access the source SharePoint site. .</br> **Action** Check your network status.  If you can access the source sites from a browser, then create a support case.|
|0x02010010|The selected source list has a different template than the target one. .</br> **Action** Make sure the source list and target list have the same template. For file share migration, the target must be a document library or my site.|
|0x0204000D|An unexcepted exception occurred when saving the Prime package. .</br> **Action** Do not open, edit or delete the SPMT working folder %appdata%\Microsoft\MigrationToolStorage or its contents. Restart your migration.|
|0x02080001|The file in the package has been changed or deleted while uploading. .</br> **Action** Do not open, edit or delete the SPMT working folder %appdata%\Microsoft\MigrationToolStorage or its contents. Restart your migration.|
|0x02010006|The source SharePoint site does not have any defined role definitions. .</br> **Action** Access to websites, lists, folders, and list items are controlled through a role-based membership system.  Users are assigned to roles that authorize their access to SharePoint objects. Check to see if your role exists when accessing source site.|
|0x02040009|The package file can't be created because the directory can't be found.Check %appdata%\Microsoft\MigrationToolStorage.  .</br> **Action** Make sure this folder is not touched during migration.|
|0x02010020|Versioning is disabled on SPO, but the source data might have version history. Please turn off version support in SPMT or enable version in SPO. .</br> **Action** Turn off migrate version history in SPMT settings or enable version in SPO.|
|0x0201000E|Invalid SharePoint path..</br> **Action** heck if the global setting has filtered out some special characters in the target path or if the path has unsupported characters like |
|0x02010016|We are unable to find your SharePoint Server user.  Make sure you are a site collection admin. .</br> **Action** Check the SharePoint user on the source web. This happens if SPMT cannot read user info from the web. Make sure you are the site collection admin for source.|