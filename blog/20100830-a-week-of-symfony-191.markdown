A week of symfony #191 (23->29 August 2010)
==========================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/08/29/a-week-of-symfony-191-23-29-august-2010)）

<br />
<br />
<hr />

今週Symfony2には新たに`ControllerInterface`インターフェイスと`BaseController`クラスを追加しました。また、プロファイラーのリファクタリングを行い、一時的にWebデベロップメントツールバー(WDT)を削除しました(後に`WebProfilerBundle`として追加します)。それと、例外管理のリファクタリング、イベントリスナーに優先度を指定するパラメータを追加しました。

(翻訳者追記: `ControllerInterface`と`BaseController`の追加とありますが、さらに修正が入って`Symfony\Component\DependencyInjection`コンポーネントの`ContainerAwareInterface`インターフェイス(DIコンテナの存在を認識する、つまりDIコンテナを指定するためのsetContainer()メソッドを持ったインターフェイス)とそれを実装した`ContainerAware`クラスになっています。)

開発メーリングリスト

- [フォームのCSRFトークンに関する問題](http://groups.google.com/group/symfony-devs/browse_thread/thread/68db5ac12f02eb5d)
- [実際のプロジェクトで基本的なウィジェットを拡張する方法](http://groups.google.com/group/symfony-devs/browse_thread/thread/6f50c26ca917c036)

Development highlights

Symfony 1.X branch:

- [r30773](http://trac.symfony-project.org/changeset/30773) [1.3, 1.4] イベントが正しく処理されない問題を修正

Symfony 2.X branch:

- [1277568](http://github.com/symfony/symfony/commit/12775689973787f282a11bd6f02f8b59cb78ddc8) [HttpFoundation] `Session`を修正
- [0319838](http://github.com/symfony/symfony/commit/0319838cdc6a997bc1b5effde0a87753c75eb0b9) [TwigBundle] flashタグを追加
- [fe78d5f](http://github.com/symfony/symfony/commit/fe78d5f0f0661e454a78478c187edd7633a71750) プロファイラーを無効にする方法を追加
- [9c07e46](http://github.com/symfony/symfony/commit/9c07e46d91b30236d89a98f738b7b7f3e2e5dfd1) [FrameworkBundle] `ControllerInterface`を追加。コントローラーは`ControllerInterface`を実装しなければならない。`BaseController`は各コントローラーのベースとなるクラス。`Controller`クラスにはいくつかのプロキシーメソッドを追加し、DIコンテナーへ配列形式でアクセスできるよう修正
- [789a02d](http://github.com/symfony/symfony/commit/789a02d56d79e32446fa7ea529f8a5d84e02a625) [FrameworkBundle] `SessionHelper::getAttribute()`メソッドを`get()`メソッドに変更
- [ec8500b](http://github.com/symfony/symfony/commit/ec8500bd647aa82ffa39d249d44c0273a0a1294e) [FrameworkBundle] 例外発生画面で以前に使われた例外が確認できるよう修正
- [3c42e0b](http://github.com/symfony/symfony/commit/3c42e0b6ce79e49ba44a0adcb8bc1144027c0ae2) [FrameworkBundle] `ignore_errors`オプションのデフォルト値を現在のデバッグモードに基づいて設定するよう修正
- [b1e7996](http://github.com/symfony/symfony/commit/b1e79963b120e3237a7a82f186ce83a5f568bdcf) [DependencyInjection] エクステンションの読み込みをフリーズ処理中に行うよう修正
- [a432417](http://github.com/symfony/symfony/commit/a432417ab9f901c7915e01d04d16904c4479155f) [DependencyInjection] 存在しないファイルの読み込み時にエラーを無視できる設定を追加(オプション的なサービスファイルの読み込み時などに利用)
- [bf67562](http://github.com/symfony/symfony/commit/bf6756226820e82ae55ae20004d20dd2eb9c79c5) [Templating] PHPレンダラーに`$template`変数を渡した場合の問題を修正
- [69f9d9c](http://github.com/symfony/symfony/commit/69f9d9c6bfc2fbdad11c32773e5bd10058b3c3e1) [DoctrineMongoDBBundle] WDT用のロガーとデータコレクターを追加
- [0867080](http://github.com/symfony/symfony/commit/086708003a8bbe490de29cae48a3b2ca9f590021) [HttpFoundation] `*Bag`クラスに`keys()`メソッドを追加
- [1d7f43e](http://github.com/symfony/symfony/commit/1d7f43eed4eb5c53a1227efc81fb5cd2b049fe72) [Framework] イベントに登録したリスナーが(イベントが処理済みだった場合などで)呼び出されなかった場合
- [82ff790](http://github.com/symfony/symfony/commit/82ff79064acc336ce284a3914070479a0fe346ef) イベントディスパッチャーのリスナーに優先度の指定を追加
- [57db35b](http://github.com/symfony/symfony/commit/57db35b93b98e9f8550cd137d4c39aa71a012687) `ExceptionManager`を`Request`へ依存しないよう修正
- [92f4b92](http://github.com/symfony/symfony/commit/92f4b92cbbbb1e51ee65fd399b83b4a5e17e6ca2) [HttpFoundation] `Session`のシリアライゼーション処理を修正
- [c78528a](http://github.com/symfony/symfony/commit/c78528a91b1a4ed00e1482d0ece76bf1ac6e11f8) [FrameworkBundle] `abbrClass()`と`abbrMethod()`ヘルパーを追加
- [eeb0742](http://github.com/symfony/symfony/commit/eeb0742826509ebd48c0bd9947ee2fedc8fa1c26) [Framework] 呼び出されたイベント/呼び出されていないイベントを取得できるよう修正
- [83a64df](http://github.com/symfony/symfony/commit/83a64df542d6fcdf8547ed97bdd5a510f36960b8) `ContainerAwareInterface`を追加
- [eb66e0d](http://github.com/symfony/symfony/commit/eb66e0dc0053e20e7897515d659e7f393b3399f1) [FrameworkBundle] `ExceptionController`を他のアクションに埋め込めるよう修正
- [72db4c7](http://github.com/symfony/symfony/commit/72db4c734253f87fba7182da221a91a75a73bff7) `Profiler`と`DataCollector`クラスをリファクタリング (WDTは一時的に削除し、後々に`WebProfilerBundle`として追加予定)
- [0208800](http://github.com/symfony/symfony/commit/02088004592d4704141f38257657755bf3a5b9f6) 例外管理のリファクタリング (`ExceptionManager`を削除)

sfDoctrinePlugin:

- [r30774](http://trac.symfony-project.org/changeset/30774): [1.3, 1.4] アドミンジェネレーター内で`Doctrine`クラスからの呼び出し処理を`Doctrine_Core`クラスに修正

[その他多数](http://trac.symfony-project.com/trac/timeline?from=08%2F29%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update)

<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
>
> 世間はRails 3の登場で活気づいていますが、Symfony2もRails 3に負けない柔軟性を誇っています(DIコンテナーなどJava的なアプローチではありますが)。とはいえまだまだ開発中で、コア部分に様々な修正が行われている段階です。よいアイディアは積極的に取り込まれていますし、興味がある方はぜひ提案/コミットしてみてください。[fivestar]
