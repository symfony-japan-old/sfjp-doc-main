---
layout: default
title: ﻿A week of symfony #232 (6->12 June 2011)
---

﻿A week of symfony #232 (6->12 June 2011)
========================================

今週の Symfony2 は、 [キャッシュウォーマを簡素化](https://github.com/symfony/symfony/commit/96fc666454195633043b162720940246af76f212) しリファクタリングされました。 Doctrine ブリッジも同じく [大幅にリファクタリング](https://github.com/symfony/symfony/commit/fbf36957e671721cc20cf76f16aeaab2723cd045) され、いくつかのクラスは [バンドルからブリッジに移動](https://github.com/symfony/symfony/commit/879242cdf5466f139b89c56fed71cd5d93fef39d) されました。コンソールコンポーネントはより強力になり、 Serializer コンポーネントはインタフェースが拡張され、内部が簡素化されました。いつもの通り、 Form コンポーネントは非常に活発に開発が行われ、 2.0 のリリースには含まれないことになった [ファイルアップロードのテンポラリストレージ機能が削除](https://github.com/symfony/symfony/commit/852a4c9c6a4103fcbc87e99135db4dadbc7ce2a4) されました。

開発メーリングリスト
--------------------

  * [\[Symfony2\] SecurityBundle refreshUser のパフォーマンス](https://groups.google.com/forum/#!topic/symfony-devs/TqqNBFIn2eI)
  * [\[Symfony2\] cache_warmer 設定オプションの一貫性のある使用法](https://groups.google.com/forum/#!topic/symfony-devs/rVPMfZqmU8Y)
  * [アノテーションの宣言の検出](https://groups.google.com/forum/#!topic/symfony-devs/63YgiunHPXQ)
  * [コンポーネントのサイトとフレームワーク内の Dependency Injector の違い](https://groups.google.com/forum/#!topic/symfony-devs/9_dULF4iMTU)
  * [AJAX 認証のリダイレクトの Symfony2 での扱い方](https://groups.google.com/forum/#!topic/symfony-devs/WvESDBprKrU)

symfony 1 開発ハイライト
------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=12%2F06%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r32635](http://trac.symfony-project.org/changeset/32635 "32635 revision on trac"): \[1.4\] fixed typo in sfNumberFormat のタイポを修正
  * [r32639](http://trac.symfony-project.org/changeset/32639 "32639 revision on trac"): \[1.4\] fixed typo in sfConfigCache のタイポを修正
  * [r32641](http://trac.symfony-project.org/changeset/32641 "32641 revision on trac"): \[1.4\] スタックトレースの追加コードを修正

Symfony2 開発ハイライト
-----------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [c2b9061](http://github.com/symfony/symfony/commit/c2b9061559a12adc9ecd5dc92f3b8f9b9034aca1 "c2b9061559a12adc9ecd5dc92f3b8f9b9034aca1 commit on github"): \[Form\] AbstractDivLayout のテストを追加
  * [eed54c1](http://github.com/symfony/symfony/commit/eed54c137e53a05e41a89e5e8978cc8b70bb24f0 "eed54c137e53a05e41a89e5e8978cc8b70bb24f0 commit on github"): \[Form\] FormView::isRendered() メソッドを修正
  * [181fb56](http://github.com/symfony/symfony/commit/181fb56925f1facfd126418c0cacc8aa25301f5f "181fb56925f1facfd126418c0cacc8aa25301f5f commit on github"), [6711a18](http://github.com/symfony/symfony/commit/6711a184fda31077de4f2c4d9bc33b21d1798963 "6711a184fda31077de4f2c4d9bc33b21d1798963 commit on github"): \[Form, Twig\] フォームテンプレートを再構成し簡素化
  * [bca17fe](http://github.com/symfony/symfony/commit/bca17fe6a33c39a4e0bc14b83baa8b9d75b2c07d "bca17fe6a33c39a4e0bc14b83baa8b9d75b2c07d commit on github"): \[Form\] コレクションのレンダリングを修正
  * [48733b9](http://github.com/symfony/symfony/commit/48733b927d3ebe6437f6f7cadf4acaea65a4909c "48733b927d3ebe6437f6f7cadf4acaea65a4909c commit on github"): \[Swiftmailer\] Swiftmailer プラグインを自動で登録するように swiftmailer.plugin タグを追加
  * [b12b11c](http://github.com/symfony/symfony/commit/b12b11c1314fd08ec09f84b01d28b6fe55144ee8 "b12b11c1314fd08ec09f84b01d28b6fe55144ee8 commit on github"): \[Form\] form_rest が呼び出された時、ネストされたビューがそれぞれレンダリングされてしまわないように修正
  * [60c463d](http://github.com/symfony/symfony/commit/60c463d184b4f5dd3d49eb4253b0750835c49787 "60c463d184b4f5dd3d49eb4253b0750835c49787 commit on github"): \[Form\] FormType ラベルが for 属性を持たないように変更
  * [5044a7b](http://github.com/symfony/symfony/commit/5044a7b56d8672308926bdf59c5f9d0fc6b3c9f6 "5044a7b56d8672308926bdf59c5f9d0fc6b3c9f6 commit on github"): \[Form, FrameworkBundle\] ビューのウィジェットで使用された時、ラベルが id 属性を含まないように修正
  * [8d2974c](http://github.com/symfony/symfony/commit/8d2974ce9088797776b0bde4e916f5e2ad4d03e4 "8d2974ce9088797776b0bde4e916f5e2ad4d03e4 commit on github"): \[Form\] ファイル入力のアクセシビリティを修正
  * [f303125](http://github.com/symfony/symfony/commit/f3031251c5ff9eb1e8c7555a8bac942b4b6841f9 "f3031251c5ff9eb1e8c7555a8bac942b4b6841f9 commit on github"): ログインパスとチェックパスにロケールのサポートを追加
  * [2a5d768](http://github.com/symfony/symfony/commit/2a5d7687b7b5fc5435e2187e4bc8c85e5c1aba9c "2a5d7687b7b5fc5435e2187e4bc8c85e5c1aba9c commit on github"): Router のキャッシュウォーマを修正
  * [85a381d](http://github.com/symfony/symfony/commit/85a381d0485e682a48dc63e65627bb27328c1bd4 "85a381d0485e682a48dc63e65627bb27328c1bd4 commit on github"): \[DoctrineBundle\] Registry::getConnections() を追加
  * [1c3fa20](http://github.com/symfony/symfony/commit/1c3fa206857450e626e413b390563177ecedd2fb "1c3fa206857450e626e413b390563177ecedd2fb commit on github"): \[DoctrineBundle\] Registry::getEntityManagers() を追加
  * [22428b8](http://github.com/symfony/symfony/commit/22428b8b144ee1b8a7580ee738a86d5601b954e3 "22428b8b144ee1b8a7580ee738a86d5601b954e3 commit on github"): \[DoctrineBundle\] Doctrine プロキシキャッシュウォーマをリファクタリング (Container の依存性を削除し、プロキシキャッシュはそれぞれのエンティティマネージャの設定を取得するようになりました)
  * [5af7c7f](http://github.com/symfony/symfony/commit/5af7c7fffd631c70ac67e157ee566a5164a9da60 "5af7c7fffd631c70ac67e157ee566a5164a9da60 commit on github"): 用途上そこでしか使用しないため、 TemplateFinder を CacheWarmer に移動
  * [5be0baf](http://github.com/symfony/symfony/commit/5be0bafe7f3c0b1035c53db406395e18a7b58f3b "5be0bafe7f3c0b1035c53db406395e18a7b58f3b commit on github"): TemplateReferenceInterface::getSignature() を削除 (既に存在していた一意な識別子である getLogicalName() で置き換え)
  * [b76eec7](http://github.com/symfony/symfony/commit/b76eec73b99484de4fd88d2f3866cc7365328e48 "b76eec73b99484de4fd88d2f3866cc7365328e48 commit on github"): \[HttpKernel\] キャッシュウォームアップが CLI でも動作するように変更
  * [96fc666](http://github.com/symfony/symfony/commit/96fc666454195633043b162720940246af76f212 "96fc666454195633043b162720940246af76f212 commit on github"): キャッシュウォーマを簡素化 (カーネルが最初に起動する際に常にキャッシュウォーマが実行され、オプションのキャッシュウォーマは cache:warmup コマンドで CLI からのみ実行されるように要求)
  * [116e004](http://github.com/symfony/symfony/commit/116e004f7dbe6505aaa749521bed3d431d21794b "116e004f7dbe6505aaa749521bed3d431d21794b commit on github"): \[DoctrineBundle\] Symfony2 では必要ないため doctrine:generate:proxies を削除
  * [41242dc](http://github.com/symfony/symfony/commit/41242dcc00169c7aa1fe578f87e03ae3ffeeb452 "41242dcc00169c7aa1fe578f87e03ae3ffeeb452 commit on github"): \[DoctrineBundle\] XML/YAML マッピングドライバーを Doctrine に対応するものとしてより BC になるよう変更
  * [fb051b2](http://github.com/symfony/symfony/commit/fb051b2f98ca036f220dc0219df404a2a26be353 "fb051b2f98ca036f220dc0219df404a2a26be353 commit on github"), [d9f00ca](http://github.com/symfony/symfony/commit/d9f00ca7be6ed8e0f6d67f68f918422df334aec7 "d9f00ca7be6ed8e0f6d67f68f918422df334aec7 commit on github"): \[Command\] 配列オプションのパースを修正
  * [37b2df2](http://github.com/symfony/symfony/commit/37b2df25bffafdc777023c668af97147d477f8be "37b2df25bffafdc777023c668af97147d477f8be commit on github"): \[FrameworkBundle\] コントローラからリクエストサービスを取得する新しい Controller::getRequest() メソッドを公開
  * [89f544a](http://github.com/symfony/symfony/commit/89f544afb672ee2b7b7cc59feda5252bdca2ee9c "89f544afb672ee2b7b7cc59feda5252bdca2ee9c commit on github"): Twig フォームテンプレートを Twig ブリッジに移動
  * [facff73](http://github.com/symfony/symfony/commit/facff730497c122a50539092abd4581fda8a618e "facff730497c122a50539092abd4581fda8a618e commit on github"), [7d3e20d](http://github.com/symfony/symfony/commit/7d3e20d87d949f3000bbacc7e1c029c2ce171ed4 "7d3e20d87d949f3000bbacc7e1c029c2ce171ed4 commit on github"), [d84728e](http://github.com/symfony/symfony/commit/d84728e278adf0d5772df5e264cfbfef4c76c31d "d84728e278adf0d5772df5e264cfbfef4c76c31d commit on github"): \[Console\] コンソールツールをより強化(ネストした名前空間のフルサポートを追加し、エイリアスは独自の名前空間を持てるようになりました)
  * [fbf3695](http://github.com/symfony/symfony/commit/fbf36957e671721cc20cf76f16aeaab2723cd045 "fbf36957e671721cc20cf76f16aeaab2723cd045 commit on github"): Doctrine Bridge をリファクタリング (RegistryInterface を追加し、全てのクラスは特定の EntityManagerの代わりに Registory に依存するようになりました)
  * [879242c](http://github.com/symfony/symfony/commit/879242cdf5466f139b89c56fed71cd5d93fef39d "879242cdf5466f139b89c56fed71cd5d93fef39d commit on github"): いくつかの Doctrine クラスをバンドルからブリッジに移動
  * [882a8e3](http://github.com/symfony/symfony/commit/882a8e3f09c602a6f0ed3b5bd20e8d4688331500 "882a8e3f09c602a6f0ed3b5bd20e8d4688331500 commit on github"): ログインパスとチェックパスにロケールのサポートを追加
  * [2d91183](http://github.com/symfony/symfony/commit/2d91183d86ac6839d1c86717802ed2bcf09c64f9 "2d91183d86ac6839d1c86717802ed2bcf09c64f9 commit on github"): \[DoctrineBridge\] フィールドを推測する仕組みを修正
  * [12dd52b](http://github.com/symfony/symfony/commit/12dd52b00b88a25328cde4062a8ccafc0db53d4a "12dd52b00b88a25328cde4062a8ccafc0db53d4a commit on github"): \[FrameworkBundle\] cache:clear の --without-debug オプションを削除 (親となるカーネルからデバッグフラグを継承するようになりました)
  * [740b2ac](http://github.com/symfony/symfony/commit/740b2ac8337b2cf9ba889477b9dbb6466c2e2896 "740b2ac8337b2cf9ba889477b9dbb6466c2e2896 commit on github"): \[Console\] ANSI 出力を無効にする --no-ansi オプションを追加
  * [188e742](http://github.com/symfony/symfony/commit/188e74273a3c1985d03d841329db9de2fcf13701 "188e74273a3c1985d03d841329db9de2fcf13701 commit on github"): \[Security\] サブリクエストの生成を修正
  * [f16e206](http://github.com/symfony/symfony/commit/f16e206cd72f1d4494cc7ae9bac47bdab90fb41d "f16e206cd72f1d4494cc7ae9bac47bdab90fb41d commit on github"): \[HttpFoundation\] リクエストヘッダーに不足していた CONTENT_TYPE と CONTENT_LENGTH を追加
  * [0af4743](http://github.com/symfony/symfony/commit/0af4743583c9bbdda80272a97cc82425ab93e8f8 "0af4743583c9bbdda80272a97cc82425ab93e8f8 commit on github"): \[HttpFoundation\] mime-type がオプションのパラメータを保持している時の Request::getFormat() を修正
  * [566511e](http://github.com/symfony/symfony/commit/566511e9e7d965d0e55f8abe04515db53ac009ea "566511e9e7d965d0e55f8abe04515db53ac009ea commit on github"): いくつかの FormView のメソッドを、実際に属している FormUtil に移動
  * [bee505a](http://github.com/symfony/symfony/commit/bee505a4bf9eaba13dd4798cd297bb9ab18198b5 "bee505a4bf9eaba13dd4798cd297bb9ab18198b5 commit on github"), [5060702](http://github.com/symfony/symfony/commit/506070266940f0c0f4c8f3265b67440cd1d54475 "506070266940f0c0f4c8f3265b67440cd1d54475 commit on github"): \[Form\] Twig テーマの継承を修正
  * [fd97dd0](http://github.com/symfony/symfony/commit/fd97dd00599a0220a0750faf3cd04aed1496df70 "fd97dd00599a0220a0750faf3cd04aed1496df70 commit on github"): \[Form\] 明示的に設定されずデータクラスがセットされていない場合のデフォルトをテキスト型に変更
  * [852a4c9](http://github.com/symfony/symfony/commit/852a4c9c6a4103fcbc87e99135db4dadbc7ce2a4 "852a4c9c6a4103fcbc87e99135db4dadbc7ce2a4 commit on github"): \[Form\] ファイルアップロードのテンポラリストレージ機能を削除 (現在の実装は 2.0 に含むには不十分。既知の問題が存在 (セキュリティ、無効化できない、クラウドと互換性がない...)
  * [34b5a67](http://github.com/symfony/symfony/commit/34b5a67987dfdccc9275d3a4440c8b0b9ce75280 "34b5a67987dfdccc9275d3a4440c8b0b9ce75280 commit on github"), [e694397](http://github.com/symfony/symfony/commit/e694397f1683bfbd96a7a4c42aeec2a169fa9b8d "e694397f1683bfbd96a7a4c42aeec2a169fa9b8d commit on github"), [46da5ff](http://github.com/symfony/symfony/commit/46da5ff0699586cee7bb30e07facf1e3f4f68328 "46da5ff0699586cee7bb30e07facf1e3f4f68328 commit on github"), [f67b3f5](http://github.com/symfony/symfony/commit/f67b3f508e72e466a97c508d2206dbbf29a94745 "f67b3f508e72e466a97c508d2206dbbf29a94745 commit on github"): \[Serializer\] インタフェースを拡張、エンコーダとデコーダの冗長な管理を削除、例外を追加し、ゆるいロードを実装
  * [ea93e4c](http://github.com/symfony/symfony/commit/ea93e4cafaf048c88cce0af34c42f5e2da7b5793 "ea93e4cafaf048c88cce0af34c42f5e2da7b5793 commit on github"): \[Form\] フォームタイプの循環参照の防止機能を追加
  * [ce3839a](http://github.com/symfony/symfony/commit/ce3839a3eac5fcfe43f3f8c74f391f530154da13 "ce3839a3eac5fcfe43f3f8c74f391f530154da13 commit on github"): \[DoctrineBundle\] MetadataFactory クラスの代わりに doctrine:generate:entities で使われるようになった新しい DisconnectedMetadataFactory クラスを追加
  * [1daca76](http://github.com/symfony/symfony/commit/1daca761975484e36e5436e575d3f57df738a401 "1daca761975484e36e5436e575d3f57df738a401 commit on github"), [03a0566](http://github.com/symfony/symfony/commit/03a05661f9abadc51b892dd57d71acf5bfa22397 "03a05661f9abadc51b892dd57d71acf5bfa22397 commit on github"): \[Form\] フォームとデータパスが生成される方法を統一
  * [5458baf](http://github.com/symfony/symfony/commit/5458baf4658ceea6b91b0b79da0fff8614636260 "5458baf4658ceea6b91b0b79da0fff8614636260 commit on github"): \[MonologBundle\] デフォルトのバブリングの動作を変更
  * [cb53414](http://github.com/symfony/symfony/commit/cb53414e9103200938ebe34248b25d36dcb3adfe "cb53414e9103200938ebe34248b25d36dcb3adfe commit on github"): \[Form\] リサイズリスナーの影響でコレクションフィールドに CSRF トークンが与えられない問題を修正
  * [fe4382e](http://github.com/symfony/symfony/commit/fe4382eb73a2da87996c60021e5b8bde2f5635e0 "fe4382eb73a2da87996c60021e5b8bde2f5635e0 commit on github"): \[Form\] CSRF リスナーを独自のクラスに移動
  * [10bb4ff](http://github.com/symfony/symfony/commit/10bb4ff25e8a461febffc252f60264a8871bc74b "10bb4ff25e8a461febffc252f60264a8871bc74b commit on github"): \[Routing\] PhpMatcherDumper を最適化。キャッチされた URL マッチャークラスが必要のないロジックを含んでいたのを修正
  * [9604573](http://github.com/symfony/symfony/commit/96045739b198b030ab159425ce19614fe2e0e665 "96045739b198b030ab159425ce19614fe2e0e665 commit on github"): \[TwigBundle\] extensions 設定を削除。 Twig エクステンションは、 twig.extension タグを通じて設定するしかなくなりました


