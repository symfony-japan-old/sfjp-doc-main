A week of symfony #214 (31 January -> 6 February 2011)
======================================================

サンフランシスコでの初めてのSymfony Live 2001の直前ということで、今週のSymfony2の開発は活発化しました。[新しいSecurityBundle](https://github.com/symfony/symfony/commit/e645090423a037912ac5e0c43bc3ea104998fa2a)が登場し、クラスローディングが独自のコンポーネントに移行し、フォームとバリデータのコンポーネントは大幅に改良されました。さらに、[symfonyコミュニティはまだ同意していません](https://groups.google.com/forum/#!topic/symfony-devs/3nwwiUaT4ds)が、[コンフィグノーマライザ](http://github.com/symfony/symfony/commit/b484763a7a331d68504b5b047c733ab076d266b9)の最初のバージョンがコミットされました。

開発メーリングリスト
------------------------

  * [[Symfony2] Yamlだけのアプリケーション設定?](https://groups.google.com/forum/#!topic/symfony-devs/rjrWWYyrkRI)
  * [モデルに対するディレクトリ構造が正常に動作しない](https://groups.google.com/forum/#!topic/symfony-devs/a9nm721Ga4w)
  * [[RFC] 自動でのクラスのコンパイル](https://groups.google.com/forum/#!topic/symfony-devs/Of6FXk-wICM)
  * [[Symfony2] サービス定義に対する明示的なファクトリクラスのプロパティ](https://groups.google.com/forum/#!topic/symfony-devs/6cMns13edtg)
  * [Symfonyの名前空間に対するバンドルのカテゴリ](https://groups.google.com/forum/#!topic/symfony-devs/AXI8nK4BQPw)
  * [RFCとExtensionのリファクタリングへのアップデート](https://groups.google.com/forum/#!topic/symfony-devs/3nwwiUaT4ds)

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [fb889a2](http://github.com/symfony/symfony/commit/fb889a2eee33db42ba5ec6af8e5c142f2c2b6d63 "fb889a2eee33db42ba5ec6af8e5c142f2c2b6d63 commit on github"), [cd96c91](http://github.com/symfony/symfony/commit/cd96c914477fb8ee2640cf98e72a0468570a515f "cd96c914477fb8ee2640cf98e72a0468570a515f commit on github"): 読みやすさのために、いくつかのvar_export()をjson_encode()に置き換え
  * [57ae50e](http://github.com/symfony/symfony/commit/57ae50e8942f1a3ee9431c320b404fc1b016b87c "57ae50e8942f1a3ee9431c320b404fc1b016b87c commit on github"): \[Security\] 多くの改善と修正
  * [e645090](http://github.com/symfony/symfony/commit/e645090423a037912ac5e0c43bc3ea104998fa2a "e645090423a037912ac5e0c43bc3ea104998fa2a commit on github"): セキュリティ関連の実装を新しいSecurityBundleへ移動(Securityコンポーネントは変更されないまま)
  * <del>[24c7715](http://github.com/symfony/symfony/commit/24c7715029548164f93fd671d1e3009ce590637a "24c7715029548164f93fd671d1e3009ce590637a commit on github"): \[DoctrineBundle\] セキュリティユーザプロバイダのEM/DMエイリアス向けにDICパラメータを作成</del>
  * [75404e6](http://github.com/symfony/symfony/commit/75404e6bd642f831efe4b976a83f7143183d99d7 "75404e6bd642f831efe4b976a83f7143183d99d7 commit on github"): HttpKernel/Cache/名前空間をHttpKernel/HttpCache/に変更
  * [cf64d2c](http://github.com/symfony/symfony/commit/cf64d2cfe7f348b6ed8dd5504f7052b5b3cbe61d "cf64d2cfe7f348b6ed8dd5504f7052b5b3cbe61d commit on github"): Security Componentの名前空間を変更
  * [ff34f7d](http://github.com/symfony/symfony/commit/ff34f7d2816813bb1a2a2d4512e71ba11a2b1636 "ff34f7d2816813bb1a2a2d4512e71ba11a2b1636 commit on github"): \[DoctrineMongoDBBundle\] 複数のドキュメントマネージャのサポートを追加
  * [0219ec3](http://github.com/symfony/symfony/commit/0219ec3dbcb497b469d254c3f16c9ca124cf2a46 "0219ec3dbcb497b469d254c3f16c9ca124cf2a46 commit on github"): \[DependencyInjection\] ContainerInterfaceクラス内の忘れられていたメソッドを追加
  * [7bd3039](http://github.com/symfony/symfony/commit/7bd30398c66c2397e3157bd886ed0583eb8ef049 "7bd30398c66c2397e3157bd886ed0583eb8ef049 commit on github"): \[FrameworkBundle\] いくつかのキャッシュウォーマを移動
  * [42f9c55](http://github.com/symfony/symfony/commit/42f9c556a35af616d3239df64f42c15b98602472 "42f9c556a35af616d3239df64f42c15b98602472 commit on github"), [6997fba](http://github.com/symfony/symfony/commit/6997fbac0d4019aed2747efeb504dea0419bff6f "6997fbac0d4019aed2747efeb504dea0419bff6f commit on github"), [95e10b3](http://github.com/symfony/symfony/commit/95e10b3ed9642332547e26739c3f10a1ae81e7b4 "95e10b3ed9642332547e26739c3f10a1ae81e7b4 commit on github"): クラスローダをコンポーネントに追加
  * [8ccb8eb](http://github.com/symfony/symfony/commit/8ccb8eb8c2c8a1aec2aa042366353476ca8af728 "8ccb8eb8c2c8a1aec2aa042366353476ca8af728 commit on github"): security.interactive_loginとsecurity.switch_userイベントを追加
  * [db81828](http://github.com/symfony/symfony/commit/db818284afce20c20d495422738aa797151fd429 "db818284afce20c20d495422738aa797151fd429 commit on github"): キャッシュ内のclass compiledをFrameworkBundleへ移動
  * [2509c9d](http://github.com/symfony/symfony/commit/2509c9da4b33645f35d4bc672aa832d745d3b8be "2509c9da4b33645f35d4bc672aa832d745d3b8be commit on github"): クラスマップに使用するオートローダを追加 (Symfony2におけるクラスは4つの異なる仕組みからロードされる。すなわち、bootstrap.php, classes.php, MapFileClassLoader, UniversalAutoloaderである)
  * [3c9c43d](http://github.com/symfony/symfony/commit/3c9c43d59286c46149a5f6c4bbf1ed912749d644 "3c9c43d59286c46149a5f6c4bbf1ed912749d644 commit on github"): \[DoctrineBundle\] dbal設定セクションを通じてDBAL Typesを設定できるよう機能追加
  * [6337506](http://github.com/symfony/symfony/commit/63375060e829b4dc2d1354250650f5d0723884aa "63375060e829b4dc2d1354250650f5d0723884aa commit on github"): \[DoctrineBundle\] doctrine-1.0.xsdをリファクタリング
  * [224e66f](http://github.com/symfony/symfony/commit/224e66f77b889db2630aa66206efba1c522da97e "224e66f77b889db2630aa66206efba1c522da97e commit on github"), [98c1056](http://github.com/symfony/symfony/commit/98c1056fbfd3a3ab3cbdc6fffc1a59929671733c "98c1056fbfd3a3ab3cbdc6fffc1a59929671733c commit on github"): \[HttpFoundation\] スタティックメソッドRequest::fromGlobals()を追加 (RequestのコンストラクタはもはやPHPのスーパーグローバルからの値を使わない。あなたの実装したフロントコントローラはアップデートされる必要がある)
  * [803dd58](http://github.com/symfony/symfony/commit/803dd58002b7bb80d90a1cc09ee3112c05e58c5e "803dd58002b7bb80d90a1cc09ee3112c05e58c5e commit on github"): 継承サポートの定義を追加
  * [0c3ca26](http://github.com/symfony/symfony/commit/0c3ca26e6e660045a0a09b4f14b8c45f99a1c565 "0c3ca26e6e660045a0a09b4f14b8c45f99a1c565 commit on github"): \[Validator\] @Valid制約を使う\Traversableオブジェクトトラバースを実装
  * [ce61baf](http://github.com/symfony/symfony/commit/ce61baf7178c20d52b0889ad762e26fe4f9b0f42 "ce61baf7178c20d52b0889ad762e26fe4f9b0f42 commit on github"): \[Form\] ChoiceFieldが'choices'オプション内でクロージャを許容するよう修正
  * [34865a3](http://github.com/symfony/symfony/commit/34865a35330daeccfedf02f24cb3724473d1ce1e "34865a35330daeccfedf02f24cb3724473d1ce1e commit on github"): \[Form\] AssertType('\DateTime')制約へのフィールド推測を追加
  * [ebd2ca6](http://github.com/symfony/symfony/commit/ebd2ca6cfe77543c8bcd06435d87902f5f765aa3 "ebd2ca6cfe77543c8bcd06435d87902f5f765aa3 commit on github"): \[Form\] ChoiceFieldに'empty_value'オプションを移動。フィールドが要求されない時は空の値が表示される。
  * [62d52d8](http://github.com/symfony/symfony/commit/62d52d8015b0ec90077a1f5302feb58e00121651 "62d52d8015b0ec90077a1f5302feb58e00121651 commit on github"): normalizeConfig()が不正な複数のフォームをハンドルできるように修正
  * [bdbfb44](http://github.com/symfony/symfony/commit/bdbfb44a96765a8b3d2a0898996160c1a2cc1c13 "bdbfb44a96765a8b3d2a0898996160c1a2cc1c13 commit on github"), [5014ee9](http://github.com/symfony/symfony/commit/5014ee9739d7cb741afd81371bec97f089698d44 "5014ee9739d7cb741afd81371bec97f089698d44 commit on github"): \[DoctrineBundle\] DoctrineBundle内のCommand名前空間をクリーンアップ
  * [c4a2fb4](http://github.com/symfony/symfony/commit/c4a2fb41ec32af5c3fd4ecd944a75950808dc0c7 "c4a2fb41ec32af5c3fd4ecd944a75950808dc0c7 commit on github"): \[DoctrineBundle\] Windowsのファイルパス長エラーを回避するため、Dependency Injection Fixture名前空間を短縮
  * [65eb70d](http://github.com/symfony/symfony/commit/65eb70d3b6373ace7ba85df404e88795cf9b5fa7 "65eb70d3b6373ace7ba85df404e88795cf9b5fa7 commit on github"): \[Kernel\] バンドル管理の微調整
  * [e23f39c](http://github.com/symfony/symfony/commit/e23f39c42fd3b1e113d08c24bfdfefd53ad66dfb "e23f39c42fd3b1e113d08c24bfdfefd53ad66dfb commit on github"): \[Security\] 設定のリファクタリング
  * [8a87953](http://github.com/symfony/symfony/commit/8a879531bdd2a4e79c51d5dcb310cecb1d80c650 "8a879531bdd2a4e79c51d5dcb310cecb1d80c650 commit on github"): \[Security\] キーノーマライゼーションを追加、いくつかの条件文を削除
  * [2539da5](http://github.com/symfony/symfony/commit/2539da5e6a05851be9bbc7ad1b4eb7906185b4db "2539da5e6a05851be9bbc7ad1b4eb7906185b4db commit on github"): \[Security\] AbstractFactoryを追加
  * [f2a3135](http://github.com/symfony/symfony/commit/f2a3135bd0644fa58b884d50ee4320a63e0c8029 "f2a3135bd0644fa58b884d50ee4320a63e0c8029 commit on github"): \[Security\] 各ファイアウォールはユニークな名前が必要
  * [025e142](http://github.com/symfony/symfony/commit/025e142dd474aacad7629ba5eb939f61979b7c70 "025e142dd474aacad7629ba5eb939f61979b7c70 commit on github"): IRCミーティングで決定されたようにパラメータコンバータを削除(サポートされるのは依然としてFrameworkExtraBundleで提供されるもの)
  * [5f11e49](http://github.com/symfony/symfony/commit/5f11e49d0bfa32e28da75556e1dacad37fa548e8 "5f11e49d0bfa32e28da75556e1dacad37fa548e8 commit on github"): \[HttpKernel\] 例外をより強固に変更 (PHPエラーの深すぎるネストを回避)
  * [5e5b6f0](http://github.com/symfony/symfony/commit/5e5b6f0cf82b22b9d187b538829aaf0d42539b3d "5e5b6f0cf82b22b9d187b538829aaf0d42539b3d commit on github"): \[HttpKernel\] 親バンドルが子バンドルよりも先に登録されることを確実に
  * [b7a0f71](http://github.com/symfony/symfony/commit/b7a0f71b8745dba38be28e41c98c307b9f69f70f "b7a0f71b8745dba38be28e41c98c307b9f69f70f commit on github"): \[FrameworkBundle\] PHPテンプレートエンジンを使用している場合のために、より多くのファイルがクラスキャッシュに追加される
  * [d1cd442](http://github.com/symfony/symfony/commit/d1cd442361bf16f1c5227ee495cbf0b549455928 "d1cd442361bf16f1c5227ee495cbf0b549455928 commit on github"): \[FrameworkBundle\] テスト環境用にセッションリスナを追加
  * [b52e282](http://github.com/symfony/symfony/commit/b52e28243d37435d88bd658e61b8cc0b77039d7a "b52e28243d37435d88bd658e61b8cc0b77039d7a commit on github"): \[HttpFoundation\] ApacheRequestを追加
  * [839cb02](http://github.com/symfony/symfony/commit/839cb027a66836505e856bd146702fb52c710781 "839cb027a66836505e856bd146702fb52c710781 commit on github"): \[HttpKernel\] HTTPキャッシュフロントコントローラ用ブートストラップファイルを追加
  * [2c43554](http://github.com/symfony/symfony/commit/2c4355460e19f52ea0c1f94e91a810f7b1ad1382 "2c4355460e19f52ea0c1f94e91a810f7b1ad1382 commit on github"): \[HttpKernel\] StoreInterfaceを追加
  * [347c069](http://github.com/symfony/symfony/commit/347c069e8d8b810726aed2688ca2a2fbab1e6926 "347c069e8d8b810726aed2688ca2a2fbab1e6926 commit on github"): \[DoctrineBundle, Form\] EntityChoiceFieldの実装
  * [3bf9f77](http://github.com/symfony/symfony/commit/3bf9f7782debd42bc1cd050ea0b51ef14fbf8e17 "3bf9f7782debd42bc1cd050ea0b51ef14fbf8e17 commit on github"): \[DoctrineBundle, Form\] EntityFieldFactoryGuesserの実装
  * [d152b5e](http://github.com/symfony/symfony/commit/d152b5e265541b3cde746d7ad0c59dd8d6255259 "d152b5e265541b3cde746d7ad0c59dd8d6255259 commit on github"): \[Form\] Doctrine2定義ファイルを移動
  * [57cbd57](http://github.com/symfony/symfony/commit/57cbd572658a2169b4dfe409096852edb91422a7 "57cbd572658a2169b4dfe409096852edb91422a7 commit on github"): \[Form\] フィールドは匿名化される一方、匿名フィールドはグループには追加されない
  * [4fcb985](http://github.com/symfony/symfony/commit/4fcb98547ce20f2e1e3bfe5be52af29355974e51 "4fcb98547ce20f2e1e3bfe5be52af29355974e51 commit on github"): \[Form\] Form::bind()を単純化し、コンビニエンスメソッドForm::bindRequest()とForm::bindGlobals()を追加
  * [c468db5](http://github.com/symfony/symfony/commit/c468db5c5bfdba26d67ca842544b59354768d752 "c468db5c5bfdba26d67ca842544b59354768d752 commit on github"): \[Form\] 単純化のため、FieldGroupとFormクラスを統合
  * [fdbc064](http://github.com/symfony/symfony/commit/fdbc064f0610b548f015f87bacdfe71485abe62e "fdbc064f0610b548f015f87bacdfe71485abe62e commit on github"): \[Form\] Formコンポーネント内の自動的なロケールの配置を削除
  * [e5ed98c](http://github.com/symfony/symfony/commit/e5ed98c324819a134490455a6ee5d2d49ece744e "e5ed98c324819a134490455a6ee5d2d49ece744e commit on github"): \[Form\] 固定値をフィールドに投入できるよう、'data'オプションをFieldに追加
  * [fb1f991](http://github.com/symfony/symfony/commit/fb1f99137dc023d63bc7022c4788009155efa139 "fb1f99137dc023d63bc7022c4788009155efa139 commit on github"): \[Form\] バウンドフォームの語義の変更(フォームは常に境界である必要があり、リクエストがPOSTであるかどうかとは独立する)
  * [a28151a](http://github.com/symfony/symfony/commit/a28151a8afd0ec11231663e1633cfd8a406df837 "a28151a8afd0ec11231663e1633cfd8a406df837 commit on github"): \[Form\] FormFactoryの削除とフォームのインスタンス化プロセスの改良
  * [b484763](http://github.com/symfony/symfony/commit/b484763a7a331d68504b5b047c733ab076d266b9 "b484763a7a331d68504b5b047c733ab076d266b9 commit on github"): \[DependencyInjection\] コンフィグノーマライザの最初のバージョンを追加(これは主に複雑な設定向けで、YAMLやXML、PHPのような一般化された異なる設定フォーマットによって作業を楽にするものである)
  * [e6dc155](http://github.com/symfony/symfony/commit/e6dc155e89f8273263d7df06e00e367423b821cc "e6dc155e89f8273263d7df06e00e367423b821cc commit on github"): バリデータクラスでのメタデータの警告を修正
  * [628a4d1](http://github.com/symfony/symfony/commit/628a4d1fd8f5e9a65bdea6adfaf43e691cea5c89 "628a4d1fd8f5e9a65bdea6adfaf43e691cea5c89 commit on github"): \[Form\] バリデーションのロジックをvalidate()メソッドにリファクタリング。APIの乱雑さを低減するためbindGlobals()を削除
  * [4f0283a](http://github.com/symfony/symfony/commit/4f0283a508c26b3bf1f761b587eb1d2bf65a86fe "4f0283a508c26b3bf1f761b587eb1d2bf65a86fe commit on github"): \[Form\] Form::isBound()を削除。Form::bind()が唯一のショートカットメソッドとなったので、フォームが送信されたかどうかを知りたい場合はForm::isSubmitted()を使用すること
  * [c923af2](http://github.com/symfony/symfony/commit/c923af287956c7acad12ff111c23609f72f88432 "c923af287956c7acad12ff111c23609f72f88432 commit on github"): \[Form\] 他のフィールドのコンストラクタと一致するようCollectionFieldのコンストラクタを導入
  * [5e3fab2](http://github.com/symfony/symfony/commit/5e3fab214e286816bd199d86e075e8caae69ecbb "5e3fab214e286816bd199d86e075e8caae69ecbb commit on github"): \[Form\] フォームがデータとは別にバリデートされるよう修正
  * [7c9c7af](http://github.com/symfony/symfony/commit/7c9c7af863e355904c4eeab4de57f331bc87bbe1 "7c9c7af863e355904c4eeab4de57f331bc87bbe1 commit on github"): \[Form\] 配列がバリデータに渡されないのを修正
  * [5ed4d91](http://github.com/symfony/symfony/commit/5ed4d91bb864e5209938270918af95aaee5d900d "5ed4d91bb864e5209938270918af95aaee5d900d commit on github"): \[Validator\] Execute制約を実装
  * [1a34743](http://github.com/symfony/symfony/commit/1a34743990c464b0d73d8b6aecf1d4da0145a332 "1a34743990c464b0d73d8b6aecf1d4da0145a332 commit on github"): \[Validator\] @Valid注釈付のCollectionsがスカラ値を含むよう修正
  * [39c1481](http://github.com/symfony/symfony/commit/39c148197f3c4f8efb4e6534259619f473292b69 "39c148197f3c4f8efb4e6534259619f473292b69 commit on github"): \[Form\] フォームバリデーションを修正(データとフォームを分離したバリデーションに深刻な欠陥があった)
  * [c05fb03](http://github.com/symfony/symfony/commit/c05fb03c7db973df27111434fa9643d0e130ddcc "c05fb03c7db973df27111434fa9643d0e130ddcc commit on github"): \[HttpKernel\] コントローラがレスポンスを返さない場合の通知のみにcore.viewイベントが使われるように変更
  * [2d69369](http://github.com/symfony/symfony/commit/2d69369c69e8481c16b086341a5967a034f84e4a "2d69369c69e8481c16b086341a5967a034f84e4a commit on github"): \[ClassLoader\] 名前空間またはプレフィックスに対して1つより多いディレクトリを割り当てることができる機能を追加
  * [b6f400a](http://github.com/symfony/symfony/commit/b6f400a2bc2cea1cd4fcc71b2ac66518d885328b "b6f400a2bc2cea1cd4fcc71b2ac66518d885328b commit on github"): \[DependencyInjection\] ダンプされたDICに対する最適化
  * [f4282ee](http://github.com/symfony/symfony/commit/f4282eea98a3cd3ec349116cd7be4b3be0beb026 "f4282eea98a3cd3ec349116cd7be4b3be0beb026 commit on github"): \[Routing\] 絶対パス指定のURL中にある一般的でないポート番号のサポートを追加
  * [ea536b0](http://github.com/symfony/symfony/commit/ea536b0d9ee17ef60cd3940c88ee2b7ee3dbf26b "ea536b0d9ee17ef60cd3940c88ee2b7ee3dbf26b commit on github"): \[FrameworkBundle\] キャッシュウォーマの優先度を追加
  * [3ed4711](http://github.com/symfony/symfony/commit/3ed47114d6d447107e992941b8c866072978ec72 "3ed47114d6d447107e992941b8c866072978ec72 commit on github"), [f455700](http://github.com/symfony/symfony/commit/f455700b88b557e19c05b3408a771cc1fe6d2827 "f455700b88b557e19c05b3408a771cc1fe6d2827 commit on github"): \[Bundle\] getPath()に関して、前後の切りつめを許容することでエラーが出にくいように修正
  * [710a1e5](http://github.com/symfony/symfony/commit/710a1e56b0ef5682b616ac1cd1b44844d6883421 "710a1e56b0ef5682b616ac1cd1b44844d6883421 commit on github"): \[TwigBundle\] Twig_Templateインスタンスとしてのテンプレートのサポートを追加
  * [1e3dc14](http://github.com/symfony/symfony/commit/1e3dc1479ce2c064947dd9d10a65c655ee49076f "1e3dc1479ce2c064947dd9d10a65c655ee49076f commit on github"): \[Testing, HttpKernel\] Raw body dataの機能テストに向けた可能性を付与
  * [7f6fc6f](http://github.com/symfony/symfony/commit/7f6fc6f0fbd442ee0c49673b42b5fcc8ac6824fa "7f6fc6f0fbd442ee0c49673b42b5fcc8ac6824fa commit on github"): \[TwigBundle\] フォームテンプレートの継承を修正

ドキュメンテーション
-------------

  * 新しい<a href="http://trac.symfony-project.org/wiki/SfLiveSfHackday2011">Symfony Live - San Francisco Hackday 2011</a>と<a href="http://trac.symfony-project.org/wiki/IRCLogs20110203">IRC ログ 2011-02-03</a>ページ

