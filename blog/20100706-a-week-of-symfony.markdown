---
layout: default
title: A week of symfony #183 (28 June -> 4 July 2010)
---

A week of symfony #183 (28 June -> 4 July 2010)
===============================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/07/05/a-week-of-symfony-183-28-june-4-july-2010)）

<br />
<br />
<hr />

初めてのSymfony2オンラインカンファレンスが盛況のうちに終了した後、先週のSymfony2の開発はコードのリファクタリングに焦点が当てられました。
Dependency Injectionは完全にリファクタリングされ、ユニットテスト、ルーティングリソース、およびいくつかのFoundationのファイルの整理が行われました。


開発メーリングリスト
--------------------

- [Will there be a stable release of the new sfDoctrineGuardPlugin](http://groups.google.es/group/symfony-devs/browse_thread/thread/127fa4c30f19180e)<br />
  sfDoctrineGuardPluginの安定版はリリースされるのか
- [Symfony2 Form in sandbox](http://groups.google.es/group/symfony-devs/browse_thread/thread/08d9950044759d1a)<br />
  Symfony2のサンドボックスのフォームで、バリデーターのエラーがでる
- [add comments to symfony-reloaded.org](http://groups.google.es/group/symfony-devs/browse_thread/thread/ea2c4e90d3cb1152)<br />
  symfony-reloaded.orgにコメントシステムが欲しい


開発ハイライト
--------------

### symfony 1.Xブランチ：

- [r30008](http://trac.symfony-project.org/changeset/30008): [1.3, 1.4] shell_execが無効になっている場合の使用方法を修正
- [r30031](http://trac.symfony-project.org/changeset/30031): [1.3, 1.4] ビューキャッシュにおけるディレクトリトラバーサルの注入脆弱性を回避



### Symfony 2.Xブランチ：

- [220f8ce](http://github.com/symfony/symfony/commit/220f8cecec3ef687e2808e818e79d1d74ea05c82): getProfile()をWebTestCaseからClientへ移動
- [28c1fb2](http://github.com/symfony/symfony/commit/28c1fb2e4cf612b8697b22d37bec609e59858bd5): [Foundation] ファイルの整理
- [898adc6](http://github.com/symfony/symfony/commit/898adc6ef9c8568af45b9cc36f989f537ce3eeb5): より分割するために新しいcollectors.xmlファイルを追加
- [a26bdb7](http://github.com/symfony/symfony/commit/a26bdb7723b65016be6e95d29a00bbcb243b4457)、[2722da2](http://github.com/symfony/symfony/commit/2722da2146b5dedd1e16a8d534171087c26b9315): [DomCrawler] 冗長なメソッドを削除
- [d8efe7e](http://github.com/symfony/symfony/commit/d8efe7edb729e9da0629e5a80c7e6ac52e4393de): [Yaml] UTF-8のバグを修正
- [95769bc](http://github.com/symfony/symfony/commit/95769bc315addb063b4b2a3dc22544707fef44d4): [FoundationBundle] request.base_pathパラメーターを削除 (DICを不変に)
- [59c1ebe](http://github.com/symfony/symfony/commit/59c1ebe1b6915bc15f811424ec518cc22acf65ac): [FoundationBundle] HelperからTemplatingへ移動
- [c98c733](http://github.com/symfony/symfony/commit/c98c7339f1252fe3db09b41da1e540d8b18e95e4): [Tests] bootstrap.phpのインクルードは不要なので削除
- [9895eaf](http://github.com/symfony/symfony/commit/9895eaf3cbbe699b30275e0bdee682a5b8a41a07): DependencyInjectionコンテナをリファクタリング
- [e578dfd](http://github.com/symfony/symfony/commit/e578dfdbecc9c8c73867dc8e16700c77c0aa37e4): [DomCrawler] テストを追加
- [aa697d8](http://github.com/symfony/symfony/commit/aa697d8a0ce23e25626565b75b871dabd1f5cdce): dev環境でモニタリングするためにリソースのリストにバンドルとエクステンションを追加
- [87ae06c](http://github.com/symfony/symfony/commit/87ae06c8cb65fe24220d0b63635a650365273361): [Routing] リソースをリファクタリング
- [244c202](http://github.com/symfony/symfony/commit/244c202a087920075252203070d082204e7a15f2): ユニットテストを整理
- [53847ca](http://github.com/symfony/symfony/commit/53847ca90c254540fb491e66dee61f5b900b9995): [DoctrineBundle] 上層の変更を反映するためにインターフェイスを修正
- [04e621a](http://github.com/symfony/symfony/commit/04e621a5cdc81b2b7082483ef09644859648dc50): [Yaml] ドキュメントの終端マーカーのサポートを追加

[その他多数](http://trac.symfony-project.com/trac/timeline?from=07%2F04%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update)

<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
> 先週はsymfony 1.xの[セキュリティリリース](20100629-security-release-symfony-1-3-6-and-1-4-6)がありました。
> symfony 1.xでビューキャッシュを利用している場合は、アップグレードすることが推奨されています。
> こういったアップグレードに迅速に対応するためにも、普段からテストを書いておくと良いですよね。
> [OSC Nagoya](http://www.ospn.jp/osc2010-nagoya/)では、symfonyのテストについての簡単なセミナーを開催する予定なので、お近くの方は是非いらしてください。
> [hidenorigoto]


