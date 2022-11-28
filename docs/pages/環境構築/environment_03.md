---
hide:
  - toc
---
#　<i class="fa fa-arrow-circle-right" aria-hidden="true"></i> 環境構築

## 3. Gitの設定
### 1. インストール※Windowsのみ

!!! Note
    Gitとは、ファイルのバージョン管理が簡単にできるツールです。<br>
    特徴は、「ファイルの変更履歴を管理」、「過去のファイルに戻せる」、「チームで共有できる」ことです。
    プログラマーにとっては、多くのコードを編集した上で何か不具合が起きたときに、元のバージョンへ戻すことはよくあることです。そういった際のファイルの管理を効率よく行えるのがGitです。
  

1. [ダウンロードを行う](https://gitforwindows.org/)

    <img src="../../../images/環境構築/windows/Git_020.png"/>

2. インストーラ実行<br>

    <img src="../../../images/環境構築/windows/Git_001.jpeg"/>

1. インストーラ実行<br>
    
    <img src="../../../images/環境構築/windows/Git_002.jpeg"/>

1. インストールディレクトリ選択<br>

    <img src="../../../images/環境構築/windows/Git_003.jpeg"/>

1. インストールコンポーネント選択<br>

    <img src="../../../images/環境構築/windows/Git_004.jpeg"/>

1. StartMenu設定<br>

    <img src="../../../images/環境構築/windows/Git_005.jpeg">

1. デフォルトエディタを選択（ここではVSCを設定）<br>

    <img src="../../../images/環境構築/windows/Git_006.jpeg"/>

1. ブランチ設定<br>

    <img src="../../../images/環境構築/windows/Git_019.png"/>

1. PATH環境を設定<br>

    <img src="../../../images/環境構築/windows/Git_007.jpeg"/>

8. SSH接続の設定<br>

    <img src="../../../images/環境構築/windows/Git_016.png"/>

8. HTTPS接続の設定<br>

    <img src="../../../images/環境構築/windows/Git_008.jpeg"/>

9. 改行コードの設定<br>

    <img src="../../../images/環境構築/windows/Git_009.jpeg"/>

10. ターミナル・エミュレータの設定<br>

    <img src="../../../images/環境構築/windows/Git_010.jpeg"/>

11. git pullの設定<br>

    <img src="../../../images/環境構築/windows/Git_017.png"/>

11. マネージャーの設定<br>

    <img src="../../../images/環境構築/windows/Git_018.png"/>

11. 拡張オプションの設定<br>

    <img src="../../../images/環境構築/windows/Git_011.jpeg"/>

12. ベータ版機能の有効化設定<br>

    <img src="../../../images/環境構築/windows/Git_012.png"/>

1.  インストール中<br>
    
    <img src="../../../images/環境構築/windows/Git_013.jpeg"/>

1.  完了<br>

    <img src="../../../images/環境構築/windows/Git_014.jpeg"/>

1.  コマンドプロンプトから確認<br>

    <img src="../../../images/環境構築/windows/Git_015.jpeg"/>

        $ git --version

### 2. アカウント設定を行う

    $ git config --global user.name "i-r.aiura-vsc"
    
    $ git config --global user.email "i-r.aiura@valuenet.co.jp"
