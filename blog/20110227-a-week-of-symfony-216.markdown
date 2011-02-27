A week of symfony #216 (14->20 February 2011)
=============================================

今週、Symfony2の必死な開発活動により、[セキュリティコンフィグレーションマージのサポート追加](https://github.com/symfony/symfony/commit/0b8fef234724cb4cb3a4ab37466efe193a6c7708)
[マージしたインテリジェントとシングルパスコンフィグロードの実装](https://github.com/symfony/symfony/commit/f9138d313b83f951cf82a2f7f902a2d6dd14fbb3) 
[新しいコンフィグレーションコンポーネントに共通のコンフィグクラスを移動](https://github.com/symfony/symfony/commit/5c905beb13624d40a768e6e9ea98cb873e149c6e)などのいくつかの大規模なコミットを組み込んだ。
加えて、新しいAsseticBundleはSymfony2に統合され、web assetsを処理するためにより強力で柔軟な方法を可能にします。
最後に、1.3.9および1.4.9メンテナンスバージョンがリリースされています。


開発メーリングリスト
------------------------

  * [[Symfony2] bootstrap.phpとbootstrap_cache.php](https://groups.google.com/forum/#!topic/symfony-devs/ZXthOcNpIRs)
  * [[Symfony2] RFC - コンテナからリクエストへデフォルトのスコープを変更](https://groups.google.com/forum/#!topic/symfony-devs/VvYiZjWLc3g)
  * [Git開発プロセス](https://groups.google.com/forum/#!topic/symfony-devs/EUyqKpvm_ms)
  * [[Symfony2] ZF2 依存性](https://groups.google.com/forum/#!topic/symfony-devs/ihFLt_mWpyw)
  * [[Symfony2] RFC: Symfony2のプロジェクトの構成](https://groups.google.com/forum/#!topic/symfony-devs/P0rqlbHkBn0)
  * [[Symfony2] DoctrineMigrationBundle](https://groups.google.com/forum/#!topic/symfony-devs/sTq0h2F3DHA)

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [f9138d3](http://github.com/symfony/symfony/commit/f9138d313b83f951cf82a2f7f902a2d6dd14fbb3 "f9138d313b83f951cf82a2f7f902a2d6dd14fbb3 commit on github"): [FrameworkBundle] FrameworkExtensionにマージしたインテリジェントオプションとシングルパスローディングの実装 (より簡単な処理とするためのコンフィグフォーマットの再構築と既存のコンフィグを壊す可能性のある重要な変更を追加)
  * [743f25a](http://github.com/symfony/symfony/commit/743f25a287ebcd0cc6b58e984e19544108b6ba28 "743f25a287ebcd0cc6b58e984e19544108b6ba28 commit on github"): [DependencyInjection] 定義については、明示的にfactoryClassプロパティを作成
  * [523e652](http://github.com/symfony/symfony/commit/523e652d9dcae71b143928df5f5eac02c7ce225a "523e652d9dcae71b143928df5f5eac02c7ce225a commit on github"): [FrameworkBundle] プロファイラコンフィグレーションワークの仕様を修正
  * [e540349](http://github.com/symfony/symfony/commit/e5403490e7ea226d19f4fb2b57bf209858caeea9 "e5403490e7ea226d19f4fb2b57bf209858caeea9 commit on github"): バンドルgetNamespace()およびgetPath()を定義する必要性を削除
  * [f56a6ef](http://github.com/symfony/symfony/commit/f56a6efbf5b86e9da8204ee53f07eb9f416b0916 "f56a6efbf5b86e9da8204ee53f07eb9f416b0916 commit on github"): [HttpFoundation] File/File.phpを完全にカバレージした
  * [bd97471](http://github.com/symfony/symfony/commit/bd97471954f18ac3843a618ccc968e2d297a3b80 "bd97471954f18ac3843a618ccc968e2d297a3b80 commit on github"): [HttpKernel] added test coverage for cache warmingのカバレージテストを追加
  * [c251a36](http://github.com/symfony/symfony/commit/c251a369351582324bf1afdd13b61ae01c3163a7 "c251a369351582324bf1afdd13b61ae01c3163a7 commit on github"): [HttpFoundation] Cookieのテストを追加
  * [9ba2943](http://github.com/symfony/symfony/commit/9ba2943aff2941c283065e0f09c05a572462fa50 "9ba2943aff2941c283065e0f09c05a572462fa50 commit on github"), [c5fb96b](http://github.com/symfony/symfony/commit/c5fb96b86b65ad0aa09f5c3ad5abada4f4f9a24e "c5fb96b86b65ad0aa09f5c3ad5abada4f4f9a24e commit on github"): [HttpKernel] Kernelのユニットテストを追加
  * [39ed62d](http://github.com/symfony/symfony/commit/39ed62de46718af993e06a99d5e5f1ddfd7a8cbf "39ed62de46718af993e06a99d5e5f1ddfd7a8cbf commit on github"): validators resourcesに日本語翻訳を追加
  * [42a3e40](http://github.com/symfony/symfony/commit/42a3e404b28def5e85a1912412a6eb2311cbaf48 "42a3e404b28def5e85a1912412a6eb2311cbaf48 commit on github"): validators resourcesにスペイン語翻訳を追加

  * [6ff4120](http://github.com/symfony/symfony/commit/6ff41207843154c1f5546de54755e56bc9d9efd5 "6ff41207843154c1f5546de54755e56bc9d9efd5 commit on github"), [09a50c3](http://github.com/symfony/symfony/commit/09a50c3c55257edb95c102cb435e353f0b118208 "09a50c3c55257edb95c102cb435e353f0b118208 commit on github"): [Form] オプションがtrueの場合(デフォルト)、参照によって変更された親フォームからオブジェクトを受信する「by_reference」フォームオプションを追加
  * [74d0ac8](http://github.com/symfony/symfony/commit/74d0ac82f7d4ef2539a7fa0114025cdfd8229c54 "74d0ac82f7d4ef2539a7fa0114025cdfd8229c54 commit on github"): [Form] ValueTransformerInterfaceクリーンアップ（CollectionToStringTransformer削除）
  * [0b8fef2](http://github.com/symfony/symfony/commit/0b8fef234724cb4cb3a4ab37466efe193a6c7708 "0b8fef234724cb4cb3a4ab37466efe193a6c7708 commit on github"): [Security/DependencyInjection] セキュリティコンフィグレーションをマージするためのサポートを追加した。どのようなフォーマットからかは関係なく同じ構造に変換され、全てコンフィグアレイに渡される(多くのメソッドと新しいアーキテクチャを追加した大規模なコミット)
  * [099b9de](http://github.com/symfony/symfony/commit/099b9dee1f4ad0ef411bb16fb38ab3a1ac91d1bb "099b9dee1f4ad0ef411bb16fb38ab3a1ac91d1bb commit on github"): [FrameworkBundle] コンフィグマージ、および正規化のためにConfiguration/Builderクラスに統合
  * [7ad4f99](http://github.com/symfony/symfony/commit/7ad4f99153eb496bed17bfe6f17edb18276e91b1 "7ad4f99153eb496bed17bfe6f17edb18276e91b1 commit on github"): [HttpFoundation] File/UploadedFile、MimeTest、Exceptionを完全にカバレージ
  * [b9ed739](http://github.com/symfony/symfony/commit/b9ed739d75fa59f5749be6c4b5ac15784fef2d91 "b9ed739d75fa59f5749be6c4b5ac15784fef2d91 commit on github"): RedirectControllerを修正 - 新しいURLを生成する前にpermanentアトリビュートを削除とテストを追加
  * [bebdcb2](http://github.com/symfony/symfony/commit/bebdcb242df685d822b7f0c4b712f67784401879 "bebdcb242df685d822b7f0c4b712f67784401879 commit on github"): [HttpKernel] ページがESIs構成されている場合、レスポンスのキャッシュ制御の変更の追加
  * [ea4ab77](http://github.com/symfony/symfony/commit/ea4ab77b6d0f6983b67aa7bd856d3873258c6913 "ea4ab77b6d0f6983b67aa7bd856d3873258c6913 commit on github"): [HttpKernel] HttpCacheはESIが存在する場合、キャッシュ制御ディレクティブをMaxAge=0で送信
  * [41bf849](http://github.com/symfony/symfony/commit/41bf849a637d9434f859eeafd816fec4a0ab51be "41bf849a637d9434f859eeafd816fec4a0ab51be commit on github"): [HttpFoundation] リクエストカバレージ
  * [9f30e42](http://github.com/symfony/symfony/commit/9f30e42c16ad24f5fd4dc512d2a85ffb785e5c26 "9f30e42c16ad24f5fd4dc512d2a85ffb785e5c26 commit on github"): consoleに--debug/-d、--env/-dを追加
  * [d447d22](http://github.com/symfony/symfony/commit/d447d22809e3751c5d6c13868c77a1657a8f04bd "d447d22809e3751c5d6c13868c77a1657a8f04bd commit on github"): [DoctrineBundle, DoctrineAbstractBundle, DoctrineMongoDBBundle] フィクスチャローダを認識するコンテナを追加
  * [5b95805](http://github.com/symfony/symfony/commit/5b95805340822da53aacc59229b747d590b26037 "5b95805340822da53aacc59229b747d590b26037 commit on github"), [f51dafc](http://github.com/symfony/symfony/commit/f51dafca3f181249ef58acb18d242a037a45371f "f51dafca3f181249ef58acb18d242a037a45371f commit on github"): [Form] フォームにdata_constructorオプションを追加
  * [9f77cab](http://github.com/symfony/symfony/commit/9f77cabd2fef2bbefa83a73312f94e297d74d8e0 "9f77cabd2fef2bbefa83a73312f94e297d74d8e0 commit on github"): [TwigBundle] twigのform_field()内のresources引数が非配列の場合、配列にキャスト
  * [5d87d83](http://github.com/symfony/symfony/commit/5d87d83a10ebf001c1609f626d27300479aba308 "5d87d83a10ebf001c1609f626d27300479aba308 commit on github"): Requestオブジェクトの重複の最適化
  * <del>[a8ec9b2](http://github.com/symfony/symfony/commit/a8ec9b27f044ea513c69442778c005cba7be8b1b "a8ec9b27f044ea513c69442778c005cba7be8b1b commit on github"): 新しいコンフィグコンポーネントに重複ファイルを移動</del> (復帰)
  * [82a8a3f](http://github.com/symfony/symfony/commit/82a8a3fb4234c5f5e87ec915f2ede1ad54b52dbf "82a8a3fb4234c5f5e87ec915f2ede1ad54b52dbf commit on github"): [WebProfilerBundle, FrameworkBundle] クロージャを正しく処理するためにイベントパネルを修正
  * <del>[f530808](http://github.com/symfony/symfony/commit/f53080860a2de21304ded72f5e6a9b6f8894dc0d "f53080860a2de21304ded72f5e6a9b6f8894dc0d commit on github"): リソースをコンフィグコンポーネントに移動</del> (復帰)
  * [fe694de](http://github.com/symfony/symfony/commit/fe694de7464ed18d9eb2947d7bc817bddde7965b "fe694de7464ed18d9eb2947d7bc817bddde7965b commit on github"), [2ed0b97](http://github.com/symfony/symfony/commit/2ed0b975f1799bbb18231166967951e1030a1c59 "2ed0b975f1799bbb18231166967951e1030a1c59 commit on github"), [5bf5933](http://github.com/symfony/symfony/commit/5bf593353f576e703c1b672a682935f437163545 "5bf593353f576e703c1b672a682935f437163545 commit on github"): \[Routing\] 任意のURL末尾のスラッシュに対応
  * [8cb3a23](http://github.com/symfony/symfony/commit/8cb3a237cc76176c7c31320ae85be85bcc197ca3 "8cb3a237cc76176c7c31320ae85be85bcc197ca3 commit on github"), [e929bc5](http://github.com/symfony/symfony/commit/e929bc5d1b3d958fc5b7d04308c21a4f61dc8cd2 "e929bc5d1b3d958fc5b7d04308c21a4f61dc8cd2 commit on github"): [FrameworkBundle, HttpKernel] サブリクエスト内の任意の2xxレスポンスコードを許可
  * [d85a839](http://github.com/symfony/symfony/commit/d85a83999704ccc958c7346fe869962b5b42b328 "d85a83999704ccc958c7346fe869962b5b42b328 commit on github"): [Routing] FileLoaderで解決しない限りファイルとしてインポートされたリソースの検索を無効化
  * [beaaa6d](http://github.com/symfony/symfony/commit/beaaa6d45720a0a8517c55aebc544dc000a086be "beaaa6d45720a0a8517c55aebc544dc000a086be commit on github"): [BrowserKit] Response::__toString()メソッドを複数ヘッダ対応に修正
  * <del>[19bbafc](http://github.com/symfony/symfony/commit/19bbafc441862d1d519e504386230253fcf9fbaa "19bbafc441862d1d519e504386230253fcf9fbaa commit on github"): [Security] セキュリティコンテキストのリファクタリング</del> (復帰)
  * [9749da6](http://github.com/symfony/symfony/commit/9749da6e52aa4f942e7e70b359e0c266a5e130e1 "9749da6e52aa4f942e7e70b359e0c266a5e130e1 commit on github"): [Security] PermissionGrantingStrategyのパフォーマンスの向上
  * [b3cb02a](http://github.com/symfony/symfony/commit/b3cb02adf237ff04526933259d689194070f3040 "b3cb02adf237ff04526933259d689194070f3040 commit on github"): [FrameworkBundle/Routing] 主なルータリソースに'type'オプション追加 (及びFrameworkExtensionコンフィグでこれを公開)
  * [a5cfc22](http://github.com/symfony/symfony/commit/a5cfc2207c09f6182333b3b812673202701c33f3 "a5cfc2207c09f6182333b3b812673202701c33f3 commit on github"): [Security/DependencyInjection] SecurityBundleのコンフィグレーションの更新とDICコンフィグクラスのいくつかのバグ修正
  * [8684055](http://github.com/symfony/symfony/commit/8684055bdfbd4e0579b9bd3ff51cf97c9942f629 "8684055bdfbd4e0579b9bd3ff51cf97c9942f629 commit on github"): プロジェクトのルートでないとき*_vendors.shスクリプトの呼び出しの修正
  * [f1633f8](http://github.com/symfony/symfony/commit/f1633f89c40e69dcef50865825ec1c1e80216eba "f1633f89c40e69dcef50865825ec1c1e80216eba commit on github"): install_vendors.shとupdate_vendors.shのマージ
  * [b716b70](http://github.com/symfony/symfony/commit/b716b707badcaac7858e17eff07eecb7e7d737df "b716b707badcaac7858e17eff07eecb7e7d737df commit on github"): DoctrineMongoDBBundleに不足している「proxy cache warmer」、「hydrator cache warmer」のコンソールコマンドの追加
  * [1292925](http://github.com/symfony/symfony/commit/12929257021741a9d0c0d4b0c2d05836208cb324 "12929257021741a9d0c0d4b0c2d05836208cb324 commit on github"): [AsseticBundle] asseticインテグレーションの初期エントリ
  * [5c905be](http://github.com/symfony/symfony/commit/5c905beb13624d40a768e6e9ea98cb873e149c6e "5c905beb13624d40a768e6e9ea98cb873e149c6e commit on github"), [8588d55](http://github.com/symfony/symfony/commit/8588d55c11285117ef953ff25a6636bc6b594077 "8588d55c11285117ef953ff25a6636bc6b594077 commit on github"): 共通コンフィグレーションクラスを新しいコンフィグコンポーネントに移動
  * [20e31cd](http://github.com/symfony/symfony/commit/20e31cd3f256b777dda0a8e880336578d8063089 "20e31cd3f256b777dda0a8e880336578d8063089 commit on github"): [HttpKernel] Kernel.phpとHttpKernel.phpに発生した2つの一般的エラーのため、いくつかの説明を追加
 added some details for two commonly encountered errors in Kernel.php and HttpKernel.php
  * [b9f4eab](http://github.com/symfony/symfony/commit/b9f4eab5c2be8fc29d671adf2fbbf8d065292466 "b9f4eab5c2be8fc29d671adf2fbbf8d065292466 commit on github"), [d22743c](http://github.com/symfony/symfony/commit/d22743cf3ace5110a2587c279f9055ec79b19ab7 "d22743cf3ace5110a2587c279f9055ec79b19ab7 commit on github"): [Security/Acl] 事前生成されたスキーマの追加
  * [0643dc4](http://github.com/symfony/symfony/commit/0643dc44fddf347f4ffdc5764b141bfadc54aeb8 "0643dc44fddf347f4ffdc5764b141bfadc54aeb8 commit on github"): [Security] security votersに優先順位属性を追加
  * [5c7fe8f](http://github.com/symfony/symfony/commit/5c7fe8f866decdae3c6f543405bf1e64d119844d "5c7fe8f866decdae3c6f543405bf1e64d119844d commit on github"): [Security] encoder factoryの実装を簡素化
  * [bc283f1](http://github.com/symfony/symfony/commit/bc283f1a66ccbdee2655274604fa87e970ca455b "bc283f1a66ccbdee2655274604fa87e970ca455b commit on github"): [Security] security.authentication_providerタグの削除
  * [b685b3a](http://github.com/symfony/symfony/commit/b685b3ab4d306eaa1838e14406a9e390564715bf "b685b3ab4d306eaa1838e14406a9e390564715bf commit on github"): [Security] logout successハンドラの追加
  * [af81bca](http://github.com/symfony/symfony/commit/af81bcabf06c389a353ffde2bb3e6158bdee3970 "af81bcabf06c389a353ffde2bb3e6158bdee3970 commit on github"), [5eee0db](http://github.com/symfony/symfony/commit/5eee0db18e158e350d4c143792a1ea1e54ddaeec "5eee0db18e158e350d4c143792a1ea1e54ddaeec commit on github"): [Templating] コンポーネントのリファクタリング
  * [73cd26e](http://github.com/symfony/symfony/commit/73cd26e2ca4fa3528e2ee5680fac6c82f7897724 "73cd26e2ca4fa3528e2ee5680fac6c82f7897724 commit on github"): [Serializer] 配列キーの先頭に@を使用してノードのattributeを追加する機能を追加
  * [4972bf6](http://github.com/symfony/symfony/commit/4972bf6350c3a2b68ccbd80171072f9f466787ef "4972bf6350c3a2b68ccbd80171072f9f466787ef commit on github"): [DependencyInjection] DICの拡張クラスのオプションからgetXsdValidationBasePath()およびgetNamespace()メソッドを作成
  * [81765f8](http://github.com/symfony/symfony/commit/81765f8b6a0cc341869b9f5593730b8317cdd406 "81765f8b6a0cc341869b9f5593730b8317cdd406 commit on github"): [DependencyInjection] XML loader修正
  * [7dbc09e](http://github.com/symfony/symfony/commit/7dbc09ed8b08a94b34184d7146ed1bf65c17fbc1 "7dbc09ed8b08a94b34184d7146ed1bf65c17fbc1 commit on github"): [Form] 検証に失敗した結果、場合によってはデータはドメインオブジェクトに書き込まれない。フォームの参照の処理の修正
  * [922cb0a](http://github.com/symfony/symfony/commit/922cb0a8323f749c334f2885c1ac2e909f690295 "922cb0a8323f749c334f2885c1ac2e909f690295 commit on github"): ベンダーのスクリプトは特定のコミットをチェックアウトできるようにする更新
  * [b8d5740](http://github.com/symfony/symfony/commit/b8d574087f29b3637d71fadceb678859d3e608c6 "b8d574087f29b3637d71fadceb678859d3e608c6 commit on github"): [Security] 認証トークンは、attributesを保持する許可
  * [14aa95b](http://github.com/symfony/symfony/commit/14aa95ba218c9fd6d02e770e279ed854314fea75 "14aa95ba218c9fd6d02e770e279ed854314fea75 commit on github"): あなたがコンフィグファイルに誤ったコンフィグレーションエイリアスを使用している場合、より良い規則とより適切なエラーメッセージを可能にする、バンドルのDIC拡張の主要なコンセプトの追加。
  * [7f182bd](http://github.com/symfony/symfony/commit/7f182bd877a88f36acadb2e2e7664f96aac55261 "7f182bd877a88f36acadb2e2e7664f96aac55261 commit on github"), [62e3053](http://github.com/symfony/symfony/commit/62e305376945022e0efb91a1f3a98d6eb2538749 "62e305376945022e0efb91a1f3a98d6eb2538749 commit on github"): 暗黙のうちに、登録されているすべてのバンドルをロードされ、すべてのローディングは、load()によって処理される。拡張が明示的にfalse設定されていた場合ローディングは無効となる
  * [a29a413](http://github.com/symfony/symfony/commit/a29a413c4828332fb87038dc436326cb3c306170 "a29a413c4828332fb87038dc436326cb3c306170 commit on github"): 静的メンバの代わりにコンテナのDICの拡張メンバを作成
  * [1230bc6](http://github.com/symfony/symfony/commit/1230bc64419539c630b218b6e5204af800a97b75 "1230bc64419539c630b218b6e5204af800a97b75 commit on github"): [AsseticBundle] 新しいLESSフィルタのコンフィグを更新
  * [cd5b603](http://github.com/symfony/symfony/commit/cd5b60359d3af704c0e051ceb0370f53731c0962 "cd5b60359d3af704c0e051ceb0370f53731c0962 commit on github"): [AsseticBundle] コントローラにローカルキャッシュを追加
  * [e62031a](http://github.com/symfony/symfony/commit/e62031a54e1902cf54c1d2001772fba8357a7ba6 "e62031a54e1902cf54c1d2001772fba8357a7ba6 commit on github"): [AsseticBundle] .jarコンフィグレーションのクロージャを修正
  * [dfd9218](http://github.com/symfony/symfony/commit/dfd921822a534dd5d88927560047c63a7595f8ac "dfd921822a534dd5d88927560047c63a7595f8ac commit on github"): [Security/Http] form-loginにCSRF保護を追加
  * [82c6844](http://github.com/symfony/symfony/commit/82c684414757af8951cef3bf0ec1b36d98f62aba "82c684414757af8951cef3bf0ec1b36d98f62aba commit on github"): [Security] SecurityExtensionのクリーンアップにしたがって、DoctrineBundleからセキュリティクラスを移動
  * [53f3ff8](http://github.com/symfony/symfony/commit/53f3ff8258d4efa4082d50ca0dd01f8c731b4dad "53f3ff8258d4efa4082d50ca0dd01f8c731b4dad commit on github"): [Security] user providerにチェインを追加
  * [1593d6f](http://github.com/symfony/symfony/commit/1593d6f75deab634e6e31208ac0ee89f942a01e6 "1593d6f75deab634e6e31208ac0ee89f942a01e6 commit on github"): [Form] FieldInterface::isEmpty()メソッドの追加
  * [40acc6a](http://github.com/symfony/symfony/commit/40acc6ac79ecafb897bbf301259ac3620a312a39 "40acc6ac79ecafb897bbf301259ac3620a312a39 commit on github"): [Form] fixed ゼロと空を区別するためにChoiceField::isChoiceSelected()を修正
  * [14c3518](http://github.com/symfony/symfony/commit/14c3518c6e4198db0c2d133f01614df7364ef8d8 "14c3518c6e4198db0c2d133f01614df7364ef8d8 commit on github"): [Form] DateFieldまたはTimeFieldがセレクトボックスに表示されている場合、allまたはnoにも関わらず選択ボックスがセレクトボックスが値を選択されている必要がある修正
  * [df011ed](http://github.com/symfony/symfony/commit/df011ed1efc2de81396b37094fda1688711e71c8 "df011ed1efc2de81396b37094fda1688711e71c8 commit on github"): [Form] TimeFieldとDateFieldのisXXXWithinRange()メソッドは空のドロップダウンを無視する修正
  * [9569262](http://github.com/symfony/symfony/commit/9569262635344223041c3812cbc48fc2838e9b31 "9569262635344223041c3812cbc48fc2838e9b31 commit on github"): [Form] 日付処理クラスは、デフォルトではサーバのタイムゾーンを使用する修正
  * [077d192](http://github.com/symfony/symfony/commit/077d1921b3d35d5bc8bc3aec2af579a24fa8c59b "077d1921b3d35d5bc8bc3aec2af579a24fa8c59b commit on github"): Builderでのvalidationのサポートを追加
  * [990910d](http://github.com/symfony/symfony/commit/990910d601e9a34ddf11fdf7076fda4c15994a3a "990910d601e9a34ddf11fdf7076fda4c15994a3a commit on github"): SwiftmailerBundleは、Configurationクラスを使用するように変換
  * [0a33cbb](http://github.com/symfony/symfony/commit/0a33cbb4033a12b6aab499352d0d580c487bcd95 "0a33cbb4033a12b6aab499352d0d580c487bcd95 commit on github"): [Finder] 相対パスのサポートが追加
  * [c5e4dfb](http://github.com/symfony/symfony/commit/c5e4dfb5a631d1144eb02ea59793a38e7335898d "c5e4dfb5a631d1144eb02ea59793a38e7335898d commit on github"): [DependencyInjection] サービスが無効なタグ値を指定されている場合、InvalidArgumentExceptionメッセージで明らかにする追加
  * [6b12c21](http://github.com/symfony/symfony/commit/6b12c212615a285a43124b70b27b476e6d5c7ccd "6b12c212615a285a43124b70b27b476e6d5c7ccd commit on github"): DependencyInjection/ConfigurationをConfig/Definitionへ移動
  * [76262b2](http://github.com/symfony/symfony/commit/76262b2ccc2129d967a6a5bb9e7dae6f73d35968 "76262b2ccc2129d967a6a5bb9e7dae6f73d35968 commit on github"): spool処理を修正

