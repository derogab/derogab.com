---
title: Hide YouTube Shorts
date: 2023-02-05 19:20:00
tags:
  - youtube
  - shorts
  - ublock
---

## Introduction

YouTube is a popular online video-sharing platform where users can upload, share, and view videos. To get the most out of YouTube, it\'s important to know how to find and watch videos, subscribe to channels, and interact with the community.

YouTube Shorts is a new feature on YouTube that allows users to create short videos using multi-segment camera footage and creative tools. 

## The problem

The Shorts have distorted the original version of YouTube bringing it towards a type of content that nobody wants to see on YouTube. 

It could certainly be interesting and entertaining to view also this type of content, but on different platforms, for example [Waveful](https://invites.waveful.app/EKYC). Not on YouTube.

The excessive amount of Shorts videos, who often prioritize clicks over substance, has also cluttered the following-channels page and made it hard to reach real videos with actual content.


## The solution

There is a very simple trick to go back to the \'Old YouTube\' without Shorts, at least on the web version. Here a quick tutorial:

1. Install [uBlock Origin](https://github.com/gorhill/uBlock) in your browser.

2. In uBlock Origin Settings, add these filters:
```
www.youtube.com##ytd-guide-renderer a.yt-simple-endpoint path[d^="M10 14.65v-5.3L15 12l-5 2.65zm7.77-4.33c-.77-.32-1.2-.5-1.2-.5L18"]:upward(ytd-guide-entry-renderer)
www.youtube.com##ytd-mini-guide-renderer a.yt-simple-endpoint path[d^="M10 14.65v-5.3L15 12l-5 2.65zm7.77-4.33c-.77-.32-1.2-.5-1.2-.5L18"]:upward(ytd-mini-guide-entry-renderer)
www.youtube.com##ytd-browse #dismissible ytd-rich-grid-slim-media[is-short]:upward(ytd-rich-section-renderer)
www.youtube.com##ytd-browse[page-subtype="home"] .ytd-thumbnail[href^="/shorts/"]:upward(ytd-rich-item-renderer)
www.youtube.com##ytd-browse[page-subtype="subscriptions"] .ytd-thumbnail[href^="/shorts/"]:upward(ytd-grid-video-renderer)
www.youtube.com##ytd-search .ytd-thumbnail[href^="/shorts/"]:upward(ytd-video-renderer)
www.youtube.com##ytd-watch-next-secondary-results-renderer .ytd-thumbnail[href^="/shorts/"]:upward(ytd-compact-video-renderer,ytd-shelf-renderer)
www.youtube.com##ytd-browse[page-subtype="subscriptions"] ytd-video-renderer .ytd-thumbnail[href^="/shorts/"]:upward(ytd-item-section-renderer)
www.youtube.com##ytd-browse[page-subtype="channels"] #contents.ytd-reel-shelf-renderer:upward(ytd-item-section-renderer)
www.youtube.com##ytd-search #contents ytd-reel-shelf-renderer
m.youtube.com##ytm-reel-shelf-renderer
m.youtube.com##ytm-pivot-bar-renderer div.pivot-shorts:upward(ytm-pivot-bar-item-renderer)
m.youtube.com##ytm-browse ytm-item-section-renderer ytm-thumbnail-overlay-time-status-renderer[data-style="SHORTS"]:upward(ytm-video-with-context-renderer)
m.youtube.com##ytm-browse ytm-item-section-renderer ytm-thumbnail-overlay-time-status-renderer[data-style="SHORTS"]:upward(ytm-compact-video-renderer)
m.youtube.com##ytm-search ytm-thumbnail-overlay-time-status-renderer[data-style="SHORTS"]:upward(ytm-compact-video-renderer)
m.youtube.com##ytm-single-column-watch-next-results-renderer ytm-thumbnail-overlay-time-status-renderer span:has-text(/^(0:\d\d|1:0\d)$/):upward(ytm-video-with-context-renderer)
```

Note that these filters have been copied from [this source](https://letsblock.it/filters/youtube-shorts). One day, with YouTube updates, it may need to be changed and updated accordingly. But let\'s enjoy it as long as it works!


## Links

<table>
<tr>
    <td>Reddit Thread</td>
    <td><a href="https://www.reddit.com/r/uBlockOrigin/comments/m9znll/hide_youtube_shorts_from_video_lists/" target="_new">Hide youtube shorts from video lists</a></td>
</tr>
<tr>
    <td>uBlock Origin - Source Code</td>
    <td><a href="https://github.com/gorhill/uBlock" target="_new">GitHub Repository</a></td>
</tr>
<tr>
    <td>uBlock Origin - Browser Extension</td>
    <td>
        <a href="https://addons.mozilla.org/addon/ublock-origin/" target="_new">Firefox</a> -
        <a href="https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm" target="_new">Chrome</a> -
        <a href="https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak" target="_new">Microsoft</a> -
        <a href="https://addons.opera.com/extensions/details/ublock/" target="_new">Opera</a>
    </td>
</tr>
<tr>
    <td>Source of Filters</td>
    <td><a href="https://letsblock.it/filters/youtube-shorts" target="_new">Hide Youtube #Shorts</a></td>
</tr>
</table>
