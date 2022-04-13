# VFC Dashboard - A Getting Started Example:
This example will guide you step by step through the VFC Dahsboard functionalities. You will create a simple but dynamic dashboard that shows the status of your three (simulated) machines that you already connected to Mindsphere. You will learn the essential nodes for dashboarding with the VFC and will be able to extend your dashboard according to your own needs. The Dashboard you create will look like this:

![dashboard_image](./doc/overview.png)

# Prerequisites:
- around 120 minutes of time
- Visual Flow Creator
- Asset Manager
- basic javascript knowledge is helpful, but not required
> All required applications and resources are part of a [Start for free](https://siemens.mindsphere.io/en/start) tenant. You can follow along this tutorial regardless of your mindsphere package.

# Setup:
We will simulate three different versions of an industrial machine:
- Basic
- Performance
- Eco

This step requires you to be familiar with Mindsphere's asset structure and can create new aspect and asset types. If this sounds like a big headache to you, please visit the [Asset Manager Tutorial](https://siemens.mindsphere.io/en/docs/tutorials/asset-manager) first.

If not, please follow the [Setup Instructions](./Setup/readme.md) and come back once you completed the process.

# Overview Dashboard:
Start by creating a new flow and name it something like *Dashboard* or *MyFirstDashboard*. Then switch to the dashboard tab under Layout, which will be blank for now.

![dashboard_menu](./doc/dashboard_menu.png)

Here you can structure the basic layout of your dashboard using tabs and groups. A tab is the equivalent of a dashboard page. You can assign different content to each tab and it will then only be displayed on that that. Each tab will display your content in groups, which act like columns. For example, a structure that you created under *Tabs & Links* looks like this:

![tab_structure](./doc/tab_structure.png)

then the corresponding dashboard page would be organized as shown below:

![tabs_groups](./doc/tabs_groups.png)


