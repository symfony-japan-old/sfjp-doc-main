---
layout: default
title: A week of symfony #200 (25->31 October 2010)
---

A week of symfony #200 (25->31 October 2010)
============================================

Symfony 公式ブログで毎週公開される、Symfony 関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony 本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/10/31/a-week-of-symfony-200-25-31-october-2010)）

<br />
<br />
<hr />
 
先週は、Output Escaper コンポーネントが大幅にリファクタリングされ、Propel バンドルが独立したバンドルへ移されました。また、<a href="http://docs.symfony-reloaded.org/master/guides/cache/http.html">Symfony2 の HTTP キャッシュのドキュメント</a>が公開されました。


開発メーリングリスト
-------------------

  * [Symfony の DIC におけるコンテキスト](http://groups.google.com/group/symfony-devs/browse_thread/thread/cded44241c728e8b)
  * [Remember Me 認証を Security コンポーネントに組み込みたい](http://groups.google.com/group/symfony-devs/browse_thread/thread/fbe83d11a7ab9aa8)
  * [レイアウトへの変数の追加](http://groups.google.com/group/symfony-devs/browse_thread/thread/bec5185f48e8cc0a)
  * [_format マジック変数を有用にする提案](http://groups.google.com/group/symfony-devs/browse_thread/thread/ff702eccdd787e8b)
  * [[Doctrine2] 継承の問題](http://groups.google.com/group/symfony-devs/browse_thread/thread/2fdb3540f8df974f)


symfony 1 開発ハイライト
------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=31%2F10%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r31247](http://trac.symfony-project.org/changeset/31247 "31247 revision on trac"): \[1.3, 1.4\] sfFilesystem の mbstring problem に関連する問題を修正
  * [r31248](http://trac.symfony-project.org/changeset/31248 "31248 revision on trac"): \[1.3, 1.4\] sfI18nModuleExtract.class.php がメッセージソースとして常にファイルを仮定している問題を修正
  * [r31250](http://trac.symfony-project.org/changeset/31250 "31250 revision on trac"): \[1.3, 1.4\] WDT で不足していた情報を追加
  * [r31253](http://trac.symfony-project.org/changeset/31253 "31253 revision on trac")、[r31254](http://trac.symfony-project.org/changeset/31254 "31254 revision on trac"): \[1.3, 1.4\] WDT の挿入処理を修正


sfDoctrinePlugin:

  * [r31249](http://trac.symfony-project.org/changeset/31249 "31249 revision on trac"): \[1.3, 1.4\] Swift_DoctrineSpool のメモリリークを修正



アクティビティーの概要: チェンジセット 58、バグレポート 13、修正されたバグ 15、クローズされた改善 3、報告されたドキュメントの不具合 5、修正されたドキュメントの不具合 1、編集されたドキュメント 11


Symfony2 開発ハイライト
-----------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [6885f90](http://github.com/symfony/symfony/commit/6885f90f17597d9519f44d2b3986664c5703a232 "6885f90f17597d9519f44d2b3986664c5703a232 commit on github"): \[HttpKernel\Security\] use ステートメントを修正し、コンストラクタのパラメータを修正
  * [3463f47](http://github.com/symfony/symfony/commit/3463f47698fe028029bbff964773a1fbe2ee16c4 "3463f47698fe028029bbff964773a1fbe2ee16c4 commit on github"): バイナリデータの 16 進表現の代わりに直接 base64 エンコードを適用するように修正
  * [1d5ca49](http://github.com/symfony/symfony/commit/1d5ca4910dffd8b07df677d6c9d61b69d9d53c65 "1d5ca4910dffd8b07df677d6c9d61b69d9d53c65 commit on github"): \[FrameworkBundle\] ide 設定のコンフィギュレーションをリファクタリング
  * [e111652](http://github.com/symfony/symfony/commit/e1116524ed79cf118568e2c124f546d596a562c0 "e1116524ed79cf118568e2c124f546d596a562c0 commit on github"): \[WebProfiler\] WDT の表示を修正
  * [c065be8](http://github.com/symfony/symfony/commit/c065be88b56d3df7463a2d7f940c7885eb390661 "c065be88b56d3df7463a2d7f940c7885eb390661 commit on github"): \[OutputEscaper\] コンポーネントをリファクタリング
  * [e23c3cc](http://github.com/symfony/symfony/commit/e23c3cc702223612c82fa001a12e136e6ef945bb "e23c3cc702223612c82fa001a12e136e6ef945bb commit on github"): \[OutputEscaper\] __call() でエスケープ戦略を変更する場合の一貫性を維持できるように getEscaper*() メソッドを修正
  * [c448429](http://github.com/symfony/symfony/commit/c448429e62f8ff411ffec67f03e873eb81af8ea0 "c448429e62f8ff411ffec67f03e873eb81af8ea0 commit on github"): \[HttpFoundation\] HTTP ヘッダーの日付フォーマットを修正 (フォーマットは RFC2822 ではなく RFC1123 に従う必要がある)
  * [7e6bdde](http://github.com/symfony/symfony/commit/7e6bddedf90319a3e27c3a14b4f6753e38f96007 "7e6bddedf90319a3e27c3a14b4f6753e38f96007 commit on github"): \[TwigBundle\] Form エクステンションの初期化を、可能な限り後で行うように修正 (パフォーマンスを改善するため)
  * [2b613f3](http://github.com/symfony/symfony/commit/2b613f34d57bc1cdb9bf626ac905e734fdf3c023 "2b613f34d57bc1cdb9bf626ac905e734fdf3c023 commit on github"): \[FrameworkBundle\] SafeDecorator でのラップが不要になったので削除
  * [3eee458](http://github.com/symfony/symfony/commit/3eee458430e2a918594b41cdbf8be8142fb907db "3eee458430e2a918594b41cdbf8be8142fb907db commit on github"): \[OutputEscaper\] JS escaper を Twig のものへ置き換え
  * [13f36b1](http://github.com/symfony/symfony/commit/13f36b165778acff165e1f7a4356a2ab784c625c "13f36b165778acff165e1f7a4356a2ab784c625c commit on github"): 二重エスケープを回避するためのロジックを削除
  * [88d30f0](http://github.com/symfony/symfony/commit/88d30f0d7496cf5f60a74827ca54c2b072cd1647 "88d30f0d7496cf5f60a74827ca54c2b072cd1647 commit on github")、[b9f33a6](http://github.com/symfony/symfony/commit/b9f33a610ee956647d3321cebac621abf97d1313 "b9f33a610ee956647d3321cebac621abf97d1313 commit on github"): Propel バンドルを削除 (独立したバンドルへ移動)



> **NOTE**
> 翻訳者コメント<br />
> Symfony2 はまだまだ本体に大きな修正が入る状況ですね。公式サイトでは [HTTP Cache のドキュメント](http://docs.symfony-reloaded.org/master/guides/cache/http.html)が公開されました。
> [DEV ML](http://groups.google.com/group/symfony-devs/) では、Symfony2 を使った開発に関する議論なども出てきていますので、Symfony2 ではどういった書き方をするのか知りたい方は、DEV ML の方もチェックしてみると面白いと思います。
> [hidenorigoto]

