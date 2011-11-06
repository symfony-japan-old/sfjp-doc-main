A week of symfony #252 (24->30 October 2011)
============================================

Symfony 1.4.15 was released this week, fixing a few bugs and demonstrating the strong support of symfony 1.4.x branch until its late 2012 deadline. Meanwhile, Symfony2 added [a matcher](https://github.com/symfony/symfony/commit/24b93928bf783290c0df193f1b9948a174b01d1b) and [a command](https://github.com/symfony/symfony/commit/8cc3158d8901b8aefadde7f24be92fd9ed2b07e7) that help debugging router matching problems.
 
Development mailing list
------------------------

  * [getRouter() instead of get('router')](https://groups.google.com/forum/#!topic/symfony-devs/HcWILuuvZ3U)
  * [Official AdminGenerator?](https://groups.google.com/forum/#!topic/symfony-devs/HMmMSQPGMZg)
  * [Making Symfony 2.0 forwards compatible](https://groups.google.com/forum/#!topic/symfony-devs/CibR6gKmRug)

symfony 1 development highlights
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=30%2F10%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r33151](http://trac.symfony-project.org/changeset/33151 "33151 revision on trac"): \[1.4\] fixed usage of mb_strlen in tasks
  * [Milestone 1.4.15 completed](http://trac.symfony-project.org/milestone/1.4.15)

sfDoctrinePlugin:

  * [r33149](http://trac.symfony-project.org/changeset/33149 "33149 revision on trac"): \[1.4\] added missing admin.delete_object event


Symfony2 development highlights
-------------------------------

[2.0 branch](http://github.com/symfony/symfony/commits/master):

  * [cbb4bba](http://github.com/symfony/symfony/commit/cbb4bbae977eb7e0651b9963cbef84fa75349c3d "cbb4bbae977eb7e0651b9963cbef84fa75349c3d commit on github"): \[Routing\] fixed side-effect in the PHP matcher dumper
  * [808088a](http://github.com/symfony/symfony/commit/808088a3ca607bf62f6c70ef7d3a3066f0cfac98 "808088a3ca607bf62f6c70ef7d3a3066f0cfac98 commit on github"): added the ability to use dot and single quotes in the keys and values
  * [27d0809](http://github.com/symfony/symfony/commit/27d080984ca8f972241cd3e38f0181d1a8722e93 "27d080984ca8f972241cd3e38f0181d1a8722e93 commit on github"), [e314931](http://github.com/symfony/symfony/commit/e3149318f522c14717041db3ff6b7e64421ce033 "e3149318f522c14717041db3ff6b7e64421ce033 commit on github"): updated Monolog to 1.0.2
  * [6343bef](http://github.com/symfony/symfony/commit/6343bef55e8f0cee33ef185081f128deb3c06656 "6343bef55e8f0cee33ef185081f128deb3c06656 commit on github"): \[HttpKernel\] updated mirror method to check for symlinks before dirs and files
  * [8dcde3c](http://github.com/symfony/symfony/commit/8dcde3c076b5c485dd133466bf20c45e53227dca "8dcde3c076b5c485dd133466bf20c45e53227dca commit on github"): \[DependencyInjection\] fixed int casting for XML files (based on what is done in the YAML component)
  * [4bbb685](http://github.com/symfony/symfony/commit/4bbb685557c9aebc54d6ee6fb268941695cde4f4 "4bbb685557c9aebc54d6ee6fb268941695cde4f4 commit on github"): \[DependencyInjection\] added tests for Definition and DefinitionDecorator exceptions
  * [80f0b98](http://github.com/symfony/symfony/commit/80f0b980baa4dbbd9a4f1dd2f75c7a6e0bbcb0bc "80f0b980baa4dbbd9a4f1dd2f75c7a6e0bbcb0bc commit on github"): \[DependencyInjection\] fixed DefinitionDecorator::getArgument() for replacements
  * [851eb73](http://github.com/symfony/symfony/commit/851eb737784b06619485c844882e98c800a8f7fb "851eb737784b06619485c844882e98c800a8f7fb commit on github"): removed a ton of unused use statements

[Master branch](http://github.com/symfony/symfony/commits/master):

  * [24b9392](http://github.com/symfony/symfony/commit/24b93928bf783290c0df193f1b9948a174b01d1b "24b93928bf783290c0df193f1b9948a174b01d1b commit on github"), [8cc3158](http://github.com/symfony/symfony/commit/8cc3158d8901b8aefadde7f24be92fd9ed2b07e7 "8cc3158d8901b8aefadde7f24be92fd9ed2b07e7 commit on github"): \[Routing, FrameworkBundle\] added a matcher and a command that help debugging matching problems
  * [8fa061c](http://github.com/symfony/symfony/commit/8fa061cc6e6635d403cca9b98e934a3b4021b892 "8fa061cc6e6635d403cca9b98e934a3b4021b892 commit on github"): \[WebProfilerBundle\] added a profiler panel for the router
  * [70e0dba](http://github.com/symfony/symfony/commit/70e0dba77c0f30154477b4f603be8ff336cf2192 "70e0dba77c0f30154477b4f603be8ff336cf2192 commit on github"): moved the Swiftmailer data collector to the Swifmailer bridge
  * [9077f6a](http://github.com/symfony/symfony/commit/9077f6a9711730559fe6e8432358c1c8b00a5ca7 "9077f6a9711730559fe6e8432358c1c8b00a5ca7 commit on github"): \[SwiftmailerBundle\] replaced MessageLogger class with the one from Swiftmailer 4.1.3
  * [95ec41b](http://github.com/symfony/symfony/commit/95ec41b075fcff99d0dee0769a7ec688bdd7a420 "95ec41b075fcff99d0dee0769a7ec688bdd7a420 commit on github"): \[Console\] made the defaults in Application more easily customizable
  * [f8065d1](http://github.com/symfony/symfony/commit/f8065d180574703dee6a7b114dbf7524ecc7408e "f8065d180574703dee6a7b114dbf7524ecc7408e commit on github"): \[HttpKernel\] added a way to get the original values returned by the router
  * [c2fa73d](http://github.com/symfony/symfony/commit/c2fa73d33aa0a07e8fba0ce49e1de4b16fd53d61 "c2fa73d33aa0a07e8fba0ce49e1de4b16fd53d61 commit on github"): \[HttpKernel\] removed the _route entry from _route_params


Updated plugins
---------------

  * [sfExtjs3](http://www.symfony-project.org/plugins/sfExtjs3Plugin):
    * fixed matching problem with quote_except value "function"

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * added the pmWidgetFormPropelInputByCode

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * added new aFiles::copy, aFiles::close methods that actually return false when things don't work
    * added a new areaHideWhenEmpty option to areas and the standardArea component. If this option is set to true, it will not output any of the area markup on the page to logged-out visitors of the site.
    * aTaskTools::setCliHost() now also supports https URLs: if app_cli_https is true, setCliHost() convinces Symfony to generate https URLs
    * added a findOnyBy and findAllBy method to aMysql
    * new app_a_feed_hide_identical_description doesn't bother outputting the RSS item's description if it is the same as the title
    * no more js errors from linkUpdates if there is no confirm message
    * fixed CkEditor behaves badly when you move slots. Moving edit views around in the DOM can cause unexpected behavior.
    * app_a_enforce_minimum_width can be set to false to stop standardArea from setting minimumWidth to match width




They talked about us
--------------------

  * [Back from Symfony Day 2011 Cologne](http://blog.marcw.net/2011/symfony-day-2011-cologne/)
  * [What is Symfony2?](http://fabien.potencier.org/article/49/what-is-symfony2)
  * [Drupal just got a whole lot more compatible](http://www.leftontheweb.com/message/Drupal_just_got_a_whole_lot_more_compatible)
  * [Drupal 8 staví na knihovnách ze Symfony2](http://www.root.cz/zpravicky/drupal-8-stavi-na-knihovnach-ze-symfony2/)
  * [It's all about the community](http://www.currentgame.de/news/its-all-about-the-community/008277/)
  * [sfForkedDoctrineApplyplugin 1.5.10](http://www.fizyk.net.pl/blog/sfforkeddoctrineapplyplugin-1-5-10)
  * [Symfony2: use a bootstrap file for your PHPUnit tests and run some console commands](http://php-and-symfony.matthiasnoback.nl/2011/10/symfony2-use-a-bootstrap-file-for-your-phpunit-tests-and-run-some-console-commands/)
  * [Symfony 2. Ограничение количества запросов](http://habrahabr.ru/blogs/symfony/131158/)
  * [Drupal 8 integra los primeros componentes de Symfony2](http://www.symfony.es/2011/10/26/drupal-8-integra-los-primeros-componentes-de-symfony2/)
  * [Symfony 1.4 – sfImageFileValidator – validate image dimensions](http://www.kamiladryjanek.com/2011/10/symfony-1-4-sfimagefilevalidator-validate-image-dimensions/)
  * [Presenting LyraAdminBundle](http://www.lyra-cms.com/blog/2011/10/presenting-lyraadminbundle.html)
  * [LexikTranslationBundle, pour éditer vos traductions avec Symfony2](http://www.lexik.fr/blog/symfony/symfony2/lexiktranslationbundle-pour-editer-vos-traductions-avec-symfony2-1753)
  * [How to use a symfony 1 layout from a different directory](http://www.devexp.eu/2011/10/28/how-to-use-a-symfony-1-layout-from-a-different-directory/)
  * [Auth checks and varnish](http://pooteeweet.org/blog/0/2033#m2033)
  * [Presentaciones Symfony en la PHP Barcelona Conference 2011](http://www.symfony.es/2011/10/29/presentaciones-symfony-en-la-php-barcelona-conference-2011/)
  * [How to install Symfony on Windows](http://aryatmajaya.com/symfony/how-to-install-symfony.html)
  * [Se publica Symfony 1.4.15](http://www.symfony.es/2011/10/30/se-publica-symfony-1-4-15/)
  * [Symfony’s Serializer Component](http://developer.e-butik.se/2011/10/symfonys-serializer-component/)
  * [Drupal integriert Symfony-2-Komponenten](http://it-republik.de/php/news/Drupal-integriert-Symfony-2-Komponenten-060873.html)
  * [How to customize form rendering in Symfony](http://blogsh.de/2011/10/26/how-to-customize-form-rendering-in-symfony/)
  * [Interfacing The PHP World Would Be Good](http://blog.astrumfutura.com/2011/10/interfacing-the-php-world-would-be-good/)
  * [Symfony2: Obtaining the Request Object](http://miller.limethinking.co.uk/2011/10/26/symfony2-obtaining-the-request-object/)
  * [Getting Symfony2 to run under PLESK](http://blog.davidweichert.de/2011/10/25/getting-symfony2-to-run-under-plesk/)
  * [Ejecutar query personalizada en symfony](http://webmasterinfo.com.ar/2011/10/ejecutar-query-personalizada-en-symfony/)
  * [Create a symfony widget like sfWidgetFormDateRang](http://www.cnblogs.com/ylxeluxi/archive/2011/10/25/2224222.html)
  * [Symfony Day 2011 in Cologne (Slides)](http://www.symfony-zone.com/wordpress/2011/10/25/symfony-day-2011-in-cologne-slides/)
  * [Mi configuración del servidor web de un sitio de Symfony](http://diman.kz/2011/10/my-apache2-conf-symfony/)
  * [What Symfonic Drupal means](http://www.garfieldtech.com/drupal-symfony2)
  * [Ubuntu11.10 Symfony2の開発環境を作る](http://omnioo.com/omnioolab/php/cat666/ubuntu1110-symfony2.php)
  * [sfCaptchaPlugin 1.0.4 has been released](http://www.symfonylab.com/sfcaptchaplugin-104-has-been-released/)
  * [Practical　symfony　12日目について](http://www.phppro.jp/qa/3453)
  * [Symfony Coding Standards Tips](http://somnathpawar.wordpress.com/2011/10/25/symfony-coding-standards-tips/)
  * [Symfony2 REST – reading data from PUT request](http://inchoo.net/tools-frameworks/simfony2-rest-put-request/)
