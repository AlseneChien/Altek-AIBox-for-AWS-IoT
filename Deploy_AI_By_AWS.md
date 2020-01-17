
How to deploy AI model to AIBox by AWS
===
---

# Table of Contents

-   [Introduction](#Introduction)
-   [Part 1: Config ...](#part_1)
-   [Part 2: Create your ... for AIBox](#part_2)
-   [Part 3: Config your ... Device](#part_3)
-   [Part 4: Deploy to your AIBox](#part_4)
-   [Part 5: Tutorials and Examples](#part_5)


<a name="Introduction"></a>
# Introduction

**About this document**

This document describes how to cover your AI Models, then deploy models to your AIBox via AWS GreenGrass.

<a name="part_1"></a>
# Part 1: Config ...

## 1.1 Active your AWS account

AIBox can be configured to work with AWS. To get started, you will need a new or existing AWS account. You can create a free account by visiting [AWS link](https://aws.amazon.com/)

## 1.2 Setup IoT ... and ... Device

To Be Updated

<a name="part_2"></a>
# Part 2: Create your ... Module for AIBox

To Be Updated

- Sample code

```

```



<a name="part_3"></a>
# Part 3: Config your ...

To Be Updated

<a name="part_4"></a>
# Part 4: Deploy to your AIBox

You can follow below steps to deploy modules to AIBox

To Be Updated

<a name="part_5"></a>
# Part 5: Tutorials and Examples

Power on your AIBox, then wait for status LED as below before further actions

![](./images/AIBoxLED_1.png)

## 5.1 Connect your AIBox with PC via Wi-Fi
At your PC side, please connect to a Wi-Fi network, named as altek_edgebox**** (**** is the last 4 characters of the device’s Wi-Fi MAC address, e.g. altek_edgebox9613). Then, you can follow step 1.1 or 1.2 to redirect AIBox network to Wi-Fi AP or Ethernet router. Password of AIBox AP is "12345678"

![](./images/Pc_network.png)

<a name="part_5_2"></a>
## 5.2 Direct your AIBox to a Wi-Fi AP (internet available for Azure)

Open web browser (e.g. Chrome) by link http://192.168.143.1/ to  AP setting webpage. 
Then, input SSID/Password for one internet-available Wi-Fi AP. AIBox nework will be redirected to your assigned Wi-Fi AP.

![](./images/ap_webpage1.png) 

After setting, wait for AIBOX to connect to Wi-Fi AP. Status LED will show as below onec internet is ready.

![](./images/AIBoxLED_2.png)

<a name="part_5_3"></a>
## 5.3 Config your IPCamera via Web UI

Power on you IPCameras. If you have ever config relative setting as ["5.3.2"](#part_5_3_2), AIBox will collect camera streaming automatically. (You can ignore ["5.4.1"](#part_5_3_1) an ["5.4.2"](#part_5_3_2) if your IPCameras have been paired with AIBox already)

<a name="part_5_3_1"></a>
### 5.3.1 View preview at Web UI
Once Wi-Fi connecting successfully, it will redirect to AIBOX IPC preview/config webpage (http://192.168.143.1:9080)

At IPC preview/configure webpage, all Onvif IPCs are scanned and listed. And you can press "Refresh“ to scan again.

You have to input username/password for Onvif IPCamera  to login. To simplify operating scenarios, all IPCameras’ account recommend be identical. Then, click camera link which you perfer start preview at web

 ![](./images/ap_webpage5.png)

<a name="part_5_3_2"></a>
 ### 5.3.2 Config your display out via Web UI
You have to config your display out via Web UI

![](./images/TVOut_config1.png)

Click "Reflash" to scan avaialble IPCameras, then enable x1~x4 cameras as below

Remember to click "Save". After saving configuration, AIBox will reconnect cameras automatically while AIBox boot-up next time.

![](./images/TVOut_config2.png)

## 5.4 Update ....
To Be Updated

## Wait for your moduel deployment

Please wait for minutes, depending on internet througput, to complete modules download from AWS to AIBox.

You can check by below cmd via SSH

```

```


## 5.5 Inference running at AIBox

Please confirm your IPCameras have been connected with AIBox before AI running

If IPCamera connection is ready, NETWORK LED status will show as below. And video analytic for AI will be run automatically once model is deployed

![](./images/AIBoxLED_3.png)

If IPCamera connection is not ready, refer to ["5.3 Config your IPCamera via Web UI"](#part_5_3_2) to connect IPCameras and AIBox

To Be Updated