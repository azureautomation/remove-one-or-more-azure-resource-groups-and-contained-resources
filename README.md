Remove one or more Azure resource groups and contained resources
================================================================

            

.SYNOPSIS   


Connects to Azure and removes resource groups that match the name filter   


.DESCRIPTION   


This runbook connects to Azure and removes resource groups with names that have substrings that match the name filter.  All of the resources in each resource group are also removed.  An important option is to run in preview mode to see which resource
 groups and resources will be removed without actually removing them.  The Azure subscription that is assumed is the subscription that contains the Automation account that is running this runbook.  The runbook will NOT remove the resource group that
 contains the Automation account that is running this runbook.   


REQUIRED AUTOMATION ASSETS      


An Automation connection asset that contains the Azure service principal, by default named AzureRunAsConnection.   


.PARAMETER  NameFilter   


Required   


Allows you to specify a name filter to limit the resource groups that you will remove.  


Pass multiple name filters through a comma separated list.       


The filter is not case sensitive and will match any resource group that contains the string.      


.PARAMETER PreviewMode   


Optional, with default of $true (preview mode is on by default).   


Execute the runbook to see which resource groups would be deleted but take no action. 


Run the runbook in preview mode first to see which resource groups would be removed.


.NOTES   


AUTHOR: Azure Automation Team    


LASTEDIT: 2016-9-19


 


 

 

        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
