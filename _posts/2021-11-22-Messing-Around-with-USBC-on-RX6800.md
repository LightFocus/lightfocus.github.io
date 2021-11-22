---
layout: post
title:  "Messing around with USBC on RX 6800"
author: lightfocus
categories: [ Hardware ]
tags: [ Gear ]
image: "https://www.amd.com/system/files/2020-10/579976-amd-radeon-6800-1260x709.png"
---

With the release of the AMD RX 6800 series, we finally have USB Type-C support on AMD GPU while macOS added the support for Rx 6800 series in 11.4.

If you're using RX 6800 as previous AMD cards in Hackintosh, namely config WhateverGreen, you'll find it works as expected. One problem is obviously the USB Type-C port on the back can only be used as a video output and power output.

To find out why, I took a look at my PCIe devices list.

<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/usbc/Screen%20Shot%202021-11-22%20at%205.08.05%20PM.png">

As we can see, in the devices that are under vendor name AMD, we sure can find something like the USB controller.
But if we check out the USB controller section, we can only see the one that's provided by the motherboard.

For now, it's pretty clear that Apple didn't do a great job "supporting" this card. This card works as expected, built-in USB controller can be detected, however, macOS failed to pair it with a normal USB controller, instead, it's paired with AppleAMDUSBXHCIPCI.

<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/usbc/Screen%20Shot%202021-11-22%20at%205.02.44%20PM.png">

To solve this prolem, I grabed a copy of XHCI-unsupported.kext and modified it into forcing use AppleUSBXHCISPT.

<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/usbc/Screen%20Shot%202021-11-22%20at%209.12.58%20PM.png">

By doing so, we're able to see a new USB controller in Hackintool.

<img src="https://lightfocus-1256547063.cos.ap-hongkong.myqcloud.com/posts/usbc/Screen%20Shot%202021-11-22%20at%209.15.55%20PM.png">

And with test, I can confirm that the data function of USB is working correctly on that port.