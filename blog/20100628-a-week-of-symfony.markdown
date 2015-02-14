---
layout: default
title: A week of symfony #182 (21->27 June 2010)
---

A week of symfony #182 (21->27 June 2010)
=========================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/06/27/a-week-of-symfony-182-21-27-june-2010)）

<br />
<br />
<hr />

先週は、[Symfony2オンラインカンファレンス](http://www.symfony-project.org/blog/2010/06/24/symfony2-online-conference)がSymfonyコミュニティで大きな注目を集めました。Symfony2の注目機能である、Symfony2アプリケーションを大幅に高速化するHTTPアクセラレーターが紹介されました。さらに、symfony 1.xブランチでは30,000個目のチェンジセットがコミットされました。


開発メーリングリスト
--------------------

- [Symfony 2 PR 2](http://groups.google.es/group/symfony-devs/browse_thread/thread/4cee3ddc7aa098bc)<br />
  Symfony2のconfigファイルのデフォルトフォーマットについて
- [Hash algorithms](http://groups.google.es/group/symfony-devs/browse_thread/thread/37c3d5aef3b8b346)<br />
  sfGuardなどで利用するパスワードハッシュアルゴリズムの強化について
- [Symfony2.0 caching](http://groups.google.es/group/symfony-devs/browse_thread/thread/b8b03eb121a340ca)<br />
  Symfony2のキャッシュについて


開発ハイライト
--------------

### symfony 1.Xブランチ：

- [r29990](http://trac.symfony-project.org/changeset/29990): [1.3, 1.4] sfOutputEscaperObjectDecorator::__isset()を追加


### Symfony 2.Xブランチ：

- [8c0f7e8](http://github.com/symfony/symfony/commit/8c0f7e8569afb801262ec3fbed3aa8c07eefa626): [OutputEscaper] オブジェクトのマジックメソッドを直接呼び出すのではなく、キャストするように変更
- [d6a7b43](http://github.com/symfony/symfony/commit/d6a7b43e8af21b3147ceefe9c3cf26e5b598144a): [DomCrawler] HTMLコンテンツを文字列として扱うメソッドの追加
- [7db3ef7](http://github.com/symfony/symfony/commit/7db3ef75a0bd23659138f37afa8d281f7bf2883a): [WebBundle] collectors.xmlをprofiling.xmlに名前変更
- [8ea13f9](http://github.com/symfony/symfony/commit/8ea13f910c9d0f43517575363eefd4cc7e384dbd): [HttpKernel] PHPUnitのアサーションの順序と合うように、アサーションの引数の順序を変更
- [0e3b88a](http://github.com/symfony/symfony/commit/0e3b88a058abfe58b9e1f1e1ef281092c12c32c9): [DependencyInjection] 拡張子を使っている場合の継承を修正
- [c486e1b](http://github.com/symfony/symfony/commit/c486e1ba10056b5cd7d1a626b423eb77ce9a5cc9): [DependencyInjection] リバート
- [7661e9a](http://github.com/symfony/symfony/commit/7661e9a5f79f32b2bd8277dcd01eaa3a14ef692b): [HttpKernel] Response::__toString()をさらに便利に
- [da23747](http://github.com/symfony/symfony/commit/da23747a1a95eb7ff75cdccc23017b0c552193b8): [HttpKernel] レスポンスのアサーションを削除
- [82d83fc](http://github.com/symfony/symfony/commit/82d83fc6c920fb526185e71856108d10d445e5a2)、[449bf62](http://github.com/symfony/symfony/commit/449bf6266da74cb480cd2679e19321b4992feadf): [PropelBundle] build-sqlコマンドを追加
- [3ec2577](http://github.com/symfony/symfony/commit/3ec25777d19455d6b129bdef038758f2e1e8de0d): [PropelBundle] namespaceによる自動パッケージを追加
- [097b87b](http://github.com/symfony/symfony/commit/097b87b451d130b5a585864e3b491d1c5f5a9375): [PropelBundle] 他のタスクのハブであるBuildタスクを作成
- [82890a3](http://github.com/symfony/symfony/commit/82890a32dccea1003bdd92af73c44ebbe70d486d): [PropelBundle] sqlmapのファイル名を修正
- [a05a82a](http://github.com/symfony/symfony/commit/a05a82a892b81f5fba728708a8f3cb65c8d24974): コードカバレッジのオートロードを修正
- [97162cf](http://github.com/symfony/symfony/commit/97162cfeda4517c9facb08ed5e3c435a39c355e7): Cookie管理をリファクタリング
- [ed72875](http://github.com/symfony/symfony/commit/ed7287538bc402da47465927254bcaa47969e423): バンドルクラスの名前を、それ自身が明確になるように変更
- [785da59](http://github.com/symfony/symfony/commit/785da59eb5ca9a58f871a1d5300f72349a74156d): [HttpKernel] キャッシュシステムを追加
- [99a63fe](http://github.com/symfony/symfony/commit/99a63fe1a66c6cb80a3a74d17afc909fccfe790d): WebBundleは単なるWebに関連するもののみではないため、FoundationBundleに名前を変更
- [3eb5545](http://github.com/symfony/symfony/commit/3eb554550b2d444c32d150a1095127d59d9077fe): [Routing] ユニットテストを追加
- [6e310bd](http://github.com/symfony/symfony/commit/6e310bd4ecdf854eb95e7702502519b64026e618)、[bcd4b6d](http://github.com/symfony/symfony/commit/bcd4b6d14095661402dacbb118930f4d5e00d4c1): フォーム、バリデーター、I18Nとファイルコンポーネントを統合
- [ca3dc31](http://github.com/symfony/symfony/commit/ca3dc3105712ea66ed048cf6330822e19bcddcfc): フォームコンポーネントと国際化拡張を切り離し
- [be9148a](http://github.com/symfony/symfony/commit/be9148adf203579d69e26f15607bfffe0cd8ff39): DoctrineMongoDBBundleを追加
- [763a99e](http://github.com/symfony/symfony/commit/763a99e3681fd2230a6b651977032a78597b5cc9): [TwigBundle] アセットタグを追加

[その他多数](http://trac.symfony-project.com/trac/timeline?from=06%2F27%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update)


<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
> Symfony2のオンラインカンファレンスが開催された後、Symfony2のプレビューリリース2が公開されました。
> Symfony2のキャッシュシステムに興味のある方は、このあたりのソースを読んでみるとよいかもしれません。
>
> - [/Symfony/Components/HttpKernel/Cache/Cache.php](http://github.com/symfony/symfony/blob/master/src/Symfony/Components/HttpKernel/Cache/Cache.php)
> - [/Symfony/Components/HttpKernel/Cache/Esi.php](http://github.com/symfony/symfony/blob/master/src/Symfony/Components/HttpKernel/Cache/Esi.php)
>
> [hidenorigoto]


