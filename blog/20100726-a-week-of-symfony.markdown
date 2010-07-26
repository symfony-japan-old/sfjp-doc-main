A week of symfony #186 (19->25 July 2010)
========================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/07/25/a-week-of-symfony-186-19-25-july-2010)）

<br />
<br />
<hr />

この週ではSymfony2ルーティング管理が新しいローダ、メソッド、設定で完全に改装されました。新しいローダにはDI(依存性注入)コンポーネントも追加されました。さらに、Doctrineのいくつかのバグが修正され、国際化コンポーネントが追加されました。


開発メーリングリスト
--------------------

- [Symfony2ドキュメントへの提案](http://groups.google.com/group/symfony-devs/browse_thread/thread/52318e33ec352c3c)<br />
- [セッションのflush](http://groups.google.com/group/symfony-devs/browse_thread/thread/ca0a40ce18bada48)<br />
- [sfTaskの制限がevent listenerから別のタスク呼び出しを難しくしている](http://groups.google.com/group/symfony-devs/browse_thread/thread/b9ecec0bea6b425f)<br />


開発ハイライト
--------------

### Symfony 2.Xブランチ：

- [b828617](http://github.com/symfony/symfony/commit/b82861742041fddcd1edf4df2837d0c54f7980e0): [DoctrineBundle] XML経由の複数の接続を修正
- [1bc973e](http://github.com/symfony/symfony/commit/1bc973e5a91a1afa452a67968a5d280c4779dab5): [DoctrineBundle] 失われたドライバオプション(sqliteに使用されるメモリ、ociに利用される文字セット)をDoctrineによるサポートされるサポート設定オプションに追加
- [7287913](http://github.com/symfony/symfony/commit/7287913bc63ebce64eeab51368e9b2033d377cb9): [DoctrineBundle] doctrine:generate:entityのXMLエクステンションに全てのマッピングタイプが追加されたときの欠陥を修正
- [e33894a](http://github.com/symfony/symfony/commit/e33894a80cd4edae7468ae4619b927b6eff7effc): [DoctrineBundle] doctrine:generate:entityコマンドの no --fields が指定されたときの問題を修正
- [216dc0f](http://github.com/symfony/symfony/commit/216dc0f5bd499574046c627db5a3d1678ae358e4): [DoctrineBundle, DoctrineMongoDBBundle] DIコンテナに構築されるときのプロキシディレクトリが作成されることを確実にした
- [93f2d6e](http://github.com/symfony/symfony/commit/93f2d6eaa64fe1df46f9d99a77e1cd6d4cc4c010): [FrameworkBundle] pdo.xmlを消去
- [e6cbfd7](http://github.com/symfony/symfony/commit/e6cbfd7292f9d94750d00b7f36d0ec4bee685892): [Console] CommandTesterにアプリケーションの必要なしにコマンドクラスのテストを許可
- [14cecd5](http://github.com/symfony/symfony/commit/14cecd5231f69b62e544eb7f20f12ecb68de5e92): [Routing] ローダをリファクタリング: supports() を追加、setResolver() メソッドをLoaderInterfaceに追加、LoaderResolverインターフェイスを追加、ローダベースクラスを追加、DelegatingLoader、ClosureLoader、PhpFileLoaderを追加及びさらなる柔軟性のためにインポート構造をリファクタリング
- [4e3e86c](http://github.com/symfony/symfony/commit/4e3e86c4a70130cbe1e292005eddf49a4fb8d9a0): ルーティング管理をリファクタリング: デフォルトルーティングの無効化が現在は可能に、Kernel::registerRoutes() メソッドを消去、routerエントリーを追加(registerRoutes() を置換)、ルーティング設定自身のrouting.xmlをリファクタリング
- [60c6827](http://github.com/symfony/symfony/commit/60c6827f233a40a9cad618fc56ce5c2c3e2d6e53)[dcaf436](http://github.com/symfony/symfony/commit/dcaf436d9af025161f9cbd6fc423ed397803edbb): [DependencyInjection] ローダをリファクタリング: supports() を追加、setResolver() メソッドをLoaderInterfaceに追加、LoaderResolverインターフェイスを追加、ローダベースクラスを追加、DelegatingLoader、ClosureLoader、PhpFileLoaderを追加及びさらなる柔軟性のためにインポート構造をリファクタリング
- [3f270f5](http://github.com/symfony/symfony/commit/3f270f5faabb309e8fc268cac28937ae68dcdd7b)[ef40118](http://github.com/symfony/symfony/commit/ef401180a73c35c826493f670d8db671ac2ba618): [FrameworkBundle] プレーンPHP内設定のためのスケルトンを追加
- [bfb081f](http://github.com/symfony/symfony/commit/bfb081fd9698822b7a47925860735db44a281ea0): [ZendBundle] Zend\\Translatorコンポーネントを追加


[その他多数](http://trac.symfony-project.com/trac/timeline?from=07%2F25%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update)

<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
> はじめまして。shishiといいます。まだあんまりsymfonyを理解してないのですが、symfonyを面白いと感じたので貢献しつつ学習できればとドキュメント整備に関わり始めました。
>現在Jobeetのチュートリアルをリファクタリング中です。
>どうぞよろしくお願いします。
> [shishi]


