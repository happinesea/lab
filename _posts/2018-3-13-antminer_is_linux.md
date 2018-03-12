---
layout: post
title: AntminerはLinux
description: 届いたAntminerをさっそく動かしてみたところ、やっぱりLinuxでした。
tags: ec happinsea mining
image: assets/images/the_firs_miner.jpg
---
専用マシンだろうかなんだろうか、こういったものは必ず何かしらのOSで動いています。

WEBページ経由で管理するので、必ずHTTPサーバは動いています。<br>

好奇心でsshでつないでみたら、なんとroot/adminで入りました！<br>
コマンドで覗いてみ、やっはり、最低限なサービスしか入っていないLinuxですね。<br>

httpサーバはお馴染みのapacheではなく、lighttpdです。<br>
ステータスなどはshで作られたcgiで結果を返しています。<br>
直接cgiをたたいてもちゃんと結果は返しています。<br>

外部ツールで死活監視はふつうのHTTPサーバの通信を確認する形でで行けそう。<br>
チップの温度はcgi経由でも取れそう。<br>
ただし、minerStatus.cgiから、いろんなデータは詰められているので、解析は必要です。
