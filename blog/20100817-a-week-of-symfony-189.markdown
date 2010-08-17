A week of symfony #189 (9->15 August 2010)
==========================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/08/15/a-week-of-symfony-189-9-15-august-2010)）

<br />
<br />
<hr />

先週のSymfony2の開発はさらに加速し、コントローラーリゾルバーのリファクタリング、ブートストラップファイルの更新、バンドルのインターフェイスの修正、およびアプリケーションのデフォルト構成の更新が行われました。


開発メーリングリスト
--------------------

- [DI - YAMLで$を使ってエイリアスを定義する機能の追加](http://groups.google.es/group/symfony-devs/browse_thread/thread/c5b5168b1bdf20eb)<br />
- [Doctrine.ORMプロキシ](http://groups.google.es/group/symfony-devs/browse_thread/thread/d7b260b96b95510b)<br />
- [symfony 1.4のタスクでモデルのカスケードが失敗する](http://groups.google.es/group/symfony-devs/browse_thread/thread/84ac8690de3437ee)<br />

開発ハイライト
--------------

### Symfony 2.Xブランチ：

- [fd70575](http://github.com/symfony/symfony/commit/fd705756d4162fbad37119a7e99ece35fb734263): [Framework] debugがtrueの場合、ブートストラップファイルを無効に
- [6a572e0](http://github.com/symfony/symfony/commit/6a572e0f34e56e3bdc9672e4fd46d834553bf123): [Framework] カーネルにDIC用のClosureLoaderを追加
- [248e501](http://github.com/symfony/symfony/commit/248e501df5f6e47cb25645dc39f9f19b55fc548f): [Routing] Route::setDefault()を追加
- [2f84c28](http://github.com/symfony/symfony/commit/2f84c280d0dd924a91439fcaa45d674cf80dd6bc): [Framework] Kernel::isClassInActiveBundle()を追加
- [485400d](http://github.com/symfony/symfony/commit/485400dd516493ba582bf4228d1c95c19fc6fcaf): コントローラーリゾルバーのリファクタリング(ルーティングを多少最適化)
- [9452437](http://github.com/symfony/symfony/commit/9452437c511f698b99ba63642558917c8372a7ad): [HttpKernel] 一貫性のために、すべてのcore.*イベントでrequest_typeパラメーターを引数にとるように修正
- [2a8a9cc](http://github.com/symfony/symfony/commit/2a8a9cc0a397c5332cbb265bdd39de1034a5b577): KernelBundleのロジックをKernelExtensionへ移動させ、test.xmlをエラーハンドラーに依存しないように修正。kernel.configのerror_handler_levelパラメーターをerror_handlerに名前変更。
- [c043c46](http://github.com/symfony/symfony/commit/c043c4611602dd633946d7cd8031499b33f06a98): [FrameworkBundle] アクションヘルパーを修正し、レゾルバーで短い表記を可能に
- [ac8e1e2](http://github.com/symfony/symfony/commit/ac8e1e29e972b39a50f36a1fa08e0d5e45754c84)、[c139fd6](http://github.com/symfony/symfony/commit/c139fd64d1375c6290750bae378ff525aedbdfee): ブートストラップファイルを更新
- [0f30e53](http://github.com/symfony/symfony/commit/0f30e539b1d786f2d85cc99959f0cc52b8301a7b): [DoctrineBundle] DoctrineExtensionコンストラクタを削除
- [f6c8626](http://github.com/symfony/symfony/commit/f6c862667f5464dc2e953be62860471ac1235d98): [DoctrineMongoDBBundle] DoctrineMongoDBExtensionコンストラクタを削除
- [53c4403](http://github.com/symfony/symfony/commit/53c44039920810151a71bad88793caff4c03010b): [FrameworkBundle] WebExtensionコンストラクタを削除
- [9e82497](http://github.com/symfony/symfony/commit/9e82497d5b492a310c92e14df2bba52c9163727f): BundleInterface::buildContainer()メソッドを削除 (エクステンションは自動的に登録されるようになった。また、規約に従っていない場合はgetExtensions()をオーバーライドする)
- [c87dd77](http://github.com/symfony/symfony/commit/c87dd7780f91281df05f8a584a5fe7f051135049): バンドルのインターフェイスを修正
- [0e36f04](http://github.com/symfony/symfony/commit/0e36f043effaddffde322d58fe16355f9f379817): [Framework] stripComments()メソッドを更新
- [7b65956](http://github.com/symfony/symfony/commit/7b659563430aedf98c797900e82a382f81f4a1ea)、[b64e66d](http://github.com/symfony/symfony/commit/b64e66dde8cff6a49db8c1d5cf4459d3167f2007)、[fca137f](http://github.com/symfony/symfony/commit/fca137fc4700f3019909293c5a044d3c3f0b939d): クラスのコンパイル処理をより高度に設定可能に
- [875366f](http://github.com/symfony/symfony/commit/875366f58476ffc20f875ae5eb82981c4fb178dd): スケルトンのデフォルト設定を更新
- [dbc5249](http://github.com/symfony/symfony/commit/dbc5249f8818a78b6e44245a6be17f1060b24422): .xmlがハードコードされている問題を修正し、ファイル拡張子を適切に扱うようにyamlをymlに変換するように
- [ef0347c](http://github.com/symfony/symfony/commit/ef0347c1b98bbbda7e49a637f3b1dde9e46dbee5): HttpKernelのリクエストの種別を単純化
- [f61bb19](http://github.com/symfony/symfony/commit/f61bb195486bb90f2a2e519729282c8b5f0c9419): Response::setRedirect()を追加
- [75ea0b8](http://github.com/symfony/symfony/commit/75ea0b83957c8e03d02e568ac976cf7e95ec3e11): Engine::renderResponse()を追加
- [38edd2a](http://github.com/symfony/symfony/commit/38edd2aafaa240e7aaa4ef23414b90cfded33f5a): ControllerResolver::forward()を追加
- [880f37c](http://github.com/symfony/symfony/commit/880f37c4eefc5a6c2a1d933cc5fc673ebd5dd591): ControllerがArrayAccessインターフェイスを実装するように変更、getRequest()メソッドを削除


[その他多数](http://trac.symfony-project.com/trac/timeline?from=08%2F15%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update)

<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
> そろそろSymfony2のプレビューリリース3が公開されそうです（ソース：[fabien氏のMLへの投稿](http://groups.google.com/group/symfony-users/browse_thread/thread/0ae3148626f1269d/17aad5f58eca36e2?show_docid=17aad5f58eca36e2&pli=1)）
> [Symfony2ベースのCMFを作るプロジェクト](http://cmf.symfony-project.org/)なども動きだし、徐々に実用段階へ進んできているようです。
> Symfony2を使ってみたレポートなどをブログに書かれた方は、是非URLをユーザー会までお知らせください。（ユーザー会のMLやtwitterなどでシェアさせていただきます）
> [hidenorigoto]


