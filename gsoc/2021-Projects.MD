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

**Responsible:** Doc Squad

### COBOL Programming Course

#### Update the Getting Started Course content to reflect updates from sister projects (ZOWE)

#### Implement some key strategic issues that have been brought forward by the community

#### Improve the Advanced Topics chapter of the course.
