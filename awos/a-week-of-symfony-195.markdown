---
layout: default
title: A week of symfony#195 (20->26 September 2010)
---

A week of symfony #195 (20->26 September 2010)
==============================================

This week, the activity of the <a href="http://groups.google.com/group/symfony-devs/">symfony developers' mailing list</a> soared with lots of interesting discussions. Among many other topics, developers discussed about Symfony2 default template engine (PHP or Twig) and the default configuration format (PHP, XML or YAML). Remember that this mailing list is the best place to get the latest news from Symfony2 and to influence its future development.

Development mailing list
------------------------

  * [[Symfony2] Default to Twig?](http://groups.google.com/group/symfony-devs/browse_thread/thread/80d5e981ed247ccb/0a59e16587091ded)
  * [Symfony2 forms: feedback from symfony 1](http://groups.google.com/group/symfony-devs/browse_thread/thread/4cf6e1fd796a16e4/63a4a763cbdafa60)
  * [Controller Dependency Injection](http://groups.google.com/group/symfony-devs/browse_thread/thread/7766abae81097e9d/c9209fd91dfc0dd0)
  * [Default format for configurations](http://groups.google.com/group/symfony-devs/browse_thread/thread/1da7eb31466bccf8)

symfony 1 development highlights
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=26%2F09%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r30951](http://trac.symfony-project.org/changeset/30951 "30951 revision on trac"): \[1.3, 1.4\] fixed WDT injects multiple times
  * [Milestone 1.3.7 completed](http://trac.symfony-project.org/milestone/1.3.7)
  * [Milestone 1.4.7 completed](http://trac.symfony-project.org/milestone/1.4.7)
  * [r30961](http://trac.symfony-project.org/changeset/30961 "30961 revision on trac"): \[1.3, 1.4\] fixed missing WDT javascript

sfPropelPlugin:

  * [r30966](http://trac.symfony-project.org/changeset/30966 "30966 revision on trac"): \[1.3, 1.4\] updated Slovenian translations for Doctrine and Propel messages
  * [r30967](http://trac.symfony-project.org/changeset/30967 "30967 revision on trac"): \[1.3, 1.4\] fixed i18n support for traditional chinese
  * [r30968](http://trac.symfony-project.org/changeset/30968 "30968 revision on trac"): \[1.3, 1.4\] fixed Persian Translation of admin generator
  * [r30969](http://trac.symfony-project.org/changeset/30969 "30969 revision on trac"): \[1.3, 1.4\] added more translations to german and italian translations

Activity summary: 64 changesets, 21 bugs reported, 4 bugs fixed, 3 enhancements suggested, 1 enhancement closed, 8 documentation defects reported, 1 documentation defect fixed, and 4 documentation edits

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [5f9c365](http://github.com/symfony/symfony/commit/5f9c365971620d3c379e96169e9b2986072a0ca4 "5f9c365971620d3c379e96169e9b2986072a0ca4 commit on github"): \[DoctrineMongoDBBundle\] fixed formatting of booleans in query log
  * [e6bff04](http://github.com/symfony/symfony/commit/e6bff045c994de097f2feca67d53753c8e08a552 "e6bff045c994de097f2feca67d53753c8e08a552 commit on github"): \[DoctrineMongoDBBundle\] added a quick profiler panel
  * [71cc3a7](http://github.com/symfony/symfony/commit/71cc3a77734796db8691ac2289fd53ee2137c4bb "71cc3a77734796db8691ac2289fd53ee2137c4bb commit on github"): \[Form\] avoid double-escape and then unescape (using the fourth parameter of htmlspecialchars)
  * [2862c6c](http://github.com/symfony/symfony/commit/2862c6cce41a3af2d9a6d64502246ea072de0b5a "2862c6cce41a3af2d9a6d64502246ea072de0b5a commit on github"): refactored configuration names (have a look at the skeleton for how to upgrade)
  * [82f6a68](http://github.com/symfony/symfony/commit/82f6a68eb2cab5a0caf7e8fc52ba770364cf2d19 "82f6a68eb2cab5a0caf7e8fc52ba770364cf2d19 commit on github"): \[Validator\] allow DateTime objects as valid DateTimes
  * [2d80788](http://github.com/symfony/symfony/commit/2d80788e3aa7f406a14d00543d32ed1e81579bdb "2d80788e3aa7f406a14d00543d32ed1e81579bdb commit on github"): \[FrameworkBundle\] added support for services as controllers
  * [f3993b4](http://github.com/symfony/symfony/commit/f3993b45c1ac6e69a82d9f66ef7e82bb87515851 "f3993b45c1ac6e69a82d9f66ef7e82bb87515851 commit on github"): added width, height, alt tags for all images used in web profilers (for proper html)
  * [d62befd](http://github.com/symfony/symfony/commit/d62befd67b0a1c86dffb4f590508199df8bef7b5 "d62befd67b0a1c86dffb4f590508199df8bef7b5 commit on github"): \[FrameworkBundle\] fixed Filesystem when used within a phar archive
  * [69b538b](http://github.com/symfony/symfony/commit/69b538b632289782848ddc4cc96b958fd6f4b074 "69b538b632289782848ddc4cc96b958fd6f4b074 commit on github"): \[FrameworkBundle\] removed the app:init command

New [developers for hire](http://trac.symfony-project.com/trac/wiki/DevelopersForHire)
-----------------------

  * Gaurang Rajvir \(gaurangrajvir@gmail.com\): Web developer and Project manager with more than 4 years experience. I work on LAMP, AJAX, php frameworks like symfony, codeigniter ... and Javascript frameworks like JQuery, JQueryUI, Prototype and more... I have more then 3 years of experience on symfony framework and provide any kind of solution.

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfDoctrineFaq](http://www.symfony-project.org/plugins/sfDoctrineFaqPlugin): allows you to embed a FAQ module within your symfony application with backend modules to manage categories and questions.
  * [sfMultiTenant](http://www.symfony-project.org/plugins/sfMultiTenantPlugin): allows you to create a multi-tenant-aware application. The plugin lets you add a tenant identifier column & reference the Tenant model, populate the tenant identifier column when saving records and adapt select queries to filter records for a tenant.
  * [sfAuditable](http://www.symfony-project.org/plugins/sfAuditablePlugin): allows you to automatically create audit fields in the model (e.g. created_by, updated_by, ...) and populate user details in these fields when a row is created or updated.
  * [sfActivateable](http://www.symfony-project.org/plugins/sfActivateablePlugin): allows you to automatically create a is_active flag (or name of your choice), create timestamp & user detail fields (e.g. activated_by, activated_at, ...) and populate timestamps & user details when is_active flag is toggled on a record.
  * [sfObjectLink](http://www.symfony-project.org/plugins/sfObjectLinkPlugin): allows you to identify the object type & object owning the record in the model by automatically create obj_type_id & obj_id fields on the model which need to be programatically populated.
  * [sfCk](http://www.symfony-project.org/plugins/sfCkPlugin): offers an unobtrousive integration between the CK WYSIWYG editor and symfony.
  * [sfGagatemplate](http://www.symfony-project.org/plugins/sfGagatemplatePlugin): integrates Gagatemplate engine in symfony.
  * [sfAdminHijack](http://www.symfony-project.org/plugins/sfAdminHijackPlugin): simple JQuery widget for doctrine one-to-many relations that "hijacks" a generated admin module for its functionality.
  * [smagBootstrap](http://www.symfony-project.org/plugins/smagBootstrapPlugin): reads and parses tasks from a yaml file and executes them.
  * [sfGoogleChart](http://www.symfony-project.org/plugins/sfGoogleChartPlugin): allows the use the Google Chart API in your symfony project.

Updated plugins
---------------

  * [lyMediaManager](http://www.symfony-project.org/plugins/lyMediaManagerPlugin):
    * improved error checking on asset file/folder deletion
    * made small changes to default list view
    * updated README with instruction on how to customize list view layout
    * improved error checking on asset/folder creating, moving, renaming, deleting operations

  * [sfPHPUnit2](http://www.symfony-project.org/plugins/sfPHPUnit2Plugin):
    * updated documentation

  * [csDoctrineActAsSortable](http://www.symfony-project.org/plugins/csDoctrineActAsSortablePlugin):
    * fixed moveToLast failed because of "moveToPosition requires an Integer as the new position
    * fixed moveToPosition moving down failed because of integrity constraint violation

  * [sfTrafficCMS](http://www.symfony-project.org/plugins/sfTrafficCMSPlugin):
    * added subnav
    * checking for images relation rather than assuming it
    * added slot to indicate the page being show for use with a nav menu on-state

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * added filterinputdate widget
    * added check so gridpanel javascript and css files are not included when listpanel is used
    * added allowClear and defaultValue to ux.TwinDateField
    * fixed quoting of iconCls for edit and list action buttons when iconCls is in the generator configuration
    * changed buildQuery and filter classes to support adding queryMethods and with statements before the form criteria is created

  * [sfAssetsLibrary](http://www.symfony-project.org/plugins/sfAssetsLibraryPlugin):
    * preparations for using sfAssetsLibraryPlugin as browser for CK Editor
    * added to documentation how to use sfAssetsLibraryPlugin with CK Editor

  * [sfDoctrineTaggable](http://www.symfony-project.org/plugins/sfDoctrineTaggablePlugin):
    * fixed bug in getTaggings() when a non existing tag is requested
    * added unit tests
    * fixed bug in getRelatedTags()
    * changed findOrCreateByTagname() so that it is not static anymore

  * [cleverFilesystem](http://www.symfony-project.org/plugins/cleverFilesystemPlugin):
    * in the case of a local disk filesystem, the cache method now returns the original filename, as caching is useless

  * [sfTaskLogger](http://www.symfony-project.org/plugins/sfTaskLoggerPlugin):
    * modified sample task short description

  * [diemProject](http://diem-project.org/):
    * added filter to prevent throwing exception on non-textual :input elements
    * enhanced to use `System / Dev / Server` admin action available in production environment

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * re-ordered a media item portion of the migration task
    * categories have been refactored (Apostrophe now has one set of categories, replacing the redundant implementations for the media repository and the blog plugin)
    * fixed overlay bug where the edit button for a selected image in a slideshow could not be clicked
    * fixed markup for Download Original button
    * implemented migration of existing category refclass data
    * fixed migrations for existing categories and assignments of existing media items to categories
    * getAllTagNameForUserWithCount now respects the pre-filtered categories for media engines
    * added the File slot, which is similar to the PDF slot (now deprecated) but allows any downloadable media type, thus providing a nice way to call attention to other file types

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * the apostrophe:migrate hooks that add blog plugin tables were accidentally disabled
    * categories have been refactored, moving quite a bit of code upstairs to apostrophePlugin

They talked about us
--------------------

  * [Symfony2 PR3](http://www.symfony.it/articoli/327/symfony2-pr3/)
  * [JustMarried : mise en place du projet Symfony2](http://sebastien.porati.me/blog/2010/09/justmarried-mise-en-place-projet-symfony2/)
  * [Interesting symfony plugins: sfBehatPlugin](http://blog.servergrove.com/2010/09/20/interesting-symfony-plugins-sfbehatplugin/)
  * [Symfony CMF](http://www.symfonylab.com/symfony-cmf/)
  * [sfAdminHijackPlugin – Hijacking a symfony admin module to manage doctrine one-to-many relations with JQuery modal dialogs](http://test.ical.ly/2010/09/21/sfadminhijackplugin-hijacking-a-symfony-admin-module-to-manage-doctrine-one-to-many-relations-with-jquery-modal-dialogs/)
  * [Propel 1.6 + phpsh = Awesome CLI to your Database](http://propel.posterous.com/propel-16-phpsh-awesome-cli-to-your-database)
  * [Conférencier à l'OSDC et Forum PHP 2010](http://www.hugohamon.com/en/blog/conferences-osdc-forum-php-2010)
  * [Propel2 and Doctrine2: Together but not scrambled](http://www.jnieto.org/article/propel2_and_doctrine2_together_but_not_scrambled)
  * [A quick start guide for sfImageTransformExtraPlugin (for use with doctrine or propel records)](http://test.ical.ly/2010/09/22/a-quick-start-guide-for-sfimagetransformextraplugin-for-use-with-doctrine-or-propel-records/)
  * [Rilasciato symfony 1.4.7](http://www.symfony.it/articoli/359/rilasciato-symfony-1-4-7/)
  * [Interview with Frantisek Troster and Ludek Vodicka (Inventic)](http://www.symfonylab.com/interview-with-frantisek-troster-and-ludek-vodicka-inventic/)
  * [sfAdminHijackPlugin – How a hijacked symfony admin module will look like](http://test.ical.ly/2010/09/23/sfadminhijackplugin-%E2%80%93-how-a-hijacked-symfony-admin-module-will-look-like/)
  * [To JCR or not: Choosing the right persistence solution for the Symfony CMF](http://www.devorigin.fr/articles/to-jcr-or-not-choosing-the-right-persistence-solution-for-the-symfony-cmf)
  * [Speaking at the International PHP Conference and SymfonyDay](http://www.leftontheweb.com/message/Speaking_at_the_International_PHP_Conference_and_SymfonyDay)
  * [Rilasciato symfony 1.4.8](http://www.symfony.it/articoli/363/rilasciato-symfony-1-4-8/)
  * [Se publican Symfony 1.3.8 y 1.4.8](http://www.symfony.es/2010/09/25/se-publican-symfony-1-3-8-y-1-4-8/)
  * [symfony 1.3.8 and 1.4.8 released and available at ServerGrove](http://blog.servergrove.com/2010/09/25/symfony-1-3-8-and-1-4-8-released-and-available-at-servergrove/)
  * [symfony で Web API を実装するときのポイントいくつか | tech.kayac.com – KAYAC engineers’ blog](http://tyudon.com/blog/?p=19451)
  * [symfony で Web API を実装するときのポイントいくつか](http://tech.kayac.com/archive/api-on-symfony.html)
  * [Here is my 2 cents on Doctrine (ORM)](http://dynamicguy.com/2010/09/here-is-my-2-cents-on-doctrine-orm/)
  * [symfony 1.4を試してみて気になった事](http://d.hatena.ne.jp/d4-1977/20100925/1285428768)
  * [Overview of PHPEdit extension for Symfony](http://www.learnwebdev.com/?p=142)
  * [Symfony mit schnellem Bugfix](http://it-republik.de/php/news/Symfony-mit-schnellem-Bugfix-057058.html)
  * [Mac OS X & Symfony – problem z build-all](http://lukasz.klis.pl/mac-os-x-symfony-problem-z-build-all/)
  * [携帯とスマートフォンでsymfonyのテンプレートを切り替える](http://labs.unoh.net/2010/09/symfony_4.html)
  * [Include partial from app/template directory in symfony](http://ryan.ifupdown.com/2010/09/23/include-partial-from-apptemplate-directory-in-symfony/)
  * [sfMobileIPPluginをsymfony 1.4で使ってみた](http://blog.loadlimits.info/2010/09/sfmobileipplugin%E3%82%92symfony-1-4%E3%81%A7%E4%BD%BF%E3%81%A3%E3%81%A6%E3%81%BF%E3%81%9F/)
  * [[Symfony]Symfony2.0初感](http://d.hatena.ne.jp/perezvon/20100920/1284976964)
