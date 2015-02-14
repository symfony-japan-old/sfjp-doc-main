---
layout: default
title: A week of symfony #221 (21->27 March 2011)
---

A week of symfony #221 (21->27 March 2011)
==========================================

今週のSymfony2は最終リリースに向けて準備するために開発ペースを加速させた。プロパティとメソッドのTonsはprotectedからprivateに切替、パブリックAPIのタグ付け開始、 ([0f231c3](https://github.com/symfony/symfony/commit/0f231c33e5971662287840e503d29d049bd5d132)),HTTP例外はリファクタリング、コンポーネント間の初めてのBridgeがコミット、 ([3e5bd67](http://github.com/symfony/symfony/commit/3e5bd67dac9da58ff7daf71b3ffa74bebb4127f9))、 [Twig 1.0.0がリリース](http://blog.twig-project.org/post/4140267310/twig-1-0-0-released)、[新しいバージョンのcache:clearコマンド](https://github.com/symfony/symfony/commit/e4a636a8851af4330a0ebafbf642166c2e8cb5d7)がフレームワークユーティリティに追加された。

加えて、[フォームリファクタリング](https://github.com/symfony/symfony/pull/399).の大規模なプルリクエストなどいくつかの他の重要な変更がまだコミットされるのを待っている。

最後に、symfonyはsymfony1.3.xの最後のブランチ開発である1.3.10と1.4.10のセキュリティリリースを今週公開した。
 
開発メーリングリスト
------------------------

  * [PUT/DELETEリクエストのデータ](https://groups.google.com/forum/#!topic/symfony-devs/ku3Tx3Ms3UQ)
  * [[Symfony2] レスポンスサブクラス vs HTTPステータスコードの例外](https://groups.google.com/forum/#!topic/symfony-devs/oVEuzS7U29Y)
  * [Admin Generatorのステータス](https://groups.google.com/forum/#!topic/symfony-devs/N1wlvj1F5Eo)
  * [キャッシュの問題：Shell vs Webserver Rights](https://groups.google.com/forum/#!topic/symfony-devs/sfL107aEyiU)
  * [[symfony2] Validatorはこれで良い？](https://groups.google.com/forum/#!topic/symfony-devs/v-fSW0JvFlA)

symfony 1 開発ハイライト
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=27%2F03%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [1.3.10マイルストーンの完了](http://trac.symfony-project.org/milestone/1.3.10)
  * [1.4.10マイルストーンの完了](http://trac.symfony-project.org/milestone/1.4.10)


Symfony2開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [06bfe82](http://github.com/symfony/symfony/commit/06bfe82bc11992e9488f7b915927684e0e433a63 "06bfe82bc11992e9488f7b915927684e0e433a63 commit on github"): [DoctrineMongoDBBundle] doctrine:mongodb:cache:clear-metadataコマンドの追加
  * [b00a903](http://github.com/symfony/symfony/commit/b00a903858aefc83942adfc5ec105bdefd4f21b8 "b00a903858aefc83942adfc5ec105bdefd4f21b8 commit on github"): [FrameworkBundle] いくつかのコマンドのclearDir()メソッドの削除（Filesystem::remove() 使用の代わり）
  * [45f9c2f](http://github.com/symfony/symfony/commit/45f9c2fbf4b200d50fd18224522f88f1533b903d "45f9c2fbf4b200d50fd18224522f88f1533b903d commit on github"), [00d4788](http://github.com/symfony/symfony/commit/00d47889a2a9986d17483991c0b7c43e14618179 "00d47889a2a9986d17483991c0b7c43e14618179 commit on github"), [5a528bc](http://github.com/symfony/symfony/commit/5a528bcb5537d47c9dc0e31e61c86aad9d22c06c "5a528bcb5537d47c9dc0e31e61c86aad9d22c06c commit on github"), [e520956](http://github.com/symfony/symfony/commit/e5209566242b1060664fc45a5152ec6f6c2224a5 "e5209566242b1060664fc45a5152ec6f6c2224a5 commit on github"), [9cf9f67](http://github.com/symfony/symfony/commit/9cf9f674e8683db0f003c3cdedcb69550d1b4e58 "9cf9f674e8683db0f003c3cdedcb69550d1b4e58 commit on github"), [e4a636a](http://github.com/symfony/symfony/commit/e4a636a8851af4330a0ebafbf642166c2e8cb5d7 "e4a636a8851af4330a0ebafbf642166c2e8cb5d7 commit on github"), [85778ca](http://github.com/symfony/symfony/commit/85778caba16ad6830fdc28eaa6ee8c1e91d009ef "85778caba16ad6830fdc28eaa6ee8c1e91d009ef commit on github"), [6ec84ba](http://github.com/symfony/symfony/commit/6ec84bad7621768be513192eb7a666c82c8b01a5 "6ec84bad7621768be513192eb7a666c82c8b01a5 commit on github"): cache:clearコマンドの追加
  * [b2f5ac8](http://github.com/symfony/symfony/commit/b2f5ac8beb6f18f802ee43ef1bed193670184e72 "b2f5ac8beb6f18f802ee43ef1bed193670184e72 commit on github"): [Routing] URLマッチオングの405 Method Not Allowedレスポンスサポートのリファクタリング
  * [10dc18b](http://github.com/symfony/symfony/commit/10dc18b28b273a257c94768709a42b3ccf08affb "10dc18b28b273a257c94768709a42b3ccf08affb commit on github"): [HttpKernel] HTTP例外がより柔軟性をもつようにリファクタリング
  * [2217a0d](http://github.com/symfony/symfony/commit/2217a0d7e46ef0ab5c6cef8fd160568200a86b25 "2217a0d7e46ef0ab5c6cef8fd160568200a86b25 commit on github"): [FrameworkBundle] 405 Method Not Foundレスポンスサポートの更新
  * [f93e4b2](http://github.com/symfony/symfony/commit/f93e4b2d73b9ae970af9529d4165f422ae2ff93b "f93e4b2d73b9ae970af9529d4165f422ae2ff93b commit on github"): ルーティングの注釈を含む新しいコントローラのファイルが追加されている場合、手動でキャッシュをクリアする必要性を排除
  * [9ee9f55](http://github.com/symfony/symfony/commit/9ee9f5552b43010dbbefac0cf2654cb70b8e91d2 "9ee9f5552b43010dbbefac0cf2654cb70b8e91d2 commit on github"): [FrameworkBundle] ベースコントローラに戻すためのリダイレクトメソッドを追加
  * [517ce9c](http://github.com/symfony/symfony/commit/517ce9c9239b6a462e9e07367e9508afd9ee0541 "517ce9c9239b6a462e9e07367e9508afd9ee0541 commit on github"): [AsseticBundle] バンドルの表記にグロブの基本的なサポートの追加
  * [e159c47](http://github.com/symfony/symfony/commit/e159c47cc92d35f4d85fcc523d6de7938cf315d0 "e159c47cc92d35f4d85fcc523d6de7938cf315d0 commit on github"): [Routing] メソッドが必要とされていない時にUrlMatcherが定義される事を修正
  * [a95f72f](http://github.com/symfony/symfony/commit/a95f72fff33bec7a357d835aea1edb88b7908cd7 "a95f72fff33bec7a357d835aea1edb88b7908cd7 commit on github"): [Routing] 多くのテストを追加
  * [98d03d1](http://github.com/symfony/symfony/commit/98d03d1aec728d6b1b6026e133b8e96e960c18ef "98d03d1aec728d6b1b6026e133b8e96e960c18ef commit on github"): [FrameworkBundle] Bundle:Controller:Actionコントローラクラスが見つからない場合、より具体的なメッセージを伝える
  * [a229410](http://github.com/symfony/symfony/commit/a2294106fb8eee0f9cdb10bf9b190c52485bd551 "a2294106fb8eee0f9cdb10bf9b190c52485bd551 commit on github"): リソースをメインのapp/ディレクトリ下を探すのを修正。すべてのリソースをグローバルに保存することができる。新いディレクトリはapp/Resources/...となる。
  * [3e5bd67](http://github.com/symfony/symfony/commit/3e5bd67dac9da58ff7daf71b3ffa74bebb4127f9 "3e5bd67dac9da58ff7daf71b3ffa74bebb4127f9 commit on github"), [9595963](http://github.com/symfony/symfony/commit/9595963c2b78721a2ace60e622c03428ac318c25 "9595963c2b78721a2ace60e622c03428ac318c25 commit on github"): RoutingとTwigのSymfony Bridgeでの統合を移動
  * [e912b34](http://github.com/symfony/symfony/commit/e912b347f01a85f0b24198c478cad129a0d22941 "e912b347f01a85f0b24198c478cad129a0d22941 commit on github"): TranslationコンポーネントとTwigのSymfony Bridgeでの統合を移動
  * [82dec51](http://github.com/symfony/symfony/commit/82dec51b300eed6a2a1f98dd2ae997435581a41e "82dec51b300eed6a2a1f98dd2ae997435581a41e commit on github"): YamlコンポーネントとTwigのSymfony Bridgeでの統合を移動
  * [662a4b3](http://github.com/symfony/symfony/commit/662a4b374089ed4b3b05afe650c9fbedde067b05 "662a4b374089ed4b3b05afe650c9fbedde067b05 commit on github"): HttpExceptionからのステータスメッセージを削除、最も有用な引数が最初となるようにシグネチャを変更しました。以前のHTTP例外のリファクタリングで導入された修正による多くの小さな問題を修正
  * [b585752](http://github.com/symfony/symfony/commit/b5857528e0b04f6f584030090fecc7b543ce359b "b5857528e0b04f6f584030090fecc7b543ce359b commit on github"): [Routing] 
moved most of the properties and methods from protected to private
  * [e4a3e0c](http://github.com/symfony/symfony/commit/e4a3e0c2c77b85116d8149da28a3e1e1e5206e17 "e4a3e0c2c77b85116d8149da28a3e1e1e5206e17 commit on github"): [Config] ほとんどのプロパティとメソッドのprotectedからにprivateへ移動
  * [1b8dc80](http://github.com/symfony/symfony/commit/1b8dc8021541ee44105ce6236bc2c166b64fa557 "1b8dc8021541ee44105ce6236bc2c166b64fa557 commit on github"): [HttpKernel] ほとんどのプロパティとメソッドのprotectedからにprivateへ移動
  * [55671be](http://github.com/symfony/symfony/commit/55671be888f6219a14898f0e59c84ce038ef5637 "55671be888f6219a14898f0e59c84ce038ef5637 commit on github"): [Templating] protocol-relative URLを残してassets helperを更新
  * [a6e6cbb](http://github.com/symfony/symfony/commit/a6e6cbbb27e57107fe18d9c178d81c3185094f88 "a6e6cbbb27e57107fe18d9c178d81c3185094f88 commit on github"): [HttpFoundation] RequestMatcherから^と$のハードコーディングを削除
  * [eeca46d](http://github.com/symfony/symfony/commit/eeca46dea0aa34a97fe03040335791c90731d349 "eeca46dea0aa34a97fe03040335791c90731d349 commit on github"): [CssSelector] ほとんどのプロパティとメソッドのprotectedからにprivateへ移動
  * [639d93c](http://github.com/symfony/symfony/commit/639d93cbbf29750d443063316fe133b66a80de6c "639d93cbbf29750d443063316fe133b66a80de6c commit on github"): [Process] ほとんどのプロパティとメソッドのprotectedからにprivateへ移動
  * [2f8d5cd](http://github.com/symfony/symfony/commit/2f8d5cd1c04b588ccc43fa3c6d3f79a041192bd7 "2f8d5cd1c04b588ccc43fa3c6d3f79a041192bd7 commit on github"): [FrameworkBundle] asset packagesのconfigのビルドの修正
  * [9c6a6e1](http://github.com/symfony/symfony/commit/9c6a6e13bf61e3bed3684e50c2b3ccc7f493b0aa "9c6a6e13bf61e3bed3684e50c2b3ccc7f493b0aa commit on github"): [Validator] コールバックを実行する制約のリネーム
  * [3e29348](http://github.com/symfony/symfony/commit/3e29348d21e848757f8dbf69a46ab6aa41e39fe2 "3e29348d21e848757f8dbf69a46ab6aa41e39fe2 commit on github"): [Validator] コールバック制約に静的なコールバックのサポートを追加
  * [bedbe51](http://github.com/symfony/symfony/commit/bedbe51081fc57abf792a08cb3cfdb770717b07e "bedbe51081fc57abf792a08cb3cfdb770717b07e commit on github"): [Security] $objectがObjectIdentityInterfaceのインスタンスでなければACL:AclVoter::voteはObjectIdentityを取得
  * [2e1924e](http://github.com/symfony/symfony/commit/2e1924ec1c6174b354174215393303afea443d89 "2e1924ec1c6174b354174215393303afea443d89 commit on github"): [AsseticBundle] Assetic変更の更新
  * [8d84fdf](http://github.com/symfony/symfony/commit/8d84fdfedc73a5ac3bbb9802695687eebb2ed514 "8d84fdfedc73a5ac3bbb9802695687eebb2ed514 commit on github"): [Finder] いくつかのFinderインスタンスを結合できるようにするFinder::append() メソッドを追加
  * [124f1d8](http://github.com/symfony/symfony/commit/124f1d8e44496452697030fe6e90e1d3b28eefbf "124f1d8e44496452697030fe6e90e1d3b28eefbf commit on github"), [cc46e8d](http://github.com/symfony/symfony/commit/cc46e8d46aca8bf34ca3c2eab7d968b70d2db6c7 "cc46e8d46aca8bf34ca3c2eab7d968b70d2db6c7 commit on github"): FilesystemクラスをFrameworkBundleからHttpKernelに移動（リファクタリングはわずか）
  * [4de468e](http://github.com/symfony/symfony/commit/4de468e181910f02100f19fde06faa700cd78016 "4de468e181910f0に2100f19fde06faa700cd78016 commit on github"): [Routing] generate()にオプションのパラメータの引数を作成
  * [1910e23](http://github.com/symfony/symfony/commit/1910e23df8a6d9cd1f3d05b1531640eea0bcc2ef "1910e23df8a6d9cd1f3d05b1531640eea0bcc2ef commit on github"): [FrameworkBundle] chromeで表示するには少し長いのでデフォルトのエラーページタイトルタグを追加
  * [6799090](http://github.com/symfony/symfony/commit/6799090a4fedfe1d55764c8fcdff9af5547d19f7 "6799090a4fedfe1d55764c8fcdff9af5547d19f7 commit on github"): [SwiftmailerBundle] Swift_NullTransportをConfigurationクラスでの選択を許可
  * [80c1027](http://github.com/symfony/symfony/commit/80c102761cf5f75678364e6bad12eae52d690617 "80c102761cf5f75678364e6bad12eae52d690617 commit on github"): [HttpKernel] ユーザーがコントローラのreturn文を忘れている可能性がある場合、「コントローラから返された応答がない」メッセージを作成
  * [c2579aa](http://github.com/symfony/symfony/commit/c2579aa2000f19fc57f9a1f9d8ec4f334d86d818 "c2579aa2000f19fc57f9a1f9d8ec4f334d86d818 commit on github"): [AsseticBundle] イベントを再削除

