# Suricata QRadar app

This QRadar app was made for visualizing data parsed by [DSM module](https://github.com/tink0mar/suricata-dsm)

Repository content:
 - **xkozak18.pdf** - the full text of the technical report with appendices.
- **qradar-suricata-addon/** - folder with the application for the QRadar system in two versions
- **qradar-suricata-addon/qradar-suricata-flask** - application for QRadar
- **qradar-suricata-addon/suricata-flask** - flask application for development version

How to install?

To install the DSM module and the application, you need to have QRadar available in a community version on the server or locally. The community release must be version 7.3. Please save the current version of QRadar before starting the installation.

# DSM module installation

The module can be installed from the included SD card or from the [repository](https://github.com/tink0mar/suricata-dsm). Once downloaded, you need to run the Extension Manager, upload the zip file and start the installation.

# Installing the QRadar app

To install QRadar app, you need to download the zip file from this repository. The file then needs to be uploaded via the QRadar REST API using the endpoint: 

**verb|POST /gui_app_framework/application_creation_task|**

To upload the file correctly, you need to send the downloaded file with the query and wait until the application is installed. If the installation fails, the previous version of QRadar must be restored. The only option left is to install the application via the [App Editor](https://exchange.xforce.ibmcloud.com/hub/extension/5d0f3f37cc5c4d16ccafe9d40d8dffe5). The application is installed in the same way as the DSM module via the extension manager. Once the application is installed and opened, a dialog box is displayed in which the option to install an existing application must be selected. 

If neither of these options works, it is possible to use a second version of the application available in the same repository in the **suricata-flask** folder, where the development version is placed. 

To get accesses in the application, you have set up token and url in **rest_apy.py**. One relates to the URL for the QRadar system and the other relates to the authorization token that can be created in the QRadar system. The application can then be run in a virtual environment.



