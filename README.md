# IFTTT Maker Channel SocketIO Server

HerokuでNodeJS(Express)をベースにした、IFTTT Maker ChannelとMilkcocoaが連携するサーバーです。

IFTTT Maker ChannelでのHTTP通信をMilkcocoaの特定のデータストアに連絡します。また、Milkcocoaの特定のデータストアに送られたデータをIFTTT Maker Channelに送ります。

## Heroku Button

以下のHeroku Buttonを押してHerokuアプリを作成しましょう。

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/1ft-seabass/heroku-ifttt-maker-channel-milkcocoa)

## 参考記事

* [Heroku | Introducing Heroku Button](https://blog.heroku.com/archives/2014/8/7/heroku-button)

## はじめの値の設定方法

* IFTTT_SECURITY_KEY
    * IFTTT Maker Channelへ送る際に必要なセキュリティキー
* MILKCOCOA_APP_ID
    * MilkcocoaのアプリID
* IFTTT_RECEIVE_DATASTORE_ID
    * IFTTTがMilkcocoaにデータを送る時のMilkcocoaデータストア
        * 初期値：IFTTTReceiveData
* IFTTT_RECEIVE_URL
    * IFTTTがMilkcocoaにデータを送る際の中継URL
        * 初期値：/ifttt/receive
* IFTTT_SEND_DATASTORE_ID
    * MilkcocoaからIFTTTにデータを送る時のMilkcocoaデータストア
        * 初期値：IFTTTSendData
* IFTTT_SEND_EVENT_NAME
    * MilkcocoaからIFTTT Maker Channelにデータを送る時のIFTTT Maker Channelイベント名
        * 初期値：IFTTTSendData
* IFTTT_SEND_URL
    * MilkcocoaからIFTTTにデータを送る時の中継URL
        * 初期値：/ifttt/send