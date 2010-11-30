A week of symfony #204 (22->28 November 2010)
=============================================

Symfony 公式ブログで毎週公開される、Symfony 関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony 本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/11/28/a-week-of-symfony-204-22-28-november-2010)）

<br />
<br />
<hr />

今週のSymfony2の開発は活発でした。Symfony2のコンポーネントに、多数の変更やチューニング、追加が行われました。Twigバンドルやフォーム、DIでパフォーマンスが改善し、OutputEscaperコンポーネントは削除され、新しい命名規則に従うように<a href="https://github.com/symfony/symfony/commit/944d91c1dfc68cf7f769ba7b60cb328fa06b786c">多数ののメソッドの名前が変更されました</a>。Symfony2は週を追うごとに活溌になってきております。そのおかげでPR4バージョンのリリースも折り返し地点に着ており、最初のベータ版も年末までには公開できそうです。
 
開発メーリングリスト
------------------------

  * [Symfony2のビューレイヤー](http://groups.google.com/group/symfony-devs/browse_thread/thread/1de6b80b134837d4)
  * [Symfony2 Preview Release 4](http://groups.google.com/group/symfony-devs/browse_thread/thread/868ed984b24c62ab)
  * [[RFC] Symfony2 メソッド命名規則](http://groups.google.com/group/symfony-devs/browse_thread/thread/2016947ac81466cd/ecf94783488c05ef)
  * [複数のホスト間でのアセット定義](http://groups.google.com/group/symfony-devs/browse_thread/thread/e46e5c8dcd0cf210)
  * [Doctrine2とSymfonyDisconnectedClassMetadataFactoryの改良案](http://groups.google.com/group/symfony-devs/browse_thread/thread/5da0cc27e5b2e939)

symfony 1 開発ハイライト
--------------------------------

[チェンジログ](http://trac.symfony-project.com/trac/timeline?from=28%2F11%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r31471](http://trac.symfony-project.org/changeset/31471 "31471 revision on trac"): \[1.3, 1.4\] session_cache_limiterのデフォルト値を'null'に修正

Symfony2 開発ハイライト
-------------------------------

[チェンジログ](http://github.com/symfony/symfony/commits/master):

  * [1bbdb5e](http://github.com/symfony/symfony/commit/1bbdb5ec071e8e22a003bc296e0158524dbfe1c6 "1bbdb5ec071e8e22a003bc296e0158524dbfe1c6 commit on github"): \[Form, FrameworkBundle, TwigBundle\] PHPとTwigのテンプレートレイヤーをリファクタリング。PHPテンプレートテーマのサポートは廃止しました
  * [6a14846](http://github.com/symfony/symfony/commit/6a148465da8080ee3713e80d5bd042972536cfe6 "6a148465da8080ee3713e80d5bd042972536cfe6 commit on github"): \[Validator, Form\] "*"全一致グループのサポートの削除
  * [940ce9a](http://github.com/symfony/symfony/commit/940ce9aedf6299a83590e7361cd75b60213d71d8 "940ce9aedf6299a83590e7361cd75b60213d71d8 commit on github"): \[Validator\] グループ列がバリデートされたときに"Default"グループはバリデート済みの参照を伝搬させるように修正
  * [46145d8](http://github.com/symfony/symfony/commit/46145d8de7eaeae8d419d44bef79d76ab4603b74 "46145d8de7eaeae8d419d44bef79d76ab4603b74 commit on github"): \[Validator\] オプションが空ではなかったときにだけValid制約が投げられるように例外を修正
  * [a0f9331](http://github.com/symfony/symfony/commit/a0f933163f2a0eff36d0a964c471f645b44fb716 "a0f933163f2a0eff36d0a964c471f645b44fb716 commit on github"), [b3ae62e](http://github.com/symfony/symfony/commit/b3ae62e2c434c3600f4eea7136171f75f67977ed "b3ae62e2c434c3600f4eea7136171f75f67977ed commit on github"), [7a255fe](http://github.com/symfony/symfony/commit/7a255fe39f8985023b335815a02bc8bcf7656343 "7a255fe39f8985023b335815a02bc8bcf7656343 commit on github"), [db3e12b](http://github.com/symfony/symfony/commit/db3e12b122493453fc1f86ae517d61715fea6ca1 "db3e12b122493453fc1f86ae517d61715fea6ca1 commit on github"): Windowsでテストが中断してしまうのを修正
  * [ac0081f](http://github.com/symfony/symfony/commit/ac0081f8b9b7cdc3ed037374a0ce41115a5bf112 "ac0081f8b9b7cdc3ed037374a0ce41115a5bf112 commit on github"): DoctypeをHTML5に切り替え
  * [e204a18](http://github.com/symfony/symfony/commit/e204a1845bbd474c18c3a53ff80499595db1b30f "e204a1845bbd474c18c3a53ff80499595db1b30f commit on github"): \[DoctrineBundle\] vendorのバンドル名前空間を用いてタスクを作成するように修正
  * [d9239d1](http://github.com/symfony/symfony/commit/d9239d1c64b87561ccc58dad44b600aa4734094f "d9239d1c64b87561ccc58dad44b600aa4734094f commit on github"): DoctrineコマンドのgetBundleMetadatas関数を修正
  * [b6923dd](http://github.com/symfony/symfony/commit/b6923dd7b9e37affac0ad51a4702982fb300e932 "b6923dd7b9e37affac0ad51a4702982fb300e932 commit on github"): Cache-Controlのデフォルト値の振る舞いを修正。PHPネイティブのキャッシュリミットをやめてHeaderBagクラスが代わりに直接管理するように修正 (詳細はコミットを参照)
  * [333504a](http://github.com/symfony/symfony/commit/333504a201538651f8680ebfef29103e5669874a "333504a201538651f8680ebfef29103e5669874a commit on github"): \[OutputEscaper\] ある変数がSafeDecoratorによってデコレートされ、そしてシステムの他の部分でデコレーションが発生するところを同じ変数がデコレートされていないときに通過するとき、のアウトプットエスケーピングを修正
  * [681ce7f](http://github.com/symfony/symfony/commit/681ce7f46a3e6ccd815ddcdc0fd369b11c41ed73 "681ce7f46a3e6ccd815ddcdc0fd369b11c41ed73 commit on github"): \[Form\] 子要素だけにエラーが発生したときに、FieldGroup::hasErrors()がtrueを返さなかったのを修正
  * [6176063](http://github.com/symfony/symfony/commit/6176063b30b4b52b45f1000de8ff8fbde6800609 "6176063b30b4b52b45f1000de8ff8fbde6800609 commit on github"): \[TwigBundle\] form.twigテンプレートのエラーブロックで変数の参照を修正
  * [a71cad4](http://github.com/symfony/symfony/commit/a71cad480a563f74f558fc9990e85ee8471d432a "a71cad480a563f74f558fc9990e85ee8471d432a commit on github"): \[Validator\] @validation:GroupSequenceをアノテーションドライバに追加
  * [68cebd6](http://github.com/symfony/symfony/commit/68cebd667aa41ee310383826c7ae83733b7e0a4f "68cebd667aa41ee310383826c7ae83733b7e0a4f commit on github"): \[Validator\] グループ列が常にグループのクラス名を含むように修正。グループ列によって再定義されるまでグループはDefaultを含まないように修正
  * [e0d6aad](http://github.com/symfony/symfony/commit/e0d6aad5f4c3fc39033ed6e64df36f1977d289e5 "e0d6aad5f4c3fc39033ed6e64df36f1977d289e5 commit on github"): \[Form, FrameworkBundle, TwigBundle\] フォームエラーをラッピングするFieldErrorクラスを導入
  * [17c500e](http://github.com/symfony/symfony/commit/17c500e0f0ef5585d3b1f021d11c9b297bafc211 "17c500e0f0ef5585d3b1f021d11c9b297bafc211 commit on github"), [e3551b5](http://github.com/symfony/symfony/commit/e3551b5f87d157887840171f0d5e81f527351cc3 "e3551b5f87d157887840171f0d5e81f527351cc3 commit on github"): \[TwigBundle\] YAMLフィルター/エンコーダーを追加
  * [84cf569](http://github.com/symfony/symfony/commit/84cf5698c53e0eb5247179c6a541366b6ccab515 "84cf5698c53e0eb5247179c6a541366b6ccab515 commit on github"): \[TwigBundle\] Twigの新しい文法を反映するようにincludeタグを修正
  * [a323dd0](http://github.com/symfony/symfony/commit/a323dd0e9365f65e2f938127d5bab8f69b73a4c8 "a323dd0e9365f65e2f938127d5bab8f69b73a4c8 commit on github"): \[TwigBundle\] コードヘルパーからフィルターを追加
  * [cbb22b4](http://github.com/symfony/symfony/commit/cbb22b4ec4e758ece9e72992cdf185131306304a "cbb22b4ec4e758ece9e72992cdf185131306304a commit on github"): \[Templating\] Engine::load()メソッドを追加
  * [67f6889](http://github.com/symfony/symfony/commit/67f6889287a2ed6d41bd86399e1ad27fd565ff23 "67f6889287a2ed6d41bd86399e1ad27fd565ff23 commit on github"): \[TwigBundle\] includeタグの引数としてTwig_Templateインスタンスのサポートを追加
  * [21f088d](http://github.com/symfony/symfony/commit/21f088d86aa2dbd440b3265d85af42828f8fdfcd "21f088d86aa2dbd440b3265d85af42828f8fdfcd commit on github"): \[DependencyInjection\] assertEquals(spl_object_hash())をassertSameに置換
  * [6fa943a](http://github.com/symfony/symfony/commit/6fa943ad5464444801fc8fe581d3a7ce3a5c7525 "6fa943ad5464444801fc8fe581d3a7ce3a5c7525 commit on github"): ExceptionとWebProfilerのテンプレートをTwigに移行
  * [97d4dce](http://github.com/symfony/symfony/commit/97d4dce61466cf2fd5d04b732e90d1756b3bcd0d "97d4dce61466cf2fd5d04b732e90d1756b3bcd0d commit on github"): 追加のウェブプロファイラのテンプレートが設定できるように修正
  * [381347b](http://github.com/symfony/symfony/commit/381347bcfe027603d075c6274e583c90c437da37 "381347bcfe027603d075c6274e583c90c437da37 commit on github"): \[WebProfilerBundle\] データコレクターの読み込みを修正 (ウェブデバッグツールバーを除くウェブプロファイラを有効にした時に常に読み込まれるべき)
  * [a79ed13](http://github.com/symfony/symfony/commit/a79ed13624152ba6004fbb100c4be7e78c5958e4 "a79ed13624152ba6004fbb100c4be7e78c5958e4 commit on github"): \[Routing\] variable_prefixesとvariable_regexのルーティングオプションを削除
  * [f9e830c](http://github.com/symfony/symfony/commit/f9e830caa2b18d70edc4ac8e7e2d0dc57ca75326 "f9e830caa2b18d70edc4ac8e7e2d0dc57ca75326 commit on github"): \[Form\] フックメソッドpreprocessData()をFieldGroupに追加
  * [d95d336](http://github.com/symfony/symfony/commit/d95d33666d4af474558d776145b93c714df15e49 "d95d33666d4af474558d776145b93c714df15e49 commit on github"): \[HttpFoundation\] fixed class Requestクラスでファイルが空だったときにNULLに変換するように修正
  * [f2f0d04](http://github.com/symfony/symfony/commit/f2f0d044c33c29855c32f5ed143ae5f9a3e3ae0a "f2f0d044c33c29855c32f5ed143ae5f9a3e3ae0a commit on github"): \[Form, FrameworkBundle\] CheckboxFieldsのデフォルト値を修正
  * [e0aa3f3](http://github.com/symfony/symfony/commit/e0aa3f30a82fbb8cc586d0959eba7d80834ae606 "e0aa3f30a82fbb8cc586d0959eba7d80834ae606 commit on github"): \[Form\] FileFieldがバリデーションが失敗した場合に一時領域にファイルを保管するように改善
  * [5b056b2](http://github.com/symfony/symfony/commit/5b056b2b9ae5ef816d391819c05f9546f141d4e3 "5b056b2b9ae5ef816d391819c05f9546f141d4e3 commit on github"): バンドル開発者がテンプレートを追加しやすいようにウェブプロファイラテンプレートの定義をリファクタリング
  * [ad68092](http://github.com/symfony/symfony/commit/ad68092291c01ebcff8bec027c41a0863f0390c2 "ad68092291c01ebcff8bec027c41a0863f0390c2 commit on github"): OutputEscaperコンポーネントを削除、Templating Engineクラスにエスケープ機構を追加
  * [60bbb8f](http://github.com/symfony/symfony/commit/60bbb8f38079bffa77a765d663658de853208ebb "60bbb8f38079bffa77a765d663658de853208ebb commit on github"): \[DependencyInjection\] コンパイルされたコンテナの最適化：Containerから__call()メソッドを削除し、ダンプされたContainer内の$shared変数を削除し、PHP Dumperの出力を最適化
  * [944d91c](http://github.com/symfony/symfony/commit/944d91c1dfc68cf7f769ba7b60cb328fa06b786c "944d91c1dfc68cf7f769ba7b60cb328fa06b786c commit on github"): フレームワーク内のより良い一貫性のために幾つかのメソッド名を修正
  * [6ab277e](http://github.com/symfony/symfony/commit/6ab277ee411b096d550e4932b39be13ded56bc0b "6ab277ee411b096d550e4932b39be13ded56bc0b commit on github"): ルーティングのためのLazyLoaderを追加
  * [44b8ee3](http://github.com/symfony/symfony/commit/44b8ee3791a6af2eafb9d12f48ae0049f12615b7 "44b8ee3791a6af2eafb9d12f48ae0049f12615b7 commit on github"): クラスキャッシュに幾つかのクラスを追加
  * [dfe8bb9](http://github.com/symfony/symfony/commit/dfe8bb9fefcabd7876c55aef4b454f3eb52ef110 "dfe8bb9fefcabd7876c55aef4b454f3eb52ef110 commit on github"): bootstrapファイルに幾つかのクラスを追加
  * [1e983a6](http://github.com/symfony/symfony/commit/1e983a6115e0bb3fee2cf591fbeee52c30884609 "1e983a6115e0bb3fee2cf591fbeee52c30884609 commit on github"): 静的なフォームの設定を新しいクラスに移行 (CSRFを有効にするための7つのクラスの読み込みを避けるように修正、ページ内にフォームが無いときにもそうなるように修正)

Documentation
-------------

  * 新規ページ：<a href="http://trac.symfony-project.org/wiki/InstallingSymfonyInASubDirectoryWithCentOSandPlesk">CentOSとPleskでサブディレクトリにSymfonyをインストールする</a>と<a href="http://trac.symfony-project.org/wiki/IRCLogs20101125">IRCログ2010-11-25</a>


> **NOTE**
> 翻訳者コメント<br />
> 今週のA Week of symfonyは、[@uechocoさん](http://twitter.com/uechoco) に翻訳していただきました。また、[@doublemarketさん](http://twitter.com/doublemarket) にも今後翻訳を手伝って頂けることになりました！
> 翻訳の基礎知識や Git の使い方はこちらから教えますので、少しでもやってみたいと思っている方は、是非 [@hidenorigoto](http://twitter.com/hidenorigoto) までお声がけ下さい！
> [hidenorigoto]

