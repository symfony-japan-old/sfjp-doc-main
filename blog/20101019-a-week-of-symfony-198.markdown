---
layout: default
title: A week of symfony #198 (11->17 October 2010)
---

A week of symfony #198 (11->17 October 2010)
============================================

Symfony 公式ブログで毎週公開される、Symfony 関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony 本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/10/17/a-week-of-symfony-198-11-17-october-2010)）

<br />
<br />
<hr />

This week, symfony project unveiled all the details for the upcoming <a href="http://www.symfony-live.com/">Symfony Live 2011</a> conferences in Paris and San Francisco. Meanwhile, Symfony2 development showed an impressive activity boosted by lots of patches committed by the community. Lastly, as a proof that time flies when you're having fun programming, the next week symfony turns 5 years old (on October 18).
今週は、パリとサンフランシスコで開催される<a href="http://www.symfony-live.com/">Symfony Live 2011</a>カンファレンスの詳細情報を公開しました。その間にもSymfony2に多くのパッチがコミットされ、飛躍的に開発が進んでいます。さて、プログラミングに熱中しているとあっという間に時間は過ぎていくもので、10月18日でsymfonyも5歳になります。
 
開発メーリングリスト
------------------------

  * [Sf2における多様的なルーティングについて](http://groups.google.com/group/symfony-devs/browse_thread/thread/74bdcfdad018cd10)
  * [Symfony2 - バリデータの制約と依存性](http://groups.google.com/group/symfony-devs/browse_thread/thread/944d9d42f7de4ba9)
  * [テーマの切り替えはどこで行えばよいか](http://groups.google.com/group/symfony-devs/browse_thread/thread/f7894031a34aa966)
  * [RFC - ハードコードされたルートクラス](http://groups.google.com/group/symfony-devs/browse_thread/thread/dd4049cffdf81207)

Symfony2 開発ハイライト
-------------------------------

[チェンジログ](http://github.com/symfony/symfony/commits/master):

  * [af8cb48](http://github.com/symfony/symfony/commit/af8cb480a3e9f77a8788ea1b80b2bba4399c337f "af8cb480a3e9f77a8788ea1b80b2bba4399c337f commit on github"): \[FrameworkBundle\] Templatingでレンダラーの遅延ローディングを行うよう修正
  * [dbde494](http://github.com/symfony/symfony/commit/dbde494424d89f50b8614f2e50040dcd21c17f7a "dbde494424d89f50b8614f2e50040dcd21c17f7a commit on github"): 国際化におけるロケールの特定の遅延ローディングを行うよう修正
  * [f033fc5](http://github.com/symfony/symfony/commit/f033fc5578b0a2953fe5e95bac6c99766c28625e "f033fc5578b0a2953fe5e95bac6c99766c28625e commit on github"): ValueTransformersにてreverseTransform()が呼ばれた際に元の値を受け取るよう修正
  * [0d9d4ac](http://github.com/symfony/symfony/commit/0d9d4ac583ad73859880973d3ffcc8f90866cbf3 "0d9d4ac583ad73859880973d3ffcc8f90866cbf3 commit on github"): Form/Configurableの最適化、ChoiceFieldが常にデータをトランスフォーマーに渡すよう修正、Doctrine ORM固有のコレクションを文字列/チョイス形式に変換する2つのトランスフォーマーの実装とユニットテストの追加
  * [ec3b3f7](http://github.com/symfony/symfony/commit/ec3b3f7637c94be6e9be4c8061b35f9e10129a6d "ec3b3f7637c94be6e9be4c8061b35f9e10129a6d commit on github"): EntityToIDTransformerで多対1もしくは1対1のエンティティをIDに変換する処理とテストの追加
  * [db3476a](http://github.com/symfony/symfony/commit/db3476aeaa74a6b888e60381929dda8a92c7491a "db3476aeaa74a6b888e60381929dda8a92c7491a commit on github"): \[WebProfilerBundle\] DIコンテナーのエクステンションをシンプルに修正
  * [bf1eb56](http://github.com/symfony/symfony/commit/bf1eb56a34cf8aa809150f28c5dfc2ca04593c73 "bf1eb56a34cf8aa809150f28c5dfc2ca04593c73 commit on github"): \[EventDispatched\] Eventで不要となったArrayAccessインターフェイスを削除
  * [d8f4cb7](http://github.com/symfony/symfony/commit/d8f4cb79c92f631d3de2bcc719a8a38245c42c14 "d8f4cb79c92f631d3de2bcc719a8a38245c42c14 commit on github"): \[Form\] FieldGroup::getFields()に柔軟性をもたらす4つのメソッドを追加
  * [fafcd02](http://github.com/symfony/symfony/commit/fafcd02684ef4029beb40b11ca72dabe2eabff2f "fafcd02684ef4029beb40b11ca72dabe2eabff2f commit on github"): \[HttpFoundation\] RequestMatcherの正規表現の扱いを修正
  * [7ad510d](http://github.com/symfony/symfony/commit/7ad510d6ef66ba7471d8d4e7fee003752c0618f9 "7ad510d6ef66ba7471d8d4e7fee003752c0618f9 commit on github"): assets:installコマンドに--symlinkオプションを追加
  * [aa1cb87](http://github.com/symfony/symfony/commit/aa1cb87f603ef87f5b5c0506ffa92e0387debf39 "aa1cb87f603ef87f5b5c0506ffa92e0387debf39 commit on github"): \[FrameworkBundle\] InitBundleCommand.phpから通知される例外のメッセージをわかりやすく変更
  * [ade5fd6](http://github.com/symfony/symfony/commit/ade5fd6574d8c17537a058d055d78489505e6992 "ade5fd6574d8c17537a058d055d78489505e6992 commit on github"): WebProfilerのrequest_panel.phpのバグを修正
  * [f667b69](http://github.com/symfony/symfony/commit/f667b6928fa481745ca4c942b79b66a7b394a5ad "f667b6928fa481745ca4c942b79b66a7b394a5ad commit on github"): \[TwigBundle\] CollectionFieldをレンダリングするためのブロックを追加
  * [1fab031](http://github.com/symfony/symfony/commit/1fab031d4d91719d49d42e6edcdc8d6da4f10339 "1fab031d4d91719d49d42e6edcdc8d6da4f10339 commit on github"): EntityToIDTransformerの追加
  * [e1be4e9](http://github.com/symfony/symfony/commit/e1be4e96899bfb03193c83b0c979c45e462e0436 "e1be4e96899bfb03193c83b0c979c45e462e0436 commit on github"): \[Form\] FieldからPropertyPathへの値の読み込み/設定処理のリファクタリング
  * [a66d883](http://github.com/symfony/symfony/commit/a66d883afd1cf69f5879734e7b6d7a2b75ebbfcd "a66d883afd1cf69f5879734e7b6d7a2b75ebbfcd commit on github"): \[Form\] CSRF関連のセッターを削除
  * [2a9ddee](http://github.com/symfony/symfony/commit/2a9ddee162e184efc862b557673b17640d2fa83a "2a9ddee162e184efc862b557673b17640d2fa83a commit on github"): \[HttpFoundation\] Session::invalidate()の追加
  * [30cf086](http://github.com/symfony/symfony/commit/30cf0868281fa2e34ce347ea0fb1201842bf1d6e "30cf0868281fa2e34ce347ea0fb1201842bf1d6e commit on github"): {% include %}の挙動をEngineから呼び出すよう上書き
  * [d376596](http://github.com/symfony/symfony/commit/d376596f7e490257db04ce307c60f1ef33767672 "d376596f7e490257db04ce307c60f1ef33767672 commit on github"): \[EventDispatcher\] EventDispatcher::disconnectで第2引数がnullの場合のバグを修正
  * [df9ef79](http://github.com/symfony/symfony/commit/df9ef799536a68c23367e11ebdd6e13947b57bb5 "df9ef799536a68c23367e11ebdd6e13947b57bb5 commit on github"): \[Form\] readPropertyPathが空配列ではなくnullを返すよう修正
  * [7e66933](http://github.com/symfony/symfony/commit/7e669338761f1b856efa0ecd01a91cc1e1180996 "7e669338761f1b856efa0ecd01a91cc1e1180996 commit on github"): イベントからHttpKernelオブジェクトが呼ばれた際の矛盾を修正

> **NOTE**
> 翻訳者コメント<br />
> 昨日はsymfonyの記念すべき5回目の誕生日でした。誕生日を祝ってか、Fabien氏からSymfony2のSecurityコンポーネントがリリースされました。全体的に荒削りではありますが、Symfony2の主要なコンポーネントは一通り出そろったようです。ぜひ興味がある方は触ってみて、バグ報告などのお手伝いをしていただければ幸いです。
> [fivestar]


