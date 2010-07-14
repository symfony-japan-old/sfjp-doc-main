A week of symfony #184 (5->11 July 2010)
========================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/07/11/a-week-of-symfony-184-5-11-july-2010)）

<br />
<br />
<hr />

先週は、Symfony2の内部の大幅なリファクタリングを行いました。
2つの主要な名前空間の名前を変更（Symfony\Framework を Symfony\Bundle に。Symfony\Foundation を Symfony\Framework に）し、HttpFoundationコンポーネントを新しく導入しました。
また、Symfony2のドキュメントが追加され、簡潔なドキュメントやガイドが合計30個になりました。

開発メーリングリスト
--------------------

- [DomCrawler Form getUri() don't return the good URI](http://groups.google.com/group/symfony-devs/browse_thread/thread/ca50e6a82669cc9f)<br />
  DomCrawlerのgetUri()のバグについて
- [sfDoctrineGuardPlugin branch 1.3 is broken](http://groups.google.com/group/symfony-devs/browse_thread/thread/7334606ff8e5a97c)<br />
  sfDoctrineGuardPluginがsymfony 1.3で動作しない
- [HTML5 application cache in Symfony2](http://groups.google.com/group/symfony-devs/browse_thread/thread/1c755c7fd5f24e2a)<br />
  Symfony2でHTML5のサポートの計画はあるのか？<br />
  スレッド中で、Symfony2のフォームコンポーネントを開発しているBernhardさんが、HTML5フォーム要素のサポートは計画中とコメントしています。


開発ハイライト
--------------

### Symfony 2.Xブランチ：

- [99c33ca](http://github.com/symfony/symfony/commit/99c33cadf058fcde2915ca6d97b3a909421eb36e): [FoundationBundle] FilesystemでFinderへの依存を削除
- [19d3e98](http://github.com/symfony/symfony/commit/19d3e9867503beff541e5f91e329f2e74676a025): [HttpKernel] プロファイルデータが2重に挿入される問題を修正
- [04a8705](http://github.com/symfony/symfony/commit/04a87053d17cde142dfe60b4448cb4c009d7c5fb): [Console] --color/-cオプションが--config/-cオプションと衝突するのを回避するために、--ansi/-aオプションに変更
- [aaa6aba](http://github.com/symfony/symfony/commit/aaa6aba60bb8162a7363b5289c1f3bc5f9e5ed7f): [Console] 名前を定義せずにスタイルを使う方法を追加
- [99952c6](http://github.com/symfony/symfony/commit/99952c6042fffeb2ee4a52aa29384723c31e1f28): [Console] 1つのコマンドだけのコンソールアプリケーションを作る方法を追加
- [a747987](http://github.com/symfony/symfony/commit/a747987625fb9e13db83d37bbc775e2f2d44d076): [Validator] カスタム作成した制約をローダーで使えるように修正
- [f6b9d9e](http://github.com/symfony/symfony/commit/f6b9d9e0461ce8fc96f0e2c91ecfa085b666a5ce): [Validator] すべてのメタデータクラスをシリアライズできるように修正
- [fd3243a](http://github.com/symfony/symfony/commit/fd3243a943a76c9959ce2d6712690417e593a5ce): [Finder] 異なるOSを想定した明示的なソートがないテストを修正
- [34dd0ea](http://github.com/symfony/symfony/commit/34dd0ea25b8667ea74d99f23174aba3c9dd76407): [Form] フォームでconfigure()が呼ばれる前にオブジェクトが保存されていたのを修正
- [1c7b459](http://github.com/symfony/symfony/commit/1c7b4597761370c4ee521804e5fcd99efd21cabb): [Form] '0'という名前のフィールドが使えるように修正
- [8c9f9de](http://github.com/symfony/symfony/commit/8c9f9de0863c77922c1240dc409378a3374e59fb): [Validator] メタデータキャッシュのサポートを追加
- [f2c4f20](http://github.com/symfony/symfony/commit/f2c4f20e70e98a76c48ce99c26fabec9430825bf): [Validator] '0'を制約のオプション値のデフォルトとして使えるように修正
- [a9ad743](http://github.com/symfony/symfony/commit/a9ad743006fef13fe757795d44dd16e61135ce94): [DependencyInjection] services.xsdをより厳密になるように変更
- [4bbf2ae](http://github.com/symfony/symfony/commit/4bbf2ae055b264325d5c8ef4136e825b872a5257): [DependencyInjection] (Springのように)constructorをfactory methodに名前変更
- [27458b6](http://github.com/symfony/symfony/commit/27458b653e6600971b34b2d5f1d0c794ad6940eb): [DependencyInjection] サービスでプロパティは利用できないので、@propertyアノテーションを削除
- [ef91396](http://github.com/symfony/symfony/commit/ef913966188e829ade0206d18c8c027db0168745)、[8d067ba](http://github.com/symfony/symfony/commit/8d067bac51f80c3fce8119deaee397b1b1f78c6e): [DependencyInjection] DI定義にファクトリークラス、ファクトリーサービスの概念を追加
- [b6799d0](http://github.com/symfony/symfony/commit/b6799d0d80836f520a983ddc75a59a8ca2a7c9bd): [FoundationBundle] サブ名前空間を持つバンドル向けの修正
- [4b24544](http://github.com/symfony/symfony/commit/4b24544cdabd3817d9bfeab91ff1d9f3f839b6f2): Symfonyのエラーハンドラーを無効にする機能を追加(PHPUnitではテスト用に、PHPのエラーが起こった場合にPHPUnit_Framework_Error、PHPUnit_Framework_Warning、PHPUnit_Framework_Noticeという例外を探す機能が組み込まれています）
- [6613555](http://github.com/symfony/symfony/commit/6613555059e45b745e080a1a13380400f89d85f6): [DomCrawler] フォームのアクション属性が絶対URLだった場合のForm::getUri()とLink::getUri()の問題を修正
- [7e8d0d2](http://github.com/symfony/symfony/commit/7e8d0d2470dc3f8452d22d9657a4c6b91a360c84): すべてのリスナークラスの名前をListenerで終わるように修正
- [e63ff6e](http://github.com/symfony/symfony/commit/e63ff6e04b37ca75f2823cef1e455957552dd002): [DependencyInjection] DOMに同じ名前の複数の要素があった場合のDOMから配列への変換処理を修正
- [9133b9e](http://github.com/symfony/symfony/commit/9133b9e5e44a02400f4e4de989e64809597c6f1f): Request/Response/Userクラスを新しいHttpFoundationコンポーネントは移動。HttpFoundationコンポーネントには、PHPのネイティブグローバル配列をラップするクラスを配置
- [6213fde](http://github.com/symfony/symfony/commit/6213fdefb9324069be77d162bb5c76de14a8c494): Symfony\Framework を Symfony\Bundle に名前変更。既存のSymfony2アプリケーションでは、Symfony\Frameworkへの参照はメインのカーネルクラス（registerBundles()とregisterBundleDirs()）と、すべてのコントローラークラスにあります。コンソールスクリプトも変更する必要があります。
- [15d4398](http://github.com/symfony/symfony/commit/15d439809c524d3478433b93008f90091a47db45): Symfony\Bundle\FoundationBundle を Symfony\Bundle\FrameworkBundle に名前変更
- [da9f36c](http://github.com/symfony/symfony/commit/da9f36ca86611eefaf5634f4d29b9c2167099d1d): Symfony\Foundation を Symfony\Framework に名前変更


[その他多数](http://trac.symfony-project.com/trac/timeline?from=07%2F11%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update)

<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
> 先週はSymfony2に大幅なリファクタリングが行われました。ベースとなる機能などはかなり固定されてきていますが、フレームワークとしては
> まだまだこのような大きな変更もあり得る段階ですので、実務プロジェクトへの採用はもう少し我慢した方がよさそうですね。
> （早く使いたいのですが・・・）
> [hidenorigoto]


