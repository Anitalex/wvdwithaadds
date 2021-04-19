# Windows Virtual Desktop with Azure AD Domain Services

<h2> Issues Viewing on Github</h2>

This project is created using Jupyterlab and you may have issues rendering it with out installing Jupyterlab or issues rendering it on Github.
The message you may receive is...
"Sorry, something went wrong. Reload?" when viewing an *.ipynb on a GitHub blob page.

Probably a problem with the GitHub notebook viewing tool - sometimes github fails to render the ipynb notebooks

<h3>Workarounnd</h3>
Try to open that notebook that you want using nbviewer online, you don't need to install it.

Open "https://nbviewer.jupyter.org/"
Paste the link to your notebook


<h2>Install Jupyter Lab or Notebooks locally</h2>
In addition you can install Jupyterlab if you do not already have it.

You can find information here to install it...https://jupyter.org/install.html
I found this article to be a great resource on getting it installed with the pre-requisites for using Powershell with Jupyter....https://blog.darrenjrobinson.com/getting-started-with-local-powershell-jupyter-notebook/


<h2>Project Outline</h2>

<h3>DO NOT USE THIS WALKTHROUGH IF YOUR ONPREMISE DOMAIN HAS ALREADY BEEN EXTENDED TO AZURE!!</h3>
There will be another future walkthrough coming for that

1. Log in to Azure
  2. Create a resource group
  3. Create virtual network and subnets
    4. Create subnet for Azure AD Domain Services
    5. Create subnet for Windows Virtual Desktop
    6. Create subnet for additional workloads
7. Connect to Azure AD
  8. Add a service principal
  9. Create the AAD DC Administrators group
    10. Add your first administrator
  11. Register the Azure AD Domain Services resource provider
12. Create a Network Security Group for AADDS and attach it to the subnnet
13. Create the Azure AD Domain Services domain
  14. Add the IPs of the 2 domain controllers to the DNS servers of the virtual network
18. Create an Azure File Shares storage account
  19. Give permission to be managed by the AADDS domain
  20. Create the Profiles share
  21. Create the Redirections share
  22. Add the Redirections.xml to the Redirections share
23. Create a virtual machine to manage the AADDS domain
  24. Add the Group Policy Management feature and the AD DS Tools feature
25. Add the FSLogix admx and the OneDrive admx to the domain
26. Configure FSLogix and OneDrive group policies
27. Create the Windows Virtual Desktop host pool
  28. Add FSLogix to the VM
29. 
