A week of symfony #225 (18->24 April 2011)
==========================================

今週、Symfony2は新しいフォーム/検証コンポーネントの開発に集中した。最初に [フォームブランチ](https://github.com/symfony/symfony/commit/0069a70e42c74205a888aa7b5f1743700b24a51f)（300ファイル以上 25,000 行近くのコードの修正）をマージした。 その後、フォームを[拡張](https://github.com/symfony/symfony/pull/623)し、[使い易く](https://github.com/symfony/symfony/commit/e790587dc22cd52cd0648ad249a54a2ec8f9477d)するための修正や調整がコミットされた。また、[Symfony2 PR12がリリース](http://symfony.com/blog/symfony2-pr12-released)され、最初のベータ版が来週に発表される。

 
開発メーリングリスト
------------------------

  * [[Symfony2] Security ACL: クラススコープのパーミッション - 考察](https://groups.google.com/forum/#!topic/symfony-devs/UR8PmwCAr40)
  * [[Symfony2] SecurityLightBundle](https://groups.google.com/forum/#!topic/symfony-devs/rpGPenSRSCI)
  * [[Symfony2] セキュリティシステムを使用しない](https://groups.google.com/forum/#!topic/symfony-devs/-Mrzh7uvpYc)
  * [RFC: LoggerInterfaceの調整](https://groups.google.com/forum/#!topic/symfony-devs/PAgd80jKn3s)
  * [[Sf2] Cache warmersとpriorities](https://groups.google.com/forum/#!topic/symfony-devs/PI_jrWHzJfk)
  * [[Symfony2] セキュリティコンポーネントを組み込む上での一般的な難点](https://groups.google.com/forum/#!topic/symfony-devs/TIX9Ynl-ZMA)
  * [[Symfony2] フレームワークからのフィードバックの考察](https://groups.google.com/forum/#!topic/symfony-devs/8eEsQZ9kyeY)


Symfony2開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [50011fa](http://github.com/symfony/symfony/commit/50011fa344cc399b681b28f0bfc863e8635d34dc "50011fa344cc399b681b28f0bfc863e8635d34dc commit on github"), [5772255](http://github.com/symfony/symfony/commit/57722550de71775b604d25b7e7e5cd48f20ce643 "57722550de71775b604d25b7e7e5cd48f20ce643 commit on github"): フォームの入力にhtml5メールを追加
  * [eb21dc9](http://github.com/symfony/symfony/commit/eb21dc9fea908004dc431734f8ed54d22e36469c "eb21dc9fea908004dc431734f8ed54d22e36469c commit on github"): [Form] validation.xmlから廃止された制約を削除
  * [bee5d07](http://github.com/symfony/symfony/commit/bee5d07d86438d17bb3bab7c5815b57bfbae3aad "bee5d07d86438d17bb3bab7c5815b57bfbae3aad commit on github"): [Form] フォームを構築する際、フォーム制約を指定する方法を追加(オブジェクトの代わりに配列を扱う場合有用)
  * [273d72e](http://github.com/symfony/symfony/commit/273d72ef757d6acd789769bc3df89ccacbf17d8c "273d72ef757d6acd789769bc3df89ccacbf17d8c commit on github"): [Form] PHPのテンプレートの区切りと一致するようにtwigのブロックを二重のアンダースコアから単一のアンダースコアへ変更
  * [b93f5a3](http://github.com/symfony/symfony/commit/b93f5a372ad75508a59e378f60eb331511356660 "b93f5a372ad75508a59e378f60eb331511356660 commit on github"): [Form] ChoiceUtilからFormUtilに名前を変更し、メソッドより一般的な名前にした。

  * [3ca5f51](http://github.com/symfony/symfony/commit/3ca5f513a40bad805ed3e8c05c135489460e8a49 "3ca5f513a40bad805ed3e8c05c135489460e8a49 commit on github"): [Form] form validationでグループのサポートを追加(配列データを利用する際)
  * [c660fcd](http://github.com/symfony/symfony/commit/c660fcd2f2310649eabe94a14d28ce14a1a8b760 "c660fcd2f2310649eabe94a14d28ce14a1a8b760 commit on github"): [Security] SwitchUserListenerのクリティカルなセキュリティバグを修正
  * [defb021](http://github.com/symfony/symfony/commit/defb0218fb1c1ff59b35ac7bbb1d92a84a67fe1a "defb0218fb1c1ff59b35ac7bbb1d92a84a67fe1a commit on github"): [DoctrineMongoDBBundle] assertMongoDBにannotation制約の名前空間エイリアスを設定
  * [5a9a657](http://github.com/symfony/symfony/commit/5a9a65701bed2dbb5924415571b8125c14ddfac8 "5a9a65701bed2dbb5924415571b8125c14ddfac8 commit on github"): [AsseticBundle] use_controllerがオンになっているときにfactory workerがパスを修正するよう追加
  * [91602df](http://github.com/symfony/symfony/commit/91602dfef4051c400b12cf8f13f403c9e10d61f6 "91602dfef4051c400b12cf8f13f403c9e10d61f6 commit on github"): [FrameworkBundle] 機能テストでリクエストの後にKernel/Containerとのやり取りを可能にする
  * [6f16820](http://github.com/symfony/symfony/commit/6f16820328f843b10a35ee04d239e4a7fc2c570f "6f16820328f843b10a35ee04d239e4a7fc2c570f commit on github"): [FrameworkBundle] ContainerDebugCommandから不要でバグな機能を削除
  * [07aae98](http://github.com/symfony/symfony/commit/07aae9849536cb5fdd0d901aa7eb113b5a8c054e "07aae9849536cb5fdd0d901aa7eb113b5a8c054e commit on github"): [Routing] _scheme要件のサポートを追加。_scheme要件は、必ず1つの指定されたschemeに一致しschemeに指定された方式で生成されるルートを強制的に使用することが可能。
  * [cdf706d](http://github.com/symfony/symfony/commit/cdf706d357b8f74acae5e7a29b4982010a854bf9 "cdf706d357b8f74acae5e7a29b4982010a854bf9 commit on github"): [DependencyInjection] より具体的にDefinition::setArgument()をreplaceArgument()にリネーム
  * [470baaa](http://github.com/symfony/symfony/commit/470baaab9f9082c1339a23bf014408040331ea67 "470baaab9f9082c1339a23bf014408040331ea67 commit on github"): [DependencyInjection] 他の定義に関連するメソッドとより一貫性のあるようにContainerBuilder::remove()をremoveDefinition()にリネーム
  * [117321d](http://github.com/symfony/symfony/commit/117321d3c651a0563ed92871be5a732a1a0c4b79 "117321d3c651a0563ed92871be5a732a1a0c4b79 commit on github"): ルーティングで配列をRequestContextに置換
  * [fd1636b](http://github.com/symfony/symfony/commit/fd1636b324b245bd632b67c263a5810672663349 "fd1636b324b245bd632b67c263a5810672663349 commit on github"): [Routing] RedirectableUrlMatcherの追加
  * [1191e3a](http://github.com/symfony/symfony/commit/1191e3aa666662027a1df66381061ff70149c766 "1191e3aa666662027a1df66381061ff70149c766 commit on github"), [f7b1839](http://github.com/symfony/symfony/commit/f7b1839296820c1a7868b3736d8ec318b13118f6 "f7b1839296820c1a7868b3736d8ec318b13118f6 commit on github"): [AsseticBundle] cache warmersの修正
  * [30511d2](http://github.com/symfony/symfony/commit/30511d29658b994c15622a969fe50d9982588c4d "30511d29658b994c15622a969fe50d9982588c4d commit on github"): [HttpFoundation] FilesystemSessionStorageの修正
  * [4d6e239](http://github.com/symfony/symfony/commit/4d6e239f106146a8db6e47795fe8f81e933995ad "4d6e239f106146a8db6e47795fe8f81e933995ad commit on github"): [Security/Acl] インターフェイスからDoctrineの依存関係を削除し実際の実装に移動
  * [f7d4414](http://github.com/symfony/symfony/commit/f7d44148df19d1564f5ce326e080cca33d805e63 "f7d44148df19d1564f5ce326e080cca33d805e63 commit on github"): [Routing] 使用していないデフォルト値を削除
  * [c6dcf0f](http://github.com/symfony/symfony/commit/c6dcf0f8f327adaa5a38033f6b091cf94f47c186 "c6dcf0f8f327adaa5a38033f6b091cf94f47c186 commit on github"): [Routing] URLを生成する際、適用されるデフォルトパラメータを設定する方法を追加
  * [7266b41](http://github.com/symfony/symfony/commit/7266b41aded2db6a88f980431752f25688cb204b "7266b41aded2db6a88f980431752f25688cb204b commit on github"): [FrameworkBundle] ルートを生成する際、現在のロケールを_localeのデフォルト値とするように追加
  * [54b77d2](http://github.com/symfony/symfony/commit/54b77d24dd7e0119d2a2654407db6fa991a5ab9c "54b77d24dd7e0119d2a2654407db6fa991a5ab9c commit on github"): transchoiceフィルタを使用している場合でも%count%変数を自動的に利用可能にする（タグの働きは類似）
  * [cad6643](http://github.com/symfony/symfony/commit/cad6643e776193e5a888b6fbd965aa8058e58bff "cad6643e776193e5a888b6fbd965aa8058e58bff commit on github"): [Bridge/Twig] Twigの自動的に行情報を追加される例外を簡略化
  * [286c457](http://github.com/symfony/symfony/commit/286c45733e47d20d0b40e8454492a5fb66d80875 "286c45733e47d20d0b40e8454492a5fb66d80875 commit on github"): [Bridge/Twig] trans tagにメッセージを渡す処理を削除（長いタグ又はフィルタの代わりに利用していた）
  * [8ad9309](http://github.com/symfony/symfony/commit/8ad93095d489a14969304d9bd30cf2d5337a2198 "8ad93095d489a14969304d9bd30cf2d5337a2198 commit on github"): [AsseticBundle] twigがデバッグモードでキャッシュを変更することができないので、コンパイル時ではなく実行時にデバッグモードを確認するようtwigを更新
  * [6a227f8](http://github.com/symfony/symfony/commit/6a227f858a2a3687459dcda899409150eec24512 "6a227f858a2a3687459dcda899409150eec24512 commit on github"): [AsseticBundle] ルートを作成する前に、URLからフェイクのフロントコントローラを削除
  * [57dd6ae](http://github.com/symfony/symfony/commit/57dd6aef865f82c0b627d2826aeb97b913256381 "57dd6aef865f82c0b627d2826aeb97b913256381 commit on github"): [AsseticBundle] ルータとコントローラの修正
  * [314684d](http://github.com/symfony/symfony/commit/314684df24c81ed2c098d0e48ac214c121311d1b "314684df24c81ed2c098d0e48ac214c121311d1b commit on github"): [FrameworkBundle] ESIの相対URLを仕様で認める(絶対パスを生成する必要が無くなる)
  * [4dc5b8e](http://github.com/symfony/symfony/commit/4dc5b8ec78b7407210a6c9008a59d16975192519 "4dc5b8ec78b7407210a6c9008a59d16975192519 commit on github"), [d86aa74](http://github.com/symfony/symfony/commit/d86aa74e3d68b8e5cf808bedcbf241fe0413649a "d86aa74e3d68b8e5cf808bedcbf241fe0413649a commit on github"): [FrameworkBundle] ユニットテストファイルでカーネルをブートする必要性を削除
  * [e6d86eb](http://github.com/symfony/symfony/commit/e6d86eb9f7b116ab9e926feb3d080402cafef00f "e6d86eb9f7b116ab9e926feb3d080402cafef00f commit on github"): 独自のリポジトリにDoctrineMongoDBBundleに移動。symfonyの他のバンドルはDoctrine Common2.0に依存しているがバンドルがDoctrine Common2.1に依存するため行った。
  * [df50e2b](http://github.com/symfony/symfony/commit/df50e2b161e84f9e2489b33cd5e44214ec742f21 "df50e2b161e84f9e2489b33cd5e44214ec742f21 commit on github"): [Form] TimezoneTypeで過剰なオプションを削除
  * [1856601](http://github.com/symfony/symfony/commit/18566015242b0ee9d4db85f577d0f35ce5b60e1f "18566015242b0ee9d4db85f577d0f35ce5b60e1f commit on github"): [Validator] 選択メッセージを修正し、複数の異なるメッセージを追加
  * [0069a70](http://github.com/symfony/symfony/commit/0069a70e42c74205a888aa7b5f1743700b24a51f "0069a70e42c74205a888aa7b5f1743700b24a51f commit on github"): 'フォーム'ブランチをマージ (300コミットと25,000以上コードの修正が含まれる)
  * [a97366f](http://github.com/symfony/symfony/commit/a97366fbcb75d96bc53916732580c4b88784cad2 "a97366fbcb75d96bc53916732580c4b88784cad2 commit on github"): [Form] FormFactory::create()のシグネチャをcreate()とcreateNamed()に分割
  * [0632327](http://github.com/symfony/symfony/commit/0632327b7781b54c02ab867431c786ed90389dfb "0632327b7781b54c02ab867431c786ed90389dfb commit on github"): コアからdata fixturesの削除(https://github.com/symfony/DoctrineFixturesBundleへ移動)
  * [5c2c16f](http://github.com/symfony/symfony/commit/5c2c16f57e56c3d001d2b219889582f33ac2d391 "5c2c16f57e56c3d001d2b219889582f33ac2d391 commit on github"): DoctrineMigrationsBundleを独自レポジトリへ移動(https://github.com/symfony/DoctrineMigrationsBundle)
  * [7644e86](http://github.com/symfony/symfony/commit/7644e86683464805305b338404ee2f4d90cda286 "7644e86683464805305b338404ee2f4d90cda286 commit on github"): セッションコンフィグレーションのリファクタリング(すべてのセッションストレージに有効な"グローバル"のオプションのみのオプション配列になる(復帰)
  * [fd05f02](http://github.com/symfony/symfony/commit/fd05f02b234aa47625246336d31d0d48bb0026e8 "fd05f02b234aa47625246336d31d0d48bb0026e8 commit on github"): [HttpFoundation] Content-Type内に関連したContent-Typesが存在しない時に自動的にcharsetを追加するロジックを追加
  * [54e66c5](http://github.com/symfony/symfony/commit/54e66c518ff9c2705b3a04200bd12cfc8d207a62 "54e66c518ff9c2705b3a04200bd12cfc8d207a62 commit on github"): [Form] FormFactoryクラスの唯一のコンストラクタ引数となるフォームエクステンションにコードを再編成。これらはは既存のローダークラスを置き換わる。
  * [1ce2db8](http://github.com/symfony/symfony/commit/1ce2db87e2e50f0269870c6bdf1c2d13729a9ab3 "1ce2db87e2e50f0269870c6bdf1c2d13729a9ab3 commit on github"): [Form] FormTypeExtensionInterfaceを追加。インターフェイスの実装では既存のタイプを修正する事が可能。
  * [6f1bc35](http://github.com/symfony/symfony/commit/6f1bc356a84208a5897e18719fd1287e68add868 "6f1bc356a84208a5897e18719fd1287e68add868 commit on github"): [Form] CoreExtensionから新しいValidatorExtensionにコードをリファクタリング
  * [2b8c7f8](http://github.com/symfony/symfony/commit/2b8c7f84b502007e2d4c8b1e62254492f88badcd "2b8c7f84b502007e2d4c8b1e62254492f88badcd commit on github"): [Form] FormFactoryの作成後にフォームエクステンションを登録する方法を追加。
  * [55e6883](http://github.com/symfony/symfony/commit/55e6883a88267f89ce8cfd253d3602bfa66f5724 "55e6883a88267f89ce8cfd253d3602bfa66f5724 commit on github"), [b347aeb](http://github.com/symfony/symfony/commit/b347aebee89af83b375e3b627b85af40c112edef "b347aebee89af83b375e3b627b85af40c112edef commit on github"): [TwigBundle] 古いコードを削除
  * [d9491a7](http://github.com/symfony/symfony/commit/d9491a743e46ed3e4cb04e6b680c3506a6791bcd "d9491a743e46ed3e4cb04e6b680c3506a6791bcd commit on github"): 関連するすべてのテストだけでなく、インターフェイスインジェクションのサポートを削
  * [9bffd8c](http://github.com/symfony/symfony/commit/9bffd8c2dbd8717a6ec1f7f18f74eea075978fb5 "9bffd8c2dbd8717a6ec1f7f18f74eea075978fb5 commit on github"): [FrameworkBundle] Configurationクラスにいくつかのデフォルト値を移動
  * [02c66e6](http://github.com/symfony/symfony/commit/02c66e658cb8aef8cb1a2361a288112b58ee34f7 "02c66e658cb8aef8cb1a2361a288112b58ee34f7 commit on github"): ファイルのテンポラリストレージのnestingLevelコンフィグレーションを削除
  * [8cc5caf](http://github.com/symfony/symfony/commit/8cc5caf1f3ca463af4bf23bad303ebfff0a5b112 "8cc5caf1f3ca463af4bf23bad303ebfff0a5b112 commit on github"): アップロードテンプディレクトリのデフォルトのディレクトリを変更し、ディレクトリを必須化
  * [f05801c](http://github.com/symfony/symfony/commit/f05801cace025986c90dc7a3b8289b9152ac9c1a "f05801cace025986c90dc7a3b8289b9152ac9c1a commit on github"): [FrameworkBundle] router.options.resource_typeとrouting.resourceの引数を削除
  * [8b74c6e](http://github.com/symfony/symfony/commit/8b74c6eb9c107d2a33e1ffacba583ca68d9ee020 "8b74c6eb9c107d2a33e1ffacba583ca68d9ee020 commit on github"): [DomCrawler] リンクやフォームのURLマネジメントをリファクタリング
  * [78b2062](http://github.com/symfony/symfony/commit/78b2062c5e81ece3afcadeeb4ee6c5ee6a9bad3d "78b2062c5e81ece3afcadeeb4ee6c5ee6a9bad3d commit on github"): [Form] DateTypeに無効なウィジェットのオプションの例外を追加
  * [8eb1dfc](http://github.com/symfony/symfony/commit/8eb1dfc6a06ec82f98661aba5016c18e90264f34 "8eb1dfc6a06ec82f98661aba5016c18e90264f34 commit on github"): [Translation] translated idにstringを強制
  * [675e5de](http://github.com/symfony/symfony/commit/675e5ded9ebd8684bd1ff6fba1df835892da7f88 "675e5ded9ebd8684bd1ff6fba1df835892da7f88 commit on github"): [Form] FormBuilder::build()をFormBuilder::create()に変更。手動でFormBuilder::add()に結果のビルダーを渡す必要がある
  * [4ed8d4f](http://github.com/symfony/symfony/commit/4ed8d4f6b5699ffe564205ce4c9cb1785bf8e12c "4ed8d4f6b5699ffe564205ce4c9cb1785bf8e12c commit on github"): [Routing] 非オプションの変数が空のときのURLの生成を修正
  * [e790587](http://github.com/symfony/symfony/commit/e790587dc22cd52cd0648ad249a54a2ec8f9477d "e790587dc22cd52cd0648ad249a54a2ec8f9477d commit on github"): [Form] オブジェクトがフォームの作成時に渡された場合、自動的にdata_classオプションを設定する
  * [dbb5ca4](http://github.com/symfony/symfony/commit/dbb5ca459dc0a191c488aab234c7bd74a3723cd5 "dbb5ca459dc0a191c488aab234c7bd74a3723cd5 commit on github"), [29802fa](http://github.com/symfony/symfony/commit/29802faef42526b467ee3d618fb706bc2d4646dd "29802faef42526b467ee3d618fb706bc2d4646dd commit on github"): [Classloader] fixed APCクラスローだの修正とユニットテストの追加
  * [e8bb64c](http://github.com/symfony/symfony/commit/e8bb64c17c9ef0a9c6a3d65a5aeb05be2ddf5642 "e8bb64c17c9ef0a9c6a3d65a5aeb05be2ddf5642 commit on github"): [Classloader] phpdocの使用例の追加とユニットテストフィクスチャのリファクタリング


