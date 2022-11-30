---
hide:
  - toc
---
#　<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> 環境構築

## 4. npmのインストール

!!! Note
    Webページ作成などの際に使われるJavaScript言語の実行環境にNode.jsというものがあります。<br>このNode.jsの様々なプログラムを管理することができるのがnpmです。

### Windowsの場合
??? インストール方法

    1.[インストールを行う](https://github.com/nullivex/nodist/releases)

    <img src="../../../images/環境構築/windows/Nodist_007.png"/>
    
    2.インストーラ実行<br>
    <img src="../../../images/環境構築/windows/Nodist_001.jpeg"/>

    2.インストーラ起動<br>
    <img src="../../../images/環境構築/windows/Nodist_002.jpeg"/>

    3.利用規約を許諾<br>
    <img src="../../../images/環境構築/windows/Nodist_003.jpeg"/>

    4.インストールフォルダを選択<br>
    <img src="../../../images/環境構築/windows/Nodist_004.jpeg"/>

    5.インストール中<br>
    <img src="../../../images/環境構築/windows/Nodist_005.jpeg"/>

    6.完了<br>
    <img src="../../../images/環境構築/windows/Nodist_006.jpeg"/>

    ・コマンドプロンプトからNodistのインストールを確認 ※表示されない場合は、一度ウインドウを閉じて再実行してください<br>

        $ nodist -v
        0.9.1

    ・指定のNode.jsバージョンを取得しインストール<br>

        $ nodist + v14.3.0
        $ nodist v14.3.0

    ・インストールされたNode.jsとNPMのバージョンを確認する<br>

        $ node -v
        v14.3.0
        $ npm -v
        6.9.0

### MacBookの場合
??? インストール方法
        
    * * *

    1.nodebrewをインストール

        $ brew install nodebrew

    * * *

    2.インストールしたnodebrewのバージョンを確認。バージョンが確認できればOK
    
        $ nodebrew -v

        nodebrew 1.0.1
        ~

    * * *

    3.nodeをインストールを

        $ nodebrew install-binary v14.3.0

    * * *

    4.使用するnodeのバージョンを設定

        $ nodebrew use v14.3.0

    * * *

    5.nodeにパスを通す

        $ echo 'export PATH=$HOME/.nodebrew/current/bin:$PATH' >> ~/.zprofile
        $ source ~/.zprofile

    * * *

    6.`npm -v`を実行しバージョンを確認。`v14.3.0`と表示されていればOK

        $ npm -v

        v14.3.0
