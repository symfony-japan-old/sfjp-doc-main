A week of symfony #217 (21->27 February 2011)
=============================================

The public API of Symfony2 will be freezed in just a few days. Therefore, this week developers committed some of the last big impact changes to the code repository: the Response was [removed from DIC](https://github.com/symfony/symfony/commit/d94acd85f9aee2342c7ec381d7fdd66aea1eafef), CompatAssetsBundle was removed [in favor of AsseticBundle](https://github.com/symfony/symfony/commit/a3207e939f4f4de24a740ce56b04483eb46e4074), and the [boostrap files](https://github.com/symfony/symfony/commit/b44d044b0afe218594d9ed7965eaeb272576bf80) were also removed.
Several other changes were proposed in the developers mailing list, such as [using keys for translations](https://groups.google.com/forum/#!topic/symfony-devs/n3HznxzQW8A) and [adding DI to Forms](https://groups.google.com/forum/#!topic/symfony-devs/WHiSVfrno74). Lastly, [Symfony2 documentation](http://docs.symfony-reloaded.org/) was profoundly reorganized and vastly expanded with new and improved contents.
 
Development mailing list
------------------------

  * [\[Symfony2\] removing the Response service](https://groups.google.com/forum/#!topic/symfony-devs/hQWgf96uVT0)
  * [Coupling of the email provider](https://groups.google.com/forum/#!topic/symfony-devs/cntxm3w4tSg)
  * [\[Symfony2\] RFC - Changing translation sources to message keys](https://groups.google.com/forum/#!topic/symfony-devs/n3HznxzQW8A)
  * [Flash messages in development mode](https://groups.google.com/forum/#!topic/symfony-devs/jrjyzeaBFMA)
  * [\[Symfony2\] RFC: Adding DI to Forms - experimental refactoring](https://groups.google.com/forum/#!topic/symfony-devs/WHiSVfrno74)
  * [Optional placeholders in routing](https://groups.google.com/forum/#!topic/symfony-devs/UVkncjTnJKQ)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [9b16f1a](http://github.com/symfony/symfony/commit/9b16f1a61428427d1e54c5ed214dacda185d593b "9b16f1a61428427d1e54c5ed214dacda185d593b commit on github"): \[SwiftMailer\] added the SendEmail Command (for the spool)
  * [f985da5](http://github.com/symfony/symfony/commit/f985da5a9c7968cbd15acf87a1379959b30a14af "f985da5a9c7968cbd15acf87a1379959b30a14af commit on github"): \[HttpFoundation\] fixed Cache-Control header when forcing the Response to have an Expires header field
  * <del>[f5b1cb1](http://github.com/symfony/symfony/commit/f5b1cb18e101115d3995f6ce2dd8597672cca058 "f5b1cb18e101115d3995f6ce2dd8597672cca058 commit on github"), [e7c098e](http://github.com/symfony/symfony/commit/e7c098e8a2ddce9e4faa761803c5b08d93dd5bdf "e7c098e8a2ddce9e4faa761803c5b08d93dd5bdf commit on github"): \[DependencyInjection\] initial implementation of an allowUnnamedChildren method on NodeBuilder. Also added an extra field exception</del> (reverted)
  * [bd15ddd](http://github.com/symfony/symfony/commit/bd15ddda96e02ab2144350105adf49e1fdd66c2f "bd15ddda96e02ab2144350105adf49e1fdd66c2f commit on github"), [554628c](http://github.com/symfony/symfony/commit/554628cf5b315a55b8814cae0b338c56245adfe7 "554628cf5b315a55b8814cae0b338c56245adfe7 commit on github"), [d6617f6](http://github.com/symfony/symfony/commit/d6617f6fba9f09d38e152341d8921d3844675fd9 "d6617f6fba9f09d38e152341d8921d3844675fd9 commit on github"): \[DependencyInjection\] added a NodeBuilder::addNodeBuilder() method that helps achieve a fluid interface when a pre-built NodeBuilder needs to be added
  * [fd5cdfc](http://github.com/symfony/symfony/commit/fd5cdfc18f118d8331583f053004e46290631109 "fd5cdfc18f118d8331583f053004e46290631109 commit on github"): \[DependencyInjection\] assured to remove XML-remapped singular options and key attribute options after processing
  * [ea768fe](http://github.com/symfony/symfony/commit/ea768fe6fcfb094b2dad2e006a3411165019bf59 "ea768fe6fcfb094b2dad2e006a3411165019bf59 commit on github"), [48459e9](http://github.com/symfony/symfony/commit/48459e9082e9477ca783ae920388671363e09761 "48459e9082e9477ca783ae920388671363e09761 commit on github"): \[Config\] made the option to remove a key attribute optional
  * [f0d2ce7](http://github.com/symfony/symfony/commit/f0d2ce7f322d47ccb98d7f9b1f1b66a9d8877d5b "f0d2ce7f322d47ccb98d7f9b1f1b66a9d8877d5b commit on github"): \[TwigBundle\] refactored TwigExtension class and implemented configuration tree
  * [026ab6c](http://github.com/symfony/symfony/commit/026ab6c6cedf23475670718ed55e5b03a550c6a1 "026ab6c6cedf23475670718ed55e5b03a550c6a1 commit on github"): \[Config\] added an ignoreExtraKeys options, which allows you to let options simply be ignore without throwing a validation exception
  * [c9406b6](http://github.com/symfony/symfony/commit/c9406b62b29874aa3d6dc818dc065822c2f0edf4 "c9406b62b29874aa3d6dc818dc065822c2f0edf4 commit on github"): \[SecurityBundle\] allowed the main Configuration tree to allow factories without a validation exception
  * [dff3585](http://github.com/symfony/symfony/commit/dff35851626f62509adff86c85382bfe5cc4979a "dff35851626f62509adff86c85382bfe5cc4979a commit on github"): fixed profiler when using ESI in dev env
  * [d2684f3](http://github.com/symfony/symfony/commit/d2684f3f7345ce35f740b4c72454cab313690d06 "d2684f3f7345ce35f740b4c72454cab313690d06 commit on github"): \[AsseticBundle\] converted to use a Configuration class
  * [c01be42](http://github.com/symfony/symfony/commit/c01be42933969fc6d9264685ddb105308051a147 "c01be42933969fc6d9264685ddb105308051a147 commit on github"): \[AsseticBundle\] made the filter manager lazy
  * [4ba0e0d](http://github.com/symfony/symfony/commit/4ba0e0d5cf311a91645ffa200137332d07751ef8 "4ba0e0d5cf311a91645ffa200137332d07751ef8 commit on github"): \[AsseticBundle\] fixed bundle notation of inputs
  * [9b15b69](http://github.com/symfony/symfony/commit/9b15b6950cfed5e613393a4b5aea14189b21f381 "9b15b6950cfed5e613393a4b5aea14189b21f381 commit on github"): \[AsseticBundle\] sort Twig assets by name before loading for filesystem-independent results
  * [f1dd3f2](http://github.com/symfony/symfony/commit/f1dd3f22e32cb951dcbdca7bee97c8d5fbf18ed6 "f1dd3f22e32cb951dcbdca7bee97c8d5fbf18ed6 commit on github"), [946d3d9](http://github.com/symfony/symfony/commit/946d3d9302a1a72db2107a26c84256110ee1e15c "946d3d9302a1a72db2107a26c84256110ee1e15c commit on github"): \[TwigBundle\] added two global variables (environment &amp; debug)
  * [2c45611](http://github.com/symfony/symfony/commit/2c45611f4e08b578fc3a54187ef1a3bae962400d "2c45611f4e08b578fc3a54187ef1a3bae962400d commit on github"): fixed WDT link to the profiler
  * [0834bf4](http://github.com/symfony/symfony/commit/0834bf47dcc7094538a6c958fd62a15049712be0 "0834bf47dcc7094538a6c958fd62a15049712be0 commit on github"): \[WebProfilerBundle\] removed the WDT on malformed HTML content
  * [f6e624b](http://github.com/symfony/symfony/commit/f6e624b1e2182be0fb598db529d4bc3e7b245746 "f6e624b1e2182be0fb598db529d4bc3e7b245746 commit on github"): \[TwigBundle\] changed all Boolean to string in XSD as you might want to use a parameter %...%
  * [a3207e9](http://github.com/symfony/symfony/commit/a3207e939f4f4de24a740ce56b04483eb46e4074 "a3207e939f4f4de24a740ce56b04483eb46e4074 commit on github"): removed CompatAssetsBundle, use AsseticBundle instead
  * [b44d044](http://github.com/symfony/symfony/commit/b44d044b0afe218594d9ed7965eaeb272576bf80 "b44d044b0afe218594d9ed7965eaeb272576bf80 commit on github"): \[HttpKernel\] removed the bootstrap files as they do not belong to the component
  * [9a25878](http://github.com/symfony/symfony/commit/9a25878109feb582e52869503b055c1f9026bef8 "9a25878109feb582e52869503b055c1f9026bef8 commit on github"): \[FrameworkBundle\] removed the Welcome page and moved it to the sandbox/standard distrib
  * [eda7475](http://github.com/symfony/symfony/commit/eda74755ba1954950f48fc1dea4eda643ca4223e "eda74755ba1954950f48fc1dea4eda643ca4223e commit on github"): \[ZendBundle\] only load the logger if there is a config
  * [28bf834](http://github.com/symfony/symfony/commit/28bf834c0c7845a3a9fc9605e0e35c99e1475a6b "28bf834c0c7845a3a9fc9605e0e35c99e1475a6b commit on github"): \[WebProfilerBundle\] made the WDT less intruisive by moving it to its own Ajax request
  * <del>[608e443](http://github.com/symfony/symfony/commit/608e443c9719bad6929115a10d2e3ecc0abfbed6 "608e443c9719bad6929115a10d2e3ecc0abfbed6 commit on github"): \[Config\] created VariableNode</del> (reverted)
  * [f4c0af7](http://github.com/symfony/symfony/commit/f4c0af76e767013ba5d64fe12b4ecd912c85ea9b "f4c0af76e767013ba5d64fe12b4ecd912c85ea9b commit on github"): \[TwigBundle\] allowed arbitrary variables to be accepted as values for globals
  * [23e9386](http://github.com/symfony/symfony/commit/23e9386a0ea8dd3f4c25e27dda4e62a1b9e52752 "23e9386a0ea8dd3f4c25e27dda4e62a1b9e52752 commit on github"): changed all extensions to use the default Extension::getAlias() impl
  * [c518074](http://github.com/symfony/symfony/commit/c5180743066cae38b13134ef24137c215a707a1d "c5180743066cae38b13134ef24137c215a707a1d commit on github"): added a DI extension for DoctrineMigrations, removed --bundle option in favor of application level settings
  * [8a8c733](http://github.com/symfony/symfony/commit/8a8c73336918a25eec11e2546e7bf641f85b8dba "8a8c73336918a25eec11e2546e7bf641f85b8dba commit on github"): \[HttpKernel\] added the possibility to define a parent token for a token in the profiler
  * [9619c7d](http://github.com/symfony/symfony/commit/9619c7dade0db54d9171dcc26c7218f94ec45e9e "9619c7dade0db54d9171dcc26c7218f94ec45e9e commit on github"): \[Routing\] removed the routing hack where we add a / at the beginning if it does not exist
  * [e729589](http://github.com/symfony/symfony/commit/e729589b106e271dc41aad72903e6e9028a12a7e "e729589b106e271dc41aad72903e6e9028a12a7e commit on github"): splitted swiftmailer configuration to avoid issues when not using smtp
  * [d4fc3c9](http://github.com/symfony/symfony/commit/d4fc3c98b1cdd6f3df63d70ad2c4b7c0840ed8f9 "d4fc3c98b1cdd6f3df63d70ad2c4b7c0840ed8f9 commit on github"), [7c9528b](http://github.com/symfony/symfony/commit/7c9528be7bb9ece6c184ad0b9978d51d0c91bb29 "7c9528be7bb9ece6c184ad0b9978d51d0c91bb29 commit on github"), [b9168bb](http://github.com/symfony/symfony/commit/b9168bb6529ea673841bfcae34639cfc35369ad3 "b9168bb6529ea673841bfcae34639cfc35369ad3 commit on github"): \[FrameworkBundle\] updated the init:bundle skeleton files
  * [f21578e](http://github.com/symfony/symfony/commit/f21578e8195ec08a1b5becfadb5c6b32a5e5c961 "f21578e8195ec08a1b5becfadb5c6b32a5e5c961 commit on github"): \[Security\] added abstract user provider definition
  * [bf20238](http://github.com/symfony/symfony/commit/bf20238178e2ab1fb759464180c1cdcfb96b6cc4 "bf20238178e2ab1fb759464180c1cdcfb96b6cc4 commit on github"): fixed a bug in Response content-type auto-detection
  * [d94acd8](http://github.com/symfony/symfony/commit/d94acd85f9aee2342c7ec381d7fdd66aea1eafef "d94acd85f9aee2342c7ec381d7fdd66aea1eafef commit on github"): removed response as a service (the Response is not available in the DIC anymore)
  * [353177d](http://github.com/symfony/symfony/commit/353177d1d66ea220137beeedb0d50915b45f88ec "353177d1d66ea220137beeedb0d50915b45f88ec commit on github"): replaced Response::createRedirect by a new RedirectResponse class
  * [fc372bc](http://github.com/symfony/symfony/commit/fc372bc217385dc5130989150e979537140771a3 "fc372bc217385dc5130989150e979537140771a3 commit on github"): \[HttpKernel\] changed core.view event to use notifyUntil() instead of filter()
  * [a0bae94](http://github.com/symfony/symfony/commit/a0bae94f882966cc60707b8a0b55ca1cd6e6029c "a0bae94f882966cc60707b8a0b55ca1cd6e6029c commit on github"): \[HttpFoundation\] updated ResponseHeaderBag to compute Cache-Control whenever any of the headers it considers changes
  * [cef86a3](http://github.com/symfony/symfony/commit/cef86a3771d28a6588492664d6c4c370a4cb676f "cef86a3771d28a6588492664d6c4c370a4cb676f commit on github"): \[HttpKernel\] added a way to change the ESI cache strategy
  * [efb5617](http://github.com/symfony/symfony/commit/efb561767b0f48c2e128cb9f422634866cd25851 "efb561767b0f48c2e128cb9f422634866cd25851 commit on github"): \[AsseticBundle\] removed response service dependency in AsseticController
  * [d7ea92a](http://github.com/symfony/symfony/commit/d7ea92a0f62175f525a99397682e6d8d143fce17 "d7ea92a0f62175f525a99397682e6d8d143fce17 commit on github"): \[AsseticBundle\] updated for latest assetic development
  * <del>[0f353c1](http://github.com/symfony/symfony/commit/0f353c14110c1dc2383b231503cf3c933b846d55 "0f353c14110c1dc2383b231503cf3c933b846d55 commit on github"): added a command to generate a migration from the sql queries executed when you load some data fixtures</del> (reverted)
  * [788f63d](http://github.com/symfony/symfony/commit/788f63d460bdb2260f008d86cc094841f2e70894 "788f63d460bdb2260f008d86cc094841f2e70894 commit on github"): \[FrameworkBundle\] simplified the over-complicated template cache warmer
  * [9f2d59c](http://github.com/symfony/symfony/commit/9f2d59c489494552d2f74fa0a0b075b1a5a0d800 "9f2d59c489494552d2f74fa0a0b075b1a5a0d800 commit on github"): \[AsseticBundle\] added stylus filter
  * [192583a](http://github.com/symfony/symfony/commit/192583a225158c2f0d3022f9ec768806b36b4003 "192583a225158c2f0d3022f9ec768806b36b4003 commit on github"): \[ZendBundle\] added a Configuration class
  * [05055d4](http://github.com/symfony/symfony/commit/05055d443c82bd0206aed396a205df56ae6e8e05 "05055d443c82bd0206aed396a205df56ae6e8e05 commit on github"): \[AsseticBundle\] fixed formula caching system
  * [d4db531](http://github.com/symfony/symfony/commit/d4db5319c821c8769771567ff6ea2d208e3bcb28 "d4db5319c821c8769771567ff6ea2d208e3bcb28 commit on github"): \[AsseticBundle\] added resources to the routing loader
  * [968c870](http://github.com/symfony/symfony/commit/968c870c9455c363ec14fed44e17313d6e4ec368 "968c870c9455c363ec14fed44e17313d6e4ec368 commit on github"): \[AsseticBundle\] added etags to controller so changes to filters etc trigger invalidation
  * [f46c6f7](http://github.com/symfony/symfony/commit/f46c6f7e45c0b046183932ae1b69e5b7500e535f "f46c6f7e45c0b046183932ae1b69e5b7500e535f commit on github"): \[Routing\] fixed the %2f problem in URLs
  * [e16c666](http://github.com/symfony/symfony/commit/e16c6662667eb7cf929ffd42415e72a54163cd7a "e16c6662667eb7cf929ffd42415e72a54163cd7a commit on github"): \[Routing\] made an empty path info to redirect to / (as for any other route that ends with a /)
  * [b6049be](http://github.com/symfony/symfony/commit/b6049beca235eece6466d6ec612b3d11cb5c788e "b6049beca235eece6466d6ec612b3d11cb5c788e commit on github"), [381d1e2](http://github.com/symfony/symfony/commit/381d1e2da1410ddf8c9e2da07b4e4b8e1344adb7 "381d1e2da1410ddf8c9e2da07b4e4b8e1344adb7 commit on github"): \[Translation\] added search to FallbackLocale Catalogue
  * [4b3c495](http://github.com/symfony/symfony/commit/4b3c49550f7a5cd21f774a103d8df9d2cb7dd719 "4b3c49550f7a5cd21f774a103d8df9d2cb7dd719 commit on github"): fixed issues found by static code analysis

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfNginxPush](http://www.symfony-project.org/plugins/sfNginxPushPlugin): allows for easy pushing to configured nginx HTTP Push Module endpoints.
  * [sfEmailTemplates](http://www.symfony-project.org/plugins/sfEmailTemplatesPlugin): (no description)
  * [sfMarae](http://www.symfony-project.org/plugins/sfMaraePlugin): a threaded forum plugin.
  * [ynWidgetAjaxAutocomplete](http://www.symfony-project.org/plugins/ynWidgetAjaxAutocompletePlugin): includes a widget to replace sfWidgetForm*Choice with an AJAX-powered autocomplete field. Works for one-to-many and many-to-many relations.
  * [sfComet](http://www.symfony-project.org/plugins/sfCometPlugin): this will be a simple plugin with a JS class, and some examples.
  * [sfIsisImporter](http://www.symfony-project.org/plugins/sfIsisImporterPlugin): has classes to help importing a CDS/ISIS Database into a Symfony project.
  * [ynFormGeo](http://www.symfony-project.org/plugins/ynFormGeoPlugin): offers widgets and validators for working with geographic data.

Updated plugins
---------------

  * [sfProjectAnalyser](http://www.symfony-project.org/plugins/sfProjectAnalyserPlugin):
    * modified the error message when a class is not found
    * removed processLib until it work

  * [sfTrafficCMS](http://www.symfony-project.org/plugins/sfTrafficCMSPlugin):
    * added faster, less memory hungry export function which uses array hydration

  * [sfDoctrineRestGenerator](http://www.symfony-project.org/plugins/sfDoctrineRestGeneratorPlugin):
    * fixed a deserialization error when passing an empty XML tag

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * Delete, Edit and Show actions can now be hiden with the 'show_when' option
    * tweaked flash messages
    * checked if the object can be deleted in BatchDelete action

  * [sfAlyssaJqGrid](http://www.symfony-project.org/plugins/sfAlyssaJqGridPlugin):
    * added an option to change the default width of jqgrid

  * [assetPackages](http://www.symfony-project.org/plugins/assetPackagesPlugin):
    * the load_panels event is listened only when web_debug is turned on
    * fixed bug on simple stylesheet list in assets-packages.yml

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * refactored mtWidgetFormPlain so that it can be easily extended
    * added a new widget (ncWidgetFormPlainDate) that extends mtWidgetFormPlain and can be used to display dates as plain fields

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * syntax clean up (single quote, double quotes)
    * added app_a_js_debug check in globalJavascripts
    * added a default value of False to the JS Debug because that makes sense
    * changed search success body class that was the same as the interior page search results container class
    * fixed fixtures loading if the Zend Search if not available
    * added maxHeight option to slideshows (used in conjunction with flexHeight to limit the height of a slideshow)
    * added an option to aWidgetFormStaticText to not escape the values passed to it
    * created an aCmsRoute and introduce a hybrid mode (apostrophe url can be used with symfony action)
    * added hybrid page management in the aPage* code
    * easier to see paths when things can't be created in a_writable
    * tolerate deleted slots

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * made the edit buttons in the blog use a_button helper

  * [sfImageTransform](http://www.symfony-project.org/plugins/sfImageTransformPlugin):
    * fixed bug when using an image as a background using GD


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [Embetted](http://www.embetted.com): \(English\) free widgets for betting sites


They talked about us
--------------------

  * [Using OR In Propel Queries Becomes Much Easier With Propel 1.6](http://propel.posterous.com/using-or-in-propel-queries-becomes-much-easie)
  * [Default filter values in admin-generated symfony module](http://www.fizyk.net.pl/blog/default-filter-values-in-admin-generated-symfony-module)
  * [Dokumentacja kodu Symfony przy użyciu narzędzia phpdoc](http://tworzenie-web.pl/2011/02/23/dokumentacja-kodu-symfony-przy-uzyciu-narzedzia-phpdoc/)
  * [sfForkedDoctrineApplyPlugin 1.5.6 - Spanish translation](http://www.fizyk.net.pl/blog/sfforkeddoctrineapplyplugin-1-5-6-spanish-translation)
  * [fzBlameablePlugin 1.1.0](http://www.fizyk.net.pl/blog/fzblameableplugin-1-1-0)
  * [OpenPNE3インストールメモ](http://d.hatena.ne.jp/yusukekomo/20110227/1298779669)
  * [What makes application framework a popular choice for Web programmers?](http://www.ayacsoft.org/what-makes-application-framework-a-popular-choice-for-web-programmers/)
  * [Le MVC dans Symfony 2: cheminement d’une requête HTTP](http://code.anonymation.com/symfony-2/le-mvc-dans-symfony-2-cheminement-dune-requete-http/)
  * [sfWidgetFormJQueryDate con hora](http://fralazar.wordpress.com/2011/02/25/sfwidgetformjquerydate-con-hora/)
  * [Semantic configuration for a Symfony2 Bundle that can be overridden by the application by using a dependency injection extension](http://test.ical.ly/2011/02/25/semantic-configuration-for-a-symfony2-bundle-that-can-be-overridden-by-the-application-by-using-a-dependency-injection-extension/)
  * [Getting used to PHP 5.3 namespaces can drive you nuts at times – the devil is in the details](http://test.ical.ly/2011/02/23/getting-used-to-php-5-3-namespaces-can-drive-you-nuts-at-times-the-devil-is-in-the-details/)
  * [2 Symfony Live Paris conference passes up for grabs](http://blogs.jetbrains.com/webide/2011/02/2-symfony-live-paris-conference-passes-up-for-grabs/)
  * [Preparandonos para la llegada de Symfony2](http://www.osukaru.es/programacion/preparandonos-para-la-llegada-de-symfony2/)
  * [Error with Doctrine – Symfony migrate and text field](http://stephanchampagne.com/blog/2011/02/error-with-doctrine-symfony-migrate-and-text-field)
  * [PHP on IIS に PHPUnit をインストールする](http://www.moonmile.net/blog/archives/2061)
  * [大人気SNS改（仮）始動・・・](http://otonanosusume.org/blog/?p=132)
  * [Symfony Live 2011 San Francisco Highlight](http://www.learnwebdev.com/?p=639)
  * [Weka Sponsor Gold du Symfony Live](http://www.weka-entertainment.com/news/weka-sponsor-gold-du-symfony-live-948)
  * [symfonyでエスケープ処理](http://d.hatena.ne.jp/moroto1122/20110223/1298459731)
  * [一日のスケジュールを書きだそう　その後](http://blog.rakumachi.com/system/post-652.html)
  * [Symfony in San Francisco](http://clearcode.cc/2011/02/23/symfony-san-francisco/)
  * [ログ](http://yanor.net/wiki/?PHP-symfony/%E3%83%AD%E3%82%B0)
  * [Quick Tour por Symfony2: Primeros pasos](http://parasitovirtual.wordpress.com/2011/02/22/quick-tour-por-symfony2-primeros-pasos/)
  * [Tydzień przed Symfony Live 2011](http://www.zalas.pl/tydzien-przed-symfony-live-2011)
  * [PHP Web Framework in the Cloud: Symfony2](http://blog.cloud-apps-experts.com/2011/02/php-web-framework-in-cloud-symfony-2.html)
  * [Symfony TV](http://www.symfonylab.com/symfony-tv/)
  * [個々一番氏、米国でリア充になる秘訣を発見？ ロングインタビュー](http://blog.candycane.jp/archives/556)
  * [Varnish上でESIの機能を利用する](http://labs.unoh.net/2011/02/varnishesi.html)
  * [Two Talks at Symfony Live 2011](http://pierrespring.com/2011/02/21/sflive2011/)
  * [symfonyで行の並び順を指定できるビヘイビアを使ってみた](http://blog.loadlimits.info/2011/02/symfony%E3%81%A7%E8%A1%8C%E3%81%AE%E4%B8%A6%E3%81%B3%E9%A0%86%E3%82%92%E6%8C%87%E5%AE%9A%E3%81%A7%E3%81%8D%E3%82%8B%E3%83%93%E3%83%98%E3%82%A4%E3%83%93%E3%82%A2%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%A6/)
  * [UIの優れたWebベース、PHP/Symfony製の時間管理ソフトウェア「TimeHive」](http://www11.atpages.jp/~sstt0001/wordpress/?p=3940)
  * [Instalación de symfony en Linux Mint](http://fecyman10.wordpress.com/)