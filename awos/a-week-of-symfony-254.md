A week of symfony #254 (7->13 November 2011)
============================================

Symfony community took a huge leap forward this week with the introduction of a new gamification strategy to [develop the community](http://symfony.com/blog/developing-the-symfony-community). Starting this week, Symfony Community members will be rewarded for their commitment and involvement in the community. In addition, the first edition of the [Symfony Community Awards](http://awards.symfony.com/) was announced to further recognize the work of the most prominent community members.
 
Development mailing list
------------------------

  * [HttpCache issue](https://groups.google.com/forum/#!topic/symfony-devs/2qKekaBJfV4)
  * [Interface with supports method](https://groups.google.com/forum/#!topic/symfony-devs/cxWDUG5jo9Y)
  * [\[Symfony2\] brain storming master/slave setups](https://groups.google.com/forum/#!topic/symfony-devs/W865kY4rSUc)


Symfony2 development highlights
-------------------------------

[2.0 branch](http://github.com/symfony/symfony/commits/2.0):

  * [380c67e](http://github.com/symfony/symfony/commit/380c67efc8bb5cc26d15269c145a2379d77729af "380c67efc8bb5cc26d15269c145a2379d77729af commit on github"): \[FrameworkBundle\] fixed HttpKernel when the app is stateless
  * [c31c512](http://github.com/symfony/symfony/commit/c31c512466c92faa59ec6f5db83df88fce870340 "c31c512466c92faa59ec6f5db83df88fce870340 commit on github"): \[FrameworkBundle\] fixed output buffering when an error occurs in a sub-request
  * [9e6ba9a](http://github.com/symfony/symfony/commit/9e6ba9ae893f5c16a42b36c10ac9dfb5b63f41df "9e6ba9ae893f5c16a42b36c10ac9dfb5b63f41df commit on github"), [d789f94](http://github.com/symfony/symfony/commit/d789f9424e0c93f7d98ae74817ccacb23555b754 "d789f9424e0c93f7d98ae74817ccacb23555b754 commit on github"), [7346896](http://github.com/symfony/symfony/commit/7346896129b7e1c466c160abf484ea8624fa8bec "7346896129b7e1c466c160abf484ea8624fa8bec commit on github"): \[Serializer\] added a supportsNormalization method
  * [414d4be](http://github.com/symfony/symfony/commit/414d4be7e81fecefa30f7f1c338f412565475c45 "414d4be7e81fecefa30f7f1c338f412565475c45 commit on github"): \[Doctrine\] refactored unit tests
  * [9d2ab9c](http://github.com/symfony/symfony/commit/9d2ab9ca9c1762c529e053cefd39a5e626102133 "9d2ab9ca9c1762c529e053cefd39a5e626102133 commit on github"): \[Doctrine\] fixed security user reloading when the user has been changed via a form with validation errors
  * [a245e15](http://github.com/symfony/symfony/commit/a245e154344c5860ba9847839afbd37326a44c35 "a245e154344c5860ba9847839afbd37326a44c35 commit on github"): \[DomCrawler\] trim URI in getURI
  * [45b218e](http://github.com/symfony/symfony/commit/45b218e7c4cb6f1d8280c6cd09b262395f8f24a4 "45b218e7c4cb6f1d8280c6cd09b262395f8f24a4 commit on github"): \[Translation\] added detection for circular references when adding a fallback catalogue
  * [6b0e7c8](http://github.com/symfony/symfony/commit/6b0e7c8c410bdc646e29b7af24d6664e5dd1d3ac "6b0e7c8c410bdc646e29b7af24d6664e5dd1d3ac commit on github"): \[Translation\] removed unneeded methods
  * [8351a11](http://github.com/symfony/symfony/commit/8351a112861cd1cc71fbe35d69455c504d2f6acf "8351a112861cd1cc71fbe35d69455c504d2f6acf commit on github"): added check for array fields to be integers in reverseTransform method
  * [e83e00a](http://github.com/symfony/symfony/commit/e83e00a7b881e6d1eccdd8c3213ca78c7add2d37 "e83e00a7b881e6d1eccdd8c3213ca78c7add2d37 commit on github"): fixed rendering of FileType (value is not a valid attribute for input[type=file])
  * [ed1a6c2](http://github.com/symfony/symfony/commit/ed1a6c2e453025ceff40193a1ac53aeb1f72647a "ed1a6c2e453025ceff40193a1ac53aeb1f72647a commit on github"), [29e12af](http://github.com/symfony/symfony/commit/29e12affb064882d5599f16a8e13f8975148520c "29e12affb064882d5599f16a8e13f8975148520c commit on github"): \[TwigBundle\] do not clean output buffering below initial level (this resulted in issues with PHPUnit 3.6, which will buffer all output and clean them in the end)
  * [7cba0a0](http://github.com/symfony/symfony/commit/7cba0a07b6e34ca4721e7be12d610a5dc3f3a5d4 "7cba0a07b6e34ca4721e7be12d610a5dc3f3a5d4 commit on github"): \[Bridge/Monolog\] also identify FirePHP by the X-FirePHP-Version header
  * [bb5fb79](http://github.com/symfony/symfony/commit/bb5fb79c3d86d86f286ac44a3ef77ccc7c1b9307 "bb5fb79c3d86d86f286ac44a3ef77ccc7c1b9307 commit on github"): changed the way we store the current ob level
  * [4858fbe](http://github.com/symfony/symfony/commit/4858fbe7e0f991dd3e8f0a3846eb0634b76fdd07 "4858fbe7e0f991dd3e8f0a3846eb0634b76fdd07 commit on github"): \[TwigBundle\] fixed trace to not show 'in at line' when file/line are empty

[Master branch](http://github.com/symfony/symfony/commits/master):

  * [6f05544](http://github.com/symfony/symfony/commit/6f05544424480f1ccd008cf773dc573d47586019 "6f05544424480f1ccd008cf773dc573d47586019 commit on github"): \[Console\] added an exception when overriding an existing argument (added some unit tests for option and arguments overriding)
  * [47b888a](http://github.com/symfony/symfony/commit/47b888a9579f65d10f568b90fa4820fb8c1c0208 "47b888a9579f65d10f568b90fa4820fb8c1c0208 commit on github"): added the real template name when an error occurs in a Twig template
  * [47fca8e](http://github.com/symfony/symfony/commit/47fca8e0a0ab74f88d2c37838d62344e28bb37a2 "47fca8e0a0ab74f88d2c37838d62344e28bb37a2 commit on github"): \[HttpKernel\] fixed file storage for the profiler
  * [a7296e7](http://github.com/symfony/symfony/commit/a7296e7c84df28201276648757b04b2da2526018 "a7296e7c84df28201276648757b04b2da2526018 commit on github"): \[Security\] made exceptions thrown by the user checker and the checkAuthentication() method use the hideUserNotFoundExceptions flag
  * [e1822e7](http://github.com/symfony/symfony/commit/e1822e78076040a64755b31f22e0d46f801d9bb0 "e1822e78076040a64755b31f22e0d46f801d9bb0 commit on github"): enable dynamic set of validation groups by a callback or Closure
  * [d08ec5e](http://github.com/symfony/symfony/commit/d08ec5e55f7e90a44589a50fdbc5c86f7278ff7f "d08ec5e55f7e90a44589a50fdbc5c86f7278ff7f commit on github"): added DelegatingValidator tests
  * [796c6b2](http://github.com/symfony/symfony/commit/796c6b2f8de8b3fc653542d2eb8f3b22501f2a1e "796c6b2f8de8b3fc653542d2eb8f3b22501f2a1e commit on github"): \[Locale\] added getIcuVersion and getIcuDataVersion to Locale
  * [9c2a26d](http://github.com/symfony/symfony/commit/9c2a26db12d6f5a488c4e22e2cb134e4039d30d5 "9c2a26db12d6f5a488c4e22e2cb134e4039d30d5 commit on github"): \[Translation\] added Mo loader tests
  * [56cb7a5](http://github.com/symfony/symfony/commit/56cb7a515bfb028e00767c3c73ed15d66a44fb6b "56cb7a515bfb028e00767c3c73ed15d66a44fb6b commit on github"): \[Translation\] added gettext PO and MO Dumper
  * [4d80ebd](http://github.com/symfony/symfony/commit/4d80ebd5c85743812a4859d26b2e5d204dfa59d7 "4d80ebd5c85743812a4859d26b2e5d204dfa59d7 commit on github"): \[Security\] remove security token if user was deleted, is disabled or locked to prevent infinite redirect loops to the login path

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfNav](http://www.symfony-project.org/plugins/sfNavPlugin): (no description)
  * [sfNavBuilder](http://www.symfony-project.org/plugins/sfNavBuilderPlugin): aids the creation of hierarchical menus.
  * [acExceptionNotifier](http://www.symfony-project.org/plugins/acExceptionNotifierPlugin): allows you to send by e-mail errors 500 (Exception type) that occur in production environments.

Updated plugins
---------------

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * added support for root node
    * added support for a type in tree

  * [sfDoctrineActAsSluggableAttachment](http://www.symfony-project.org/plugins/sfDoctrineActAsSluggableAttachmentPlugin):
    * fixed addional '/' added to url when not using image as attachment

  * [sfTools](http://www.symfony-project.org/plugins/sfToolsPlugin):
    * added a session storage class for the Flash session bug
    * added the sfAdvFilesystem.class.php

  * [sfJqueryReloaded](http://www.symfony-project.org/plugins/sfJqueryReloadedPlugin):
    * setting sf_jquery_core to false now prevents jquery itself from being loaded by the plugin so that it can be loaded by other means in your project without conflicts

  * [sfSyncContent](http://www.symfony-project.org/plugins/sfSyncContentPlugin):
    * new --resolve-links option copies the folders and files that symbolic links point to rather than the symbolic links themselves

  * [sfTrafficCMS](http://www.symfony-project.org/plugins/sfTrafficCMSPlugin):
    * added template for easy copy and paste

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * added new lines and tabs to the assets output by apostrophe so that they're more human-readable
    * cleaned up noisy logging and Added a bit of logging for the cache
    * added paypal and wufoo slot icons
    * fixed bug with nested navigation. child navigation were coming up with duplicate ID names
    * fixed aMysql::findOneBy method
    * added lots of useful classes to the navigation component
    * added CSS3 PIE to the a-helpers file to allow the use of unsupported CSS3 features in Internet Explorer

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * don't assume blog permissions don't exist when migrating to 1.5

  * [apostropheExtraSlots](http://www.symfony-project.org/plugins/apostropheExtraSlotsPlugin):
    * added contact slot to the extraslots plugin
    * uniformized the class names and added reasonable default styles
    * added aAnchorTitleSlot slot that allows you to create title slots that can serve as headings for sections or as invisible inline anchors if the 'title' options is set to false

They talked about us
--------------------

  * [symfony basics: form default values](http://symfony-world.blogspot.com/2011/11/symfony-basics-form-default-values.html)
  * [Symfony2 – pierwsze wrażenia](http://www.kamiladryjanek.com/2011/11/symfony2-pierwsze-wrazenia/)
  * [Symfony2: running PHPUnit from within a controller](http://php-and-symfony.matthiasnoback.nl/2011/11/symfony2-running-phpunit-from-within-a-controller/)
  * [Un piccolo problema con Symfony2 e PHPUnit 3.6](http://www.symfony.it/articoli/538/un-piccolo-problema-con-symfony2-e-phpunit-3-6/)
  * [extending doctrine admin module: filtered sum](http://symfony-world.blogspot.com/2011/11/extending-doctrine-admin-filtered-sum.html)
  * [Sensio Connect for the Symfony community](http://vvv.tobiassjosten.net/symfony/sensio-connect-for-the-symfony-community)
  * [Symfony2. Подводные камни кэширования](http://habrahabr.ru/blogs/symfony/132211/)
  * [AppKernel and DependencyInjection container in Symfony 2 tests](http://www.noop.lv/2011/11/09/appkernel-and-dependencyinjection-container-in-symfony-2-tests/)
  * [PHPUnit: create a ResultPrinter for output in the browser](http://php-and-symfony.matthiasnoback.nl/2011/11/phpunit-create-a-resultprinter-for-output-in-the-browser/)
  * [State of the Symfony2 CMF](http://pooteeweet.org/blog/0/2042#m2042)
  * [Un bundle de mise en maintenance pour vos sites avec Symfony2](http://www.lexik.fr/blog/symfony/symfony2/un-bundle-de-mise-en-maintenance-pour-vos-sites-avec-symfony2-1807)
  * [Drupal 8 to be Based on Symfony2 Components](http://www.cmswire.com/cms/web-cms/drupal-8-to-be-based-on-symfony2-components-013441.php)
  * [Drupal8 et Symfony2 en... concert](http://www.toolinux.com/Drupal8-et-Symfony2-en-concert)
  * [PHP : Drupal 8 et Symfony 2 main dans la main](http://www.silicon.fr/php-drupal-8-et-symfony-2-main-dans-la-main-64956.html)
  * [Profesionalizando la comunidad de Symfony](http://www.symfony.es/2011/11/11/profesionalizando-la-comunidad-de-symfony/)
  * [Anunciada la primera edición de los Premios de la Comunidad Symfony](http://www.symfony.es/2011/11/11/anunciada-la-primera-edicion-de-los-premios-de-la-comunidad-symfony/)
  * [Symfony2: get controller / action name in Twig template](http://www.kamiladryjanek.com/2011/11/symfony2-get-controller-action-name-in-twig-template/)
  * [Symfony 2: La fonction render de Twig pour appeller une action depuis une vue](http://www.dinduks.com/symfony-2-la-fonction-render-de-twig-pour-appeller-une-action-depuis-une-vue)
  * [Sensio Connect for Symfony Community](http://www.mellzamora.com/2011/11/sensio-connect-for-symfony-community/)
  * [Symfony2 global variables in TWIG](http://www.articles4.us/2011/11/symfony2-global-variables-in-twig/)
  * [phpconf 2011 – Symfony簡介](http://ricky.ez2.us/2011/11/12/phpconf-2011-symfony%E7%B0%A1%E4%BB%8B/)
  * [Symfony: la paginación](http://xn--80ajjboungj8a.com.ua/symfony-pagination.html)
  * [Usar nl2br en el motor Twig de Symfony](http://carlosaisa.com.es/2011/11/11/usar-nl2br-en-el-motor-twig-de-symfony/)
  * [Installing and Configuring Symfony](http://monsterbirth.ru/symfony-2-book-na-russkom/installing-and-configuring-symfony-rus/)
  * [Drupal 8 to be Based on Symfony2 Components](http://bestsouvenir.org/http:/bestsouvenir.org/2011/11/10/drupal-8-to-be-based-on-symfony2-components/souvenir-gift-present-iphone-ipad-phone-surprise-ebay-amazon)
  * [Symfony Blog: Die Entwicklung des Symfony Gemeinschaft](http://www.php-boutique.de/symfony-blog-die-entwicklung-des-symfony-gemeinschaft)
  * [Statische Datei aus dem Web-Verzeichniss verlinken](http://www.symfony-blog.de/symfony-1-4/statische-datei-aus-dem-web-verzeichniss-verlinken/)
  * [Symfony 2 : This script is only accessible from localhost / You are not allowed to access this file](http://www.remy-mellet.com/blog/255-symfony-2-this-script-is-only-accessible-from-localhost-you-are-not-allowed-to-access-this-file/)
  * [Disable csrf protection in Symfony](http://somnathpawar.wordpress.com/2011/11/09/disable-csrf-protection-in-symfony/)
  * [Setup and Install Symfony 2.0 project](http://www.bitspace.in/2011/11/setup-and-install-symfony-20-project.html)
  * [[Symfony] Apache標準の404 Not Found が表示されるので mod_rewrite を有効にする](http://codenote.net/apache/356.html)
  * [Drupal 8: it will be with Symphony 2!](http://mb-c.pro/en/cms/drupal)
  * [Belajar Membuat Library Form Symfony](http://blog.politekniktelkom.ac.id/tfn/2011/11/08/belajar-membuat-library-form-symfony/)
  * [Installing and Configuring Behat with Mink and Sahi Headlessly](http://www.thenetcircle.com/2011/11/08/installing-and-configuring-behat-with-mink-and-sahi-headlessly/)
  * [Doctrine Migrations for beginners](http://www.symfonylab.com/doctrine-migrations-for-beginners/)
  * [How to Write a symfony Plugin](http://sunzhen.blogspot.com/2011/11/how-to-write-symfony-plugin.html)
  * [Symfony Day Cologne 2011](http://www.ausgebloggt.de/2011/11/07/symfony-day-cologne-2011/)
  * [symfonyでのheader("Location: $url")メモ](http://tomomis0091.blogspot.com/2011/11/symfonyheaderlocation-url.html)
  * [So what is Symfony then?](http://www.testically.org/2011/11/10/so-what-is-symfony-then/)
  * [Spicing up with Symfony – Refactoring Legacy Code](http://www.testically.org/2011/11/11/spicing-up-with-symfony-refactoring-legacy-code/)
