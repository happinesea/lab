---
title: rws-libのプロジェクトページです。
layout: post
description: '楽天ペイAPI(RakutenPayOrderAPI)を含めて、RWS(RMS WEB SERVICE)の通信データをGroovy/Javaから扱いしやすいためのライブラリーです'
image: assets/images/pic07.jpg
nav-menu: true
---

## About rws-lib
rws-libは名前通り、楽天のEC店舗管理向け、RWS(RMS WEB SERVICE)のAPI連携用ライブラリです。<br>
もともとRWS向けのJava系のライブラリは少なく、ちょうどう、楽天の受注関連のAPIは仕様変更のきっかけで、RWS向けのオープンソースオブジェクトを立ち上げました。<br>
<br>
SOAP時代から、楽天本家から、Java向けのライブラリを提供していたが、古すぎるところもあるし、物足りないです。<br>
このプロジェクトは、直接店舗向けの商品を出すつもりがないが、RWSのAPI連携の際に、共通と思われる課題を解決するためのライブラリとの位置づけにしたいと思います。<br>

RWSのAPI連携ツールを開発する方は多くいます。<br>
開発者の工数を1人日でも短縮、開発を少しでも楽にできたらと思い、rws-libの成果物を自由に使ってください。<br>
こちらに対して支払いなど必要ないが、かわりにバグの報告だけ、ご協力していただければと思います。

## Feature

<ul>
<li>0.0.4
  <ol>
    <li>RMS web API、Wowma APIを特化したXMLパーサーフレームワーク</li>
    <li>RMS web APIを特化したJSONパーサーフレームワーク</li>
    <li>RMS web API、Wowma APIを特化したAPI通信フレームワーク/li>
    <li>RMS商品マスタのCSVファイル出力フレームワーク/li>
    <li>商品タイトルの一括変更ためのライブラリの用意</li>
  </ol>
</li>
</ul>


## Installation

最新のリリースモジュールは<a href="https://maven-badges.herokuapp.com/maven-central/com.happinesea/rws-lib" target="_blank"><img src="https://maven-badges.herokuapp.com/maven-central/com.happinesea/rws-lib/badge.svg"></a>に登録しますので、Gradleの場合、以下のように依存関係を設定すればよいです。<br>

<pre>
repositories {
    mavenCentral()
}
dependencies {
    compile 'com.happinesea:rws-lib:&lt;バージョン番号&gt;'
}
</pre>

Gradle以外ビルドフレームワークの場合、<a href="https://maven-badges.herokuapp.com/maven-central/com.happinesea/rws-lib" target="_blank"><img src="https://maven-badges.herokuapp.com/maven-central/com.happinesea/rws-lib/badge.svg"></a>をご参考してください。


## Documentation

[Groovy docs](http://lab.happinesea.com/docs/rws-lib/0.0.3/groovydoc/)<br>
[Guides and Tutorials](https://github.com/happinesea/rws-lib-tutorial)(作成中)
