A week of symfony #210 (3->9 January 2011)
==========================================

Symfony 公式ブログで毎週公開される、Symfony 関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony 本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2011/01/09/a-week-of-symfony-210-3-9-january-2011)）

<br />
<br />
<hr />

先週、Symfony2リポジトリには主にTwig、フォーム、セキュリティ、Doctrineコンポーネントなど多数のコミットがありました。
twigバンドルは[今週公開されたTwig 1.0 RC1](http://blog.twig-project.org/post/2665679442/twig-1-0-0-rc1-released)で導入された重要な変更に合わせて大きくリファクタリングされました。
セキュリティコンポーネントは新しいACLシステムが追加され、フォームコンポーネントはvirtual field groupsのサポートと自動的にクラスのメタデータを解析してフィールドを作成するFieldFactory機構のサポートを追加しました。
一方、[先週のIRCミーティング](http://trac.symfony-project.org/wiki/IRCLogs20110106)で、Fabienは最終リリースまでのロードマップとweb assestsの取扱を含むいくつかの興味深い情報を発表しました。

開発メーリングリスト
------------------------

  * [Symfony2とtwigを使用してコマンドラインスクリプトからメールを送信](https://groups.google.com/forum/#!topic/symfony-devs/13tR02waev4)
  * [[Symfony2] RFC: 変換](https://groups.google.com/forum/#!topic/symfony-devs/-ZClznjOk7I)
  * [[symfony2] アクションコントローラでのリダイレクトに問題](https://groups.google.com/forum/#!topic/symfony-devs/LaeOR7TQ-0M)
  * [Security Acl - カスタムパーミッションの追加](https://groups.google.com/forum/#!topic/symfony-devs/BuPiIGzPySs)
  * [RFC: ネーミングの問題](https://groups.google.com/forum/#!topic/symfony-devs/lsUe6_jrAEI)
  * [Symfony2: RFC バンドルの特定リソースファイルの上書き](https://groups.google.com/forum/#!topic/symfony-devs/ET78rq4wCsU)
  * [assetsの絶対パス](https://groups.google.com/forum/#!topic/symfony-devs/19oEaZAz7Ac)

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [baf07a1](http://github.com/symfony/symfony/commit/baf07a13acd1270c23b615f8d3077ad560911a35 "baf07a13acd1270c23b615f8d3077ad560911a35 commit on github"), [1af2122](http://github.com/symfony/symfony/commit/1af21221ae2c0003041d7e905f685027280a3152 "1af21221ae2c0003041d7e905f685027280a3152 commit on github"), [3516a04](http://github.com/symfony/symfony/commit/3516a043bcc4dda95b0a6cc74f0bed05b34b844e "3516a043bcc4dda95b0a6cc74f0bed05b34b844e commit on github"): テストを含めたコンバータマネージャとコンバータインタフェースの追加
  * [cbd6d0a](http://github.com/symfony/symfony/commit/cbd6d0aecee7dd9fa6ca941f6c401e7cfb0ece22 "cbd6d0aecee7dd9fa6ca941f6c401e7cfb0ece22 commit on github"): \[DoctrineBundle\] Doctrineのリクエストパラメータのコンバータを追加
  * [f8a88e8](http://github.com/symfony/symfony/commit/f8a88e822f17e2b4bf70bdb7ba8113e97b6e369a "f8a88e822f17e2b4bf70bdb7ba8113e97b6e369a commit on github"), [13fc135](http://github.com/symfony/symfony/commit/13fc13519edfd777fa1fe0fef2a18e0670f530e4 "13fc13519edfd777fa1fe0fef2a18e0670f530e4 commit on github"), [2ee4252](http://github.com/symfony/symfony/commit/2ee4252a1f9500697f8582878fce151c593d1ce0 "2ee4252a1f9500697f8582878fce151c593d1ce0 commit on github"): \[HttpFoundation\] テストでの利用のためArraySessionStorageを追加
  * [385ad72](http://github.com/symfony/symfony/commit/385ad72d643cd58d5d224e3128d4660b73abeeeb "385ad72d643cd58d5d224e3128d4660b73abeeeb commit on github"): \[FrameworkBundle\] 特定のルーティングリゾルバをDIC compilerパスに変更
  * [8e6a384](http://github.com/symfony/symfony/commit/8e6a3849ee68d9d4f4e200579ea1ba41b2b2a42e "8e6a3849ee68d9d4f4e200579ea1ba41b2b2a42e commit on github"): \[TwigBundle\] 特定のTwig EnvironmentクラスをDIC compilerクラスに変更
  * [2985cfa](http://github.com/symfony/symfony/commit/2985cfa5a91deefb401d2eb0047b607041e6afb3 "2985cfa5a91deefb401d2eb0047b607041e6afb3 commit on github"): \[FrameworkBundle\] 特定のProfilerクラスをDIC compilerクラスに変更
  * [59996bd](http://github.com/symfony/symfony/commit/59996bd8b91ceac3327eb14ecd5d1cb8e1c1efe5 "59996bd8b91ceac3327eb14ecd5d1cb8e1c1efe5 commit on github"): \[TwigBundle\] form.twigが{% display %}を使っていたのを修正
  * [46949e2](http://github.com/symfony/symfony/commit/46949e2c22c7663516d99b88a51e919160fba6b6 "46949e2c22c7663516d99b88a51e919160fba6b6 commit on github"): \[DoctrineBundle, DoctrineMongoDBBundle\] DaoAuthenticationProviderを使うことによりドキュメントの定義とエンティティクラスにショートカットを作ることが可能になる
  * [ba2b1aa](http://github.com/symfony/symfony/commit/ba2b1aad281d389d9464bc53ef31e565272cdb5e "ba2b1aad281d389d9464bc53ef31e565272cdb5e commit on github"): Doctrineバンドルが柔軟な構成を可能なようにリファクタリング
  * [db5e180](http://github.com/symfony/symfony/commit/db5e180d3750687ab6d65ebbdd951b80e16590d6 "db5e180d3750687ab6d65ebbdd951b80e16590d6 commit on github"): DIコンテナの調整
  * [6aa750d](http://github.com/symfony/symfony/commit/6aa750d1ceb49dfae1e9d9f8d782ce385401f9b4 "6aa750d1ceb49dfae1e9d9f8d782ce385401f9b4 commit on github"): \[DoctrineBundle\] DoctrineConverterクラスにテストを追加
  * [46b1b5b](http://github.com/symfony/symfony/commit/46b1b5bd60432ba07bde2732a2310a5e76f94174 "46b1b5bd60432ba07bde2732a2310a5e76f94174 commit on github"): \[Security\] トークンが空の場合、LogoutListenerhandlersはハンドラのlogout()メソッドを呼ぶべきではない
  * [500e02d](http://github.com/symfony/symfony/commit/500e02d4fd123cc03f7456527a9f70cdedb2d3d5 "500e02d4fd123cc03f7456527a9f70cdedb2d3d5 commit on github"): 共通コードの中でMongoDBとORM Annotation Reader定義間の齟齬はバグにつながるので修正
  * [c886d88](http://github.com/symfony/symfony/commit/c886d88bf367c2f7be1afc3e861c05b8e2baf9e6 "c886d88bf367c2f7be1afc3e861c05b8e2baf9e6 commit on github"), [5c73619](http://github.com/symfony/symfony/commit/5c73619d801ad0e006a9bc3d05c820ef0439afc0 "5c73619d801ad0e006a9bc3d05c820ef0439afc0 commit on github"): \[DependencyInjection\] interface injectionsをリゾルビングする時に強制的にクラスファイルを読み込む
  * [b428845](http://github.com/symfony/symfony/commit/b4288459cc440fda95eb7f2b431d04dd3e54f80e "b4288459cc440fda95eb7f2b431d04dd3e54f80e commit on github"): ACLシステムをセキュリティコンポーネントに追加
  * [49a3e52](http://github.com/symfony/symfony/commit/49a3e52fa8c25a7307b4ce33fa679b9cd068f368 "49a3e52fa8c25a7307b4ce33fa679b9cd068f368 commit on github"): \[HttpFoundation\] デフォルトのセッション名をPHP 5.3以降で動作していないように見える_SESSIONから_SESSに変更
  * [62cd09e](http://github.com/symfony/symfony/commit/62cd09e7081795809a4f1f5e24f2db287b905913 "62cd09e7081795809a4f1f5e24f2db287b905913 commit on github"): \[TwigBundle\] assetタグからasset関数へ置き換え( {% asset css/foo.css %}から{{ asset('css/foo.css') }}へ
  * [d8b8ae0](http://github.com/symfony/symfony/commit/d8b8ae0608b8b9933865a84f8d3acb6e044bbfb4 "d8b8ae0608b8b9933865a84f8d3acb6e044bbfb4 commit on github"): \[FrameworkBundle, TwigBundle\] Formレンダリングにfield_rowテンプレートを導入
  * [b9c2e98](http://github.com/symfony/symfony/commit/b9c2e983159d31b217873d446138fde6e0e10489 "b9c2e983159d31b217873d446138fde6e0e10489 commit on github"): \[Form, Locale\] LocaleFieldに実装し、ICUのデータを更新するためのスクリプトを追加
  * [52ecffe](http://github.com/symfony/symfony/commit/52ecffe51b93afa93a38dd46839889ca9dd5c287 "52ecffe51b93afa93a38dd46839889ca9dd5c287 commit on github"): \[Validator\] Locale制約の実装
  * [2daa6b5](http://github.com/symfony/symfony/commit/2daa6b5bfedac13702cd75f4dc5d12a5d742724d "2daa6b5bfedac13702cd75f4dc5d12a5d742724d commit on github"): \[TwigBundle\] twigテンプレートのDateFields表示の修正
  * [a99d8c8](http://github.com/symfony/symfony/commit/a99d8c8558717d5d0cd29bcdc23f5ac077ade106 "a99d8c8558717d5d0cd29bcdc23f5ac077ade106 commit on github"): セキュリティIDの重複可能の修正
  * [55a48bc](http://github.com/symfony/symfony/commit/55a48bcfa629059b3b86c4319f38a15fbc8920e9 "55a48bcfa629059b3b86c4319f38a15fbc8920e9 commit on github"): AclVoterを最適化し、ユニットテストを追加
  * [fa7fded](http://github.com/symfony/symfony/commit/fa7fdedf4b4ea492d38dff7e5f1a4094b6cd7ff0 "fa7fdedf4b4ea492d38dff7e5f1a4094b6cd7ff0 commit on github"): 400以上のコードがORMとMongoDBバンドルで重複していたため、メタバンドルのDoctrineAbstractBundleを導入
  * [302dbd1](http://github.com/symfony/symfony/commit/302dbd12257fb00cc7198bac01af6ad4994cc908 "302dbd12257fb00cc7198bac01af6ad4994cc908 commit on github"): Symfony DICがEventManagerを使用するようにリファクタリング
  * [eb4788e](http://github.com/symfony/symfony/commit/eb4788e98e4e578ae4178536c41536a79b4a1dfd "eb4788e98e4e578ae4178536c41536a79b4a1dfd commit on github"): \[DependencyInjection\] サービスキーおよびエイリアスの大文字と小文字を区別しない(PHPのメソッド名は大文字小文字区別しないように)
  * [840bd8a](http://github.com/symfony/symfony/commit/840bd8aacd4ab48474e0600ecd54acee7b82f080 "840bd8aacd4ab48474e0600ecd54acee7b82f080 commit on github"): \[TwigBundle\] 'render'タグでのHelperTokenParserの利用を削除
  * [3f492ca](http://github.com/symfony/symfony/commit/3f492cae400bcfed53537c675d69cd13e64ef699 "3f492cae400bcfed53537c675d69cd13e64ef699 commit on github"): \[TwigBundle\] js/cssタグでのHelperTokenParserの利用を削除
  * [5c6b594](http://github.com/symfony/symfony/commit/5c6b594daed30f30bd5152d3021943b1f6642978 "5c6b594daed30f30bd5152d3021943b1f6642978 commit on github"): \[TwigBundle\] フォームフィルターを関数に変換
  * [8b843e2](http://github.com/symfony/symfony/commit/8b843e266203e3c5416eb01c72dffe91d87a7e1a "8b843e266203e3c5416eb01c72dffe91d87a7e1a commit on github"): \[TwigBundle\] Twigの変更に伴うtransタグの修正
  * [ba422e8](http://github.com/symfony/symfony/commit/ba422e8472c8c16235760cb095f228f6ee9496f5 "ba422e8472c8c16235760cb095f228f6ee9496f5 commit on github"): \[Form\] virtual field groupsのサポートの追加
  * [708c780](http://github.com/symfony/symfony/commit/708c7802135aa88e6f66223fbe45fc6d36186ce1 "708c7802135aa88e6f66223fbe45fc6d36186ce1 commit on github"): \[Validator\] @Validation制約を@Setにリネーム
  * [8513082](http://github.com/symfony/symfony/commit/85130820079a65494d7cd4834eb120b126650e56 "85130820079a65494d7cd4834eb120b126650e56 commit on github"): \[Form, HttpFoundation\] FileとUploadedFileクラスの改善
  * [e9a7531](http://github.com/symfony/symfony/commit/e9a7531a26cccd06e701e3b8ee9df5faa3f4d075 "e9a7531a26cccd06e701e3b8ee9df5faa3f4d075 commit on github"): \[Form\] 制約メソッドのField::isTransformationSuccessful()を追加
  * [48af2fc](http://github.com/symfony/symfony/commit/48af2fc86edffd83034e2d3d3b94dc75511eae97 "48af2fc86edffd83034e2d3d3b94dc75511eae97 commit on github"): \[Form, FrameworkBundle, HttpFoundation\] フォームがCSRFから保護されている時に自動的にセッションを開始する
  * [acdd5c0](http://github.com/symfony/symfony/commit/acdd5c06de1e62caa042df8a37360403475c58f0 "acdd5c06de1e62caa042df8a37360403475c58f0 commit on github"): \[Form\] Value TransformerでUnexpectedTypeException例外をスローするように変更
  * [114b2cf](http://github.com/symfony/symfony/commit/114b2cf6c1a3ec20957db2333a1dc6d0211032dc "114b2cf6c1a3ec20957db2333a1dc6d0211032dc commit on github"): \[FrameworkBundle\] PHPのレンダーでフォームフィールドをレンダリングする時にattributesも渡す事ができるようにする
  * [39c9bf1](http://github.com/symfony/symfony/commit/39c9bf160e5716aec0f42b3552524804e534b8e5 "39c9bf160e5716aec0f42b3552524804e534b8e5 commit on github"): \[Validator\] @Ip制約の実装
  * [9b10c8a](http://github.com/symfony/symfony/commit/9b10c8a86652d50e4b3e38dc5dd8ca14ffb5619c "9b10c8a86652d50e4b3e38dc5dd8ca14ffb5619c commit on github"): \[WebProfileBundle\] リダイレクトが中断した時にレスポンスコンテンツにより多くの情報を追加
  * [0e487cd](http://github.com/symfony/symfony/commit/0e487cdda65766d5af9d9181cfc7da5dfb30145f "0e487cdda65766d5af9d9181cfc7da5dfb30145f commit on github"): \[TwigBundle\] 現在のプレースホルダー変換{{ foo }}シンタックスを%foo%に変更
  * [b60d254](http://github.com/symfony/symfony/commit/b60d254be2f9b9a8b1340a8f7b40270748692ca5 "b60d254be2f9b9a8b1340a8f7b40270748692ca5 commit on github"): \[TwigBundle\] リクエストとセッションをグローバル変数として追加(フォームテンプレートから'_view'変数を削除、セッションをフォームから直接利用可能になったので'flash()'関数を削除)
  * [7b7e83f](http://github.com/symfony/symfony/commit/7b7e83f428fceec8ad20d23e7247a9116f08dc2f "7b7e83f428fceec8ad20d23e7247a9116f08dc2f commit on github"): 期待通りに働かなかったのでjs/cssヘルパーとTwig integrationを削除
  * [7fdc61f](http://github.com/symfony/symfony/commit/7fdc61f2723232ad9e256b01f0ea941c69f9eb63 "7fdc61f2723232ad9e256b01f0ea941c69f9eb63 commit on github"): \[TwigBundle\] Twigグローバルフォームコンフィギュレーションに登録する方法を追加
  * [aea712d](http://github.com/symfony/symfony/commit/aea712d8a20ed6a0cb46b49726b0a2cf5b150bf9 "aea712d8a20ed6a0cb46b49726b0a2cf5b150bf9 commit on github"): \[ZendBundle\] 新しいwritersを追加する簡単な方法を追加 (zend.logger.writerタグを使用してサービスを追加)
  * [1148519](http://github.com/symfony/symfony/commit/114851969581bbcdae88ea4ac293ca47e878cb1c "114851969581bbcdae88ea4ac293ca47e878cb1c commit on github"): \[HttpKernel\] WindowsとUnixでパスの統一
  * [1e27d43](http://github.com/symfony/symfony/commit/1e27d4359c9f70484ca28645da3a288f0267555a "1e27d4359c9f70484ca28645da3a288f0267555a commit on github"): \[DoctrineBundle\] class_metadata_factory_name設定オプションを追加
  * [3ab82cb](http://github.com/symfony/symfony/commit/3ab82cbd534d19fa2f164c099d87782aedd86eea "3ab82cbd534d19fa2f164c099d87782aedd86eea commit on github"): \[FrameworkBundle, Security\] 明示的に提供されているセキュリティプロバイダのDICエイリアスを作成
  * [598d458](http://github.com/symfony/symfony/commit/598d458a3c5e45f67a2f6686433272abde29b1e3 "598d458a3c5e45f67a2f6686433272abde29b1e3 commit on github"): CompatAssetsBundleに非推奨のcss/jsヘルパーとタグを再導入
  * [4b78c43](http://github.com/symfony/symfony/commit/4b78c4376ff02a33afc6c0ac720cf014ac4d90e0 "4b78c4376ff02a33afc6c0ac720cf014ac4d90e0 commit on github"): \[Form\] クラスのメタデータを解析することによって自動的にフィールドを作成するFieldFactory機構の追加
  * [c5ef113](http://github.com/symfony/symfony/commit/c5ef113b186caa09b951c48cc4f637c2660cef6f "c5ef113b186caa09b951c48cc4f637c2660cef6f commit on github"): DIコンテナの最適化
  * [da5475e](http://github.com/symfony/symfony/commit/da5475ec428102c90067c284a8995a87f91a8013 "da5475ec428102c90067c284a8995a87f91a8013 commit on github"): サービスの参照権限設定の変更
  * [b5e26d9](http://github.com/symfony/symfony/commit/b5e26d9db8c723c8812fa4dee6bd2c8a11dd6c5a "b5e26d9db8c723c8812fa4dee6bd2c8a11dd6c5a commit on github"): \[SwiftmailerBundle\] プライベートサービスの追加
  * [f946355](http://github.com/symfony/symfony/commit/f946355f80373f9a985937394d181144742a3b15 "f946355f80373f9a985937394d181144742a3b15 commit on github"): \[TwigBundle\] form_row()関数の追加
  * [584769d](http://github.com/symfony/symfony/commit/584769dd164b1e8f82888c88d436f84fc3146aec "584769dd164b1e8f82888c88d436f84fc3146aec commit on github"): \[HttpFoundation\] SessionクラスにremoveFlashメソッドとclearFlashesメソッドを追加
  * [afc2f96](http://github.com/symfony/symfony/commit/afc2f965498e1e482ab2c3fcc30b87438f12ac13 "afc2f965498e1e482ab2c3fcc30b87438f12ac13 commit on github"), [ed359af](http://github.com/symfony/symfony/commit/ed359af5438b93bf0ab1f78a041528a92713db0a "ed359af5438b93bf0ab1f78a041528a92713db0a commit on github"): \[Templating\] Twigとグローバル変数の実装を追加
  * [911dbe9](http://github.com/symfony/symfony/commit/911dbe9cc4286e51933a0cee6589289afa3bba08 "911dbe9cc4286e51933a0cee6589289afa3bba08 commit on github"): twigサービスとテンプレートの設定の循環参照を削除 (新規にテンプレート名をパースするTemplateNameConverterを追加, twigローダとテンプレートエンジンの間の依存関係の削除)
  * [af8ebea](http://github.com/symfony/symfony/commit/af8ebeaabbb3878e5314d73c2ee74b184775e5a9 "af8ebeaabbb3878e5314d73c2ee74b184775e5a9 commit on github"): \[DependencyInjection\] サービスの循環参照の自動検出を追加
  * [cfd4e21](http://github.com/symfony/symfony/commit/cfd4e2186f0dc444bec4438a165eef317c58e4e2 "cfd4e2186f0dc444bec4438a165eef317c58e4e2 commit on github"): UniversalClassLoaderのマッチングの衝突を修正
  * [314defa](http://github.com/symfony/symfony/commit/314defa8b4f70b41f1c5476d310861766e22ef29 "314defa8b4f70b41f1c5476d310861766e22ef29 commit on github"): 汎用encoder factoryの追加
  * [9553971](http://github.com/symfony/symfony/commit/9553971d06875d417695c4a63e03885a608dafb7 "9553971d06875d417695c4a63e03885a608dafb7 commit on github"): \[TwigBundle\] リクエストとセッションが利用できない場合でもRenderer::evaluate()を許可
  * [2ded40f](http://github.com/symfony/symfony/commit/2ded40fb7534388209c7522317f8c455480da5d3 "2ded40fb7534388209c7522317f8c455480da5d3 commit on github"): \[TwigBundle\] コンフィギュレーションからエクステンションを簡単に登録する方法を追加
  * [964bf43](http://github.com/symfony/symfony/commit/964bf4356ecedcdf02e0bce2d9d7fd0681cd7904 "964bf4356ecedcdf02e0bce2d9d7fd0681cd7904 commit on github"): Doctrine2が存在しない場合セキュリティテストが失敗していたのを修正
  * [0c50ca8](http://github.com/symfony/symfony/commit/0c50ca87755daf2da40bdca9b8da4868f9b3c7a1 "0c50ca87755daf2da40bdca9b8da4868f9b3c7a1 commit on github"): \[TwigBundle\] renderer::evaluate()はリクエストが定義されており空でない事を確認する必要がある
  * [554c86c](http://github.com/symfony/symfony/commit/554c86c5895f9ef3e48d6da3d4155b2fd763332d "554c86c5895f9ef3e48d6da3d4155b2fd763332d commit on github"): \[DependencyInjection\] エクステンションローダメソッドに役立つhasInterfaceInjectorForClass()の追加
  * [f2ac2a4](http://github.com/symfony/symfony/commit/f2ac2a4c8a1e3aa1f75622c358a83984af3bf017 "f2ac2a4c8a1e3aa1f75622c358a83984af3bf017 commit on github"): レンダラのセッターインジェクションを使用するようTemplatingコンポーネントを変更
  * [bc2ca8f](http://github.com/symfony/symfony/commit/bc2ca8f1cf77a60fdf460614fc9cdc218110dd43 "bc2ca8f1cf77a60fdf460614fc9cdc218110dd43 commit on github"): テンプレートでPHPレンダラはオプショナルに
  * [3785a99](http://github.com/symfony/symfony/commit/3785a99b947c26b84585ffe34225b600822b382e "3785a99b947c26b84585ffe34225b600822b382e commit on github"): DIコンテナのサービスエイリアスに参照権限を設定できるように機能追加
  * [a116199](http://github.com/symfony/symfony/commit/a11619973b9fea3b4452a9429968e1905c831392 "a11619973b9fea3b4452a9429968e1905c831392 commit on github"): \[DependencyInjection\] pharアーカイブの中のエクステンションのxmlバリデーションの修正
  * [50809d2](http://github.com/symfony/symfony/commit/50809d2ae03d4ce0d744ff6fd2b3c515da353d6c "50809d2ae03d4ce0d744ff6fd2b3c515da353d6c commit on github"): \[TwigBundle\] セキュリティコンテキストとユーザを、定義されている場合にそれぞれグローバル変数に追加するように修正
  * [10fee8c](http://github.com/symfony/symfony/commit/10fee8c8bbd42a8a13efc9bc8e6b9e51ce8edb2a "10fee8c8bbd42a8a13efc9bc8e6b9e51ce8edb2a commit on github"): \[HttpKernel\] SQLite storageプロファイラにエスケープ処理を追加



> **NOTE**
> 翻訳者コメント<br />
> 今週のA Week of symfonyは、[@taka512さん](http://twitter.com/taka512) に翻訳していただきました。
> Symfony2は3月の正式リリースに向けていよいよベータバージョンが発表される段階になっています。これからの2ヶ月は、Symfony2からは目が離せませんね！
> [hidenorigoto]
