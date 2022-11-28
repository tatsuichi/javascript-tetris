## はじめに
JavaScriptの勉強のためにテトリスを自作しました。

## ルール
基本的なルールは、[テトリス - Wikipedia](https://ja.wikipedia.org/wiki/%E3%83%86%E3%83%88%E3%83%AA%E3%82%B9)を参考にさせて頂きました。
回転のルールは、[テトリス学入門 - メモ帳](https://null-mn.hatenablog.com/entry/2019/12/13/065412)を参考にさせて頂きました。

![回転イメージ](/img/回転イメージ.png) 

## 構成
+ index.html

index.htmlのみ、sytleもJavaScriptもhtmlに記載しました。
jQueryは使用しない方針としました。装飾はせず素のままです。

## 動作環境
+ Windows 10 64bit
+ Chrome 107

## 開発環境
+ Windows 10 64bit 
+ VS Code

## 開発メモ
+ 基本、[MDN Web Docs](https://developer.mozilla.org/ja/)で調べました。
+ 配列同士の重複判定は[配列同士で重複する値があるか確認する | きるこの日記帳](https://www.dkrk-blog.net/javascript/duplicate_an_array)を参考にさせて頂きました。
+ htmlのフォーマットは「shift + alt + F」でできる。結構、便利。
+ ネットで「JavaScript　テトリス」を調べるとたくさんのサイトがでてきますが、完成するまで見ないようにしました。
  普通なら、こんなやり方やらないよね、といったソースコードになっているかもしれません。
+ 落ち切ったテトリミノ（ブロック）の位置を、どうやって管理するか悩みました。
  座標位置を文字列配列で保持することにしました。そのため、文字列操作が基本となります。
  (e.g. フィールドの左上を1-1（1行1列）として、array=['20-1','20-2', '20-3', '20-4'])
+ 回転処理は愚直に座標を変換することで対応しました。（もっと良い方法ありそう、そもそも文字列管理が良くない!?）

![回転座標](/img/回転座標.png)
![座標変換一覧](/img/座標変換一覧.png)