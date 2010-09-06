A week of symfony #192 (30 August -> 5 September 2010)
======================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/09/05/a-week-of-symfony-192-30-august-5-september-2010)）

<br />
<br />
<hr />

今週 Symfony2 の新しいWebプロファイラーバンドルが紹介されました。 SymfonyプロファイラーはWebデバッグツールバーをより強力にしたもので、どのフレームワークよりも詳細なデバッグ情報を提供してくれます。

(訳者追記: スクリーンキャプチャと説明についてはhttp://symfony-reloaded.org/toolsを参照)

開発メーリングリスト
----------------------

- [GitHub Pull Requests 2.0 と Symfony](http://groups.google.com/group/symfony-devs/browse_thread/thread/636c059a6000b3a3)
- [Propel のミラーサーバーの UUID](http://groups.google.com/group/symfony-devs/browse_thread/thread/7861beb34be45af1)

開発ハイライト
----------------

### symfony 1開発ハイライト

[チェンジログ](http://trac.symfony-project.com/trac/timeline?from=05%2F09%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

- [r30790](http://trac.symfony-project.org/changeset/30790) [1.3, 1.4] "%"の文字がエラーメッセージに含まれているときのWebデバッグツールバーへ正しく表示されるように修正

活動概要: 49 changesets, 10 bugs reported, 16 bugs fixed, 3 enhancements suggested, 3 enhancements closed, 5 documentation defects reported, 1 documentation defect fixed, and 8 documentation edits

### Symfony2開発ハイライト

[チェンジログ](http://github.com/symfony/symfony/commits/master):

- [478fcca](http://github.com/symfony/symfony/commit/478fcca88d9357779f353d07bb3ca301966e88d6) [Templating] Engine::exists() の追加
- [6b5c3d0](http://github.com/symfony/symfony/commit/6b5c3d05bd25b250918fbaec14774e408dee71f9) [FrameworkBundle] 内部コントローラーのためにControllerクラスの利用の削除
- [994a6c3](http://github.com/symfony/symfony/commit/994a6c36ac1e24f8f940a20a3debc91ee9e22c4c) actions::render() ヘルパーメソッドの特性を変更
- [8c6478d](http://github.com/symfony/symfony/commit/8c6478dab976700a247e819179a21d196e252cb1) [HttpKernel] import/export を Profiler に追加
- [d94271b](http://github.com/symfony/symfony/commit/d94271ba9c5e27d8767693a5e073fc4849535694) [FrameworkBundle] DICを利用して依存部分の削除
- [d40d174](http://github.com/symfony/symfony/commit/d40d1746e0f5f5c3c081b2fc8f53541e80a44e2c) [ZendBundle] エラーハンドラーとして zend logger を登録するためのオプションを追加
- [7503463](http://github.com/symfony/symfony/commit/7503463a1e0f78737bf34c31e6cb3e4e28b236af) [DoctrineMongoDBBundle] javascript シェルに似たログフォーマットを更新
- [935ac56](http://github.com/symfony/symfony/commit/935ac5633c5a04421e78a62ef917176d9173d9b3) [DoctrineBundle] 多対多のリレーションを消去するときにdata:loadで発生していたバグの修正
- [60ea1ee](http://github.com/symfony/symfony/commit/60ea1eef698c6eae0d19465e00e9ff9be29bfc4b) 例外が発生したときにのみプロファイラーが有効になるような設定を追加
- [ad835f8](http://github.com/symfony/symfony/commit/ad835f8a1693111a46aaffeee19bcbeecbdaaf2d) [HttpKernel] プロファイラーのストレージのインターフェースにpurge()メソッドを追加
- [ab9be87](http://github.com/symfony/symfony/commit/ab9be87354a29bba11ca8644fcd26bcbaced9956) [HttpKernel] FlattenException ステータスコードの修正
- [a29211a](http://github.com/symfony/symfony/commit/a29211a9ee79a687aa1ecc691e9d91b76271c11c) [FrameworkBundle] テンプレートでヘルパーへの配列アクセスの利用を削除
- [4e57899](http://github.com/symfony/symfony/commit/4e57899374edd84bab3c98f852035a5626f7fa7b), [5913c40](http://github.com/symfony/symfony/commit/5913c40a12becf5775dabf7fd10be524ef4d055e), [7e2f135](http://github.com/symfony/symfony/commit/7e2f135245c0d789a8d3f2f7bd3b8e178992afec), [c8935cc](http://github.com/symfony/symfony/commit/c8935cc25a08fa009681c8e1c4afd82b4d08e51f) [WebProfilerBundle] バンドルを追加
- [ebae1d7](http://github.com/symfony/symfony/commit/ebae1d7bf20d7e68f19f83c6ef71a43967a29d10), [a4d4963](http://github.com/symfony/symfony/commit/a4d496309ba68ed5d0aea897e10fe8bb2b3440ab) [FrameworkBundle] Webプロファイラー設定のスケルトンを更新
- [2d04ca3](http://github.com/symfony/symfony/commit/2d04ca34434f00751e903d8b6ab41f7fef87d5bd) [EventDispatcher] イベント名で全てのリスナーの接続を外す方法を追加
- [15cd264](http://github.com/symfony/symfony/commit/15cd2643c04a1441db3476aa5d09ff05e9c0d83f) [HttpFoundation] Request::getClientIp()メソッドを追加

> **NOTE**
> 翻訳者コメント<br />
> Symfony2 のWebプロファイラーバンドルはとても強力ですし、こういうところに力を入れているところがSymfonyらしいですね。