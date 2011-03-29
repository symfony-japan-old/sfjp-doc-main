A week of symfony #219 (7->13 March 2011)
=========================================

This week, the echoes of the last [Symfony Live](http://www.symfony-live.com/) conference still resonated in the symfony community. Meanwhile, Symfony2 switched most of its methods and properties from protected to private, a decision made to ease its maintenance that generated a [lengthy and heated discussion](https://groups.google.com/forum/#!topic/symfony-devs/WKDQFWIsE8s) on the mailing list. Lastly, in [the last weekly IRC meeting](http://trac.symfony-project.org/wiki/IRCLogs20110310) core developers decided that "there won't be any other big change before Symfony 2.0 version, no matter what".

今週は、最後の [Symfony Live](http://www.symfony-live.com/) カンファレンスの余韻が symfony コミュニティに漂っていました。一方で、 Symfony2 は多くのメソッドとプロパティーを protected から private に変更し、メーリングリストでの [長く熱い議論](https://groups.google.com/forum/#!topic/symfony-devs/WKDQFWIsE8s) が生み出した、メンテナンスを簡単にするための決断がなされました。最後に、 [先週の IRC ミーティング](http://trac.symfony-project.org/wiki/IRCLogs20110310) ではコア開発者が、「 Symfony 2.0 バージョンまで、大きな変更は行わない。何があってもだ。」という決断をしました。
 
開発メーリングリスト
--------------------

  * [Symfony Standard Edition - Framework Extra?](https://groups.google.com/forum/#!topic/symfony-devs/-sHn_4E739w)
  * [Symfony2 の現時点でのロードマップ](https://groups.google.com/forum/#!topic/symfony-devs/vQRm6jZ3IwI)
  * [\[Symfony2\] AdminBundle](https://groups.google.com/forum/#!topic/symfony-devs/DenokIKxKmM)
  * [\[Symfony2\] なぜ parameters.ini を？](https://groups.google.com/forum/#!topic/symfony-devs/CervMfwHeVk)
  * [Doctrine*Bundle 設定内の短縮記法を削除](https://groups.google.com/forum/#!topic/symfony-devs/yEuuTtulp7o)
  * [アノテーションとカスタムバリデーション](https://groups.google.com/forum/#!topic/symfony-devs/gP0OcIDlKbE)
  * [\[Symfony2\] フォーマットにとらわれないフォームの取り扱い](https://groups.google.com/forum/#!topic/symfony-devs/Y8V4ytzMg5M)
  * [プライベートなメソッドとプロパティ](https://groups.google.com/forum/#!topic/symfony-devs/WKDQFWIsE8s)
  * [\[Symfony2\] Configuration クラスの改善](https://groups.google.com/forum/#!topic/symfony-devs/ck6XYH0w3Yw)

Symfony2 開発ハイライト
-----------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [b80f307](http://github.com/symfony/symfony/commit/b80f307efd1f86be7c756d67304d94bf303d1b0b "b80f307efd1f86be7c756d67304d94bf303d1b0b commit on github"): \[HttpKernel\] parse_url が URI では動作しないため、URL の URI への変換を破棄
  * [bf18183](http://github.com/symfony/symfony/commit/bf18183adfe84a8dd69b356b4f41403e126baea3 "bf18183adfe84a8dd69b356b4f41403e126baea3 commit on github"): \[FrameworkBundle\] 例外ページにおいてデフォルトでログを隠さないように変更
  * [4f15840](http://github.com/symfony/symfony/commit/4f15840e4b276f533ba9cf47bf58ef84421ca6ad "4f15840e4b276f533ba9cf47bf58ef84421ca6ad commit on github"), [ed09566](http://github.com/symfony/symfony/commit/ed09566a47ca078e9a1354728d962569c9bd9f1a "ed09566a47ca078e9a1354728d962569c9bd9f1a commit on github"): \[webProfilerBundle\] 'token not found' ページを新しいデザインにアップデート
  * [69ad4e4](http://github.com/symfony/symfony/commit/69ad4e4f77fc2d8d382bb14196968e6f4b6e631d "69ad4e4f77fc2d8d382bb14196968e6f4b6e631d commit on github"): \[FrameworkBundle\] 間違った設定の解決を助けるよう例外を追加し、いくつかの不足していたテストを追加
  * [d171eaf](http://github.com/symfony/symfony/commit/d171eaf8019035ca31068335cdfcb7ae8a678ae8 "d171eaf8019035ca31068335cdfcb7ae8a678ae8 commit on github"), [62341e5](http://github.com/symfony/symfony/commit/62341e5ad6d993e5ff59a707d940dde3f571c24d "62341e5ad6d993e5ff59a707d940dde3f571c24d commit on github"): \[WebProfilerBundle\] エラーの数と一緒にログのエントリ数を表示 (切り戻し)
  * [de6c353](http://github.com/symfony/symfony/commit/de6c353b40176937209580c13c1f960187e8b1e6 "de6c353b40176937209580c13c1f960187e8b1e6 commit on github"): \[DependencyInjection\] 多くの一時的で使用されない ContainerBuilder オブジェクトがあるため、コンパイラの制約を再度緩和
  * [94c4459](http://github.com/symfony/symfony/commit/94c445957c6ba3a1f28901fc1d9dc367c4f1688d "94c445957c6ba3a1f28901fc1d9dc367c4f1688d commit on github"): \[Yaml\] ほとんどの protected なメソッドやプロパティを private に変更
  * [75b29ff](http://github.com/symfony/symfony/commit/75b29ffdfed36d1713c1ae2a38619580648445e2 "75b29ffdfed36d1713c1ae2a38619580648445e2 commit on github"): \[Translation\] ほとんどの protected なメソッドやプロパティを private に変更
  * [c9b965d](http://github.com/symfony/symfony/commit/c9b965dbeec86be6cb2713185b3389c04dbd0444 "c9b965dbeec86be6cb2713185b3389c04dbd0444 commit on github"): \[Finder\] ほとんどの protected なメソッドやプロパティを private に変更
  * [32d2ec7](http://github.com/symfony/symfony/commit/32d2ec7571f520ecb220d8cedfb2f1a98534868b "32d2ec7571f520ecb220d8cedfb2f1a98534868b commit on github"): \[ClassLoader\] ほとんどの protected なメソッドやプロパティを private に変更
  * [95a2f17](http://github.com/symfony/symfony/commit/95a2f17e9650e1cdbeb0138155acbcd136fb174d "95a2f17e9650e1cdbeb0138155acbcd136fb174d commit on github"): \[DoctrineMongoDBBundle\] いくつかの getParameter() 呼び出しを %wildcard% 文法のパラメータを代わりに使うよう書き換え (これが最適解)
  * [a135004](http://github.com/symfony/symfony/commit/a13500459f0e044be09308740bac749f8abcfebf "a13500459f0e044be09308740bac749f8abcfebf commit on github"): \[DoctrineMongoDBBundle\] DoctrineMongoDBExtension の新しい Configuration クラスの新規使用
  * [42a0b22](http://github.com/symfony/symfony/commit/42a0b22f0eb8b90a3ab3089b1fa0b8b81cc7becf "42a0b22f0eb8b90a3ab3089b1fa0b8b81cc7becf commit on github"): \[DoctrineMongoDBBundle\] XML の 余計な 'connections' と 'document_managers' ラッパーを削除。一貫性がなかったので無用の難しさを正常化
  * [bdd2336](http://github.com/symfony/symfony/commit/bdd23369e2b49e62704139f6e9457e71c0984bb5 "bdd23369e2b49e62704139f6e9457e71c0984bb5 commit on github"): \[DoctrineMongoDBBundle\] doctrine.odm.mongodb.metadata_cache_driver パラメータを削除
  * [9179168](http://github.com/symfony/symfony/commit/9179168e0d82594c6187b1ceb960d42f1628d228 "9179168e0d82594c6187b1ceb960d42f1628d228 commit on github"): \[DoctrineMongoDBBundle\] エクステンションのメソッドをより正しい名前である overrideParameters() に改名
  * [9ca8f17](http://github.com/symfony/symfony/commit/9ca8f171f791e7e69678b9bbbda4f8431ceca768 "9ca8f171f791e7e69678b9bbbda4f8431ceca768 commit on github"): \[DoctrineMongoDBBundle\] 1度も使用されなかった default_connection DI パラメータを削除
  * [1e492e2](http://github.com/symfony/symfony/commit/1e492e231c9ca6a66863e47a663762624ea8c763 "1e492e231c9ca6a66863e47a663762624ea8c763 commit on github"): \[DoctrineMongoDBBundle\] Extension での document_managers のロードのされ方をリファクタリングし、必要のない2つの DIC パラメータを削除
  * [0fe6f13](http://github.com/symfony/symfony/commit/0fe6f13be829877b67f1c8d48ebeda34f76ac119 "0fe6f13be829877b67f1c8d48ebeda34f76ac119 commit on github"): \[DoctrineMongoDBBundle\] YAML の完全な設定の例を追加
  * [c9ab593](http://github.com/symfony/symfony/commit/c9ab59399c6a8331edca2fcb0cfddb703525eb8b "c9ab59399c6a8331edca2fcb0cfddb703525eb8b commit on github"): \[WebProfilerBundle\] クエリーにトークンが常に含まれるよう変更
  * [f49a30c](http://github.com/symfony/symfony/commit/f49a30c36673d981af7396f9be1fe0b369f760c5 "f49a30c36673d981af7396f9be1fe0b369f760c5 commit on github"): \[WebProfilerBundle\] 結果が空のクエリーの扱いを改善
  * [652bca1](http://github.com/symfony/symfony/commit/652bca131da6d3e89966410ecfced8aaf8af5d65 "652bca131da6d3e89966410ecfced8aaf8af5d65 commit on github"), [477109f](http://github.com/symfony/symfony/commit/477109f1e849500eac8e073ec56c4903c768201e "477109f1e849500eac8e073ec56c4903c768201e commit on github"): \[DoctrineBundle\] DoctrineBundle に Configuration クラスを追加し、エクステンションがそれを使用するようリファクタリング
  * [0d0f053](http://github.com/symfony/symfony/commit/0d0f05368256058c9c2f66e4d9b2df45fdd70129 "0d0f05368256058c9c2f66e4d9b2df45fdd70129 commit on github"): \[DoctrineBundle\] XSD スキーマのアップデート
  * [527749c](http://github.com/symfony/symfony/commit/527749ca3fd3f2c8ff42ec69b7bea61b66adcb5e "527749ca3fd3f2c8ff42ec69b7bea61b66adcb5e commit on github"): ORMを使用する際には最低1つのエンティティマネージャを、DBMLを使用する際には最低1つのコネクションを保持するのを必須にするよう変更
  * [e522424](http://github.com/symfony/symfony/commit/e52242496776a31c1601b3b4443ba2e68a1e3c12 "e52242496776a31c1601b3b4443ba2e68a1e3c12 commit on github"): \[DoctrineBundle\] デフォルトのロギングパラメータを kernel.debug に変更し、コンテナユニットテストを修正
  * [d698baf](http://github.com/symfony/symfony/commit/d698baf06be26d92ea12fec944e1b2c7a22a9b45 "d698baf06be26d92ea12fec944e1b2c7a22a9b45 commit on github"): \[FrameworkBundle\] 毎回全てのリスナーインスタンスを生成してしまわないよう、デバッグイベントのディスパッチャを最適化
  * [88cfc4c](http://github.com/symfony/symfony/commit/88cfc4c0114b4ec7f371467cc2e3017f43d51f3a "88cfc4c0114b4ec7f371467cc2e3017f43d51f3a commit on github"): \[Form\] enctype 属性がない場合のために例外を追加
  * [17ef911](http://github.com/symfony/symfony/commit/17ef911f19116f0d06630797baf2f691746736be "17ef911f19116f0d06630797baf2f691746736be commit on github"): \[Routing\] normalizeUrl() メソッドを削除し、より正確に表すよう URL を pathinfo に変更
  * [dded195](http://github.com/symfony/symfony/commit/dded1955e47c37a8f394407375e99bbda48fed4c "dded1955e47c37a8f394407375e99bbda48fed4c commit on github"): \[Routing\] URL セグメント内の / の問題を修正
  * [1d5538f](http://github.com/symfony/symfony/commit/1d5538fc6011c53f5fd905be55866fbf5c21097a "1d5538fc6011c53f5fd905be55866fbf5c21097a commit on github"): AccountInterface を UserInterface に、SecurityContext::vote() を SecurityContext::isGranted() に変更
  * [e3e60f1](http://github.com/symfony/symfony/commit/e3e60f1a685049af7df811335eaf478a8eeb26e8 "e3e60f1a685049af7df811335eaf478a8eeb26e8 commit on github"): \[DoctrineMongoDBBundle\] 設定内の短縮記法を削除
  * [ec46c6e](http://github.com/symfony/symfony/commit/ec46c6e6c57a5c22e7a69f1653d7bbd4449e0eb2 "ec46c6e6c57a5c22e7a69f1653d7bbd4449e0eb2 commit on github"), [51106a8](http://github.com/symfony/symfony/commit/51106a8540539a701c999ad88c0d143801496174 "51106a8540539a701c999ad88c0d143801496174 commit on github"): \[DoctrineMongoDBBundle\] プロファイラ内のクエリーを MongoDB の JavaScript シェルコードに似せるよう変更
  * [4dd45d3](http://github.com/symfony/symfony/commit/4dd45d3b4a67a53f75750582461bbe3bdfb9924e "4dd45d3b4a67a53f75750582461bbe3bdfb9924e commit on github"): DoctrineBundle 内の短縮記法を削除
  * [3d97638](http://github.com/symfony/symfony/commit/3d976388130e359750ccbe8a88819d8df0278784 "3d976388130e359750ccbe8a88819d8df0278784 commit on github"): \[Security\] remember-me コードをリファクタリング
  * [d8022e3](http://github.com/symfony/symfony/commit/d8022e34eba66c7bc15bf25fcc5ff783452004f3 "d8022e34eba66c7bc15bf25fcc5ff783452004f3 commit on github"): \[Security\] core.security イベントを削除
  * [c2e9dd2](http://github.com/symfony/symfony/commit/c2e9dd27b2e485803a62c1a96095a9f84ed7ebb6 "c2e9dd27b2e485803a62c1a96095a9f84ed7ebb6 commit on github"): \[Console\] エラー発生時の概要を修正
  * [b940cc6](http://github.com/symfony/symfony/commit/b940cc6f40fab9cf2c5fd529a3ef97edc33b0509 "b940cc6f40fab9cf2c5fd529a3ef97edc33b0509 commit on github"): Console コンポーネント内の多くの protected を private に変更
  * [f321fad](http://github.com/symfony/symfony/commit/f321fadad69d7f8fd0a41ed6e99130250cdc6778 "f321fadad69d7f8fd0a41ed6e99130250cdc6778 commit on github"): \[DependencyInjection\] 多くの protected を private に変更
  * [c8c5720](http://github.com/symfony/symfony/commit/c8c5720fa1b238262dc038d140951bd6ef4c8836 "c8c5720fa1b238262dc038d140951bd6ef4c8836 commit on github"): \[DomCrawler\] protected から private に変更
  * [bc6ffee](http://github.com/symfony/symfony/commit/bc6ffeef83990af58c49b0758ff08bf14d4000b2 "bc6ffeef83990af58c49b0758ff08bf14d4000b2 commit on github"): \[HttpFoundation\] フラッシュの管理を修正
  * [8421f95](http://github.com/symfony/symfony/commit/8421f95476dd08bcc9d635395e8ed6f5fe4f722d "8421f95476dd08bcc9d635395e8ed6f5fe4f722d commit on github"), [48c222d](http://github.com/symfony/symfony/commit/48c222dd021aed854d85ffca24314c20c25f7e7f "48c222dd021aed854d85ffca24314c20c25f7e7f commit on github"), [92acd46](http://github.com/symfony/symfony/commit/92acd46edeb658ce74d4d6b4524eeba0b97a1022 "92acd46edeb658ce74d4d6b4524eeba0b97a1022 commit on github"), [e0b46fe](http://github.com/symfony/symfony/commit/e0b46fea73a4ee293fc005647011b6a867c29831 "e0b46fea73a4ee293fc005647011b6a867c29831 commit on github"): \[WebProfilerBundle\] もう一つのリクエストのために現在のフラッシュを保持するよう WDT を修正
  * [757e4ea](http://github.com/symfony/symfony/commit/757e4ea4d6eb3147e6729e4b22af1913455d449d "757e4ea4d6eb3147e6729e4b22af1913455d449d commit on github"): \[ClassLoader\] 継承からキャッシュレイヤーを作成できるよう protected な findFile() メソッドを作成
  * [441a154](http://github.com/symfony/symfony/commit/441a15420333de9c8d8338511214f819949b5311 "441a15420333de9c8d8338511214f819949b5311 commit on github"): \[ClassLoader\] APC クラスローダーを追加
  * [7b3fbb4](http://github.com/symfony/symfony/commit/7b3fbb46c2911a58a7b9e96847724e9e56ecc270 "7b3fbb46c2911a58a7b9e96847724e9e56ecc270 commit on github"): \[DoctrineMongoDBBundle\] ロギングを無効にできるよう変更
  * [a809453](http://github.com/symfony/symfony/commit/a809453416130078122401ff3cba6378a163cdb1 "a809453416130078122401ff3cba6378a163cdb1 commit on github"): \[Console\] スタイルプレースホルダーにカスタム正規表現を定義する機能を追加
  * [70867f0](http://github.com/symfony/symfony/commit/70867f06e97ec521ac83b030e59ba770f221ce04 "70867f06e97ec521ac83b030e59ba770f221ce04 commit on github"): \[Security\] デバッグのために __toString メソッドを再度追加
  * [411a382](http://github.com/symfony/symfony/commit/411a382d801a4b4118f4855effd5c0105019e0d2 "411a382d801a4b4118f4855effd5c0105019e0d2 commit on github"): \[Serializer\] 1文字のタグのサポートについて XmlEncoder を修正
  * [d9ffa42](http://github.com/symfony/symfony/commit/d9ffa420b4a12c5d38dc785735c3b79ec2a6832a "d9ffa420b4a12c5d38dc785735c3b79ec2a6832a commit on github"), [823d699](http://github.com/symfony/symfony/commit/823d6991948267a5c6b73737eb1ea5da2768d006 "823d6991948267a5c6b73737eb1ea5da2768d006 commit on github"), [974f64c](http://github.com/symfony/symfony/commit/974f64cb7275bf3f01408c6eb4ec82b3f056a2a6 "974f64cb7275bf3f01408c6eb4ec82b3f056a2a6 commit on github"), [0f255aa](http://github.com/symfony/symfony/commit/0f255aa5ee53ab752bccbb79f2401c9f8512c75f "0f255aa5ee53ab752bccbb79f2401c9f8512c75f commit on github"): \[FrameworkBundle\] バリデータのフランス語翻訳を追加
  * [87cc306](http://github.com/symfony/symfony/commit/87cc306d986f0d502fbb15b804520b59ac568972 "87cc306d986f0d502fbb15b804520b59ac568972 commit on github"): \[FrameworkBundle\] バリデータのスロバニア語翻訳を追加

ドキュメンテーション
-------------

  * [IRC Logs 2011-03-10](http://trac.symfony-project.org/wiki/IRCLogs20110310) ページ

