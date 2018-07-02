---
layout: post
title: 楽天のWEBAPIも、やはり制限が多いですね。
description: 楽天のWEBAPIも、やはり制限が多いですね。一括編集は有料？！
tags: rws-lib tutorial happinsea ec
image: 
---

商品の詳細API「item.get」から、詳細な商品情報を取得しようとして、<br>
いつもAuthErrorで、失敗してしまう現象が発生していました。<br>

カスタマーサポートに確認したところ、一括更新するには、別途申請が必要とのことです。<br>
https://mainmenu.rms.rakuten.co.jp/auth/index.phtml?params=navi3/item/03_051.html&s=&param2=0


普通は有料のオプションの代わりに、自らツールを作って、賄いたかったが、<br>
楽天店舗の管理を効率化しようとして、楽天に追加料金で支払わなくてはならないことをみえてきました。<br>


rws-libの当初の目的の一つは、基本料金以外、無料の枠の業務効率化で、一括商品変更や、在庫管理のツールを<br>
開発したかったが、制限が多いことで、今の開発をそろそろ終了させたいと思います。


ただし、rws-libのコアな部分のXMLパーサーは、かなり優れているので、<br>
これから楽天のWEBAPI関連の開発を行う技術者の皆さんに、力になればと思います。
