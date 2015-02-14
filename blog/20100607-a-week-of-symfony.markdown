---
layout: default
title: A week of symfony #179 (31 May -> 6 June 2010)
---

A week of symfony #179 (31 May -> 6 June 2010)
==============================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/06/06/a-week-of-symfony-179-31-may-6-june-2010)）

<br />
<br />
<hr />

先週は、Symfonyコミュニティによる3つのカンファレンスが告知されました。
スペインの[Jornadas symfony](http://www.symfony-project.org/blog/2010/05/31/announcing-the-first-spanish-symfony-conference)と、
ウクライナの[Symfony Camp](http://www.symfony-project.org/blog/2010/06/04/symfony-camp-ukraine-2010)は7月に開催されます。
そして、Symfony2の現状とすばらしい機能について説明する[初のSymfonyオンラインカンファレンス](http://www.symfony-project.org/blog/2010/05/31/the-state-of-symfony-2-online-conference)も開催されます。


開発メーリングリスト
--------------------

- [Symfony2: Renaming setCulture to setLocale across the framework](http://groups.google.com/group/symfony-devs/browse_thread/thread/0860664bfab8ff15)<br />
  setCultureではなくてsetLocaleにしようという議論で、Symfony2ではlocaleに統一する流れのようです
- [Create symfony 2 sandbox script](http://groups.google.com/group/symfony-devs/browse_thread/thread/b212116fc0eba366)<br />
  Symfony2のサンドボックス環境を生成するスクリプトについて


開発ハイライト
--------------

### symfony 1.Xブランチ：

- [マイルストーン 1.3.5 完了](http://trac.symfony-project.org/milestone/1.3.5)
- [マイルストーン 1.4.5 完了](http://trac.symfony-project.org/milestone/1.4.5)

### Symfony 2.Xブランチ：

- [1a3790a](http://github.com/symfony/symfony/commit/1a3790a636f78ec7c5b08e6981672cf323428c5c): [Foundation] アプリケーション名をクラス名とし使用する場合に正規化する
- [12328a1](http://github.com/symfony/symfony/commit/12328a1bcbf231da8eaf942f8d68c7dc0c7c4f38): [TwigBundle] 最新バージョンのTwigで動作するようにバンドルを更新
- [6261cc2](http://github.com/symfony/symfony/commit/6261cc26693fa1697bcbbd671f18f4902bef07bc): [DoctrineBundle] doctrine:generate:entitiesのヘルプの例が間違っていたのを修正
- [227653f](http://github.com/symfony/symfony/commit/227653fd243498495e4414218e0d4282eef3876e): [TwigBundle] ヘルパーエクステンションに、JavaScriptトークンパーサーを追加


### sfPropelPlugin

- [r29716](http://trac.symfony-project.org/changeset/29716): [1.3, 1.4] default.cssのスタイルを修正


[その他多数](http://trac.symfony-project.com/trac/timeline?from=06%2F06%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update)


<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
> Symfony2についての最新情報が聞けるオンラインカンファレンス[The State of Symfony2](http://www.symfony-live.com/)のアナウンスがありました。
> (記事の日本語訳は[こちら](20100604))
> Symfony2のセカンドプレビューリリースも同時に公開されるそうなので、とても楽しみですね！
> [hidenorigoto]


