---
title: Instagram doesn't encrypt stories
date: 2017-05-22 23:12:47
tags:
  - instagram
  - ssl
  - tls
---

## Preamble
This article was copied from an old blog I had opened with a friend. It does not fully reflect the style and content of my blog, but I did not want this work to be lost.

## Introduction
After the rise of Snapchat, the _stories_ also invaded the most used social in the world: Facebook (and Messenger), Instagram, and WhatsApp.

The main reason for the success of stories is that content disappears after just 24 hours.

But is not so.

**Nothing disappears from the internet.** Or not when we believe it.

In particular I analyzed Instagram and I found out that..

## Instagram is not safe
Unfortunately, Instagram stories are not downloaded to your smartphones using an encrypted connection.
In this way **anyone can have access to your stories, even if you have a private profile**.

Any man-in-the-middle, connected to the same network as your friend (for example, in university, in a bar or any other public wifi), could intercept your stories as soon as he opens Instagram.

As a result, **this person could do whatever he wants with your content**. He can save them, publish them or else.

## Seeing is believing
To analyze this fact I did a _sniffing_ with [Wireshark](https://www.wireshark.org/).

see [Wikipedia](https://en.wikipedia.org/wiki/Packet_analyzer)
> A packet analyzer (also known as a network analyzer, protocol analyzer or packet sniffer—or, for particular types of networks, an Ethernet sniffer or wireless sniffer) is a computer program or piece of computer hardware that can intercept and log traffic that passes over a digital network or part of a network.

To intercept my friends\' stories I connected the computer and the smartphone to the same wifi network. Then I opened Wireshark.

_I saw all my network data that was not encrypted._

At this time I opened Instagram and clicked on my friend\'s story.

![alt text][story_img]

After that I searched for the [HTTP](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) requests that WireShark had sniffed from the net and **I found the resources corresponding to the stories I had looked at on the smartphone!**

![alt text][sniffing]

For the most experienced..
The data obtained with WireShark containing the stories was like this
GET /codes_numbers.jpg HTTP/1.1 for images
GET /codes_numbers.mp4 HTTP/1.1 for videos

So I could find the _full request URI_ containing the direct link to the contents.

![alt text][img_analysis]
![alt text][img_content]

## Self-destruction
In the following days I kept the contents under control and I could verify that the images and videos were deleted only after 3 days.

## Alternative Stories\' Apps
The procedure is not applicable with Snapchat, Facebook and Whatsapp because they use an encrypted protocol: [TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security).

## Video demo
<iframe width="100%" height="355" src="https://www.youtube-nocookie.com/embed/jHUwCL9oRbQ?rel=0&amp;showinfo=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Disclaimer
Article for information purposes. I take no responsibility for misuse of the information obtained from this article.

## Update
After some updates of the app it seems that **this bug has been fixed**.



[story_img]: /image/linked-to/Instagram-doesn-t-encrypt-stories/img00_ok.jpg "Image in the stories"
[sniffing]: /image/linked-to/Instagram-doesn-t-encrypt-stories/img01_ok.png "Sniffing"
[img_analysis]: /image/linked-to/Instagram-doesn-t-encrypt-stories/img02_ok.png "Content Analysis"
[img_content]: /image/linked-to/Instagram-doesn-t-encrypt-stories/img03_ok.png "Content Image"