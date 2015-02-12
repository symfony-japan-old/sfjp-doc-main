---
layout: default
title: A week of symfony#194 (13->19 September 2010)
---

A week of symfony #194 (13->19 September 2010)
==============================================

Symfony2 PR3 was published this week, paving the way for the soon to be released Symfony2 alpha version. Meanwhile, the Symfony\Framework namespace was deleted and its code was moved to Symfony\Component\HttpKernel and Symfony\Bundle\FrameworkBundle.

Development mailing list
------------------------

  * [Symfony2: Admin Generator](http://groups.google.com/group/symfony-devs/browse_thread/thread/d0a19513d6cd8148/11d3f231ed3c07d5)
  * [Using templates for field rendering -- Proof of concept](http://groups.google.com/group/symfony-devs/browse_thread/thread/fb5fb9732cf5fc1e/df4e1a8131f931aa)
  * [Wanting to help complete the Forms framework for Symfony2](http://groups.google.com/group/symfony-devs/browse_thread/thread/c4b9586115736fe6/b6ccd29642250a49)

symfony 1 development highlights
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=19%2F09%2F2010&amp;daysback=6&amp;milestone=on&amp;ticket=on&amp;changeset=on&amp;update=Update):

  * [r30894](http://trac.symfony-project.org/changeset/30894 "30894 revision on trac"): \[1.3, 1.4\] improved test coverage of sfWebRequest::isSecure()
  * [r30896](http://trac.symfony-project.org/changeset/30896 "30896 revision on trac"): \[1.3, 1.4\] updated tests to better reset the path info array
  * [r30900](http://trac.symfony-project.org/changeset/30900 "30900 revision on trac"): \[1.3, 1.4\] fixed getUriPrefix() when requested is forwarded from a secure one
  * [r30912](http://trac.symfony-project.org/changeset/30912 "30912 revision on trac"): \[1.3, 1.4\] fixed view class overriding
  * [r30915](http://trac.symfony-project.org/changeset/30915 "30915 revision on trac"): \[1.3, 1.4\] added support for "image/x-ms-bmp" mime type


sfDoctrinePlugin:

  * [r30901](http://trac.symfony-project.org/changeset/30901 "30901 revision on trac"): \[1.3, 1.4\] reverted remove of comments in Doctrine-generated table classes



Activity summary: 36 changesets, 10 bugs reported, 11 bugs fixed, and 5 documentation edits

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [61f1866](http://github.com/symfony/symfony/commit/61f18667f4d1c924824bace22ca1cbccfdd6c70b "61f18667f4d1c924824bace22ca1cbccfdd6c70b commit on github"): \[Console\] added some tests for command shortcuts
  * [7734f44](http://github.com/symfony/symfony/commit/7734f44bc55bf13780dd0c56d1c73fa5365aefdb "7734f44bc55bf13780dd0c56d1c73fa5365aefdb commit on github"): \[Process\] added a Process:isSucessful() method
  * [1990fc5](http://github.com/symfony/symfony/commit/1990fc543b9629f91328846a5d8c2905baba4ce3 "1990fc543b9629f91328846a5d8c2905baba4ce3 commit on github"): \[HttpKernel\] added Closure support to ControllerResolver
  * [d657adb](http://github.com/symfony/symfony/commit/d657adbfa20878ca27ddc069ff5ba1e9904df931 "d657adbfa20878ca27ddc069ff5ba1e9904df931 commit on github"): removed Symfony\Framework. Things have been moved to Symfony\Component\HttpKernel and Symfony\Bundle\FrameworkBundle. The kernel configuration namespace was removed and merged with the main web configuration namespace

Documentation
-------------

  * Updated <a href="http://trac.symfony-project.org/wiki/HowToConnectToMSSQLServer">How To Connect To MSSQL Server</a> page


New [developers for hire](http://trac.symfony-project.com/trac/wiki/DevelopersForHire)
-----------------------

  * [NextSeven UG](http://www.nextseven.de): Symfony is the framework of our choice! We work in Berlin, Germany and are happy to work with you and your Symfony-Projects.


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfOptimizeSchema](http://www.symfony-project.org/plugins/sfOptimizeSchemaPlugin): extends the sfDoctrinePlugin Postgres database and is compatible with sfPostgresDoctrinePlugin.
  * [sfGoogleSitemap](http://www.symfony-project.org/plugins/sfGoogleSitemapPlugin): build your XML sitemap easily for symfony 1.4 and earlier.
  * [sfBehat](http://www.symfony-project.org/plugins/sfBehatPlugin): helps to write Cucumber-like Behat features to test symfony applications.

Updated plugins
---------------

  * [sfPHPUnit2](http://www.symfony-project.org/plugins/sfPHPUnit2Plugin):
    * added task for generating the default phpunit.xml.dist configuration file

  * [ggEmail](http://www.symfony-project.org/plugins/ggEmailPlugin):
    * corrected some typos and changed the plugin's status to beta

  * [daYamlEditor](http://www.symfony-project.org/plugins/daYamlEditorPlugin):
    * fixed the method scope

  * [sfZendMail](http://www.symfony-project.org/plugins/sfZendMailPlugin):
    * added option for sending html email to sendemail action
    * added parameter checking and string cleanup for sendemail action

  * [sfApplicationMap](http://www.symfony-project.org/plugins/sfApplicationMapPlugin):
    * added Windows support

  * [sfJqueryReloaded](http://www.symfony-project.org/plugins/sfJqueryReloadedPlugin):
    * added funcionality in jq_remote_function for the failure callback

  * [sfAtosPayment](http://www.symfony-project.org/plugins/sfAtosPaymentPlugin):
    * optimized getOrm with sfConfig::get("sf_orm")

  * [sfAssetsLibrary](http://www.symfony-project.org/plugins/sfAssetsLibraryPlugin):
    * added more compatibility with Windows

  * [sfPropel15](http://www.symfony-project.org/plugins/sfPropel15Plugin):
    * updated externals to Propel 1.5.4

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * fixed grouping support for ListView
    * added ux.list.ProgressColumn

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * added a wrapper tag to the "Add" Button in the inlineTaggableWidget
    * changed a wrapper CSS class to be more consistently named with it's siblings

  * [sfDatagrid](http://www.symfony-project.org/plugins/sfDatagridPlugin):
    * initial preview alpha for the new datagrid generator
    * finished the first part for admin generator
    * release 1.5.5 Admin generator propel 1.4

  * [pmJSCookMenu](http://www.symfony-project.org/plugins/pmJSCookMenuPlugin):
    * refactored plugin

  * [sfErrorNotifier](http://www.symfony-project.org/plugins/sfErrorNotifierPlugin):
    * try to make the plugin work with Symfony 1.4.6

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * fixed if you are beyond the last page you are redirected to the last page
    * added inline help for the feed slot to advertise its new capabilities
    * new layouts for Media engine
    * fixed a bug with createPage where you couldn't hit the enter key to submit the form
    * moved createPage javascript to a.js
    * refactored JS for toggling the template dropdown off and on for both Create Page and Page Settings, the JS is now shared instead of duplicated
    * refactored multiple selections to a.js and a_js_call() and made that compatible with cropping
    * default destination for the button slot is now url_for('@homepage') rather than /.
    * cleaned up RawHTML Slot, Button Slot, aText slot
    * merged the page settings and add page forms
    * removed obsolete _createPage.php partial and executeCreate method
    * added flexible i18n for the media item privacy statements
    * refactored the persistent file upload widget
    * refactored media's showSuccess to use the same mediaItem partial as indexSuccess
    * added show_constraints as a set of options for each media layout
    * prototyped the Javascript for four-up media view hover to expand functionality
    * audio player works in both media repository and slot

  * [lyMediaManager](http://www.symfony-project.org/plugins/lyMediaManagerPlugin):
    * removed other functions from 'tools' class


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [Le Phénix](http://www.lephenix.fr/): \(French\) Scène nationale de Valenciennes (developed with Diem CMF/CMS 5.1

New [symfony bloggers](http://trac.symfony-project.com/trac/wiki/SymfonyBloggers)
--------------------

  * [In a maze of gyruses](http://www.charnad.com/blog/tag/symfony/) \([feed](http://feeds2.feedburner.com/charnad)\) \(Russian\)

They talked about us
--------------------

  * [Symfony framework instead of a well-known CMS](http://symfony-world.blogspot.com/2010/09/symfony-framework-instead-of-well-known.html)
  * [Propel 2 utilizará Doctrine 2](http://www.symfony.es/2010/09/17/propel-2-utilizara-doctrine-2/)
  * [Nuova preview release per Symfony2](http://www.symfony.it/articoli/314/nuova-preview-release-per-symfony2/)
  * [Placer des valeurs par défaut dans un Filter Admin Generator](http://blog.damienalexandre.fr/index.php?post/2010/09/13/[Symfony-pro-tips)
  * [new releases of sfApplicationMapPlugin](http://symfony-world.blogspot.com/2010/09/new-releases-of-sfapplicationmapplugin.html)
  * [Sensio Labs contrôle la qualité des applications web](http://www.silicon.fr/sensio-labs-controle-la-qualite-des-applications-web-41899.html)
  * [Propel 1.5.4 Released](http://propel.posterous.com/propel-154-released)
  * [You can not set a custom view class when using getPresentationFor() to render another symfony action](http://test.ical.ly/2010/09/15/you-can-not-set-a-custom-view-class-when-using-getpresentationfor-to-render-another-symfony-action/)
  * [Symfony: иерархический URL](http://www.charnad.com/blog/symfony-hierarcial-url/)
  * [Implementing a staging/live website system with symfony and Apostrophe CMS](http://blog.servergrove.com/2010/09/15/implementing-a-staginglive-website-system-with-symfony-and-apostrophe-cms/)
  * [How to render another symfony action without the decoration using getPresentationFor()](http://test.ical.ly/2010/09/16/how-to-render-another-symfony-action-without-the-decoration-using-getpresentationfor/)
  * [Validar formato de patentes de autos en Chile con expresiones regulares](http://joaquinnunez.cl/blog/2010/09/10/validar-formato-de-patentes-de-autos-en-chile-con-expresiones-regulares/)
  * [sfProjectAnalyserPlugin: is your code beautiful?](http://www.symfonic.fr/en/2010/09/sfprojectanalyserplugin-is-your-code-beautiful/)
  * [Basic authentication](http://www.symfony.it/articoli/316/basic-authentication/)
  * [iT人甘苦談─軟體人的另一面 為資訊教育付出](http://www.ithome.com.tw/itadm/article.php?c=63350)
  * [Sensio Labs : le Contrôle technique des applicatifs Web](http://www.programmez.com/actualites.php?titre_actu=Sensio-Labs--le-Controle-technique-des-applicatifs-Web&amp;id_actu=8131)
  * [Personalizando el objeto sfUser de Symfony 1/1](http://micayael.wordpress.com/2010/09/17/personalizando-el-objeto-sfuser-de-symfony-1/)
  * [Retour de vacances : nouveau poste et nouveau projet](http://sebastien.porati.me/blog/2010/09/retour-de-vacances-nouveau-poste-et-nouveau-projet/)
  * [FrOSCamp: Symfony2 CMF and CouchDB ODM](http://pooteeweet.org/blog/0/1824#m1824)
  * [Afficher les statistiques dans une application symfony grâce à l’API Google Analytics](http://blog.cwx.be/?p=216)
  * [Symfony, Doctrine – Как изменить название загружаемого файла?](http://of.com.ua/symfony/symfony-doctrine-%D0%BA%D0%B0%D0%BA-%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B8%D1%82%D1%8C-%D0%BD%D0%B0%D0%B7%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B7%D0%B0%D0%B3%D1%80%D1%83%D0%B6%D0%B0%D0%B5%D0%BC%D0%BE/)
  * [symfony常用命令](http://www.ioola.org/2010/09/symfony_cmd/)
  * [Nos canards découvrent Symfony2](http://gilsrc.wordpress.com/2010/09/18/nos-canards-decouvrent-symfony2/)
  * [symfony, propel: records batch deleting](http://www.engoyan.com/533/symfony-propel-records-batch-deleting.html)
  * [symfony Day Cologne am 8. Oktober 2010](http://community.oreilly.de/blog/2010/09/17/symfony-day-cologne-am-8-oktober-2010/)
  * [ORM Designer](http://toni.uebernickel.info/development/orm-designer/)
  * [Offrez-vous les services d'un gourou de l'open source](http://www.channelnews.fr/actu-societes/57-editeurs-independant-isv/7633-offrez-vous-les-services-dun-gourou-de-lopen-source.html)
  * [Symfony Applications: Make The Most Of Innovative Applications](http://frontarticle.com/symfony-applications-make-the-most-of-innovative-applications.html)
  * [海外でも通用するエンジニアになる](http://el.jibun.atmarkit.co.jp/kaigaiengineer/2010/09/i18nsymfony-d3f.html)
  * [sandbox symfony не отображаются картинки](http://hudson.su/2010/09/15/sandbox-symfony-ne-otobrazhayutsya-kartinki/)
  * [Symfony: Control Model-&gt;save() function to perform INSERT or UPDATE](http://www.techiecorner.com/141/symfony-control-model-save-function-to-perform-insert-or-update/)
  * [Symfony ve Action içerisinde bulunan “@author” satırı](http://selam.sonsuzdongu.com/symfony-ve-action-icerisinde-bulunan-author-satiri)
  * [Die System/CMS Entscheidung – Teil 3/4: Symfony](http://www.ausgebloggt.de/2010/09/14/die-systemcms-entscheidung-teil-3-symfony/)
  * [[vim] vim, l’IDE et les plugin pour symfony (1/3)](http://romain.therrat.fr/vim-vim-lide-et-les-plugin-pour-symfony-13/309/)
  * [symfony Day 2010: Entwickler aus aller Welt treffen sich in Köln](http://serverwolken.de/symfony-day-2010-entwickler-aus-aller-welt-treffen-sich-in-koln-2477/)
  * [Unas chuletas para Symfony](http://symfony.cl/blog/2010/09/unas-chuletas-para-symfony/)
  * [True FastCGI for PHP 5.3 - migration and benchmarks](http://chetzit.com/blog/php/28.html)
