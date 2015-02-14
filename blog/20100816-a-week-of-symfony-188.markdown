---
layout: default
title: A week of symfony #188 (2->8 August 2010)
---

A week of symfony #188 (2->8 August 2010)
=========================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/08/08/a-week-of-symfony-188-2-8-august-2010)）

<br />
<br />
<hr />

暑い夏にもかかわらず、Symfonyの開発は続けられています。先週はSymfony2において、DoctrineBundleのいくつかのバグが修正され、Symfony2の全体にわたってPHPDocが更新されてシンプルになり、DIコンテナ内でタグ付けできるようにアノテーションの名前が変更されました。


開発メーリングリスト
--------------------

- [Symfony2でブラウザへ徐々に値を出力する方法](http://groups.google.com/group/symfony-devs/browse_thread/thread/105e3295b4ed325d)<br />
  Ajaxで処理すべき、という回答など。
- [Symfony2におけるユーザー認証と権限](http://groups.google.com/group/symfony-devs/browse_thread/thread/4504d3f318f32fcc)<br />
- [Symfony2におけるカスタムエラー処理](http://groups.google.com/group/symfony-devs/browse_thread/thread/b0ca4ce41e6ade7f)<br />

開発ハイライト
--------------

### symfony 1.Xブランチ：

- [r30527](http://trac.symfony-project.org/changeset/30527): [1.3, 1.4] sleepの使用方法を修正
- [r30530](http://trac.symfony-project.org/changeset/30530): [1.3, 1.4] Windowsでプロジェクトを作成し、Linuxで実行する場合のパスを修正
- [r30563](http://trac.symfony-project.org/changeset/30563): [1.3, 1.4] sfWebController::redirectメソッドがHTTPの仕様に準拠していなかったのを修正


### Symfony 2.Xブランチ：

- [86b5538](http://github.com/symfony/symfony/commit/86b5538f010e744d443bcec320eea24e4b5b7096): [DoctrineBundle] XML内の古い未使用のサービスを削除し、PHP内にサービスを定義。
- [88c7427](http://github.com/symfony/symfony/commit/88c742731d3bd3e0fffdc4d1e81fbc53e588043f): [FrameworkBundle] Controller::getMailer()メソッドを削除。(代わりに->container['mailer']を使う)
- [1a9f2ca](http://github.com/symfony/symfony/commit/1a9f2ca755ecdc8f069e586c6e9bd0c4df59415e): APIツールがuseステートメントを認識するので、PHPDocを修正
- [e931825](http://github.com/symfony/symfony/commit/e931825b476d644645ad866602659df20eccf599)、[a113c2b](http://github.com/symfony/symfony/commit/a113c2b3ad8c5fc2a4276e29ea8dba3057f14984): [HttpFoundation] Request::overrideGlobals()を呼び出した場合にHTTPヘッダーを使って$_SERVERを生成
- [8275034](http://github.com/symfony/symfony/commit/8275034f5f6a80fa5415183a723ffa4c00febcd5): [DependencyInjection] クラスのロード順を修正。生成したクラスキャッシュを使ってSymfonyカーネルを起動した場合の'Cannot redeclare class Symfony\Components\Routing\RouterInterface' fatalエラーの原因を修正。
- [84229f0](http://github.com/symfony/symfony/commit/84229f038af88f4cb65bfc22d02fd1f54d77cb1b): [HttpKernel] SQLite3の読み取り専用フラグを削除
- [ee2ff39](http://github.com/symfony/symfony/commit/ee2ff39eaf228b029f8a308a4bb1b3f9383ef2ee): アノテーションの@packageと@subpackageを削除
- [b9199cb](http://github.com/symfony/symfony/commit/b9199cb21c7320bc428e0e32fc660bfc7bd9ba72): [FrameworkBundle] XSDにバリデーションを追加
- [a3fc1be](http://github.com/symfony/symfony/commit/a3fc1be13fa1bded13e33fa5eec12c857deea16c)、[c9001f3](http://github.com/symfony/symfony/commit/c9001f37fcea7c2fb461ed6d3928439fb2e98c67): [DoctrineBundle] デフォルト設定を1回だけ読み込むように更新。DoctrineBundleでconfigファイルをパースするたびにデフォルト設定をロードしていたのを初回のみロードするように修正。この問題により、インポートされたファイルがデフォルト値で上書きされていた。
- [3b1c7e5](http://github.com/symfony/symfony/commit/3b1c7e59f628d998ceab13ce3c024ce053109322): [DoctrineBundle, DoctrineMongoDBBundle] 両方のバンドルが有効化されている場合でもテストが動作するように更新。DoctrineBundleとDoctrineMongoDBBundleの両方を有効化してSymfony2のユニットテストを実行すると、YamlBundle、XmlBundle、AnnotationBundleのクラス再定義エラーが発生していた。これらのテストで使うバンドルを完全修飾名前空間に修正した。
- [51ae607](http://github.com/symfony/symfony/commit/51ae607aeb174eaf90e3a39cbc90007c8850b755): [DoctrineMongoDBBundle] デフォルトのキャッシュサービスをxmlに追加
- [d876ea0](http://github.com/symfony/symfony/commit/d876ea07664e32370889b65c5a8c88f971db7a05)、[eb8b764](http://github.com/symfony/symfony/commit/eb8b7645d4b32f8fad95bdc046ddc7740c770ea3): [HttpKernel] sleep()の誤った使用方法を修正
- [82e440c](http://github.com/symfony/symfony/commit/82e440c1811b0ac23d6e404a67f8206ec5d4b8df): [DoctrineMongoDBBundle] DI拡張に"default_database"属性を追加
- [8f21e5d](http://github.com/symfony/symfony/commit/8f21e5d918eb3e1fd3b3a18cb4f50340e52a9692): ドキュメントマネージャごとにdefault_databaseを設定できるように修正
- [355ed9b](http://github.com/symfony/symfony/commit/355ed9b5f9a24f34e0b84f25f5a51a7c71581065): DIC内でタグ付けできるようにアノテーションの名前を変更


### sfPropelPlugin：

- [r30526](http://trac.symfony-project.org/changeset/30526): [1.3, 1.4] AdminGeneratorの翻訳ファイルにロシア語とウクライナ語を追加
- [r30529](http://trac.symfony-project.org/changeset/30529): [1.3, 1.4] メッセージがGLOBカラムyに保存されている場合のSwift_PropelSpoolを修正


[その他多数](http://trac.symfony-project.com/trac/timeline?from=08%2F08%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update)

<hr />
<br />

