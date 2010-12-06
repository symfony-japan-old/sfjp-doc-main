A week of symfony #205 (29->5 November 2010)
============================================

今週は [Symfony2 Preview Release 4](http://www.symfony-project.org/blog/2010/12/01/symfony2-pr4-released) がリリースされました。開発完了にはまだまだですが、これはフル機能バージョンですので、Symfony2の哲学を学ぶには最高の方法です。
 
開発メーリングリスト
------------------------

  * [バリデーション、アノテーション、継承](http://groups.google.com/group/symfony-devs/browse_thread/thread/037e226b31eaac7b/dc2a8723cc70c9a4)
  * [Doctrator](http://groups.google.com/group/symfony-devs/browse_thread/thread/ac74f962ed1fdad6/8c2a75165c13602a)
  * [RFC - カスタムローダーリソースの表記法](http://groups.google.com/group/symfony-devs/browse_thread/thread/3104c1a9e45799d2/20fbe393c1afe088)
  * [Facebook Connectプロバイダ](http://groups.google.com/group/symfony-devs/browse_thread/thread/50b8a825c853056e/94ca1dfcf898d5bc)
  * [RFCは意味的に異なる2種類のリダイレクトを許している](http://groups.google.com/group/symfony-devs/browse_thread/thread/2a7815dbc424979f)

symfony 1 開発ハイライト
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=05%2F12%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r31562](http://trac.symfony-project.org/changeset/31562 "31562 revision on trac"): \[YAML\] 単純なインラインドキュメントの解析を修正
  * [r31563](http://trac.symfony-project.org/changeset/31563 "31563 revision on trac"): \[YAML\] sfYaml 1.0.4をリリース

sfPropelPlugin:

  * [r31584](http://trac.symfony-project.org/changeset/31584 "31584 revision on trac"): \[1.3, 1.4\] オランダ語の翻訳欠落分を追加

Activity summary: 79 changesets, 23 bugs reported, 23 bugs fixed, 3 enhancements suggested, 5 documentation defects reported, 1 documentation defect fixed, and 25 documentation edits

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [07eceb7](http://github.com/symfony/symfony/commit/07eceb7ade737185a84f5abb55a54ee1109ecb03 "07eceb7ade737185a84f5abb55a54ee1109ecb03 commit on github"): \[TwigBundle\] セキュリティコンテキストが有効でない時のifroleタグを修正
  * [757fd80](http://github.com/symfony/symfony/commit/757fd80b9bd181c867127346f413d4f6b8181c49 "757fd80b9bd181c867127346f413d4f6b8181c49 commit on github"): RouterApacheDumperCommandのコマンドドキュメントを改善し、script_nameをオプションとして指定できる機能を追加
  * [d171df0](http://github.com/symfony/symfony/commit/d171df0c3b04ebe8ea3899d2d4b0cf6b1a76a2b6 "d171df0c3b04ebe8ea3899d2d4b0cf6b1a76a2b6 commit on github"): \[DependencyInjection\] アサーションを発生させる代わりに、例外クラスをキャッチするようテストを修正
  * [547eaa8](http://github.com/symfony/symfony/commit/547eaa81f70a8b06272d75d82da17c8ca9bdd7da "547eaa81f70a8b06272d75d82da17c8ca9bdd7da commit on github"): \[TwigBundle\] Twig_Environmentのオプション管理を修正
  * [1e9e1b3](http://github.com/symfony/symfony/commit/1e9e1b346d248b706235370de2d7bd4552e33f38 "1e9e1b346d248b706235370de2d7bd4552e33f38 commit on github"): \[Routing\] ApacheMatcherDumper、PhpMatcherDumper、UrlMatcherのテストを追加
  * [739ebf9](http://github.com/symfony/symfony/commit/739ebf92f5d5daa32806489890d0decd4e244044 "739ebf92f5d5daa32806489890d0decd4e244044 commit on github"): \[Routing\] 他のすべての必要条件と整合性が取れるように、changed the _methodのルートの必要条件を正規表現になるよう修正
  * [91c5c91](http://github.com/symfony/symfony/commit/91c5c910eb95da5c2ee5d0b67c3ed2387e29db24 "91c5c910eb95da5c2ee5d0b67c3ed2387e29db24 commit on github"): \[FrameworkBundle\] セッションが自動起動可能になる設定ができるように、auto-startとauto_startオプションを追加
  * [d10bc3e](http://github.com/symfony/symfony/commit/d10bc3e412c60ea765fc477fff0b046ddb5f8747 "d10bc3e412c60ea765fc477fff0b046ddb5f8747 commit on github"): \[FrameworkBundle\] クラスキャッシュに更にファイルを追加
  * [9c8cae2](http://github.com/symfony/symfony/commit/9c8cae24f86d1852b079a4369f6fca8c2a66f1b7 "9c8cae24f86d1852b079a4369f6fca8c2a66f1b7 commit on github"): \[Console\] InputArgumentTestにおける不正な定数参照を修正
  * [7efb463](http://github.com/symfony/symfony/commit/7efb4630b8d7c32834a4dcd4888a64f7f2fbf2c8 "7efb4630b8d7c32834a4dcd4888a64f7f2fbf2c8 commit on github"): \[Command\] 特定のオプションに割り当てられた値あるいは値がないことを参照するための定数であることを正確に表すため、InputOption::PARAMETER_*定数をInputOption::VALUE_*定数に変更
  * [7ad3eca](http://github.com/symfony/symfony/commit/7ad3eca188f7d987dc613428b228a5ff5b3940f4 "7ad3eca188f7d987dc613428b228a5ff5b3940f4 commit on github"): \[TwigBundle\] Twig Optimizerエクステンションをデフォルトで有効にするよう変更
  * [6e18a2c](http://github.com/symfony/symfony/commit/6e18a2c52930a6b3e150f18499b71b04f117ddf4 "6e18a2c52930a6b3e150f18499b71b04f117ddf4 commit on github"): \[Yaml\] 単純なインラインドキュメントの解析を修正
  * [314d3d0](http://github.com/symfony/symfony/commit/314d3d06aec646b2ac4e6ea205f30e4139251b77 "314d3d06aec646b2ac4e6ea205f30e4139251b77 commit on github"): \[DependencyInjection\] PhpDumperクラスのfindTaggedServiceIdsメソッド内のタグを整形
  * [b2eec52](http://github.com/symfony/symfony/commit/b2eec52429e15a12f4a2ef0748fade8e7933f9c3 "b2eec52429e15a12f4a2ef0748fade8e7933f9c3 commit on github"): \[Routing\] Route::setRequirement()を追加
  * [dca8a79](http://github.com/symfony/symfony/commit/dca8a79bf5cf6faca5a0a0ee74dad91c19461ec8 "dca8a79bf5cf6faca5a0a0ee74dad91c19461ec8 commit on github"): \[Routing\] アノテーションクラスローダーをより柔軟に変更
  * [73331cf](http://github.com/symfony/symfony/commit/73331cf1c13212475d509e0e58c878e19643c752 "73331cf1c13212475d509e0e58c878e19643c752 commit on github"): \[DependencyInjection\] Interface Injectionを実装
  * [794634d](http://github.com/symfony/symfony/commit/794634db7ca1a630a68d4f631d4e9421266a1a26 "794634db7ca1a630a68d4f631d4e9421266a1a26 commit on github"), [45e34c2](http://github.com/symfony/symfony/commit/45e34c29fd7e615b837aecd9f9acd865ff40f148 "45e34c29fd7e615b837aecd9f9acd865ff40f148 commit on github"): \[Routing\] より効率的になるように、PhpGeneratorDumperクラス内のmethod_existsをルート名の配列に変更

Documentation
-------------

  * <a href="http://trac.symfony-project.org/wiki/IRCLogs20101202">IRC ログ 2010 12 02</a>ページ

