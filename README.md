Local machine Script:
    -Invokes getnavworkshopvm.json ARM Template
ARM Template deploys the machine and invokes initialize.ps1:
    -Downloads all the scripts and files to the machine
    -Invokes SetupStart.ps1
SetupStart.ps1 invokes SetupVM.ps1
SetupVM.ps1:
    -Installs prerrequisites
    -Invokes SetupNavContainer.ps1
    -Invokes SetupDesktop.ps1
    -Invokes SetupWorkshop.ps1
    -Invokes FinalSetupScript.ps1 (if exists)
    -Invokes Windows Update
SetupNavContainer.ps1 builds Containers
SetupDesktop.ps1 installs VSCode and shortcuts
SetupWorkshop.ps1 installs .NET, Report Builder, GIT, P4Merge and Chrome

# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
