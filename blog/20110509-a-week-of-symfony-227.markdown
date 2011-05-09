A week of symfony #227 (2->8 May 2011)
======================================

今週もSymfony2の開発者たちはDoctrine2の統合が簡単になるように注力しました：DoctrineBundleには、[新しいRegistryクラス](https://github.com/symfony/symfony/commit/6b5438aa38d90c70a36ce80da73e518c1a197857)や[よりスマートにエンティティを生成するコマンド](https://github.com/symfony/symfony/commit/ca4c1355c750a5db87b01ee03215e89cf2d61d3c)、そして[より簡単なYAMLの設定方法](https://github.com/symfony/symfony/commit/b7c84420680723c0b4353e43d339b32b9ce25f0f)が加わりました。それと同時に、Serializerコンポーネントはリファクタリングされ、[幾つかの例外が改善されました](http://symfony.com/blog/symfony2-getting-easier-part-2)。
 
 開発ML
------------------------

  * [\[Sf2\] Form: 永続的にファイルをアップロードする?](https://groups.google.com/forum/#!topic/symfony-devs/Sknb5JBpYFA)
  * [RFC: イベント定数の削除](https://groups.google.com/forum/#!topic/symfony-devs/y5sZ3PbNSQ8)
  * [\[2.0 BETA1\] Formで設定エラー](https://groups.google.com/forum/#!topic/symfony-devs/YKzMZweyvuU)
  * [\[Sf2\] Formコンポーネントの微調整](https://groups.google.com/forum/#!topic/symfony-devs/81RcMAWdQ0Y)
  * [\[Symfony2\] 今後5.3.1がサポートされない理由の詳細がほしい](https://groups.google.com/forum/#!topic/symfony-devs/cQ5r_hAQS6o)
  * [Symfony Book](https://groups.google.com/forum/#!topic/symfony-devs/PRjSEmNyaxw)

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [11cdff9](http://github.com/symfony/symfony/commit/11cdff93f3b6756d467da019c4158c950494ee3e "11cdff93f3b6756d467da019c4158c950494ee3e commit on github"): \[FrameworkBundle\] container:debugコマンドのリファクタリング (コンテナをキャッシュにせリアライズするときにダンパーを使い、抽象サービスを表示しない)
  * [1cd83c9](http://github.com/symfony/symfony/commit/1cd83c93e0bd8a695a020284f55cbe7113b08696 "1cd83c93e0bd8a695a020284f55cbe7113b08696 commit on github"): \[AsseticBundle\] アセットをダンプしたときの _controller/ プレフィックスの修正
  * [d05c592](http://github.com/symfony/symfony/commit/d05c59227d4c6f6e27d3556f0034d456b5a4a713 "d05c59227d4c6f6e27d3556f0034d456b5a4a713 commit on github"): \[HttpKernel\] Windowsでエラーがコンソールに漏れてしまうのを防止
  * [25d7009](http://github.com/symfony/symfony/commit/25d7009c1c65558abe8006fc01901269c5f294d3 "25d7009c1c65558abe8006fc01901269c5f294d3 commit on github"): \[FrameworkBundle\] ERR以上のすべてのログメッセージをエラーとして扱う
  * [a56ea15](http://github.com/symfony/symfony/commit/a56ea15363076ce9097725be52c009404e2e21c6 "a56ea15363076ce9097725be52c009404e2e21c6 commit on github"): \[MonologBundle\] 新しいMonologログレベルのサポート追加
  * [d0e31b8](http://github.com/symfony/symfony/commit/d0e31b8ca6c777f5a0db2fd5ebdef87e9246dfc7 "d0e31b8ca6c777f5a0db2fd5ebdef87e9246dfc7 commit on github"): CLIの早い段階でなにか悪いことが起きたときに、いいエラーメッセージが出るようにアプリケーションを変更
  * [838853e](http://github.com/symfony/symfony/commit/838853e58bfe97cf67c9454d2ee2308ba25957a3 "838853e58bfe97cf67c9454d2ee2308ba25957a3 commit on github"): \[HttpKernel\] ログの500+エラーをクリティカルとするが、エラーではない (これによって404レスポンスとアプリケーションの本当のエラーとの間に、簡単にフィルターできる)
  * [6b5438a](http://github.com/symfony/symfony/commit/6b5438aa38d90c70a36ce80da73e518c1a197857 "6b5438aa38d90c70a36ce80da73e518c1a197857 commit on github"), [014b190](http://github.com/symfony/symfony/commit/014b19040c90184633fb308b47d4b2500a4d3008 "014b19040c90184633fb308b47d4b2500a4d3008 commit on github"): \[DoctrineBundle\] Registryクラスの導入. Registryはサービスコンテナ内で宣言されたすべての接続とエンティティマネージャを知っている。Registryは'doctrine'サービス経由で利用可能で、接続やエンティティマネージャを名前で取得して使うことができる。
  * [d2a9b23](http://github.com/symfony/symfony/commit/d2a9b23c287b0690ac2240b490a081dd27022a4a "d2a9b23c287b0690ac2240b490a081dd27022a4a commit on github"): \[Routing\] オプション変数の１セグメントだけを持つパターンの時のルーティングの修正
  * [0139a80](http://github.com/symfony/symfony/commit/0139a800f9a7022cb5fbbc8685e18f291325808a "0139a800f9a7022cb5fbbc8685e18f291325808a commit on github"): \[HttpKernel\] テスト中にコンソールに出力されるのを防止
  * [ca4c135](http://github.com/symfony/symfony/commit/ca4c1355c750a5db87b01ee03215e89cf2d61d3c "ca4c1355c750a5db87b01ee03215e89cf2d61d3c commit on github"), [ec226cd](http://github.com/symfony/symfony/commit/ec226cd4bc4aae18f3740f064933cbfa3f823932 "ec226cd4bc4aae18f3740f064933cbfa3f823932 commit on github"), [0cdd6ca](http://github.com/symfony/symfony/commit/0cdd6ca4e2b0886adcba73a79a111b6b41e4e4f7 "0cdd6ca4e2b0886adcba73a79a111b6b41e4e4f7 commit on github"): \[DoctrineBundle\] doctrine:generate:entities をよりスマートに (バンドル名やクラス名、あるいは名前空間に基づいてクラスを生成することが可能となった。可能であればレポジトリクラスも生成する)
  * [27d02a7](http://github.com/symfony/symfony/commit/27d02a7d4ad986878c1415736f9cce6bb2b4d871 "27d02a7d4ad986878c1415736f9cce6bb2b4d871 commit on github"): \[Routing\] 回帰バグの修正 (fooがデフォルト値ではないときに / は /{foo} でマッチしてはいけない)
  * [0147df6](http://github.com/symfony/symfony/commit/0147df6b22ac45674ae70b963846e532b0ecb491 "0147df6b22ac45674ae70b963846e532b0ecb491 commit on github"): ポルトガル語翻訳の追加
  * [2c28767](http://github.com/symfony/symfony/commit/2c287676fbf0120303368602e4bc005a9473cab7 "2c287676fbf0120303368602e4bc005a9473cab7 commit on github"): \[DependencyInjection\] プロパティ挿入を使用している定義のリクエスト時のバグを修正
  * [17aa0ed](http://github.com/symfony/symfony/commit/17aa0ed0edb613cf7bfaba89f202e340270bf18d "17aa0ed0edb613cf7bfaba89f202e340270bf18d commit on github"): 革新的でより良いセキュリティのために、クッキーに対するhttpOnlyの初期値を変更
  * [f7808de](http://github.com/symfony/symfony/commit/f7808de3a8aec96ce20758951886ab90185bbe1a "f7808de3a8aec96ce20758951886ab90185bbe1a commit on github"): \[DoctrineBundle\] DIC定義をさらに orm.xml の中に移動
  * [1cfed9e](http://github.com/symfony/symfony/commit/1cfed9e24ef3d281bbb9b200f3d08fbc991f8ed6 "1cfed9e24ef3d281bbb9b200f3d08fbc991f8ed6 commit on github"): エストニア語翻訳のサポート
  * [eb50d76](http://github.com/symfony/symfony/commit/eb50d766da359e3ee228f223ad1da8eb809c4de5 "eb50d766da359e3ee228f223ad1da8eb809c4de5 commit on github"): \[Form\] ネストしたフォームヘルパーに入ったときの変数のスコープを修正。このコミットによって、囲っているフォームヘルパーがすでに通過している変数が、アクセス可能となる。
  * [86d0ddb](http://github.com/symfony/symfony/commit/86d0ddb4e3e957671df26e0ad98249ee566f150c "86d0ddb4e3e957671df26e0ad98249ee566f150c commit on github"): \[DoctrineBundle\] Registry::getEntityManager()を２つのメソッドに分割 (閉じられたときに暗黙的にエンティティマネージャがリセットされる代わりに、開発者がリセット出来ると思ったタイミングで手動でリセットするべきである)
  * [bf1dfbb](http://github.com/symfony/symfony/commit/bf1dfbbe99d610a923db9b0444bec7005d69b0e9 "bf1dfbbe99d610a923db9b0444bec7005d69b0e9 commit on github"): \[Form\] フォームコンポーネントは、モデルにUploadFileオブジェクトを常に渡すことが保証された
  * [3cc5d9f](http://github.com/symfony/symfony/commit/3cc5d9f4cdd1956374c034798ab65f664a74a47c "3cc5d9f4cdd1956374c034798ab65f664a74a47c commit on github"): \[Form\] コレクションタイプの変更可能なオプションをallow_addとallow_deleteに分割
  * [74cca63](http://github.com/symfony/symfony/commit/74cca63938a548eb0be8c7934382364de2a07167 "74cca63938a548eb0be8c7934382364de2a07167 commit on github"): \[Form\] ビューがルートではないならば、今後 CSRFフィールドはFormViewの子孫には含まれない
  * [ae46150](http://github.com/symfony/symfony/commit/ae46150bc835ac71ee609fb061b0274c91642360 "ae46150bc835ac71ee609fb061b0274c91642360 commit on github"): \[HttpFoundation\] X-Forwarded-Port リクエストハンドラのサポート追加
  * [b7c8442](http://github.com/symfony/symfony/commit/b7c84420680723c0b4353e43d339b32b9ce25f0f "b7c84420680723c0b4353e43d339b32b9ce25f0f commit on github"), [d9299e9](http://github.com/symfony/symfony/commit/d9299e930b0a3b000abf98eaefca1118149587c6 "d9299e930b0a3b000abf98eaefca1118149587c6 commit on github"), [dfd5b65](http://github.com/symfony/symfony/commit/dfd5b653cb22e04e61a0a667dc8af8ddb8bd0595 "dfd5b653cb22e04e61a0a667dc8af8ddb8bd0595 commit on github"): \[DoctrineBundle\] Doctrineメタデータ設定がより簡単に (Doctrineのメタデータを'doctrine'という名前の単一のファイルで設定できる)
  * [aba8f1e](http://github.com/symfony/symfony/commit/aba8f1e1802fbafcd954c2b6f59272492bd4e6f7 "aba8f1e1802fbafcd954c2b6f59272492bd4e6f7 commit on github"): \[ClassLoader\] デバッグクラスローダを追加
  * [0f0e581](http://github.com/symfony/symfony/commit/0f0e5817b18cfaabbce63ebbb49696990981e553 "0f0e5817b18cfaabbce63ebbb49696990981e553 commit on github"): \[HttpKernel\] Kernel::init() メソッドを追加
  * [ca3c5e6](http://github.com/symfony/symfony/commit/ca3c5e652ed5278a1ab8366ed181b04c0cb662f6 "ca3c5e652ed5278a1ab8366ed181b04c0cb662f6 commit on github"): ErrorHandler 管理を distributions に移動
  * [3f69333](http://github.com/symfony/symfony/commit/3f69333acb61dd0836af2032dec7e38e17a14b35 "3f69333acb61dd0836af2032dec7e38e17a14b35 commit on github"): \[HttpKernel\] ErrorHandlerクラスのリファクタリング
  * [486ecdc](http://github.com/symfony/symfony/commit/486ecdc6a63c8ed8843a859019bea234adb44c6f "486ecdc6a63c8ed8843a859019bea234adb44c6f commit on github"): \[Config\] 幾つかの例外を改善
  * [daeedb5](http://github.com/symfony/symfony/commit/daeedb570525db79e6becdfffcc4dfe4db2441b6 "daeedb570525db79e6becdfffcc4dfe4db2441b6 commit on github"), [62c0b10](http://github.com/symfony/symfony/commit/62c0b10b88757071bde1e7dd4001a7b3fed5e32c "62c0b10b88757071bde1e7dd4001a7b3fed5e32c commit on github"): 検索エンジンはProfilerとExceptionのページをインデックスするべきではない
  * [ec1199e](http://github.com/symfony/symfony/commit/ec1199eda7f756a4782d8bfc7bf94f039875365f "ec1199eda7f756a4782d8bfc7bf94f039875365f commit on github"): \[Serializer\] SerializerInterfaceの更新
  * [919f16a](http://github.com/symfony/symfony/commit/919f16a7d613a5054a25d28769e9fa628b31adbe "919f16a7d613a5054a25d28769e9fa628b31adbe commit on github"): \[Serializer\] Traversableオブジェクトのサポート追加
  * [ded30a2](http://github.com/symfony/symfony/commit/ded30a2937a053eae91ceac09cae3d4570a988b9 "ded30a2937a053eae91ceac09cae3d4570a988b9 commit on github"): \[Serializer\] supports を supportsNormalization と supportsDenormalization に分割
