A week of symfony #203 (15->21 November 2010)
=============================================

Symfony 公式ブログで毎週公開される、Symfony 関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony 本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/11/07/a-week-of-symfony-201-1-7-november-2010)）

<br />
<br />
<hr />

今週はSymfony2の開発が大きく加速した一週間になりました。まず、Bernhard Schussekがフォームとバリデーターコンポーネントの開発を再度担当することになり、年内中に開発が終えられそうです。次に、Fabienが開発メーリングリストに「<a href="http://groups.google.com/group/symfony-devs/browse_thread/thread/925d40f1cff7fe11">アウトプットエスケーパーの削除について</a>」と「<a href="http://groups.google.com/group/symfony-devs/browse_thread/thread/5f09925263e9d86e">URIテンプレートの利用</a>」の2つの内容を投稿し、議論が行われました。最後に、<a href="http://trac.symfony-project.org/wiki/IRCLogs20101118">ウィークリーIRCミーティング</a>にてSymfony2に関する議論やアイディア、ベストプラクティスなどが活発に行われました。

開発メーリングリスト
------------------------

  * [チャンク形式のレスポンス](http://groups.google.com/group/symfony-devs/browse_thread/thread/47a44c763f510678)
  * [RFC - ルーティングにおけるURIテンプレートの利用](http://groups.google.com/group/symfony-devs/browse_thread/thread/5f09925263e9d86e)
  * [RFC - アウトプットエスケーパーの削除](http://groups.google.com/group/symfony-devs/browse_thread/thread/925d40f1cff7fe11)
  * [XMLとYAMLの設定](http://groups.google.com/group/symfony-devs/browse_thread/thread/e64d3eac79bb8e9a)
  * [redirect()をビューに移動](http://groups.google.com/group/symfony-devs/browse_thread/thread/6a26b1f306da1d1a)

symfony 1 開発ハイライト
--------------------------------

[チェンジログ](http://trac.symfony-project.com/trac/timeline?from=21%2F11%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r31398](http://trac.symfony-project.org/changeset/31398 "31398 revision on trac"): \[1.3, 1.4\] sfRouteクラスのtypoを修正
  * [r31399](http://trac.symfony-project.org/changeset/31399 "31399 revision on trac"), [r31400](http://trac.symfony-project.org/changeset/31400 "31400 revision on trac"): \[1.3, 1.4\] sfViewCacheManagerが正しくないhttp_protocol問題を修正

sfPropelPlugin:

  * [r31401](http://trac.symfony-project.org/changeset/31401 "31401 revision on trac"): \[1.3, 1.4\] esの翻訳を更新

Symfony2 development highlights
-------------------------------

[チェンジログ](http://github.com/symfony/symfony/commits/master):

  * [8b9e979](http://github.com/symfony/symfony/commit/8b9e97911848cef50636aeab89a100034a2f4921 "8b9e97911848cef50636aeab89a100034a2f4921 commit on github"): \[FrameworkBundle\] 常にセッションのサービス情報が設定されるよう修正
  * [f6ddeeb](http://github.com/symfony/symfony/commit/f6ddeeb36b39e02221abd9357908a0caecfa7119 "f6ddeeb36b39e02221abd9357908a0caecfa7119 commit on github"): \[HttpFoundation\] Response::setPublic()を追加し、setPrivate()は引き数を受け取らないよう修正
  * [942104a](http://github.com/symfony/symfony/commit/942104a5ff1a91178a4f868bd7e96be872b5b07c "942104a5ff1a91178a4f868bd7e96be872b5b07c commit on github"), [7257571](http://github.com/symfony/symfony/commit/7257571be4017c7356c25fe1aec19c4b2eff4750 "7257571be4017c7356c25fe1aec19c4b2eff4750 commit on github"): \[HttpFoundation\] 連想配列を受け取って複数のHTTPキャッシュヘッダーの設定を1度で行えるsetCache()メソッドを実装
  * [4aa5ef6](http://github.com/symfony/symfony/commit/4aa5ef63f5122330024d1c2801cb3703dbcdf19e "4aa5ef63f5122330024d1c2801cb3703dbcdf19e commit on github"), [6f898a5](http://github.com/symfony/symfony/commit/6f898a5008361294a751d2407ca3c2fc7bcdf68c "6f898a5008361294a751d2407ca3c2fc7bcdf68c commit on github"): \[HttpKernel\] いくつかのテストをよりロバストに修正
  * [35148c5](http://github.com/symfony/symfony/commit/35148c5ac3d497df759c9aa4d600d37a828f8252 "35148c5ac3d497df759c9aa4d600d37a828f8252 commit on github"): \[FrameworkBundle\] ルーティングの国際化を実装
  * [3813eec](http://github.com/symfony/symfony/commit/3813eecf173b62b2591bc96a38d68a914d6d55ec "3813eecf173b62b2591bc96a38d68a914d6d55ec commit on github"), [519cc09](http://github.com/symfony/symfony/commit/519cc094884e8aefcbab66ef14d47b9c6cf1e60c "519cc094884e8aefcbab66ef14d47b9c6cf1e60c commit on github"): \[Translation\] Yamlファイルローダーを追加
  * [9ab33e4](http://github.com/symfony/symfony/commit/9ab33e4ae4463f51e8bf26f9415531647448bb9b "9ab33e4ae4463f51e8bf26f9415531647448bb9b commit on github"): \[DoctrineMongoDBBundle\] イベントリスナーの登録処理をDIコンテナー経由で行うよう修正
  * [da18873](http://github.com/symfony/symfony/commit/da188734d884843e68b68b0feff65b07150285f3 "da188734d884843e68b68b0feff65b07150285f3 commit on github"): \[DoctrineMongoDBBundle\] イベントマネージャーを複数扱える仕組みをDIエクステンションに追加
  * [b932441](http://github.com/symfony/symfony/commit/b932441ac9270a664e20a3ca8cf4888234ea2b05 "b932441ac9270a664e20a3ca8cf4888234ea2b05 commit on github"): \[DoctrineMongoDBBundle\] グローバルなリスナーを登録する仕組みを追加
  * [58a240b](http://github.com/symfony/symfony/commit/58a240baba084a862648acdbcb1be060a4ca7cd5 "58a240baba084a862648acdbcb1be060a4ca7cd5 commit on github"): \[HttpFoundation\] SERVER_PORTの値が文字列型として返されても問題なく扱えるよう修正
  * [92f3d9e](http://github.com/symfony/symfony/commit/92f3d9e7ec0e56445b968977d17ba25d3f62a62c "92f3d9e7ec0e56445b968977d17ba25d3f62a62c commit on github"): \[DependencyInjection\] 無名サービスの登録の際に用いられるIDの先頭につく_を削除
  * [53dd4e3](http://github.com/symfony/symfony/commit/53dd4e39c734934f9a3d66cd2fc62ab617243659 "53dd4e39c734934f9a3d66cd2fc62ab617243659 commit on github"): \[DependencyInjection\] YAMLでのオプショナルなサービスの表記を@@から@?に変更
  * [f6cc63c](http://github.com/symfony/symfony/commit/f6cc63c99c88de6cb2916e5a5d35be810b5d6306 "f6cc63c99c88de6cb2916e5a5d35be810b5d6306 commit on github"): ContainerとControllerからArrayAccessインターフェイスの実装を削除
  * [d45954a](http://github.com/symfony/symfony/commit/d45954af07802bed51296d29b58d8e21f79760b6 "d45954af07802bed51296d29b58d8e21f79760b6 commit on github"): \[Form, TwigBundle\] レンダリングするすべてのフィールドを確認するよう修正
  * [4e5c99d](http://github.com/symfony/symfony/commit/4e5c99dab049d73bd5cbed1c00f312ca63ccf5ce "4e5c99dab049d73bd5cbed1c00f312ca63ccf5ce commit on github"): \[EventDispatcher\] リスナーを削除する際に指定したイベント名のすべてのリスナーを削除するよう修正
  * [3cbc99c](http://github.com/symfony/symfony/commit/3cbc99c180d8a1604ddef43fd5602677121de3de "3cbc99c180d8a1604ddef43fd5602677121de3de commit on github"): \[Translation\] flattenメソッドをArrayLoaderに追加
  * [5aeb358](http://github.com/symfony/symfony/commit/5aeb3587211517b95e1a05478fe8886008cf2279 "5aeb3587211517b95e1a05478fe8886008cf2279 commit on github"): \[Validator\] バリデーターの名前空間のプレフィックスを変更可能に修正
  * [23ac47e](http://github.com/symfony/symfony/commit/23ac47e0119f783b4396ebeaf682aaa465916caa "23ac47e0119f783b4396ebeaf682aaa465916caa commit on github"): \[Form\] PropertyPathに__getと__setのサポートを追加
  * [0bdb271](http://github.com/symfony/symfony/commit/0bdb27160895b08a4df476286c934b4e63290904 "0bdb27160895b08a4df476286c934b4e63290904 commit on github"): \[Form\]フィールドとトランスフォーマーに親クラスのconfigure()メソッド呼び出しを追加
  * [3127312](http://github.com/symfony/symfony/commit/3127312139bb735663c5184ef5a0a7031c69712d "3127312139bb735663c5184ef5a0a7031c69712d commit on github"): \[Form\] 'value_transformer'と'normalization_transformer'オプションをフィールドクラスに追加

Documentation
-------------

  * <a href="http://trac.symfony-project.org/wiki/IRCLogs20101118">IRCログ 2010 11 18</a>ページ

<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
> 今週の変更の中で気になった点が、ControllerクラスからArrayAccessが外された点です。現在Symfony2でアプリケーションの開発を行っている方でArrayAccess形式でContainerにアクセスしている場合に動かなくなってしまいます。
> ArrayAccessについては本当に配列として扱いたいようなものでない限り外される傾向にあると思われます。(以前はEventクラスからも外されています。)
> ほかにもResponse::setPrivate()が引き数を受け取らないようになり、setPublic()を使うようになっていますので、HTTPキャッシュを使いたい場合にも修正が必要になるかと思われますので、お気をつけください。
> [fivestar]
