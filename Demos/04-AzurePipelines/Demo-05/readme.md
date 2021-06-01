# Configure a self hosted agent on an Azure Windows VM

[Self-hosted Windows agents](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/v2-windows?view=azure-devops)

## Quick Guide

-   Execute `create-agent-vm.azcli` to install the vm in Cloud Shell using

```bash
curl https://raw.githubusercontent.com/arambazamba/az-400/main/Demos/04-AzurePipelines/Demo-05/create-agent-vm.azcli | bash
```

> Note: If you want to change the vm size use: `az vm list-sizes --location westeurope -o table`

-   Execute `install-sw-devops-agent-vm.ps1` from inside the vm you created in the prev step to install Build Agent on VM

> Note: Instead of copying you can also execute `install-sw-devops-agent-vm.ps1` from GitHub in an elevated PowerShell prompt:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force;
Invoke-Expression ((New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/ARambazamba/AZ-400/main/Demos/04-AzurePipelines/Demo-05/setup-devops-agent-vm.ps1'))
```

-   Complete the agent config:

![config-agent.jpg](_images/config-agent.jpg)
