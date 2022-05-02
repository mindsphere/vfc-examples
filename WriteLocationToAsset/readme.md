# How to write location data directly to your Asset using the Asset Management API

How to use this flow:
- Copy the json flow structure from [Here](./IMPORT_WriteLocationToAsset.json)
- Click Import in the VFC and paste the json data in the blank field
- Click Import
- Change the asset id's in the GET and PUT call to the id of your own asset
- Change the locational information by altering the body in the function node (optional)
- Save the flow

You are done! Your flow should now look like this:

![image](https://user-images.githubusercontent.com/90254123/166233405-ead98700-e29d-4f24-b1a2-54699fbd7572.png)

If you execute the flow, your location is written directly to your assets static information. You can now use it in e.g. the Asset Manager and always check the current location of your Asset:



https://user-images.githubusercontent.com/90254123/166235568-542ba4b4-f1ab-4f04-8ea0-b8f044007429.mp4

You do not have to write all information (e.g. postal code, street address, country, ...) for the map to be functional. Writing longitude and latitude is sufficient. However, if you only sent longitude and latitude information, Asset Manager will show *now location available*. 

> Take a look at the [MindSphere Documentation](https://documentation.mindsphere.io/MindSphere/apis/advanced-assetmanagement/api-assetmanagement-api.html) if you want to know more about the Asset Management API.
