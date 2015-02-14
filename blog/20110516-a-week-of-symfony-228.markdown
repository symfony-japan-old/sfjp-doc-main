---
layout: default
title: A week of symfony #228 (9->15 May 2011)
---

A week of symfony #228 (9->15 May 2011)
=======================================

今週のSymfony2では、いくつかのバンドルにおいてDICのパラメータを再び導入しました：エラーページテンプレートのカスタマイズをよりシンプルにしました(https://github.com/symfony/symfony-docs/commit/736fc4c6ecf88c7d4e7779851400b48a4c7e63c5)。 また、Asseticバンドルではパスに基づいたアセットに自動適用フィルターの設定を導入しました(https://github.com/symfony/symfony/commit/4ae40f1ea4fca1574282abe709517c312159c7f1)。同時に、Symfony2のドキュメントチームは作業を続けており、セキュリティコンポーネントのドキュメントが整備されました(https://github.com/symfony/symfony-docs/pull/288)。


開発ML
------------------------

  * [\[Symfony2\] XMLの設定に関する考えについて](https://groups.google.com/forum/#!topic/symfony-devs/FcZ0rhlmLd0)
  * [\[Symfony2\] 403, 404, 500等のテンプレートのカスタマイズは難しすぎないですか？](https://groups.google.com/forum/#!topic/symfony-devs/hHI3CwIB4nY)
  * [Symfony2アプリケーションのプロファイリングについて](https://groups.google.com/forum/#!topic/symfony-devs/r0wOiAMQcbg)
  * [\[Symfony2\] セキュリティコンポーネントに関する質問や考えについて](https://groups.google.com/forum/#!topic/symfony-devs/5hTpWDsVEiE)
  * [\[Symfony2\] より短いリリースサイクルについて](https://groups.google.com/forum/#!topic/symfony-devs/V2vnKSf_180)
  * [より複雑なルーティングについて](https://groups.google.com/forum/#!topic/symfony-devs/WpD4ntlB5yI)

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [0ed6d04](http://github.com/symfony/symfony/commit/0ed6d04a5fc894cea284e83b97af42dee84a2e7e "0ed6d04a5fc894cea284e83b97af42dee84a2e7e commit on github"), [c90c794](http://github.com/symfony/symfony/commit/c90c79472ca88b64993e7a7e99ba4da36e008061 "c90c79472ca88b64993e7a7e99ba4da36e008061 commit on github"): \[MonologBundle\] ハンドラーをBridgeのネームスペースに移動しました
  * [f78be41](http://github.com/symfony/symfony/commit/f78be41355f8d16ba35c0a5b63c12b7dea6de228 "f78be41355f8d16ba35c0a5b63c12b7dea6de228 commit on github"), [520941d](http://github.com/symfony/symfony/commit/520941d60d4825b8f30c1016839c119d305f233f "520941d60d4825b8f30c1016839c119d305f233f commit on github"): \[AsseticBundle\] デバッグモードごとにアセットをダンプするようにdumpコマンドを修正しました
  * [01a1049](http://github.com/symfony/symfony/commit/01a104916bfa610e1aa4ef2ea269301ae927cb54 "01a104916bfa610e1aa4ef2ea269301ae927cb54 commit on github"), [3ecc960](http://github.com/symfony/symfony/commit/3ecc9602e4e04c93dbe52f162983c60df82e0553 "3ecc9602e4e04c93dbe52f162983c60df82e0553 commit on github"), [24dcfef](http://github.com/symfony/symfony/commit/24dcfef33fa7da119e02a88387188ca5c21e0ad5 "24dcfef33fa7da119e02a88387188ca5c21e0ad5 commit on github"), [1f8defa](http://github.com/symfony/symfony/commit/1f8defaeebd716d3b8509ab080f75f945a702972 "1f8defaeebd716d3b8509ab080f75f945a702972 commit on github"), [89e056b](http://github.com/symfony/symfony/commit/89e056bb8b460e077efbc4e3330d79a695be78c9 "89e056bb8b460e077efbc4e3330d79a695be78c9 commit on github"), [e6a0248](http://github.com/symfony/symfony/commit/e6a02482c7ff8083cec69c501670d1ca0632891f "e6a02482c7ff8083cec69c501670d1ca0632891f commit on github"): \[Serializer\] SerializerAwareInterfaceを実装しました
  * [a4a40f5](http://github.com/symfony/symfony/commit/a4a40f57cdbbd3ee753b637369a5b61b9ebb5411 "a4a40f57cdbbd3ee753b637369a5b61b9ebb5411 commit on github"): \[MonologBundle\] デフォルトの値をConfigurationクラスに移動しました
  * [d8e6ab7](http://github.com/symfony/symfony/commit/d8e6ab7f7afeabf0f8078cae1f48f8989adaf36b "d8e6ab7f7afeabf0f8078cae1f48f8989adaf36b commit on github"): \[MonologBundle\] SwiftMailerHandlerとNativeMaileHandlerのサポートを追加しました
  * [ad41d21](http://github.com/symfony/symfony/commit/ad41d21675aa6fb6f40d6bde01fb9bfa3cf46090 "ad41d21675aa6fb6f40d6bde01fb9bfa3cf46090 commit on github"): \[FrameworkBundle\] Windows用にAssetsInstallCommandのエラーメッセージを追加しました
  * [f8447aa](http://github.com/symfony/symfony/commit/f8447aa74c21ed3644c09c975f626ded9e13abab "f8447aa74c21ed3644c09c975f626ded9e13abab commit on github"): \[Serializer\] NormalizableInterfaceはSerializerを受け取るように変更したので、formatは常にオプショナルとしました
  * [e1c5276](http://github.com/symfony/symfony/commit/e1c52764ce8dbb321dfff0088f9673820d529193 "e1c52764ce8dbb321dfff0088f9673820d529193 commit on github"): \[Finder\] SortableIteratorをリファクタリングしました
  * [05e75e2](http://github.com/symfony/symfony/commit/05e75e2712c6bfa19d72d92b235267bacd69e4ec "05e75e2712c6bfa19d72d92b235267bacd69e4ec commit on github"): \[Finder\] CustomフィルターがすべてのPHPのコールバックを受け取るようにしました
  * [9844685](http://github.com/symfony/symfony/commit/9844685a4013dda001076059c368c9b9b49b5e47 "9844685a4013dda001076059c368c9b9b49b5e47 commit on github"): \[HttpKernel\] ESIのキャッシュ戦略のデフォルトを微調整しました
  * [3854d34](http://github.com/symfony/symfony/commit/3854d34c1441c35b94ee4ac4e80486f59b3ea6fe "3854d34c1441c35b94ee4ac4e80486f59b3ea6fe commit on github"): \[DoctrineBundle\] 生成するエンティティがサブのネームスペースを持つ際のdoctrine:generate:entityコマンドを修正しました
  * [99c6713](http://github.com/symfony/symfony/commit/99c67134fe7fc5d6a13404c2ea5cdb9d06285ac8 "99c67134fe7fc5d6a13404c2ea5cdb9d06285ac8 commit on github"): \[Serializer\] decoder/encoder mapsを分割しました
  * [89f60e0](http://github.com/symfony/symfony/commit/89f60e04d1e09dcb0ed9bb98b204902aebb2b08e "89f60e04d1e09dcb0ed9bb98b204902aebb2b08e commit on github"), [411659b](http://github.com/symfony/symfony/commit/411659bc07bc99b0f4e83ce068f988926ce878a0 "411659bc07bc99b0f4e83ce068f988926ce878a0 commit on github"), [9408ab3](http://github.com/symfony/symfony/commit/9408ab30103398827313d2d9a68293e5fd323ea6 "9408ab30103398827313d2d9a68293e5fd323ea6 commit on github"): \[HttpFoundation\] getDeep()メソッドを削除して、代わりにget()メソッドにbooleanのフラグを追加しました
  * [d96e2c5](http://github.com/symfony/symfony/commit/d96e2c5d79a35fea38147669a456532281550761 "d96e2c5d79a35fea38147669a456532281550761 commit on github"): \[Validator\] CallbackValidatorにクロージャのサポートを追加しました
  * [7f95ea6](http://github.com/symfony/symfony/commit/7f95ea69aaffbdb44c2d02c26c4b9255102301cb "7f95ea69aaffbdb44c2d02c26c4b9255102301cb commit on github"): \[FrameworkBundle\] バリデータメッセージ: チェコ語の翻訳を追加しました
  * [aa71d16](http://github.com/symfony/symfony/commit/aa71d1681295c32230fbea53bc62871d5dd3b35a "aa71d1681295c32230fbea53bc62871d5dd3b35a commit on github"): \[Form\] TimezoneChoiceListクラスがArrayChoiceListを継承するのをやめて、ChoiceListInterfaceを実装するようにしました
  * [dac798c](http://github.com/symfony/symfony/commit/dac798c791aee2adde072f1f80bfd2c2f9c7c885 "dac798c791aee2adde072f1f80bfd2c2f9c7c885 commit on github"): \[Form\] DataTransformersで例外をキャッチするようにしました
  * [2e68801](http://github.com/symfony/symfony/commit/2e68801ff3524d1a7ee1856d25151d7cffc373d6 "2e68801ff3524d1a7ee1856d25151d7cffc373d6 commit on github"): \[Form\] BaseDateTimeTransformerの引数の型チェックを追加しました
  * [40795fc](http://github.com/symfony/symfony/commit/40795fcc5d88feda15cd4d0f56724745a24f7c3c "40795fcc5d88feda15cd4d0f56724745a24f7c3c commit on github"): \[MonologBundle\] GroupHandlerのサポートを追加しました
  * [514b47c](http://github.com/symfony/symfony/commit/514b47c6d4b3db59f32ebf37ca24702ccd15f550 "514b47c6d4b3db59f32ebf37ca24702ccd15f550 commit on github"): \[FrameworkBundle\] HTTPのステータスコードによって簡単にエラーをカスタマイズする方法を追加
  * [0bad012](http://github.com/symfony/symfony/commit/0bad0122903fad6039de16058d070294078d390e "0bad0122903fad6039de16058d070294078d390e commit on github"): \[FrameworkBundle\] ExceptionControllerのTemplateReferenceインスタンスによるテンプレート文字列を変更しました
  * [20c77ac](http://github.com/symfony/symfony/commit/20c77ac400eed5c07a7607fb46eb973b9c800e27 "20c77ac400eed5c07a7607fb46eb973b9c800e27 commit on github"), [b8f57c4](http://github.com/symfony/symfony/commit/b8f57c4bcdc5a42d82e00fcd1e4f274f03d7f86c "b8f57c4bcdc5a42d82e00fcd1e4f274f03d7f86c commit on github"), [d6d3516](http://github.com/symfony/symfony/commit/d6d3516d840569a2ff3f2a200403760bb5a54bf2 "d6d3516d840569a2ff3f2a200403760bb5a54bf2 commit on github"): \[MonologBundle\] MailHandler and GroupHandlerのスキーマ定義を追加しました
  * [0a3ff1c](http://github.com/symfony/symfony/commit/0a3ff1c737db8b0311dd96b32c0a337fbe7d8d4f "0a3ff1c737db8b0311dd96b32c0a337fbe7d8d4f commit on github"): \[HttpKernel\] ページがESIを含んでいない際のデフォルトのESIのキャッシュ戦略を修正しました
  * [08846af](http://github.com/symfony/symfony/commit/08846af9e23e08e57825e1f6717fcc68ce72682e "08846af9e23e08e57825e1f6717fcc68ce72682e commit on github"): \[HttpFoundation\] PUTメソッドの処理をcreateFromGlobals()メソッドに移動しました
  * [8f426c0](http://github.com/symfony/symfony/commit/8f426c0c772ea08881f7b7b86119a775c2a03ade "8f426c0c772ea08881f7b7b86119a775c2a03ade commit on github"): \[HttpKernel\] 起動時間中に使われる例外ハンドラーを追加しました
  * [0758033](http://github.com/symfony/symfony/commit/07580335b022649084dd5b148fc613e94ad60c6f "07580335b022649084dd5b148fc613e94ad60c6f commit on github"), [36d60a4](http://github.com/symfony/symfony/commit/36d60a4a877d1d5c01b7ad58f4bbfec509b83392 "36d60a4a877d1d5c01b7ad58f4bbfec509b83392 commit on github"): \[HttpKernel\] ExceptionHandlerをよりErrorHandlerらしく変更しました
  * [0de8a55](http://github.com/symfony/symfony/commit/0de8a55f02b9880298967e66fe59d0049e4450cf "0de8a55f02b9880298967e66fe59d0049e4450cf commit on github"), [05a946b](http://github.com/symfony/symfony/commit/05a946bf9dfd05ca1090a422bf1e6bf16905b977 "05a946bf9dfd05ca1090a422bf1e6bf16905b977 commit on github"), [f7aea2a](http://github.com/symfony/symfony/commit/f7aea2a830a131ceff5586ca3cc1703b19b3aeff "f7aea2a830a131ceff5586ca3cc1703b19b3aeff commit on github"), [4525eb9](http://github.com/symfony/symfony/commit/4525eb969097f4fa63dacff445da148343bc0589 "4525eb969097f4fa63dacff445da148343bc0589 commit on github"), [8dbccc7](http://github.com/symfony/symfony/commit/8dbccc7a8b0ed053144d93c66843b6c9c40580a8 "8dbccc7a8b0ed053144d93c66843b6c9c40580a8 commit on github"): より良いオーバーライドを実現するためにSecurytBundle、DoctrineBundle、FrameworkBundle、AsseticBundle、WebProfilerBundleのDICのパラメータを再導入しました
  * [faab5e4](http://github.com/symfony/symfony/commit/faab5e4452ade3a7ac8983806314d125400a9ab7 "faab5e4452ade3a7ac8983806314d125400a9ab7 commit on github"): \[HttpKernel\] エクステンションがlogs/やcaches/に何か書けるようにするため、log/ディレクトリとcacheディレクトリの作成をより処理の前に移動しました
  * [21013b9](http://github.com/symfony/symfony/commit/21013b930c04ce5bb903664541c9ab3856e3802a "21013b930c04ce5bb903664541c9ab3856e3802a commit on github"): \[Form\] FormFactoryのテストカバレッジを向上させて、エラーハンドリングを改良しました
  * [da28f8e](http://github.com/symfony/symfony/commit/da28f8e3b3ea52380c8197fd56fe0fd0300b7760 "da28f8e3b3ea52380c8197fd56fe0fd0300b7760 commit on github"), [7570e04](http://github.com/symfony/symfony/commit/7570e04589f60861aeb592f284f4d2a7dc7e13e6 "7570e04589f60861aeb592f284f4d2a7dc7e13e6 commit on github"): \[Form\] FormTypeInterface::getAllowedOptionValues()メソッドにより良いバリデートオプションを追加しました
  * [b173884](http://github.com/symfony/symfony/commit/b1738845e9e8da992c4504f19efe1059a5129a81 "b1738845e9e8da992c4504f19efe1059a5129a81 commit on github"): \[AsseticBundle\] Asseticの変更を最新にしました
  * [7f7ea42](http://github.com/symfony/symfony/commit/7f7ea428700b008048fdf97d6ff40d5b3380bbfe "7f7ea428700b008048fdf97d6ff40d5b3380bbfe commit on github"): \[AsseticBundle\] バンドル表記を使用した際に、アセットルートをセットするようにしました
  * [4ae40f1](http://github.com/symfony/symfony/commit/4ae40f1ea4fca1574282abe709517c312159c7f1 "4ae40f1ea4fca1574282abe709517c312159c7f1 commit on github"), [c0dcb7c](http://github.com/symfony/symfony/commit/c0dcb7caade20a75e37cc3fa7271ad9c966d84b3 "c0dcb7caade20a75e37cc3fa7271ad9c966d84b3 commit on github"): \[AsseticBundle\] アセットのターゲットパスに基づいた自動追加フィルターの設定を追加しました
  * [dcb4ef6](http://github.com/symfony/symfony/commit/dcb4ef6e23d9fb3bacbdaca42a685259fcb0a8d6 "dcb4ef6e23d9fb3bacbdaca42a685259fcb0a8d6 commit on github"), [e81b88c](http://github.com/symfony/symfony/commit/e81b88c576842ea75a96db43cc07d7913098ce7d "e81b88c576842ea75a96db43cc07d7913098ce7d commit on github"), [11fa8d8](http://github.com/symfony/symfony/commit/11fa8d8698d15ca8394e5f615e6ac5a0365b5ca8 "11fa8d8698d15ca8394e5f615e6ac5a0365b5ca8 commit on github"): \[HttpFoundation\] Request::__toString()メソッドとHeaderBag::__toString()メソッドを追加しました

