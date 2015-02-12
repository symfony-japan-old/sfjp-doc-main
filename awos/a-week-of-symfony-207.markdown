---
layout: default
title: A week of symfony#207 (13->19 December 2010)
---

A week of symfony #207 (13->19 December 2010)
=============================================

Symfony2 committed this week two huge changesets related to the Security component: [fixed user refreshing after unserialization](https://github.com/symfony/symfony/commit/3c692bd1608eb2bef30f74343f476a5e045ab38b) and [added authentication trust resolver](https://github.com/symfony/symfony/commit/abe804726279148cdebae017550308c7fc21114b). It also committed two small but important tweaks: the new hash syntax for Twig templates and the new format for XML attribute names.

Development mailing list
------------------------

  * ["[Symfony2] hashing password"](https://groups.google.com/forum/?pli=1#!topic/symfony-devs/6xLFKlasiMw)
  * ["[Symfony2] RFC: Merging field groups into a form"](https://groups.google.com/forum/?pli=1#!topic/symfony-devs/2PRlTxIOKb8)
  * ["Symfony2: what is the recommended way to start a new project"](https://groups.google.com/forum/?pli=1#!topic/symfony-devs/zFvPZ9C4WPU)
  * ["[Symfony2] password field prefill"](https://groups.google.com/forum/?pli=1#!topic/symfony-devs/IFhlASNJiJY)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [984a857](http://github.com/symfony/symfony/commit/984a857a96252ce3c355554e2ab133649f743b70 "984a857a96252ce3c355554e2ab133649f743b70 commit on github"): \[Validator\] fixed the static method loader to not repeat the loading when the static method is in the parent classes
  * [131b3fe](http://github.com/symfony/symfony/commit/131b3fe3730ba979eb57d4e3d7d683be472da09c "131b3fe3730ba979eb57d4e3d7d683be472da09c commit on github"): \[Form\] refactored Field and FieldGroup to facilitate modifications in subclasses
  * [e80aa9a](http://github.com/symfony/symfony/commit/e80aa9a5ab9643ad7dbf85727cf4188e58cda6ed "e80aa9a5ab9643ad7dbf85727cf4188e58cda6ed commit on github"): \[Form\] fixed the data in a CollectionField is resized down if fields are removed
  * [f73b6b4](http://github.com/symfony/symfony/commit/f73b6b4e1c5c563d31176c9de1fdeb962a94d0e3 "f73b6b4e1c5c563d31176c9de1fdeb962a94d0e3 commit on github"): \[PropertyPath\] fixed usage of __get() and __set() when accessing properties that exist in the object but are not public
  * [1b2ca25](http://github.com/symfony/symfony/commit/1b2ca259f12cf7de86626c78d2d8b1573e8ddf85 "1b2ca259f12cf7de86626c78d2d8b1573e8ddf85 commit on github"), [af291bb](http://github.com/symfony/symfony/commit/af291bb0f1c9032adaa96790829cbe04077a8234 "af291bb0f1c9032adaa96790829cbe04077a8234 commit on github"): \[Validator\] fixed string-based constraint validators to accept empty values
  * [e49cc36](http://github.com/symfony/symfony/commit/e49cc363395ef02f7dc68ced1726f69e08429492 "e49cc363395ef02f7dc68ced1726f69e08429492 commit on github"): \[DependencyInjection\] fixed interfaces can now also be defined on containers which are built with an Extension and interface injection can also be used on classes that require constructor arguments
  * [48e3053](http://github.com/symfony/symfony/commit/48e30537c407db8a645a3e18c854a13b9d9b1873 "48e30537c407db8a645a3e18c854a13b9d9b1873 commit on github"): added exception when a loaded YAML resource is not an array
  * [504463c](http://github.com/symfony/symfony/commit/504463c30769264e4cefc32f99018d9000e7c51c "504463c30769264e4cefc32f99018d9000e7c51c commit on github"): \[Routing\] refactored PHP generator dumper code
  * [7cb8dca](http://github.com/symfony/symfony/commit/7cb8dca04dad72679e3615e3b45ab067c34494bf "7cb8dca04dad72679e3615e3b45ab067c34494bf commit on github"), [5857576](http://github.com/symfony/symfony/commit/5857576024739919dd03dd9f204bb3446cacfc01 "5857576024739919dd03dd9f204bb3446cacfc01 commit on github"): \[Routing\] added . as a valid character in route names
  * [a7c8157](http://github.com/symfony/symfony/commit/a7c81577c7f26cbbf34df49d200d496c91f825e2 "a7c81577c7f26cbbf34df49d200d496c91f825e2 commit on github"): \[HttpFoundation\] added a way to retrieve raw body from a request
  * [abe8047](http://github.com/symfony/symfony/commit/abe804726279148cdebae017550308c7fc21114b "abe804726279148cdebae017550308c7fc21114b commit on github"): added authentication trust resolver
  * [30f231d](http://github.com/symfony/symfony/commit/30f231deaf5208b2f4854b3f550259a15f8fbebd "30f231deaf5208b2f4854b3f550259a15f8fbebd commit on github"): moved default form template to the DIC config
  * [e6d0385](http://github.com/symfony/symfony/commit/e6d03857780abf17d02ae2b76e90d76d370ba302 "e6d03857780abf17d02ae2b76e90d76d370ba302 commit on github"): \[HttpFoundation\] fixed Request::create() when using HTTPS and getUri()/getPathForUri() when script name should be removed
  * [02a92ec](http://github.com/symfony/symfony/commit/02a92ec297cc1bbc19cabc6103f4b708bfe3771c "02a92ec297cc1bbc19cabc6103f4b708bfe3771c commit on github"): \[TwigBundle\] added autoescape option in Twig configuration
  * [84c7496](http://github.com/symfony/symfony/commit/84c749656543265d966d105cdefa2aea2583f0ae "84c749656543265d966d105cdefa2aea2583f0ae commit on github"): \[DoctrineBundle\] fixed createOrmProxyDirectory method
  * [6970a46](http://github.com/symfony/symfony/commit/6970a46b84072b835a90612e19fb8109f1f78738 "6970a46b84072b835a90612e19fb8109f1f78738 commit on github"): updated Twig templates for the new hash syntax
  * [c9f08c0](http://github.com/symfony/symfony/commit/c9f08c0a68446ef27e5ec089c9ec5b85ba78b35a "c9f08c0a68446ef27e5ec089c9ec5b85ba78b35a commit on github"): changed all XML attribute names to take - instead of _ (everything should be consistent now)
  * [3c692bd](http://github.com/symfony/symfony/commit/3c692bd1608eb2bef30f74343f476a5e045ab38b "3c692bd1608eb2bef30f74343f476a5e045ab38b commit on github"): fixed user refreshing after unserialization

New [developers for hire](http://trac.symfony-project.com/trac/wiki/DevelopersForHire)
-----------------------

  * e-Zest Solutions \(http://www.e-zest.net/php-software-development.html\): is a leading PHP software development company from India. With a bunch of dedicated and expert developers in LAMP (Linux, Apache, MySQL and PHP) technology makes e-Zest a great partner for low cost open source technology development company.


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfWindguru](http://www.symfony-project.org/plugins/sfWindguruPlugin): is an interface to windguru.cz website. It allows displaying forecasts fetched from windguru website.
  * [sfRADIUSAuth](http://www.symfony-project.org/plugins/sfRADIUSAuthPlugin): provides means to authenticate sfGuard Users against a RADIUS server.
  * [sfUserVoice](http://www.symfony-project.org/plugins/sfUserVoicePlugin): is an interface to uservoice.com feedback. It allows 'feedback' popup tab fetched from uservoice.com website.

Updated plugins
---------------

  * [gjPositions](http://www.symfony-project.org/plugins/gjPositionsPlugin):
    * released the first stable version

  * [sfAntiBruteForce](http://www.symfony-project.org/plugins/sfAntiBruteForcePlugin):
    * released the fist version that handles basic functionnalities on file storage
    * improved security
    * fixed bug when cache directory not created
    * added license and readme files

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * modified form partial and stylesheets

  * [ncPropelChangeLogBehavior](http://www.symfony-project.org/plugins/ncPropelChangeLogBehaviorPlugin):
    * added a method to determine whether an object has any changelog elements
    * updated some minor typos and made some little improvements

  * [ggEmail](http://www.symfony-project.org/plugins/ggEmailPlugin):
    * promoted the plugin to stable

  * [sfHttpHeaderCache](http://www.symfony-project.org/plugins/sfHttpHeaderCachePlugin):
    * don't need the routing object anymore

  * [sfGuardExtra](http://www.symfony-project.org/plugins/sfGuardExtraPlugin):
    * enforced strong password with min length of 8

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * changed the markup for tags output by the multipleSelect a little bit

  * [sfProjectAnalyser](http://www.symfony-project.org/plugins/sfProjectAnalyserPlugin):
    * when the plugin_to_parse config is empty, no plugin is analysed (instead of all plugins)
    * corrected bad warning reporting when using validateXXX methods and the compat1.0 plugin
    * added a config option for the compat10 mode
    * fixed a bug with report generation date
    * added a detected value 'all' for the config parameter [plugin][to_parse] to parse all the plugins of the project
    * updated package and README with new roadmap and ideas

  * [sfGeshi](http://www.symfony-project.org/plugins/sfGeshiPlugin):
    * geshi customization can be made in app.yml file

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * fixed date and time parsing to be more tolerant so the add to google calendar button always works as expected
    * added Add to iCal, Outlook, etc. links for events
    * added vcalendar support for Outlook 2003
    * removed the separate partial for event title and slug editing since it was only used on the first load and was not different in any case
    * moved the New Event / New Blog Post buttons into the sidebar
    * created _meta partials for bundled Blog and Events templates
    * updated markup for Blog and Events bundled templates, showSuccess, and indexSuccess to be more consistent between each other
    * brought tags into Events template
    * updated default time set for newly created events
    * updated blog and events templates to better share a single _addThis partial
    * updated blog and events templates to better share a single _tags partial
    * updated sidebar markup to use a_button helpers for tags
    * started aBlogConstructor JS modeled after a.js so we can build upon it as the blog evolves
    * fixed bug with saving event engine settings
    * removed query orderBy in blog and event actions
    * added default ordering to createQuery in Event and Post tables
    * fixed the slug got wiped out on every save of the blog post / event metadata form
    * updated Blog / Events _sidebars to share markup more closely with Media _browser
    * events and actions engines now support alternate page templates
    * reorganized the blog and events sidebar form so the status field is consistent with the author field

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * aDate::normalize now has an optional timeOnly flag (when this flag is true, only the offset in seconds from midnight is returned)
    * removed include_stylesheets and include_javascripts calls at the top of the ajaxUpdateSlot partial
    * published_at is now set when publishing pages
    * clarified that aSlot::getText() should return real UTF-8 plaintext, not entity-esscaped text
    * implemented aString::toVcal(), which returns a string cleaned up to be legal in a vcal or ical .vcs or .ics file
    * aHtml::toPlaintext converts &nbsp; to a regular space rather than a unicode nonbreaking space
    * help text for the categories list in user admin
    * admin generator templates now generate save-and-list, cancel and delete buttons and label them as save, cancel and delete, matching common user interface standards
    * sidebar buttons are styled properly for users, groups, permissions
    * implemented aPage::getAllSlots() method allowing easy access to all current slots for the page in a neatly structured nested array
    * fixed the Popup login form to use menuToggle like every other popup
    * fixed styling for cancel button (missing X)
    * updated the a-rss-feed button
    * created a class for a-controls to stack them vertically
    * started to update media _browser partial to match the blog sidebar
    * uploaded thumbnails are once again allowed (though not mandatory) for videos from services we don't support directly
    * updated the markup in Media _browser so that it is consistent with the sidebars in Blog and Events
    * made the Multiple Select values behave like the rest of our similar interfaces
    * engines can now easily support multiple variations individually selectable as "page types."
    * the page settings form was refactored removing quite a bit of javascript code



New [symfony bloggers](http://trac.symfony-project.com/trac/wiki/SymfonyBloggers)
--------------------

  * [Jason Longshore](http://jsltbh.blogspot.com/) \([feed](http://jsltbh.blogspot.com/feeds/posts/default)\) \(English\)
  * [Micayael's blog](http://blog.micayael.com/category/symfony) \([feed](http://blog.micayael.com/category/symfony/feed/)\) \(Spanish\)

They talked about us
--------------------

  * [10 Steps I do to fix a bug in a symfony plugin](http://test.ical.ly/2010/12/13/10-steps-i-do-to-fix-a-bug-in-a-symfony-plugin/)
  * [Propel Gets Better at Naming Things](http://propel.posterous.com/propel-gets-better-at-naming-things)
  * [Speaking at Symfony Live!](http://blog.marcw.net/conference/speaking-at-symfony-live-2011/)
  * [First stable release of gjPositionsPlugin for easy page composition with symfony and doctrine](http://test.ical.ly/2010/12/14/first-stable-release-of-gjpositionsplugin-for-easy-page-composition-with-symfony-and-doctrine/)
  * [Easily generate excel files from a symfony action](http://sf.khepin.com/2010/12/easily-output-excel-files-from-a-symfony-application/)
  * [Custom values in sfWidgetFormDoctrineChoice](http://www.symfonylab.com/custom-values-in-sfwidgetformdoctrinechoice/)
  * [Petit projet de série d’articles sur Symfony2/ESI](http://sebastien.porati.me/blog/2010/12/petit-projet-de-serie-articles-sur-symfony2-esi/)
  * [Sensio Labs recrute de nouveaux talents!](http://www.hugohamon.com/en/blog/sensio-labs-recrute-de-nouveaux-talents)
  * [Propel Adds Support For Database Schemas in Version 1.6](http://propel.posterous.com/propel-adds-support-for-database-schemas-in-v)
  * [My technology setup for the next project](http://test.ical.ly/2010/12/16/my-technology-setup-for-the-next-project/)
  * [Sensio Labs annonce les conférences Symfony Live 2011](http://www.nexen.net/articles/communique_de_presse/19947-sensio_labs_annonce_les_conferences_symfony_live_2011.php)
  * [ServerGrove sponsoring Symfony Live 2011 / SF & Paris](http://blog.servergrove.com/2010/12/17/servergrove-sponsoring-symfony-live-2011-sf-paris/)
  * [postDelete in doctrine](http://www.symfonylab.com/postdelete-in-doctrine/)
  * [Running Symfony 1.4 with MS SQL Server 2008](http://tecnofuenteabierta.blogspot.com/2010/12/running-symfony-14-with-ms-sql-server.html)
  * [symfony で普段使っているpluginをまとめてみた](http://d.hatena.ne.jp/kopug/20101218/1292685587)
  * [vim-symfony ver 0.10 についてのまとめ【決定版】](http://d.hatena.ne.jp/sugarbabe335/20101218/1292602452)
  * [symfonyのインストール](http://d.hatena.ne.jp/kobakey/20101213/1292258310)
  * [フィードバックサイクルを素早く回すために](http://labs.unoh.net/2010/12/for-quick-feedback-cycle.html)
  * [Atelier 1: Symfony Framework](http://hanichalouati.blogspot.com/2010/12/atelier-1-symfony-framework.html)
  * [フォームへカレンダーから日付を入力](http://d.hatena.ne.jp/hiroiwa/20101213/1292227966)
  * [symfony2をローカルで動作させる環境をサクッと作る](http://d.hatena.ne.jp/jiskay/20101214/1292261989)
  * [Symfony2 + MongoDB ODM を使ってみる](http://d.hatena.ne.jp/ja9/20101214/1292348839)
  * [symfony1.4(フレームワーク)について](http://maxura.blog62.fc2.com/blog-entry-187.html)
  * [Symfony2 sandboxコミッターになった瞬間](http://hiroki.jp/2010/12/16/973/)
  * [sfDoctrineMasterSlavePluginを使う時のTips](http://d.hatena.ne.jp/ken39arg/20101219/1292734152)
  * [AdminGeneratorで生成されるファイル](http://d.hatena.ne.jp/moroto1122/20101214/1292319464)
