A week of symfony #211 (10->16 January 2011)
============================================

Symfony2 introduced this week some minor but profound refactorings: the [routing component adopted URI template notation](http://github.com/symfony/symfony/commit/b63de46374d330464aa3c3f9f3288c2524ad4229), bundles changed their names [to be the class name of the bundle](https://github.com/symfony/symfony/commit/7ac6d59173a201082e0da665ab6c7766a7cda427) not the last part of the namespace and [templates name format changed](https://github.com/symfony/symfony/commit/a365ab2884b76c99a8f5884a2ee289e9dc5bd227) to bundle:section:template.renderer.format (both the renderer and the format are mandatory). Meanwhile, [the Symfony2 donation drive](http://www.symfony-project.org/blog/2011/01/13/symfony2-donation-drive) to fund code security audits was an astonishing success.
 
Development mailing list
------------------------

  * ["[Symfony2] RFC - Global variables in templates"](https://groups.google.com/forum/#!topic/symfony-devs/VVbAf-bzky4)
  * [Admin generator on Symfony2](https://groups.google.com/forum/#!topic/symfony-devs/0x2oTwdUaUY)
  * ["[Symfony2] RFC: Extension config keys"](https://groups.google.com/forum/#!topic/symfony-devs/HrHPjvCLX2o)
  * ["[Symfony2] removing _format template lookup magic"](https://groups.google.com/forum/#!topic/symfony-devs/C1XndD5OiQc)
  * ["[Symfony 2] askeet/jobeet port"](https://groups.google.com/forum/#!topic/symfony-devs/RWt3QdtREK0)
  * ["[Symfony2] Directory structure, third-party code, and more"](https://groups.google.com/forum/#!topic/symfony-devs/cudAyOwgWBE)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [e85546e](http://github.com/symfony/symfony/commit/e85546ef7de757e6f36f29d17665886f47d59aa2 "e85546ef7de757e6f36f29d17665886f47d59aa2 commit on github"): \[DependencyInjection\] made some improvments to the container compiler (added generic repeated pass, better optimization of services, started adding some integration tests)
  * [d1a2a65](http://github.com/symfony/symfony/commit/d1a2a65d192977f139fc93dec72f90d89f01a4d7 "d1a2a65d192977f139fc93dec72f90d89f01a4d7 commit on github"): \[DependencyInjection\] improved performance and added better analysis tools
  * [f1e41a9](http://github.com/symfony/symfony/commit/f1e41a9671304953f6741e0c3056f315063567c6 "f1e41a9671304953f6741e0c3056f315063567c6 commit on github"): \[DependencyInjection\] made some improvements to the container compiler (inline private services which are references multiple times, but where all references originate from the same definition, bug fix for non-shared services which were considered shared within the scope in which they were inlined)
  * [3734c0e](http://github.com/symfony/symfony/commit/3734c0e01e9e454e3dacbc43ec85f3796dbaea94 "3734c0e01e9e454e3dacbc43ec85f3796dbaea94 commit on github"): updated bootstrap file
  * [f41654f](http://github.com/symfony/symfony/commit/f41654fd6064c2f550fa82af3b40878f09df46e7 "f41654fd6064c2f550fa82af3b40878f09df46e7 commit on github"): \[Console\] added rendering previous exceptions
  * [9a2e053](http://github.com/symfony/symfony/commit/9a2e053cbc841d02baa13b15805e0b1af7a1884e "9a2e053cbc841d02baa13b15805e0b1af7a1884e commit on github"): \[Event\] collected data is about listener (not event) calls
  * [47b87e9](http://github.com/symfony/symfony/commit/47b87e902eff70b226748455a2d0fb05d391fd41 "47b87e902eff70b226748455a2d0fb05d391fd41 commit on github"): \[TwigBundle\] made global more powerful (a global can now be a service or a string)
  * [450a6b3](http://github.com/symfony/symfony/commit/450a6b39a20c8c6f7d0bdf96f2ecf2bd2307e1ac "450a6b39a20c8c6f7d0bdf96f2ecf2bd2307e1ac commit on github"): \[TwigBundle\] moved global variables under the app. prefix
  * [b63de46](http://github.com/symfony/symfony/commit/b63de46374d330464aa3c3f9f3288c2524ad4229 "b63de46374d330464aa3c3f9f3288c2524ad4229 commit on github"), [1f88edd](http://github.com/symfony/symfony/commit/1f88edd9e04be8aade52191781a51ac5a44f3238 "1f88edd9e04be8aade52191781a51ac5a44f3238 commit on github"), [6dd1d61](http://github.com/symfony/symfony/commit/6dd1d6172ff1b3876f9d68c2dc70685d6017e0bc "6dd1d6172ff1b3876f9d68c2dc70685d6017e0bc commit on github"): \[Routing\] moved from :var to {var} (this follows the URI template notation: http://code.google.com/p/uri-templates)
  * [40dac23](http://github.com/symfony/symfony/commit/40dac2363ec21af0adcc809ab02bd0ca4cc9ac22 "40dac2363ec21af0adcc809ab02bd0ca4cc9ac22 commit on github"): \[WebProfiler\] normalize header name and use a single reference
  * [b056a6c](http://github.com/symfony/symfony/commit/b056a6c3c1013c10b276de3f33e39241c62572f5 "b056a6c3c1013c10b276de3f33e39241c62572f5 commit on github"), [46f3da5](http://github.com/symfony/symfony/commit/46f3da50d8aabc5fa9328c7837cd01004917664b "46f3da50d8aabc5fa9328c7837cd01004917664b commit on github"): \[TwigBundle\] fixed cache problem for some global variables
  * [9770944](http://github.com/symfony/symfony/commit/9770944a1d6176b91fc08e062a9ba37e7d39cc9e "9770944a1d6176b91fc08e062a9ba37e7d39cc9e commit on github"): \[SQLiteProfilerStorage\] escape special chars in URLs and IPs
  * [5506e9d](http://github.com/symfony/symfony/commit/5506e9d1a302c53ae7bee43cac285371b929d439 "5506e9d1a302c53ae7bee43cac285371b929d439 commit on github"): fixed loading of validation files for bundles in a vendor namespace
  * [b4ac798](http://github.com/symfony/symfony/commit/b4ac7982be347194170b3dbf45097c8b136f6c10 "b4ac7982be347194170b3dbf45097c8b136f6c10 commit on github"), [7b940ce](http://github.com/symfony/symfony/commit/7b940ce82a48da8c7572a5534db9da72d24259be "7b940ce82a48da8c7572a5534db9da72d24259be commit on github"): made it easier to implement alternative app directory structures
  * [c38c0c3](http://github.com/symfony/symfony/commit/c38c0c303e1600e56fc4e8ef84c1f2d014f65447 "c38c0c303e1600e56fc4e8ef84c1f2d014f65447 commit on github"): refactored Templating (made the renderer argument of Storage ctor mandatory, refactored the Engine class to, simplified the check for a template that extends another one but with a different renderer)
  * [3a6f556](http://github.com/symfony/symfony/commit/3a6f5561891688bc7109295ee226e3414e02c581 "3a6f5561891688bc7109295ee226e3414e02c581 commit on github"): \[FrameworkBundle\] registered FileSystem as a service, switched commands to use it
  * [2a3d94a](http://github.com/symfony/symfony/commit/2a3d94a6d0453dc9bcf483a2346be76acc57353e "2a3d94a6d0453dc9bcf483a2346be76acc57353e commit on github"): \[DependencyInjection\] added support for anonymous services in XmlDumper
  * [9ec6955](http://github.com/symfony/symfony/commit/9ec69553f3a3825be1f78d59fd0a7443d5dc392e "9ec69553f3a3825be1f78d59fd0a7443d5dc392e commit on github"): \[Profiler\] use base64 encoding which is more efficient than unpack (space wise)
  * [a69b9e7](http://github.com/symfony/symfony/commit/a69b9e73ec3635b5b5ca7464fbca242136dbc3f5 "a69b9e73ec3635b5b5ca7464fbca242136dbc3f5 commit on github"), [e41df3d](http://github.com/symfony/symfony/commit/e41df3dd41031c75986b2af2e2c00882f77dc30a "e41df3dd41031c75986b2af2e2c00882f77dc30a commit on github"): \[DoctrineBundle\] added missing entry in XSD
  * [b47cf79](http://github.com/symfony/symfony/commit/b47cf7984bc6bcf5ca6cd1c0e5ea0383c348b596 "b47cf7984bc6bcf5ca6cd1c0e5ea0383c348b596 commit on github"): changed priority meaning to be more intuitive
  * [5ee48c4](http://github.com/symfony/symfony/commit/5ee48c496324e5ab46786f486ec3941f9fcbeab1 "5ee48c496324e5ab46786f486ec3941f9fcbeab1 commit on github"), [6011073](http://github.com/symfony/symfony/commit/6011073e7c7745ad0bb520c5bff4c00fdb468997 "6011073e7c7745ad0bb520c5bff4c00fdb468997 commit on github"): \[DependencyInjection\] fixed XML entities in XmlDumper
  * [4460b49](http://github.com/symfony/symfony/commit/4460b498024504f7af33bcf6a74d749ed4bc67e3 "4460b498024504f7af33bcf6a74d749ed4bc67e3 commit on github"): added support for base tag for Link and Form
  * [055b6e4](http://github.com/symfony/symfony/commit/055b6e4d6e6d99f13dddce6b63c408752cd8898b "055b6e4d6e6d99f13dddce6b63c408752cd8898b commit on github"): made a big refactoring of the templating sub-framework (better separation of concerns, made TwigBundle independant of the PHP Engine, removed one layer of abstraction, made it easier to create a new Engine for any templating library, made engines lazy-loaded, reduced memory footprint)
  * [75c6f47](http://github.com/symfony/symfony/commit/75c6f47937ffefc0e9d9b94fa36054eb190f075a "75c6f47937ffefc0e9d9b94fa36054eb190f075a commit on github"): removed the magic discovering of format in template name
  * [a365ab2](http://github.com/symfony/symfony/commit/a365ab2884b76c99a8f5884a2ee289e9dc5bd227 "a365ab2884b76c99a8f5884a2ee289e9dc5bd227 commit on github"): changed the template name format (from bundle:section:template.format.renderer to bundle:section:template.renderer.format)
  * [e84c867](http://github.com/symfony/symfony/commit/e84c867336e26d1371bde1ccffda3c25bb496d80 "e84c867336e26d1371bde1ccffda3c25bb496d80 commit on github"): \[FrameworkBundle\] added some unit tests
  * [7ac6d59](http://github.com/symfony/symfony/commit/7ac6d59173a201082e0da665ab6c7766a7cda427 "7ac6d59173a201082e0da665ab6c7766a7cda427 commit on github"): changed the bundle name to be the class name of the bundle, not the last part of the namespace
  * [ff91ea5](http://github.com/symfony/symfony/commit/ff91ea5f24ae120b76d9bbec83e7b274a601e22e "ff91ea5f24ae120b76d9bbec83e7b274a601e22e commit on github"): \[DoctrineBundle\] added support for MySQL Session Init Listener, refactored driver and driverClass approach to follow the Doctrine DBAL factory more closely for this to work easily
  * [38cbc61](http://github.com/symfony/symfony/commit/38cbc610e97a74fbc6c2bb873950d9cbcf6b4cde "38cbc610e97a74fbc6c2bb873950d9cbcf6b4cde commit on github"): \[FrameworkBundle\] fixed controller names conversion when a bundle is defined in two different namespaces
  * [98b52b6](http://github.com/symfony/symfony/commit/98b52b607cbfe67697b36aa426dfacc126be817e "98b52b607cbfe67697b36aa426dfacc126be817e commit on github"): better support for cookie handling, use native PHP function to set cookies
  * [11085fd](http://github.com/symfony/symfony/commit/11085fd6a6c1080cc812f7032ad6169910a6f7ae "11085fd6a6c1080cc812f7032ad6169910a6f7ae commit on github"): \[Validator\] added a significant amount of PHPDoc to the Validator component
  * [5c64ca8](http://github.com/symfony/symfony/commit/5c64ca8a30b95c3a69db3973111e27becf3a3d8a "5c64ca8a30b95c3a69db3973111e27becf3a3d8a commit on github"): renamed Container::freeze() to Container::compile()
  * [d5c9f37](http://github.com/symfony/symfony/commit/d5c9f3798289dde7443700f632564e1fd321b3ea "d5c9f3798289dde7443700f632564e1fd321b3ea commit on github"): \[DependencyInjection\] added compiler passes as resources
  * [612dce8](http://github.com/symfony/symfony/commit/612dce873be0b2cd36aaeca04a602a7213d0453d "612dce873be0b2cd36aaeca04a602a7213d0453d commit on github"): \[DependencyInjection\] added the possibility to pass the type of compiler pass in ContainerBuilder::addCompilerPAss
  * [be35aa1](http://github.com/symfony/symfony/commit/be35aa1d6a3d0e57ab0279a9beaec0aa5dbe7c2a "be35aa1d6a3d0e57ab0279a9beaec0aa5dbe7c2a commit on github"): \[HttpKernel\] added the possibility to add non-namespaced classes to the compiled class cache
  * [b7d2528](http://github.com/symfony/symfony/commit/b7d2528384953db272f3a5f78042e6d788c6a866 "b7d2528384953db272f3a5f78042e6d788c6a866 commit on github"): added a way for any extension to add classes to the class cache

Documentation
-------------

  * New <a href="http://trac.symfony-project.org/wiki/IRCLogs20110113">IRC Logs 2011-01-13</a> page

New [job postings](http://trac.symfony-project.com/trac/wiki/JobPostings)
----------------

  * Two experienced Symfony developers at [OnlineVille](http://www.onlineville.com/) - full-time based in Montpellier, France - Contact: admin [at] onlineville [dot] com



[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [ksWdCalendar](http://www.symfony-project.org/plugins/ksWdCalendarPlugin): (no description)
  * [pmModelUtils](http://www.symfony-project.org/plugins/pmModelUtilsPlugin): adds extra functionality to our Propel (or Doctrine) models.
  * [sfTCPDFReloaded](http://www.symfony-project.org/plugins/sfTCPDFReloadedPlugin): allows you to easily create a pdf file. You can also import an existing pdf in the background.

Updated plugins
---------------

  * [sfDoctrineShortUrl](http://www.symfony-project.org/plugins/sfDoctrineShortUrlPlugin):
    * added the notion of unallowed domain
    * renamed the is_malware field into is_warning (there is no reliable method to detect malware pages)

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * fixed errors with numeric tags

  * [apostrophePeople](http://www.symfony-project.org/plugins/apostrophePeoplePlugin):
    * updated hide/show ajax in index view
    * removed personSlim template as js updates make it obsolete
    * removed some bad class files

  * [sfRADIUSAuth](http://www.symfony-project.org/plugins/sfRADIUSAuthPlugin):
    * fixed plugin config to automatically set sf_guard_callable option
    * updated readme to reflect changed plugin config needs

  * [sfDataSource](http://www.symfony-project.org/plugins/sfDataSourcePlugin):
    * fixed an error retrieving a table name from a query

  * [sfGrid](http://www.symfony-project.org/plugins/sfGridPlugin):
    * added an option to handle custom URI paramenters in a link widget

  * [sfDoctrineJQueryUISortable](http://www.symfony-project.org/plugins/sfDoctrineJQueryUISortablePlugin):
    * added an option to allow superclass relationships

  * [sfDoctrineRestGenerator](http://www.symfony-project.org/plugins/sfDoctrineRestGeneratorPlugin):
    * do not remove zero filters from the request parameters
    * fixed parameters cleanup when the passed parameter is an empty value
    * made json the default format for generated APIs

  * [sfPropel15](http://www.symfony-project.org/plugins/sfPropel15Plugin):
    * updated externals to use Propel 1.5.6

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * fixed a strange ColumnModel bug where the column config option sortable would get overridden when creating the ColumnModel with Ext.ComponentMgr
    * found a better way to fix the ColumnModel sortable bug
    * fixed a bug with how the gridpanel CheckBoxSelectionModel is instantiated by ColumnModel that was causing an error when checking a column

  * [sfProjectAnalyser](http://www.symfony-project.org/plugins/sfProjectAnalyserPlugin):
    * fixed alert reporting for admin generated modules

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * fixed sorts were busted in blog and event admin
    * event sort by "date" (start date) now has a secondary sort by start time
    * posts always have a secondary sort by descending pub date and events have a secondary sort by descending start date and time
    * event slots based on tags and categories no longer show events that already happened
    * you can now edit content in an area if there are no events or blog posts found either by filtering or because there are none in the engine
    * tweaked the labels for next and previous buttons for blog post and event date filters
    * wrapped the blog header area in logic to not output the area markup if there are no slots
    * set disqus_needed slot for all post and event templates
    * added an app.yml option to let you limit the amount of items on a blog/events page

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * added an Area to the media engine that can be customized for when there are no media items present
    * cleaned up and styled the Permissions UI that was busted previously
    * removed _privileges.php from a module it was no longer in use
    * moved the Apostrophe badge outside of the logged-in buttons
    * updated the a-drag handle box to use modern a_button helper
    * updated history browser
    * limited the slots available in the area that is displayd when there are no media items to display to just a Rich Text slot
    * you will now see only links to pages you are allowed to visit
    * renamed the 'area_add_content_label' option to be 'area-label'
    * shortened the noMediaItemsArea to being a singleton slot that gets default content from pages.yml fixtures in sandbox if you use them
    * apostrophe:publish-all-pages task sets published_at for all published pages (not archived pages)
    * commited first draft of SlideShare support
    * fixed bugs affecting viddler and potentially other media embed services
    * updated error404Success and noMediaItemsArea
    * Viddler now has caching of its requests that require an api call on every page load of the media repo or a page with a video slot
    * apostrophe:migrate now upgrades tables to UTF-8
    * added some additional logic to the addSlot label for when there is only a single slot enabled in an a_area
    * tag editor columns are now sortable
    * put popular tags in order of usage


They talked about us
--------------------

  * [Symfony Code'n'Coffee Minsk (Belarus) Jan 2011 (Внеочередная!)](http://habrahabr.ru/blogs/symfony/111565/)
  * [Conferencia sobre Symfony2 en Alicante](http://www.symfony.es/2011/01/11/conferencia-sobre-symfony2-en-alicante/)
  * [PHP Conferences news roundup](http://blog.servergrove.com/2011/01/11/php-conferences-news-roundup/)
  * [Propel Gets I18n Behavior, And Why It Matters](http://propel.posterous.com/propel-gets-i18n-behavior-and-why-it-matters)
  * [Barcodes and QR codes in PHP](http://www.leftontheweb.com/message/Barcodes_and_QR_codes_in_PHP)
  * [symfony und Google Analytics](http://nerdpress.org/2011/01/12/symfony-und-google-analytics/)
  * [¿Pagarías para que Symfony2 fuera más seguro?](http://www.symfony.es/2011/01/12/%C2%BFpagarias-para-que-symfony2-fuera-mas-seguro/)
  * [symfony command line tool with custom php.ini](http://www.fizyk.net.pl/blog/symfony-command-line-tool-with-custom-php-ini-en)
  * [Propel 1.5.6 Is There, Upgrade To Get The Bugfixes](http://propel.posterous.com/propel-156-is-there-upgrade-to-get-the-bugfix)
  * [Symfony Vivo 2011](http://www.symfony.es/2011/01/14/symfony-vivo-2011/)
  * [Symfony2 Hackday Hub](http://blog.liip.ch/archive/2011/01/14/symfony2-hackday-hub.html)
  * [Integrating Doctrine: Symfony vs Yii](http://www.jnieto.org/article/integrating_doctrine_symfony_vs_yii)
  * [Testing Symfony2](http://pooteeweet.org/blog/0/1869#m1869)
  * [Outsourcing applications with symfony](http://symfony-world.blogspot.com/2011/01/outsourcing-applications-with-symfony.html)
  * [Productivity gain when PHPUnit testing decoupled code](http://test.ical.ly/2011/01/10/productivity-gain-when-phpunit-testing-decouple-code/)
  * [La hoja de ruta de Symfony2](http://www.symfony.es/2011/01/10/la-hoja-de-ruta-de-symfony2/)
  * [Pop­u­lat­ing a Sym­fony drop down from a database](http://www.howitt.com/?p=411)
  * [Symfony Actions – Kein Echo benutzen](http://blog.schreibersebastian.de/2011/01/symfony-actions-kein-echo-benutzen/)
  * [OpenPNEのインストールにはまりまくった　その２](http://benkyoudaisuki.blog63.fc2.com/blog-entry-53.html)
  * [Dependency Injection: Czym jest jest Dependency Injection?](http://rekurencja.pl/php/symfony2/czym-jest-dependency-injection.html)
  * [Remove 'is empty' checkbox from Filter Form in Symfony](http://sakrawebstudio.blogspot.com/2011/01/remove-is-empty-checkbox-from-filter.html)
  * [Presentacion Symfony2 ADWE Alicante](http://www.raulfrailebeneyto.com/2011/01/15/74/)
  * [symfony2 めも entitiesのジェネレートのとこ](http://d.hatena.ne.jp/kajisuke/20110115/1295097656)
  * [第2回Symfony2勉強会 これからの「Symfony2」の話をしよう](http://hiroki.jp/2011/01/15/1460/)
  * [Symfony Midnight #3](http://atnd.org/events/11753)
  * [Which Web 2.0 lang/framework should I choose coming from Java?](http://webdevelopmente.com/which-web-2-0-langframework-should-i-choose-coming-from-java.html)
  * [Using th native MySQL ENUM type in Symfony 1.4 and Doctrine](http://imanpage.com/code/using-th-native-mysql-enum-type-symfony-14-and-doctrine)
  * [1台のPCに複数の XAMPP をインストールした場合の symfony 環境](http://technology.rey-net.com/?eid=1155857)
  * [Doctrine – überlagern einer bestehenden getter Methode in einer Model Klasse](http://www.symfony-blog.de/2011/01/13/doctrine-uberlagern-einer-bestehenden-getter-methode-in-einer-model-klasse/)
  * [Twigでカスタムタグを追加する](http://blog.asial.co.jp/791)
  * [Symfony多表关联](http://www.cyun.org/archives/symfony%E5%A4%9A%E8%A1%A8%E5%85%B3%E8%81%94/)
  * [PHP 5.3 and the Symfony2 UniversalClassLoader – Where to load?](http://test.ical.ly/2011/01/13/php-5-3-and-the-symfony2-universalclassloader-where-to-load/)
  * [国外十大最流行PHP框架排名](http://hi.baidu.com/jis2007/blog/item/afaaa0586fa975cc9d8204fc.html)
  * [Compare symfony 1.4 and Symfony 2](http://blog.elivingsystems.com/2011/01/12/compare-symfony-1-and-symfony-2/)
  * [User management in Symfony](http://www.programmer-pov.com/symfony-user-management-sfdoctrineguardplugin/)
  * [Symfony Doctrine Execute Raw SQL](http://www.tutorialjinni.com/2011/01/symfony-doctrine-execute-raw-sql.html)
  * [Symfony admin generator link with filters](http://www.noop.lv/2011/01/10/symfony-admin-generator-link-with-filters/)