---
layout: default
title: A week of symfony#201 (1->7 November 2010)
---

A week of symfony #201 (1->7 November 2010)
===========================================

Symfony2 development focused this week on unit tests. Hundreds of new tests were committed, mostly on the Security component. In addition, the symfony developers mailing list activity surged with some insightful discussions.

Development mailing list
------------------------

  * [Usage of Controller ArrayAccess and $this['servicename'] is confusing](http://groups.google.com/group/symfony-devs/browse_thread/thread/1badb342882f2f7a)
  * [Symfony2 form-login redirect loop](http://groups.google.com/group/symfony-devs/browse_thread/thread/3d7a80a5308256e8)
  * [Symfony2 form validation](http://groups.google.com/group/symfony-devs/browse_thread/thread/97021a9b5739b39c)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [a4fbf74](http://github.com/symfony/symfony/commit/a4fbf74593cb81a5dc3f2fcde64c491e37a4de38 "a4fbf74593cb81a5dc3f2fcde64c491e37a4de38 commit on github"): added a user provider for Doctrine MongoDB
  * [a5d4acc](http://github.com/symfony/symfony/commit/a5d4acc54ddd8536404fd3348752865156702800 "a5d4acc54ddd8536404fd3348752865156702800 commit on github"): \[HttpFoundation\] updated get() signature to get($key, $default = null, $first = true)
  * [ae888b8](http://github.com/symfony/symfony/commit/ae888b80f65e4f28803dc28e9f869bcfd3289782 "ae888b80f65e4f28803dc28e9f869bcfd3289782 commit on github"): \[HttpFoundation\] removed port number from HOST header to be consistent with backup values (SERVER_NAME, SERVER_ADDR)
  * [dd9b77e](http://github.com/symfony/symfony/commit/dd9b77ed96e768bd0c54755b0ea88272febea285 "dd9b77ed96e768bd0c54755b0ea88272febea285 commit on github"): \[HttpFoundation\] added Response::setVary()
  * [3d5054f](http://github.com/symfony/symfony/commit/3d5054f21fc92a9cff70b5e87f467295252c52a6 "3d5054f21fc92a9cff70b5e87f467295252c52a6 commit on github"): \[Security\] added unit tests for the Authentication sub-namespace
  * [ec41757](http://github.com/symfony/symfony/commit/ec417578caa531a3854ef3c76914471ed22504e9 "ec417578caa531a3854ef3c76914471ed22504e9 commit on github"), [a19cdce](http://github.com/symfony/symfony/commit/a19cdce1bcd93cb30a34a3011f745439b9215d40 "a19cdce1bcd93cb30a34a3011f745439b9215d40 commit on github"): \[Security\] added unit tests to some authenticated providers (code coverage is more than 96% for the Security component now)
  * [58bd4ac](http://github.com/symfony/symfony/commit/58bd4acdd167a6f47343abf5f9eeec99877ab0c5 "58bd4acdd167a6f47343abf5f9eeec99877ab0c5 commit on github"): \[Translation\] added some unit tests
  * [556bfcb](http://github.com/symfony/symfony/commit/556bfcb804b11f2027522d108007e4f7dff86076 "556bfcb804b11f2027522d108007e4f7dff86076 commit on github"): \[HttpKernel\] added some more unit tests
  * [5bd03e1](http://github.com/symfony/symfony/commit/5bd03e1c588cc39ddd3cc211a468f72a1bcf8d20 "5bd03e1c588cc39ddd3cc211a468f72a1bcf8d20 commit on github"): \[HttpKernel\] added unit tests for ESI
  * [e7ea2eb](http://github.com/symfony/symfony/commit/e7ea2eb433ff05ae4302b6e3b1c3e7b3fcefacae "e7ea2eb433ff05ae4302b6e3b1c3e7b3fcefacae commit on github"): \[FrameworkBundle\] ensuring the exception page renders even when the Request format is unknown to Symfony



New [developers for hire](http://trac.symfony-project.com/trac/wiki/DevelopersForHire)
-----------------------

  * [knpLabs](http://www.knplabs.com): a french web agency who loves quality work, innovation and excitement! We've specialized in developing websites and web apps with the symfony and Symfony2 frameworks.


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfWebgrind](http://www.symfony-project.org/plugins/sfWebgrindPlugin): (no description)
  * [sfI18N](http://www.symfony-project.org/plugins/sfI18NPlugin): (no description)
  * [smagEntityWorkflow](http://www.symfony-project.org/plugins/smagEntityWorkflowPlugin): handles a Workflow for Entities. If you need to bring an Object through several steps before it reaches a Final state, an Article for example, this is what you need.
  * [sfDoctrineAdServer](http://www.symfony-project.org/plugins/sfDoctrineAdServerPlugin): ad serving platform.
  * [sfFilesystemFixtures](http://www.symfony-project.org/plugins/sfFilesystemFixturesPlugin): (no description)
  * [sfPhpunitHelper](http://www.symfony-project.org/plugins/sfPhpunitHelperPlugin): adds some useful helpers for functional selenium tests.
  * [sfWpAdmin](http://www.symfony-project.org/plugins/sfWpAdminPlugin): a wordpress style menu for application backends with login screen, ability to set credentials and menu items controlled by YAML config file.

Updated plugins
---------------

  * [sfCouch](http://www.symfony-project.org/plugins/sfCouchPlugin):
    * updated documentation

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * added a document export option

  * [sfThrift](http://www.symfony-project.org/plugins/sfThriftPlugin):
    * added new config params

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * no labels for empty divs
    * added some more customizability
    * fixed warning if there are no suggested tags

  * [idlErrorManagement](http://www.symfony-project.org/plugins/idlErrorManagementPlugin):
    * fixed the get_username technics
    * added specific logs
    * switched to standard SVN structure

  * [idlDoctrineMigration](http://www.symfony-project.org/plugins/idlDoctrineMigrationPlugin):
    * switched to standard SVN structure

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * added the pmWidgetFormJQuerySearch and pmWidgetFormPropelJQuerySearch
    * added mtWidgetFormInputDate and mtValidatorDateString

  * [sfThumbnail](http://www.symfony-project.org/plugins/sfThumbnailPlugin):
    * added the loadData functionality to the sfImagickAdapter class
    * included new tests for functionality as well as making sure nothing old was broken

  * [sfCKEditor](http://www.symfony-project.org/plugins/sfCKEditorPlugin):
    * updated README

  * [sfEnvironmentFixtures](http://www.symfony-project.org/plugins/sfEnvironmentFixturesPlugin):
    * now working without app present
    * tweaked task messages
    * updated documentation

  * [swBaseApplication](http://www.symfony-project.org/plugins/swBaseApplicationPlugin):
    * added an security filter base on the module/action name and the related security filter

  * [sfDoctrineGuard](http://www.symfony-project.org/plugins/sfDoctrineGuardPlugin):
    * use sfWidgetFormInputText instaed of old sfWidgetFormInput

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * improvements to import-site task
    * fixed button slot rich text description
    * limited getPopulars to 10 tags
    * fixed issue with importing images
    * partial for easy project level overrides when you want to add a few extra buttons to the admin bar
    * aWidgetFormJQueryTime works with both string and array input
    * no more $height undefined warnings from aImageSlot/_placeholder
    * apostrophe.formUpdates now attaches an "updating" tab to the element being updated, then changes it to "updated," then removes it
    * brought back the ability to actually add a video slot
    * videos that we don't directly support previews of say "Video" rather than nothing
    * refactored my update tab functionality so you can use it anytime
    * added a visual feedback when saving slots
    * updated jquery to 1.4.3
    * adjusted a text layout bug when selecting images with constraints and there are no media items in the library
    * removed obsolete navigation partials
    * eliminated nearly all script blocks from the 'a' module
    * refactored page queries in aPageTable

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * fixed two issues of blog calendar related to output escaping
    * limited popular tags on Event and Blog forms to 10
    * blog and events admin completely overhauled
    * ordering works now and you can see the blog posts slot doing what it's supposed to do
    * you can now see existing selections when you reopen a blog posts slot with specific blog posts in it
    * catch routing exceptions and display a helpful "you must have a blog page / events page" message rather than crashing the home page
    * fixed migrating brand new sites that don't have an a_blog_category table


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [ACR World](http://www.acrworld.com.au/): \(English\) Australian engineering and construction recruitment
  * [AIME Mentoring](http://aimementoring.com/): \(English\) Help Indigenous Australians get the mentoring they need and bridging the gap between education and employment
  * [StableSmart](http://www.stablesmart.com.au/): \(English\) (no description)
  * [OneVoice Competition](http://onevoice.generationone.org.au/): \(English\) Competition for Australian school students to voice their support and message for ending indigenous disparity in Australia

New [symfony bloggers](http://trac.symfony-project.com/trac/wiki/SymfonyBloggers)
--------------------

  * [\\0xC0DEDBAD - Pierre Minnieur](http://pierre-minnieur.de) \([feed](http://pierre-minnieur.de/rss)\) \(English\)

They talked about us
--------------------

  * [Se presenta la nueva versión de MondonGO](http://www.symfony.es/2010/11/02/se-presenta-la-nueva-version-de-mondongo/)
  * [Symfony2: Boilerplate](http://pierre-minnieur.de/post/1413374301/symfony2-boilerplate)
  * [Organisation et visibilité dans vos projets symfony](http://www.lafermeduweb.net/billet/organisation-et-visibilite-dans-vos-projets-symfony-964.html)
  * [symfony: sfWebProfilerPlugin](http://pierre-minnieur.de/post/1430628598/symfony-sfwebprofilerplugin)
  * [Programmez! Numéro spécial PHP](http://www.hugohamon.com/en/blog/programmez-numero-special-php)
  * [Symfony2: (Http)ServerBundle](http://pierre-minnieur.de/post/1446608465/symfony2-http-serverbundle)
  * [Forum PHP AFUP 2010 paré au décollage!](http://www.hugohamon.com/en/blog/forum-php-afup-2010-pare-au-decollage)
  * [Ajouter une étoile aux champs obligatoires de manière automatique](http://evoilliot.u7n.org/2010/11/ajouter-une-etoile-aux-champs-obligatoires-de-maniere-automatique/)
  * [lyMediaManagerPlugin 0.6.0 released](http://www.lyra-cms.com/blog/2010/11/lymediamanagerplugin-0-6-0-released.html)
  * [Nicolas Silberman (AFUP): Microsoft France s'est beaucoup rapproché de la communauté PHP](http://www.journaldunet.com/developpeur/php/nicolas-silberman-interview-nicolas-silberman-afup.shtml)
  * [Boostrapping a Symfony2 project](http://blog.bearwoods.dk/symfony2-project-initilization)
  * [Doctrine SoftDelete behavior usage](http://symfony-world.blogspot.com/2010/10/doctrine-softdelete-behavior-usage.html)
  * [Advanced symfony Techniques](http://www.symfonylab.com/advanced-symfony-techniques/)
  * [Un anno senza ORM?](http://www.symfony.it/articoli/370/un-anno-senza-orm/)
  * [Symfony2を理解する為にシンプルなアプリケーションを書く](http://d.hatena.ne.jp/chobi_e/20101105/1288980901)
  * [Diem, Symfony - Set value for Form field in processForm](http://codjng.blogspot.com/2010/11/diem-symfony-set-value-for-form-field.html)
  * [Frameworks PHP: Symfony vs CodeIgniter a traves de dos casos de éxito](http://www.lostiemposcambian.com/blog/web-2-0/frameworks-php-symfony-vs-codeigniter-casos-de-exito/)
  * [Les formulaires Symfony](http://www.avanim-prod.com/blog/symfony/les-formulaires-symfony-168)
  * [30 Consejos para trabajar con symfony](http://blog.solucionex.com/symfony/30-consejos-para-trabajar-con-symfony)
