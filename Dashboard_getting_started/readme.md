# VFC Dashboard - A Getting Started Example:
This example will guide you step by step through the VFC Dahsboard functionalities. You will create a simple but dynamic dashboard that shows the status of your three (simulated) machines that you already connected to Mindsphere. You will learn the essential nodes for dashboarding with the VFC and will be able to extend your dashboard according to your own needs. The Dashboard you create will look like this:

![dashboard_image](./doc/overview.png)

# Prerequisites:
- around 120 minutes of time
- Visual Flow Creator
- Asset Manager
- basic Javascript knowledge is helpful, but not required
> All required applications and resources are part of a [Start for free](https://siemens.mindsphere.io/en/start) tenant. You can follow this tutorial along regardless of your Mindsphere package.

# Setup:
We will simulate three different versions of an industrial machine:
- Basic
- Performance
- Eco

This step requires you to be familiar with Mindsphere's asset structure and that you can create new aspects, assets and asset types. If this sounds like a big headache to you, please visit the [Asset Manager Tutorial](https://siemens.mindsphere.io/en/docs/tutorials/asset-manager) first.

If not, please follow the [Setup Instructions](./Setup/readme.md) and come back once you completed the process.

# Dashboard Structure:
Start by creating a new flow and name it something like *Dashboard* or *MyFirstDashboard*. Then switch to the dashboard tab under Layout, which will be blank for now.

![dashboard_menu](./doc/dashboard_menu.png)

Here you can structure the basic layout of your dashboard using tabs and groups. A tab is the equivalent of a dashboard page. You can assign different content to each tab and it will then only be displayed on that that. Each tab will display your content in groups, which act like columns. For example, a structure that you created under *Tabs & Links* like this:

![tab_structure](./doc/tab_structure.png)

the corresponding dashboard page would be organized as shown below:

![tabs_groups](./doc/tabs_groups.png)

Inside a group (column), the dashboard content is structured vertically, from top to bottom. If you assigned three items to a single group on a single tab like this:

![group_structure](./doc/group_structure.png)

the corresponding dashboard page would be organized as shown below:

![groups_content](./doc/groups_content.png)

As you can see, *Group 1* is centered automatically on the tab. You don't have to worry about the position of your groups, Mindsphere does that automatically for you. Just remember the following rule of thumb:

> **Tabs** are **individual dashboard pages**. You can only view one tab at once.

> **Groups**, that are structured from **top to bottom**, will be displayed from **left to right** on your dashboard page.

> **Content**, that is structured from **top to bottom**, will be displayed from **top to bottom** inside a group.

Now let's start building the overview dashboard:
- Create a tab and name it *Overview*
- Under *Overview*, create three new groups
- Rename these groups to *Selector*, *Asset Map* and *Info*
- Remember the way the VFC is displaying groups. You want to place the *Selector* group on the left and the *Info* group on the right

You can rename tabs and groups by hovering over them and clicking the *edit* button:

![group_edit](./doc/group_edit.png)

Now create a second tab called *Detail* with only one group named *Events*. We will use the *Detail* tab at the very end of this tutorial, so consider this a little teaser.

# Overview Dashboard:
In this chapter, we will bring some life and functionality to our Overview dashboard. This tutorial is designed to build all elements from scratch and simultaneously show the logic behind a VFC dashboard. Some steps might be overcomplicated with the purpose of demonstrating several VFC nodes.

> If you just want to check out the final result, you can copy paste the [Json Flow Data From Here](./Resources/Dashboard.json). It will import all elements, including nodes, tabs and groups. Remember to adjust all *read-timeseries* and *write-timeseries* nodes to your own assets.

For the beginning, we will place three *text* nodes and three *button* nodes in the flow. This will be our Asset selector, where each machine has it's own button like below:

![asset_selector](./doc/selector.png)

But before styling our nodes, we have to adjust the width of the group. Click *edit* on the *Selector* group and give it a width of 9. Rearrange your nodes in the flow, so that the *text* nodes are alternating with the *button* nodes, starting with the text node. Double click the first *text node* to open it's properties. Here you can assign the node to a group and change it's apperence. We will start with our Basic machine. Copy the following setting:

![text_node_settings](./doc/text_node.png)

So we assigned the *text* node to our *Selector* group, gave it a form of 6x2 (width x height) and chose the: <br> *label* **value** (left aligned)<br> format, where *label* = Asset: and **value** = Basic. This text is static and will not change depending on the input.<br> Now rinse and repeat for the other two *text* nodes, but remember to change the **value** to Performance and Eco.

Now apply the following settings to the three *button* nodes:

![button_nodes_settings](./doc/button_node.png)

The positioning of nodes in the flow is not relevant for the structure of the dashboard. By organizing your flow, you will have a huge benefit once it get's complicated, but the order of the nodes under the *Selection* group is decisive. The check, which node in the group is the corresponding node in the flow, just hover over it. The node in the flow will be bordered red:

![check_nodes](./doc/check_nodes.png)

Your flow should look like this:

![flow_actual](./doc/flowpic_1.png)

Now you want to switch to your dashboard and view your progress. The *Selection* group of the dashboard should look like this:

![Selection_actual](./doc/dashpic_1.png)

>Hint: You can open your dashboard by clicking *Open dashboard in new tab*. Here, you can also reload all dashboards to apply changes made to the flow model.
>
>![how_to_open_dashboard](./doc/open_dashboard.png)

The next step is to implement a map, where you can see the location of the asset you chose in the *Selector* group. Mindsphere offers some pre-build nodes, that reflect the Mindsphere look and feel and can be implemented into your VFC dashboards. You find them in the *MDSP Dashboard* node section. There is a date picker, timeseries chart, asset list, aspect variable selector, event table and the Mindsphere Map. But first, change the *Asset Map* group width to 122. Now drop the *MDSP Map* and another *text* node into your flow, assign them to the *Asset Map* group (the *MDSP Map* node is positioned below the *text* node)  and configure them as follows:

![map_text](./doc/map_text.png)

![MDSP_Map](./doc/map.png)

Maybe you have noticed that we already set initial position and zoom level for the *MDSP Map* node. Feel free to alter the position to your company's headquarters and experiment with the zoom level. Furthermore, the **value** of the *text* node is {{msg.name}}. We want to display a dynamic text which changes depending on your selection in the *Selector* group. The text node will check the incoming message to have a msg.name property and will display it`s value. Changing the text according to the selected Asset is great, but we want to display the stored location of this asset in the map too.

> You can change the initial position of the *MDSP Map* by sending a payload with {{latitude, longitude, zoomLevel}
