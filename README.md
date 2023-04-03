# Automatic Alcohol Dispenser with Infrared Thermometer

> 2022.05.31
> This is the project of EECS Interdisciplinary Experiment
> with team member of 4 people.

## 簡介 Introduction

主要利用Arduino以及Esp8266，並結合UART、MG996r伺服馬達、紅外線測溫器等器材，製作一台自動酒精噴霧機，並搭配額溫感測器和播放語音提醒。


### 操作流程 Operation Process

1. 當設備架設連結好後，網頁此時代表機器未開啟(machine-stateoff)，點擊ON即可啟動機器，啟動機器後，MP3 player 播放「machine is on」的聲音。
   ![](https://i.imgur.com/m5qfAiJ.png)
2. 啟動機器後，將額頭靠近溫度感測器，測量額溫，並同時將手靠近酒精瓶與紅外線感測模組，當小於一定距離時，啟動馬達按壓酒精瓶，噴出酒精，進行手部消毒，感測器有防誤觸功能，必須待在感測器前一定時間才會有反應。
3. 測量額溫後，若是額溫小於 37.5 度，LCD則顯示「save 與 溫度」，並播放體溫正常之音效，若是額溫大於 37.5 度，LCD則顯示「fucking high 與 溫度」，並播報語音提醒側後者。
4. 使用完畢，機器呈現開啟狀態(machine–stateon)，點擊OFF即可關閉機器，關閉機器後，播報語音關機提示。
   ![](https://i.imgur.com/xVZc6YY.png)

### 流程圖 Flow Chart

![](https://i.imgur.com/BsTJNLT.png)