A week of symfony #193 (6->12 September 2010)
=============================================

Annotations shined this week: Symfony2 routing component <a href="http://github.com/symfony/symfony/commit/130494066d7ef69ce0b5ac48e82b5f150bee0357">added an annotation loader</a>, a new experimental <a href="http://bundles.symfony-reloaded.org/frameworkextrabundle/">FrameworkExtraBundle</a> was released to support annotations for controllers and development mailing-list hosted a discussion about <a href="http://groups.google.com/group/symfony-devs/browse_thread/thread/19c04caa20bc8dc9">defining services with annotations</a>. Unfortunately, this week we also found out that Symfony2 will probably delay its launch date until the next Symfony Live Conference (3-5 March 2011).
 
Development mailing list
------------------------

  * [Support for defining services with annotations](http://groups.google.com/group/symfony-devs/browse_thread/thread/19c04caa20bc8dc9)
  * [Vendor bundles' Entities are not properly mapped](http://groups.google.com/group/symfony-devs/browse_thread/thread/48ce8e16346ac86a)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [2914c44](http://github.com/symfony/symfony/commit/2914c443441bf5ea84e166934b7e23f6d97042d6 "2914c443441bf5ea84e166934b7e23f6d97042d6 commit on github"): \[DoctrineBundle\] replaced "Entities" with "Entity"
  * [e71eec3](http://github.com/symfony/symfony/commit/e71eec3f5d95f849052aa113776808e37113b63a "e71eec3f5d95f849052aa113776808e37113b63a commit on github"): \[DoctrineMongoDBBundle\] removed some mostly unnecessary calls to json_encode from logger
  * [7c1b42e](http://github.com/symfony/symfony/commit/7c1b42e81b7e63423607200ae08911ca58bcdcae "7c1b42e81b7e63423607200ae08911ca58bcdcae commit on github"): \[DependencyInjection\] added a way to inject an anonymous service in an extension configuration
  * [4f33761](http://github.com/symfony/symfony/commit/4f337615e3b465f5f325a4ef50dac1def32fdda9 "4f337615e3b465f5f325a4ef50dac1def32fdda9 commit on github"): \[HttpFoundation\] added request matcher
  * [0b378d1](http://github.com/symfony/symfony/commit/0b378d1b3e93416dcf6b1737a87ab631b286f3dd "0b378d1b3e93416dcf6b1737a87ab631b286f3dd commit on github"): added a way to conditionnaly enable the profiler based on the request
  * [1719bfb](http://github.com/symfony/symfony/commit/1719bfb871e1f923185efda47a319385c2f5a793 "1719bfb871e1f923185efda47a319385c2f5a793 commit on github"): \[DomCrawler\] fixed URIs being incorrectly generated
  * [26e4b2e](http://github.com/symfony/symfony/commit/26e4b2e2ef094472598fcbc3ff80a2245dc3d294 "26e4b2e2ef094472598fcbc3ff80a2245dc3d294 commit on github"): \[Finder\] fixed randomly failing tests due to the order files are read from the filesystem
  * [179fe8e](http://github.com/symfony/symfony/commit/179fe8e6237589d06dceed177f726484ae675d12 "179fe8e6237589d06dceed177f726484ae675d12 commit on github"): fixed Symfony\Component\Routing\Route::setRequirements() _method requirement can be an array
  * [1443d4a](http://github.com/symfony/symfony/commit/1443d4a0baea7add0e190d9d78ba7cadf10dc585 "1443d4a0baea7add0e190d9d78ba7cadf10dc585 commit on github"): \[HttpFoundation\] updated getQueryString() to work in more scenarios
  * [eb7cbb7](http://github.com/symfony/symfony/commit/eb7cbb77ec9ff4ca8143679ed66c0c9b94e08413 "eb7cbb77ec9ff4ca8143679ed66c0c9b94e08413 commit on github"): fixed exception HTML markup
  * [2f8db91](http://github.com/symfony/symfony/commit/2f8db9135a25a32fc77a9f8387f1f4b350f02cff "2f8db9135a25a32fc77a9f8387f1f4b350f02cff commit on github"): fixed webprofiler on Windows
  * [df98a22](http://github.com/symfony/symfony/commit/df98a229f3dbc7acf45531250cc6f524a6456ae6 "df98a229f3dbc7acf45531250cc6f524a6456ae6 commit on github"): \[DoctrineMongoDBBundle\] added support for more Mongo and ODM types
  * [1304940](http://github.com/symfony/symfony/commit/130494066d7ef69ce0b5ac48e82b5f150bee0357 "130494066d7ef69ce0b5ac48e82b5f150bee0357 commit on github"), [b753ea4](http://github.com/symfony/symfony/commit/b753ea45b24bf84c3285de91e684974006e9ef81 "b753ea45b24bf84c3285de91e684974006e9ef81 commit on github"), [c39534e](http://github.com/symfony/symfony/commit/c39534e258c8f08a47f6a6c5cf0b623a20f176e1 "c39534e258c8f08a47f6a6c5cf0b623a20f176e1 commit on github"): \[Routing\] added an annotation loader
  * [4d669d1](http://github.com/symfony/symfony/commit/4d669d106ed8ac5dcd98e34c3d1d8ca7bd08ebf7 "4d669d106ed8ac5dcd98e34c3d1d8ca7bd08ebf7 commit on github"): \[Validator\] changed Xliff loader to get XSD locally
  * [5155321](http://github.com/symfony/symfony/commit/51553211f3da2f9d73030847600e6e2543003d1f "51553211f3da2f9d73030847600e6e2543003d1f commit on github"), [e6b0d54](http://github.com/symfony/symfony/commit/e6b0d5453187b66fd16700a98ec82b7340f21490 "e6b0d5453187b66fd16700a98ec82b7340f21490 commit on github"): \[DoctrineMongoDBBundle\] added symfony proxies for Doctrine ODM schema:create and schema:drop console commands
  * [c53ebe7](http://github.com/symfony/symfony/commit/c53ebe7a8e8f8af1ed7b5bacf6b2bebefbe696b6 "c53ebe7a8e8f8af1ed7b5bacf6b2bebefbe696b6 commit on github"): \[Form\] fixed Form::bind() when no values are submitted
  * [40c0fe8](http://github.com/symfony/symfony/commit/40c0fe854f8b102a7d450c4700af3d391e70f70e "40c0fe854f8b102a7d450c4700af3d391e70f70e commit on github"): \[Form\] added a FileField
  * [fc9325a](http://github.com/symfony/symfony/commit/fc9325a737f0c9764b2315484ef59646f841bf58 "fc9325a737f0c9764b2315484ef59646f841bf58 commit on github"): fixed file upload
  * [a141c98](http://github.com/symfony/symfony/commit/a141c98917ded11f43239e30189ca76f9271455a "a141c98917ded11f43239e30189ca76f9271455a commit on github"): \[HttpFoundation\] moved File Component into the HttpFoundation one
  * [6fc9b68](http://github.com/symfony/symfony/commit/6fc9b68fa7b54c916d0d6d3fa527eeda10569b6f "6fc9b68fa7b54c916d0d6d3fa527eeda10569b6f commit on github"): \[Form\] Replace unset() with non-destructive logic in case the "choices" option is an object
  * [2b776bf](http://github.com/symfony/symfony/commit/2b776bf2e8b3d4c1003b12655f43b4fca1172ccf "2b776bf2e8b3d4c1003b12655f43b4fca1172ccf commit on github"), [e52cf7a](http://github.com/symfony/symfony/commit/e52cf7afe0d266256e3b78db8cb9eb305e075710 "e52cf7afe0d266256e3b78db8cb9eb305e075710 commit on github"), [b3648b2](http://github.com/symfony/symfony/commit/b3648b219b3f354fa0932e492adc8b92b841c1d7 "b3648b219b3f354fa0932e492adc8b92b841c1d7 commit on github"), [9f5469f](http://github.com/symfony/symfony/commit/9f5469f62d2096bc486ecd31202dc2931bfd040f "9f5469f62d2096bc486ecd31202dc2931bfd040f commit on github"): \[Form\] added several unit tests
  * [9be7cbb](http://github.com/symfony/symfony/commit/9be7cbb115a81193e2b15222c3d4630821589d72 "9be7cbb115a81193e2b15222c3d4630821589d72 commit on github"): \[Form\] CollectionField::setData() should remove old fields missing from new data
  * [fb24b29](http://github.com/symfony/symfony/commit/fb24b291c826c55497b2daa1d56a978de5425146 "fb24b291c826c55497b2daa1d56a978de5425146 commit on github"): \[Form\] FieldGroup::addError() can now map errors to fields within nested FieldGroups
  * [b9a7b7e](http://github.com/symfony/symfony/commit/b9a7b7e51a89119b8a9bfc9d1bfd529060f04539 "b9a7b7e51a89119b8a9bfc9d1bfd529060f04539 commit on github"), [c537fb9](http://github.com/symfony/symfony/commit/c537fb9eb231d63c06584077c9b3b3c0cdec7907 "c537fb9eb231d63c06584077c9b3b3c0cdec7907 commit on github"): \[DoctrineBundle, DoctrineMongoDBBundle\] fix mapping dirs
  * <del>[d326c39](http://github.com/symfony/symfony/commit/d326c398e2721c996d9f45108c1ab0cdfceb8ea6 "d326c398e2721c996d9f45108c1ab0cdfceb8ea6 commit on github"): \[Form\] fixed default CSRF token generation as a token must be tied to the user somewhat</del>
  * [226277f](http://github.com/symfony/symfony/commit/226277fd0ed37181e967abf5043a389e355079fc "226277fd0ed37181e967abf5043a389e355079fc commit on github"): added a way to activate CSRF protection from the configuration
  * [74bc9d4](http://github.com/symfony/symfony/commit/74bc9d461bb60e7fedd6ddf8abf2454a7e312c48 "74bc9d461bb60e7fedd6ddf8abf2454a7e312c48 commit on github"): \[FrameworkBundle\] made csrf_secret parameter optional


New [job postings](http://trac.symfony-project.com/trac/wiki/JobPostings)
----------------

  * Senior PHP developer with Symfony experience at [Skylab](http://www.studioskylab.com) - full-time based in Manchester, United Kingdom - Contact: careers [at] studioskylab [dot] com

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [vjMoreTimestampable](http://www.symfony-project.org/plugins/vjMoreTimestampablePlugin): provides an advanced timestampable behavior to use more than created_at and updated_at fields (ex: validated_at, deleted_at, archivated_at).
  * [sfRestWebService](http://www.symfony-project.org/plugins/sfRestWebServicePlugin): offers an easy interface for REST API based on your domain model.
  * [pmSuperfishMenu](http://www.symfony-project.org/plugins/pmSuperfishMenuPlugin): provides the functionality to create dynamic menus using Superfish (based on jQuery).
  * [sfYAC](http://www.symfony-project.org/plugins/sfYACPlugin): Query-caching plugin based on tags system. Requires only simple configuration in schema file.
  * [sfI18NGettextPlural](http://www.symfony-project.org/plugins/sfI18NGettextPluralPlugin): interprets the plural form formula, that's usually located in PO/MO file's meta data section, removing the need to specify the same formula whenever you use format_number_choice.
  * [sfDoctrineMultiDBMigration](http://www.symfony-project.org/plugins/sfDoctrineMultiDBMigrationPlugin): adds new tasks to manage Database migrations when multiple databases are defined in database.yml.

Updated plugins
---------------

  * [sfVideo](http://www.symfony-project.org/plugins/sfVideoPlugin):
    * bugs fixed with autoplay/autobufferng config options

  * [lyMediaManager](http://www.symfony-project.org/plugins/lyMediaManagerPlugin):
    * moved thumbnail creation functions to a dedicated class
    * removed some functions from 'tools' class

  * [tdCore](http://www.symfony-project.org/plugins/tdCorePlugin):
    * added breadcrumb support
    * added model and modules for subpages and configuration
    * improved SEO for subpages
    * added tdLink model and module

  * [sfGuardExtra](http://www.symfony-project.org/plugins/sfGuardExtraPlugin):
    * fixed README

  * [sfTaskLogger](http://www.symfony-project.org/plugins/sfTaskLoggerPlugin):
    * logging comments in doctrine purge

  * [sfProjectAnalyser](http://www.symfony-project.org/plugins/sfProjectAnalyserPlugin):
    * updated roadmap and README

  * [sfDatagrid](http://www.symfony-project.org/plugins/sfDatagridPlugin):
    * fixed RenderActionsBar was using deprecated select_tag()

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * fixed a js syntax bug affecting Chrome and Safari
    * added a container around the typeahead input + add buttons
    * rewrote Taggable::preloadTags to work with any DB vendor

  * [sfPHPUnit2](http://www.symfony-project.org/plugins/sfPHPUnit2Plugin):
    * added possibility to define custom test suites for the test-all task
    * added hints for best practices of the phpunit.xml
    * added return values of the PHPUnit command line executions

  * [sfDoctrineShortUrl](http://www.symfony-project.org/plugins/sfDoctrineShortUrlPlugin):
    * added rel=shortlink fetching
    * better count of visits

  * [sfAssetsLibrary](http://www.symfony-project.org/plugins/sfAssetsLibraryPlugin):
    * added generation of PDF thumbnails
    * fixed slash on relative URLs not working on Windows

  * [sfSimplePage](http://www.symfony-project.org/plugins/sfSimplePagePlugin):
    * mod make action prototype more strict

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * added dcWidgetFormAjaxDependence and dcWidgetFormPropelAjaxDependence
    * updated README and ajax dependence widget

  * [sfDoctrineJCroppable](http://www.symfony-project.org/plugins/sfDoctrineJCroppablePlugin):
    * now uses original image if the same size as the final image
    * correctly loads images without blurring on db reload
    * fix for incorrect ratio thanks to Nicholas Tipping

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * Removed extra markup that caused date widget to not automatically save the post when changes were made
    * reworked blog admin markup to share a-subnav-wrapper and inner divs with the media admin and subnavigation
    * re-worked the markup for blog admin layout

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * edit view forms are now AJAX loaded when the edit button is clicked for vastly better performance in browsers that are adversely affected by too many FCK instances
    * moved the JS out of reorganizeSuccess and into a.js
    * refactored the JavaScript associated with the up and down arrows
    * added iframe to the list of tags allowed for media embed code purposes
    * added _doNotEdit.php partial to layout.php for easy toggling of the editing message for staging sites after we launch production
    * added app.yml flag app_a_do_not_edit true/false for toggling the doNotEdit partial
    * fixed menu toggle for Add Page so that you can actually add a page
    * automatic open of rich text editor when you add a rich text slot is back
    * fixed invalid markup around the settings submit buttons
    * refactored aMenuToggle in aUI.js (moved it to a.js and made it work with all of the menus)
    * refactored some browseHistory JS to be in a.js
    * created globalJavascripts partial to load some general JS at the bottom of layout.php once instead of every time a partial is used
    * fixed a bug with the apostrophe.menuToggle calls in _area.php
    * enhanced apostrophe.menuToggle to fail gracefully if the toggle button is undefined
    * fixed the cancel button for menu toggles so that they work even in the form was added later with ajax
    * fixed the route on the multipleList edit button to fix a 404
    * unifying subnavs sidebars and select areas
    * fixed a longstanding subtle issue probably present in most PHP applications: if you try to upload something that exceeds your php.ini post_max_size setting, the entire POST array is empty, leading to confusing results


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [Yonococino](http://www.yonococino.com): \(Spanish\) online restaurant aggregator

New [symfony bloggers](http://trac.symfony-project.com/trac/wiki/SymfonyBloggers)
--------------------

  * [Raphael Burnes](http://raphaelburnes.com/category/symfony) \([feed](feed://raphaelburnes.com/category/symfony/feed/)\) \(English\)

They talked about us
--------------------

  * [symfony crons and cron task logging](http://symfony-world.blogspot.com/2010/09/symfony-crons-and-cron-task-logging.html)
  * [High Performance Mobile Symfony](http://www.symfonylab.com/high-performance-mobile-symfony/)
  * [[Widget] sfWidgetFormTimeAndClear](http://blog.symfotips.fr/2010/09/06/widget-sfwidgetformtimeandclear/)
  * [WebExpo bude nejvýznamnější konferencí o webu ve střední Evropě](http://www.zive.cz/tiskove-zpravy/webexpo-bude-nejvyznamnejsi-konferenci-o-webu-ve-stredni-evrope/sc-5-a-153655/default.aspx)
  * [sfTaskLoggerPlugin updated for symfony 1.4](http://www.strangebuzz.com/index.php/2010/09/06/42-sftaskloggerplugin-updated-for-symfony-14)
  * [symfony file upload - leave original file name](http://symfony-world.blogspot.com/2010/09/symfony-file-upload-leave-original-file.html)
  * [Did you know there are loads of configuration options to symfony routes that the reference book is not telling you?](http://test.ical.ly/2010/09/07/did-you-know-there-are-loads-of-configuration-options-to-symfony-routes-that-the-reference-book-is-not-telling-you/)
  * [Full highlighting functionality with symfony, Geshi and TinyMCE](http://www.jnieto.org/article/full_highlighting_functionality_with_symfony_geshi_and_tinymce)
  * [Using fabric to deploy symfony application](http://rabaix.net/en/articles/2010/09/07/using-fabric-to-deploy-symfony-application)
  * [Creating mobile symfony sites](http://webmozarts.com/2010/09/07/creating-mobile-symfony-sites/)
  * [MVC in symfony 1.x : the geek, the artist and the businessman](http://www.coolkeums.org/en/article/mvc-in-symfony-1-x-the-geek-the-artist-and-the-businessman.html)
  * [Why you should not handle your symfony form inside a component](http://test.ical.ly/2010/09/09/why-you-should-not-handle-your-symfony-form-inside-a-component/)
  * [PHP: Symfony 2 jusqu’à dix fois plus rapide que la mouture précédente ?](http://www.silicon.fr/php-symfony-2-jusqu%E2%80%99a-dix-fois-plus-rapide-que-la-mouture-precedente-41832.html)
  * [symfony Workshop – How to handle a form from a component in an action](http://test.ical.ly/2010/09/10/symfony-workshop-how-to-handle-a-form-from-a-component-in-an-action/)
  * [ Symfony: прячем фильтры в админ-генераторе](http://habrahabr.ru/blogs/symfony/103950/)
  * [Propel2 Will Be an ActiveRecord Implementation Based On Doctrine2](http://propel.posterous.com/propel2-will-be-an-activerecord-implementatio)
  * [Así funciona Symfony por dentro](http://www.symfony.es/2010/09/10/asi-funciona-symfony-por-dentro/)
  * [¿Es posible combinar las licencias GPL y MIT?](http://softlibre.barrapunto.com/article.pl?sid=10/09/10/0852212)
  * [Symfony with SaaS](http://raphaelburnes.com/2010/09/06/symfony-with-saas/)
  * [Finding the right symfony documentation](http://raphaelburnes.com/2010/09/06/finding-the-right-symfony-documentation/)
  * [Using HTMLPurifier in Symfony 1.4](http://raphaelburnes.com/2010/09/07/using-htmlpurifier-in-symfony-1-4/)
  * [More Videos From Spanish Symfony Conference 2010](http://www.symfonylab.com/more-videos-from-spanish-symfony-conference-2010/)
  * [Symfony: External libraries shared for all modules](http://sebastian.formzoo.com/2010/09/06/symfony-external-libraries-shared-for-all-modules/)
  * [Symfony 2 & Facebook: часть 1, первый проект](http://hudson.su/2010/09/06/symfony-2-facebook-part-1-first-project/)
  * [L'avenir de PHP vu par Frédéric Hardy](http://blog.mageekbox.net/?post/2010/09/05/L-avenir-de-PHP-vu-par-Fr%C3%A9d%C3%A9ric-Hardy)
  * [Installing & configuring Symfony Framework in Ubuntu](http://it.gansukh.com/2010/09/installing-configuring-symfony.html)
  * [Practical symfony 6 дахь өдөр More with the Model (орчуулсан: Ариунсүлд)](http://erheme318.wordpress.com/2010/09/06/practical-symfony-6-%D0%B4%D0%B0%D1%85%D1%8C-%D3%A9%D0%B4%D3%A9%D1%80-more-with-the-model-%D0%BE%D1%80%D1%87%D1%83%D1%83%D0%BB%D1%81%D0%B0%D0%BD-%D0%B0%D1%80%D0%B8%D1%83%D0%BD%D1%81%D2%AF%D1%80/)
  * [SYMFONY 助手 （Helpers）](http://hi.baidu.com/54lwh/blog/item/3b48c81b00c6a4f1ae5133e7.html)
  * [A Symfony Plugin for Generating Charts using Googles Visualization API (sdInteractiveChartPlugin)](http://www.sebdangerfield.me.uk/2010/09/a-symfony-plugin-for-generating-charts-using-googles-visualization-api-sdinteractivechartplugin/)
  * [Beschreibung der symfony Form widgets and validators](http://www.typeed.de/blog/2010/09/12/beschreibung-der-symfony-form-widgets-and-validators)
  * [Symfony2 event dispatcher](http://www.zyxist.com/en/archives/103)
  * [MOONGIFT : Symfonyに関するニュース、ブログを集約する「Symfony-news」 オープンソース・ソフトウェア/フリーウェアを毎日紹介](http://tyudon.com/blog/?p=19059)
  * [Symfonyに関するニュース、ブログを集約する「Symfony-news」](http://www.moongift.jp/2010/09/symfony-news/)
  * [Making Objects Linkable in symfony](http://developers.nationalfield.org/2010/09/making-objects-linkable-in-symfony/)
  * [Passing a propel criteria to the symfony routing function that retrieves the object](http://softwareobjects.net/technology/other/passing-a-propel-criteria-to-the-symfony-routing-function-that-retrieves-the-object/)
  * [symfony 1.4を試してみた](http://d.hatena.ne.jp/d4-1977/20100910/1284131878)
  * [How to Write a symfony Plugin](http://jasonswett.net/how-to-write-a-symfony-plugin/)
  * [Symfony 1.4 + Codeigniter = Symfony 2](http://www.sajithmr.me/symfony-1-4-codeigniter-symfony-2/)
  * [Is it just me or is Symfony2 gaining momentum?](http://test.ical.ly/2010/09/08/is-it-just-me-or-is-symfony-2-gaining-momentum/)
  * [Capturar evento logout y login en Symfony](http://axiacore.com/2010/09/capturar-evento-logout-y-login-en-symfony/)
  * [Good Symfony 1.1 Forms Introduction](http://symfonynerds.com/blog/?p=106)
  * [Cómo embeber formularios en symfony sin sobreescribir métodos](http://patriciomacadden.com.ar/2010/09/07/como-embeber-formularios-en-symfony-sin-sobreescribir-metodos/)
  * [Funciones js en config.yml](http://symfony.cl/blog/2010/09/funciones-js-en-config-yml/)
