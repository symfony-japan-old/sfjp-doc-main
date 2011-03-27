A week of symfony #220 (14->20 March 2011)
==========================================

今週、[国際拡張の要件](https://groups.google.com/forum/#!topic/symfony-devs/RBtwBObsLCE)に関連していくつかの問題を防ぐため、Symfony2は新しい国際拡張スタブを得た。また、おそらくSymfony2コードの最後の大きな変更となる[新しいイベントマネージャ](https://github.com/symfony/symfony/commit/699e046b4f0022fbd510a917efef9cf8b9587ed2) がコミットされた。最後に、symfony-docsリポジトリはSymfony2が安定化していきそのドキュメントが改善していく[たくさんのコミットを受信](https://github.com/symfony/symfony-docs/commits)した。
 
開発メーリングリスト
------------------------

  * [SEからFrameworkExtraBundleを削除すべき](https://groups.google.com/forum/#!topic/symfony-devs/hzsfPn7bTfw)
  * [[symfony2] SecurityBundle & UserBundle](https://groups.google.com/forum/#!topic/symfony-devs/dm8t8DBAZsE)
  * [[Symfony2] SCのパラメータ](https://groups.google.com/forum/#!topic/symfony-devs/2cPoSHY1HWI)
  * [[Symfony2] bootstrapファイル](https://groups.google.com/forum/#!topic/symfony-devs/4AKypCKmaFA)
  * [Alternateイベントの実装](https://groups.google.com/forum/#!topic/symfony-devs/LfGFzdEzTqk)

Symfony2開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [481bb4c](http://github.com/symfony/symfony/commit/481bb4cdf9179c2756f7ad7dc543ecaa8d4921dd "481bb4cdf9179c2756f7ad7dc543ecaa8d4921dd commit on github"): [WebProfilerBundle] ツールバー項目のテンプレートへの取込
  * [f752dd3](http://github.com/symfony/symfony/commit/f752dd34a0d366467e41d0c8a4ab90fb4e7e6ae8 "f752dd34a0d366467e41d0c8a4ab90fb4e7e6ae8 commit on github"): [Profiler] プロファイラはビジュアルフィードバックに使用されるステータスを返す
 (取消)
  * [5b39894](http://github.com/symfony/symfony/commit/5b39894efcb044fd6385f38392006a05f0614f08 "5b39894efcb044fd6385f38392006a05f0614f08 commit on github"): [WebProfilerBundle] ツールバーのパネルへのショートカットを追加
  * [b04a647](http://github.com/symfony/symfony/commit/b04a647c6536b93d2b6cdec369d01f051c5351aa "b04a647c6536b93d2b6cdec369d01f051c5351aa commit on github"), [36d51d7](http://github.com/symfony/symfony/commit/36d51d7bbd959dbba63155af53c7b86df0862ec2 "36d51d7bbd959dbba63155af53c7b86df0862ec2 commit on github"): [WebProfilerBundle] 設定パネルを作成
  * [0f0539f](http://github.com/symfony/symfony/commit/0f0539f983e23f83c7d113d594e0d739b51e682e "0f0539f983e23f83c7d113d594e0d739b51e682e commit on github"): [FrameworkBundle] init:bundle後、ユーザーのための多くの情報の追加
  * [138ef0d](http://github.com/symfony/symfony/commit/138ef0d1ae641e71048ce57e1d2a1e52f58aaa04 "138ef0d1ae641e71048ce57e1d2a1e52f58aaa04 commit on github"), [f657d0e](http://github.com/symfony/symfony/commit/f657d0e85d662c9658324a4e5a9f39587ed523c6 "f657d0e85d662c9658324a4e5a9f39587ed523c6 commit on github"): [DoctrineBunble, DoctrineMongoDBBundle] doctrine:mapping:infoコマンドの出力の改善
  * [d2cc5a0](http://github.com/symfony/symfony/commit/d2cc5a048a37e1abc23a50c259cd1fe2e16ada63 "d2cc5a048a37e1abc23a50c259cd1fe2e16ada63 commit on github"), [629451a](http://github.com/symfony/symfony/commit/629451a34537fe475a9e6f9d25196768c5214720 "629451a34537fe475a9e6f9d25196768c5214720 commit on github"): [DoctrineBundle, DoctrineMongoDBBundle] improved error exceptions thrown when loading data fixturesデータフィクスチャをロードする時のエラー例外のスローの改善
  * [25931ca](http://github.com/symfony/symfony/commit/25931caeabe546cf3708dca8a4cce21047196a03 "25931caeabe546cf3708dca8a4cce21047196a03 commit on github"), [699e046](http://github.com/symfony/symfony/commit/699e046b4f0022fbd510a917efef9cf8b9587ed2 "699e046b4f0022fbd510a917efef9cf8b9587ed2 commit on github"), [06c682b](http://github.com/symfony/symfony/commit/06c682b4fb8b68606d461db431e1f1a2d3671cb4 "06c682b4fb8b68606d461db431e1f1a2d3671cb4 commit on github"), [663b0a9](http://github.com/symfony/symfony/commit/663b0a97acc5d2b67f349e056521c39f90cc7934 "663b0a97acc5d2b67f349e056521c39f90cc7934 commit on github"): [EventDispatcher] 新しいイベントマネージャのコミット
  * [157f001](http://github.com/symfony/symfony/commit/157f0012531392fb759eb3035ab59b6ef22f3968 "157f0012531392fb759eb3035ab59b6ef22f3968 commit on github"), [73464f4](http://github.com/symfony/symfony/commit/73464f411ebdc9f675df4e8acc36a3be19afca34 "73464f411ebdc9f675df4e8acc36a3be19afca34 commit on github"): 最初のPHP国際拡張スタブのコミット
  * [19aa266](http://github.com/symfony/symfony/commit/19aa266b6a8974334d6f5c88dc50cbb468f9768c "19aa266b6a8974334d6f5c88dc50cbb468f9768c commit on github"): [DoctrineBundle] 何も設定がされていない時、デフォルトとして最初のエンティティマネージャを使用
  * [ed4e945](http://github.com/symfony/symfony/commit/ed4e9456c8242aa5d15fdcc4cea247dc2d26e01a "ed4e9456c8242aa5d15fdcc4cea247dc2d26e01a commit on github"): [DoctrineMongoDBBundle] 何も設定がされていない時、デフォルトとして最初のドキュメントマネージャを使用
  * [f4e4a2a](http://github.com/symfony/symfony/commit/f4e4a2aa1b1a4279057ff43c7c9a59f8124746fa "f4e4a2aa1b1a4279057ff43c7c9a59f8124746fa commit on github"): ConfigCacheのリファクタリングとcontainer:debugタスクの最適化
  * [98216a9](http://github.com/symfony/symfony/commit/98216a9af25a58f175f2f3dc8099f6dac880c0b5 "98216a9af25a58f175f2f3dc8099f6dac880c0b5 commit on github"): [DependencyInjection] いくつかの例外のリファクタリング
  * [cef7089](http://github.com/symfony/symfony/commit/cef70893dfb6533832ccbcce192d7be6ecebc072 "cef70893dfb6533832ccbcce192d7be6ecebc072 commit on github"): [HttpKernel, FrameworkBundle] getContainerClassメソッドとkernel.container_classパラメータの追加
  * [d1ebc8d](http://github.com/symfony/symfony/commit/d1ebc8da9faaaa901432ecae129a734bc1a80ed2 "d1ebc8da9faaaa901432ecae129a734bc1a80ed2 commit on github"), [bbfb1ff](http://github.com/symfony/symfony/commit/bbfb1ffb53ee3510f62688252feda0d84ebc54ae "bbfb1ffb53ee3510f62688252feda0d84ebc54ae commit on github"): 抽象的なPDOのプロファイラのストレージを追加、SQLiteストレージ更新、mysqlのストレージを追加。フレームワークバンドルのconfigプロファイラを更新
  * [345e2d3](http://github.com/symfony/symfony/commit/345e2d39b51c61b907c5bba444e465ff2637bfe5 "345e2d39b51c61b907c5bba444e465ff2637bfe5 commit on github"), [44c95f9](http://github.com/symfony/symfony/commit/44c95f97a4a93890901eb35f9631b32ea0da3550 "44c95f97a4a93890901eb35f9631b32ea0da3550 commit on github"), [39504fc](http://github.com/symfony/symfony/commit/39504fc98d98f4487e2a8dfec890a3a3e1a37f5f "39504fc98d98f4487e2a8dfec890a3a3e1a37f5f commit on github"), [11f42a8](http://github.com/symfony/symfony/commit/11f42a82dc9b3b4f578a699f138d7bb99046505e "11f42a82dc9b3b4f578a699f138d7bb99046505e commit on github"), [db27b4d](http://github.com/symfony/symfony/commit/db27b4d288791d5cf3a68b0ff59508f9484db201 "db27b4d288791d5cf3a68b0ff59508f9484db201 commit on github"): [SecurityBundle] WDTのセキュリティタブを調整
  * [5c2e089](http://github.com/symfony/symfony/commit/5c2e0898d104d3ec5571474610fb854faa9a7b6b "5c2e0898d104d3ec5571474610fb854faa9a7b6b commit on github"): [DoctrineBundle] コンフィグレーションを介してカスタムDQL関数を登録する方法を追加
  * [b638cf0](http://github.com/symfony/symfony/commit/b638cf07a5865ed93efda9cf223d79897ee78277 "b638cf07a5865ed93efda9cf223d79897ee78277 commit on github"): [SecurityBundle] HTTPベーシックおよびダイジェスト認証のrealm設定を作成
  * [2610e1b](http://github.com/symfony/symfony/commit/2610e1b69959add9793afd399291dc846001fb78 "2610e1b69959add9793afd399291dc846001fb78 commit on github"): [SecurityBundle] X509証明認証のためにユーザと資格情報の設定を作成
  * [2cf0601](http://github.com/symfony/symfony/commit/2cf0601f1871f0d837874028c7b1e44302349ab0 "2cf0601f1871f0d837874028c7b1e44302349ab0 commit on github"): [SecurityBundle] デフォルトではランダムのanonymous keyパラメータの設定を作成
  * [61abc3d](http://github.com/symfony/symfony/commit/61abc3d01f5a09016cbc739bfc87ef7d0b4bb169 "61abc3d01f5a09016cbc739bfc87ef7d0b4bb169 commit on github"): PHPテンプレートもグローバル変数を追加
  * [28d9b33](http://github.com/symfony/symfony/commit/28d9b331bd9adbfa04a04bfef85c77e9ca62a6cf "28d9b331bd9adbfa04a04bfef85c77e9ca62a6cf commit on github"): [FrameworkBundle] プロファイラに簡単な設定を作成
  * [df08655](http://github.com/symfony/symfony/commit/df08655e97e33d17a8e719ce36c23efdb1b9a0a8 "df08655e97e33d17a8e719ce36c23efdb1b9a0a8 commit on github"): SwiftmailerBundleにDataCollectorを追加
  * [e8b0b48](http://github.com/symfony/symfony/commit/e8b0b488cb7a9b2bb667eaf0920ab2ce5907400c "e8b0b488cb7a9b2bb667eaf0920ab2ce5907400c commit on github"): [HttpKernel] 独自のメソッドに例外管理ロジックを移動
  * [de57480](http://github.com/symfony/symfony/commit/de5748070da42105eb3ecb84793066d7cf56a28f "de5748070da42105eb3ecb84793066d7cf56a28f commit on github"): [FrameworkBundle] 現在、実装することができないのでDIタグのサポートのEventSubscriberを削除
  * [ab57e5c](http://github.com/symfony/symfony/commit/ab57e5c61165897c1239bab9cb1b8bb193696b0b "ab57e5c61165897c1239bab9cb1b8bb193696b0b commit on github"): [HttpKernel] HttpKernelイベントに多くのコードのドキュメントを追加
  * [466f1b9](http://github.com/symfony/symfony/commit/466f1b99c50a82722bccdeb68fede04f85dc7b0b "466f1b99c50a82722bccdeb68fede04f85dc7b0b commit on github"), [1219b98](http://github.com/symfony/symfony/commit/1219b98ec5f8129b2aad3af6eab09f381b3410d4 "1219b98ec5f8129b2aad3af6eab09f381b3410d4 commit on github"): [Security] ファイアウォールのリスナーのメソッド名の修正
  * [1e0ed22](http://github.com/symfony/symfony/commit/1e0ed22c55115eb09838972c9246d68e59285147 "1e0ed22c55115eb09838972c9246d68e59285147 commit on github"): [Config] コンポーネントリファクタリング。構成コンポーネントAPIが変更され、拡張の設定ファイルを変更に応じて更新する必要がある。
  * [65681cd](http://github.com/symfony/symfony/commit/65681cdc8577dad0ef4fc6b0f5b4cedefca0529a "65681cdc8577dad0ef4fc6b0f5b4cedefca0529a commit on github"): [Console] 出力フォーマッタインターフェイスの追加
  * [e5700b8](http://github.com/symfony/symfony/commit/e5700b817bdce1c96bafedb4ec3493f1aa22d552 "e5700b817bdce1c96bafedb4ec3493f1aa22d552 commit on github"): [Console] カスタムスタイルを定義するためのアウトプットフォーマッタのスタイルクラスを実装
  * [4fe2efd](http://github.com/symfony/symfony/commit/4fe2efd49e83075f6b59ba6c60afcd5d9331d5d4 "4fe2efd49e83075f6b59ba6c60afcd5d9331d5d4 commit on github"): [Console] アウトプットメッセージの形式化とデコレートのためにアウトプットフォーマッタの実装
  * [644cf61](http://github.com/symfony/symfony/commit/644cf612b36dc335ffa13ee1c546f38c004fb4b7 "644cf612b36dc335ffa13ee1c546f38c004fb4b7 commit on github"), [8b885a9](http://github.com/symfony/symfony/commit/8b885a991c1795db3c135666565b39ca2b9b0a0c "8b885a991c1795db3c135666565b39ca2b9b0a0c commit on github"): [Console] 新しいアウトプットフォーマッタとスタイルをサポートするためにコンソール出力を更新
  * [6960925](http://github.com/symfony/symfony/commit/69609257acbc13ffcaa3c359e17114ea46a19530 "69609257acbc13ffcaa3c359e17114ea46a19530 commit on github"): [DomCrawler] テンプディレクトリにソースファイルをコピーすることによって、より実アップロードをエミュレートするためのアップロードロジックを更新
  * [9fd7d05](http://github.com/symfony/symfony/commit/9fd7d05ecf439e2059455a7d70372c35ceaae3af "9fd7d05ecf439e2059455a7d70372c35ceaae3af commit on github"): [Config] NodeBuilderをサブクラス化することなく、ノードタイプを追加および上書きする機能
  * [69d324e](http://github.com/symfony/symfony/commit/69d324eca8370cd496792cd277989427d406affa "69d324eca8370cd496792cd277989427d406affa commit on github"): [EventDispatcher] EventDispatcher::removeSubscriber()の追加
  * [136b23e](http://github.com/symfony/symfony/commit/136b23ead4ae994293600d6d124922b96610f2c8 "136b23ead4ae994293600d6d124922b96610f2c8 commit on github"), [bd8d2b8](http://github.com/symfony/symfony/commit/bd8d2b829f821a5a083d0870a3072c9761593007 "bd8d2b829f821a5a083d0870a3072c9761593007 commit on github"): [EventDispatcher] コードのリファクタリング
  * [7f52346](http://github.com/symfony/symfony/commit/7f523466f4a3b8f120e1766bca786ed021f13cf8 "7f523466f4a3b8f120e1766bca786ed021f13cf8 commit on github"), [d959a3e](http://github.com/symfony/symfony/commit/d959a3ed4bbe9b2a3dff0f0c5285086a2318ac96 "d959a3ed4bbe9b2a3dff0f0c5285086a2318ac96 commit on github"): [TwigBundle] cache warmerの修正
  * [20a717e](http://github.com/symfony/symfony/commit/20a717ea3c97a3e52d70255c66c03ede91c91f8e "20a717ea3c97a3e52d70255c66c03ede91c91f8e commit on github"): [WebProfileBundle] WDTのコントローラの呼び出し名を追加
  * [0c8ff92](http://github.com/symfony/symfony/commit/0c8ff92ecd4318561bcba2c055e6cc17c51b0148 "0c8ff92ecd4318561bcba2c055e6cc17c51b0148 commit on github"), [f36b10a](http://github.com/symfony/symfony/commit/f36b10afe7dba0a6bb9068c8718d851f9d5fc38a "f36b10afe7dba0a6bb9068c8718d851f9d5fc38a commit on github"): WDTクリックのコントローラ名を作成
  * [e596931](http://github.com/symfony/symfony/commit/e596931dc89925f9d73ded72db5e63a0d7940e18 "e596931dc89925f9d73ded72db5e63a0d7940e18 commit on github"): [DomCrawler] 機能テストにおいてJavaScriptがエミュレートできるようにするため、フォームフィールドの削除を有効化
  * [a56dbec](http://github.com/symfony/symfony/commit/a56dbec6d8a4a8600a3b7cac0c65a4c054632f8a "a56dbec6d8a4a8600a3b7cac0c65a4c054632f8a commit on github"), [7e1c4d5](http://github.com/symfony/symfony/commit/7e1c4d57481077cd1fc736dc30e0c8a26bba40e0 "7e1c4d57481077cd1fc736dc30e0c8a26bba40e0 commit on github"): [Security] 多くのインターフェイスからの必要のないイベントパラメータを削除
  * [3fd50ea](http://github.com/symfony/symfony/commit/3fd50ea4e622d9741547337b0223ad055d785750 "3fd50ea4e622d9741547337b0223ad055d785750 commit on github"), [e4eee05](http://github.com/symfony/symfony/commit/e4eee05b065b3bbe2d23bfbc75d4f476b2bdf25b "e4eee05b065b3bbe2d23bfbc75d4f476b2bdf25b commit on github"): [Routing] ルーティング設定がサポートされていないキーを持っている場合、例外をスローする
  * [a505ff4](http://github.com/symfony/symfony/commit/a505ff43b59a63262cc71ec4f7f0bc84b0a209b0 "a505ff43b59a63262cc71ec4f7f0bc84b0a209b0 commit on github"): [Routing] シングルコントローラ用の複数のルートアノテーションのサポート追加


