---
layout: default
title: A week of symfony #187 (26 July -> 1 August 2010)
---

A week of symfony #187 (26 July -> 1 August 2010)
=================================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/08/01/a-week-of-symfony-187-26-july-1-august-2010)）

<br />
<br />
<hr />

先週は、Symfony2の開発のほとんどをDoctrine Bundleに費やしました。
また、symfony 1.xブランチでは、DoctrineからDoctrine_Coreへの切り替えが行われました。
Symfony2のドキュメントでは、markdown形式からreStructuredText形式への切り替えが行われました。
同時に、[Symfony2ドキュメントの翻訳](http://docs.symfony-reloaded.org/contributing/documentation/translations.html)の募集も開始しました。


開発メーリングリスト
--------------------

- [sfValidatorSchema::preClean()が値を返さない](http://groups.google.com/group/symfony-devs/browse_thread/thread/8aca880a58a7f2d5)<br />
  
- [DoctrineBundleでデフォルト値を1回だけ読み込むように](http://groups.google.com/group/symfony-devs/browse_thread/thread/aca5384feeb2fb31)<br />

- [Symfony2のJavaScriptとスタイルシートのヘルパーを改善](http://groups.google.com/group/symfony-devs/browse_thread/thread/69257ef6578336cc)<br />
  JavaScriptやスタイルシートをヘルパーで追加した場合に、意図した順番にならないという件。
- [sfOutputEscaperObjectDecoratorの制限またはバグ](http://groups.google.com/group/symfony-devs/browse_thread/thread/1b1718488688ed9d)<br />
  sfOutputEscaperObjectDecoratorがパラメーター2つのgetメソッドを適切に処理しない件。


開発ハイライト
--------------

### Symfony 2.Xブランチ：

- [29e083e](http://github.com/symfony/symfony/commit/29e083e9daeb714028e1c955128fc4331d91c582): [DoctrineBundle] コンテナがfreeze()を呼び出していないことに関連するDoctrineExtensionTestの失敗を修正
- [df8ccb4](http://github.com/symfony/symfony/commit/df8ccb46964269ef26096244517666fc9cd5bb48): [FrameworkBundle] コントローラーの引数をフィルタリングするイベントを追加
- [7dc5ae3](http://github.com/symfony/symfony/commit/7dc5ae38080154e1fa5222d105e8dc7890f9ce55): request pathプロパティの名前をrequest attributesに変更
- [3ec9005](http://github.com/symfony/symfony/commit/3ec9005680f10314baae94795fd323949e291085): [Templating] 2重にレンダリングされる問題を引き起こす変数の不適切な命名を修正
- [e35d345](http://github.com/symfony/symfony/commit/e35d3452043bf9322eeb51d97efda36f481b1c94): HttpKernelのワークフローを、より柔軟になるように変更
- [f12e574](http://github.com/symfony/symfony/commit/f12e5747ae2af71675f0af50cb71b5d8f2c81b0f): [Routing] RouterInterfaceを単純化
- [fb55f7b](http://github.com/symfony/symfony/commit/fb55f7beb23d12337831778628f98569c9dcae98): [HttpFoundation] httponlyをデフォルトでtrueに設定
- [6142700](http://github.com/symfony/symfony/commit/6142700881e1717ef516f37fc433ce9c9a48de9b): [HttpFoundation] Cookieのドメインの必須を解除
- [ee9a5db](http://github.com/symfony/symfony/commit/ee9a5db50c4a282961ff3ae8af08620a6549d15e): [DoctrineMongoDBBundle] DoctrineMongoDBBundleで複数の接続/ドキュメントマネージャーのサポートを実装し、コードのリファクタリングとクリーンアップを完了
- [ef070d0](http://github.com/symfony/symfony/commit/ef070d0dd175f4dc3749d4eb2e4304928c5b27d5): [DoctrineBundle] DoctrineBundleをDoctrineMongoDBBundleに合うようにリファクタリング
- [1366396](http://github.com/symfony/symfony/commit/13663966d09d9d3ffdb063f7c314b24779da02a5): [DoctrineBundle] 各エンティティマネージャーのキャッシュドライバーのコンフィギュレーションが無かったのを追加
- [1caabe1](http://github.com/symfony/symfony/commit/1caabe11236d45cef56e28588008d163893dcc9c): [HttpKernel] charsetがレスポンスのContent-Typeヘッダーの一部にある場合のESIでのContent-Typeの管理を修正


### sfDoctrinePlugin：

- [r30441](http://trac.symfony-project.org/changeset/30441)、[r30442](http://trac.symfony-project.org/changeset/30442): [1.3, 1.4] オートローダーへの登録や他の定数をDoctrineからDoctrine_Coreに変更
- [r30444](http://trac.symfony-project.org/changeset/30444): [1.3, 1.4] DoctrineではなくDoctrine_Coreを読み込むようにプラグインを修正
- [r30445](http://trac.symfony-project.org/changeset/30445): [1.3, 1.4] コンパイルされたコアを使えるように、Doctrineがすでに読み込まれているかどうかのチェックを追加



[その他多数](http://trac.symfony-project.com/trac/timeline?from=08%2F01%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update)

<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
> symfony 1.x系では、7/31～8/1に「[Symfony翻訳温泉ツアー](20100801-symfony-translation-spa)」を開催して、Gentle Introductionというsymfony 1.4向けのドキュメントの翻訳を進めました。また、Symfony2系では、公式ドキュメントにsphinxとreStructuredText形式が採用されました。こちらも日本Symfonyユーザー会が中心となって翻訳を進めて行く予定です。どちらもGitHubを使います。未翻訳のドキュメントや英語版の更新に追いつけていないドキュメントなど、作業はたくさんあります。「何か手伝いたい！（けどやり方が分からない）」という方は、お気軽にユーザー会のメーリングリストやtwitterなどで質問してください！
> [hidenorigoto]


