---
layout: default
title: A week of symfony#204 (22->28 November 2010)
---

A week of symfony #204 (22->28 November 2010)
=============================================

Symfony2 development activity exploded this week with thousands of changes, tweaks and additions across most of its components: twig bundle, forms and dependency injection improved their performance; the Output Escaper component was removed; and <a href="https://github.com/symfony/symfony/commit/944d91c1dfc68cf7f769ba7b60cb328fa06b786c">lots of methods were renamed</a> to follow the new naming convention. Symfony2 is gaining momentum week by week and therefore, the release of PR4 version is around the corner and the first beta version could be published before the end of the year.

Development mailing list
------------------------

  * [View layer for Symfony2](http://groups.google.com/group/symfony-devs/browse_thread/thread/1de6b80b134837d4)
  * [Symfony2 Preview Release 4](http://groups.google.com/group/symfony-devs/browse_thread/thread/868ed984b24c62ab)
  * [[RFC] Symfony2 method naming conventions](http://groups.google.com/group/symfony-devs/browse_thread/thread/2016947ac81466cd/ecf94783488c05ef)
  * [Multiple asset hosts](http://groups.google.com/group/symfony-devs/browse_thread/thread/e46e5c8dcd0cf210)
  * [Doctrine2 and Symfony Disconnected Class Metadata Factory](http://groups.google.com/group/symfony-devs/browse_thread/thread/5da0cc27e5b2e939)

symfony 1 development highlights
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=28%2F11%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r31471](http://trac.symfony-project.org/changeset/31471 "31471 revision on trac"): \[1.3, 1.4\] changed the default value for session_cache_limiter to 'null'

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [1bbdb5e](http://github.com/symfony/symfony/commit/1bbdb5ec071e8e22a003bc296e0158524dbfe1c6 "1bbdb5ec071e8e22a003bc296e0158524dbfe1c6 commit on github"): \[Form, FrameworkBundle, TwigBundle\] refactored the PHP and Twig templating layer. Support for theming in PHP templates has been dropped
  * [6a14846](http://github.com/symfony/symfony/commit/6a148465da8080ee3713e80d5bd042972536cfe6 "6a148465da8080ee3713e80d5bd042972536cfe6 commit on github"): \[Validator, Form\] removed support for match-all group *
  * [940ce9a](http://github.com/symfony/symfony/commit/940ce9aedf6299a83590e7361cd75b60213d71d8 "940ce9aedf6299a83590e7361cd75b60213d71d8 commit on github"): \[Validator\] group "Default" is now propagated to validated references when group sequences are validated
  * [46145d8](http://github.com/symfony/symfony/commit/46145d8de7eaeae8d419d44bef79d76ab4603b74 "46145d8de7eaeae8d419d44bef79d76ab4603b74 commit on github"): \[Validator\] fixed exception thrown in Valid constraint to be thrown only when the options are not empty
  * [a0f9331](http://github.com/symfony/symfony/commit/a0f933163f2a0eff36d0a964c471f645b44fb716 "a0f933163f2a0eff36d0a964c471f645b44fb716 commit on github"), [b3ae62e](http://github.com/symfony/symfony/commit/b3ae62e2c434c3600f4eea7136171f75f67977ed "b3ae62e2c434c3600f4eea7136171f75f67977ed commit on github"), [7a255fe](http://github.com/symfony/symfony/commit/7a255fe39f8985023b335815a02bc8bcf7656343 "7a255fe39f8985023b335815a02bc8bcf7656343 commit on github"), [db3e12b](http://github.com/symfony/symfony/commit/db3e12b122493453fc1f86ae517d61715fea6ca1 "db3e12b122493453fc1f86ae517d61715fea6ca1 commit on github"): fixed tests breaking on windows
  * [ac0081f](http://github.com/symfony/symfony/commit/ac0081f8b9b7cdc3ed037374a0ce41115a5bf112 "ac0081f8b9b7cdc3ed037374a0ce41115a5bf112 commit on github"): switched doctypes to HTML5
  * [e204a18](http://github.com/symfony/symfony/commit/e204a1845bbd474c18c3a53ff80499595db1b30f "e204a1845bbd474c18c3a53ff80499595db1b30f commit on github"): \[DoctrineBundle\] made the task works with vendor bundle namespace
  * [d9239d1](http://github.com/symfony/symfony/commit/d9239d1c64b87561ccc58dad44b600aa4734094f "d9239d1c64b87561ccc58dad44b600aa4734094f commit on github"): fixed doctrine command getBundleMetadatas function
  * [b6923dd](http://github.com/symfony/symfony/commit/b6923dd7b9e37affac0ad51a4702982fb300e932 "b6923dd7b9e37affac0ad51a4702982fb300e932 commit on github"): changed Cache-Control default value behavior. The PHP native cache limiter feature has been disabled as this is now managed by the HeaderBag class directly instead (see commit for details)
  * [333504a](http://github.com/symfony/symfony/commit/333504a201538651f8680ebfef29103e5669874a "333504a201538651f8680ebfef29103e5669874a commit on github"): \[OutputEscaper\] fixed output escaping when a variable was decorated with SafeDecorator and passed to another part of the system where decoration also happens on the same un-decorated variable
  * [681ce7f](http://github.com/symfony/symfony/commit/681ce7f46a3e6ccd815ddcdc0fd369b11c41ed73 "681ce7f46a3e6ccd815ddcdc0fd369b11c41ed73 commit on github"): \[Form\] fixed FieldGroup::hasErrors() does not return true if only children have errors
  * [6176063](http://github.com/symfony/symfony/commit/6176063b30b4b52b45f1000de8ff8fbde6800609 "6176063b30b4b52b45f1000de8ff8fbde6800609 commit on github"): \[TwigBundle\] fixed variable reference in the errors block of the form.twig template
  * [a71cad4](http://github.com/symfony/symfony/commit/a71cad480a563f74f558fc9990e85ee8471d432a "a71cad480a563f74f558fc9990e85ee8471d432a commit on github"): \[Validator\] added @validation:GroupSequence to annotation driver
  * [68cebd6](http://github.com/symfony/symfony/commit/68cebd667aa41ee310383826c7ae83733b7e0a4f "68cebd667aa41ee310383826c7ae83733b7e0a4f commit on github"): \[Validator\] Group sequences must now always contain the group &lt;ClassName&gt; and never the group Default since that group is redefined by the group sequence
  * [e0d6aad](http://github.com/symfony/symfony/commit/e0d6aad5f4c3fc39033ed6e64df36f1977d289e5 "e0d6aad5f4c3fc39033ed6e64df36f1977d289e5 commit on github"): \[Form, FrameworkBundle, TwigBundle\] introduced class FieldError to wrap form errors
  * [17c500e](http://github.com/symfony/symfony/commit/17c500e0f0ef5585d3b1f021d11c9b297bafc211 "17c500e0f0ef5585d3b1f021d11c9b297bafc211 commit on github"), [e3551b5](http://github.com/symfony/symfony/commit/e3551b5f87d157887840171f0d5e81f527351cc3 "e3551b5f87d157887840171f0d5e81f527351cc3 commit on github"): \[TwigBundle\] added a yaml filter/encoder
  * [84cf569](http://github.com/symfony/symfony/commit/84cf5698c53e0eb5247179c6a541366b6ccab515 "84cf5698c53e0eb5247179c6a541366b6ccab515 commit on github"): \[TwigBundle\] fixed include tag to reflect the new syntax from Twig
  * [a323dd0](http://github.com/symfony/symfony/commit/a323dd0e9365f65e2f938127d5bab8f69b73a4c8 "a323dd0e9365f65e2f938127d5bab8f69b73a4c8 commit on github"): \[TwigBundle\] added filters from Code helpers
  * [cbb22b4](http://github.com/symfony/symfony/commit/cbb22b4ec4e758ece9e72992cdf185131306304a "cbb22b4ec4e758ece9e72992cdf185131306304a commit on github"): \[Templating\] added an Engine::load() method
  * [67f6889](http://github.com/symfony/symfony/commit/67f6889287a2ed6d41bd86399e1ad27fd565ff23 "67f6889287a2ed6d41bd86399e1ad27fd565ff23 commit on github"): \[TwigBundle\] added support for Twig_Template instances as argument to include tag
  * [21f088d](http://github.com/symfony/symfony/commit/21f088d86aa2dbd440b3265d85af42828f8fdfcd "21f088d86aa2dbd440b3265d85af42828f8fdfcd commit on github"): \[DependencyInjection\] replaced assertEquals(spl_object_hash()) with assertSame
  * [6fa943a](http://github.com/symfony/symfony/commit/6fa943ad5464444801fc8fe581d3a7ce3a5c7525 "6fa943ad5464444801fc8fe581d3a7ce3a5c7525 commit on github"): moved Exception and WebProfiler templates to Twig
  * [97d4dce](http://github.com/symfony/symfony/commit/97d4dce61466cf2fd5d04b732e90d1756b3bcd0d "97d4dce61466cf2fd5d04b732e90d1756b3bcd0d commit on github"): added the ability to configure additional web profiler templates
  * [381347b](http://github.com/symfony/symfony/commit/381347bcfe027603d075c6274e583c90c437da37 "381347bcfe027603d075c6274e583c90c437da37 commit on github"): \[WebProfilerBundle\] fixed data collector loading (they should always be loaded as you can enable the web profiler without the web debug toolbar)
  * [a79ed13](http://github.com/symfony/symfony/commit/a79ed13624152ba6004fbb100c4be7e78c5958e4 "a79ed13624152ba6004fbb100c4be7e78c5958e4 commit on github"): \[Routing\] removed the variable_prefixes and variable_regex Route options
  * [f9e830c](http://github.com/symfony/symfony/commit/f9e830caa2b18d70edc4ac8e7e2d0dc57ca75326 "f9e830caa2b18d70edc4ac8e7e2d0dc57ca75326 commit on github"): \[Form\] added hook method preprocessData() to FieldGroup
  * [d95d336](http://github.com/symfony/symfony/commit/d95d33666d4af474558d776145b93c714df15e49 "d95d33666d4af474558d776145b93c714df15e49 commit on github"): \[HttpFoundation\] fixed class Request to convert empty files to NULL
  * [f2f0d04](http://github.com/symfony/symfony/commit/f2f0d044c33c29855c32f5ed143ae5f9a3e3ae0a "f2f0d044c33c29855c32f5ed143ae5f9a3e3ae0a commit on github"): \[Form, FrameworkBundle\] fixed default values of CheckboxFields
  * [e0aa3f3](http://github.com/symfony/symfony/commit/e0aa3f30a82fbb8cc586d0959eba7d80834ae606 "e0aa3f30a82fbb8cc586d0959eba7d80834ae606 commit on github"): \[Form\] improved FileField to store files in a temporary location in case validation fails
  * [5b056b2](http://github.com/symfony/symfony/commit/5b056b2b9ae5ef816d391819c05f9546f141d4e3 "5b056b2b9ae5ef816d391819c05f9546f141d4e3 commit on github"): refactored web profiler template definitions to make it easier for bundle developers to add their templates
  * [ad68092](http://github.com/symfony/symfony/commit/ad68092291c01ebcff8bec027c41a0863f0390c2 "ad68092291c01ebcff8bec027c41a0863f0390c2 commit on github"): removed the OutputEscaper component, added escape mechanism in the Templating Engine class
  * [60bbb8f](http://github.com/symfony/symfony/commit/60bbb8f38079bffa77a765d663658de853208ebb "60bbb8f38079bffa77a765d663658de853208ebb commit on github"): \[DependencyInjection\] optimized compiled containers: removed the __call() method in Container, removed the $shared variable in the dumped Container classes and optimized the PHP Dumper output
  * [944d91c](http://github.com/symfony/symfony/commit/944d91c1dfc68cf7f769ba7b60cb328fa06b786c "944d91c1dfc68cf7f769ba7b60cb328fa06b786c commit on github"): made some method name changes to have a better coherence throughout the framework
  * [6ab277e](http://github.com/symfony/symfony/commit/6ab277ee411b096d550e4932b39be13ded56bc0b "6ab277ee411b096d550e4932b39be13ded56bc0b commit on github"): added a LazyLoader for the routing
  * [44b8ee3](http://github.com/symfony/symfony/commit/44b8ee3791a6af2eafb9d12f48ae0049f12615b7 "44b8ee3791a6af2eafb9d12f48ae0049f12615b7 commit on github"): added more classes in the class cache
  * [dfe8bb9](http://github.com/symfony/symfony/commit/dfe8bb9fefcabd7876c55aef4b454f3eb52ef110 "dfe8bb9fefcabd7876c55aef4b454f3eb52ef110 commit on github"): added more classes to the bootstrap file
  * [1e983a6](http://github.com/symfony/symfony/commit/1e983a6115e0bb3fee2cf591fbeee52c30884609 "1e983a6115e0bb3fee2cf591fbeee52c30884609 commit on github"): moved static Form configuration to a new class (avoid loading 7 classes just to enable CSRF -- even when no form is present in the page)

Documentation
-------------

  * New <a href="http://trac.symfony-project.org/wiki/InstallingSymfonyInASubDirectoryWithCentOSandPlesk">Installing Symfony In A SubDirectory With CentOS and Plesk</a>, and <a href="http://trac.symfony-project.org/wiki/IRCLogs20101125">IRC Logs 2010-11-25</a> pages

New [job postings](http://trac.symfony-project.com/trac/wiki/JobPostings)
----------------

  * Symfony developer at [Useweb](http://www.useweb.fr) - full-time based in Rennes (Cesson-Sévigné), France - Contact: cv@useweb.com



[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [majaxMarkdown](http://www.symfony-project.org/plugins/majaxMarkdownPlugin): provides a Markdown editor for Symfony, and related rendering tools.
  * [majaxPheanstalk](http://www.symfony-project.org/plugins/majaxPheanstalkPlugin): Tools for integrating with Beanstalkd from within Symfony.
  * [sfContentArchive](http://www.symfony-project.org/plugins/sfContentArchivePlugin): easily generates a 'blog-style' content archive in your symfony application.
  * [sfNubioAddonFunctions](http://www.symfony-project.org/plugins/sfNubioAddonFunctionsPlugin): adds a helper with multiple functions that perform commonly used tasks.
  * [sfOPTView](http://www.symfony-project.org/plugins/sfOPTViewPlugin): allows the use of Open Power Templates in Symfony.
  * [sfPaymentWebMoney](http://www.symfony-project.org/plugins/sfPaymentWebMoneyPlugin): allows you to interact with WebMoney (it's based on sfPaymentPlugin).
  * [sfAdminAjaxTheme](http://www.symfony-project.org/plugins/sfAdminAjaxThemePlugin): ajaxifies symfony admin generator.
  * [sfWidgetWordCounter](http://www.symfony-project.org/plugins/sfWidgetWordCounterPlugin): a jQuery word counter that counts the words in a given input field and displays the counter in a html tag.

Updated plugins
---------------

  * [sfThrift](http://www.symfony-project.org/plugins/sfThriftPlugin):
    * fixed bug in TSocketPool
    * moved server transport classes to its own directory

  * [isicsBreadcrumbs](http://www.symfony-project.org/plugins/isicsBreadcrumbsPlugin):
    * added symfony 1.3 and 1.4 compatibility

  * [sfDoctrineRestGenerator](http://www.symfony-project.org/plugins/sfDoctrineRestGeneratorPlugin):
    * fixed routes names in order to match the documentation
    * added some explanations about the API location
    * added a YAML serializer
    * added the formats_strict option
    * improved the deserialization abstraction
    * improved the documentation
    * added cleanupParameters() method to avoid code duplication
    * added the capacity to serialize single objects
    * improved the performance of the XML serializer
    * added a basic show action
    * added setFieldVisibility() and configureFields() methods in order to share code between index and show actions
    * fixed executeUpdate() so that the content is not a parameter of the request but the content of the PUT request
    * have the XML serializer return a PHP array
    * allow to create or update related objects in the very same request
    * updated documentation
    * enabled the show route by default
    * have executeDelete() refer to the primary key and not systematically the previously hardcoded "id"
    * fixed the way relation fields are hidden, particularly in the case of many-to-many relationships
    * fixed warning when there are no related objects for a n-n relation delcared in the configuration key

  * [sfDoctrinePoll](http://www.symfony-project.org/plugins/sfDoctrinePollPlugin):
    * added the Poll for the question into the admin generator

  * [sfAmf](http://www.symfony-project.org/plugins/sfAmfPlugin):
    * updated Doctrine template

  * [pmSuperfishMenu](http://www.symfony-project.org/plugins/pmSuperfishMenuPlugin):
    * added options managements
    * added autoinclusion of stylesheets and javascripts feature depending on selected options
    * added _authenticated_ menu condition

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * added the pre_list partial

  * [sfHttpHeaderCache](http://www.symfony-project.org/plugins/sfHttpHeaderCachePlugin):
    * added a new session storage class based on sfCacheSessionStorage for selectively enabling/disabling the cache based on the "no_session" parameter of a given route

  * [sfDoctrineRestBasic](http://www.symfony-project.org/plugins/sfDoctrineRestBasicPlugin):
    * added sfDoctrineRestBasicRoute which cleans up the routing by extending the sfRequestRoute to handle the requested actions
    * namespaced the helper classes to stop potential issues
    * added a very important executePut method
    * cleaned up logger code kill multiple instantiation

  * [ddOnlineStore](http://www.symfony-project.org/plugins/ddOnlineStorePlugin):
    * added the color option in the products

  * [idlErrorManagement](http://www.symfony-project.org/plugins/idlErrorManagementPlugin):
    * added a show error page in the admin module
    * switched to use the Doctrine Abstraction layer when saving PHP_errors to be compatible with any database engine

  * [sfTangoIcons](http://www.symfony-project.org/plugins/sfTangoIconsPlugin):
    * added a new animation function
    * updated documentation

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * fixed apostrophe bug that couldn't find the taggable script for media items
    * renamed our richtext and date/time widgets and removed obsolete versions to avoid conflicts with other parties' Symfony plugins (especially sfFormExtrasPlugin)
    * always disable filters for tag admin (otherwise it breaks in its default configuration)
    * added app.yml options to optionally disable the is_active and password fields in user admin, removing the need for separate admin gen modules just because you have Shibboleth or LDAP auth
    * fixed a bug in executeMoveSlot that prevented correct permission checking
    * fixed a bug in executeDeleteSlot that ignored aTools::getAreaOptions
    * password, is_active and permissions fields in user admin can be disabled via app.yml for convenience
    * fixed the description wasn't shown when image was set to false
    * moved the disqus code into the globalJavascripts partial (it should live there, and it keeps layout.php clean)
    * added the escaping stuff to the top of the defaultTemplate in the button thing
    * implemented use_bundled_javascripts similar to use_bundled_stylesheets, allowing you to specify exactly which javascripts you want to override
    * styling fix for validation errors on date and time widgets in event form

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * fixed bug where categories and tags with periods would cause mayhem with the routing system
    * fixed a routing problem involving tags + categories with periods
    * fixed a blog migration bug unsetting categories array
    * end date/time is now validated so you can't set the end prior to the beginning

  * [sfDoctrineActAsCommentable](http://www.symfony-project.org/plugins/sfDoctrineActAsCommentablePlugin):
    * made actions and components easier to override
    * removed groupBy in retrieveCommentCountForObject

  * [apostropheFormBuilder](http://www.symfony-project.org/plugins/apostropheFormBuilderPlugin):
    * form builder plugin migrations for moving from pkFormBuilderPlugin



New [symfony bloggers](http://trac.symfony-project.com/trac/wiki/SymfonyBloggers)
--------------------

  * [My Dev Life!](http://blog.odhodki.si/) \([feed](http://blog.odhodki.si/feed/atom)\) \(English\)
  * [Przypadki » Grzegorz Śliwiński](http://www.fizyk.net.pl/blog/tag/symfony) \([feed](http://www.fizyk.net.pl/blog/tag/symfony.atom)\) \(English, Polish\)

They talked about us
--------------------

  * [New release of sfImageTransformExtraPlugin – automatic thumb removal now documented and several fixes](http://test.ical.ly/2010/11/23/new-release-of-sfimagetransformextraplugin-automatic-thumb-removal-now-documented-and-several-fixes/)
  * [Installation d’Apache+PHP 5.3 avec MacPorts pour Symfony2](http://jerome.tamarelle.net/blog/2010/11/installation-apache-php-5-3-avec-macports-pour-symfony2/)
  * [New symfony plugin, sfContentArchivePlugin](http://www.lyra-cms.com/blog/2010/11/new-symfony-plugin-sfcontentarchiveplugin.html)
  * [Symfony Code'n'Coffe Minsk (Belarus)](http://habrahabr.ru/blogs/symfony/108739/)
  * [A ray of light for PHP](http://pooteeweet.org/blog/0/1854#m1854)
  * [Follow-up release 1.0.12 of sfImageTransformExtraPlugin – replacing RecursiveDirectoryIterator with glob() – less recursion and much much much faster!](http://test.ical.ly/2010/11/25/follow-up-release-1-0-12-of-sfimagetransformextraplugin-replacing-recursivedirectoryiterator-with-glob-less-recursion-and-much-much-much-faster/)
  * [Últimos días para apuntarse al Symfony Live 2011](http://www.symfony.es/2010/11/25/ultimos-dias-para-apuntarse-al-symfony-live-2011/)
  * [Symfony base global validator: sfGlobalValidator](http://www.jnieto.org/article/symfony_base_global_validator_sfglobalvalidator)
  * [sfAdminAjaxThemePlugin now in symfony plugin repository](http://nibsirahsieu.wordpress.com/2010/11/26/sfadminajaxthemeplugin-now-in-symfony-plugin-repository/)
  * [Talking JSON in Symfony2, like really!](http://pooteeweet.org/blog/0/1861#m1861)
  * [Installing Symfony 1.4 on a subdomain with CentOS 5.5 and Plesk 10 on a dedicated server](http://blog.odhodki.si/2010/11/installing-symfony-1-4-on-a-subdomain-with-centos-5-5-and-plesk-on-a-dedicated-server/)
  * [A note on symfony caching](http://www.symfonylab.com/a-note-on-symfony-caching/)
  * [King23 Benchmark – playing a numbers game](http://devedge.wordpress.com/2010/11/28/king23-benchmark-playing-a-numbers-game/)
  * [Symfony Framework](http://edeveloperpardeep.blogspot.com/2010/11/symfony-framework.html)
  * [Embedding forms using sfPropel15Plugin](http://nibsirahsieu.wordpress.com/2010/11/28/embedding-form-using-sfpropel15plugin/)
  * [Symfony 携帯絵文字対応をやってみた](http://blog.cypher-works.com/?p=1235)
  * [Why use CMS and web frameworks in your web development](http://www.tech-thoughts-blog.com/2010/11/why-use-cms-and-web-frameworks-in-your.html)
  * [Cómo configurar varios proyectos Symfony en un mismo servidor](http://senechaux.blogspot.com/2010/11/como-configurar-varios-proyectos.html)
  * [Stable Symfony2 just around the corner](http://clearcode.cc/2010/11/23/stable-symfony2-corner/)
  * [symfony をやってみよう　その3](http://d.hatena.ne.jp/creativeability/20101122/1290425414)
  * [Transacciones MySQL con Doctrine y Symfony](http://jonsegador.com/2010/11/transacciones-mysql-con-doctrine-y-symfony/)
  * [Proyecto Symfony2 Reloaded](http://blog.javiernunez.com/symfony-2-reloaded/proyecto-symfony-2-reloaded)
  * [[event][symfony]第1回Symfony2勉強会に参加しました ](http://d.hatena.ne.jp/Fivestar/20101122/1290414157)
  * [sfForkedDoctrineApply w wersji 1.5](http://www.fizyk.net.pl/blog/sfforkeddoctrineapply-w-wersji-1-5)
  * [fzTagPlugin 1.2.1](http://www.fizyk.net.pl/blog/fztagplugin-1-2-1)
