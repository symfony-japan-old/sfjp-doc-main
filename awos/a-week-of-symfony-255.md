A week of symfony #255 (14->20 November 2011)
=============================================

This week, [Symfony 2.0.6 was published](http://symfony.com/blog/security-release-symfony-2-0-6) as an important security release. Meanwhile, the official Symfony Community celebrated its first week introducing several improvements and announcing its 1,000th member milestone.
 
Development mailing list
------------------------

  * [Monolog swiftmailer handler configuration](https://groups.google.com/forum/#!topic/symfony-devs/IZ4a_-Oyt2c)
  * [\[RFC\] Symfony2 CI server](https://groups.google.com/forum/#!topic/symfony-devs/cjlktnXGmN0)
  * [LTS release](https://groups.google.com/forum/#!topic/symfony-devs/bp2QyeKRQR8)

symfony 1 development highlights
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=20%2F11%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r33208](http://trac.symfony-project.org/changeset/33208 "33208 revision on trac"): \[1.4\] fixed ob_start usage (to avoid warning in PHP 5.4)
  * [r33214](http://trac.symfony-project.org/changeset/33214 "33214 revision on trac"): \[1.4\] fixed ob_start() behavior on CLI

Symfony2 development highlights
-------------------------------

[2.0 branch](http://github.com/symfony/symfony/commits/master):

  * [0462a89](http://github.com/symfony/symfony/commit/0462a895620bee27053c7b2444f7a31fed69db9b "0462a895620bee27053c7b2444f7a31fed69db9b commit on github"): \[Security\] fixed HttpUtils::checkRequestPath() to not catch all exceptions
  * [d67fbe9](http://github.com/symfony/symfony/commit/d67fbe9e48b90c29c7e0d3ce19e5d1ef643ace7a "d67fbe9e48b90c29c7e0d3ce19e5d1ef643ace7a commit on github"): \[HttpFoundation\] added an exception to MimeTypeGuesser::guess() when no guesser are available
  * [f7c5bf1](http://github.com/symfony/symfony/commit/f7c5bf1db2d18dfb480ac4dc1e6b1be160952edf "f7c5bf1db2d18dfb480ac4dc1e6b1be160952edf commit on github"): \[HttpKernel\] fixed Content-Length header when using ESI tags
  * [86a8b9f](http://github.com/symfony/symfony/commit/86a8b9f567d8d30a1c629c46a6a8950944d2a4bb "86a8b9f567d8d30a1c629c46a6a8950944d2a4bb commit on github"): allow vendors checkout transport method to be overridden manually (http, https, git)
  * [79ae3fc](http://github.com/symfony/symfony/commit/79ae3fced982331aa89885289b942a5961646846 "79ae3fced982331aa89885289b942a5961646846 commit on github"): \[Form\] fixed radio and checkbox when data is not bool

[Master branch](http://github.com/symfony/symfony/commits/master):

  * [6d7e6a8](http://github.com/symfony/symfony/commit/6d7e6a87a8eb76b8a18de42bd04eed5e0d1be9f7 "6d7e6a87a8eb76b8a18de42bd04eed5e0d1be9f7 commit on github"): \[DoctrineBundle\] enhanced error reporting during mapping validation when nested exceptions occur
  * [62fb019](http://github.com/symfony/symfony/commit/62fb019c6283ee0510f34ea188159cdb83fee47b "62fb019c6283ee0510f34ea188159cdb83fee47b commit on github"): added event priorities in the profiler
  * [43e6c36](http://github.com/symfony/symfony/commit/43e6c3690908ba59c9a7eb9bee5cdd62b60dff19 "43e6c3690908ba59c9a7eb9bee5cdd62b60dff19 commit on github"): \[FrameworkBundle\] changed the session listeners to be subscribers
  * [264a033](http://github.com/symfony/symfony/commit/264a033728e6063bb19702463e3c3c0989d924fd "264a033728e6063bb19702463e3c3c0989d924fd commit on github"): fixed uncompatible closure declaraction in FileldTypeValidatorExtensionTest
  * [e3655f3](http://github.com/symfony/symfony/commit/e3655f3a5ccfdf866d4cd629c283203330516d67 "e3655f3a5ccfdf866d4cd629c283203330516d67 commit on github"): changed priorities for kernel.request listeners (the Firewall is now executed after the Router)
  * [5e4b7cb](http://github.com/symfony/symfony/commit/5e4b7cb1ba06445dd5370d861caeb5cc5eacf912 "5e4b7cb1ba06445dd5370d861caeb5cc5eacf912 commit on github"): renamed Propel Bridge from Propel to Propel1

Updated plugins
---------------

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * updated crWidgetFormJsTree
    * fixed jstreemerge special case
    * added suport for view selection on tree when editing
    * fixed required option now working and widget configuration option merge
    * modified alWidgetFormTimepicker to adapt to current jquery ui theme

  * [cpDatePicker](http://www.symfony-project.org/plugins/cpDatePickerPlugin):
    * added 'noscript' option

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * set REMOTE_ADDR if it is missing in aTaskTools::signinAsTaskUser()
    * added rsync-extras to apostrophe:deploy
    * cleaned up some of the variable namespacing in slotEnableForm and slotEnableFormButtons
    * moved the php below the doctype in layout so there's no whitespace at the top of the document when it's rendered
    * fixed display of tiny images in the media library
    * use pnmflip, not pamflip, because many systems still don't have pamflip (notably Ubuntu)
    * links to files in the file slot open in a new tab/window

  * [apostropheCkEditor](http://www.symfony-project.org/plugins/apostropheCkEditorPlugin):
    * removed an error_log() call and an apostrophe.log() call from the plugin


They talked about us
--------------------

  * [Travis, CI for OSS](http://pooteeweet.org/blog/0/2046#m2046)
  * [Symfony2 – how to find current environment](http://www.noop.lv/2011/11/14/symfony2-how-to-find-current-environment/)
  * [Symfony2: An alternative to Symfony 1's routing.load_configuration event](http://php-and-symfony.matthiasnoback.nl/2011/11/symfony2-an-alternative-to-symfony-1s-routing-load_configuration-event/)
  * [Abilitare estensioni aggiuntive per Twig](http://www.symfony.it/articoli/540/abilitare-estensioni-twig/)
  * [FunstaffTikaBundle: Wrapper pour Tik](http://www.funstaff.ch/2011/11/14/funstafftikabundle-wrapper-pour-tika)
  * [Symfony2 Tutorial: 3 premiers chapitres du tuto Watch My Desk](http://www.lafermeduweb.net/billet/symfony2-tutorial-3-premiers-chapitres-du-tuto-watch-my-desk-1232.html)
  * [Se publica la actualización de seguridad 2.0.6](http://www.symfony.es/2011/11/17/se-publica-la-actualizacion-de-seguridad-2-0-6/)
  * [Symfony + Backbone.js for highly dynamic apps](http://sf.khepin.com/2011/11/symfony-backbone-js-for-highly-dynamic-apps/)
  * [Resumen de la reunión de desarrolladores (17-11-2011)](http://www.symfony.es/2011/11/18/resumen-de-la-reunion-de-desarrolladores-17-11-2011/)
  * [Drupal8 und Symfony2 gehen gemeinsame Wege](http://relevant.at/wirtschaft/pr/323075/drupal8-symfony2-gehen-gemeinsame-wege.story)
  * [Setting PHPUnit for symfony projects on Ubuntu](http://www.noop.lv/2011/11/19/setting-phpunit-for-symfony-projects-on-ubuntu/)
  * [Twitter @Anywhere and PHP Symfony. Implementing login action](http://shared-memos.blogspot.com/2011/11/twitter-anywhere-and-php-symfony.html)
  * [symfony1.4でとにかく初期化するためのコマンド](http://d.hatena.ne.jp/Kmusiclife/20111119/1321690826)
  * [開発環境でsymfonyのプロジェクトをpost-commit + svn update + Capistrano + rsync + sshで簡単デプロイする方法](http://www.polyglot-software.com/2011/11/19/238)
  * [Symfony 2: “render” helper for calling an action from a view](http://www.dinduks.com/symfony-2-render-helper-for-calling-an-action-from-a-view)
  * [pear下安装symfony的步骤](http://kulouxia.com/view/2011-11-17/install-symfony-in-pear.html)
  * [Symfony 2 Фиктивные модели для форм](http://png-tech.blogspot.com/2011/11/symfony-2.html)
  * [Insertando calendarios de jQuery con Symfony](http://simelo-es.blogspot.com/2011/11/insertando-calendarios-de-jquery-con.html)
  * [配置nginx支持Symfony](http://www.yylog.net/archives/41/)
  * [SymfonyでHello world!を作ってみる](http://omnioo.com/omnioolab/php/-hello-worldsymfonyurl---symfony5w1h-symfony-hello-worldhello-world-symfony.php)
  * [Instalasi Symfony di Mac OS](http://ihsanrama.wordpress.com/2011/11/16/instalasi-symfony-di-mac-os/)
  * [Symfony 2 SQLite](http://weblabor.hu/forumok/temak/110469)
  * [Symfony Development Community Encourages Every Contribution](http://blog.oxagile.com/2011/11/15/symfony-development-community-encourages-every-contribution/)
  * [Installing and using Coffee-Script with Assetic on Windows](http://www.symfony-zone.com/wordpress/2011/11/15/installing-and-using-coffee-script-with-assetic-on-windows/)
  * [A Static Cache for Symfony and Silex – Would you use it?](http://www.testically.org/2011/11/15/a-static-cache-for-symfony-and-silex-would-you-use-it/)
  * [Change user roles during a session in Symfony](http://blogsh.de/2011/11/15/change-user-roles-during-a-session-in-symfony/)
  * [Symfony忘れた…→Symfonyめんどい→Symfonyすごい→(半年後)→Symfony忘れた…](http://uzulla.hateblo.jp/entry/2011/11/15/033321)
  * [El final del autoloading](http://desarrolla2.com/php-symfony/el-final-del-autoloading/)
  * [php、Symfony　Widgetsについての質問](http://www.phppro.jp/qa/2972)
  * [Symfony 1.0 NULL](http://mmj.99ing.net/Entry/1103/)
  * [Symfony on Plesk 10.2](http://www.swiftwater-solutions.com/?p=219)
  * [openPNE创建项目](http://www.cnblogs.com/dreamhome/archive/2011/11/13/2247541.html)
