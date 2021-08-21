---
title: ITA vs COVID bot
date: 2021-01-10 13:40:32
tags:
  - covid
  - italy
  - telegram
  - bot
---

## Preamble

Impossible not to know what the coronavirus emergency is for the world. And the subsequent need for mass vaccination. So let\'s move on ...


## Introduction

ITAvsCOVID ([@itavscovidbot](https://t.me/itavscovidbot)) is a telegram bot that download [official data](https://github.com/italia/covid19-opendata-vaccini) about vaccination campaign in Italy to gives you information on the status of vaccines and calculate a prediction about when everything could end.

![alt-text][screenshot_v1]

The data (which are sent daily or only on request) concern the number of daily new vaccinated and the percentage of total number of people vaccinated compared to the famous herd immunity.
In addition, the calculation that estimates the number of days missing from achieving herd immunity is calculated by considering the percentage missing from achieving 80% of the vaccinated population.


## Thanks
I have to thank [@MarcoBuster](https://github.com/MarcoBuster) because the idea for this bot came to me after seeing his project _[quanto-manca](https://github.com/MarcoBuster/quanto-manca)_. And the charts source code was taken directly from this public project.


## Update: version 2 

After the first few months it is necessary to differentiate people who received the partial vaccination from people who received the full vaccination course.

In the second version this differentiation has been added and all calculations are reasonably based on the number of people who received the full vaccination.

![alt-text][screenshot_v2]


## Links

<table>
<tr>
    <td>Source Code</td>
    <td><a href="https://github.com/derogab/ITAvsCOVIDbot" target="_new">https://github.com/derogab/ITAvsCOVIDbot</a></td>
</tr>
<tr>
    <td>Telegram Bot</td>
    <td><a href="https://t.me/itavscovidbot" target="_new">https://t.me/itavscovidbot</a></td>
</tr>
</table>



[screenshot_v1]: /image/linked-to/ITA-vs-COVID-bot/screenshot1.png "Screenshot of ITAvsCOVIDbot first version"
[screenshot_v2]: /image/linked-to/ITA-vs-COVID-bot/screenshot2.png "Screenshot of ITAvsCOVIDbot second version"
