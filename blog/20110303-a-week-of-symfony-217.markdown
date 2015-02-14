---
layout: default
title: A week of symfony #217 (21->27 February 2011)
---

A week of symfony #217 (21->27 February 2011)
=============================================

Symfony2のパブリックAPIはまもなく数日中には凍結されるでしょう。そのため、今週の開発者たちは、最後の影響の大きな変更をリポジトリにコミットしました：Responseは[DICから削除](https://github.com/symfony/symfony/commit/d94acd85f9aee2342c7ec381d7fdd66aea1eafef)されました、 [AsseticBundleを支持して](https://github.com/symfony/symfony/commit/a3207e939f4f4de24a740ce56b04483eb46e4074) CompatAssetsBundleは削除されました、そして [boostrap ファイル](https://github.com/symfony/symfony/commit/b44d044b0afe218594d9ed7965eaeb272576bf80) も削除されました。
他の幾つかの変更点も開発者MLで提案されました。例えば [translationするときにキーを使う](https://groups.google.com/forum/#!topic/symfony-devs/n3HznxzQW8A) や [FormsにDIを追加](https://groups.google.com/forum/#!topic/symfony-devs/WHiSVfrno74) などです。最後に、[Symfony2 ドキュメント](http://docs.symfony-reloaded.org/)が大きく再編され、新しいコンテンツやよりよいコンテンツがたくさん増えました。

開発者ML
------------------------

  * [\[Symfony2\] Responseサービスの削除](https://groups.google.com/forum/#!topic/symfony-devs/hQWgf96uVT0)
  * [emailプロバイダの結合](https://groups.google.com/forum/#!topic/symfony-devs/cntxm3w4tSg)
  * [\[Symfony2\] RFC - translationソースをメッセージキューに変更](https://groups.google.com/forum/#!topic/symfony-devs/n3HznxzQW8A)
  * [developmentモードにおけるFlashメッセージ](https://groups.google.com/forum/#!topic/symfony-devs/jrjyzeaBFMA)
  * [\[Symfony2\] RFC: FromsにDIを追加 - 実験的なリファクタリング](https://groups.google.com/forum/#!topic/symfony-devs/WHiSVfrno74)
  * [ルーティングにおける任意のプレースホルダー](https://groups.google.com/forum/#!topic/symfony-devs/UVkncjTnJKQ)

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [9b16f1a](http://github.com/symfony/symfony/commit/9b16f1a61428427d1e54c5ed214dacda185d593b "9b16f1a61428427d1e54c5ed214dacda185d593b commit on github"): \[SwiftMailer\] SendEmail Command の追加 (spool用)
  * [f985da5](http://github.com/symfony/symfony/commit/f985da5a9c7968cbd15acf87a1379959b30a14af "f985da5a9c7968cbd15acf87a1379959b30a14af commit on github"): \[HttpFoundation\] ResponseがExpiresヘッダフィールドを強制している時のCache-Control ヘッダの修正
  * <del>[f5b1cb1](http://github.com/symfony/symfony/commit/f5b1cb18e101115d3995f6ce2dd8597672cca058 "f5b1cb18e101115d3995f6ce2dd8597672cca058 commit on github"), [e7c098e](http://github.com/symfony/symfony/commit/e7c098e8a2ddce9e4faa761803c5b08d93dd5bdf "e7c098e8a2ddce9e4faa761803c5b08d93dd5bdf commit on github"): \[DependencyInjection\] NodeBuilderにallowUnnamedChildrenメソッドを初期実装。同時に、余分なフィールドの例外を追加</del> (取り消されました)
  * [bd15ddd](http://github.com/symfony/symfony/commit/bd15ddda96e02ab2144350105adf49e1fdd66c2f "bd15ddda96e02ab2144350105adf49e1fdd66c2f commit on github"), [554628c](http://github.com/symfony/symfony/commit/554628cf5b315a55b8814cae0b338c56245adfe7 "554628cf5b315a55b8814cae0b338c56245adfe7 commit on github"), [d6617f6](http://github.com/symfony/symfony/commit/d6617f6fba9f09d38e152341d8921d3844675fd9 "d6617f6fba9f09d38e152341d8921d3844675fd9 commit on github"): \[DependencyInjection\] pre-buildなNodeBuilderを追加する必要があるときに流れるようなインターフェースを実現するための NodeBuilder::addNodeBuilder() メソッドの追加
  * [fd5cdfc](http://github.com/symfony/symfony/commit/fd5cdfc18f118d8331583f053004e46290631109 "fd5cdfc18f118d8331583f053004e46290631109 commit on github"): \[DependencyInjection\] XMLに再マップされた単一のオプションやキー属性オプションが、処理されたあとに削除されることを保証
  * [ea768fe](http://github.com/symfony/symfony/commit/ea768fe6fcfb094b2dad2e006a3411165019bf59 "ea768fe6fcfb094b2dad2e006a3411165019bf59 commit on github"), [48459e9](http://github.com/symfony/symfony/commit/48459e9082e9477ca783ae920388671363e09761 "48459e9082e9477ca783ae920388671363e09761 commit on github"): \[Config\] キー属性の削除を表すオプションをリネーム
  * [f0d2ce7](http://github.com/symfony/symfony/commit/f0d2ce7f322d47ccb98d7f9b1f1b66a9d8877d5b "f0d2ce7f322d47ccb98d7f9b1f1b66a9d8877d5b commit on github"): \[TwigBundle\] TwigExtensionクラスをリファクタリングし、コンフィグレーションツリーを実装
  * [026ab6c](http://github.com/symfony/symfony/commit/026ab6c6cedf23475670718ed55e5b03a550c6a1 "026ab6c6cedf23475670718ed55e5b03a550c6a1 commit on github"): \[Config\] バリデーションの例外を通さずにオプションを簡単に無視できるように ignoreExtraKeys オプションを追加
  * [c9406b6](http://github.com/symfony/symfony/commit/c9406b62b29874aa3d6dc818dc065822c2f0edf4 "c9406b62b29874aa3d6dc818dc065822c2f0edf4 commit on github"): \[SecurityBundle\] バリデーションの例外なしにメインのConfigurationツリーを構築できるように修正
  * [dff3585](http://github.com/symfony/symfony/commit/dff35851626f62509adff86c85382bfe5cc4979a "dff35851626f62509adff86c85382bfe5cc4979a commit on github"): dev環境でESIを使うときのプロファイラを修正
  * [d2684f3](http://github.com/symfony/symfony/commit/d2684f3f7345ce35f740b4c72454cab313690d06 "d2684f3f7345ce35f740b4c72454cab313690d06 commit on github"): \[AsseticBundle\] Configurationクラスを使うように変換
  * [c01be42](http://github.com/symfony/symfony/commit/c01be42933969fc6d9264685ddb105308051a147 "c01be42933969fc6d9264685ddb105308051a147 commit on github"): \[AsseticBundle\] フィルタマネージャをあとから読み込むように修正
  * [4ba0e0d](http://github.com/symfony/symfony/commit/4ba0e0d5cf311a91645ffa200137332d07751ef8 "4ba0e0d5cf311a91645ffa200137332d07751ef8 commit on github"): \[AsseticBundle\] inputsのバンドル表記法を修正
  * [9b15b69](http://github.com/symfony/symfony/commit/9b15b6950cfed5e613393a4b5aea14189b21f381 "9b15b6950cfed5e613393a4b5aea14189b21f381 commit on github"): \[AsseticBundle\] ファイルシステム独自の結果を読み込む前にTwigアセットを名前でソート
  * [f1dd3f2](http://github.com/symfony/symfony/commit/f1dd3f22e32cb951dcbdca7bee97c8d5fbf18ed6 "f1dd3f22e32cb951dcbdca7bee97c8d5fbf18ed6 commit on github"), [946d3d9](http://github.com/symfony/symfony/commit/946d3d9302a1a72db2107a26c84256110ee1e15c "946d3d9302a1a72db2107a26c84256110ee1e15c commit on github"): \[TwigBundle\] 2つのグローバル変数を追加 (environment &amp; debug)
  * [2c45611](http://github.com/symfony/symfony/commit/2c45611f4e08b578fc3a54187ef1a3bae962400d "2c45611f4e08b578fc3a54187ef1a3bae962400d commit on github"): プロバイダへのWDTリンクを修正
  * [0834bf4](http://github.com/symfony/symfony/commit/0834bf47dcc7094538a6c958fd62a15049712be0 "0834bf47dcc7094538a6c958fd62a15049712be0 commit on github"): \[WebProfilerBundle\] 誤った形式のHTMLコンテンツ上のWDTを削除
  * [f6e624b](http://github.com/symfony/symfony/commit/f6e624b1e2182be0fb598db529d4bc3e7b245746 "f6e624b1e2182be0fb598db529d4bc3e7b245746 commit on github"): \[TwigBundle\] %…%パラメータを使えるように、XSDにおけるすべてのboolean型をstring型に変更
  * [a3207e9](http://github.com/symfony/symfony/commit/a3207e939f4f4de24a740ce56b04483eb46e4074 "a3207e939f4f4de24a740ce56b04483eb46e4074 commit on github"): CompatAssetsBundleを削除し、代わりにAsseticBundleを使用
  * [b44d044](http://github.com/symfony/symfony/commit/b44d044b0afe218594d9ed7965eaeb272576bf80 "b44d044b0afe218594d9ed7965eaeb272576bf80 commit on github"): \[HttpKernel\] コンポーネントに属していないのでbootstrapファイルを削除
  * [9a25878](http://github.com/symfony/symfony/commit/9a25878109feb582e52869503b055c1f9026bef8 "9a25878109feb582e52869503b055c1f9026bef8 commit on github"): \[FrameworkBundle\] Welcomeページを削除し、sandbox/standard 配布物の中に移動
  * [eda7475](http://github.com/symfony/symfony/commit/eda74755ba1954950f48fc1dea4eda643ca4223e "eda74755ba1954950f48fc1dea4eda643ca4223e commit on github"): \[ZendBundle\] ログ設定がある場合に１つしかロガーを読み込まないように修正
  * [28bf834](http://github.com/symfony/symfony/commit/28bf834c0c7845a3a9fc9605e0e35c99e1475a6b "28bf834c0c7845a3a9fc9605e0e35c99e1475a6b commit on github"): \[WebProfilerBundle\] 自身のAjaxリクエストに移動することで、WDTの煩わしさを軽減
  * <del>[608e443](http://github.com/symfony/symfony/commit/608e443c9719bad6929115a10d2e3ecc0abfbed6 "608e443c9719bad6929115a10d2e3ecc0abfbed6 commit on github"): \[Config\] VariableNodeを作成</del> (取り消されました)
  * [f4c0af7](http://github.com/symfony/symfony/commit/f4c0af76e767013ba5d64fe12b4ecd912c85ea9b "f4c0af76e767013ba5d64fe12b4ecd912c85ea9b commit on github"): \[TwigBundle\] 任意の変数がグローバルな値として許容されるように修正
  * [23e9386](http://github.com/symfony/symfony/commit/23e9386a0ea8dd3f4c25e27dda4e62a1b9e52752 "23e9386a0ea8dd3f4c25e27dda4e62a1b9e52752 commit on github"): すべてのExtensionが デフォルトでExtension::getAlias() 実装を使用するように変更
  * [c518074](http://github.com/symfony/symfony/commit/c5180743066cae38b13134ef24137c215a707a1d "c5180743066cae38b13134ef24137c215a707a1d commit on github"): アプリケーションレベルの設定を支持して、DoctrineMigrationsのためのDI Extensionを追加し、-bundleオプションを削除
  * [8a8c733](http://github.com/symfony/symfony/commit/8a8c73336918a25eec11e2546e7bf641f85b8dba "8a8c73336918a25eec11e2546e7bf641f85b8dba commit on github"): \[HttpKernel\] プロファイラトークンで親トークンを定義できるように修正
  * [9619c7d](http://github.com/symfony/symfony/commit/9619c7dade0db54d9171dcc26c7218f94ec45e9e "9619c7dade0db54d9171dcc26c7218f94ec45e9e commit on github"): \[Routing\] スラッシュ記号が先頭になかったときに自動的に追加するようなルーティングハックを削除
  * [e729589](http://github.com/symfony/symfony/commit/e729589b106e271dc41aad72903e6e9028a12a7e "e729589b106e271dc41aad72903e6e9028a12a7e commit on github"): SMTPを使用しないときに問題を避けるためにSwiftMailerの設定を分割
  * [d4fc3c9](http://github.com/symfony/symfony/commit/d4fc3c98b1cdd6f3df63d70ad2c4b7c0840ed8f9 "d4fc3c98b1cdd6f3df63d70ad2c4b7c0840ed8f9 commit on github"), [7c9528b](http://github.com/symfony/symfony/commit/7c9528be7bb9ece6c184ad0b9978d51d0c91bb29 "7c9528be7bb9ece6c184ad0b9978d51d0c91bb29 commit on github"), [b9168bb](http://github.com/symfony/symfony/commit/b9168bb6529ea673841bfcae34639cfc35369ad3 "b9168bb6529ea673841bfcae34639cfc35369ad3 commit on github"): \[FrameworkBundle\] init:bundle スケルトンファイルを更新
  * [f21578e](http://github.com/symfony/symfony/commit/f21578e8195ec08a1b5becfadb5c6b32a5e5c961 "f21578e8195ec08a1b5becfadb5c6b32a5e5c961 commit on github"): \[Security\] abstract user provider定義を追加
  * [bf20238](http://github.com/symfony/symfony/commit/bf20238178e2ab1fb759464180c1cdcfb96b6cc4 "bf20238178e2ab1fb759464180c1cdcfb96b6cc4 commit on github"): Response content-type の自動判別のバグを修正
  * [d94acd8](http://github.com/symfony/symfony/commit/d94acd85f9aee2342c7ec381d7fdd66aea1eafef "d94acd85f9aee2342c7ec381d7fdd66aea1eafef commit on github"): サービスとしてのresponseを削除 (今後はDICでResponseを使用することはできない)
  * [353177d](http://github.com/symfony/symfony/commit/353177d1d66ea220137beeedb0d50915b45f88ec "353177d1d66ea220137beeedb0d50915b45f88ec commit on github"): Response::createRedirect を新しいRedirectResponse クラスに置換
  * [fc372bc](http://github.com/symfony/symfony/commit/fc372bc217385dc5130989150e979537140771a3 "fc372bc217385dc5130989150e979537140771a3 commit on github"): \[HttpKernel\] core.view イベントをfilter()の代わりにnotifyUntil()を使うように変更
  * [a0bae94](http://github.com/symfony/symfony/commit/a0bae94f882966cc60707b8a0b55ca1cd6e6029c "a0bae94f882966cc60707b8a0b55ca1cd6e6029c commit on github"): \[HttpFoundation\] いつ変更されてもいいように、Cache-Controlを計算するようにResponseHeaderBagを更新
  * [cef86a3](http://github.com/symfony/symfony/commit/cef86a3771d28a6588492664d6c4c370a4cb676f "cef86a3771d28a6588492664d6c4c370a4cb676f commit on github"): \[HttpKernel\] ESI キャッシュstrategyを変更できる方法を追加
  * [efb5617](http://github.com/symfony/symfony/commit/efb561767b0f48c2e128cb9f422634866cd25851 "efb561767b0f48c2e128cb9f422634866cd25851 commit on github"): \[AsseticBundle\] AsseticControllerにおけるResponseサービスへの依存性を削除
  * [d7ea92a](http://github.com/symfony/symfony/commit/d7ea92a0f62175f525a99397682e6d8d143fce17 "d7ea92a0f62175f525a99397682e6d8d143fce17 commit on github"): \[AsseticBundle\] 最新のassetic developmentを更新
  * <del>[0f353c1](http://github.com/symfony/symfony/commit/0f353c14110c1dc2383b231503cf3c933b846d55 "0f353c14110c1dc2383b231503cf3c933b846d55 commit on github"): data fixtureを読み込むときに実行されたSQLクエリからのマイグレーションを生成するコマンドを追加</del> (取り消されました)
  * [788f63d](http://github.com/symfony/symfony/commit/788f63d460bdb2260f008d86cc094841f2e70894 "788f63d460bdb2260f008d86cc094841f2e70894 commit on github"): \[FrameworkBundle\] 複雑になりすぎたテンプレートキャッシュwarmerを簡素化
  * [9f2d59c](http://github.com/symfony/symfony/commit/9f2d59c489494552d2f74fa0a0b075b1a5a0d800 "9f2d59c489494552d2f74fa0a0b075b1a5a0d800 commit on github"): \[AsseticBundle\] stylusフィルタの追加
  * [192583a](http://github.com/symfony/symfony/commit/192583a225158c2f0d3022f9ec768806b36b4003 "192583a225158c2f0d3022f9ec768806b36b4003 commit on github"): \[ZendBundle\] Configurationクラスの追加
  * [05055d4](http://github.com/symfony/symfony/commit/05055d443c82bd0206aed396a205df56ae6e8e05 "05055d443c82bd0206aed396a205df56ae6e8e05 commit on github"): \[AsseticBundle\] formula キャッシングシステムを修正
  * [d4db531](http://github.com/symfony/symfony/commit/d4db5319c821c8769771567ff6ea2d208e3bcb28 "d4db5319c821c8769771567ff6ea2d208e3bcb28 commit on github"): \[AsseticBundle\] ルーティングローダにリソースを追加
  * [968c870](http://github.com/symfony/symfony/commit/968c870c9455c363ec14fed44e17313d6e4ec368 "968c870c9455c363ec14fed44e17313d6e4ec368 commit on github"): \[AsseticBundle\] コントローラにetagsを追加したのでフィルタなどが無効化された
  * [f46c6f7](http://github.com/symfony/symfony/commit/f46c6f7e45c0b046183932ae1b69e5b7500e535f "f46c6f7e45c0b046183932ae1b69e5b7500e535f commit on github"): \[Routing\] URLの%2f問題を修正
  * [e16c666](http://github.com/symfony/symfony/commit/e16c6662667eb7cf929ffd42415e72a54163cd7a "e16c6662667eb7cf929ffd42415e72a54163cd7a commit on github"): \[Routing\] からのパス情報が/にリダイレクトするように修正(ほかの/で終わっているルートに関して)
  * [b6049be](http://github.com/symfony/symfony/commit/b6049beca235eece6466d6ec612b3d11cb5c788e "b6049beca235eece6466d6ec612b3d11cb5c788e commit on github"), [381d1e2](http://github.com/symfony/symfony/commit/381d1e2da1410ddf8c9e2da07b4e4b8e1344adb7 "381d1e2da1410ddf8c9e2da07b4e4b8e1344adb7 commit on github"): \[Translation\] FallbackLocale Catalogueの検索を追加
  * [4b3c495](http://github.com/symfony/symfony/commit/4b3c49550f7a5cd21f774a103d8df9d2cb7dd719 "4b3c49550f7a5cd21f774a103d8df9d2cb7dd719 commit on github"): 静的コード分析によって見つかった問題を修正


> **NOTE**
> [@uechoco](http://twitter.com/uechoco) さんに翻訳していただいたものです。

