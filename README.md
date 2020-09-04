<!--
  Github Repository Template (https://github.com/APrettyCoolProgram/repository-template)
  Version: Version 20.9.200904.1150
  Authors: development@aprettycoolprogram.com
-->

<h2 align="center">

  <img src="RepositoryData/Asset/Image/Logo/avatool-template-logo-with-text-256x256.png" alt="Avatool Template Logo" width="210"><br>
  A blank Avatool template
  <br>
  
</h2>

<h2 align="center">

  <img src="https://img.shields.io/badge/status-active-brightgreen.svg">&nbsp;[![License](https://img.shields.io/github/license/spectrum-health-systems/avatool-template)](https://www.apache.org/licenses/LICENSE-2.0)&nbsp;![GitHub release](https://img.shields.io/github/release/spectrum-health-systems/avatool-template?label=latest%20release)
  <br>

</h2>

<!-- SOON -->
<!-- REPOSITORY SCREENSHOT -->
<!--
<h1 align="center">

  <img src="RepositoryData/Asset/Image/Screenshot/screenshot.png" alt="Repository Screenshot" width="500">
  <br>

</h1>
-->

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
  [SETUP](#setup)<br>
  [USAGE](#usage)<br>
  [COMPILING](#compiling)<br>
  [TESTING](#testing)<br>
  [API](#api)<br>
  [DEVELOPMENT](#development)<br>
  [ADDITIONAL INFORMATION](#additional-information)<br>

</td>
</tr>
</table>

# About
The Avatool Template is a blank template for building your own Avatool utilities.
### Features
* Feature #1
* Feature #2
* Feature #3

# Getting started
### Before you begin
Before you create your own Avatool utility, make sure what you're looking for isn't already in [Avatool](https://github.com/spectrum-health-systems/avatool).
### Prerequisites
* Visual Studio 2019
* .NET Framework 4.7+
* Access to the Netsmart Web Services

#### Netsmart Web Services that are currently used with Avatool
Avatool uses the following Netsmart Web Services:

- User Management (WEBSVC.UserManagement.CLS)

# Setup
1. Download the latest [release](https://github.com/spectrum-health-systems/avatool-template/releases)
2. Open the solution in Visual Studio 2019

<!-- HOW TO USE -->
# Using
## Adding a Netsmart Avatar Web Service to your project
Before you add a Netsmart Web Service to your project, you need to know where the Netsmart Web Services are located.

### Determining the Web Services location
To do this in for AVPM Web Services in your LIVE environment
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

For other Avatar Environments, the Web Services location will look like this:
```
URL Regirsty Setting Value: https://<ORGANIZATION>csp.netsmartcloud.com/csp/<ORGANIZATION><ENVIRONMENT>/avpm
```

## Verifying the Web Services location
To verify that the Netsmart Web Services are where they should be, and are active, open the following URL in a web browser:
```
https://<ORGANIZATION>.netsmartcloud.com/csp/<ORGANIZATION><ENVIRONMENT>/avpm/WEBSVC.UserManagement.cls
```

The supported operations of the User Management Web Service should be displayed.

Next, add `?WSDL` to the end of the URL so it looks like this:
```
https://<ORGANIZATION>.netsmartcloud.com/csp/<ORGANIZATION><ENVIRONMENT>/avpm/WEBSVC.UserManagement.cls?WSDL
```

This should display the Web Service Definition Language XML.

## Adding a Netsmart Web Service to your project:
These instructions are for Visual Studio 2019 projects .NET Framwork 4.7.2 C# projects.

1. Right-click on your project
2. Click **Add**
3. Click **Service Reference**
4. In the *Address* field, put the URL for the Web Service WSDL:
```
https://<ORGANIZATION>.netsmartcloud.com/csp/<ORGANIZATION><ENVIRONMENT>/avpm/WEBSVC.UserManagement.cls?WSDL
```

5. Click **Go**. The Web Service should be found.

6. In the *Namespace* field, give the Web Service a name. This is the name that your project will use to reference the Web Service, so make it something meaningful. For example:
```
NtstWebSvcUatUserManagement
```

7. Click **Ok**.

Repeat steps 1-5 for each of your Avatar environments.

<!-- FREQUENTLEY ASKED QUESTIONS -->
# FAQ
### Are you nice?
I think so.

<!-- PROJECT DEVELOPMENT -->
# Development
A blurb about development can go here.
### Contributors
* [Contributor #1](URL/Email)
* [Contributor #2](URL/Email)
* [Contributor #3](URL/Email)
### Contributing
If you are interested in contributing to this project, please see our:
* [Code of conduct](doc/repository/code-of-conduct.md)
* [Contributing guidelines](doc/repository/contributing.md)
* [Testing procedures](doc/repository/testing.md)
* [Issue template](doc/repository/issue-template.md)
* [Pull request template](doc/repository/pull-request-template.md)
### Built with
* [Built with #1](URL)
* [Built with #2](URL)
* [Built with #3](URL)
### Acknowledgements
* [Acknowledgements](doc/repository/acknowledgements.md)
* [Third-party notices](doc/repository/roadmap.md)
### Project files
* [Development notes](doc/repository/development-notes.md)

# ADDITIONAL INFORMATION
### RELATED PROJECTS
* [Related project #1](URL)
* [Related project #2](URL)
* [Related project #3](URL)
### ADDITIONAL READING
* [Additional reading #1](URL)
* [Additional reading #2](URL)
* [Additional reading #3](URL)

***

<!-- DEVELOPMENT FOOTER -->
[![Developed by](https://img.shields.io/badge/developed%20by-a%20pretty%20cool%20program-17806D.svg)](https://aprettycoolprogram.com)&nbsp;[![Feedback](https://img.shields.io/badge/feedback@aprettycoolprogram.com-17806D.svg)](mailto:feedback@aprettycoolprogram.com)&nbsp;[![GitHub](https://img.shields.io/github/followers/aprettycoolprogram.svg?label=GitHub&style=social)](https://github.com/aprettycoolprogram)&nbsp;[![Twitter](https://img.shields.io/twitter/follow/aprettycoolprog.svg?label=Twitter&style=social)](https://twitter.com/aprettycoolprog)&nbsp;<br>
[![Repository built using](https://img.shields.io/badge/repository%20built%20using-a%20pretty%20cool%20repository%20template-17806D.svg)](https://github.com/APrettyCoolProgram/repository-template/tree/master)