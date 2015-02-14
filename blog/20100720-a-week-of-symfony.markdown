---
layout: default
title: A week of symfony #185 (12->18 July 2010)
---

A week of symfony #185 (12->18 July 2010)
========================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/07/18/a-week-of-symfony-185-12-18-july-2010)）

<br />
<br />
<hr />

先週は、Symfony2の主要なコンポーネントの1つであるDependency Injectionコンポーネントの大きなリファクタリングが行われました。
また、数百ものsymfonyに関連するブログに、新たに4つのブログが追加されました。


開発メーリングリスト
--------------------

- [Symfony2 Sandbox & Cache](http://groups.google.com/group/symfony-devs/browse_thread/thread/ba33c34a6e5e334c)<br />
  Symfony2のサンドボックスと、Cache機能の利用、サンドボックスの更新などについて
- [symfony 1.2 maintenance / contribution](http://groups.google.com/group/symfony-devs/browse_thread/thread/1c45be901ac553d)<br />
  symfony 1.2のメンテナンス等について
- [Symfony plugin README breakage](http://groups.google.com/group/symfony-devs/browse_thread/thread/5c2b94512708fb04/222e29c2ca7550e9#222e29c2ca7550e9)<br />
  symfony pluginのREADMEページが正しく動作していなかった件、fabienさんが適用した修正をrevertしたとのこと


開発ハイライト
--------------

### Symfony 2.Xブランチ：

- [ab26f9f](http://github.com/symfony/symfony/commit/ab26f9f3bf1aa79a6fac14bda95c23258624435d): [OutputEscaper] __get()をEscaperからObjectEscaperへ移動
- [fe7e01c](http://github.com/symfony/symfony/commit/fe7e01c653677c298de698cd9f244807d47a21fb): [OutputEscaper] object escaperに__isset()マジックメソッドを追加
- [0fbb1b9](http://github.com/symfony/symfony/commit/0fbb1b916b4e2a09d0c50bbaaa28540be7a8c70f): DIエクステンションの読み込み機構をクリーンアップ
- [4375594](http://github.com/symfony/symfony/commit/437559491f92554a0ab127b348a805a70fc82891): ExceptionFormatterでContainer->hasParameter()をContainer->getParameterBag()->has()に置き換え
- [44a16fc](http://github.com/symfony/symfony/commit/44a16fc8c4f5444ef2594d7755a757093daeb132): [Finder] 除外イテレーターを修正(相対パスのみにマッチするように)
- [fb4bd35](http://github.com/symfony/symfony/commit/fb4bd3568d21a5e13ae7766b6a0c328cc45af4e7): controller managerをリファクタリングし、一般的な部分をHttpKernelコンポーネントへ移動
- [0163178](http://github.com/symfony/symfony/commit/0163178f7b8750c8d6fa5ba75255ea22a54a6512): BundleInterface::buildContainer()のシグニチャを変更
- [b8f29f1](http://github.com/symfony/symfony/commit/b8f29f18c07e09ef2c59ed79a384ac4d8c7ee475)、[6462814](http://github.com/symfony/symfony/commit/6462814483bd276f8c445116aeb0fe7ff3e95882)、[826e615](http://github.com/symfony/symfony/commit/826e61561a4d4923e72ef59a6f36fad3c6f6c5f9): [Framework] コマンド登録処理をクリーンアップ
- [92130c3](http://github.com/symfony/symfony/commit/92130c3da16a8887cc0946879dffac7a69a2ec8b): bootstrap.phpを更新
- [7796eb2](http://github.com/symfony/symfony/commit/7796eb213c2f9baea0f8f484986e845ecfb075d1): BuilderConfigurationとBuilderクラスを新しいContainerBuilderクラスへマージ
- [6bad580](http://github.com/symfony/symfony/commit/6bad58012f8f0d94f13e7e68bc88ef4878fcf429): [DependencyInjection] ContainerBuilder::resolveValue()をParameterBagへ移動
- [47fd5e8](http://github.com/symfony/symfony/commit/47fd5e848be60f9bebc8ca2eea684d03c5718907): [DependencyInjection] パラメーター値のプレスホルダー管理を修正
- [2a051b5](http://github.com/symfony/symfony/commit/2a051b50392d94d72a84ab5911fba267551ab340): DIエクステンションクラスを自身のサブ名前空間へ移動
- [ca87621](http://github.com/symfony/symfony/commit/ca8762141fe7c9a2eb6795ecfba93e919b82882f)、[1dd5b61](http://github.com/symfony/symfony/commit/1dd5b61e17ac7a37ee3e15db1c80f191e50a4e75)、[44757b0](http://github.com/symfony/symfony/commit/44757b0c77d0bc3f9f81f566f31822cc68d45cf2): [DependencyInjection] コンテナのPHPへのダンプ時にクラス名のチェックを追加
- [82ec700](http://github.com/symfony/symfony/commit/82ec7004d547e6d7d45858a7bf2ec95eef63df2c): [Console] InputDefinitionのsetArgumentsでhasAnArrayArgumentをリセットするように修正


[その他多数](http://trac.symfony-project.com/trac/timeline?from=07%2F18%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update)

<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
> メーリングリストでsymfony 1.2のメンテナンスについての議論があったようですが、twitterでもsymfony 1.xのメンテナンス期間等についての議論があったようです。議論は[こちら](http://togetter.com/li/35970)にまとめています。
> symfony 1.xのサポート期間については、ユーザー会のIRC集会でも話題にしたことはありますが、なかなか難しい問題です。
> OSSをメンテナンスしていくにはある程度の覚悟が必要ですし、また、そのソフトウェアへの理解も必要です。
> が、必要なことであれば、まずは「やる！」と言うことが大切なのかもしれませんね。
> [hidenorigoto]


