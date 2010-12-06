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

New [job postings](http://trac.symfony-project.com/trac/wiki/JobPostings)
----------------

  * Symfony developers at [QP Media GmbH](http://www.qpondo.de) - full-time based in Oldenburg, Germany - Contact: jobs [at] qpmedia [dot] de

New [developers for hire](http://trac.symfony-project.com/trac/wiki/DevelopersForHire)
-----------------------

  * [Clearcode](http://clearcode.cc): is a software development company focused on providing custom software solutions for the advertising industry. We specialize in ad serving, analytics, targeting, crawling & tracking technologies. We are located in Wroclaw/Poland and speak English, German & Polish. We have been working with symfony since 2006.


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [RosfEsiSimulator](http://www.symfony-project.org/plugins/RosfEsiSimulatorPlugin): It renders components, partials or any piece of code you need to speed up, the same way as it would be if you were using Edge-Side Includes (ESI).
  * [sfSimpleAuth](http://www.symfony-project.org/plugins/sfSimpleAuthPlugin): permits to secure an application quickly, for lightweight website that just need a single account to manage it.
  * [gjPositions](http://www.symfony-project.org/plugins/gjPositionsPlugin): adds a compositioning workflow to your admin module (so called Composition Canvas) that allows the user to compose a canvas from components/partials (so called Design Elements) and manually assign any type of content (so called Content Elements) to them.
  * [sfMultipleAjaxUploadGallery](http://www.symfony-project.org/plugins/sfMultipleAjaxUploadGalleryPlugin): generates a gallery management module with an ajax multiple photo uploader.
  * [tsJQuerySuggest](http://www.symfony-project.org/plugins/tsJQuerySuggestPlugin): provides a jquery base suggest/autocompleter input.
  * [jlGMapSlot](http://www.symfony-project.org/plugins/jlGMapSlotPlugin): allows Apostrophe editors to add Google Map slots to any page. 
  * [sfRedminishAdmin](http://www.symfony-project.org/plugins/sfRedminishAdminPlugin): an admin generator with a theme based on the one provided by Redmine.

Updated plugins
---------------

  * [pmSuperfishMenu](http://www.symfony-project.org/plugins/pmSuperfishMenuPlugin):
    * improved current route matching detection to set superfish plugin selected attribute

  * [sfDoctrineRestGenerator](http://www.symfony-project.org/plugins/sfDoctrineRestGeneratorPlugin):
    * updated install documentation

  * [sfNubioAddonFunctions](http://www.symfony-project.org/plugins/sfNubioAddonFunctionsPlugin):
    * added add_include_path()

  * [sfPropel15](http://www.symfony-project.org/plugins/sfPropel15Plugin):
    * added js escaping in sfWidgetFormSchemaOptional
    * added options to new related form

  * [sfTemplating](http://www.symfony-project.org/plugins/sfTemplatingPlugin):
    * included basic install instructions in README

  * [srPageChooser](http://www.symfony-project.org/plugins/srPageChooserPlugin):
    * changed jQuery helper to a helper, because sfJqueryReloadedPlugin is no longer part of Apostrophe trunk

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * enabled variants in newly generated slot types
    * respect relative_root_url when outputting links to minified, merged stylesheets and js
    * fixed bug where the move arrows disappear when you create a new slot
    * improved the move arrow behaviors so that when you are in the middle of adding a new slot, you are not prevented from moving the existing slots amongst themselves
    * fixed the page overlay for page settings and history
    * date range for date widget was 5 yrs +/- today: increased it to 150 yrs +/-
    * moved the $this->getOption(...) to be below the parent::configure
    * added many optimizations to the media library for embedded Videos: new Select interface, autoplay functionality for YouTube and Vimeo videos, embeds are not output in the page by default

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * added ordering of categories for user category queries
    * added alphabetical ordering to post and event form


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [NombresDeBebes.co](http://www.nombresdebebes.co/): \(Spanish\) site about names
  * [quejodidavida.com](http://www.quejodidavida.com): \(Spanish\) Web 2.0 application type fmylife.com
  * [31cosas.com](http://www.31cosas.com): \(Spanish\) Web 2.0 application to create a list of goals for your life
  * [Code Avantage](http://www.codeavantage.net/): \(French\) Promo codes search engine
  * [imgzy.com](http://imgzy.com): \(English\) simple image hosting & sharing

New [symfony bloggers](http://trac.symfony-project.com/trac/wiki/SymfonyBloggers)
--------------------

  * [havvgs life](http://toni.uebernickel.info/tag/symfony) \([feed](http://toni.uebernickel.info/tag/symfony/feed/)\) \(English\)
  * [hribo - symfony blog](http://symfony-hribo.blogspot.com/) \([feed](http://symfony-hribo.blogspot.com/feeds/posts/default)\) \(English\)

They talked about us
--------------------

  * [simple mailing system with symfony - part I](http://symfony-world.blogspot.com/2010/11/simple-mailing-system-with-symfony-part.html)
  * [When developing your own symfony admin theme ? embrace templates and abolish widget formatters!](http://test.ical.ly/2010/11/29/when-developing-your-own-symfony-admin-theme-embrace-templates-and-abolish-widget-formatters/)
  * [Symfony2: Generation d’un nouveau projet](http://www.funstaff.ch/2010/11/24/symfony2-generation-dun-nouveau-projet)
  * [Form entries positioning](http://www.symfonylab.com/form-entries-positioning/)
  * [A note on symfony caching](http://www.symfonylab.com/a-note-on-symfony-caching/)
  * [Заголовок Last-Modified, Symfony и ускорение поисковой индексации](http://habrahabr.ru/blogs/symfony/109043/)
  * [fzTagPlugin 1.2.3 and sfForkedDoctrineApply 1.5.4](http://www.fizyk.net.pl/blog/fztagplugin-1-2-3-and-sfforkeddoctrineapply-1-5-4-en)
  * [gjPositionsPlugin ? Easy page composition with symfony ? Second Beta, some nice usability enhancements with the use of jQuery](http://test.ical.ly/2010/11/30/gjpositionsplugin-easy-page-composition-with-symfony-second-beta-some-nice-usability-enhancements-with-the-use-of-jquery/)
  * [Niente calendario dell’avvento per il 2010](http://www.symfony.it/articoli/381/niente-calendario-dellavvento-per-il-2010/)
  * [New Documentation Chapter: Propel Active Record reference](http://propel.posterous.com/new-documentation-chapter-propel-active-recor)
  * [Beware! symfony form validator schemas and embedded forms can be out of sync ? Updating sfDoctrineDynamicFormRelationsPlugin](http://test.ical.ly/2010/12/01/beware-symfony-form-validator-schemas-and-embedded-forms-can-be-out-of-sync-updating-sfdoctrinedynamicformrelationsplugin/)
  * [Se publica Symfony2 PR4](http://www.symfony.es/2010/12/01/se-publica-symfony2-pr4/)
  * [Configuration YAML : Attention !](http://romain.cambien.net/configuration-yaml-attention)
  * [Symfony2 - Preview Release 4](http://www.fizyk.net.pl/blog/symfony2-preview-release-4-pl)
  * [Prze??czanie kontekstow aplikacji. Usuwanie cache’u dla innego kontekstu.](http://tworzenie-web.pl/2010/12/02/przelaczanie-kontekstow/)
  * [Fine supporto symfony 1.3](http://www.symfony.it/articoli/384/fine-supporto-symfony-1-3/)
  * [PHP Content Repository: Full implementation in sight](http://blog.liip.ch/archive/2010/12/03/php-content-repository-full-implementation-in-sight.html)
  * [Custom validator and fields in Symfony2](http://blog.bearwoods.dk/custom-validator-and-fields-in-symfony2)
  * [Symfony2: Adding a event listener](http://blog.bearwoods.dk/symfony2-adding-a-event-listener)
  * [Your feedback is important: Symfony2 PR4](http://www.jnieto.org/article/your_feedback_is_important_symfony2_pr4)
  * [Выпущен Symfony2 PR4, возможно, последний preview release перед beta](http://habrahabr.ru/blogs/symfony/109212/)
  * [symfony referer redirect](http://www.symfonylab.com/symfony-referer-redirect/)
  * [[rb]Debug a symfony object](http://insightmed.eu/blog/programming-scripting/rbdebug-a-symfony-object_2010_12.html)
  * [Wampserver & Symfony](http://drmsite.blogspot.com/2010/12/wampserver-symfony.html)
  * [symfonyでデータベースの接続情報を扱う](http://d.hatena.ne.jp/yuchimiri/20101204/p1)
  * [Symfony2で強制的にhello worldと表示するバンドルを作った話](http://sideport.g.hatena.ne.jp/anatoo/20101204/1291420969)
  * [Les aperos sont-ils aux conferences ce que les tweets sont aux billets de blog?](http://blog.cibul.org/les-aperos-sont-aux-conferences-ce-que-les-tweets-sont-aux-billets-de-blog/)
  * [Symfony - Returning an array from app.yml](http://codjng.blogspot.com/2010/12/symfony-returning-array-from-appyml.html)
  * [Symfony 2.0 PR4 Released](http://www.apperbase.com/2010/12/symfony-2-0-pr4-released/)
  * [Sortie de Symfony 2 PR4, la derniere avant la Beta](http://dev.neowebmag.com/php/sortie-de-symfony-2-pr4-la-derniere-avant-la-beta)
  * [os x に OpenPNE 3.4.9 をインストール](http://www.yokada.net/blog/1981)
  * [Symfony CMS frameworks comparation](http://www.symfony.pe/?p=42)
  * [Post validators en symfony](http://blog.solucionex.com/symfony/post-validators-en-symfony)
  * [Symfony 2 “from scratch” bootstrappen](http://nerdpress.org/2010/12/01/symfony-2-from-scratch-bootstrappen/)
  * [Symfony　すごい！！としか言いようがない](http://d.hatena.ne.jp/staro0519/20101201/1291182244)
  * [Symfony 生のSQL実行 あとおまけ](http://blog.cypher-works.com/?p=1285)
  * [Symfony Doctrine Migrations](http://gpupo.com/symfony-doctrine-migrations)
  * [symfonyでlogやcacheを別フォルダに保存する](http://blog.makotokw.com/2010/11/30/symfony%E3%81%A7log%E3%82%84cache%E3%82%92%E5%88%A5%E3%83%95%E3%82%A9%E3%83%AB%E3%83%80%E3%81%AB%E4%BF%9D%E5%AD%98%E3%81%99%E3%82%8B/)
  * [symfony 1.4 Embedded form & Ajax ашигласан жишээ . /Санал асуулга бэлдэх/-2 ](http://blog.okta.mn/show/328)
  * [symfony をやってみよう　その５](http://d.hatena.ne.jp/creativeability/20101129/1291042021)
