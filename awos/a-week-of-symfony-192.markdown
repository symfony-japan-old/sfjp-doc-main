---
layout: default
title: A week of symfony#192 (30 August -> 5 September 2010)
---

A week of symfony #192 (30 August -> 5 September 2010)
======================================================

Symfony2 introduced this week its new Web Profiler Bundle. The Symfony Profiler augments the web development toolbar and provides the most detailed debug information available in any framework.

Development mailing list
------------------------

  * [GitHub Pull Requests 2.0 and Symfony](http://groups.google.com/group/symfony-devs/browse_thread/thread/636c059a6000b3a3)
  * [UUID of Propel mirror server](http://groups.google.com/group/symfony-devs/browse_thread/thread/7861beb34be45af1)

symfony 1 development highlights
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=05%2F09%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r30790](http://trac.symfony-project.org/changeset/30790 "30790 revision on trac"): \[1.3, 1.4\] fixed logging of PHP errors to the WDT when error messages include a "%" character

Activity summary: 49 changesets, 10 bugs reported, 16 bugs fixed, 3 enhancements suggested, 3 enhancements closed, 5 documentation defects reported, 1 documentation defect fixed, and 8 documentation edits

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [478fcca](http://github.com/symfony/symfony/commit/478fcca88d9357779f353d07bb3ca301966e88d6 "478fcca88d9357779f353d07bb3ca301966e88d6 commit on github"): \[Templating\] added Engine::exists()
  * [6b5c3d0](http://github.com/symfony/symfony/commit/6b5c3d05bd25b250918fbaec14774e408dee71f9 "6b5c3d05bd25b250918fbaec14774e408dee71f9 commit on github"): \[FrameworkBundle\] removed usage of Controller class for internal controllers
  * [994a6c3](http://github.com/symfony/symfony/commit/994a6c36ac1e24f8f940a20a3debc91ee9e22c4c "994a6c36ac1e24f8f940a20a3debc91ee9e22c4c commit on github"): changed actions::render() helper method signature
  * [8c6478d](http://github.com/symfony/symfony/commit/8c6478dab976700a247e819179a21d196e252cb1 "8c6478dab976700a247e819179a21d196e252cb1 commit on github"): \[HttpKernel\] added import/export to Profiler
  * [d94271b](http://github.com/symfony/symfony/commit/d94271ba9c5e27d8767693a5e073fc4849535694 "d94271ba9c5e27d8767693a5e073fc4849535694 commit on github"): \[FrameworkBundle\] removed dependency with the DIC
  * [d40d174](http://github.com/symfony/symfony/commit/d40d1746e0f5f5c3c081b2fc8f53541e80a44e2c "d40d1746e0f5f5c3c081b2fc8f53541e80a44e2c commit on github"): \[ZendBundle\] added an option to register zend logger as an error handler
  * [7503463](http://github.com/symfony/symfony/commit/7503463a1e0f78737bf34c31e6cb3e4e28b236af "7503463a1e0f78737bf34c31e6cb3e4e28b236af commit on github"): \[DoctrineMongoDBBundle\] updated log format to look more like the javascript shell
  * [935ac56](http://github.com/symfony/symfony/commit/935ac5633c5a04421e78a62ef917176d9173d9b3 "935ac5633c5a04421e78a62ef917176d9173d9b3 commit on github"): \[DoctrineBundle\] fixed bug in data:load when purging many-to-many relationships
  * [60ea1ee](http://github.com/symfony/symfony/commit/60ea1eef698c6eae0d19465e00e9ff9be29bfc4b "60ea1eef698c6eae0d19465e00e9ff9be29bfc4b commit on github"): added a configuration to allow the profiler to be enabled only when an exception occurs
  * [ad835f8](http://github.com/symfony/symfony/commit/ad835f8a1693111a46aaffeee19bcbeecbdaaf2d "ad835f8a1693111a46aaffeee19bcbeecbdaaf2d commit on github"): \[HttpKernel\] added purge() in the profiler storage interface
  * [ab9be87](http://github.com/symfony/symfony/commit/ab9be87354a29bba11ca8644fcd26bcbaced9956 "ab9be87354a29bba11ca8644fcd26bcbaced9956 commit on github"): \[HttpKernel\] fixed FlattenException status code
  * [a29211a](http://github.com/symfony/symfony/commit/a29211a9ee79a687aa1ecc691e9d91b76271c11c "a29211a9ee79a687aa1ecc691e9d91b76271c11c commit on github"): \[FrameworkBundle\] removed usage of array access for helpers in templates
  * [4e57899](http://github.com/symfony/symfony/commit/4e57899374edd84bab3c98f852035a5626f7fa7b "4e57899374edd84bab3c98f852035a5626f7fa7b commit on github"), [5913c40](http://github.com/symfony/symfony/commit/5913c40a12becf5775dabf7fd10be524ef4d055e "5913c40a12becf5775dabf7fd10be524ef4d055e commit on github"), [7e2f135](http://github.com/symfony/symfony/commit/7e2f135245c0d789a8d3f2f7bd3b8e178992afec "7e2f135245c0d789a8d3f2f7bd3b8e178992afec commit on github"), [c8935cc](http://github.com/symfony/symfony/commit/c8935cc25a08fa009681c8e1c4afd82b4d08e51f "c8935cc25a08fa009681c8e1c4afd82b4d08e51f commit on github"): \[WebProfilerBundle\] added the bundle
  * [ebae1d7](http://github.com/symfony/symfony/commit/ebae1d7bf20d7e68f19f83c6ef71a43967a29d10 "ebae1d7bf20d7e68f19f83c6ef71a43967a29d10 commit on github"), [a4d4963](http://github.com/symfony/symfony/commit/a4d496309ba68ed5d0aea897e10fe8bb2b3440ab "a4d496309ba68ed5d0aea897e10fe8bb2b3440ab commit on github"): \[FrameworkBundle\] updated skeleton with the web profiler configuration
  * [2d04ca3](http://github.com/symfony/symfony/commit/2d04ca34434f00751e903d8b6ab41f7fef87d5bd "2d04ca34434f00751e903d8b6ab41f7fef87d5bd commit on github"): \[EventDispatcher\] added a way to disconnect all listeners for an event name
  * [15cd264](http://github.com/symfony/symfony/commit/15cd2643c04a1441db3476aa5d09ff05e9c0d83f "15cd2643c04a1441db3476aa5d09ff05e9c0d83f commit on github"): \[HttpFoundation\] added Request::getClientIp()

New [developers for hire](http://trac.symfony-project.com/trac/wiki/DevelopersForHire)
-----------------------

  * [Laveaucoupet.fr](http://www.laveaucoupet.fr): french small web agency based in le Mans. We develop onligne app and website for any kind of business model. See our site for details.

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [twLoremIpsum](http://www.symfony-project.org/plugins/twLoremIpsumPlugin): false data generator with more-or-less normal distribution of letters.
  * [gjShortUrl](http://www.symfony-project.org/plugins/gjShortUrlPlugin): easy and flexible management of redirect rules and keyword landing pages.
  * [twAdmin](http://www.symfony-project.org/plugins/twAdminPlugin): plugin based on sfAdminDashPlugin with style projected for Thunderwolf system backend.
  * [sfJqueryValidation](http://www.symfony-project.org/plugins/sfJqueryValidationPlugin): creates a powerful system to handle validation by both jQuery Validation and Symfony 1.3/1.4 in a unified manner (displays the same error messages in same markup whether validated server side or client side and can handle directly most symfony validation formats)
  * [bsJobQueue](http://www.symfony-project.org/plugins/bsJobQueuePlugin): allows to postpone the execution of function from any Table class.
  * [sfHarmonyRest](http://www.symfony-project.org/plugins/sfHarmonyRestPlugin): (no description)
  * [sdInteractiveChart](http://www.symfony-project.org/plugins/sdInteractiveChartPlugin): allows you to use Google's Visualization API without writing any javascript, it simplifies the creation of charts and makes the code a lot neater which is especially useful if your planning to include more than one chart in a page.
  * [ajDoctrineLuceneable](http://www.symfony-project.org/plugins/ajDoctrineLuceneablePlugin): provides three things: 1) a behaviour to add your doctrine records automaticly to a lucene index, 2) a way to add lucene search to FilterForms, 3) a wrapper class to search Lucene indexes.

Updated plugins
---------------

  * [sfPostgresDoctrine](http://www.symfony-project.org/plugins/sfPostgresDoctrinePlugin):
    * fixed bugs with inheritance and with tables patterns
    * updated README
    * fixed bug with yml files
    * added One To One relation in schema and model generation

  * [idlDropbox](http://www.symfony-project.org/plugins/idlDropboxPlugin):
    * added option to select OAuth library (Pear or Standard PHP lib)

  * [sfAssetsLibrary](http://www.symfony-project.org/plugins/sfAssetsLibraryPlugin):
    * changed from doSave to updateObject in sfAssetForm to allow saving of external objects
    * changed schema to get more friendly relation names
    * fixed a bug for moved files
    * added a check for file correctly saved

  * [pmPropelWorkflowableBehavior](http://www.symfony-project.org/plugins/pmPropelWorkflowableBehaviorPlugin):
    * behavior improved to work on sf 1.4

  * [sfReCaptcha](http://www.symfony-project.org/plugins/sfReCaptchaPlugin):
    * added option to validator to use classic invalid error

  * [sfDoctrineJCroppable](http://www.symfony-project.org/plugins/sfDoctrineJCroppablePlugin):
    * fixed bug with cropper image height not getting set correctly

  * [swBaseApplication](http://www.symfony-project.org/plugins/swBaseApplicationPlugin):
    * added jquery 1.4.2 and jquery-ui 1.8.4

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * added support for listview in generator as the default list
    * fridpanel and Listview are now set via list.layout generator.yml config
    * created new rowactions plugin to support object_actions for listview
    * created new checkcolumn plugin to support boolean checkbox columns for listview
    * created new ListPanel extension to hold listview and handle paging and toolbars
    * added ProgressColumn plugins for listview and grid

  * [sfSparkline](http://www.symfony-project.org/plugins/sfSparklinePlugin):
    * added support for symfony 1.4.x

  * [sfTaskLogger](http://www.symfony-project.org/plugins/sfTaskLoggerPlugin):
    * updated sample and purge tasks
    * moved "env" and "application" options at the base task level
    * prepared package and README for 1.0.2 version
    * fixed typos

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * new inline taggable widget
    * added jQueryAutocompleteSuccess.php
    * InlineTaggableWidget: performance enhancements, code readability enhancements, and moved functionality for unsetting existing popular tags to this script
    * refactored the makeLink function into two separate functions (makePopularLinks and makeRemoveLinks)
    * added the ability to pass in a label for the 'Existing Tags'

  * [sfAdminDash](http://www.symfony-project.org/plugins/sfAdminDashPlugin):
    * updated French translation

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * added mtWidgetFormPlain widget

  * [tdCore](http://www.symfony-project.org/plugins/tdCorePlugin):
    * enable the graphics module from tdCorePlugin to enable AJAX actions in other plugins to run correctly

  * [tdGuestbook](http://www.symfony-project.org/plugins/tdGuestbookPlugin):
    * added the activate/deactivate AJAX interface in the backend

  * [tdVideo](http://www.symfony-project.org/plugins/tdVideoPlugin):
    * added the activate/deactivate AJAX interface in the backend

  * [tdAudio](http://www.symfony-project.org/plugins/tdAudioPlugin):
    * added the activate/deactivate AJAX interface in the backend

  * [tdVisualFactory](http://www.symfony-project.org/plugins/tdVisualFactoryPlugin):
    * added the activate/deactivate AJAX interface in the backend

  * [tdBlog](http://www.symfony-project.org/plugins/tdBlogPlugin):
    * added the activate/deactivate AJAX interface in the backend

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * fixed pushTargetEnginePage to work when passed with a slug and no engine specified
    * don't try to calculate dimensions if PDF preview is turned off
    * backported improvements to aImageConverter and aValidatorFilePersistent
    * reworked a few engine link_to() calls to remove the need to query the database
    * never return attributes for a logged-out users in the media repository
    * removed the reference to the non-existent inline tagging widget
    * cleaned up some of the unused tagging code
    * saving page settings now updates the search index
    * fixed a bug with the Link option in button slots
    * improved stability when clicking save multiple times on an image selection
    * modified Page Settings Form to use the new Inline Taggable Widget
    * stopped unsetting some of the popular tags for the new tagging widget
    * you now can upload any mix of allowed file extensions
    * the set of file extensions, mime types and overall media types ("images," "video," "office") are now configurable (in principle) via app.yml
    * every item is now previewed either with an icon for its format or (for images) with an actual preview
    * you can now remove items during the annotation pass
    * when you are browsing for images for a slot, you can only upload images. When you are filtering by images, you can only upload images
    * the file upload widget is much smarter about detecting mime types and preferred file extensions correctly for a wide variety of file types including Office files
    * previews can be templated anywhere in the template containing the form
    * removed the "active" field in favor of paying attention to the names of the item fields
    * re-worked the page settings form significantly
    * fixed uploads in which one or more files are not acceptable

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * made sure new calendar widget defaults to false
    * fixed alphabetizing of categories in show actions for aEvent and aBlog
    * fixed save trigger for date widgets in blog and event admins
    * updated the blog plugin sidebar in the admin view to output a slightly different set of text for events and blog posts that are already published
    * switched the php date to use the aDate help for internationalization
    * updated the published at or published on interface so that it works with Ajax refreshes
    * refactored code in aBlogActions and aEventActions
    * fixed issue where past events were not showing up in calendar view


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [Corsi, lezioni e ripetizioni private](http://www.corsi-lezioni-ripetizioni.it/): \(Italian\) classified ads site for tutoring
  * [Alojamientos Dominicanos](http://alojamientodominicano.com): \(Spanish\) Hotel Guide Dominican Republic

New [symfony bloggers](http://trac.symfony-project.com/trac/wiki/SymfonyBloggers)
--------------------

  * [symfonic.fr](http://www.symfonic.fr) \([feed](http://www.symfonic.fr/feed/)\) \(English, French\)

They talked about us
--------------------

  * [Options for setting up a Doctrine database connection when PHPUnit testing symfony plugins](http://test.ical.ly/2010/08/30/options-for-setting-up-a-doctrine-database-connection-when-phpunit-testing-symfony-plugins/)
  * [Deploying a symfony project into production using capistrano](http://refineweb.co.uk/2010/08/30/deploying-a-symfony-project-into-production-using-capistrano/)
  * [Mysql ERROR 1005 (HY000): Can't create table (errno: 150)](http://broderix.blogspot.com/2010/08/mysql-error-1005-hy000-cant-create.html)
  * [gjShortUrlPlugin – Creating SEO landing pages and manage redirection of legacy URLs with the symfony and Doctrine plugin](http://test.ical.ly/2010/08/31/gjshorturlplugin-creating-seo-landing-pages-and-manage-redirection-of-legacy-urls-with-the-symfony-and-doctrine-plugin/)
  * [Storing emails in XML and sending them with sfMailer](http://refineweb.co.uk/2010/08/31/update-sending-emails-stored-in-xml-with-sfmailer/)
  * [PHP conferences update](http://blog.servergrove.com/2010/08/31/php-conferences-update/)
  * [Highlight code with symfony and Geshi](http://www.jnieto.org/article/highlight_code_with_symfony_and_geshi)
  * [A small symfony doctrine migration improvement task](http://rabaix.net/en/articles/2010/09/01/a-small-symfony-doctrine-migration-improvement-task)
  * [Frameworks for PHP Development in India Why and Which One to Use](http://www.jazzou.com/index.php?option=com_content&task=view&id=8338)
  * [Symfony2 presenta su WebProfiler](http://www.symfony.es/2010/09/01/symfony2-presenta-su-webprofiler/)
  * [symfony Day 2010: Entwickler aus aller Welt treffen sich in Köln](http://www.presseanzeiger.de/meldungen/it-computer-internet/383223.php)
  * [Hint to avoid memory exhausted error (symfony + doctrine1.2)](http://www.nacho-martin.com/hint-to-avoid-memory-exhausted-error-symfony-doctrine1-2)
  * [Symfony et Doctrine : connexions multiples](http://www.symfonic.fr/2010/09/symfony-et-doctrine-connexions-multiples/)
  * [ahDoctrineEasyEmbeddedRelationsPlugin and Composite Primary Keys](http://shout.setfive.com/2010/09/03/ahdoctrineeasyembeddedrelationsplugin-and-composite-primarykeys/)
  * [Zend Technologies : « Notre but est d'industrialiser et de professionnaliser l'utilisation de PHP »](http://www.channelinsider.fr/fr/entretien/2010/09/03/zend_technologies_____notre_but_est_d_industrialiser_et_de_professionnaliser_l_utilisation_de_php__)
  * [[symfony]EclipseのAntタスクからsymfonyコマンドを実行に関して](http://d.hatena.ne.jp/chronos_devel/20100905/1283695223)
  * [High Performance Mobile Symfony](http://www.symfonylab.com/high-performance-mobile-symfony/)
  * [Symfony Web Development: Offering Fast Paced Web Application Development](http://www.securesilverlight.net/935024-Symfony-Web-Development-Offering-Fast-Paced-Web-Application-Development.html)
  * [Instanciando la vista (sfView) y accediendo al contender de variables](http://www.loalf.com/2010/09/instanciando-la-vista-sfview-y-accediendo-al-contender-de-variables/)
  * [FoxMaSk au pays des merveilles du Web Developpement](http://www.foxmask.info/post/2010/09/04/foxmask-au-pays-des-merveilles-du-web-developpement/)
  * [How to validate and sanitize a URL in symfony](http://jasonswett.net/how-to-validate-and-sanitize-a-url-in-symfony/)
  * [symfony×OpenPNE3勉強会のまとめ（9/2@Nifty会議室）](http://www.tejimaya.com/archives/6221)
  * [Crear Módulo Inicio para tu Proyecto](http://symfony.cl/blog/2010/09/crear-modulo-inicio-para-tu-proyecto/)
  * [5 PHP Frameworks to Help PHP Developer Code Better in Less Time](http://www.tonarticles.com/5-php-frameworks-to-help-php-developer-code-better-in-less-time.html)
  * [AJAX und Flash-Variablen in symfony](http://www.typeed.de/blog/2010/08/31/ajax-und-flash-variablen-in-symfony)
  * [CentOS に symfony 1.2.9 を入れ直す](http://dev.halhal.info/archives/145)
