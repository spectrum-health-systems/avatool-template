<!--
  Github Repository Template (https://github.com/APrettyCoolProgram/repository-template)
  Version: Version 20.9.200904.1150
  Authors: development@aprettycoolprogram.com
-->

<!-- avatool-template README.md v1.0.0.0 -->

<h2 align="center">

  <img src="RepositoryData/Asset/Image/Logo/avatool-template-logo-with-text-256x256.png" alt="Avatool Template Logo" width="210"><br>
  A blank Avatool template
  <br>
  
</h2>

<h2 align="center">

  <img src="https://img.shields.io/badge/status-active-brightgreen.svg">&nbsp;[![License](https://img.shields.io/github/license/spectrum-health-systems/avatool-template)](https://www.apache.org/licenses/LICENSE-2.0)&nbsp;![GitHub release](https://img.shields.io/github/release/spectrum-health-systems/avatool-template?label=latest%20release)
  <br>

</h2>

<h6 align="center">

  [CHANGELOG](doc/repository/changelog.md)&nbsp;&bull;&nbsp;[ROADMAP](doc/repository/roadmap.md)&nbsp;&bull;&nbsp;[KNOWN ISSUES](doc/repository/known-issues.md)&nbsp;&bull;&nbsp;[SUPPORT](doc/repository/support.md)
  <br>

</h6>

<!-- The HTML indentations have to stay this way to work. -->
<table>
<tr>
<td img src="RepositoryData/Asset/Image/Document/README/spacer.png" alt="blank-spacer" width="1000" height="1">

  ### CONTENTS
  [ABOUT](#about)<br>
  [GETTING STARTED](#getting-started)<br>
  [INSTALLING](#installing)<br>
  [USING](#using)<br>
  [DEVELOPMENT](#development)<br>
  [ADDITIONAL INFORMATION](#additional-information)<br>

</td>
</tr>
</table>

# ABOUT
The Avatool Template is a blank template for building your own Avatool utilities for use with Netsmart's [myAvatar™](https://www.ntst.com/Solutions-and-Services/Offerings/myAvatar) EHR.

# GETTING STARTED

### Before you begin
Before you create your own Avatool utility, make sure the functionality you are looking for isn't already in [Avatool](https://github.com/spectrum-health-systems/avatool), and if it isn't, consider contributing to the Avatool project [directly](https://github.com/spectrum-health-systems/avatool/blob/master/doc/repository/contributing.md).

### Prerequisites
* Visual Studio 2019
* .NET Framework 4.7+
* Access to [Netsmart myAvatar™ web services](doc/list-of-netsmart-avatar-web-services.md)
* Optionally, access to a custom web service for use with myAvatar™

# INSTALLING
1. Download the latest [release](https://github.com/spectrum-health-systems/avatool-template/releases) of the Avatool Template
2. Copy the `avatool-template-vx.x.x.x-YYMMDD` file to the Visual Studio C# project template folder
3. Create a new project in Visual Studio using the Avatool Template project type

# USING
Out of the box, the Avatool Template is not associated with any web service(s), Netsmart or custom. You will need to add the web services you would like to use.

## Adding a Netsmart Avatar web service to your project

### Choose a Netsmart myAvatar™ web service
Look through the [list of Netsmart myAvatar™ web services](doc/list-of-netsmart-avatar-web-services.md) and determine which, if any, will suit your needs.

### Find the locations of Netsmart myAvatar™ web services in your environment
Before you add a Netsmart web service to your project, you need to know where the Netsmart web services are located.

To do this in for AVPM web services in your LIVE environment
1. Login to your LIVE environment
2. Open the **Registry Settings** form
3. In the upper right text box, type **Web Service**
4. Click **View Registry Settings**

A list of Registry Settings will appear.

Find the **Avatar Web Services[Avatar PM]** > **Set System Defaults** entry.

There should be a line that looks similar to this:
```
URL Regirsty Setting Value: https://<ORGANIZATION>csp.netsmartcloud.com/csp/<ORGANIZATION>/avpm
```

where `ORGANIZATION` is the name of your organization/company.

For other myAvatar™ Environments, the web services location will look like this:
```
URL Registy Setting Value: https://<ORGANIZATION>csp.netsmartcloud.com/csp/<ORGANIZATION><ENVIRONMENT>/avpm
```

### Verifying the Netsmart myAvatar™ web services location
To verify that the Netsmart Web Services are where they should be, and are active, open the following URL in a web browser:
```
https://<ORGANIZATION>.netsmartcloud.com/csp/<ORGANIZATION><ENVIRONMENT>/avpm/WEBSVC.UserManagement.cls
```

The supported operations of the User Management Web Service should be displayed.

Next, add `?WSDL` to the end of the URL so it looks like this:
```
https://<ORGANIZATION>.netsmartcloud.com/csp/<ORGANIZATION><ENVIRONMENT>/avpm/WEBSVC.UserManagement.cls?WSDL
```

This should display the web service definition language (WSDL) XML.

### Add a Netsmart myAvatar™ web service Service Reference to your project
These instructions are for Visual Studio 2019 projects .NET Framwork 4.7.2 C# projects.

1. Right-click on your project
2. Click **Add**
3. Click **Service Reference**
4. In the *Address* field, put the URL for the Web Service WSDL:
```
https://<ORGANIZATION>.netsmartcloud.com/csp/<ORGANIZATION><ENVIRONMENT>/avpm/WEBSVC.UserManagement.cls?WSDL
```

5. Click **Go**. The web service should be found.

6. In the *Namespace* field, give the web service a name. This is the name that your project will use to reference the web service, so make it something meaningful. For example:
```
NtstWebSvcUatUserManagement
```

7. Click **Ok**.

Repeat the above steps for each of your myAvatar™ environments.

## Adding a custom web service to your project
Instructions to add a custom web service to the Avatool template coming soon.

# DEVELOPMENT

### Contributors
* [Chris Banwarth](https://github.com/APrettyCoolProgram)

### Contributing
* [Code of conduct](doc/repository/code-of-conduct.md)
* [Contributing guidelines](doc/repository/contributing.md)
* [Testing procedures](doc/repository/testing.md)
* [Issue template](doc/repository/issue-template.md)
* [Pull request template](doc/repository/pull-request-template.md)

### Acknowledgements
* [Acknowledgements](doc/repository/acknowledgements.md)

# ADDITIONAL INFORMATION

### RELATED PROJECTS
* [ScriptLinkStandard](https://github.com/rcskids/ScriptLinkStandard)

***

<!-- DEVELOPMENT FOOTER -->
[![Developed by](https://img.shields.io/badge/developed%20by-a%20pretty%20cool%20program-17806D.svg)](https://aprettycoolprogram.com)&nbsp;[![Feedback](https://img.shields.io/badge/feedback@aprettycoolprogram.com-17806D.svg)](mailto:feedback@aprettycoolprogram.com)&nbsp;[![GitHub](https://img.shields.io/github/followers/aprettycoolprogram.svg?label=GitHub&style=social)](https://github.com/aprettycoolprogram)&nbsp;[![Twitter](https://img.shields.io/twitter/follow/aprettycoolprog.svg?label=Twitter&style=social)](https://twitter.com/aprettycoolprog)&nbsp;<br>
[![Repository built using](https://img.shields.io/badge/repository%20built%20using-a%20pretty%20cool%20repository%20template-17806D.svg)](https://github.com/APrettyCoolProgram/repository-template/tree/master)