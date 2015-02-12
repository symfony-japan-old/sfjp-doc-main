---
layout: default
title: "A week of symfony #218 (28 February -> 6 March 2011)"
---

A week of symfony #218 (28 February -> 6 March 2011)
====================================================

What a week for symfony project! [Hundreds of developers](http://www.flickr.com/search/?q=sflive2011&s=rec&z=t) gathered in Paris for [Symfony Live 2011](http://www.symfony-live.com/paris) conference, attending [tens of technical sessions](https://docs.google.com/document/pub?id=1rXrCNX25JArMq5TEHJOFiJjnmsKjRX4JpUoFxTXqob0), discussing [the future of Symfony2](http://trac.symfony-project.org/wiki/SfliveParisDevMeeting) and getting in touch with other community members.

A new way to download and install Symfony2 [based on distributions](http://symfony.com/distributions) was unveiled during the conference. In addition, at the closing keynote, symfony project showed its brand-new visual identity and the new [symfony.com](http://symfony.com) domain. This new design is already [being adopted in Symfony2 code](http://twitter.com/#!/fabpot/status/44353455271313408).

Development mailing list
------------------------

  * [\[Symfony2\] Third-party dependencies in Components (reloaded)](https://groups.google.com/forum/#!topic/symfony-devs/rknqUKNzFig)
  * [Extending NotFoundHttpException](https://groups.google.com/forum/#!topic/symfony-devs/UKRV_6PcQwg)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [5683c6e](http://github.com/symfony/symfony/commit/5683c6e6e15d399e442826412914d15a9647e461 "5683c6e6e15d399e442826412914d15a9647e461 commit on github"): \[AsseticBundle\] separated read and write paths to facilitate writing assets to a CDN via a custom stream wrapper
  * [0306c9a](http://github.com/symfony/symfony/commit/0306c9aa66955671d530f6ed917a34af6326fcc5 "0306c9aa66955671d530f6ed917a34af6326fcc5 commit on github"), [057e861](http://github.com/symfony/symfony/commit/057e86161e48f99fe7f23c1d50211202fefc2ca2 "057e86161e48f99fe7f23c1d50211202fefc2ca2 commit on github"): fixed array argument parsing in ArgvInput
  * [d57c665](http://github.com/symfony/symfony/commit/d57c6657bda010b6864f81045744f8307b7a84d4 "d57c6657bda010b6864f81045744f8307b7a84d4 commit on github"): \[AsseticBundle\] added config option to limit which bundles formulae are loaded from
  * [26e7470](http://github.com/symfony/symfony/commit/26e7470eb33adff42202bc20899e5645560b32b9 "26e7470eb33adff42202bc20899e5645560b32b9 commit on github"): \[ZendBundle\] added classes to compile
  * [67c886f](http://github.com/symfony/symfony/commit/67c886f3df49a236ef326478565e506002ddd4e1 "67c886f3df49a236ef326478565e506002ddd4e1 commit on github"): \[DependencyInjection/Compiler\] fixed a bug which silently changed the scope of services
  * [3a47fa6](http://github.com/symfony/symfony/commit/3a47fa6eeddfd51c64de67ec9b83c2ba39a75aaa "3a47fa6eeddfd51c64de67ec9b83c2ba39a75aaa commit on github"): \[Tests\] fixed lots of typos on test files
  * [9283877](http://github.com/symfony/symfony/commit/9283877828c3c11e91ee00f55eab0b3caccc3ccc "9283877828c3c11e91ee00f55eab0b3caccc3ccc commit on github"): \[AsseticBundle\] progress migrating functional tests to unit tests
  * [f7b7288](http://github.com/symfony/symfony/commit/f7b7288892f4d2bf6c5aa1dd0f8d71f772d05ab2 "f7b7288892f4d2bf6c5aa1dd0f8d71f772d05ab2 commit on github"): \[AsseticBundle\] added compiler pass for factory workers
  * [4a8f101](http://github.com/symfony/symfony/commit/4a8f10192f5bbc781e999677add6d8568335bd03 "4a8f10192f5bbc781e999677add6d8568335bd03 commit on github"): \[DependencyInjection\] fixed unit tests when using phar and suhosin
  * [44d069a](http://github.com/symfony/symfony/commit/44d069a3fb4b02639d0b2948bcdce725b0016736 "44d069a3fb4b02639d0b2948bcdce725b0016736 commit on github"): \[HttpKernel\] added an subclass merge extension configuration compiler pass to ensure each bundle's main extension is loaded
  * [44d069a](http://github.com/symfony/symfony/commit/44d069a3fb4b02639d0b2948bcdce725b0016736 "44d069a3fb4b02639d0b2948bcdce725b0016736 commit on github"): \[DependencyInjection\] extensions should only load if called during configuration
  * [3567fc4](http://github.com/symfony/symfony/commit/3567fc4e6cc56f17a88891b04e8c3ece1c53b35d "3567fc4e6cc56f17a88891b04e8c3ece1c53b35d commit on github"): \[HttpFoundation\] added Session tests
  * [f82b89c](http://github.com/symfony/symfony/commit/f82b89cdc5f13220bf2678825ad9ffd041cafa1a "f82b89cdc5f13220bf2678825ad9ffd041cafa1a commit on github"): \[Security\] changed defaults for MessageDigestEncoder (encode_as_base64 set to true, iterations increased to 5000 from 1)
  * [8d4dae9](http://github.com/symfony/symfony/commit/8d4dae9f2ace9dd389c136b4d740910303462069 "8d4dae9f2ace9dd389c136b4d740910303462069 commit on github"): \[AsseticBundle\] finished and enabled php templating support
  * [ed338d9](http://github.com/symfony/symfony/commit/ed338d9422ae9b25d32cc03195c289a50a0edd12 "ed338d9422ae9b25d32cc03195c289a50a0edd12 commit on github"): \[Yaml\] improved support for double quoted values (added support for the full range of escaped values in double quoted strings in chapter 5 of the YAML 1.1 and 1.2 specs)
  * [dbde41c](http://github.com/symfony/symfony/commit/dbde41c0829ebb1408a7a522ff24de5b0ae503aa "dbde41c0829ebb1408a7a522ff24de5b0ae503aa commit on github"): \[Security\] added the 'key' attribute of RememberMeToken to serialized string to be stored in session
  * [3e7ccae](http://github.com/symfony/symfony/commit/3e7ccae2ba7f03cbf6bec6c26c3591b6cddd1d07 "3e7ccae2ba7f03cbf6bec6c26c3591b6cddd1d07 commit on github"): \[HttpKernel\] added tests for debug stuff
  * [4c54218](http://github.com/symfony/symfony/commit/4c54218a4bf652b224c44bacd1107122571feb6f "4c54218a4bf652b224c44bacd1107122571feb6f commit on github"): \[AsseticBundle\] fixed url for assets in the debugging mode
  * [87e1359](http://github.com/symfony/symfony/commit/87e1359ebdcef503f357fc3c7929e6250c1d2323 "87e1359ebdcef503f357fc3c7929e6250c1d2323 commit on github"): \[HttpFoundation\] more sophisticated checks for valid expiration
  * [7900e86](http://github.com/symfony/symfony/commit/7900e8624ffaeec6be668b43186e5b37879aecf8 "7900e8624ffaeec6be668b43186e5b37879aecf8 commit on github"): \[HttpFoundation\] added some more tests on response
  * [44b0bbc](http://github.com/symfony/symfony/commit/44b0bbc0d1b64177c08f685eaf4f97e5576a228a "44b0bbc0d1b64177c08f685eaf4f97e5576a228a commit on github"): \[HttpKernel\] added Tests for DataCollectors
  * [c2e0537](http://github.com/symfony/symfony/commit/c2e0537c31cef79943bb3d53937c7877f152f521 "c2e0537c31cef79943bb3d53937c7877f152f521 commit on github"): added cache warmed routers support to RouteHelper
  * [f75ec8d](http://github.com/symfony/symfony/commit/f75ec8d4ada912de982d73ef6dedba991922a619 "f75ec8d4ada912de982d73ef6dedba991922a619 commit on github"), [f0e1df2](http://github.com/symfony/symfony/commit/f0e1df26883a94f5189d719573b5c4fc8cd47ac3 "f0e1df26883a94f5189d719573b5c4fc8cd47ac3 commit on github"), [124461c](http://github.com/symfony/symfony/commit/124461cceeedfffcb200e8504f2bda826d8fe39c "124461cceeedfffcb200e8504f2bda826d8fe39c commit on github"), [be8618e](http://github.com/symfony/symfony/commit/be8618ec5661d2106fce2d3c752c30e4906016c5 "be8618ec5661d2106fce2d3c752c30e4906016c5 commit on github"): \[FrameworkBundle\] implemented new exception stack trace layout
  * [2d68ca4](http://github.com/symfony/symfony/commit/2d68ca4d00e473c6928268bbf46efdf8983227c1 "2d68ca4d00e473c6928268bbf46efdf8983227c1 commit on github"), [a8e882a](http://github.com/symfony/symfony/commit/a8e882ac514097e32f81e1a928fa52b9c266f44e "a8e882ac514097e32f81e1a928fa52b9c266f44e commit on github"), [1134fd1](http://github.com/symfony/symfony/commit/1134fd17ab1d70ab3490d1e66c13c0d9308de435 "1134fd17ab1d70ab3490d1e66c13c0d9308de435 commit on github"), [fcc66ad](http://github.com/symfony/symfony/commit/fcc66ad540d42e17b7955ebfc7e1b6d357703bc8 "fcc66ad540d42e17b7955ebfc7e1b6d357703bc8 commit on github"): \[WebProfilerBundle\] changed web debug toolbar css layout
  * [d37f52c](http://github.com/symfony/symfony/commit/d37f52c74380b49ca5bf1f4143e550de59a5ea30 "d37f52c74380b49ca5bf1f4143e550de59a5ea30 commit on github"), [e51c46b](http://github.com/symfony/symfony/commit/e51c46b21ae1f846effc0686a9eafd3df0f96ae7 "e51c46b21ae1f846effc0686a9eafd3df0f96ae7 commit on github"), [ce7fddd](http://github.com/symfony/symfony/commit/ce7fddd4ea7cb8113be8d22d73dfb4007f3c0f58 "ce7fddd4ea7cb8113be8d22d73dfb4007f3c0f58 commit on github"), [8367694](http://github.com/symfony/symfony/commit/83676943716fac60b2950178be4ab1d807450069 "83676943716fac60b2950178be4ab1d807450069 commit on github"), [f4f78d4](http://github.com/symfony/symfony/commit/f4f78d47c89ddd81b743a5364f3599af966673b4 "f4f78d47c89ddd81b743a5364f3599af966673b4 commit on github"), [91caf4b](http://github.com/symfony/symfony/commit/91caf4b6e38dd3059571266634f19cf97422f7a4 "91caf4b6e38dd3059571266634f19cf97422f7a4 commit on github"), [0b41116](http://github.com/symfony/symfony/commit/0b41116a7bb801402cc09c7c2734c005546cc7e6 "0b41116a7bb801402cc09c7c2734c005546cc7e6 commit on github"), [659bfc5](http://github.com/symfony/symfony/commit/659bfc5615503c3b140504122c54dfd686a7af76 "659bfc5615503c3b140504122c54dfd686a7af76 commit on github"), [aca2c16](http://github.com/symfony/symfony/commit/aca2c161c8d18be708abd63ec616317df6eecb19 "aca2c161c8d18be708abd63ec616317df6eecb19 commit on github"): \[WebProfilerBundle\] implemented new web profiler layout

Documentation
-------------

  * New Symfony Live Paris Developers Meeting page

New [job postings](http://trac.symfony-project.com/trac/wiki/JobPostings)
----------------

  * Senior Symfony PHP Developer at [Elan Media Partner](http://elanmediapartners.com/) - full-time based in Melbourne, Australia - Contact: michael.tibben [at] elanmediapartners [dot] com
  * PHP / Symfony2 Developer at [YOOtheme GmbH](http://www.yootheme.com) - full-time based in Hamburg, Germany - Contact: info [at] yootheme [dot] com

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfDbQuickAccess](http://www.symfony-project.org/plugins/sfDbQuickAccessPlugin): provides an easy interface to quickly find and access tables from your configured databases.
  * [sfHttpDigestAuth](http://www.symfony-project.org/plugins/sfHttpDigestAuthPlugin): adds support for HTTP Digest authentication in symfony 1.x.
  * [ohMailChimp](http://www.symfony-project.org/plugins/ohMailChimpPlugin): a simple wrapper for the MailChimp API .
  * [sfDatePickerTime](http://www.symfony-project.org/plugins/sfDatePickerTimePlugin): provides a hybrid jQuery datepiker and a time selector widget based on the sfWidgetFormDateTime widget.

Updated plugins
---------------

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * moved the blog test post/event tasks into the apostrophe namespace
    * changed disqus comment count default from # to 0

  * [apostrophePeople](http://www.symfony-project.org/plugins/apostrophePeoplePlugin):
    * fixed some issues with the admin headshot stuff

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * updated the aPageSettings to extend aAdmin which extends SF
    * a culture in the URL works properly as a culture switcher if you go straight to an engine page without visiting a normal page for that culture first
    * the engine page cache correctly matches when a culture is in the URL
    * the engine page cache correctly matches when a frontend controller name is in the URL


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [Sydney Scoreboard - IWG 2010](http://www.sydneyscoreboard.com): \(English\) The legacy of the 5th IWG World Conference on Women and Sport held in Sydney, 2010. Its aim is to increase women’s representation on sport boards globally.


They talked about us
--------------------

  * [Should my next project use Symfony2?](http://blog.seric.at/2011/02/28/should-my-next-project-use-symfony2/)
  * [Lexik sera présent au symfony live 2011 à paris](http://www.lexik.fr/blog/symfony/non-classe/lexik-sera-present-au-symfony-live-2011-a-paris-1505)
  * [Live from Symfony Live Parigi – giorno #1](http://www.symfony.it/articoli/413/live-from-symfony-live-parigi-giorno-1/)
  * [Don't Copy Code. Oh, and Inheritance and Composition are Bad, Too](http://propel.posterous.com/dont-copy-code-oh-and-inheritance-and-composi)
  * [Editing Twig templates in Dreamweaver](http://blog.servergrove.com/2011/03/03/editing-twig-templates-in-dreamweaver/)
  * [Symfony Live : Sensio Labs (Symfony) lance un plan d’embauches sans précédent](http://www.silicon.fr/sensio-labs-symfony-lance-un-plan-d%E2%80%99embauches-sans-precedent-46686.html)
  * [Bug Features update - projects and technologies keeping me quiet](http://bugfeatures.com/blog/index.php?entry=entry110303-125353)
  * [sfLive2011: Crónica de la primera jornada](http://www.symfony.es/2011/03/03/sflive2011-cronica-de-la-primera-jornada/)
  * [sfLive2011: Crónica visual de la primera jornada](http://www.symfony.es/2011/03/03/sflive2011-cronica-visual-de-la-primera-jornada/)
  * [Symfony Live : le forum phpBB migre sous Symfony 2](http://www.silicon.fr/phpbb-va-migrer-sous-symfony-2-46692.html)
  * [Presenting the new Symfony2 Livechat open source app](http://blog.servergrove.com/2011/03/04/presenting-the-new-symfony2-livechat-open-source-app/)
  * [Live from Symfony Live Parigi – giorno #2](http://www.symfony.it/articoli/441/live-from-symfony-live-parigi-giorno-2/)
  * [Symfony Live : « Programmeurs, privilégiez la simplicité »](http://www.silicon.fr/symfony-live-%C2%AB-programmeurs-privilegiez-la-simplicite-%C2%BB-46718.html)
  * [Symfony Live : les frameworks pour redonner le goût de la simplicité](http://www.lemagit.fr/article/microsoft-developpement-php-framework/8254/1/symfony-live-les-frameworks-pour-redonner-gout-simplicite/)
  * [sfLive2011: El proyecto Symfony renueva su imagen](http://www.symfony.es/2011/03/04/sflive2011-el-proyecto-symfony-renueva-su-imagen/)
  * [sfLive2011: Symfony2 se basará en distribuciones](http://www.symfony.es/2011/03/04/sflive2011-symfony2-se-basara-en-distribuciones/)
  * [Configurable required fields for symfony forms](http://sf.khepin.com/2011/03/configurable-required-fields-for-symfony-forms/)
  * [Retour sur mon symfony live 2011](http://blog.damienalexandre.fr/index.php?post/2011/03/04/Retour-sur-mon-symfony-live-2011)
  * [Utiliser sfForm (Symfony 1.4) de manière autonome dans vos projets](http://blog.slynett.com/developpement-web/php/utiliser-sfform-symfony-1-4-de-maniere-autonome-dans-vos-projets.html)
  * [Using Doctrine in Joomla](http://www.paulderaaij.nl/2011/03/05/using-doctrine-in-joomla/)
  * [Escribir mensajes de log desde el modelo que funcionan en las tareas CLI de Symfony](http://www.rodri.org/blog/2011/03/escribir-mensajes-de-log-desde-el-modelo-que-funcionan-en-las-tareas-cli-de-symfony/)
  * [Symfony Live 2011: Day 2](http://symfony-blog.driebit.nl/2011/03/symfony-live-2011-day-2/)
  * [Liveblogging Symfony Live Paris: Unconference Day](http://window.punkave.com/2011/03/04/liveblogging-symfony-live-paris-unconference-day/)
  * [Liveblogging Symfony Live Paris](http://window.punkave.com/2011/03/03/liveblogging-symfony-live-paris/)
  * [Symfony Live 2011 in Paris – Day 2 – (almost) live](http://test.ical.ly/2011/03/04/symfony-live-2011-in-paris-%E2%80%93-day-2-%E2%80%93-almost-live/)
  * [Relaciones Muchos a Muchos (M:N) en symfony 1.4 y Doctrine](http://roy-rc.blogspot.com/2011/03/relaciones-muchos-muchos-mn-en-symfony.html)
  * [Using th native MySQL ENUM type in Symfony 1.4 and Doctrine](http://imanpage.com/code/using-th-native-mysql-enum-type-symfony-14-and-doctrine)
  * [Symfony live 2011](http://www.willdurand.fr/symfony-live-2011/)
  * [CSSやJSファイルの配信を最適化するAsseticが便利そう](http://blog.candycane.jp/archives/561)
  * [Comienza la Symfony Live 2011](http://blog.solucionex.com/symfony/comienza-la-symfony-live-2011)
  * [My first symfony2 Bundle ProjectUtilitiesBundle](http://digitalkaoz.net/2011/03/projectutilitiesbundle/)
  * [Symfony Live Paris 2011](http://www.antistatique.net/blog/2011/03/01/symfony-live-paris-2011/)
  * [Formulario de registro básico en Symfony 1.4](http://jonsegador.com/2011/03/formulario-de-registro-basico-en-symfony-1-4/)
  * [PHP5 Symfony сэдэвт практикт суурилсан сургалт](http://www.kt.mn/nuur/kt-undsen-bulanguud/medee/2947-php5-symfony-sedevt-praktikt-suurilsan-surgalt.html)
  * [Symfony Live : one more time](http://www.amicalement-web.net/symfony-live-one-more-time/2011/02/28/)
  * [symfony conditional validation](http://www.entroducing.com/view/symfony-conditional-validation)
  * [Fabien Potencier – the father and the mother of Symfony framework](http://www.symfonylab.com/fabien-potencier-the-father-and-the-mother-of-symfony-framework/)
  * [symfony1.4でZnedFrameworkのOAuthを使う](http://d.hatena.ne.jp/brtRiver/20110227/1298786034)
  * [Symfony Live 2011: Day 1](http://symfony-blog.driebit.nl/2011/03/symfony-live-2011-day-1/)
  * [Открылся новый официальный сайт symfony](http://habrahabr.ru/blogs/symfony/115006/)
  * [sfLive2011: Crónica de la segunda jornada](http://www.symfony.es/2011/03/06/sflive2011-cronica-de-la-segunda-jornada/)
  * [[Symfony2] Sandbox/Standard Edition – bootstrap.php]()
  * [PHP中静态调用非静态方法](http://www.foolbirds.com/php%E4%B8%AD%E9%9D%99%E6%80%81%E8%B0%83%E7%94%A8%E9%9D%9E%E9%9D%99%E6%80%81%E6%96%B9%E6%B3%95.html)
  * [ymfony framework / Открылся новый официальный сайт symfony](http://allaps.ru/symfony-framework-otkrylsya-novyj-oficialnyj-sajt-symfony)
  * [Symfony2 – UserBundle (FOSUserBundle)](http://www.issam-hakimi.com/?p=21229)
  * [Débuter Symfony 1.4: 8 interrogations et erreurs courantes](http://blog.slynett.com/developpement-web/symfony/debuter-symfony-1-4-8-interrogations-et-erreurs-courantes.html)
  * [sfLive2011: Resumen de todas las presentaciones](http://www.symfony.es/2011/03/06/sflive2011-resumen-de-todas-las-presentaciones/)
