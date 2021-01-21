# Command device via MQTT

This flow demonstrates how you can use Visual Flow Creator to trigger sending of a command to a device connected to MindSphere via IoT Extension. 
Every time the flow is triggered, the command specified in the payload is send to the device linked using the device-ID.

![image](./doc/commandMqttDevice.png)

## Prerequisites
- [access to Visual Flow Creator](xxx)
- [access to IoT Extension](xxx)

## Setup & Configuration

### Setup in IoT Extension
1. Connect a device to IoT Extension
2. Issue VFC credentails for IoT Extension access

### Setup in Visual Flow Creator
1. Import the flow in Visual Flow Creator
2. Adjust the payload body in the function node
    - specify device-ID as found in IoT Extension
    - set the command
4.  Save the flow 

:cloud: :heavy_check_mark: You're ready to command a device once the flow is triggered - enjoy!


## Result


## See also
- [Device Control for IoT Extension](https://cumulocity.com/guides/reference/device-control/)
- [Integrate an MQTT Device via IoT Extension](https://developer.mindsphere.io/howto/howto-mqtt-mciot.html)
- [:shopping_cart: MindSphere Store: Visual Flow Creator](https://www.dex.siemens.com/mindsphere/applications/visual-flow-creator?viewState=DetailView&cartID=&portalUser=&store=&cclcl=en_US)
- [:shopping_cart: MindSphere Store: IoT Extension](mindsphere.io/store)







