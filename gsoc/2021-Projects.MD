![](https://github.com/openmainframeproject/artwork/blob/master/projects/mentorship/mentorship-color.svg)

# Proposed Projects for the Mentorship Project

Projects proposed for the Google Summer of Code.

## Potential Project Status

### Zowe

#### Graphical awareness of UIs in the API Catalog

**Problem:** Logging onto the API Gateway takes the user to the API Catalog which shows a set of tiles for registered API 
services. The API Mediation layer can also have UIs registered. Base Zowe has four UIs registered (ZLUX, MVS Explorer, 
USS Explorer, JES Explorer) and Zowe conformant plugins can (and do) introduce their own. The URLs to launch these is 
/ui/v1/pluginId. Unless a user knows of their existence they may not use these.

**Solution:** Provide a way for registered UIs to be visible on the API Gateway. On the API Gateway homepage there could 
be a link to the UI services (similar to the link for the catalog) and the list of services could allow linking into each 
of the registered UIs.

**Responsible:** API ML Squad

#### Graphical visualization of the Extensions and Plugins in the API Catalog

The Zowe CLI, Zowe App Server as well as the Zowe API Mediation Layer support plugins and extensions. There is at the 
moment no visualization of the installed ones. The API Catalog is a logical place that could contain these information. 

**Responsible:** API ML Squad 

#### Patch to the Linux PAX project to understand the headers properly

At the moment it isn't possible for us to use the Linux PAX to distinguish whether specific files stored within PAX are
encoded in ASCII or EBCDIC despite the PAX format containing the information. The goal here is to update the linux pax
to properly read and provide the metadata on the encoding. 

**Responsible:** Web UI Squad

#### Improve starting of the app server 

At the moment the App server doesn't wait for the API Mediation Layer to be fully started. As such there are lots of
confusing messages in the Spool around the App server being unable to register to the API Mediation Layer. The goal
is to use the API provided by the API Mediation Layer to wait with registration and full startup untill the API Mediation 
Layer is started. 

**Responsible:** Web UI Squad

#### Slack integration to Zowe

Allow a user to create a slack channel to their mainframe and ask questions, e.g. "Is my job finished" or "Is task ABCD 
still running", ... Slack communicates using Zowe CLI commands and a text to command language parser creates the calls, 
e.g. Watson AI assistant

**Responsible:** Systems Squad

#### GitHub PR integration for manual testing simplification. 

When a PR is being reviewed have an integrated powerup that allows the ability to build and deploy a Zowe system, and to 
log onto it, so the user can do some testing and verification of the environment and manual testing, without having to 
manually download, install and do manual test. When the PR is merged the environment is torn down.

**Responsible:** Systems Squad

#### ML data analysis to recognize potential security breaches.

**Responsible:** API ML Squad

#### Improve the Zowe doc site generator and UI 

Zowe docs consist of several high-level sections such as Getting Started, User Guide, Extending, etc. Due to the limitation of the Vuepress (current site generator) sidebar depth, the sidebar or navigation experience is not satisfactory. Also most open source docs now provide a three column layout and many other social functions such as Share. The goal is to provide a good and more industry-standard doc navigation experience for the Zowe doc site with better UI and functions that engage users.  A new site generator can be explored.

### Create ZSS Zowe CLI Plugin
ZSS is a HTTP server written in Metal C, its part of zowe, and provide some very useful API for ZLUX, and otherwise. It would be greate if we can build a CLI plugin for ZSS, this way ZSS can be executed from thick client like desktop as well. ZSS has ability to get and update USS files, datasets, and some useful api like reset system password etc. It would be great to have it as CLI Plugin.

**Responsible:** WebUI Squad

#### Zowe toolkit plugin for IntelliJ IDEA

 This proposal is for creating a common library and set of Zowe plugins for IntelliJ IDEA, leveraging API ML for access to z/OS resources and services.

 IntelliJ IDEA is one of the most popular integrated development environments among software developers. It is best known for its Java variant, but there are also options for Kotlin, JavaScript, Python, PHP and others. All these environments are built on same platform and plugins developed for one can be used in any of the other variants (subject to specific module dependencies/independencies).

 Currently Zowe features several client applications for access to Zowe Mainframe resources - Zowe CLI for scripting, zLUX for web access, and several plugins for VS Studio Code for graphical desktop access to MF resources and services. While these tools cover wide range of use cases, when it comes to individual developer's taste/choice of tool, the users are limited to a single one for the purpose. Developers, however, are often reluctant to change their favorite IDE or to use multiple IDEs simultaneously to be able to do their work. This consequently slows down or eventually even prevents the Zowe adoption.

 Here in we propose to develop a set of Zowe plugins for the  IntelliJ family of development environments. This will ensure uniform user experience, while adding the possibility to work in their favorite development environment. The plugins will share a common foundation to interface with the IntelliJ platform SDK and to access the Zowe resources through Zowe API ML. 

 Currently there exists Zowe plugin for IntelliJ IDEA, which was created during previous Broadcom innovation weeks as a PoC and is not a production grade SW. The plugin allows to access single mainframe LPAR/security domain and to work with datasets and JOBs. This plugin can be used as a foundation for future development. 
 The following features can constitute the roadmap of the IDEA plugin development:

 1. Create a library which interfaces the IntelliJ IDEA platform specifics in order to minimize dependencies to IntelliJ SDK changes.
 2. Create (optionally interface with existing) REST client library handling API ML specifics using token security.
 3. Create layer/library with routines to handle API ML security requirements, i.e. handle authentication options and security flows implemented by API ML, namely utilize API ML /Zowe tokens for access to API ML.
 4. Create a simple sample plugin based on the libraries above.
 5. Implement token lifecycle client side routines - login/logout/refresh/revoke etc.
 6. Allow for multiple connections to different LPARs/Sysplex environments. 
 7. Build foundations / create UI framework for simultaneous visualization and control of multiple MF systems.
 8. Implement the most important foundational Zowe Explorer APIs like datasets and Jobs access.
 9. Add more plugins similar to the Visual Studio Code Zowe plugin/s.
 10. Extend the plugin set with additional plugins empowered by using APIs of specific MF products.

 The high level capabilities list above can be used to subtract a number of concrete tasks to be accomplished in the course of the OMF/Zowe mentorship program. Items 1. to 4. provide sufficient scope and it can be trimmed down if necessary.

**Responsible:** Doc Squad

#### Quick search in mainframe data sets and files from VS Code

**Problem:** Searching in files is a typical activity during software development. VS Code makes it very easy to find files that contain a given string or match a regular expression. But searching of mainframe data sets, members, or files is not easy. Even locating a member in a large library is difficult. Searching by content is not possible.  

**Solution:** The goal is to provide a similar interface to VS Code for searching in data sets and files. It will be possible to locate a dataset, member, or file by name and by content. As a part of the implementation, the internal Zowe Client SDK will be extended. New Zowe CLI for search will be created too.

**Responsible:** Explorer Squad

### COBOL Programming Course

#### Update the Getting Started Course content to reflect updates from sister projects (ZOWE)

#### Implement some key strategic issues that have been brought forward by the community

#### Improve the Advanced Topics chapter of the course.
