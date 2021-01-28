# Visual Flow Creator Examples

[![The MDL License](https://img.shields.io/badge/license-MDL-009999.svg?style=flat)](./LICENSE.md)
[![Documentation](https://img.shields.io/badge/mindsphere-documentation-%23009999.svg)](https://opensource.mindsphere.io/docs/mindconnect-nodejs/index.html)
[![Forum](https://img.shields.io/badge/mindsphere-community-%23009999.svg)](https://community.plm.automation.siemens.com/t5/Developer-Space/bd-p/MindSphere-platform-forum)


## Example Overview

Current examples in this repository for Visual Flow Creator (VFC):

| Name | Description | Complexity Rating | Prerequisites |
| --- | --- | --- | --- | --- |
|[Creation of custom API endpoints](./createCustomEndpoint/readme.md) | | :star: | |
|[Command MQTT devices connected via IoT Extension](./commandMqttDevice/readme.md) | | :star: :star: | |
|[Generate sample data](./generateSampleData/readme.md) | | :star: | |
|[Create rule for asset type](./createRuleForAssetType/readme.md) | | :star: | |
|[Virtual machine simulator](./virtualMachineSimulator/readme.md) | | :star: | |

## Prerequisites
All application examples shown in this respository require the *Visual Flow Creator* MindSphere Application. 
To use them, ensure that
- VFC is available in your MindSphere tenant ([VFC in MindSphere Store](https://www.dex.siemens.com/mindsphere/applications/visual-flow-creator))
![image](./MindSphere_Launchpad_VFC.png)
- you have *admin* or *user* access to VFC ([VFC user role settings](https://documentation.mindsphere.io/resources/html/visualflow-creator/en-US/108812512779.html))
![image](./VFC_roles.png)

If you can see Visual Flow Creator on your Launchpad, you're ready to start developments. 

## Import of Examples
To import any of the examples shown in this repository, launch the VFC. In the menu, select *Import* and paste the JSON template as found in the application examples. 
Drop the nodes in the editor and save the just imported flow.  
![image](./How_To_Import.gif)

