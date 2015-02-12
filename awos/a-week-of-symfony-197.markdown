---
layout: default
title: A week of symfony#197 (4->10 October 2010)
---

A week of symfony #197 (4->10 October 2010)
===========================================

This week the symfony community gathered around the <a href="http://www.symfonyday.com/">Symfony Day 2010</a> conference. The event hosted many insightful sessions and the <a href="http://github.com/symfony-cmf/symfony-cmf/wiki/Post-Symfony-Day-Cologne-2010-Meeting-Notes">Symfony2 CMF meetup</a>. In addition, a new major component of Symfony2 was introduced: the Firewall component, which provides authentication and authoritation for applications.

Development mailing list
------------------------

  * [Symfony2 security feedback](http://groups.google.com/group/symfony-devs/browse_thread/thread/2308fe4e5f9a7dc2)
  * [Symfony2: Preferred languages and culture fallback](http://groups.google.com/group/symfony-devs/browse_thread/thread/fb60300108652cb4)
  * [asset installation](http://groups.google.com/group/symfony-devs/browse_thread/thread/74290e62ae026d23)

symfony 1 development highlights
--------------------------------

Activity summary: 43 changesets, 14 bugs reported, 10 bugs fixed, 7 enhancements suggested, 1 enhancement closed, 2 documentation defects reported, and 13 documentation edits

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [2525998](http://github.com/symfony/symfony/commit/2525998f6e47299438ccf07e6c5c92b4755f66a5 "2525998f6e47299438ccf07e6c5c92b4755f66a5 commit on github"): replaced form field rendering with plain templates
  * [ff683a6](http://github.com/symfony/symfony/commit/ff683a694e37ecf779e1a16b5058666d6443ce85 "ff683a694e37ecf779e1a16b5058666d6443ce85 commit on github"), [3bc3115](http://github.com/symfony/symfony/commit/3bc3115d8c784c5be201d0156a51d6626135a246 "3bc3115d8c784c5be201d0156a51d6626135a246 commit on github"): integrated new data fixtures code
  * [caa9d82](http://github.com/symfony/symfony/commit/caa9d827463a40fe2c1454351218be93b9c10817 "caa9d827463a40fe2c1454351218be93b9c10817 commit on github"): \[HttpFoundation\] added support for attributes in RequestMatcher


New [developers for hire](http://trac.symfony-project.com/trac/wiki/DevelopersForHire)
-----------------------

  * [Scenic City Labs](http://www.ScenicCityLabs.com): is a web application development company with 10+ years of experience. We are currently based in Chattanooga, TN. We use symfony for the majority of our projects but can custom tailer any application to whatever you desire.
  * Tejaswi Sharma \(tej.nri@gmail.com\): I am Tejaswi Sharma and I am working in PHP/MySql/Apache for 4 years and symfony for 2 years. Feel free to contact me if you have any issues in symfony.


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [themeTwentyten](http://www.symfony-project.org/plugins/themeTwentytenPlugin): TwentyTen Wordpress theme version under symfony sfThemePlugin.
  * [sfPrintableForm](http://www.symfony-project.org/plugins/sfPrintableFormPlugin): Make a form printable version.
  * [sfPLValidators](http://www.symfony-project.org/plugins/sfPLValidatorsPlugin): Provides validation of polish specific codes (NIP, Polish tax identification number and Pesel, Polish human identification number)
  * [acHostDependant](http://www.symfony-project.org/plugins/acHostDependantPlugin): provides the ability to have different configuration depending on the hostname.
  * [fpBackup](http://www.symfony-project.org/plugins/fpBackupPlugin): (no description)
  * [pokretWidgetFormDateTimeWithAmPm](http://www.symfony-project.org/plugins/pokretWidgetFormDateTimeWithAmPmPlugin): (no description)

Updated plugins
---------------

  * [sfDoctrineActAsSignable](http://www.symfony-project.org/plugins/sfDoctrineActAsSignable):
    * added sfDoctrineGuardPlugin behavior

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * added query method to fetch tags and tagging counts for various a set of taggable models
    * modified TagTable::queryTagsWithCountsByModel to be more compatible with existing doctrine relations
    * fixed Iterators for escaped arrays stop when a false value is encountered
    * added function to merge two tags

  * [tdCore](http://www.symfony-project.org/plugins/tdCorePlugin):
    * improvements in tdSubpage

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * fixed sorting route generated url
    * added listpanel loader
    * added Listview CheckboxSelection ux and checkbox selection support to ListView
    * updated ListView RowActions css
    * added ListView override to fix a bug with IE (can be removed when ExtJs 3.3.0 is released)
    * added ListView support to batch actions
    * added tasks to create admin modules in an existing plugin

  * [sfPHPUnit2](http://www.symfony-project.org/plugins/sfPHPUnit2Plugin):
    * refactored loading of sfApplicationConfiguration instance
    * added helper method for debugging

  * [sfFormExtra](http://www.symfony-project.org/plugins/sfFormExtra):
    * fixed the impossibility to remove the value for the sfWidgetFormJQueryAutocompleter

  * [srPageChooser](http://www.symfony-project.org/plugins/srPageChooserPlugin):
    * removed srValidatorSlug (deprecated by aValidatorSlug)
    * cleaned up the widget class
    * fixed javascript error on button click
    * allowed for output escaping to be turned on

  * [sfAssetsLibrary](http://www.symfony-project.org/plugins/sfAssetsLibraryPlugin):
    * new helper for ckeditor browser
    * updated readme with instructions how to use sfAssetsLibraryPlugin as CKEditor file browser without other Plugin

  * [sfCKEditor](http://www.symfony-project.org/plugins/sfCKEditorPlugin):
    * updated readme waiting for deploymet of sfAssetsLibraryPlugin with CK Editor addon

  * [sfI18nFormExtractor](http://www.symfony-project.org/plugins/sfI18nFormExtractorPlugin):
    * now translates help messages from forms

  * [sfAtosPayment](http://www.symfony-project.org/plugins/sfAtosPaymentPlugin):
    * fixed some syntax bugs

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * initial version of aTagAdmin
    * styled the feedback you get after using the Replace File feature
    * if the update's timestamp is no good, don't attempt to strtotime() it
    * moved the ajax submit function to a.js to get it out of the edit partial
    * created apostrophe.linkToRemote so we can begin replacing all of those inline jq_link_to_remote() functions
    * working on getting editing working correctly in the four-up view in Media
    * added disqus partial includes to layout.php
    * made it easier to override default behavior of aCategoryAdmin
    * page editing permissions have been completely overhauled (a big win for large sites with many editors)
    * slideshow slots now support displaying everything with certain categories and tags as an alternative to browsing for individual images
    * removed Image slot
    * renamed Slideshow slot in BaseaTools as the first step to unifying aImage and aSlideshow
    * updated instructions for choosing a photo or photos with the slideshow slot
    * new aMediaItem::getImageAvailable method is preferred to checking for a width before trying to display a thumbnail
    * fixed some of the default dimensions issues in the button slot
    * adjusted four-up behavior for non-images
    * created active states for the View settings so you know which one is selected
    * the new view permissions are roughed in and working
    * fixed potential bug in category merging
    * added category merging to tag admin
    * moved slide show image ordering into Slot classes

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * integrated disqus comments
    * added orderBy to aEventActions:buildQuery
    * added 'Preview' to the Blog and Events admin
    * added a max_per_page setting to aBlog and aEvent in app.yml
    * BlogItem::getMediaForAreas() now respects slide show ordering


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [Blidoo](http://www.blidoo.com/): \(English\) a generalist classified ads site
  * [dramadance.pl](http://www.dramadance.pl/): \(Polish\) website of an entertainment company
  * [EticWeb](http://www.avendresurle.net/): \(French\) our site offers to reduce the carbon footprint of individuals while minimizing travel-related purchases, sales and barter of goods and services
  * [Reflector Guide](http://www.reflector-guide.com): \(English, Spanish, Finnish, Russian\) site about pedestrian reflectors
  * [Työkyvyntuki](https://www.tyokyvyntuki.fi): \(Finnish\) work ability service for medium sized companies
  * [MediaBurse.ru](http://mediaburse.ru): \(Russian\) place where journalists and publishers buy\sell articles
  * [InterScientia.com](http://interscientia.com): \(English, Finnish, French, Russian, Swedish\) a Workshop for All Men And Women Seeking to Share Knowledge Across Borders

New [symfony bloggers](http://trac.symfony-project.com/trac/wiki/SymfonyBloggers)
--------------------

  * [Synofony](http://sf.khepin.com/) \([feed](http://sf.khepin.com/feed/)\) \(English\)

They talked about us
--------------------

  * [How to make symfony use a different login page depending on your current module/action?](http://test.ical.ly/2010/10/04/how-to-make-symfony-use-a-different-login-page-depending-on-your-current-moduleaction/)
  * [Symfony filter forms and related tables](http://sf.khepin.com/2010/10/symfony-filter-forms-and-related-tables/)
  * [Easy list ordering / sorting on any field](http://sf.khepin.com/2010/10/easy-list-ordering-sorting-on-any-field/)
  * [Logging MongoDB queries using Symfony2 and Doctrine ODM](http://blog.servergrove.com/2010/10/05/logging-mongodb-queries-using-symfony-2-and-doctrine-odm/)
  * [SfDoctrineGuardPlugin bug: Unknown method SfGuardUserTable::retrieveByUsername](http://www.kennethvr.be/blog/2010/10/05/sfdoctrineguardplugin-bug-unknown-method-sfguardusertableretrievebyusername/)
  * [symfony & Doctrine behavior review](http://symfony-world.blogspot.com/2010/10/symfonydoctrine-behavior-review.html)
  * [How to define a default value in your schema.yml when using the Doctrine data type Array](http://test.ical.ly/2010/10/06/how-to-define-a-default-value-in-your-schema-yml-when-using-the-doctrine-data-type-array/)
  * [Doctrine query caching causing 'Invalid parameter number' error for queries using 'IN ?'](http://jlcoady.net/symfony/doctrine-query-caching-causing-invalid-parameter-number-error)
  * [Thank you for PHPMatsuri!](http://pugi-pogi.blogspot.com/2010/10/thank-you-for-phpmatsuri.html)
  * [Setting up a symfony project with PHPUnit on Hudson](http://dev.esl.eu/blog/2010/10/06/setting-up-a-symfony-project-and-phpunit-on-hudson/)
  * [Ocari, le CMS français orienté presse, pour les gens de la presse](http://www.silicon.fr/ocari-le-cms-francais-%C2%AB-oriente-presse-pour-les-gens-de-la-presse-%C2%BB-41835.html)
  * [Projet planté ? Demandez l'aide d'un gourou de l’open source](http://www.01net.com//editorial/520821/projet-plante-demandez-laide-dun-gourou-de-l-open-source/)
  * [Symfony Parallel Content Delivery](http://www.saynotoflash.com/archives/symfony-parallel-content-delivery/)
  * [Symfony – file uploads with custom names and paths](http://www.whiteoctober.co.uk/blog/2010/10/07/symfony-file-uploads-with-custom-names-and-paths/)
  * [Creating indexes for your Doctrine ODM documents with Symfony 2](http://blog.servergrove.com/2010/10/07/creating-indexes-for-your-doctrine-odm-documents-with-symfony-2/)
  * [Relaunch der softSCIENCE-Homepage](http://www.inar.de/blog/webwelt/20101007/relaunch-der-softscience-homepage.html)
  * [symfony day 2010 in Cologne](http://test.ical.ly/2010/10/08/symfony-day-2010-in-cologne/)
  * [JustMarried : mise à jour de Symfony2](http://sebastien.porati.me/blog/2010/10/justmarried-mise-a-jour-de-symfony2/)
  * [El estado actual de Symfony2](http://www.symfony.es/2010/10/10/el-estado-actual-de-symfony2/)
  * [Doctrine and Zend Framework](http://www.symfonylab.com/doctrine-and-zend-framework/)
  * [Extendiendo el sfActions de Symfony 2/2](http://blog.micayael.com/2010/10/07/extendiendo-el-sfactions-de-symfony-ii/)
  * [Formularios en Symfony](http://www.maquiavelica.com.ar/formularios-en-symfony/)
  * [Symfony, cron and HTML emails (getPartial from cron)](http://codesauce.com/2010/10/07/symfony-cron-and-html-emails-getpartial-from-cron/)
  * [Come gestire pagine statiche con symfony](http://www.ftassi.com/2010/10/howto-gestire-pagine-statiche-symfony.html)
  * [絵文字のためにsymfonyのカスタムハンドラーを作ってみました](http://labs.unoh.net/2010/10/symfony.html)
  * [Add properties to a relationship – Dealing with forms in symfony 1.4](http://www.michelsalib.com/2010/10/add-properties-to-a-relationship-dealing-with-forms-in-symfony-1-4/)
  * [まずSymfony中。](http://onoki.jp/archives/1230)
  * [Symfony 1.4 quick commands](http://botchedcode.com/2010/10/08/symfony-1-4-quick-commands/)
  * [Desenvolvendo um módulo de contato no Symfony 1.4](http://www.fonini.net/posts/51-desenvolvendo-um-modulo-de-contato-no-symfony-14)
  * [Установка и конфигурирование php-фреймворка symfony](http://www.learnwebdev.com/?p=197)
  * [Dialogos con Jquery y symfony](http://www.angelontheweb.com/es/dialogos-con-jquery-y-symfony/)
  * [5 pasos para trasladar aplicación Symfony a ambiente de producción](http://symfony.cl/blog/2010/10/5-pasos-para-trasladar-aplicacion-symfony-a-ambiente-de-produccion/)
  * [Doctrine Nested Sets in Symfony](http://www.ausgebloggt.de/2010/10/05/doctrine-nested-sets-in-symfony/)
  * [Saving Multiple Objects With One Form in symfony](http://jasonswett.net/saving-multiple-objects-with-one-form-in-symfony/)
  * [symfony框架实战视频：60分钟开发一个CMS](http://lampstudy.net/post/t201010/symfony-framework-develop-a-cms.html)
  * [Creating an arbitrary pulldown filter](http://symfony-blog.driebit.nl/2010/10/creating-an-arbitrary-pulldown-filter/)
