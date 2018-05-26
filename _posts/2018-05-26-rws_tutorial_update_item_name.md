---
layout: post
title: rws-libチュートリアル：商品名を一括変更
description: rws-lib
tags: rws-lib tutorial happinsea
image: assets/images/rakuten-item-name-change.png
---
rws-libは楽天のWEB APIを操作するライブラリです。<br>
今回は、商品名称を一括変更のチュートリアルを実行する方法を紹介します。<br>

SEOの一環として、毎月のスーパーセールや、お買い物マラソンなど、クーポンを発行する期間中に、<br>
商品名称に「クーポン」や、「ポイントUP」などのキーワードをつけると、ユーザに伝わりやすいといわれています。<br>
<br>
もちろん、RMSのCSV登録を利用する方法は一般かもしれませんが、<br>
毎月1万円ぐらいかかるわけですから、中小の店舗だと、やはり、負担を感じるでしょう。<br>

happinesea labは無料で商品名称を一括変更する方法を紹介します。<br>
<br>

+ 実行する前に、rws-lib-tutorialのソースコードを落としてください。
https://github.com/happinesea/rws-lib-tutorial

勿論、gitでも落とせますが、よくわからない方は、直接zipファイルをダウンロードして、<br>
解凍して使ってください。

+ ダウンロードできたら、適当なところに解凍して、実際のディレクトリに移動してください。
<br><img src="http://lab.happinesea.com/assets/images/rakuten-item-name-change/1.png" width="500px">

+ テキストエディタで、以下のファイルに「<license key>」と「<service secret>」を、実際のRMSのWEB APIの設定に書き換えてください。<br>
勿論、テスト店舗を持っている場合、先にテスト店舗で動作確認しておくのがベストです。<br>
「src/main/groovy/com/happinesea/TutorialChangeItemNameBatch.groovy」<br>
<br><img src="http://lab.happinesea.com/assets/images/rakuten-item-name-change/2.png" width="500px">

+ 続いて、置換用文字列の編集をします。<br>
25行当たり、newStrとregexの変数に、新たに置換される文字列と、置換する箇所を指定します。<br>
尚、デフォルトでは、誤って変えてしまわないように、逆に設定しています。<br>
例えば、商品名の先頭に、「[最大2000円OFFクーポン]」をつけたい場合、以下画像のように、書き換えてください。<br>
イベントが終了して、商品名を戻したい場合、ソースコードをもとに戻して、もう一回実行すればよいです。
<br><img src="http://lab.happinesea.com/assets/images/rakuten-item-name-change/3.png" width="500px">

+ 準備作業の最後、商品のURLを指定してください。

こちらは<a href="https://chrome.google.com/webstore/detail/copytables/ekdpkppgmlalfkphpibadldikjimijon" target="_blank">Chrome copytables</a>のようなプラグインを使ったほうがやりやすいと思います。<br>

+ 上記の準備はでき上げれば、以下のコマンドを実行して、更新します。
<pre>
 gradlew launch -Pmain=com.happinesea.TutorialChangeItemNameBatch
</pre>
<br><img src="http://lab.happinesea.com/assets/images/rakuten-item-name-change/4.png" width="500px">


商品名称を一括変更するチュートリアルの説明はこれで以上となります。<br>
なるべく分かりやすく説明しようとしていますが、gradleなど経験のない一般の方には、中々ハードルが高いかもしれません。<br>
ご不明や、質問などありましたら、下のコメント欄に聞いてください。<br>
