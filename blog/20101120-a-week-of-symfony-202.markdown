A week of symfony #202 (8->14 November 2010)
============================================

Symfony 公式ブログで毎週公開される、Symfony 関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony 本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/11/14/a-week-of-symfony-202-8-14-november-2010)）

<br />
<br />
<hr />

今週、Symfonyコミュニティで[第1回 Symfony2 IRCミーティング](http://trac.symfony-project.org/wiki/Symfony2IRCMeetingLogs)が開催されました。これから毎週いくつかのトピックを選んで議論を行っていく予定です。
 
開発メーリングリスト
------------------------

  * [Symfony2 recent best practices](http://groups.google.com/group/symfony-devs/browse_thread/thread/24c851f77783403c)
  * [Weekly IRC meetings](http://groups.google.com/group/symfony-devs/browse_thread/thread/3bfdc24722e427eb)
  * [Generating entities problem](http://groups.google.com/group/symfony-devs/browse_thread/thread/f5c9246bbbc52908)

  * [Symfony2の最新のベストプラクティス](http://groups.google.com/group/symfony-devs/browse_thread/thread/24c851f77783403c)
  * [ウィークリーIRCミーティング](http://groups.google.com/group/symfony-devs/browse_thread/thread/3bfdc24722e427eb)
  * [エンティティの生成に関する問題](http://groups.google.com/group/symfony-devs/browse_thread/thread/f5c9246bbbc52908)

Symfony2 開発ハイライト
-------------------------------

[チェンジログ](http://github.com/symfony/symfony/commits/master):

  * [1e13ecb](http://github.com/symfony/symfony/commit/1e13ecb5f3e27de1a1ee078955448beabfba9d89 "1e13ecb5f3e27de1a1ee078955448beabfba9d89 commit on github"): \[TwigBundle\] routeタグをpathタグとurlタグに分割
  * [6aacfa3](http://github.com/symfony/symfony/commit/6aacfa321698d95109bd86cd7ecc2ce0c6676a52 "6aacfa321698d95109bd86cd7ecc2ce0c6676a52 commit on github"): Cookieのパスが/にセットされている場合にへっダーにセットされないバグを修正
  * [4fc1031](http://github.com/symfony/symfony/commit/4fc10310efd5d1de1dd74cd28b9da9a665823966 "4fc10310efd5d1de1dd74cd28b9da9a665823966 commit on github"): \[DoctrineBundle\] CollectionToStringTransformerのデフォルトのシリアライズ/デシリアライズをオーバーライドするためのコールバックを追加
  * [52ec875](http://github.com/symfony/symfony/commit/52ec8752d89882dd9978a76e954615a0e3d1f7d5 "52ec8752d89882dd9978a76e954615a0e3d1f7d5 commit on github"): \[TwigBundle\] route_attributesがnullの場合に例外が発生しないよう修正
  * [a471f65](http://github.com/symfony/symfony/commit/a471f6575945ea44eac333cbb9ae87dd016004a3 "a471f6575945ea44eac333cbb9ae87dd016004a3 commit on github"): \[HttpKernel\] HttpKernelInterfaceを調整
  * [4d4f9f3](http://github.com/symfony/symfony/commit/4d4f9f344ee882f5d0cab51ec5cd9395a4d7642a "4d4f9f344ee882f5d0cab51ec5cd9395a4d7642a commit on github"): RequsetのattributesをRequestDataCollectorとWebプロファイラーに追加
  * [6f28511](http://github.com/symfony/symfony/commit/6f28511ee42edf4f06946f53edfa890c1bf07fa4 "6f28511ee42edf4f06946f53edfa890c1bf07fa4 commit on github"): \[Form\] FileFieldにtypeを追加
  * [d7d4880](http://github.com/symfony/symfony/commit/d7d4880a90a4bd5c6dff98393e08c31bf99c6610 "d7d4880a90a4bd5c6dff98393e08c31bf99c6610 commit on github"): \[TwigBundle\] Twigの最新バージョンにあわせてフィルターを更新
  * [7b02766](http://github.com/symfony/symfony/commit/7b027663734e398ab0ea076fc67d455d49d48bef "7b027663734e398ab0ea076fc67d455d49d48bef commit on github"), [51a3d0b](http://github.com/symfony/symfony/commit/51a3d0ba6a5f5d97887f6d424e411deffd53ed61 "51a3d0ba6a5f5d97887f6d424e411deffd53ed61 commit on github"): セッションの管理方法を修正(Requestオブジェクトが複製された際にSessionオブジェクトが共有されるよう修正; コンフィギュレーションの変更など)
  * [4cd5b2b](http://github.com/symfony/symfony/commit/4cd5b2b1ff9f2c0223b1722a84d21b35fcf315e5 "4cd5b2b1ff9f2c0223b1722a84d21b35fcf315e5 commit on github"): \[WebProfilerBundle\] リダイレクト時の割り込み処理を修正
  * [bfae4ad](http://github.com/symfony/symfony/commit/bfae4ad86cd58737346864ca475104f87adeb66e "bfae4ad86cd58737346864ca475104f87adeb66e commit on github"): \[Form\] PercentFieldのオプションの衝突を修正
  * [6f034d2](http://github.com/symfony/symfony/commit/6f034d2c80183309711c6860a4a2ac7926c3b602 "6f034d2c80183309711c6860a4a2ac7926c3b602 commit on github"): \[FrameworkBundle\] FormAuthenticationListenerのuse_forwardオプションを設定可能に修正
  * [efed600](http://github.com/symfony/symfony/commit/efed6005cbc34c3e3a872bf91bfc39d0be476ad5 "efed6005cbc34c3e3a872bf91bfc39d0be476ad5 commit on github"): \[DependencyInjection\] PHPダンパーを修正
  * [5860bdd](http://github.com/symfony/symfony/commit/5860bdd75adc3f1cecdc0f3b7149dab26b37b05b "5860bdd75adc3f1cecdc0f3b7149dab26b37b05b commit on github"): \[FrameworkBundle\] Requestサービスの定義を追加(実際にはこの定義の内容は使われません)
  * [f5b451f](http://github.com/symfony/symfony/commit/f5b451f5b93f80a1d4bc01503e5e49b317106388 "f5b451f5b93f80a1d4bc01503e5e49b317106388 commit on github"): \[Form\] MoneyToLocalizedStringTransformerの修正とテストの追加
  * [4c340c5](http://github.com/symfony/symfony/commit/4c340c5cc989609066c141f06205b9bb51aef498 "4c340c5cc989609066c141f06205b9bb51aef498 commit on github"): \[Form\] フォームにグループ化されたバリデーションの修正
  * [a198bbc](http://github.com/symfony/symfony/commit/a198bbcf43f2b2d4d671046f55f6e4f615829c73 "a198bbcf43f2b2d4d671046f55f6e4f615829c73 commit on github"): \[Form\] CSRFトークンを生成するときにsession_id()が空の場合例外を発生させるよう修正
  * [48b3e92](http://github.com/symfony/symfony/commit/48b3e92504357eabe14dc6f52adeb1614addd4e6 "48b3e92504357eabe14dc6f52adeb1614addd4e6 commit on github"): \[Form\] Fieldでオプションを指定した後にparent::configure()が呼び出されるよう修正
  * [69cd21d](http://github.com/symfony/symfony/commit/69cd21d8be484fe2f351c1ea0f153cc62ea24e19 "69cd21d8be484fe2f351c1ea0f153cc62ea24e19 commit on github"): \[Validator\] アノテーションローダーで親の制約を2回追加しない用修正

ドキュメンテーション
---------------------

  * <a href="http://trac.symfony-project.org/wiki/Symfony2IRCMeetingLogs">Symfony2 IRCミーティングログ</a>ページ


<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
> 本日、日本Symfonyユーザー会主催で[第1回Symfony2勉強会](http://symfony.gr.jp/events/20101014-symfony2-study)が開催されました。多くの方が参加され、Symfony2に対する期待の高さが伺えました。
> Symfony2本体も開発が活発に行われており、ウィークリーIRCミーティングの開催などより一層よいものを作るためにさまざまな活動が行われています。
> よりよいものにするため、興味がある方はぜひさまざまなイベントに参加してみてください。
> [fivestar]
