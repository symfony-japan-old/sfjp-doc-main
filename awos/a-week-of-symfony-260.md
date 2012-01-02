A week of symfony #260 (19->25 December 2011)
=============================================

This week, the Symfony2 master branch focused on a big [DoctrineBridge](https://github.com/symfony/symfony/tree/master/src/Symfony/Bridge/Doctrine) refactorization. In addition, the Filesystem class was [moved to its own component](https://github.com/symfony/symfony/commit/818a3321c01c504c5aed05caf9a8b3984071a82d). Lastly, the 2.0 branch was made compatible with the upcoming Twig 1.5 version.
 
Development mailing list
------------------------

  * [Consider better strategies for regenerating cache files](https://groups.google.com/forum/#!topic/symfony-devs/0-k8gNEh-2o)
  * [A component for kernel](https://groups.google.com/forum/#!topic/symfony-devs/nCrZe29L1Xg)
  * [Asset Dependency Bundle](https://groups.google.com/forum/#!topic/symfony-devs/63-dWfagCyE)

symfony 1 development highlights
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=25%2F12%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r33292](http://trac.symfony-project.org/changeset/33292 "33292 revision on trac"): \[1.4\] fixed test for PHP 5.3

Symfony2 development highlights
-------------------------------

[2.0 branch](http://github.com/symfony/symfony/commits/2.0):

  * [29f4111](http://github.com/symfony/symfony/commit/29f4111f3e20e6dc123badfb87ea9faa4efa31b7 "29f4111f3e20e6dc123badfb87ea9faa4efa31b7 commit on github"): \[DoctrineBridge\] added a failing test showing the issue for proxy users
  * [649fa52](http://github.com/symfony/symfony/commit/649fa5219f98cca4d80908fd73560a854f21de4e "649fa5219f98cca4d80908fd73560a854f21de4e commit on github"): \[DoctrineBridge\] fixed the entity provider to support proxies
  * [ebc9979](http://github.com/symfony/symfony/commit/ebc9979a571e223cec27f759b42d97eb720379c5 "ebc9979a571e223cec27f759b42d97eb720379c5 commit on github"): \[Process\] fixed unit tests on PHP 5.4
  * [3dd1072](http://github.com/symfony/symfony/commit/3dd1072edc2d955da926c0a081957e4d4552373a "3dd1072edc2d955da926c0a081957e4d4552373a commit on github"): \[HttpKernel\] fixed unit tests that can fail randomly
  * [5a6c989](http://github.com/symfony/symfony/commit/5a6c989abc88d893b725676f678a417b9b0db776 "5a6c989abc88d893b725676f678a417b9b0db776 commit on github"): \[FrameworkBundle\] added test-attribute in xsd-schema to write functional-tests if using xml-configurations
  * [8235848](http://github.com/symfony/symfony/commit/8235848b5bf588071d766bcc2c00ed81dcb8cc80 "8235848b5bf588071d766bcc2c00ed81dcb8cc80 commit on github"): \[HttpFoundation\] added flv file default extension
  * [1b4aaa2](http://github.com/symfony/symfony/commit/1b4aaa2c8ee2500ec39f0fa3b9a2e3b75a9fc943 "1b4aaa2c8ee2500ec39f0fa3b9a2e3b75a9fc943 commit on github"): \[HttpFoundation\] fixed ApacheRequest (pathinfo was incorrect when using mod_rewrite; added better test coverage)
  * [bebdd07](http://github.com/symfony/symfony/commit/bebdd07f4126d4f45d138a617bdeb2ee029c5c01 "bebdd07f4126d4f45d138a617bdeb2ee029c5c01 commit on github"): \[TwigBridge\] simplified code
  * [6e98730](http://github.com/symfony/symfony/commit/6e987307fc42d6b3ca7d3d94fbf7c0efb56ed841 "6e987307fc42d6b3ca7d3d94fbf7c0efb56ed841 commit on github"): added forwards compatibility with Symfony 2.1 for the Filesystem component
  * [adea589](http://github.com/symfony/symfony/commit/adea589a3df4047055c6bcb002180080f21eb406 "adea589a3df4047055c6bcb002180080f21eb406 commit on github"): \[Twig\] made code compatible with Twig 1.5

[Master branch](http://github.com/symfony/symfony/commits/master):

  * [517eebc](http://github.com/symfony/symfony/commit/517eebcb317b971785db78a8d086e81acbc4530d "517eebcb317b971785db78a8d086e81acbc4530d commit on github"): \[DoctrineBridge\] refactored entity choice list to be ORM independant using an EntityLoader interface
  * [fd174a2](http://github.com/symfony/symfony/commit/fd174a228b2964ae6f362d2f2b22ee2e353b5803 "fd174a228b2964ae6f362d2f2b22ee2e353b5803 commit on github"): \[Tests\] use proper assertion for counting
  * [b919d92](http://github.com/symfony/symfony/commit/b919d92b523eb5fb35e25f40245d8d00e67627ef "b919d92b523eb5fb35e25f40245d8d00e67627ef commit on github"): \[DoctrineBridge\] optimized fetching of entities to use WHERE IN and fix other inefficencies
  * [3b5c617](http://github.com/symfony/symfony/commit/3b5c617ad01e36f74bd949d55d90326c69acc85e "3b5c617ad01e36f74bd949d55d90326c69acc85e commit on github"): \[DoctrineBridge\] removed large parts of the EntityChoiceList code that were completly unnecessary
  * [3c81b62](http://github.com/symfony/symfony/commit/3c81b6295572fe435e2fbc67846d6029be7e5010 "3c81b6295572fe435e2fbc67846d6029be7e5010 commit on github"): \[DoctrineBridge\] cleanup and move loader into its own method
  * [200ed54](http://github.com/symfony/symfony/commit/200ed5490b3ee33dafc465ea2f7ebc53a2f29fad "200ed5490b3ee33dafc465ea2f7ebc53a2f29fad commit on github"): \[DoctrineBridge\] extracted the common type and made the choice list generic
  * [f1199c0](http://github.com/symfony/symfony/commit/f1199c0c684f6e16e2be58b9e87905156edd8dc2 "f1199c0c684f6e16e2be58b9e87905156edd8dc2 commit on github"): \[DoctrineBridge\] decoupled the EntityUserProvider from the ORM (it can now be used by any Doctrine project implementing the interfaces from Doctrine Common 2.2)
  * [84ad40d](http://github.com/symfony/symfony/commit/84ad40dcc80b9a5cd51e53fc2183f966cadca6fe "84ad40dcc80b9a5cd51e53fc2183f966cadca6fe commit on github"): added cache clear hook
  * [24319bb](http://github.com/symfony/symfony/commit/24319bb0f4e66a269c47d5ed9d2c2896b3620fc7 "24319bb0f4e66a269c47d5ed9d2c2896b3620fc7 commit on github"): \[DoctrineBridge\] made it possible to change the manager used by the provider
  * [9653be6](http://github.com/symfony/symfony/commit/9653be618a72885fea2c93d45afab3f57226bcc2 "9653be618a72885fea2c93d45afab3f57226bcc2 commit on github"): moved the EntityFactory to the bridge
  * [818a332](http://github.com/symfony/symfony/commit/818a3321c01c504c5aed05caf9a8b3984071a82d "818a3321c01c504c5aed05caf9a8b3984071a82d commit on github"): \[Component\] moved Filesystem class to its own component
  * [74cfd04](http://github.com/symfony/symfony/commit/74cfd045049267d5bad7fe70131e5d95025aa393 "74cfd045049267d5bad7fe70131e5d95025aa393 commit on github"): \[Security\] made the logout path check configurable
  * [9daa2a6](http://github.com/symfony/symfony/commit/9daa2a6cc8e073a22c7954994183bf00e02cc353 "9daa2a6cc8e073a22c7954994183bf00e02cc353 commit on github"): \[Profiler\] added function to get parent token directly

Updated plugins
---------------

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * added onChange event on autocomplete

  * [WebPurify](http://www.symfony-project.org/plugins/WebPurifyPlugin):
    * replaced simple_xml_call with sfWebBrowser, which uses CURL
    * added 10 second timeout

  * [sfSphinx](http://www.symfony-project.org/plugins/sfSphinxPlugin):
    * updated main lib to version 2.0.2-beta

  * [cpUniForm](http://www.symfony-project.org/plugins/cpUniFormPlugin):
    * added a missing require_once

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * fixed bug with singleton slots and the areaHideWhenEmpty flag
    * more flexible form fields in the blog / events admin sidebar
    * the placeholder of media slots is now sized automatically and clickable
    * created a utility function for checking and calling a callback

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * added more descriptive labels for the delete button in the admin form
    * when app_a_simple_permissions is true (PR), there is no list of allowed editors for a blog post
    * moved that refactored JS to a.js from aBlog.js because it can be shared by both admin generator skeletons


They talked about us
--------------------

  * [Pst...Zsh now friends with symfony](http://www.noop.lv/2011/12/20/pst-zsh-now-friends-with-symfony/)
  * [FOSUserBundle – compatibility break](http://www.noop.lv/2011/12/20/fosuserbundle-compatibility-break/)
  * [Symfony2 & Doctrine Common: creating powerful annotations](http://php-and-symfony.matthiasnoback.nl/2011/12/symfony2-doctrine-common-creating-powerful-annotations/)
  * [Introducing IngewikkeldWrapperBundle](http://www.leftontheweb.com/message/Introducing_IngewikkeldWrapperBundle)
  * [Un llamamiento a la solidaridad de la comunidad Symfony](http://www.symfony.es/2011/12/22/un-llamamiento-a-la-solidaridad-de-la-comunidad-symfony/)
  * [Une semaine symfonique #259 - du 12 au 18 décembre 2011](http://www.strangebuzz.com/post/2011/12/21/Une-semaine-symfonique-259-du-12-au-18-d%C3%A9cembre-2011)
  * [Symfony Google Recaptcha Widget + Validator](http://sstaynov.com/posts/symfony-google-recaptcha-widget-validator/)
  * [業務連絡 Symfony Advent Calendar JP 2011 参加者の皆さんへ](http://d.hatena.ne.jp/koyhoge/20111226/symfonyadvent)
  * [Symfony custom configuration files](http://www.jpgranja.com/2011/12/25/symfony-custom-configuration-files/)
  * [Continuous Testing of lime unit tests in Symfony 1.4 using watchr, Growl, growlnotify and launchd plists](http://bordenia.wordpress.com/2011/12/20/continuous-testing-of-lime-unit-tests-in-symfony-1-4-using-watchr-growl-growlnotify-and-launchd-plists/)
  * [[symfony] Symfony2のRequestクラスの解説](http://fivestar.hatenablog.com/entry/2011/12/21/013929)
  * [How to make a twig extension in symfony2](http://devdream.wordpress.com/2011/12/20/how-to-make-a-twig-extension-in-symfony2/)
  * [Default Validation Messages überschreiben](http://www.symfony-blog.de/symfony-1-4/default-validation-messages-uberschreiben/)
  * [Configuration Reference(配置参考)](http://www.phperblog.net/?p=329)
  * [■２日目■　symfonyの学習-プロジェクト作成→モジュール作成まで-](http://ehipygeb.blogspot.com/2011/12/symfony.html)
  * [The "default" context does not exist и symfony doctrine:data-dump](http://ivansudakov.blogspot.com/2011/12/default-context-does-not-exist-symfony.html)
  
