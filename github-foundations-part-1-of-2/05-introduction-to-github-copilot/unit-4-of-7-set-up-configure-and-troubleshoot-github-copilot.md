# Set up, configure, and troubleshoot GitHub Copilot

> 📘 Note: These notes follow a two-line progressive summary method.  
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

We will learn to sign up for GitHub Copilot, configure it for VS Code and troubleshoot it in VS Code
> Copilot has free and paid plans, configurable from VS Code

## Sign up for GitHub Copilot

Copilot requires a free trial or subscription
> Copilot can be used from VS Code with a subscription

GitHub > Profile Photo > *Settings* > *Code, planning and automation*
> You can sign up for Copilot from GitHub to use it in VS Code

You need to install an extension for your environment
> You can sign up for Copilot from GitHub to use it in an extension for VS Code, Visual Studio, JetBrains or Neovim

For this module we will use VS Code
> GitHub offers a plan for Copilot to use in your IDE

You can set up Copilot for other environments too
> Copilot is supported by extensions in VS Code, Visual Studio, JetBrains and Neovim

## Configure GitHub Copilot in VS Code

### Add the VS Code extension for GitHub Copilot

1. Find [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) in Visual Studio Marketplace and select *Install*
2. Select *Open* in the popup dialogue
3. Select *Install* on the *Extension: GitHub Copilot* tab in VS Code
4. Select *Sign in to GitHub* if prompted

> You can add a VS Code extension for Copilot from Visual Studio Marketplace

After installation you can enable, disable and configure Copilot in VS Code
> Copilot for VS Code  autocompletes code and has advanced settings that can be configured

### Enable or disable GitHub Copilot in VS Code

![Status Pane](https://learn.microsoft.com/en-us/training/github/introduction-to-github-copilot/media/status-icon-visual-studio-code.png)

1. Select the Copilot status icon and select *enable* or *disable*
2. When disabling, select *Disable completions* or *Disable completions for LANGUAGE*

> Copilot extension can be installed in VS Code from Visual Studio Marketplace and enabled globally, disabled globally, or disabled for specific languages

### Enable or disable inline suggestions in VS Code

![VSC Settings](https://learn.microsoft.com/en-us/training/github/introduction-to-github-copilot/media/vsc-settings.png)

1. *File* menu > *Preferences* > *Settings*
2. On the left pane of the settings tab, select *Extensions* > *GitHub Copilot*
3. *Editor: Enable Auto Completions* > checkbox

> In VS Code you can install Copilot Extension, enable it, disable it, disable for specific languages, and toggle auto completions

You can also enable or disable inline suggestions, and specify which for which languages you want to enable Copilot
> In VS Code you can install Copilot Extension, enable or disable it globally or for specific languages, and toggle auto completions

## Troubleshoot GitHub Copilot in VS Code

You can find VS Code logs by entering `Developer: Open Log File` or `Developer: Open Extensions Logs Folder`
> In VS Code you can install Copilot Extension, enable or disable by language, toggle auto completions, and troubleshoot using the VS Code logs

You can access Electron logs with *Help* > *Toggle Developer Tools* to access the logs for the process running VS Code
> In VS Code you can install Copilot Extension, enable or disable it by language, toggle auto complete, and troubleshoot using VS Code logs or Electron logs if needed

Network restrictions, firewall or proxy may cause problems for Copilot connection
> In VS Code Copilot you can enable or disable by language, toggle auto completion, and troubleshoot with VS Code logs and Electron logs, but your network must be configured correctly

**Troubleshoot connectivity for Copilot**
1. Open command palette with `Ctrl + Shift + P` (or `Cmd + Shift + P` for Mac)
2. Enter *Diagnostics* and select *GitHub Copilot: Collect Diagnostics*


