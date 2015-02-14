---
layout: default
title: A week of symfony #195 (20->26 September 2010)
---

A week of symfony #195 (20->26 September 2010)
==============================================

今週は、Symfony開発者メーリングリストが様々な議論が活発に行われました。数あるトピックの中でも、Symfony2のデフォルトテンプレートエンジン(PHP or Twig)についてと、デフォルトの設定ファイルのフォーマット(PHP, XML or YAML)について議論が行われていました。このメーリングリストこそSymfony2に関する最先端の情報を得られる場所で、まさに今後の方向性を担う場所でもあります。
 
開発メーリングリスト
------------------------

  * [[Symfony2] デフォルトはTwig？](http://groups.google.com/group/symfony-devs/browse_thread/thread/80d5e981ed247ccb/0a59e16587091ded)
  * [Symfony2フォーム: symfony 1からのフィードバック](http://groups.google.com/group/symfony-devs/browse_thread/thread/4cf6e1fd796a16e4/63a4a763cbdafa60)
  * [コントローラーとDI](http://groups.google.com/group/symfony-devs/browse_thread/thread/7766abae81097e9d/c9209fd91dfc0dd0)
  * [設定ファイルのデフォルトフォーマット](http://groups.google.com/group/symfony-devs/browse_thread/thread/1da7eb31466bccf8)

symfony 1 開発ハイライト
--------------------------------

[チェンジログ](http://trac.symfony-project.com/trac/timeline?from=26%2F09%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r30951](http://trac.symfony-project.org/changeset/30951 "30951 revision on trac"): \[1.3, 1.4\] WDTが複数入らないよう修正
  * [マイルストーン 1.3.7 完了](http://trac.symfony-project.org/milestone/1.3.7)
  * [マイルストーン 1.4.7 完了](http://trac.symfony-project.org/milestone/1.4.7)
  * [r30961](http://trac.symfony-project.org/changeset/30961 "30961 revision on trac"): \[1.3, 1.4\] WDTのJavaScriptが挿入されない問題を修正

sfPropelPlugin:

  * [r30966](http://trac.symfony-project.org/changeset/30966 "30966 revision on trac"): \[1.3, 1.4\] スロベニア用の翻訳ファイルを修正
  * [r30967](http://trac.symfony-project.org/changeset/30967 "30967 revision on trac"): \[1.3, 1.4\] 中国語繁体字のサポートに関する修正
  * [r30968](http://trac.symfony-project.org/changeset/30968 "30968 revision on trac"): \[1.3, 1.4\] アドミンジェネレータにおけるペルシャ語の翻訳を修正
  * [r30969](http://trac.symfony-project.org/changeset/30969 "30969 revision on trac"): \[1.3, 1.4\] ドイツ語とイタリア語の翻訳を追加

アクティビティ要約: 64 changesets, 21 bugs reported, 4 bugs fixed, 3 enhancements suggested, 1 enhancement closed, 8 documentation defects reported, 1 documentation defect fixed, and 4 documentation edits

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [5f9c365](http://github.com/symfony/symfony/commit/5f9c365971620d3c379e96169e9b2986072a0ca4 "5f9c365971620d3c379e96169e9b2986072a0ca4 commit on github"): \[DoctrineMongoDBBundle\] クエリログ中のboolean型の表示フォーマットを修正
  * [e6bff04](http://github.com/symfony/symfony/commit/e6bff045c994de097f2feca67d53753c8e08a552 "e6bff045c994de097f2feca67d53753c8e08a552 commit on github"): \[DoctrineMongoDBBundle\] クイックプロファイラーパネルを追加
  * [71cc3a7](http://github.com/symfony/symfony/commit/71cc3a77734796db8691ac2289fd53ee2137c4bb "71cc3a77734796db8691ac2289fd53ee2137c4bb commit on github"): \[Form\] 二重にエスケープに関してhtmlspecialchars()の第4引数を用いて対応するよう修正
  * [2862c6c](http://github.com/symfony/symfony/commit/2862c6cce41a3af2d9a6d64502246ea072de0b5a "2862c6cce41a3af2d9a6d64502246ea072de0b5a commit on github"): 設定項目名の変更 (コミットログにアップグレード方法を記載)
  * [82f6a68](http://github.com/symfony/symfony/commit/82f6a68eb2cab5a0caf7e8fc52ba770364cf2d19 "82f6a68eb2cab5a0caf7e8fc52ba770364cf2d19 commit on github"): \[Validator\] DateTimeオブジェクトがバリデーションに通るよう修正
  * [2d80788](http://github.com/symfony/symfony/commit/2d80788e3aa7f406a14d00543d32ed1e81579bdb "2d80788e3aa7f406a14d00543d32ed1e81579bdb commit on github"): \[FrameworkBundle\] サービスをコントローラとして扱える仕組みを追加
  * [f3993b4](http://github.com/symfony/symfony/commit/f3993b45c1ac6e69a82d9f66ef7e82bb87515851 "f3993b45c1ac6e69a82d9f66ef7e82bb87515851 commit on github"): Webプロファイラー内の全img要素にwidth, height, alt属性を指定
  * [d62befd](http://github.com/symfony/symfony/commit/d62befd67b0a1c86dffb4f590508199df8bef7b5 "d62befd67b0a1c86dffb4f590508199df8bef7b5 commit on github"): \[FrameworkBundle\] pharアーカイブ利用時に関するFilesystemクラスの修正
  * [69b538b](http://github.com/symfony/symfony/commit/69b538b632289782848ddc4cc96b958fd6f4b074 "69b538b632289782848ddc4cc96b958fd6f4b074 commit on github"): \[FrameworkBundle\] app:initコマンドの削除




> **NOTE**
> 翻訳者コメント<br />
> Symfony2のメーリングリストが活発になってきました。デフォルトをTwigにするかどうかなど、Symfony2をよりよいものにするために様々な議論が行われています。いいアイディアがあればぜひ開発メーリングリストに意見を出してみましょう！
> [fivestar]

