A week of symfony #213 (24->30 January 2011)
============================================

Symfony2 achieved this week a remarkable milestone: more than 500 pull requests have been submitted by tens of developers around the world. In addition, Symfony2 added some cool new features, such as a [cache warmer](http://github.com/symfony/symfony/commit/d0b4bfc8f61becce7cb31a3435bf31ad60e0dd62) to improve performance, [definition inheritance support for DIC](https://github.com/fabpot/symfony/commit/803dd58002b7bb80d90a1cc09ee3112c05e58c5e) and a complete [refactorization of the CSRF protection](https://github.com/symfony/symfony/commit/7848a7ca6383dce22584c96b3acd38af6d190be5). Lastly, [three new sessions](http://www.symfony-project.org/blog/2011/01/28/symfony-live-conferences-updates) were unveiled for the [Symfony Live conferences](http://www.symfony-live.com/).
 
Development mailing list
------------------------

  * [Improving the event management](https://groups.google.com/forum/#!topic/symfony-devs/dG4MTWMlSCE)
  * [Symfohub - GitHub-based symfony repositories catalog](https://groups.google.com/forum/#!topic/symfony-devs/KvlXC78RNrw)
  * [\[RFC\] New Event container.dumped](https://groups.google.com/forum/#!topic/symfony-devs/y234jr82wAQ)
  * [\[Symfony2\] \[RFC\] EventDispatcher method signature changes](https://groups.google.com/forum/#!topic/symfony-devs/CinP69ZdYUY)
  * [\[Symfony2\] RFC: Supporting Doctrine2 in Form/Validator](https://groups.google.com/forum/#!topic/symfony-devs/tuzlF70WlNk)
  * [Proposed removal of DI extension-consumed parameters from DI extension resources](https://groups.google.com/forum/#!topic/symfony-devs/_RSKT2VAuCE)
  * [\[Symfony2\] Problems with the design of DI extensions](https://groups.google.com/forum/#!topic/symfony-devs/FE-EaSViqF8)
  * [\[Symfony2\] Third-party dependencies in Components](https://groups.google.com/forum/#!topic/symfony-devs/7wNhSRpBeIo)
  * [False positive for sfValidatorEmail](https://groups.google.com/forum/#!topic/symfony-devs/3uY45yQcqm8)
  * [\[RFC\] Allow multiple extensions with same name (Alias + Method = Unique Key)](https://groups.google.com/forum/#!topic/symfony-devs/ITIfeCKV8Jc)
  * [\[RFC\] Argument mapping in service definitions](https://groups.google.com/forum/#!topic/symfony-devs/iOZNf0Vymsk)

symfony 1 development highlights
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=30%2F01%2F2011&amp;daysback=6&amp;milestone=on&amp;ticket=on&amp;changeset=on&amp;update=Update):

  * [r31890](http://trac.symfony-project.org/changeset/31890 "31890 revision on trac"), [r31893](http://trac.symfony-project.org/changeset/31893 "31893 revision on trac"): \[1.3, 1.4\] fixed sfDomCssSelector on class names with hyphens
  * [r31895](http://trac.symfony-project.org/changeset/31895 "31895 revision on trac"): \[1.3, 1.4\] fixed _auto_link_urls() does not pick up URLs with complex fragments (as per RFC3986)
  * [r31927](http://trac.symfony-project.org/changeset/31927 "31927 revision on trac"): \[1.3, 1.4\] fixed "expired" tests
  * [r31928](http://trac.symfony-project.org/changeset/31928 "31928 revision on trac"): \[1.3, 1.4\] copied more values into a cachable partial's cloned response when the partial is marked as contextual in cache.yml

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [9310eea](http://github.com/symfony/symfony/commit/9310eea57abfadbbbfb5d31db97341ee77788927 "9310eea57abfadbbbfb5d31db97341ee77788927 commit on github"): optimized templating layer (you must now explicitly register the templating engine you want to use)
  * [1c11d81](http://github.com/symfony/symfony/commit/1c11d816119814f17b30cb5b717a5bd9d3631356 "1c11d816119814f17b30cb5b717a5bd9d3631356 commit on github"): made all event listeners lazy loaded (the register() method on all listeners has been removed and instead, the information is now put directly in the DIC tag)
  * [0144dd8](http://github.com/symfony/symfony/commit/0144dd86da764105105525dd53c21774d0e75c71 "0144dd86da764105105525dd53c21774d0e75c71 commit on github"): added synthetic attribute to definitions (this attribute can be used to hint that the service is being injected dynamically at runtime, and not constructed by the DIC)
  * [49793c2](http://github.com/symfony/symfony/commit/49793c22d489cc86f2df0f6e9ab263f0c653212c "49793c22d489cc86f2df0f6e9ab263f0c653212c commit on github"): fixed event dispatcher
  * [ca8c790](http://github.com/symfony/symfony/commit/ca8c7907e238d5240696383d09ee88d2318c2760 "ca8c7907e238d5240696383d09ee88d2318c2760 commit on github"): \[Routing\] added setContext() method to both matchers and generators
  * [d0b4bfc](http://github.com/symfony/symfony/commit/d0b4bfc8f61becce7cb31a3435bf31ad60e0dd62 "d0b4bfc8f61becce7cb31a3435bf31ad60e0dd62 commit on github"): added a cache warmer sub-framework
  * [206b49a](http://github.com/symfony/symfony/commit/206b49a22f1e9c0564bdc2dd74de81d563eac1b8 "206b49a22f1e9c0564bdc2dd74de81d563eac1b8 commit on github"), [2860c26](http://github.com/symfony/symfony/commit/2860c2651c30256b9f093f9781c45366bffe1061 "2860c2651c30256b9f093f9781c45366bffe1061 commit on github"), [2499ac4](http://github.com/symfony/symfony/commit/2499ac4d218f8458cbc7c7e490b77e72a7df3858 "2499ac4d218f8458cbc7c7e490b77e72a7df3858 commit on github"), [03e51cc](http://github.com/symfony/symfony/commit/03e51cc1e2a54f6089bdf9bfeb1d915b4e4a8d21 "03e51cc1e2a54f6089bdf9bfeb1d915b4e4a8d21 commit on github"): \[FrameworkBundle\] added a cache warmer to pre-compute template paths
  * [8f6e8a4](http://github.com/symfony/symfony/commit/8f6e8a4691deb537e14474b901397276aaabf2c8 "8f6e8a4691deb537e14474b901397276aaabf2c8 commit on github"): \[TwigBundle\] added a cache warmer to generate all Twig templates cache
  * [edb11ad](http://github.com/symfony/symfony/commit/edb11ad5cbe9ffe2a00dc611864505e23de45bc1 "edb11ad5cbe9ffe2a00dc611864505e23de45bc1 commit on github"): \[FrameworkBundle\] added a cache warmer for the router
  * [14e4b97](http://github.com/symfony/symfony/commit/14e4b9733d75763774f2898b75b9d88b6f54e4df "14e4b9733d75763774f2898b75b9d88b6f54e4df commit on github"): \[HttpFoundation\] fixed FileBag to handle sub-requests
  * [2bc6197](http://github.com/symfony/symfony/commit/2bc6197859ffa43ca9793fec44f2a84198ad220e "2bc6197859ffa43ca9793fec44f2a84198ad220e commit on github"): \[DoctrineBundle\] fixed bug in Auto Proxy Generation introduced with config merge refactoring
  * [f29a5f7](http://github.com/symfony/symfony/commit/f29a5f74a11cfc1b50a4a79d06f45bcfe5655bea "f29a5f74a11cfc1b50a4a79d06f45bcfe5655bea commit on github"): made the DI config validation more strict to catch errors early
  * [79dce16](http://github.com/symfony/symfony/commit/79dce161dd2a74a38dbd2ca2521c02c45c15458d "79dce161dd2a74a38dbd2ca2521c02c45c15458d commit on github"): made a performance optimization (requires the modification of autoload.php file)
  * [561a3e4](http://github.com/symfony/symfony/commit/561a3e47b394ae4c25146f405e57cc70c0574ff0 "561a3e47b394ae4c25146f405e57cc70c0574ff0 commit on github"): \[HttpKernel\] made another speed optimization
  * [4d4eec6](http://github.com/symfony/symfony/commit/4d4eec618c003c87330fe0263a2ca8c358bbc214 "4d4eec618c003c87330fe0263a2ca8c358bbc214 commit on github"), [18c611a](http://github.com/symfony/symfony/commit/18c611a29e60846743d2a1078f08f59b473196a0 "18c611a29e60846743d2a1078f08f59b473196a0 commit on github"), [3eadf73](http://github.com/symfony/symfony/commit/3eadf73cbdf463522835b71618f2c63e02ae93d9 "3eadf73cbdf463522835b71618f2c63e02ae93d9 commit on github"): \[DoctrineBundle\] implemented Proxy CacheWarmer
  * [6f5c2e2](http://github.com/symfony/symfony/commit/6f5c2e2d8baeb7ce3653af56ecad3f1ee28be812 "6f5c2e2d8baeb7ce3653af56ecad3f1ee28be812 commit on github"): \[Serializer\] abstract classes now implement their respective interfaces
  * [08f8b22](http://github.com/symfony/symfony/commit/08f8b223ff4d7e05248e0f83b17a306c5c10fe50 "08f8b223ff4d7e05248e0f83b17a306c5c10fe50 commit on github"): \[Serializer\] added hasEncoder and getEncoder to the SerializerInterface
  * [d341e8b](http://github.com/symfony/symfony/commit/d341e8bccb7b9d3f72659c07b95c436f41f4fc32 "d341e8bccb7b9d3f72659c07b95c436f41f4fc32 commit on github"): \[Form\] adding PHPDoc to many Field objects; added empty_value option on CountryField, LanguageField, LocaleField, and TimezoneField; dded missing date_pattern to DateTimeField; made the currency option on MoneyField required
  * [7848a7c](http://github.com/symfony/symfony/commit/7848a7ca6383dce22584c96b3acd38af6d190be5 "7848a7ca6383dce22584c96b3acd38af6d190be5 commit on github"): \[Form\] refactored CSRF implementation to be reusable and to work correctly with the session service
  * [0239d62](http://github.com/symfony/symfony/commit/0239d62619f253c5e0eb14b5e059c014d734184b "0239d62619f253c5e0eb14b5e059c014d734184b commit on github"): \[Form\] made the CSRF provider service public so that it can be used without forms
  * [d017970](http://github.com/symfony/symfony/commit/d0179708672b829dbb28603e0fb2691ffb7f27ae "d0179708672b829dbb28603e0fb2691ffb7f27ae commit on github"): \[Form\] implemented FormFactory::buildDefault() to ease the use of the new CSRF implementation without the DIC
  * [0e66e38](http://github.com/symfony/symfony/commit/0e66e388ecd7f838d1de89edb80ea1dfddb8ca0a "0e66e388ecd7f838d1de89edb80ea1dfddb8ca0a commit on github"): added two interfaces: EventInterface and EventDispatcherInterface
  * [6bbfffb](http://github.com/symfony/symfony/commit/6bbfffb981d095ff813ecd3ff704607bcc01a70f "6bbfffb981d095ff813ecd3ff704607bcc01a70f commit on github"): added path, and domain to clearCookie() in accordance with RFC 2109, and RFC 2965
  * [40dec88](http://github.com/symfony/symfony/commit/40dec8831f5e5aa4e38de5625161b8b5c27ec911 "40dec8831f5e5aa4e38de5625161b8b5c27ec911 commit on github"): added helper method to normalize keys
  * [fb4e7fb](http://github.com/symfony/symfony/commit/fb4e7fb5c5b4a24cab982bc1ab8a4e59d2b5bc09 "fb4e7fb5c5b4a24cab982bc1ab8a4e59d2b5bc09 commit on github"), [36dcce4](http://github.com/symfony/symfony/commit/36dcce40ebd9a7bea206435625052fe7c4693878 "36dcce40ebd9a7bea206435625052fe7c4693878 commit on github"): added KernelInterface
  * [8b62df7](http://github.com/symfony/symfony/commit/8b62df7247c25c9b25697ad7f228f18d31707387 "8b62df7247c25c9b25697ad7f228f18d31707387 commit on github"): changed the EventDispatcher and Event interfaces (the three notification methods do not return the Event instance anymore: notify() does not return anything, notifyUntil() returns the returned value of the event that has processed the event, filter() returns the filtered value)
  * [db2f2b1](http://github.com/symfony/symfony/commit/db2f2b1315b07e76e502c30b91a6086aba5ff991 "db2f2b1315b07e76e502c30b91a6086aba5ff991 commit on github"): refactored template name parser to occur independently of the loaders

Documentation
-------------

  * New <a href="http://trac.symfony-project.org/wiki/IRCLogs20110127">IRC Logs 2011-01-27</a> page


New [developers for hire](http://trac.symfony-project.com/trac/wiki/DevelopersForHire)
-----------------------

  * [Webfit](http://webfit.co.nz): is an Auckland, New Zealand web development studio with extensive experience in Symfony application development. We specalise in ecommerce websites, web applications and business process automation.


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [icfbAutocomplete](http://www.symfony-project.org/plugins/icfbAutocompletePlugin): provides symfony wiget for facebook style autocomplete which can be used in various of situations like sending messages.
  * [sfGooglePropelLogin](http://www.symfony-project.org/plugins/sfGooglePropelLoginPlugin): allows a simple login via Google Accounts using OpenID.
  * [buMixpanel](http://www.symfony-project.org/plugins/buMixpanelPlugin): aims to provide an easy to use integration of mixpanel into your project.
  * [assetPackages](http://www.symfony-project.org/plugins/assetPackagesPlugin): provides you the ability to group stylesheet and javascript calls into packages that you can easily organise through a simple yaml config file, with a simple dependency system.
  * [sfGenerateLibFiles](http://www.symfony-project.org/plugins/sfGenerateLibFilesPlugin): allows you to create model files with a visual tool.
  * [drKint](http://www.symfony-project.org/plugins/drKintPlugin): basic integration of Kint (http://code.google.com/p/kint/)
  * [apostropheExtraSlots](http://www.symfony-project.org/plugins/apostropheExtraSlotsPlugin): extra functionality for Apostrophe in the form of new and alternative slot types.
  * [lbCart](http://www.symfony-project.org/plugins/lbCartPlugin): more than a simple commercial cart, the "cart" of lbCartPlugin will receive any object with behavior (actAs) Cartable. Thus, it can be used for the user to reference contacts, books, movies, and any object present on the site, whether commercial or not.
  * [sfDoctrineActAsSluggableAttachment](http://www.symfony-project.org/plugins/sfDoctrineActAsSluggableAttachmentPlugin): lets you bind an uploaded file to a model and rename the file into a slug version. It also handles thumbnailing of images.

Updated plugins
---------------

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * generated excels now are 'fitted to page' when printing
    * generated excels now are horizontally centered when printing
    * the title of the 'filter form' in every module have been changed to "Show/Hide filters"
    * added CustomEditSuccess templates

  * [sfPinba](http://www.symfony-project.org/plugins/sfPinbaPlugin):
    * refactoring &amp; added sfPinbaScriptNameFilter
    * added propel 1.5 logger
    * return 'other' by default in operation
    * fixed Oracle dsn parsing

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * added check to not add empty fieldsets to the formPanel
    * fixed a bug where one to one related tables with the same column name were overriding the main table columns

  * [sfAlyssaDoctrineObjectPath](http://www.symfony-project.org/plugins/sfAlyssaDoctrineObjectPathPlugin):
    * added missing where property path
    * improved documentation

  * [sfDataSource](http://www.symfony-project.org/plugins/sfDataSourcePlugin):
    * implemented filter feature with doctrine datasource
    * updated filter method in DataSourceArray

  * [sfGrid](http://www.symfony-project.org/plugins/sfGridPlugin):
    * implemented basic processing of filtering data

  * [sfAlyssaJqGrid](http://www.symfony-project.org/plugins/sfAlyssaJqGridPlugin):
    * implemented filtering feature

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * removed a call to stripslashes() on the output of json_encode

  * [crBarcode](http://www.symfony-project.org/plugins/crBarcodePlugin):
    * fixed imagewidth and imageheight warning

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * added dcWidgetFormJQueryActivator
    * fixed 'evaluate_method_extra_params'

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * to be sufficiently unique the crc used as an id for the email obfuscation must be based on the username, the domain and the label
    * allowed the transition duration to be set as a slideshow option (it still defaults to 300ms)
    * removed obsolete columns from apostrophe:migrate
    * fixed a bug with Crop when aspect width and height are used
    * it is now possible to easily override the way the name of a group is displayed in page settings
    * updated the javascript to use .find() when traversing down, and .closest() when traversing up, so that it is both more flexible and more specific
    * created a filters icon because it was missing
    * updated 'filters' button to have the same treatment as the 'linked accounts' button
    * added the css-colors-report task. This task generates a visual report of all CSS colors used in apostrophePlugin/web/css and web/css CSS files
    * lots of fixes to apostrophe:migrate-data-from-pkcontextcms and apostrophe:migrate
    * fixed a bug in the button slot where you ccouldn't set the "tool" for the richtext
    * check formatOnly, then PDF support, not the other way round for performance boost

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * migrate a_blog_category_user relationships to the new a_category_user table
    * migrate a_blog_category_group if it exists
    * made blog category migration more tolerant of things like bad foreign keys on the old tables
    * apostrophe:migrate now ensures that all blog items' virtual pages have the same categories and tags as the blog items

  * [apostropheExtraSlots](http://www.symfony-project.org/plugins/apostropheExtraSlotsPlugin):
    * created the first Extra Slot: the inset image slot lets text wrap around it

They talked about us
--------------------

  * [Redpill Linpro And Varnish Software, Gold Sponsors Of Symfony Live (Paris) 2011](http://eatmymonkeydust.com/2011/01/redpill-linpro-and-varnish-software-gold-sponsors-of-symfony-live-paris-2011/)
  * [Desarrollo basado en el comportamiento con Symfony](http://www.symfony.es/2011/01/24/desarrollo-basado-en-el-comportamiento-con-symfony/)
  * [ValidatorEmailList : valider une liste d’e-mails](http://www.symfonic.fr/2011/01/validatoremaillist-valider-une-liste-de-mails/)
  * [How to test UTF-8 email subject lines in Symfony](http://www.whiteoctober.co.uk/blog/2011/01/25/how-to-test-utf-8-email-subject-lines-in-symfony/)
  * [InfoWorld review: Fabulous PHP frameworks](http://www.networkworld.com/reviews/2011/012611-infoworld-review-fabulous-php.html)
  * [Fabulous PHP frameworks: Symfony](http://www.networkworld.com/reviews/2011/012611-fabulous-php-frameworks.html)
  * [Gérer vos cron avec Symfony grâce à sfDoctrineCronManagerPlugin](http://www.lafermeduweb.net/billet/gerer-vos-cron-avec-symfony-grace-a-sfdoctrinecronmanagerplugin-1033.html)
  * [Symfohub = symfony + GitHub](http://habrahabr.ru/blogs/symfony/112653/)
  * [sfPropel16Plugin Is Already There, Didn't You Know?](http://propel.posterous.com/sfpropel16plugin-is-already-there-didnt-you-k)
  * [Symfony2 : écrire un Helper de vue en 5 étapes](http://www.elao.org/developpement/symfony2-ecrire-un-helper-de-vue-en-5-etapes.html)
  * [Getting an extra ‘Invalid’ or other error on your symfony form?](http://shout.setfive.com/2011/01/27/getting-an-extra-invalid-or-other-error-on-your-symfony-form/)
  * [Easily override i.e. article headlines on a homepage using gjPositionsPlugin](http://test.ical.ly/2011/01/28/easily-override-i-e-article-headlines-on-a-homepage-using-gjpositionsplugin/)
  * [Novedades en el desarrollo de Symfony2](http://www.symfony.es/2011/01/28/novedades-en-el-desarrollo-de-symfony2/)
  * [Type and boolean columns with Doctrine and Symfony](http://www.jnieto.org/article/type_and_boolean_columns_with_doctrine_and_symfony)
  * [File uploader. Reload](http://www.symfonylab.com/file-uploader-reload/)
  * [Charger des fixtures au format YML](http://kromack.com/developpement-php/symfony/charger-des-fixtures-au-format-yml/)
  * [Tạo trang web tìm việc bằng Symfony framework](http://chaudanghuy.blogspot.com/2011/01/tao-trang-web-tim-viec-bang-symfony.html)
  * [Symfony: doctrine raw sql, get alphabet from i18n model](http://vit228.blogspot.com/2011/01/symfony-doctrine-raw-sql-get-alphabet.html)
  * [在symfony1.4中使用utf-8](http://www.willsonchen.com/archives/324)
  * [Form Validator usando dois campos](http://dicas-symfony.blogspot.com/2011/01/form-validator-usando-dois-campos.html)
  * [Configuración .htaccess Symfony y WordPress](http://hotdesign.com.ar/blog/2011/01/configuracion-htaccess-symfony-y-wordpress/)
  * [[PHP] さくらインターネットでセッションが使用できなくなっていた件](http://nplll.com/archives/2011/01/php_7.php)
  * [Getting the best out of Symfony](http://www.23pixels.com/web-2-property/getting-the-best-out-of-symfony/)
  * [Web デベロッパーが知っておくべき、15種類の オープンソース･プロジェクト](http://agilecat.wordpress.com/2011/01/27/web-%E3%83%87%E3%83%99%E3%83%AD%E3%83%83%E3%83%91%E3%83%BC%E3%81%8C%E7%9F%A5%E3%81%A3%E3%81%A6%E3%81%8A%E3%81%8F%E3%81%B9%E3%81%8D%E3%80%8115%E7%A8%AE%E9%A1%9E%E3%81%AE-%E3%82%AA%E3%83%BC%E3%83%97/)
  * [Sencillez de PHP, rapidez y versatilidad de Symfony](http://wi7max.wordpress.com/2011/01/26/sencillez-de-php-rapidez-y-versatilidad-de-symfony/)
  * [Você conhece o Symfony (PHP) Framework?](http://blog.tiagopassos.com/2011/01/26/voce-conhece-o-symfony-php-framework/)
  * [Plugin d’intégration Symfony pour Eclipse](http://www.pompeleup.com/2011/01/25/plugin-dintegration-symfony-pour-eclipse/)
  * [Symfonyのmigrate機能](http://sand-clock.heteml.jp/blog/?p=78)
  * [Dependecy Injection: Kontenery Dependency Injection](http://rekurencja.pl/php/symfony2/kontenery-dependency-injection.html)
  * [Symfony2 : petite séance de prise en main](http://www.spackydev.net/2011/01/25/symfony2-petite-seance-de-prise-en-main/)
  * [III Jornadas Nacionales del Informático 2011](http://boloquizhpeblog.blogspot.com/2011/01/iii-jornadas-nacionales-del-informatico.html)
  * [Sencillez de PHP y Versatilidad de Synfony](http://gramaticasformales.wordpress.com/2011/01/24/sencillez-de-php-y-versatilidad-de-synfony/)
  * [独自Viewクラスを設定する](http://d.hatena.ne.jp/moroto1122/20110124/1295865091)
  * [Symfony2 GraphvizでDIコンテナをグラフィカルに表示](http://blog.stripejam.jp/archives/465)
  * [How to create a command (task) in Symfony 2](http://razvantudorica.wordpress.com/2011/01/30/how-to-create-a-command-task-in-symfony-2/)
  * [sfSagePayPlugin – a work in progress](http://www.richsage.co.uk/2011/01/30/sfsagepayplugin-a-work-in-progress/)