---
hide:
  - toc
---
#　<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> 環境構築

## 5. Expo CLIのインストール

!!! Note
    アプリケーションを開発する上で便利なものでフレームワークと言われるものがあります。
    このフレームワークとは、アプリケーションやシステムを開発するために必要な機能があらかじめ用意された枠組みのことです。
    このJavaScriptフレームワークの1つであるReact Nativeを使用すると、効率よくiOS、Androidのアプリケーションを同時に開発することができます。<br>
    そのReact Nativeの開発環境となるのがExpoです。


1.Expoをインストール

```
$ npm install expo-cli --g
```

2.EAS CLIをインストール

```
$ npm i -g eas-cli
```

3.EASアカウントでログイン

  - アカウントはEASアカウントを作成する必要があります
  - **※ログインは必ず必要ではありませんが、iOSをExpo Go上で動かす場合は必要になるケースが多いです**

```
$ eas login 
```