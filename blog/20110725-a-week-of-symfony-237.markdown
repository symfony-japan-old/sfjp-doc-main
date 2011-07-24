A week of symfony #237 (11->17 July 2011)
=========================================

Symfony2は今週[クッキー管理の方法](https://github.com/symfony/symfony/commit/f08eeb443345237ac4629d1aabfd755fcc2ef218)を変更し、[Security ComponentからDoctrine bridgeへ](https://github.com/symfony/symfony/commit/1633cb30bdafe96337d021b8fd357035322094d5)EntityUserProviderを移動し、マイナーなエラーを修正した。また、Symfony2の最終リリース準備のための安定版を公開している外部のSymfony2ライブラリグループが参加して、Twig は性能が改善されたバージョン1.1.1となり、Assetic1.0の最終安定版を公開した。

開発メーリングリスト
------------------------

  * [現在のリクエストのすべてをアクションに含める](https://groups.google.com/forum/#!topic/symfony-devs/30SznkjIuRI)
  * [命名規則](https://groups.google.com/forum/#!topic/symfony-devs/3ECsenFBJKw)

Symfony2開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [ea7a0eb](http://github.com/symfony/symfony/commit/ea7a0eb19c487e882693659d472aca61bed4a9ed "ea7a0eb19c487e882693659d472aca61bed4a9ed commit on github"): [Security] パターンで{_locale}を使用した際のリダイレクトURLの修正
  * [30d348d](http://github.com/symfony/symfony/commit/30d348d18db64072b7eb948277bbaa05e346d5ee "30d348d18db64072b7eb948277bbaa05e346d5ee commit on github"): [Form] デフォルト無効メッセージを翻訳可能に作成
  * [0e4d057](http://github.com/symfony/symfony/commit/0e4d057984e6b71f9ae270b2301691fe1b9ee70a "0e4d057984e6b71f9ae270b2301691fe1b9ee70a commit on github"): いくつかのレスポンスのRFC対応を調整するロジックのパブリックメソッドを再利用するため移動
  * [dbe1854](http://github.com/symfony/symfony/commit/dbe1854e1f1d59c020dcf11ef11d8cb3d4aa3a5d "dbe1854e1f1d59c020dcf11ef11d8cb3d4aa3a5d commit on github"): AccessDeniedExceptionをラップするAccessDeniedHttpExceptionを追加
  * [00c7e91](http://github.com/symfony/symfony/commit/00c7e91182fb3e6995d8b208ac5bd9f3429cf81a "00c7e91182fb3e6995d8b208ac5bd9f3429cf81a commit on github"): [HttpKernel] CLIを使用する特殊なケースを削除
  * [e718a51](http://github.com/symfony/symfony/commit/e718a51b595ab80bf5352727380348b9392b0f9f "e718a51b595ab80bf5352727380348b9392b0f9f commit on github"): [DependencyInjection] エイリアスに関わる循環参照の非検出を修正
  * [f08eeb4](http://github.com/symfony/symfony/commit/f08eeb443345237ac4629d1aabfd755fcc2ef218 "f08eeb443345237ac4629d1aabfd755fcc2ef218 commit on github"): HeaderBagの管理クッキーをResponseHeaderBagに移動
  * [d34caee](http://github.com/symfony/symfony/commit/d34caeea3a689ea8ff34eaee0545a94ec2523575 "d34caeea3a689ea8ff34eaee0545a94ec2523575 commit on github"): field_labelブロックとform_labelブロックをgeneric_labelにマージと統一
  * [f91f4dd](http://github.com/symfony/symfony/commit/f91f4dda135f8144a6991c0d2dfdfafd4adf63a8 "f91f4dda135f8144a6991c0d2dfdfafd4adf63a8 commit on github"): 別のドメインとパスに同じ名前のクッキーを設定する方法を追加
  * [2a24603](http://github.com/symfony/symfony/commit/2a2460306164f296bb5930931b1dd931bbac1c26 "2a2460306164f296bb5930931b1dd931bbac1c26 commit on github"): [Routing] 単一メソッドでデフォルト名を持つ複数の@routeアノテーションを許可
  * [88d915d](http://github.com/symfony/symfony/commit/88d915d1754b0ca318af0447d9629c29cbc195fd "88d915d1754b0ca318af0447d9629c29cbc195fd commit on github"): [Validator] 入力値が数値でない時のMinとMaxバリデータを修正(現在は例外の代わりにエラーメッセージを返す)
  * [91cfb24](http://github.com/symfony/symfony/commit/91cfb24e40de915a6482854615eeb542342a181f "91cfb24e40de915a6482854615eeb542342a181f commit on github"): 各環境に固有のDoctrineキャッシュの名前空間を作成
  * [df34e0e](http://github.com/symfony/symfony/commit/df34e0eb2939e173a48f7b4aa4de39a42b596d1e "df34e0eb2939e173a48f7b4aa4de39a42b596d1e commit on github"): [FrameworkBundle] カスタムファイルのリンクのフォーマットを設定するため修正
  * [1633cb3](http://github.com/symfony/symfony/commit/1633cb30bdafe96337d021b8fd357035322094d5 "1633cb30bdafe96337d021b8fd357035322094d5 commit on github"), [b33e1ba](http://github.com/symfony/symfony/commit/b33e1bae296cc152388db99957a14d90fdb812dd "b33e1bae296cc152388db99957a14d90fdb812dd commit on github"): [Security] EntityUserProviderをDoctrine Bridgeに移動
  * [182f9e6](http://github.com/symfony/symfony/commit/182f9e6508419dd4f4e945c3bcb3304091204519 "182f9e6508419dd4f4e945c3bcb3304091204519 commit on github"): [HttpFoundation] PHP_AUTH_*データに基づいて、Authorizationヘッダーの値を追加
  * [29e4063](http://github.com/symfony/symfony/commit/29e4063825cf394b60f54f8694114c343755f858 "29e4063825cf394b60f54f8694114c343755f858 commit on github"): [Security] 最初の特定の事をチェックするチェック順序の変更
  * [1238bb3](http://github.com/symfony/symfony/commit/1238bb3d5312cecb2a5037bff7c74b210c6053d3 "1238bb3d5312cecb2a5037bff7c74b210c6053d3 commit on github"): [HttpKernel] XDebugが有効になっている時、テストをパスするためFlattenExceptionのキープするレベルの数値を下げる (デフォルトの最大ネストレベルが100のため)
  * [c045120](http://github.com/symfony/symfony/commit/c04512086e60202a01125b7e0e5829b4d42f9671 "c04512086e60202a01125b7e0e5829b4d42f9671 commit on github"): [Validator] コレクションエラーが発生した時のエラーメッセージのプロパティパスの修正
  * [af67e65](http://github.com/symfony/symfony/commit/af67e65cbd576d1fde36 "af67e65cbd576d1fde36 commit on github"): [Form] validation_constraintのオプションを使用した際のバリデーションの修正
  * [2c224ce](http://github.com/symfony/symfony/commit/2c224ce42be53800ca70a767a84584f45ba73af1 "2c224ce42be53800ca70a767a84584f45ba73af1 commit on github"): 例外のメッセージを改善し、文字列内の文字列のみを許可する不必要な制約を削除
  * [634131b](http://github.com/symfony/symfony/commit/634131bc77f8ccf5038abcf2e69be3576c20383b "634131bc77f8ccf5038abcf2e69be3576c20383b commit on github"): [Twig] 深くネストされたコレクションでフォームをレンダリングする時にXDebugの持つ問題を回避するために小さな最適化を行った
  * [a1d8c70](http://github.com/symfony/symfony/commit/a1d8c70890510e0e24a5adda87a4ed98e3b7d947 "a1d8c70890510e0e24a5adda87a4ed98e3b7d947 commit on github"): [Routing] デフォルトの値が整数であるバグを修正


