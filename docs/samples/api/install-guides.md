# Installation guides for two audiences

This sample compares two guides for the same task, installing REST API documentation, written for two different audiences.

## About this sample

The project details are as follows:

- **Audiences:** Server administrators who install the API documentation on a server, and individual users who need the documentation on a local workstation outside the firewall
- **Problem:** The server installation made the documentation available only inside the firewall, so some users needed a separate local installation
- **My role:** Wrote both guides as lead writer
- **Verification:** Tested the local installation procedure by installing the software, and reviewed the server installation through demos with the deployment team

## How the guides differ

The two guides differ in the following ways:

| | Server installation | Local installation |
| --- | --- | --- |
| Audience | Server administrators at the financial institution | Individual users who need the documentation outside the firewall |
| Scope | Install or upgrade the REST API web server, by executable or command line, then confirm the installation | Install a standalone copy of the API documentation on one workstation |
| Prerequisites | .NET Framework, ASP.NET Core runtime, Web Deploy, current Windows updates, and the IIS server role on Windows Server | IIS enabled on the workstation |
| Structure | Checklist of procedures, prerequisites, field reference tables, and separate install and upgrade paths | Two short procedures |

## Excerpts

The following excerpts show how each guide addresses its audience.

### Server installation: introduction

This guide outlines the procedures to install or upgrade the REST API web server. The following checklist includes all the procedures in this guide:

- Set up the web server environment.
- Download the installation file and .zip file.
- Install or upgrade the REST API web server.
- Confirm the installation.
- Optional: Configure log file settings.

**Prerequisites:**

- Release current with the REST API package.
- Microsoft .NET Framework version 4.7.2 or later.
- Latest Microsoft Windows updates.
- Windows Server 2016 or Windows Server 2019, with the Web Server (IIS) role and role services installed.
- Microsoft ASP.NET Core 2.1 Runtime (v2.1.0) or later.
- Microsoft Web Deploy 3.6 on the workstation that runs the installation.

!!! important
    Perform the installation on a standalone server. You can't install REST API on a new or existing application server.

### Server installation: environment fields

On the environment window of the installer, specify the following:

| Field | Description |
| --- | --- |
| Environment | Select **Staging** or **Production** to indicate the install environment. Install in your staging environment first to confirm that it works as expected. |
| Environment Name | Enter the name of the environment, such as staging or production. |
| Institution Name | Enter the institution name as it appears in the virtual directory file path. You can use an abbreviation. |
| Site To Deploy | Leave this field as is unless you have already configured multiple websites on this web server. |

### Local installation

This procedure installs REST API documentation on a local workstation. The server installation makes the documentation available only inside the firewall. This procedure installs a standalone version of the API site so you can access the documentation from your workstation.

**Enable the web server (IIS):**

1. On your local workstation, open Control Panel and search for **Features**.
2. Click **Turn Windows features on or off**.
3. Select **Internet Information Services**, and then click **OK**. Windows installs the IIS feature.

**Install REST API documentation locally:**

1. Extract the contents of the REST API documentation .zip file to the following location on your workstation: `C:\API\2021`
2. In IIS, add a virtual directory. Enter an alias and the path where you extracted the files, and then click **OK**.
3. Select the virtual directory, and then click **Browse**. The REST API documentation opens in your browser.

!!! tip
    Bookmark the site location for future use.
