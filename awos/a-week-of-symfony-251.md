---
layout: default
title: "A week of symfony #251 (17->23 October 2011)"
---

A week of symfony #251 (17->23 October 2011)
============================================

This week, Symfony2 [added a stopwatch](https://github.com/symfony/symfony/commit/106ebdbe184b0cd9ff8f3a12232cf242b0696f58) to profile code. The first use of this stopwatch is the new [timeline panel](https://github.com/symfony/symfony/commit/842ac36f339a65e3e31fd345a01ba4002a7430ae) in the web profiler. All these new features were introduced during the last [Symfony Day 2011](http://www.symfonyday.com/en/) conference.

Development mailing list
------------------------

  * [Doctrine2 Inheritance](https://groups.google.com/forum/#!topic/symfony-devs/kJwLcRhrtmM)
  * [Chain an additional display function in Twig](https://groups.google.com/forum/#!topic/symfony-devs/GrYkFF7eo9s)

Symfony2 development highlights
-------------------------------

[Master branch](http://github.com/symfony/symfony/commits/master):

  * [97d6591](http://github.com/symfony/symfony/commit/97d6591985cb1c427b55cabb15664a882c55f532 "97d6591985cb1c427b55cabb15664a882c55f532 commit on github"): \[WebProfilerBundle\] tweaked the default layout to make more room for interesting content
  * [347053c](http://github.com/symfony/symfony/commit/347053c363aac66e79e91a3c0a205e417521c153 "347053c363aac66e79e91a3c0a205e417521c153 commit on github"): moved most of the logic from ResponseListener to the Response::prepare() method (this allows projects that only use HttpFoundation and not HttpKernel to be able to enforce the HTTP specification rules)
  * [312b20f](http://github.com/symfony/symfony/commit/312b20f94b5a2fed200908c5d41eb97917a8ba52 "312b20f94b5a2fed200908c5d41eb97917a8ba52 commit on github"): \[FrameworkBundle\] added more info to debug command output
  * [fbc422b](http://github.com/symfony/symfony/commit/fbc422b978cc2b5840c3452d21e62b1044f6e03d "fbc422b978cc2b5840c3452d21e62b1044f6e03d commit on github"): \[BrowserKit\] added the standard output when an error occurs during the request execution
  * [106ebdb](http://github.com/symfony/symfony/commit/106ebdbe184b0cd9ff8f3a12232cf242b0696f58 "106ebdbe184b0cd9ff8f3a12232cf242b0696f58 commit on github"): \[HttpKernel\] added a Stopwatch
  * [842ac36](http://github.com/symfony/symfony/commit/842ac36f339a65e3e31fd345a01ba4002a7430ae "842ac36f339a65e3e31fd345a01ba4002a7430ae commit on github"): added Stopwatch support in debug mode, added a timeline representing the stopwatch events in the web profiler
  * [c5ca40c](http://github.com/symfony/symfony/commit/c5ca40c711511c245039c4a4cafb204c4ccd46bf "c5ca40c711511c245039c4a4cafb204c4ccd46bf commit on github"): \[Routing\] added support for _scheme requirement in UrlMatcher
  * [46a69f1](http://github.com/symfony/symfony/commit/46a69f1ca004f712d39478d9c23076e03b781e88 "46a69f1ca004f712d39478d9c23076e03b781e88 commit on github"), [ad7fcf5](http://github.com/symfony/symfony/commit/ad7fcf5206cc4f1f98effcb4feaf1cc18c8f23f2 "ad7fcf5206cc4f1f98effcb4feaf1cc18c8f23f2 commit on github"): define a WarmableInterface and only warm the cache if it implements warmable to allow replacing the core router
  * [3134ef1](http://github.com/symfony/symfony/commit/3134ef132a00267a6aded6f3b0075ec2d40e51e0 "3134ef132a00267a6aded6f3b0075ec2d40e51e0 commit on github"): \[HttpKernel\] removed usage of assertCount which has been introduced in PHPUnit 3.6
  * [2e1344e](http://github.com/symfony/symfony/commit/2e1344eb7ef1e4a6c5cc21e098fd2a6404f2b289 "2e1344eb7ef1e4a6c5cc21e098fd2a6404f2b289 commit on github"): \[Routing\] added the possibility to define default values and requirements for placeholders in prefix

[2.0 branch](http://github.com/symfony/symfony/commits/2.0):

  * [e81c710](http://github.com/symfony/symfony/commit/e81c71078464d32a4537cc8dcbec6db29d44c447 "e81c71078464d32a4537cc8dcbec6db29d44c447 commit on github"), [1a43505](http://github.com/symfony/symfony/commit/1a43505a3e690394bef2ecdf75c5ce194f687a7e "1a43505a3e690394bef2ecdf75c5ce194f687a7e commit on github"): \[FrameworkBundle\] increased the priority of the profiler request listener
  * [HttpKer](http://github.com/symfony/symfony/commit/HttpKernel "HttpKernel commit on github"): check if cache_warmer service is available before doing the actual cache warmup


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfExport](http://www.symfony-project.org/plugins/sfExportPlugin): (no description)
  * [sfDoctrineTable](http://www.symfony-project.org/plugins/sfDoctrineTablePlugin): generates feature packed base tables to each model. Base table contains PHPDocs of available pre-generated WHERE, COUNT and JOIN considering table relations and its depth.
  * [sfTools](http://www.symfony-project.org/plugins/sfToolsPlugin): provides some tools and debugging functions. * sfDebugTools.class.php (dump(), dump2(), getElapsedTime()).
  * [sfDoctrineExtra](http://www.symfony-project.org/plugins/sfDoctrineExtraPlugin): includes the following behaviors: Blameable, EventLoggable, GoogleI18n, Localizable, Sortable, Taggable, Temporal.

Updated plugins
---------------

  * [sfRedis](http://www.symfony-project.org/plugins/sfRedisPlugin):
    * upgraded Predis to 0.6.6
    * deprecated commands alias in Predis
    * added option for reversing ZSET pager

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * fixed show_when stuff on linkTo* methods

  * [apostropheExtraSlots](http://www.symfony-project.org/plugins/apostropheExtraSlotsPlugin):
    * fixed bug with IE and the map JS

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * fixed a bug with the .a-normal / .a-editing class name that is toggled on areas and slots when the edit view is toggled
    * singleton slots were missing the .a-slot toggle because of the nature of the markup and the way the slot was being targeted
    * verbose logging for static file sync while we test a few things
    * fixed menuToggle issue
    * AJAX media edit form now supports CKEditor
    * a little clean up in layout for assembling the body class
    * added handy getDatabases() and databaseExists() methods in aMysql
    * aString::limitWords now supports an ellipsis option that lets you override what is appended as an ellipsis
    * added aHtml::lazyUrls, which turns likely hostnames into proper http:// URLs so that textToHtml() can pick up on them

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * disabled the save on blur behavior for the blog admin interface in old apostrophe 1.4

They talked about us
--------------------

  * [Symfony2: create a response filter and set extra response headers](http://php-and-symfony.matthiasnoback.nl/2011/10/symfony2-create-a-response-filter-and-set-extra-response-headers/)
  * [Streaming content with Symfony 1.4](http://jsltbh.blogspot.com/2011/10/streaming-content-with-symfony-14.html)
  * [How to add a custom class to form field in Symfony2](http://blog.sznapka.pl/how-to-add-a-custom-class-to-form-field-in-symfony2/)
  * [Disabling remember me in FOSUserBundle](http://sf.khepin.com/2011/10/disabling-remember-me-in-fosuserbundle/)
  * [[Symfony 2][Twig] – Enabling (native) Twig Extensions](http://nerdpress.org/2011/10/19/symfony-2-twig-enabling-native-twig-extensions/)
  * [Use DocBlox in Symfony2 for inspecting DocComment blocks](http://php-and-symfony.matthiasnoback.nl/2011/10/use-docblox-in-symfony2-for-inspecting-doccomment-blocks/)
  * [Symfony Day 2011](http://vvv.tobiassjosten.net/symfony/symfony-day-2011)
  * [Symfony2: how to create a custom Response using an event listener](http://php-and-symfony.matthiasnoback.nl/2011/10/symfony2-how-to-create-a-custom-response-using-an-event-listener/)
  * [symfony1 sfToolsPlugin 1-0-0 released](http://www.strangebuzz.com/post/2011/10/22/symfony1-sfToolsPlugin-1-0-0-released)
  * [Interfacing the PHP world](http://pooteeweet.org/blog/0/2008#m2008)
  * [Use Proxy-Object in Symfony2 applications to test non-public methods](http://blog.sznapka.pl/use-proxy-object-in-symfony2-applictions-to-test-non-public-methods/)
  * [Todas las presentaciones del Symfony Day 2011](http://www.symfony.es/2011/10/23/todas-las-presentaciones-del-symfony-day-2011/)
  * [Symfony – Telepítés](http://blog.starweb.hu/php/symfony-telepites.php)
  * [Photos from Symfony Day 2011](http://developer.e-butik.se/2011/10/photos-from-symfony-day-2011/)
  * [Symfony Day 11 Cologne](http://symfony-blog.driebit.nl/2011/10/symfony-day-11-cologne/)
  * [symfony Jobeet學習紀錄--Jobeet網站的資料模型(The Data Model)--(03/24)](http://books.bod.idv.tw/2011/10/symfony-jobeet-jobeetthe-data-model.html)
  * [Linking between applications in symfony 1.4](http://www.seattleveggieburgers.com/blog/?p=130)
  * [Symfony2 Generate Entities Starting from a Database](http://blog.aelius.fr/blog/2011/10/symfony2-generate-entities-starting-from-a-database/)
  * [Symfony 1.0 action url_for](http://mmj.99ing.net/Entry/1067/)
  * [Symfony2 – first impressions](http://www.jessehanson.com/2011/10/19/symfony2-first-impressions/)
  * [My first thoughts on Symfony2](http://www.nigeldunn.com/2011/10/20/my-first-thoughts-on-symfony2/)
  * [How to use the repeated field type in Symfony](http://blogsh.de/2011/10/19/how-to-use-the-repeated-field-type-in-symfony/)
  * [Symfony: Error Unable to load i18nHelper.php](http://comunidadcodificada.com/portal/index.php/2011/10/symfony-error-unable-to-load-i18nhelper-php/)
  * [How to Create a Page for your Website Using Symfony](http://ikesser.com/?p=15)
  * [Bloginy 3, Symfony 2, retour d’expérience](http://blog.riadbenguella.com/bloginy-3-symfony-2-retour-dexperience/)
  * [Envoi d’e-mails à partir d’un fichier batch Symfony 1.4](http://blog.aelius.fr/fr/2011/10/19/envoi-de-mails-a-partir-dun-fichier-batch-symfony-1-4/)
  * [Mon premier projet en Symfony2 PART2 – Création de la base de données et du model Doctrine2](http://clycks.fr/2011/10/495-mon-premier-projet-en-symfony2-part2-creation-de-la-base-de-donnees-du-model-doctrine2)
  * [¿Memoria agotada al intentar generar el modelo en Symfony 1.4.6 con Propel?](http://pedrobonilla.blogspot.com/2011/10/memoria-agotada-al-intentar-generar-el.html)
  * [Trimiterea de e-mail-uri dintr-un fişier batch Symfony 1.4](http://blog.aelius.fr/ro/2011/10/19/trimiterea-de-e-mail-uri-dintr-un-fisier-batch-symfony-1-4/)
  * [Silex: Le service de traduction et les templates Twig](http://www.dinduks.com/silex-le-service-de-traduction-et-les-templates-twig)
  * [Symfony Embedded Forms (take 2)](http://www.reecefowell.com/2011/10/18/symfony-embedded-forms-take-2/)
  * [Preparando LightTPD sobre Windows para Symfony](http://carlosaisa.com.es/2011/10/18/preparando-lighttpd-sobre-windows-para-symfony/)
  * [Doctrine migrations para actualizar la base de datos desde el fichero schema.yml](http://desarrolla2.com/php-symfony/doctrine-migrations-para-actualizar-la-base-de-datos-desde-el-fichero-schema-ml/)
  * [Creación de Reportes Graficos con High Charts y symfony 1.4](http://blog.datasolutions.pe/index.php/20111017/creacion-de-reportes-graficos-con-high-charts-symfony-1-4/)
  * [symfonyでDATE_FORMATを使う](http://netsket-koshiba.blogspot.com/2011/10/symfonydateformat1-doctrinequerycreate.html)
  * [Firesymfony: как сделать WebDebugToolbar еще более удобным](http://symfony.artsofte.ru/blog/post/id/13)
