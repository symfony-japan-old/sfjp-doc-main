A week of symfony #202 (8->14 November 2010)
============================================

This week, the symfony community held <a href="http://trac.symfony-project.org/wiki/Symfony2IRCMeetingLogs">the first Symfony2 IRC meeting</a>. From now on, these meetings will discuss every week several topics chosen by the community, such as best practices and solutions for very specific issues.
 
Development mailing list
------------------------

  * [Symfony2 recent best practices](http://groups.google.com/group/symfony-devs/browse_thread/thread/24c851f77783403c)
  * [Weekly IRC meetings](http://groups.google.com/group/symfony-devs/browse_thread/thread/3bfdc24722e427eb)
  * [Generating entities problem](http://groups.google.com/group/symfony-devs/browse_thread/thread/f5c9246bbbc52908)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [1e13ecb](http://github.com/symfony/symfony/commit/1e13ecb5f3e27de1a1ee078955448beabfba9d89 "1e13ecb5f3e27de1a1ee078955448beabfba9d89 commit on github"): \[TwigBundle\] split the route tag to 2 tags: path and url
  * [6aacfa3](http://github.com/symfony/symfony/commit/6aacfa321698d95109bd86cd7ecc2ce0c6676a52 "6aacfa321698d95109bd86cd7ecc2ce0c6676a52 commit on github"): fixes a bug where in most cases cookies with path / were not set properly
  * [4fc1031](http://github.com/symfony/symfony/commit/4fc10310efd5d1de1dd74cd28b9da9a665823966 "4fc10310efd5d1de1dd74cd28b9da9a665823966 commit on github"): \[DoctrineBundle\] added callbacks to override the default serialization and deserialization of the CollectionToStringTransformer
  * [52ec875](http://github.com/symfony/symfony/commit/52ec8752d89882dd9978a76e954615a0e3d1f7d5 "52ec8752d89882dd9978a76e954615a0e3d1f7d5 commit on github"): \[TwigBundle\] when route_attributes is null an exception is raised
  * [a471f65](http://github.com/symfony/symfony/commit/a471f6575945ea44eac333cbb9ae87dd016004a3 "a471f6575945ea44eac333cbb9ae87dd016004a3 commit on github"): \[HttpKernel\] tweaked HttpKernelInterface
  * [4d4f9f3](http://github.com/symfony/symfony/commit/4d4f9f344ee882f5d0cab51ec5cd9395a4d7642a "4d4f9f344ee882f5d0cab51ec5cd9395a4d7642a commit on github"): added request attributes in the request data collector and web profiler
  * [6f28511](http://github.com/symfony/symfony/commit/6f28511ee42edf4f06946f53edfa890c1bf07fa4 "6f28511ee42edf4f06946f53edfa890c1bf07fa4 commit on github"): \[Form\] added type for FileField class
  * [d7d4880](http://github.com/symfony/symfony/commit/d7d4880a90a4bd5c6dff98393e08c31bf99c6610 "d7d4880a90a4bd5c6dff98393e08c31bf99c6610 commit on github"): \[TwigBundle\] updated filters for the latest version of Twig
  * [7b02766](http://github.com/symfony/symfony/commit/7b027663734e398ab0ea076fc67d455d49d48bef "7b027663734e398ab0ea076fc67d455d49d48bef commit on github"), [51a3d0b](http://github.com/symfony/symfony/commit/51a3d0ba6a5f5d97887f6d424e411deffd53ed61 "51a3d0ba6a5f5d97887f6d424e411deffd53ed61 commit on github"): fixed session management (the Session is an optional dependency of the Request; when duplicating a request, the session is shared between the parent and the child; reading from the session does not start the session anymore; refactored configuration)
  * [4cd5b2b](http://github.com/symfony/symfony/commit/4cd5b2b1ff9f2c0223b1722a84d21b35fcf315e5 "4cd5b2b1ff9f2c0223b1722a84d21b35fcf315e5 commit on github"): \[WebProfilerBundle\] fixed redirection interceptions (we must keep as many headers as possible)
  * [bfae4ad](http://github.com/symfony/symfony/commit/bfae4ad86cd58737346864ca475104f87adeb66e "bfae4ad86cd58737346864ca475104f87adeb66e commit on github"): \[Form\] PercentField fixed option collision
  * [6f034d2](http://github.com/symfony/symfony/commit/6f034d2c80183309711c6860a4a2ac7926c3b602 "6f034d2c80183309711c6860a4a2ac7926c3b602 commit on github"): \[FrameworkBundle\] make the use_forward option of FormAuthenticationListener configurable
  * [efed600](http://github.com/symfony/symfony/commit/efed6005cbc34c3e3a872bf91bfc39d0be476ad5 "efed6005cbc34c3e3a872bf91bfc39d0be476ad5 commit on github"): \[DependencyInjection\] fixed PHP dumper (in the dumped PHP class, we must use get() and not get*Service() methods to get services)
  * [5860bdd](http://github.com/symfony/symfony/commit/5860bdd75adc3f1cecdc0f3b7149dab26b37b05b "5860bdd75adc3f1cecdc0f3b7149dab26b37b05b commit on github"): \[FrameworkBundle\] re-added a fake request service so that you can rely on it when defining services with a dependency on it
  * [f5b451f](http://github.com/symfony/symfony/commit/f5b451f5b93f80a1d4bc01503e5e49b317106388 "f5b451f5b93f80a1d4bc01503e5e49b317106388 commit on github"): \[Form\] fixed MoneyToLocalizedStringTransformer and added tests
  * [4c340c5](http://github.com/symfony/symfony/commit/4c340c5cc989609066c141f06205b9bb51aef498 "4c340c5cc989609066c141f06205b9bb51aef498 commit on github"): \[Form\] fixed forms grouped validation
  * [a198bbc](http://github.com/symfony/symfony/commit/a198bbcf43f2b2d4d671046f55f6e4f615829c73 "a198bbcf43f2b2d4d671046f55f6e4f615829c73 commit on github"): \[Form\] throw an exception if session_id() is empty when a csrf token is generated
  * [48b3e92](http://github.com/symfony/symfony/commit/48b3e92504357eabe14dc6f52adeb1614addd4e6 "48b3e92504357eabe14dc6f52adeb1614addd4e6 commit on github"): \[Form\] fixed: parent::configure() should always be called after adding options to overrule options in the parent class
  * [69cd21d](http://github.com/symfony/symfony/commit/69cd21d8be484fe2f351c1ea0f153cc62ea24e19 "69cd21d8be484fe2f351c1ea0f153cc62ea24e19 commit on github"): \[Validator\] fixed annotation loader to not add parent constraints twice

Documentation
-------------

  * New <a href="http://trac.symfony-project.org/wiki/Symfony2IRCMeetingLogs">Symfony2 IRC Meeting Logs</a> page

New [job postings](http://trac.symfony-project.com/trac/wiki/JobPostings)
----------------

  * PHP developer with Symfony experience at [Second2](http://www.second2.com) - full-time based in Beaconsfield, United Kingdom - Contact: jon.busby [at] second2 [dot] com
  * Symfony + PHP/XML developer at [Agsmart](http://www.agsmart.com.au) -  - Contact: mriddell@agsmart.com.au

New [developers for hire](http://trac.symfony-project.com/trac/wiki/DevelopersForHire)
-----------------------

  * [Webmil](http://webmil.com.ua): web development studio based in Ivano-Frankivsk, Ukraine. We use all privileges of symfony framework. Usage of doctrine orm and symfony lets us to gain good results in short terms. CLI and work with model layer are very fast flexible. I18n and yaml are a great plus too. Usually it takes us 1-2 weeks to create new website from scratch including web-design stage.


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [smagEntityLocking](http://www.symfony-project.org/plugins/smagEntityLockingPlugin): Locks Objects by Route. If someone edits an Object no other user can access the route with the same ID to edit the Object too.
  * [sfPinba](http://www.symfony-project.org/plugins/sfPinbaPlugin): Allow monitor each request with Pinba.
  * [sfMailTemplate](http://www.symfony-project.org/plugins/sfMailTemplatePlugin): (no description)
  * [sfPropelCustomSelect](http://www.symfony-project.org/plugins/sfPropelCustomSelectPlugin): provides a capability to select arbitrary columns in propel, without loosing the power of ORM.
  * [dcOAIServiceProvider](http://www.symfony-project.org/plugins/dcOAIServiceProviderPlugin): provides an implementation of an OAI-PMH Service Provider.

Updated plugins
---------------

  * [sfDoctrineGuard](http://www.symfony-project.org/plugins/sfDoctrineGuardPlugin):
    * updated russian translation

  * [sfPhpExcel](http://www.symfony-project.org/plugins/sfPhpExcelPlugin):
    * updaated svn externals of PHPExcel library to 1.7.4

  * [ddOnlineStore](http://www.symfony-project.org/plugins/ddOnlineStorePlugin):
    * extended actions in a base actions file
    * the capacity field in product is not available by default
    * the product details now shows in a popup for jquery fancybox
    * change the label of the button that saves and adds another category

  * [spyMenu](http://www.symfony-project.org/plugins/spyMenuPlugin):
    * fixed bugs in renderer

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * updated jquery_search.js
    * updated ajax dependence JavaScript
    * added pagination to jquery search widget
    * updated jquery search action and template

  * [sfExtjs3](http://www.symfony-project.org/plugins/sfExtjs3Plugin):
    * fixes for dev mode detection to enable debug libraries

  * [sfEnvironmentFixtures](http://www.symfony-project.org/plugins/sfEnvironmentFixturesPlugin):
    * updated documentation
    * fixed recursive fixture loading

  * [pkContextCMS](http://www.symfony-project.org/plugins/pkContextCMSPlugin):
    * made some changes to help with page validation

  * [pkToolkit](http://www.symfony-project.org/plugins/pkToolkitPlugin):
    * removed jquery.autogrow.js from use
    * added jquery.simpleautogrow.js because it's more modern and doesn't throw errors in IE
    * some general cleanup to help with page validation

  * [sfDoctrineApply](http://www.symfony-project.org/plugins/sfDoctrineApplyPlugin):
    * the uppercase value of the method attribute prevented a page with these forms from validating

  * [sfGeshi](http://www.symfony-project.org/plugins/sfGeshiPlugin):
    * GeSHi settings are now defined in app.yml file
    * updated documentation

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * references to DoctrineException corrected to sfDoctrineException

  * [sfAssetsLibrary](http://www.symfony-project.org/plugins/sfAssetsLibraryPlugin):
    * added validation rule for reserved folder name "thumbnail"

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * improvements to formpanel components

  * [sfThrift](http://www.symfony-project.org/plugins/sfThriftPlugin):
    * tweaked code
    * added documentation, comments and changelog

  * [sfTangoIcons](http://www.symfony-project.org/plugins/sfTangoIconsPlugin):
    * added category, device, emblem, emot, mime type, place and status models
    * updated documentation
    * fixed bug with double start timer

  * [WebPurify](http://www.symfony-project.org/plugins/WebPurifyPlugin):
    * updated the web service endpoint URL

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * added queryWithPage to BlogItemTable
    * fixed a bug in 1.4 blog/events pertaining to engine pages without selected categories and tags
    * added slideshow option for idSuffix to the normalView for each of these slots

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * apostrophe:demo-fixtures runs quietly now
    * demo fixtures load quietly
    * fixed bug that broke slideshow navigation
    * removed all unused jquery plugins
    * removed all unused CSS files
    * updated autogrow plugin for plaintext/rawhtml slots
    * updated aHelper to only include the resources we are using
    * fixed the bugginess with the slideshowSlot
    * cleaned up / rewrote parts of the slideshowSlot js
    * created jQuery triggers for advancing the slideshow
    * created the ability to crossfade between images instead of doing the hide / fadeIn behavior we have been using
    * added a idSuffix to the slideshow so other slots like the blogSlot that use the slideshow component can append unique identifiers to the slideshow

  * [sfJunaioChannel](http://www.symfony-project.org/plugins/sfJunaioChannelPlugin):
    * fixed XML helper class
    * updated documentation


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [SocialCompare.com](http://socialcompare.com/): \(English, French\) online community to create, update and share comparisons about everything

New [symfony bloggers](http://trac.symfony-project.com/trac/wiki/SymfonyBloggers)
--------------------

  * [symfony tricks](http://symfonytricks.blogspot.com) \([feed](http://symfonytricks.blogspot.com/feeds/posts/default)\) \(English\)

They talked about us
--------------------

  * [sfDoctrineRestGeneratorPlugin](http://www.symfonylab.com/sfdoctrinerestgeneratorplugin/)
  * [[best practice] How to distribute symfony plugins when you’re working with GitHub](http://test.ical.ly/2010/11/08/best-practice-how-to-distribute-symfony-plugins-when-you-are-working-with-github/)
  * [Nouveau site perso (symfony 1.4)](http://www.experimental-symfony.com/sfSimpleBlog/show/stripped_title/nouveau-site-perso-symfony-1-4)
  * [既存の稼働中DBのテーブルに、カラムを追加](http://symfony.jobweb.jp/?p=855)
  * [How to avoid all that cache clearing when developing a symfony admin theme](http://test.ical.ly/2010/11/09/how-to-avoid-all-that-cache-clearing-when-developing-a-symfony-admin-theme/)
  * [Selectbox para escolher cidade de acordo com o estado utilizando widgets e symfony 1.4 (Propel/Doctrine)](http://www.symfonybr.com/2010/11/09/selectbox-para-escolher-cidade-de-acordo-com-o-estado-utilizando-widgets-e-symfony-1-4-propeldoctrine/)
  * [SF Symfony Meetup wrapup](http://blog.servergrove.com/2010/11/09/sf-symfony-meetup-wrapup/)
  * [Symfony article in Datormagazin](http://vvv.tobiassjosten.net/symfony/symfony-article-in-datormagazin)
  * [First demonstration of current implementation status of gjPositionsPlugin for easy symfony/doctrine page composition](http://test.ical.ly/2010/11/10/first-demonstration-of-current-implementation-status-of-gjpositionsplugin-for-easy-symfonydoctrine-page-composition/)
  * [Slide of my Presentation for the PHP Forum 2010 in Paris](http://propel.posterous.com/slide-of-my-presentation-for-the-php-forum-20)
  * [If you want to heavily modify the HTML of your symfony forms – step away from the widgets!](http://test.ical.ly/2010/11/11/if-you-want-to-heavily-modify-the-html-of-your-symfony-forms-step-away-from-the-widgets/)
  * [How to add a preview to a symfony admin module or admin theme](http://test.ical.ly/2010/11/12/how-to-add-a-preview-to-a-symfony-admin-module-or-admin-theme/)
  * [symfony 1.4 – automatisierte builds](http://nerdpress.org/2010/11/12/symfony-1-4-automatisierte-builds/)
  * [Forum PHP : vers l’industrialisation du langage](http://www.lemagit.fr/article/france-orange-developpement-php/7486/1/forum-php-vers-industrialisation-langage/)
  * [Our new control panel is live!](http://blog.servergrove.com/2010/11/12/our-new-control-panel-is-live/)
  * [Selecting arbitrary columns using propel](http://nibsirahsieu.wordpress.com/2010/11/12/selecting-arbitrary-columns/)
  * [Facebook Integration on a symfony project - part I](http://symfonytricks.blogspot.com/2010/11/facebook-integration-on-symfony-project.html)
  * [sfPropelCustomSelectPlugin sample usage](http://nibsirahsieu.wordpress.com/2010/11/14/sfpropelcustomselectplugin-sample-usage/)
  * [Doctrine Migrations for beginners](http://www.symfonylab.com/doctrine-migrations-for-beginners/)
  * [SOLUTION: symfony 1.4 doctrine:generate-module error: The ](xxxForm" form only accepts a "xxx" object")
  * [phpBB 4 Meets Symfony 2 (Part 1 of 4)](http://www.learnwebdev.com/?p=345)
  * [Some useful symfony commands](http://techbitsdaily.blogspot.com/2010/11/some-usefull-symfony-commands.html)
  * [Symfony 2.x, Apostrophe 1.x and Concrete](http://window.punkave.com/2010/11/12/symfony-2-0-apostrophe-1-5-and-concrete/)
  * [Forum Php 2010 2ème journée](http://www.creation-site-lyon.com/2010/11/12/forum-php-2010-2eme-journee/)
  * [Schema changes and updating your database](http://symfony-blog.driebit.nl/2010/11/schema-changes-and-updating-your-database/)
  * [php、Symfony　Widgetsについての質問](http://www.phppro.jp/qa/2972)
  * [Symfony admin custom filter propel](http://cgcerro.wordpress.com/2010/11/10/symfony-admin-custom-filter-propel/)
  * [symfony1.1でpluginを入れようとして失敗（symfonyを使ってみる8）](http://cafe-system.com/system152.html)
  * [Créer une liste triable avec Symfony et jquery ui](http://www.avanim-prod.com/blog/symfony/creer-une-liste-triable-avec-symfony-et-jquery-ui-186)
  * [Update to sdInteractiveChartPlugin for Symfony PHP](http://www.sebdangerfield.me.uk/2010/11/update-to-sdinteractivechartplugin-for-symfony-php/)
  * [Symfonyに関するニュース、ブログを集約する「Symfony-news」](http://www.moongift.jp/2010/09/symfony-news/)
  * [スクリーンの大きさとか](http://d.hatena.ne.jp/tohokuaiki/20101108/1289199256)
