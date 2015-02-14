---
layout: default
title: A week of symfony #224 (11->17 April 2011)
---

A week of symfony #224 (11->17 April 2011)
==========================================

今週は、 [新しい Symfony2 フォーム](https://github.com/symfony/symfony/tree/form) がベータとして登場し、Cookie とセッションの機能テストが追加されました。同時に、 Symfony2 ベースのマイクロフレームワークである [Silex](http://silex-project.org/) に、フォームと swiftmailer のサポートが追加され、簡単なアドミンジェネレータも含まれるようになりました。最後に、 symfony コミュニティは、[NetBeans IDE に Symfony2 のサポートをするよう依頼](http://netbeans.org/bugzilla/show_bug.cgi?id=197729) する活動を始めました。

開発メーリングリスト
------------------------

  * [\[Symfony2\] チケットの整理中](https://groups.google.com/forum/#!topic/symfony-devs/NM0OSpbJ8Lw)
  * [ルート生成での _locale の自動マージ](https://groups.google.com/forum/#!topic/symfony-devs/RfVyX5AIcVY)
  * [\[Symfony2\] 自動生成された PHP ファイルの末尾に .cache を付与する](https://groups.google.com/forum/#!topic/symfony-devs/3qgVSA60XgI)
  * [\[Symfony2\] インタフェースインジェクション](https://groups.google.com/forum/#!topic/symfony-devs/77GxWI8F8lU)
  * [\[Symfony2\] IRC ミーティング](https://groups.google.com/forum/#!topic/symfony-devs/ZIPR8RdGnTk)
  * [\[Symfony2\] 適切なパーミッションのキャッシュのための正しいワークフロー](https://groups.google.com/forum/#!topic/symfony-devs/_7AvZjdH1Iw)
  * [Symfony2 の vendors ディレクトリに PHPUnit を含めるべきか](https://groups.google.com/forum/#!topic/symfony-devs/6xuoXP8L3d0)

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [7cc51d8](http://github.com/symfony/symfony/commit/7cc51d8596ffc9c74951ec9989722b20a5509068 "7cc51d8596ffc9c74951ec9989722b20a5509068 commit on github"): \[FrameworkBundle\] テンプレートキャッシュウォーマーのリソース継承を修正
  * [27a327e](http://github.com/symfony/symfony/commit/27a327e0de1585ce4ce33706ab2f6598fc230380 "27a327e0de1585ce4ce33706ab2f6598fc230380 commit on github"), [c45d5c8](http://github.com/symfony/symfony/commit/c45d5c89cc3f5d734e6a9527b1ceb2b43303bf06 "c45d5c89cc3f5d734e6a9527b1ceb2b43303bf06 commit on github"): \[FrameworkBundle\] TemplateLocator クラスにユニットテストを追加
  * [e80a693](http://github.com/symfony/symfony/commit/e80a693cfe4e5d36e8d2a3bc042b8d556333e931 "e80a693cfe4e5d36e8d2a3bc042b8d556333e931 commit on github"): \[FrameworkBundle\] テンプレートが TemplateReferenceInterface のインスタンスであるよう強制
  * [e254ff8](http://github.com/symfony/symfony/commit/e254ff8cc65c1fb3ff60b261ffd2b260fd015ed7 "e254ff8cc65c1fb3ff60b261ffd2b260fd015ed7 commit on github"): 例外のメッセージにテンプレートの論理名を表示
  * [3e41bef](http://github.com/symfony/symfony/commit/3e41bef1e89b3e37c3114655d210fbdd44a27cf6 "3e41bef1e89b3e37c3114655d210fbdd44a27cf6 commit on github"): \[FrameworkBundle\] ルーティングパラメータの出力のされ方を修正
  * [7d61c00](http://github.com/symfony/symfony/commit/7d61c003da253cd8fce7a71b1fffb721ac229c20 "7d61c003da253cd8fce7a71b1fffb721ac229c20 commit on github"): \[FrameworkBundle\] init:bundle が / をネームスペースのセパレータとして許容するよう変更
  * [d27dc86](http://github.com/symfony/symfony/commit/d27dc86c259bfa87320f637f91d678f15777b3aa "d27dc86c259bfa87320f637f91d678f15777b3aa commit on github"): \[FrameworkBundle, Validation\] YAML バリデーションファイルを検出しないバグを修正
  * [8e6233e](http://github.com/symfony/symfony/commit/8e6233e9c253aa837f26bbd525c34266cbe9c86c "8e6233e9c253aa837f26bbd525c34266cbe9c86c commit on github"): \[Serializer\] いくつかの動作を許可するため、 XmlEncoder 内で SimpleXmlElement の代わりに DOMElement を使用するよう変更 (切り戻し)
  * [a4b04c4](http://github.com/symfony/symfony/commit/a4b04c4add7bbfbf41025e1df2b38a2d2407a591 "a4b04c4add7bbfbf41025e1df2b38a2d2407a591 commit on github"): 特別な例外の代わりにシンセティックサービスを使用するよう変更
  * [d300b94](http://github.com/symfony/symfony/commit/d300b94745d6a191dbe3ac32e54941ec3911b59c "d300b94745d6a191dbe3ac32e54941ec3911b59c commit on github"), [d39ea6a](http://github.com/symfony/symfony/commit/d39ea6ae79fa11496f9a87f38215b2b55326ed78 "d39ea6ae79fa11496f9a87f38215b2b55326ed78 commit on github"): \[Bridge, Twig\] transchoice フィルターを追加
  * [55a8f8d](http://github.com/symfony/symfony/commit/55a8f8d0980806e6a48ba7ca5434455ab6e950cb "55a8f8d0980806e6a48ba7ca5434455ab6e950cb commit on github"): 内部あるいはコア部分のページの一般的なレイアウトを抽出
  * [61dba2d](http://github.com/symfony/symfony/commit/61dba2dd34a4be4811979b86d81ca55a298f8364 "61dba2dd34a4be4811979b86d81ca55a298f8364 commit on github"): \[FrameworkBundle\] service.xml に ContainerAwareInterfaceを追加
  * [d873f21](http://github.com/symfony/symfony/commit/d873f21f69c9d4706658b4d938ad584743d44dc3 "d873f21f69c9d4706658b4d938ad584743d44dc3 commit on github"): \[FrameworkBundle\] ファイルが存在しない時の例外からリンクを削除
  * [2397bcb](http://github.com/symfony/symfony/commit/2397bcbe948b92cdbd0217254493842a38085a07 "2397bcbe948b92cdbd0217254493842a38085a07 commit on github"): \[DependencyInjection\] ロギングを改良
  * [bfb0f09](http://github.com/symfony/symfony/commit/bfb0f094f42f10e4781623a0d98c06704bb7eea1 "bfb0f094f42f10e4781623a0d98c06704bb7eea1 commit on github"): \[AsseticBundle\] バンドルノードを他のものと合うよう改修し、バリデーションを整理
  * [227c874](http://github.com/symfony/symfony/commit/227c87404f252c05c5dd5c5d03c5ff08295f93de "227c87404f252c05c5dd5c5d03c5ff08295f93de commit on github"): セッション書き込み時に行が更新されたかチェックするよう、 PDO セッションストレージを修正
  * [6722910](http://github.com/symfony/symfony/commit/672291087c67c8cf0cd173c3ea82266a606a76d9 "672291087c67c8cf0cd173c3ea82266a606a76d9 commit on github"): アトリビュートの代わりに XML の値を使用するために、多くの特別な標準化ロジックを設定から削除
  * [8193913](http://github.com/symfony/symfony/commit/81939136adf084646d35d8213bdd5864e28c15ad "81939136adf084646d35d8213bdd5864e28c15ad commit on github"): \[WebProfilerBundle\] セッションが設定されていない時のエラーを修正
  * [84dde40](http://github.com/symfony/symfony/commit/84dde4074a833d52e813405a7632f5288c69b745 "84dde4074a833d52e813405a7632f5288c69b745 commit on github"): \[HttpFoundation\] PHP のデフォルトと一致するように、Cookie の httponly 引数のデフォルト値を変更
  * [66c4bc7](http://github.com/symfony/symfony/commit/66c4bc727c9cbc0cbeaae245425742f2f5438083 "66c4bc727c9cbc0cbeaae245425742f2f5438083 commit on github"): \[HttpFoundation\] DomCrawler コンポーネントとの整合性を取るため、 Cookie::getExpire() を getExpiresTime() に名前変更
  * [e2c9fdf](http://github.com/symfony/symfony/commit/e2c9fdf2c72d80d6e758b411b4e489ed836af6a4 "e2c9fdf2c72d80d6e758b411b4e489ed836af6a4 commit on github"): \[HttpFoundation\] Cookie の有効期限を修正 (PHP は UNIX タイムスタンプを要求していた)
  * [79cfea2](http://github.com/symfony/symfony/commit/79cfea20fd39267093922e8c40b00c8d2ecacc28 "79cfea20fd39267093922e8c40b00c8d2ecacc28 commit on github"): \[WebProfilerBundle\] セッションが設定されていなくても検索フォームを表示するよう変更
  * [6957dae](http://github.com/symfony/symfony/commit/6957dae4f9f2c69c75aedfefb67952956e729b91 "6957dae4f9f2c69c75aedfefb67952956e729b91 commit on github"): \[HttpKernel\] Client で Cookie をサポートするよう追加
  * [3322cdb](http://github.com/symfony/symfony/commit/3322cdbefc254c4a0ed001ccc7fc24b5452e3bf2 "3322cdbefc254c4a0ed001ccc7fc24b5452e3bf2 commit on github"): \[FrameworkBundle\] イベントリスナーとしてスコープサービスを追加する際の問題を修正
  * [ea84bb0](http://github.com/symfony/symfony/commit/ea84bb025b4679903d31919c509638930f74318f "ea84bb025b4679903d31919c509638930f74318f commit on github"): 機能テストでのセッション管理を修正
  * [9cc340a](http://github.com/symfony/symfony/commit/9cc340a262842ef527fcf5dc973812ce659ed156 "9cc340a262842ef527fcf5dc973812ce659ed156 commit on github"): FileLocator クラスの矛盾を修正
  * [6ea9fb1](http://github.com/symfony/symfony/commit/6ea9fb16c7128b10977f5f8f13d7a8ddc81e2a25 "6ea9fb16c7128b10977f5f8f13d7a8ddc81e2a25 commit on github"): \[DependencyInjection\] リファクタリングといくつかのロギングメッセージ追加
  * [ad112da](http://github.com/symfony/symfony/commit/ad112da5bce28955298d55d3d0e0bf8b24984881 "ad112da5bce28955298d55d3d0e0bf8b24984881 commit on github"): RequestDataCollector にリクエストの中身を追加
  * [7e58c3f](http://github.com/symfony/symfony/commit/7e58c3f9768a94ab5b4989b743e5e59a2d76f75d "7e58c3f9768a94ab5b4989b743e5e59a2d76f75d commit on github"): \[Routing\] route 変数のデフォルトが null なのを許すよう修正
  * [c6818d8](http://github.com/symfony/symfony/commit/c6818d8bf75a840acce5bdf9a0968f1a4bccb6ff "c6818d8bf75a840acce5bdf9a0968f1a4bccb6ff commit on github"): \[HttpKernel\] コントローラが配列で __invoke メソッドを持つオブジェクトであるよう修正
  * [30bac46](http://github.com/symfony/symfony/commit/30bac46e1bcda1ecd4f77354b9b88832113b785a "30bac46e1bcda1ecd4f77354b9b88832113b785a commit on github"): \[DependencyInjection\] 自動生成されたコンテナのベースクラスが設定可能なように修正
  * [874c4b6](http://github.com/symfony/symfony/commit/874c4b6e07f31b6cb0af92e1ed748d485bfc52af "874c4b6e07f31b6cb0af92e1ed748d485bfc52af commit on github"): Encoder がデコードもサポートしているかどうかを簡単に判別できるように、 DecodeInterface (と SerializerAwareInterface) を追加

