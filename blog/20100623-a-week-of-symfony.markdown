A week of symfony #181 (14->20 June 2010)
=========================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/06/20/a-week-of-symfony-181-14-20-june-2010)）

<br />
<br />
<hr />

先週は、Symfony 2のコンポーネントのうちProfilerバンドルが活発に更新されました。
一方で、[State of Symfony 2 online conference](http://www.symfony-live.com/)で発表される予定のSymfony 2の魅力的な機能について、多くの開発者が関心を寄せています。
[カンファレンスへの登録](http://www.symfony-live.com/registration/choice)や、[カンファレンスハブの開催](http://www.symfony-project.org/blog/2010/06/09/state-of-symfony-2-conference-hubs)についてもお忘れ無く。



開発メーリングリスト
--------------------

- [symfony 1 git repo mirror](http://groups.google.com/group/symfony-devs/browse_thread/thread/0184e59e051c4bc6)<br />
  symfony 1.4のgitリポジトリについて
- [add support for HTTP OPTIONS](http://groups.google.com/group/symfony-devs/browse_thread/thread/4fb298db8bd6024d)<br />
  Symfony 2でHTTP OPTIONSリクエストを処理したい
- [service method calls dereference](http://groups.google.com/group/symfony-devs/browse_thread/thread/0923d7e0d7939649)<br />
  Symfony 2のDIで、サービスメソッド呼び出しの参照解決


開発ハイライト
--------------

### symfony 1.Xブランチ：

- [r29818](http://trac.symfony-project.org/changeset/29818): [1.3, 1.4] PHP 5.2でのsimple xmlのエスケープ処理を修正


### Symfony 2.Xブランチ：

- [16f7d3a](http://github.com/symfony/symfony/commit/16f7d3a0406c5107077f38c3049c3d49f9f533f5): [PropelBundle] DBALが設定されていない場合のPropelコンフィギュレーションの修正
- [b174004](http://github.com/symfony/symfony/commit/b17400454bb969c6a04edea1e88cb247d270a7f6): [DomCrawler] APIを分かりやすくするためにFormクラスへのショートカットメソッドをいくつか追加
- [14cb6dd](http://github.com/symfony/symfony/commit/14cb6dd77ce74f2cfbafd8beade01eec4cebe19b): スケルトンのデフォルトで、テストコンフィギュレーションをdevから継承するように
- [25c4ff3](http://github.com/symfony/symfony/commit/25c4ff3b9c0bb30d9a3c4559da9171d91d8c41bb): ツールバーの設定がオーバーライドされた場合の修正
- [cec2f48](http://github.com/symfony/symfony/commit/cec2f484053a65bcfa4ab065a73bf4c336b60ca9): [ProfilerManager] プロファイリングが有効な場合にX-Debug-Tokenヘッダーを追加
- [fad8bd7](http://github.com/symfony/symfony/commit/fad8bd768c1cee2190835d4fac188e399ad6c713): テスターを削除
- [b9ae18d](http://github.com/symfony/symfony/commit/b9ae18db39e3d0c7d923351bb603972f71ad894f)、[61a8fc3](http://github.com/symfony/symfony/commit/61a8fc3c2ce810f8393b3c24a858c6ff5c114bc0): [ProfilerBundle] プロファイラーバンドルをリファクタリング
- [f815a6a](http://github.com/symfony/symfony/commit/f815a6a4a6fb3c1853ad52ca9a44a5f0a4a1eaaa): Webデバッグツールバーのコンテナ依存を削除
- [3b4efe5](http://github.com/symfony/symfony/commit/3b4efe52cb7f691bb791032e182af9627d4c95d2): テストからプロファイラーを取得する方法を追加


[その他多数](http://trac.symfony-project.com/trac/timeline?from=06%2F20%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update)


<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
> Symfony 2のオンラインカンファレンスが[開催されました](20100622-the-state-of-symfony2-1)。
> Symfony 2の機能がどれも魅力的すぎて、私の心は一気にSymfony 2に奪われてしまいました。
> 今週中に公開される予定のSymfony 2のプレビューリリース 2が待ち遠しいですね！
> [hidenorigoto]


