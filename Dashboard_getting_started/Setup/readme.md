# Setup steps for the getting started VFC Dashboard:
This short tutorial will show you how to set up the assets and the data generator for the VFC dashboard example.

# Asset Setup
We want to create an Asset Type **VFC_Dashboard_Machine** as a **Core.BasicAsset**:

![Asset_type](../doc/asset_type.png)

with three Aspects assigned to the Aseet type:
- Dashboard_Machine_Location [Static]
- Dashboard_Machine_Sensor [Dynamic]
- Dashboard_Machine_Status [Dynamic]

To do this, please follow the following steps:
- [x] Setup static Aspect type Dashboard_Machine_Location with the variables:
  - latitude [DOUBLE]
  - longitude [DOUBLE]
  - Software_Version [STRING, 32]
