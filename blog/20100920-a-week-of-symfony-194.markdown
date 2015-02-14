---
layout: default
title: A week of symfony #194 (13->19 September 2010)
---

A week of symfony #194 (13->19 September 2010)
==============================================

Symfony 公式ブログで毎週公開される、Symfony 関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony 本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/09/19/a-week-of-symfony-194-13-19-september-2010)）

<br />
<br />
<hr />

先週は Symfony2 PR3 が公開され、じきにリリースされる Symfony2 アルファバージョンへ一歩近づきました。
また、Symfony\Framework 名前空間は削除され、Symfony\Component\HttpKernel と Symfony\Bundle\FrameworkBundle へコードが移動されました。
 
開発メーリングリスト
--------------------

  * [Symfony2: Admin ジェネレーター](http://groups.google.com/group/symfony-devs/browse_thread/thread/d0a19513d6cd8148/11d3f231ed3c07d5)
  * [フィールドのレンダリングにテンプレートを使用 -- コンセプトの検証](http://groups.google.com/group/symfony-devs/browse_thread/thread/fb5fb9732cf5fc1e/df4e1a8131f931aa)
  * [Symfony2 用のフォームフレームワークの完成へ向けて手伝ってくれる方を募集](http://groups.google.com/group/symfony-devs/browse_thread/thread/c4b9586115736fe6/b6ccd29642250a49)

symfony 1 開発ハイライト
------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=19%2F09%2F2010&amp;daysback=6&amp;milestone=on&amp;ticket=on&amp;changeset=on&amp;update=Update):

  * [r30894](http://trac.symfony-project.org/changeset/30894 "30894 revision on trac"): \[1.3, 1.4\] sfWebRequest::isSecure() のテストカバレッジを向上
  * [r30896](http://trac.symfony-project.org/changeset/30896 "30896 revision on trac"): \[1.3, 1.4\] パス情報配列のリセットをうまく行うようにテストを更新
  * [r30900](http://trac.symfony-project.org/changeset/30900 "30900 revision on trac"): \[1.3, 1.4\] リクエストがセキュアなページからフォワードされた場合の getUriPrefix() を修正
  * [r30912](http://trac.symfony-project.org/changeset/30912 "30912 revision on trac"): \[1.3, 1.4\] ビュークラスのオーバーライドを修正
  * [r30915](http://trac.symfony-project.org/changeset/30915 "30915 revision on trac"): \[1.3, 1.4\] "image/x-ms-bmp" MIME タイプのサポートを追加


sfDoctrinePlugin:

  * [r30901](http://trac.symfony-project.org/changeset/30901 "30901 revision on trac"): \[1.3, 1.4\] Doctrine で生成したテーブルクラスのコメント削除処理をリバート



アクティビティ要約: チェンジセット 36、バグレポート 10、バグフィックス 11、ドキュメントの変更 5


Symfony2 開発ハイライト
-----------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [61f1866](http://github.com/symfony/symfony/commit/61f18667f4d1c924824bace22ca1cbccfdd6c70b "61f18667f4d1c924824bace22ca1cbccfdd6c70b commit on github"): \[Console\] コマンドショートカットのテストをいくつか追加
  * [7734f44](http://github.com/symfony/symfony/commit/7734f44bc55bf13780dd0c56d1c73fa5365aefdb "7734f44bc55bf13780dd0c56d1c73fa5365aefdb commit on github"): \[Process\] Process:isSucessful() メソッドを追加
  * [1990fc5](http://github.com/symfony/symfony/commit/1990fc543b9629f91328846a5d8c2905baba4ce3 "1990fc543b9629f91328846a5d8c2905baba4ce3 commit on github"): \[HttpKernel\] ControllerResolver に Closure のサポートを追加
  * [d657adb](http://github.com/symfony/symfony/commit/d657adbfa20878ca27ddc069ff5ba1e9904df931 "d657adbfa20878ca27ddc069ff5ba1e9904df931 commit on github"): Symfony\Framework を削除し、Symfony\Component\HttpKernel と Symfony\Bundle\FrameworkBundle へ移動。カーネル設定の名前空間は削除され、メインのウェブ設定名前空間へマージ。

ドキュメント
------------

  * <a href="http://trac.symfony-project.org/wiki/HowToConnectToMSSQLServer">MSSQL サーバーへの接続方法Server</a> ページの更新


Symfony に関するブログ
----------------------

  * [海外でも通用するエンジニアになる](http://el.jibun.atmarkit.co.jp/kaigaiengineer/2010/09/i18nsymfony-d3f.html)




> **NOTE**
> 翻訳者コメント<br />
> Symfony2 の PR3 がリリースされ、日本の PHP ユーザーの間でも、ちらほらと Symfony2 を試している方がいらっしゃるようです。
> また、fabien さんからは Symfony2 を利用した Sinatra ライクなフレームワークである「[Silex](http://github.com/fabpot/Silex)」がリリースされています。
> Silex を作る上で必要になった要素などが、Symfony2 の機能として追加されたりしています（コントローラーをクロージャーで実装できる機能など）<br />
> symfony 1系も多少フィックスが行われていますので、そろそろ 1.4.7 がリリースされるかもしれません。
> [hidenorigoto]

