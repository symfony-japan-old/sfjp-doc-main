A week of symfony #200 (25->31 October 2010)
============================================

This week the Output Escaper component was heavily refactored and the Propel bundle was transformed into an independent bundle. In addition, the <a href="http://docs.symfony-reloaded.org/master/guides/cache/http.html">Symfony2 HTTP cache documentation</a> was published.
 
Development mailing list
------------------------

  * [Contexts for the Symfony DIC](http://groups.google.com/group/symfony-devs/browse_thread/thread/cded44241c728e8b)
  * [Remember Me Authentication](http://groups.google.com/group/symfony-devs/browse_thread/thread/fbe83d11a7ab9aa8)
  * [Injecting variables into the layout](http://groups.google.com/group/symfony-devs/browse_thread/thread/bec5185f48e8cc0a)
  * [making _format magic more useful](http://groups.google.com/group/symfony-devs/browse_thread/thread/ff702eccdd787e8b)
  * [[Doctrine2] issues with inheritance](http://groups.google.com/group/symfony-devs/browse_thread/thread/2fdb3540f8df974f)

symfony 1 development highlights
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=31%2F10%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r31247](http://trac.symfony-project.org/changeset/31247 "31247 revision on trac"): \[1.3, 1.4\] fixed mbstring problem in sfFilesystem
  * [r31248](http://trac.symfony-project.org/changeset/31248 "31248 revision on trac"): \[1.3, 1.4\] fixed sfI18nModuleExtract.class.php always assumes a file based message source
  * [r31250](http://trac.symfony-project.org/changeset/31250 "31250 revision on trac"): \[1.3, 1.4\] added some missing information in the WDT
  * [r31253](http://trac.symfony-project.org/changeset/31253 "31253 revision on trac"), [r31254](http://trac.symfony-project.org/changeset/31254 "31254 revision on trac"): \[1.3, 1.4\] fixed WDT injection


sfDoctrinePlugin:

  * [r31249](http://trac.symfony-project.org/changeset/31249 "31249 revision on trac"): \[1.3, 1.4\] fixed memory leak in Swift_DoctrineSpool



Activity summary: 58 changesets, 13 bugs reported, 15 bugs fixed, 3 enhancements closed, 5 documentation defects reported, 1 documentation defect fixed, and 11 documentation edits

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [6885f90](http://github.com/symfony/symfony/commit/6885f90f17597d9519f44d2b3986664c5703a232 "6885f90f17597d9519f44d2b3986664c5703a232 commit on github"): \[HttpKernel\Security\] fixed use statement and updated parameters constructor
  * [3463f47](http://github.com/symfony/symfony/commit/3463f47698fe028029bbff964773a1fbe2ee16c4 "3463f47698fe028029bbff964773a1fbe2ee16c4 commit on github"): applied base64 encoding directly to the binary data instead of their hexadecimal representation
  * [1d5ca49](http://github.com/symfony/symfony/commit/1d5ca4910dffd8b07df677d6c9d61b69d9d53c65 "1d5ca4910dffd8b07df677d6c9d61b69d9d53c65 commit on github"): \[FrameworkBundle\] refactored ide setting configuration
  * [e111652](http://github.com/symfony/symfony/commit/e1116524ed79cf118568e2c124f546d596a562c0 "e1116524ed79cf118568e2c124f546d596a562c0 commit on github"): \[WebProfiler\] fixed WDT display
  * [c065be8](http://github.com/symfony/symfony/commit/c065be88b56d3df7463a2d7f940c7885eb390661 "c065be88b56d3df7463a2d7f940c7885eb390661 commit on github"): \[OutputEscaper\] refactored the component
  * [e23c3cc](http://github.com/symfony/symfony/commit/e23c3cc702223612c82fa001a12e136e6ef945bb "e23c3cc702223612c82fa001a12e136e6ef945bb commit on github"): \[OutputEscaper\] made getEscaper*() methods more consistent with the way you can change the escaping strategy in __call()
  * [c448429](http://github.com/symfony/symfony/commit/c448429e62f8ff411ffec67f03e873eb81af8ea0 "c448429e62f8ff411ffec67f03e873eb81af8ea0 commit on github"): \[HttpFoundation\] fixed date format for HTTP headers (format must be RFC1123, not RFC2822)
  * [7e6bdde](http://github.com/symfony/symfony/commit/7e6bddedf90319a3e27c3a14b4f6753e38f96007 "7e6bddedf90319a3e27c3a14b4f6753e38f96007 commit on github"): \[TwigBundle\] moved Form extension initialization as late as possible (it's better for performance)
  * [2b613f3](http://github.com/symfony/symfony/commit/2b613f34d57bc1cdb9bf626ac905e734fdf3c023 "2b613f34d57bc1cdb9bf626ac905e734fdf3c023 commit on github"): \[FrameworkBundle\] removed the need for decorating  with SafeDecorator
  * [3eee458](http://github.com/symfony/symfony/commit/3eee458430e2a918594b41cdbf8be8142fb907db "3eee458430e2a918594b41cdbf8be8142fb907db commit on github"): \[OutputEscaper\] replaced the JS escaper with the one from Twig
  * [13f36b1](http://github.com/symfony/symfony/commit/13f36b165778acff165e1f7a4356a2ab784c625c "13f36b165778acff165e1f7a4356a2ab784c625c commit on github"): Removed logic that tried to avoid double-escaping
  * [88d30f0](http://github.com/symfony/symfony/commit/88d30f0d7496cf5f60a74827ca54c2b072cd1647 "88d30f0d7496cf5f60a74827ca54c2b072cd1647 commit on github"), [b9f33a6](http://github.com/symfony/symfony/commit/b9f33a610ee956647d3321cebac621abf97d1313 "b9f33a610ee956647d3321cebac621abf97d1313 commit on github"): removed Propel bundle (it has been moved as an independant bundle)



New [developers for hire](http://trac.symfony-project.com/trac/wiki/DevelopersForHire)
-----------------------

  * Wojtek Orzech \(w.orzech@gmail.com\): 26 years old PHP developer with almost 4 years of professional experience. Zend PHP5 certified engineer. I have been using Symfony for two years. I'm located in Cracow, Poland.


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [idlErrorManagement](http://www.symfony-project.org/plugins/idlErrorManagementPlugin): set of functionnalities to manage errors on production systems: DB logging, emailing, user feedback, ...
  * [sfCatalogoProdotti](http://www.symfony-project.org/plugins/sfCatalogoProdottiPlugin): product catalogue.
  * [cgHoptoadNotifier](http://www.symfony-project.org/plugins/cgHoptoadNotifierPlugin): submits bug reports to hoptoad and works with the api version 2.

Updated plugins
---------------

  * [sfDoctrineGuard](http://www.symfony-project.org/plugins/sfDoctrineGuardPlugin):
    * updated french translations
    * fixed setupInheritance access
    * begin to merge sfDoctrineGuardExtraPlugin into sfDoctrineGuardPlugin
    * added more translations
    * use mailer compose function
    * added username or email validator to password forgot
    * removed flash translation in action you can do it in the template my mistake
    * moved mailer call into function
    * moved query into table class
    * fixed mail function
    * fixed password change function
    * add config param app_sf_guard_plugin_password_change_url and simplified code

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * added the change for credentials widget
    * added partial widget
    * updated README
    * added jquery ajax dependence
    * added the select jquery autocomplete widget
    * updated JavaScript

  * [sfTangoIcons](http://www.symfony-project.org/plugins/sfTangoIconsPlugin):
    * fixed function name
    * updated documentation
    * added new helper functions

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * updated DateTimeField widget for edit panels to enable a time field
    * fixed a bug where the generator wasn't passing the form and filter generators a dbMap
    * fixed a bug with mulitple panels batch_actions combo having the same id
    * fixed regression with foreign filter date widgets
    * added new Plain textfield widget and associated ux
    * switched formpanel to used edit configuration
    * renamed fieldset config from params_ to config_ for consistancy

  * [sfThrift](http://www.symfony-project.org/plugins/sfThriftPlugin):
    * updated directory structure
    * updated documentation
    * added Thrift protocol factory

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * created a Taggable widget that extends the sfWidgetFormInput class

  * [sfPHPUnit2](http://www.symfony-project.org/plugins/sfPHPUnit2Plugin):
    * added task for compiling plugin core classes for external plugin usage
    * integrated lime lib to compiled file

  * [sfAssetsLibrary](http://www.symfony-project.org/plugins/sfAssetsLibraryPlugin):
    * fixed pdf thumbnail generation

  * [sfGrid](http://www.symfony-project.org/plugins/sfGridPlugin):
    * added support to custom columns (data is obtainded from invoking methods for the current object-row)

  * [sfAlyssaJqGrid](http://www.symfony-project.org/plugins/sfAlyssaJqGridPlugin):
    * added support for custom columns

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * you can now put :sf_culture in the a_page route if you wish
    * initial version of apostrophe site importer
    * changed image_tag() to url_for() because you can't use image_tag() inside of an input element
    * aImporter now supports loading of richText and foreignHtml
    * Fixed a lot of search stuff, providing the underpinnings for several bug reports
    * put a mute on aZendSearch
    * there is now blog search in the blog sidebar, which is aware of both publication dates and the category restrictions of the blog engine page you are searching on
    * aMultipleSelect now has an "autocomplete" option
    * changed the cancel helper
    * menuToggle needs to accept functions for before and after open and closing
    * minifier now inserts a newline after each .js file minified
    * created a Taggable widget that extends the sfWidgetFormInput class
    * button slots accept an option for image
    * removed pages fixtures from the plugin
    * added a Focus parameter to the menuToggle so you can focus something after it opens
    * added a persistentLabel parameter to apostrophe.selfLabel so you can choose whether or not the label persists on focus
    * styled the New Post / New Event modal forms
    * refactored the enhanced media pager stuff out of indexSuccess
    * added blog slot stuff to a-area-slots.css
    * styled blog post pager to be visually consistent with media pager
    * fixed bug that was showing esc_raw in the search box
    * updated the aAdmin generator theme to more closely resemble the aBlogAdmin theme

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * the event form now has an 'all day' check box which toggles event time
    * the onChange autosave has been replaced by a setInterval autosave
    * save button has been added to the top of the form
    * the new post / event buttons now use the menuToggle like all of the other menus in apostrophe
    * on initial save, don't override published_at if it has already been specified
    * don't try to setTitle on the page object until it has been saved
    * removed stray references to the catTag area
    * added apostrophe-blog:generate-test-posts task, which creates 100 posts with random titles and text
    * implemented 20/50/100 pager


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [MyBestApulia](http://www.mybestapulia.com): \(English, Italian\) Online hotel booking and tourist info in Apulia (or Puglia), Italy
  * [MyBestTrentino](http://www.mybesttrentino.com): \(English, Italian\) Online hotel booking and tourist info in Trentino-Alto Adige, Italy


They talked about us
--------------------

  * [Doctrine behaviour LooseCoupling now collects garbage with a new deletion cascade](http://test.ical.ly/2010/10/25/doctrine-behaviour-loosecoupling-now-collects-garbage-with-a-new-deletion-cascade/)
  * [Propel at Forum PHP Paris](http://propel.posterous.com/propel-at-forum-php-paris)
  * [Diem is hiring!](http://diem-project.org/blog/diem-is-hiring)
  * [symfony.xrea.jp の閉鎖のお知らせ](http://blog.sarabande.jp/post/1409868373)
  * [A quick start guide to deploying symfony/doctrine applications to productive systems](http://test.ical.ly/2010/10/27/a-quick-start-guide-to-deploying-symfonydoctrine-applications-to-productive-systems/)
  * [Utilisation de VHost pour l’accès au backend](http://www.lexik.fr/blog/symfony/symfony/utilisation-de-vhost-pour-lacces-au-backend-1307)
  * [lyMediaManagerPlugin: FCKEditor and PDF thumbnails](http://www.lyra-cms.com/blog/2010/10/lymediamanagerplugin-fckeditor-pdf-thumbnails.html)
  * [Lets talk about JSON in Symfony2](http://pooteeweet.org/blog/0/1850#m1850)
  * [One simple way how to use different symfony app.yml settings for development, preproduction and production servers](http://test.ical.ly/2010/10/28/one-simple-way-how-to-use-different-symfony-app-yml-settings-for-development-preproduction-and-production-servers/)
  * [How to customize the error pages in Symfony2](http://blog.servergrove.com/2010/10/28/how-to-customize-the-error-pages-in-symfony2/)
  * [Presentaciones Symfony en la PHP Barcelona 2010](http://www.symfony.es/2010/10/30/presentaciones-symfony-en-la-php-barcelona-2010/)
  * [Video: IDE Autocompletion with Propel](http://propel.posterous.com/video-ide-autocompletion-with-propel)
  * [Symfony2 stuff](http://pooteeweet.org/blog/0/1853#m1853)
  * [Advanced symfony Techniques](http://www.symfonylab.com/advanced-symfony-techniques/)
  * [Unit testing symfony plugins with php unit](http://www.phphatesme.com/blog/qualitatssicherung/unit-testing-symfony-plugins-with-php-unit/)
  * [Symfony MIME-type problem uploading image files](http://yureg.com/dev-flow/2010/10/symfony-mime-type-problem-uploading-image-files/)
  * [Les tableaux associatif dans les fichiers de configuration .yml de Symfony](http://matthieu.igwane.com/2010/10/29/les-tableaux-associatif-dans-les-fichiers-de-configuration-yml-de-symfony/)
  * [Organizing larger symfony projects with plugins](http://www.gerryvandermaesen.com/posts/organizing-larger-symfony-projects-with-plugins)
  * [symfony insert raw sql using doctrine](http://islamkhalil.wordpress.com/2010/10/28/symfony-insert-raw-sql-using-doctrine/)
  * [SYMFONY 助手 （Helpers）](http://hi.baidu.com/54lwh/blog/item/3b48c81b00c6a4f1ae5133e7.html)
  * [getInstance method for Doctrine tables](http://symfony-blog.driebit.nl/2010/10/getinstance-method-for-doctrine-tables/)
  * [symfonyでのグローバル定数について](http://www.phppro.jp/qa/2941)
  * [Wordpressのテンプレートでsymfonyを使う](http://www.exgear.jp/blog/2010/10/wordpress-with-symfony/)
  * [symfony: get installed plugin](http://www.meteenee.com/symfony-get-installed-plugin)
  * [Bonnes pratiques Symfony: Refactorisons le code](http://www.avanim-prod.com/blog/symfony/bonnes-pratiques-symfony-refactorisons-le-code-142)
