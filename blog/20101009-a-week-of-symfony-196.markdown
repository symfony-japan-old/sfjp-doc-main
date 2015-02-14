---
layout: default
title: A week of symfony #196 (27 September -> 3 October 2010)
---

A week of symfony #196 (27 September -> 3 October 2010)
===============================================================

Symfony 公式ブログで毎週公開される、Symfony 関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony 本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/10/03/a-week-of-symfony-196-27-september-3-october-2010)）

<br />
<br />
<hr />

先週は、Symfony2 の国際化関連機能の開発が行われました。新しい <a href="http://github.com/symfony/symfony/commit/a7537906b4e6e370e5911448f41d6d2552f6832b">Translation コンポーネント</a>が導入され、Twig バンドルに翻訳用のヘルパーが追加されました。また、テンプレートを呼び出す記法でレンダラー（訳注：.php や .twig）の指定が必須となるよう変更され、バリデーションのアノテーションの記述がシンプルになりました。
 
開発メーリングリスト
-------------------

  * [RFC - ホストごとに切り替わる設定ファイル](http://groups.google.com/group/symfony-devs/browse_thread/thread/2d29f16e073d0c93)
  * [Symfony2 でルートコレクション](http://groups.google.com/group/symfony-devs/browse_thread/thread/32282c009eab91df/1cb677bcdf984326)
  * [|safe は分かりづらい](http://groups.google.com/group/symfony-devs/browse_thread/thread/b927063310c74411)
  * [AOP は SF2 に組み込まれますか?](http://groups.google.com/group/symfony-devs/browse_thread/thread/8547bebaf4dbe0f0)

symfony 1 開発ハイライト
------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=03%2F10%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r31002](http://trac.symfony-project.org/changeset/31002 "31002 revision on trac"): \[1.3, 1.4\] 生成される Admin アクションクラスに parent::preExecute() の呼び出しを追加

アクティビティサマリー: チェンジセット 48、バグレポート 16、クローズされた改善 1、ドキュメントのエラー報告 5、ドキュメントの編集 6

Symfony2 開発ハイライト
-----------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [866c306](http://github.com/symfony/symfony/commit/866c306dc860b6b5bf436d9dc9a67c5764bfe504 "866c306dc860b6b5bf436d9dc9a67c5764bfe504 commit on github"): バリデーターコンポーネントからメッセージ補完システムを削除 (i18n の管理を特定のコンポーネントではなくグローバルに行う)
  * [eb942c8](http://github.com/symfony/symfony/commit/eb942c8f18021d1f42d88f17082a99e00828ab39 "eb942c8f18021d1f42d88f17082a99e00828ab39 commit on github"): \[ZendBundle\] Translator の設定を変更
  * [86b6aff](http://github.com/symfony/symfony/commit/86b6aff5b6104e4c55b6d675d72522d22d69c1ac "86b6aff5b6104e4c55b6d675d72522d22d69c1ac commit on github"): \[Form\] setLocale が動作しなかったバグを修正
  * [a305eb0](http://github.com/symfony/symfony/commit/a305eb063d40f0a01d77792e7b502a95a89be86f "a305eb063d40f0a01d77792e7b502a95a89be86f commit on github"): \[Form\] NumberFields に丸めモードオプションのサポートを追加
  * [9e84f45](http://github.com/symfony/symfony/commit/9e84f450c21093391a29f25fd3b9dc38c8d50829 "9e84f450c21093391a29f25fd3b9dc38c8d50829 commit on github"): \[Form\] IntegerField の十進数丸めの修正 (四捨五入の代わりに整数値へのキャスト、つまり常に切り捨てに)
  * [b2e4b45](http://github.com/symfony/symfony/commit/b2e4b452a43e1b82286b972960e806ffc3014deb "b2e4b452a43e1b82286b972960e806ffc3014deb commit on github"): \[Form\] stdClass オブジェクトのサポートを追加
  * [aaba52d](http://github.com/symfony/symfony/commit/aaba52d92816bdc9ce27b491dc8d28c2587c2c2c "aaba52d92816bdc9ce27b491dc8d28c2587c2c2c commit on github"): \[FrameworkBundle\] すべての Router のオプションを設定可能に
  * [b890c34](http://github.com/symfony/symfony/commit/b890c3429df5e929d11af2dedebfec15a885c550 "b890c3429df5e929d11af2dedebfec15a885c550 commit on github"): \[FrameworkBundle\] Code ヘルパーの検出とフォーマット処理を修正
  * [6317ddf](http://github.com/symfony/symfony/commit/6317ddfbe144ed9ca16928d9bf80e7b2e41714f1 "6317ddfbe144ed9ca16928d9bf80e7b2e41714f1 commit on github"): \[ZendBundle\] translator サポートを修正
  * [a753790](http://github.com/symfony/symfony/commit/a7537906b4e6e370e5911448f41d6d2552f6832b "a7537906b4e6e370e5911448f41d6d2552f6832b commit on github"): \[Translation\] コンポーネントを追加
  * [d6f55c3](http://github.com/symfony/symfony/commit/d6f55c31d14db014a1596cdcfcce598985598e42 "d6f55c31d14db014a1596cdcfcce598985598e42 commit on github"): \[TwigBundle\] 翻ヘルパーを追加
  * [d3aca1c](http://github.com/symfony/symfony/commit/d3aca1c04a102b1358cf8cf350764051adee94ab "d3aca1c04a102b1358cf8cf350764051adee94ab commit on github"): \[FrameworkBundle\] Translation コンポーネントのサポートを追加
  * [9580c74](http://github.com/symfony/symfony/commit/9580c74f0bb55fd837fe0745982630ac847d6c3a "9580c74f0bb55fd837fe0745982630ac847d6c3a commit on github"): \[Validator\] メッセージのプレースホルダーの記述ルールを Twig と互換性のあるスタイルに変更 (%limit% から {{ limit }} に)
  * [7072054](http://github.com/symfony/symfony/commit/707205410e1c95c176ee35db04c89e31610e9c43 "707205410e1c95c176ee35db04c89e31610e9c43 commit on github"): 設定がない場合でも translator サービスを常に利用できるように IdentityTranslator を追加
  * [9e50782](http://github.com/symfony/symfony/commit/9e50782b9d3b1724e2f9aca6515c773f6461cec0 "9e50782b9d3b1724e2f9aca6515c773f6461cec0 commit on github"): リクエストのデータコレクターを修正
  * [4ac65ce](http://github.com/symfony/symfony/commit/4ac65cebcf69b78ba7560a78a81e2839d18a7861 "4ac65cebcf69b78ba7560a78a81e2839d18a7861 commit on github"): \[Translation\] Range の名前を Interval に変更
  * [a6dc10c](http://github.com/symfony/symfony/commit/a6dc10c31ae78744ecd513263270f309651c42b0 "a6dc10c31ae78744ecd513263270f309651c42b0 commit on github"): テンプレートを指定する名前の記述方法を変更 (旧: bundle:section:name.format:renderer フォーマットとレンダラーは両方ともオプション; 新: bundle:section:name.format.renderer フォーマットのみオプション)
  * [6aa190b](http://github.com/symfony/symfony/commit/6aa190b2a6c61e1700a3375d4ed245774b8f111f "6aa190b2a6c61e1700a3375d4ed245774b8f111f commit on github"): \[OutputEscaper\] SafeDecoratorInterface を追加
  * [3b1e833](http://github.com/symfony/symfony/commit/3b1e83380b927017e6e9d2a8d88d67e78343c0ae "3b1e83380b927017e6e9d2a8d88d67e78343c0ae commit on github"): \[Validator\] エラーパラメーターが %% で分割される規則を削除
  * [7b9a523](http://github.com/symfony/symfony/commit/7b9a523a43d9026de7725ad734a65774a60bfcbe "7b9a523a43d9026de7725ad734a65774a60bfcbe commit on github")、[6dc6d4a](http://github.com/symfony/symfony/commit/6dc6d4a7d3bbc101d700506e81b68c0dd8b66db0 "6dc6d4a7d3bbc101d700506e81b68c0dd8b66db0 commit on github")、[68bff2d](http://github.com/symfony/symfony/commit/68bff2d21460d222621f71c216e5ee9790cbfe53 "68bff2d21460d222621f71c216e5ee9790cbfe53 commit on github"): \[TwigBundle\] trans タグを修正
  * [4297609](http://github.com/symfony/symfony/commit/42976091563c59cd9c8f9f87e8c2a8dcdc3a4f40 "42976091563c59cd9c8f9f87e8c2a8dcdc3a4f40 commit on github")、[3ce8ad1](http://github.com/symfony/symfony/commit/3ce8ad17189e98596a7535c0139b1dd3e03727a3 "3ce8ad17189e98596a7535c0139b1dd3e03727a3 commit on github"): \[TwigBundle\] エクステンションから translator ヘルパーを削除 (マジック _view 変数コンテキストの使用を削除)
  * [eff1bdf](http://github.com/symfony/symfony/commit/eff1bdf50fa523eccb38e01b59747b09de2a3d87 "eff1bdf50fa523eccb38e01b59747b09de2a3d87 commit on github"): \[TwigBundle\] trans と transchoice タグで変数を利用できるように修正
  * [416bd78](http://github.com/symfony/symfony/commit/416bd7872ec7fb4df5676280414b7e41872b62d8 "416bd7872ec7fb4df5676280414b7e41872b62d8 commit on github"): \[TwigBundle\] ヘルパーの呼び出しを最適化
  * [0fc8906](http://github.com/symfony/symfony/commit/0fc8906feb5865705dfd61c31e871420dcec2bd3 "0fc8906feb5865705dfd61c31e871420dcec2bd3 commit on github"): \[Validator\] 衝突を避けるために、すべてのバリデーション用のアノテーションで validation 名前空間を強制にし、@Validation アノテーションでのラッピングを不要に



> **NOTE**
> 翻訳者コメント<br />
> まだまだ「実案件で使うのはクレイジーだ」と [fabien さんのスライド](http://www.slideshare.net/fabpot/the-state-of-symfony2-symfonyday-2010)でも書かれている Symfony2 ですが、徐々にいろいろな機能が形になってきているようです。また Symfony2 とは別に、Doctrine2 自体もかなり開発が進んでおり、先日開催された [PHP Matsuri](20101005-php-matsuri-2010) の Symfony2 ワークショップでは、Doctrine2 の強力さを目の当たりにしました。
> 日本の Symfony ユーザーの間でも、徐々に Symfony2 や Doctrine2 を試している方がでてきています。
> Symfony2 や Doctrine2 を使ってみたという方、使ってみたけど誰かに聞いてみたいという方、よろしければ [IRC 集会](../events/20101009-irc)で一緒に Symfony2 話で盛り上がりませんか？
> [hidenorigoto]

