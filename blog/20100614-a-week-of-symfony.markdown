A week of symfony #180 (7->13 June 2010)
========================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/06/13/a-week-of-symfony-180-7-13-june-2010)）

<br />
<br />
<hr />

先週は、Symfony 2のWebBundle（init:applicationコマンドの追加）、TwigBundle（Twigの最新版との同期）、PropelBundleなどのバンドル開発が集中的に行われました。
また、symfonyコミュニティでは[Symfony 2オンラインカンファレンス](http://www.symfony-live.com/)用の[カンファレンスハブ](http://www.symfony-project.org/blog/2010/06/09/state-of-symfony-2-conference-hubs)の準備が進められました。


開発メーリングリスト
--------------------

- [Symfony 2 - helpers and project container](http://groups.google.com/group/symfony-devs/browse_thread/thread/2f95e5c1513eb2d1)<br />
  Symfony 2のヘルパーとプロジェクトコンテナについて


開発ハイライト
--------------

### Symfony 2.Xブランチ：

- [a79ad89](http://github.com/symfony/symfony/commit/a79ad894f920e2f78d1f09f25901e91a74430686): 外部ライブラリに依存するテストの実行方法を追加
- [b057ef6](http://github.com/symfony/symfony/commit/b057ef613fab4bc06d77bd45d77ed16ba35f7fc8)、[a7e5f81](http://github.com/symfony/symfony/commit/a7e5f81803c6d36aa9b81b25519b01f93492c3d8): [DependencyInjection] エクステンションが既存のコンフィギュレーションを継承したりマージしたりできるようにエクステンションのメカニズムを変更
- [294e54f](http://github.com/symfony/symfony/commit/294e54fb21d1fed671a1abb07cccc044e8dc45ee): [TwigBundle] サービス名を修正
- [409a742](http://github.com/symfony/symfony/commit/409a7425036d200716bcdf286baea157f38cb891): [ZendBundle] ZE2を使うようにZend Frameworkバンドルを更新
- [28f4bcc](http://github.com/symfony/symfony/commit/28f4bccb33ba64ca732cdc3b71049435b62e3053): cultureをlocaleに変更
- [b86880d](http://github.com/symfony/symfony/commit/b86880da5e946fdd70ccc631e3cabdbf09f06e7e): [TwigBundle] Twigの最新版に関連するバンドルの更新
- [6d5f186](http://github.com/symfony/symfony/commit/6d5f186728117a3e7845df7c49b59a65e7a4114d): [DoctrineBundle] DoctrineExtensionからarray_reverseを削除。これによりsrc/Application/SomeBundle/Entities/Entity.phpがsrc/Bundle/SomeBundle/Entities/Entity.phpより優先されるように。
- [50610bc](http://github.com/symfony/symfony/commit/50610bc92b526499a49ae3c6539c89c28ceda4e8): [SwiftmailerBundle] swiftmailerのパスをインクルードパスに追加しなくても良いように
- [a78f886](http://github.com/symfony/symfony/commit/a78f88687c0a008518c8a6c471df3ecf6523de98): [WebBundle] デフォルトスケルトンの修正
- [e3c2e40](http://github.com/symfony/symfony/commit/e3c2e40c06303eb33b43a77cff019cde0df3051d): [Foundation] Kernel::__clone()を追加
- [defa307](http://github.com/symfony/symfony/commit/defa307d40b9f350f29c8c82f1acc2b182b727cd): [WebBundle] 機能テストを記述する際に定型的なコードを書かなくてすむよう特殊な処理を追加
- [77d3f92](http://github.com/symfony/symfony/commit/77d3f924df2f27972922d2b27c008d91c747b7e3): 機能テストで環境とデバッグフラグを簡単に変更する方法の追加
- [075edbc](http://github.com/symfony/symfony/commit/075edbc3b79230c69cac86292f88cd4480056ab3): [TwigBundle] 最新バージョンのTwigを利用するようにバンドルを更新
- [ca00e20](http://github.com/symfony/symfony/commit/ca00e2074838ec08eb84e12a10f97be6f47bc8e7): [PropelBundle] Propelで名前空間がサポートされたため、カスタムオートローダーの利用を削除
- [3a35c32](http://github.com/symfony/symfony/commit/3a35c327c5d1c33b9f525d71dac60d25fe87f2d0): [PropelBundle] READMEに詳細を追加
- [d3f9431](http://github.com/symfony/symfony/commit/d3f9431757a3b8783810bd2861e304d30b59593e): [PropelBundle] 古いモデルのオートローダーを削除
- [6ec9b99](http://github.com/symfony/symfony/commit/6ec9b9966e541d09df7d87cb7a9a8ae4fe8e591a): XMLとYAMLファイルのコーディング規約に関する修正
- [b48cc5b](http://github.com/symfony/symfony/commit/b48cc5b3115a23e1ce91dab809887faa6a7195fd): [WebBundle] 新規アプリケーションを初期化するコマンドを追加

[その他多数](http://trac.symfony-project.com/trac/timeline?from=06%2F13%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update)


<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
> Symfony 2のオンラインカンファレンスがいよいよ来週にせまりました。
> チケットを5枚買えば、6人以上集まってカンファレンスを視聴できる「カンファレンスハブ」制度について案内がありました。
> 日本国内でカンファレンスハブの設置について名乗りを挙げているところはまだ無いようですが、興味のある方（個人もしくは企業）は一度ユーザー会までご相談ください。（告知等協力いたします）
> [hidenorigoto]


