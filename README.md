# Scala Basic
目的：
プログラミング初学者やScala言語初学者が
言語処理をScala言語で始める前に、
Scala言語に慣れるために、
Jupyter Notebook上でScalaの対話型評価環境REPL（Read-eval-print loop）を体験します。
（ついでに、Jupyter Notebook上でR言語も実行してみます。）

## 環境構築
OSがWindowsの場合はVMWareを起動してUbuntu上に開発環境を作成します。
OSがMac, Ubuntu, CentOSなどUNIXの場合はVMWareなしで開発環境を作成します。

OSがWindowsの場合は、WMWareをインストールして、Ubuntuを作成してください。

次の文書では、「VMware Player 7」をWindows 7にインストールする方法が書かれています。
最新版の「VMware Workstation 12.5.0 Player」も方法は大体同じです。  
http://okuzawats.com/ubuntu-on-vmware-20150605  
VMware Workstation 12.5.0 Playerダウンロードページ  
https://my.vmware.com/web/vmware/free#desktop_end_user_computing/vmware_workstation_player/12_0|PLAYER-1250|product_downloads
---
ここからはWindows以外のOSとWindows上のUbuntuと共通の作業。

次のページからOracle Java 8 JDKをダウンロードしてインストールしてください。  
http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html  
「Java SE Development Kit 8u102」の「Accept License Agreement 」にチェックを入れて、開発環境のOSと対応するダウンロードのリンクをクリックしてください。

Scalaをインストールしてください。  
http://www.scala-lang.org/  
トップページにあるダウンロードボタンをクリックしてください。（OSがUnixの場合は、MacPortsやapt-getなどからインストールできるかもしれません）

***ここまででも今回の内容の基本的なところは扱えます。***

Python 3をインストールしてください。（OSがUnixの場合は、MacPortsやapt-getなどからインストールできるかもしれません）  
https://www.python.org/downloads/  

Jupyter Notebookをインストールしてください。（OSがUnixの場合は、MacPortsやapt-getなどからインストールできるかもしれません）  
http://jupyter.readthedocs.io/en/latest/install.html

Jupyter Scalaをインストールしてください。  
https://github.com/alexarchambault/jupyter-scala  
```
curl -L -o jupyter-scala https://git.io/vrHhi && chmod +x jupyter-scala && ./jupyter-scala && rm -f jupyter-scala
```

R言語をインストールしてください。（OSがUnixの場合は、MacPortsやapt-getなどからインストールできるかもしれません）  
https://www.r-project.org/

IRKernelをインストールしてください。  
https://github.com/IRkernel/IRkernel  
注意）jupyterとjupyter-kernelspecにパスを通しておかないとインストールできません。

## 今後のための環境構築
IntelliJ IDEA  
Community Editionは無料ですが、有償のUltimate Editionも学生なら「JetBrains Products for Learning」に申請すると無料で使用できます。  
「JetBrains Products for Learning」  
https://www.jetbrains.com/shop/eform/students  
Scalaプラグインをインストールしてください。

Bitbucket  
プライベートリポジトリ用のバージョン管理サイト  
https://bitbucket.org  
アカウントを作成してください。  
SSHの鍵を生成して、公開鍵をサイトに登録しましょう。

GitHub  
公開リポジトリ用のバージョン管理サイト  
https://github.com/  
アカウントを作成してください。  
SSHの鍵を生成して、公開鍵をサイトに登録しましょう。

Git  
バージョン管理ソフト  
コマンドラインから実行する場合は、次のページからインストールしてください。  
https://git-scm.com/book/ja/v1/%E4%BD%BF%E3%81%84%E5%A7%8B%E3%82%81%E3%82%8B-Git%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB

GUIから実行する場合は、
SourceTreeかGitHub Desktopをインストールしてください。

SourceTree  
https://ja.atlassian.com/software/sourcetree  

Github Desktop  
https://desktop.github.com/

## 日本語処理のためのソフト
MeCab  
UTF-8 only modeでインストールしてください。  
http://taku910.github.io/mecab/

MeCab辞書  
IPA 辞書、Juman 辞書、Unidic 辞書を全てインストールしてください。

mecab-ipadic-NEologdをインストールしてください。  
https://github.com/neologd/mecab-ipadic-neologd/blob/master/README.ja.md

CaboCha  
UTF-8 only modeでインストールしてください。  
https://taku910.github.io/cabocha/

Juman  
http://nlp.ist.i.kyoto-u.ac.jp/index.php?cmd=read&page=JUMAN&alias%5B%5D=%E6%97%A5%E6%9C%AC%E8%AA%9E%E5%BD%A2%E6%85%8B%E7%B4%A0%E8%A7%A3%E6%9E%90%E3%82%B7%E3%82%B9%E3%83%86%E3%83%A0JUMAN

KNP  
http://nlp.ist.i.kyoto-u.ac.jp/?KNP

## 全文検索のためのソフト
Indri  
https://sourceforge.net/projects/lemur/

Solr  
http://lucene.apache.org/solr/

## 分散処理のためのソフト
UIMA-ASのためのApache ActiveMQ  
http://activemq.apache.org/download.html

RaSC  
https://alaginrc.nict.go.jp/rasc/ja/

Spark  
http://spark.apache.org/

## テストのためのソフト（SBTでプロジェクトごとにインストールします）
ScalaTest  
http://www.scalatest.org/

JUnit  
http://junit.org/junit4/

## コマンドラインアプリのためのソフト（SBTでプロジェクトごとにインストールします）
args4j  
http://args4j.kohsuke.org/

## Configのためのソフト（SBTでプロジェクトごとにインストールします）
Ficus  
https://github.com/iheartradio/ficus
