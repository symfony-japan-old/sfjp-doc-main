A week of symfony #210 (3->9 January 2011)
==========================================

Symfony2 repository received this week a massive amount of commits, mostly on Twig, Form, Security and Doctrine components. Twig bundle was heavily refactored to match the important changes introduced in Twig 1.0 RC1, which was also [published this week](http://blog.twig-project.org/post/2665679442/twig-1-0-0-rc1-released). Security component added a brand-new ACL system and Form component added support for virtual field groups and a FieldFactory mechanism to automatically create fields by introspecting metadata of a class.
Meanwhile, in [the last weekly IRC meeting](http://trac.symfony-project.org/wiki/IRCLogs20110106), Fabien unveiled some interesting information about Symfony2, including a new way to handle web assests and the expected roadmap until its final release.
 
Development mailing list
------------------------

  * [Sending emails from command line scripts with Symfony2 and twig](https://groups.google.com/forum/#!topic/symfony-devs/13tR02waev4)
  * [\[Symfony2\] RFC: Translations](https://groups.google.com/forum/#!topic/symfony-devs/-ZClznjOk7I)
  * [\[symfony2\] redirect issue in action Controller](https://groups.google.com/forum/#!topic/symfony-devs/LaeOR7TQ-0M)
  * [Security Acl - Add custom permissions](https://groups.google.com/forum/#!topic/symfony-devs/BuPiIGzPySs)
  * [RFC: Naming issues](https://groups.google.com/forum/#!topic/symfony-devs/lsUe6_jrAEI)
  * [Symfony2: RFC overwrite specific Resources files of a Bundle](https://groups.google.com/forum/#!topic/symfony-devs/ET78rq4wCsU)
  * [Absolute assets url](https://groups.google.com/forum/#!topic/symfony-devs/19oEaZAz7Ac)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [baf07a1](http://github.com/symfony/symfony/commit/baf07a13acd1270c23b615f8d3077ad560911a35 "baf07a13acd1270c23b615f8d3077ad560911a35 commit on github"), [1af2122](http://github.com/symfony/symfony/commit/1af21221ae2c0003041d7e905f685027280a3152 "1af21221ae2c0003041d7e905f685027280a3152 commit on github"), [3516a04](http://github.com/symfony/symfony/commit/3516a043bcc4dda95b0a6cc74f0bed05b34b844e "3516a043bcc4dda95b0a6cc74f0bed05b34b844e commit on github"): added converter manager and converter interface including tests
  * [cbd6d0a](http://github.com/symfony/symfony/commit/cbd6d0aecee7dd9fa6ca941f6c401e7cfb0ece22 "cbd6d0aecee7dd9fa6ca941f6c401e7cfb0ece22 commit on github"): \[DoctrineBundle\] added a request param converter for Doctrine
  * [f8a88e8](http://github.com/symfony/symfony/commit/f8a88e822f17e2b4bf70bdb7ba8113e97b6e369a "f8a88e822f17e2b4bf70bdb7ba8113e97b6e369a commit on github"), [13fc135](http://github.com/symfony/symfony/commit/13fc13519edfd777fa1fe0fef2a18e0670f530e4 "13fc13519edfd777fa1fe0fef2a18e0670f530e4 commit on github"), [2ee4252](http://github.com/symfony/symfony/commit/2ee4252a1f9500697f8582878fce151c593d1ce0 "2ee4252a1f9500697f8582878fce151c593d1ce0 commit on github"): \[HttpFoundation\] added ArraySessionStorage for usage in tests
  * [385ad72](http://github.com/symfony/symfony/commit/385ad72d643cd58d5d224e3128d4660b73abeeeb "385ad72d643cd58d5d224e3128d4660b73abeeeb commit on github"): \[FrameworkBundle\] converted the special routing resolver to a DIC compiler pass
  * [8e6a384](http://github.com/symfony/symfony/commit/8e6a3849ee68d9d4f4e200579ea1ba41b2b2a42e "8e6a3849ee68d9d4f4e200579ea1ba41b2b2a42e commit on github"): \[TwigBundle\] converted the special Twig Environment class to a DIC compiler class
  * [2985cfa](http://github.com/symfony/symfony/commit/2985cfa5a91deefb401d2eb0047b607041e6afb3 "2985cfa5a91deefb401d2eb0047b607041e6afb3 commit on github"): \[FrameworkBundle\] converted the special Profiler class to a DIC compiler class
  * [59996bd](http://github.com/symfony/symfony/commit/59996bd8b91ceac3327eb14ecd5d1cb8e1c1efe5 "59996bd8b91ceac3327eb14ecd5d1cb8e1c1efe5 commit on github"): \[TwigBundle\] fixed form.twig calls to {% display %}
  * [46949e2](http://github.com/symfony/symfony/commit/46949e2c22c7663516d99b88a51e919160fba6b6 "46949e2c22c7663516d99b88a51e919160fba6b6 commit on github"): \[DoctrineBundle, DoctrineMongoDBBundle\] makes it possible to use shortcuts for defining document or entity classes when using the DaoAuthenticationProvider
  * [ba2b1aa](http://github.com/symfony/symfony/commit/ba2b1aad281d389d9464bc53ef31e565272cdb5e "ba2b1aad281d389d9464bc53ef31e565272cdb5e commit on github"): refactored Doctrine*Bundle to allow a much more flexible configuration
  * [db5e180](http://github.com/symfony/symfony/commit/db5e180d3750687ab6d65ebbdd951b80e16590d6 "db5e180d3750687ab6d65ebbdd951b80e16590d6 commit on github"): tweaked DI container
  * [6aa750d](http://github.com/symfony/symfony/commit/6aa750d1ceb49dfae1e9d9f8d782ce385401f9b4 "6aa750d1ceb49dfae1e9d9f8d782ce385401f9b4 commit on github"): \[DoctrineBundle\] added tests for DoctrineConverter class
  * [46b1b5b](http://github.com/symfony/symfony/commit/46b1b5bd60432ba07bde2732a2310a5e76f94174 "46b1b5bd60432ba07bde2732a2310a5e76f94174 commit on github"): \[Security\] LogoutListener should not invoke handlers' logout() method if token is empty
  * [500e02d](http://github.com/symfony/symfony/commit/500e02d4fd123cc03f7456527a9f70cdedb2d3d5 "500e02d4fd123cc03f7456527a9f70cdedb2d3d5 commit on github"): fixed inconsistency between MongoDB and ORM Annotation Reader definition that lead to a bug in the common code
  * [c886d88](http://github.com/symfony/symfony/commit/c886d88bf367c2f7be1afc3e861c05b8e2baf9e6 "c886d88bf367c2f7be1afc3e861c05b8e2baf9e6 commit on github"), [5c73619](http://github.com/symfony/symfony/commit/5c73619d801ad0e006a9bc3d05c820ef0439afc0 "5c73619d801ad0e006a9bc3d05c820ef0439afc0 commit on github"): \[DependencyInjection\] forced loading of class file when resolving interface injections
  * [b428845](http://github.com/symfony/symfony/commit/b4288459cc440fda95eb7f2b431d04dd3e54f80e "b4288459cc440fda95eb7f2b431d04dd3e54f80e commit on github"): added ACL system to the Security Component
  * [49a3e52](http://github.com/symfony/symfony/commit/49a3e52fa8c25a7307b4ce33fa679b9cd068f368 "49a3e52fa8c25a7307b4ce33fa679b9cd068f368 commit on github"): \[HttpFoundation\] changed the default name of the session to _SESS as using _SESSION does not seem to work with PHP 5.3.
  * [62cd09e](http://github.com/symfony/symfony/commit/62cd09e7081795809a4f1f5e24f2db287b905913 "62cd09e7081795809a4f1f5e24f2db287b905913 commit on github"): \[TwigBundle\] replaced the asset tag with an asset function (from {% asset css/foo.css %} to {{ asset('css/foo.css') }}
  * [d8b8ae0](http://github.com/symfony/symfony/commit/d8b8ae0608b8b9933865a84f8d3acb6e044bbfb4 "d8b8ae0608b8b9933865a84f8d3acb6e044bbfb4 commit on github"): \[FrameworkBundle, TwigBundle\] introduced field_row template for Form rendering
  * [b9c2e98](http://github.com/symfony/symfony/commit/b9c2e983159d31b217873d446138fde6e0e10489 "b9c2e983159d31b217873d446138fde6e0e10489 commit on github"): \[Form, Locale\] implemented LocaleField and added script for updating ICU data
  * [52ecffe](http://github.com/symfony/symfony/commit/52ecffe51b93afa93a38dd46839889ca9dd5c287 "52ecffe51b93afa93a38dd46839889ca9dd5c287 commit on github"): \[Validator\] implemented Locale constraint
  * [2daa6b5](http://github.com/symfony/symfony/commit/2daa6b5bfedac13702cd75f4dc5d12a5d742724d "2daa6b5bfedac13702cd75f4dc5d12a5d742724d commit on github"): \[TwigBundle\] fixed display of DateFields in twig templates
  * [a99d8c8](http://github.com/symfony/symfony/commit/a99d8c8558717d5d0cd29bcdc23f5ac077ade106 "a99d8c8558717d5d0cd29bcdc23f5ac077ade106 commit on github"): fixed possible duplicate security identities
  * [55a48bc](http://github.com/symfony/symfony/commit/55a48bcfa629059b3b86c4319f38a15fbc8920e9 "55a48bcfa629059b3b86c4319f38a15fbc8920e9 commit on github"): optimized AclVoter and added unit tests
  * [fa7fded](http://github.com/symfony/symfony/commit/fa7fdedf4b4ea492d38dff7e5f1a4094b6cd7ff0 "fa7fdedf4b4ea492d38dff7e5f1a4094b6cd7ff0 commit on github"): introduced meta-bundle DoctrineAbstractBundle to squash 400+ loc of code duplication from ORM and MongoDB Bundles
  * [302dbd1](http://github.com/symfony/symfony/commit/302dbd12257fb00cc7198bac01af6ad4994cc908 "302dbd12257fb00cc7198bac01af6ad4994cc908 commit on github"): refactor Doctrine Bundle to use Symfony DIC Enabled EventManager
  * [eb4788e](http://github.com/symfony/symfony/commit/eb4788e98e4e578ae4178536c41536a79b4a1dfd "eb4788e98e4e578ae4178536c41536a79b4a1dfd commit on github"): \[DependencyInjection\] made service keys and aliases case insensitive (as method names are case insensitive in PHP)
  * [840bd8a](http://github.com/symfony/symfony/commit/840bd8aacd4ab48474e0600ecd54acee7b82f080 "840bd8aacd4ab48474e0600ecd54acee7b82f080 commit on github"): \[TwigBundle\] removed usage of HelperTokenParser for the 'render' tag
  * [3f492ca](http://github.com/symfony/symfony/commit/3f492cae400bcfed53537c675d69cd13e64ef699 "3f492cae400bcfed53537c675d69cd13e64ef699 commit on github"): \[TwigBundle\] removed usage of HelperTokenParser for the js/css tags
  * [5c6b594](http://github.com/symfony/symfony/commit/5c6b594daed30f30bd5152d3021943b1f6642978 "5c6b594daed30f30bd5152d3021943b1f6642978 commit on github"): \[TwigBundle\] converted form filters to functions
  * [8b843e2](http://github.com/symfony/symfony/commit/8b843e266203e3c5416eb01c72dffe91d87a7e1a "8b843e266203e3c5416eb01c72dffe91d87a7e1a commit on github"): \[TwigBundle\] fixed trans tag due to Twig changes
  * [ba422e8](http://github.com/symfony/symfony/commit/ba422e8472c8c16235760cb095f228f6ee9496f5 "ba422e8472c8c16235760cb095f228f6ee9496f5 commit on github"): \[Form\] added support for virtual field groups
  * [708c780](http://github.com/symfony/symfony/commit/708c7802135aa88e6f66223fbe45fc6d36186ce1 "708c7802135aa88e6f66223fbe45fc6d36186ce1 commit on github"): \[Validator\] renamed @Validation constraint to @Set
  * [8513082](http://github.com/symfony/symfony/commit/85130820079a65494d7cd4834eb120b126650e56 "85130820079a65494d7cd4834eb120b126650e56 commit on github"): \[Form, HttpFoundation\] improved File and UploadedFile class
  * [e9a7531](http://github.com/symfony/symfony/commit/e9a7531a26cccd06e701e3b8ee9df5faa3f4d075 "e9a7531a26cccd06e701e3b8ee9df5faa3f4d075 commit on github"): \[Form\] added the constrained method Field::isTransformationSuccessful()
  * [48af2fc](http://github.com/symfony/symfony/commit/48af2fc86edffd83034e2d3d3b94dc75511eae97 "48af2fc86edffd83034e2d3d3b94dc75511eae97 commit on github"): \[Form, FrameworkBundle, HttpFoundation\] the session is now automatically started when a form is CSRF protected
  * [acdd5c0](http://github.com/symfony/symfony/commit/acdd5c06de1e62caa042df8a37360403475c58f0 "acdd5c06de1e62caa042df8a37360403475c58f0 commit on github"): \[Form\] changed value transformers to throw UnexpectedTypeException instances
  * [114b2cf](http://github.com/symfony/symfony/commit/114b2cf6c1a3ec20957db2333a1dc6d0211032dc "114b2cf6c1a3ec20957db2333a1dc6d0211032dc commit on github"): \[FrameworkBundle\] attributes can now be passed when rendering form fields with the PHP renderer
  * [39c9bf1](http://github.com/symfony/symfony/commit/39c9bf160e5716aec0f42b3552524804e534b8e5 "39c9bf160e5716aec0f42b3552524804e534b8e5 commit on github"): \[Validator\] implemented @Ip constraint
  * [9b10c8a](http://github.com/symfony/symfony/commit/9b10c8a86652d50e4b3e38dc5dd8ca14ffb5619c "9b10c8a86652d50e4b3e38dc5dd8ca14ffb5619c commit on github"): \[WebProfileBundle\] added more information to the Response content returned when an intercept is redirected
  * [0e487cd](http://github.com/symfony/symfony/commit/0e487cdda65766d5af9d9181cfc7da5dfb30145f "0e487cdda65766d5af9d9181cfc7da5dfb30145f commit on github"): \[TwigBundle\] replaced current {{ foo }} syntax for translation placeholders to %foo%
  * [b60d254](http://github.com/symfony/symfony/commit/b60d254be2f9b9a8b1340a8f7b40270748692ca5 "b60d254be2f9b9a8b1340a8f7b40270748692ca5 commit on github"): \[TwigBundle\] added request and session as global variables (removed the '_view' variable from templates, removed the 'flash()' function because it's now available from the session directly)
  * [7b7e83f](http://github.com/symfony/symfony/commit/7b7e83f428fceec8ad20d23e7247a9116f08dc2f "7b7e83f428fceec8ad20d23e7247a9116f08dc2f commit on github"): removed js and css helpers and Twig integration as they do not work as expected
  * [7fdc61f](http://github.com/symfony/symfony/commit/7fdc61f2723232ad9e256b01f0ea941c69f9eb63 "7fdc61f2723232ad9e256b01f0ea941c69f9eb63 commit on github"): \[TwigBundle\] added a way to register Twig globals from configuration
  * [aea712d](http://github.com/symfony/symfony/commit/aea712d8a20ed6a0cb46b49726b0a2cf5b150bf9 "aea712d8a20ed6a0cb46b49726b0a2cf5b150bf9 commit on github"): \[ZendBundle\] added a simple way to add new writers (add a service with a zend.logger.writer tag)
  * [1148519](http://github.com/symfony/symfony/commit/114851969581bbcdae88ea4ac293ca47e878cb1c "114851969581bbcdae88ea4ac293ca47e878cb1c commit on github"): \[HttpKernel\] unified paths on Windows and *nix
  * [1e27d43](http://github.com/symfony/symfony/commit/1e27d4359c9f70484ca28645da3a288f0267555a "1e27d4359c9f70484ca28645da3a288f0267555a commit on github"): \[DoctrineBundle\] added class_metadata_factory_name Configuration option
  * [3ab82cb](http://github.com/symfony/symfony/commit/3ab82cbd534d19fa2f164c099d87782aedd86eea "3ab82cbd534d19fa2f164c099d87782aedd86eea commit on github"): \[FrameworkBundle, Security\] created DIC aliases for security providers that are explicit services
  * [598d458](http://github.com/symfony/symfony/commit/598d458a3c5e45f67a2f6686433272abde29b1e3 "598d458a3c5e45f67a2f6686433272abde29b1e3 commit on github"): added CompatAssetsBundle to reintroduce the deprecated css/js helpers/tags
  * [4b78c43](http://github.com/symfony/symfony/commit/4b78c4376ff02a33afc6c0ac720cf014ac4d90e0 "4b78c4376ff02a33afc6c0ac720cf014ac4d90e0 commit on github"): \[Form\] added FieldFactory mechanism to automatically create fields by introspecting metadata of a class
  * [c5ef113](http://github.com/symfony/symfony/commit/c5ef113b186caa09b951c48cc4f637c2660cef6f "c5ef113b186caa09b951c48cc4f637c2660cef6f commit on github"): DI container optimization
  * [da5475e](http://github.com/symfony/symfony/commit/da5475ec428102c90067c284a8995a87f91a8013 "da5475ec428102c90067c284a8995a87f91a8013 commit on github"): service visibility changes
  * [b5e26d9](http://github.com/symfony/symfony/commit/b5e26d9db8c723c8812fa4dee6bd2c8a11dd6c5a "b5e26d9db8c723c8812fa4dee6bd2c8a11dd6c5a commit on github"): \[SwiftmailerBundle\] added more private services
  * [f946355](http://github.com/symfony/symfony/commit/f946355f80373f9a985937394d181144742a3b15 "f946355f80373f9a985937394d181144742a3b15 commit on github"): \[TwigBundle\] added a form_row() function
  * [584769d](http://github.com/symfony/symfony/commit/584769dd164b1e8f82888c88d436f84fc3146aec "584769dd164b1e8f82888c88d436f84fc3146aec commit on github"): \[HttpFoundation\] added removeFlash &amp; clearFlashes methods to the Session
  * [afc2f96](http://github.com/symfony/symfony/commit/afc2f965498e1e482ab2c3fcc30b87438f12ac13 "afc2f965498e1e482ab2c3fcc30b87438f12ac13 commit on github"), [ed359af](http://github.com/symfony/symfony/commit/ed359af5438b93bf0ab1f78a041528a92713db0a "ed359af5438b93bf0ab1f78a041528a92713db0a commit on github"): \[Templating\] added Global variables as they are implemented with Twig
  * [911dbe9](http://github.com/symfony/symfony/commit/911dbe9cc4286e51933a0cee6589289afa3bba08 "911dbe9cc4286e51933a0cee6589289afa3bba08 commit on github"): removed a circular reference in the definition of the templating and Twig services (added a new TemplateNameConverter that parses a template name, removed the dependency between the Twig loader and the Templating engine)
  * [af8ebea](http://github.com/symfony/symfony/commit/af8ebeaabbb3878e5314d73c2ee74b184775e5a9 "af8ebeaabbb3878e5314d73c2ee74b184775e5a9 commit on github"): \[DependencyInjection\] added automatic detection for service circular references
  * [cfd4e21](http://github.com/symfony/symfony/commit/cfd4e2186f0dc444bec4438a165eef317c58e4e2 "cfd4e2186f0dc444bec4438a165eef317c58e4e2 commit on github"): fixed UniversalClassLoader matching collisions
  * [314defa](http://github.com/symfony/symfony/commit/314defa8b4f70b41f1c5476d310861766e22ef29 "314defa8b4f70b41f1c5476d310861766e22ef29 commit on github"): added generic encoder factory
  * [9553971](http://github.com/symfony/symfony/commit/9553971d06875d417695c4a63e03885a608dafb7 "9553971d06875d417695c4a63e03885a608dafb7 commit on github"): \[TwigBundle\] allowed Renderer::evaluate() even when Request and Session are not available
  * [2ded40f](http://github.com/symfony/symfony/commit/2ded40fb7534388209c7522317f8c455480da5d3 "2ded40fb7534388209c7522317f8c455480da5d3 commit on github"): \[TwigBundle\] added a way to easily register extensions from the configuration
  * [964bf43](http://github.com/symfony/symfony/commit/964bf4356ecedcdf02e0bce2d9d7fd0681cd7904 "964bf4356ecedcdf02e0bce2d9d7fd0681cd7904 commit on github"): fixed Security tests failing when Doctrine2 is not present
  * [0c50ca8](http://github.com/symfony/symfony/commit/0c50ca87755daf2da40bdca9b8da4868f9b3c7a1 "0c50ca87755daf2da40bdca9b8da4868f9b3c7a1 commit on github"): \[TwigBundle\] renderer::evaluate() should ensure the Request is both defined and non-empty
  * [554c86c](http://github.com/symfony/symfony/commit/554c86c5895f9ef3e48d6da3d4155b2fd763332d "554c86c5895f9ef3e48d6da3d4155b2fd763332d commit on github"): \[DependencyInjection\] added hasInterfaceInjectorForClass() which is helpful for extension loader methods
  * [f2ac2a4](http://github.com/symfony/symfony/commit/f2ac2a4c8a1e3aa1f75622c358a83984af3bf017 "f2ac2a4c8a1e3aa1f75622c358a83984af3bf017 commit on github"): changed templating to use setter injection for renderers
  * [bc2ca8f](http://github.com/symfony/symfony/commit/bc2ca8f1cf77a60fdf460614fc9cdc218110dd43 "bc2ca8f1cf77a60fdf460614fc9cdc218110dd43 commit on github"): made PHP renderer optional in Templating
  * [3785a99](http://github.com/symfony/symfony/commit/3785a99b947c26b84585ffe34225b600822b382e "3785a99b947c26b84585ffe34225b600822b382e commit on github"): added visibility to aliases
  * [a116199](http://github.com/symfony/symfony/commit/a11619973b9fea3b4452a9429968e1905c831392 "a11619973b9fea3b4452a9429968e1905c831392 commit on github"): \[DependencyInjection\] fixed xml validation for extension in phar archive
  * [50809d2](http://github.com/symfony/symfony/commit/50809d2ae03d4ce0d744ff6fd2b3c515da353d6c "50809d2ae03d4ce0d744ff6fd2b3c515da353d6c commit on github"): \[TwigBundle\] added the security context and the user as global variables when they are defined
  * [10fee8c](http://github.com/symfony/symfony/commit/10fee8c8bbd42a8a13efc9bc8e6b9e51ce8edb2a "10fee8c8bbd42a8a13efc9bc8e6b9e51ce8edb2a commit on github"): \[HttpKernel\] added escaping to the profiler SQLite storage

Documentation
-------------

  * New <a href="http://trac.symfony-project.org/wiki/IRCLogs20110106">IRC logs 2011-01-06</a> page

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfAmazon](http://www.symfony-project.org/plugins/sfAmazonPlugin): Allows you to manage amazon aws servers from symfony cli. Also includes widgets, validators, and helpers that you can use within your symfony projects.
  * [apostrophePeople](http://www.symfony-project.org/plugins/apostrophePeoplePlugin): a simple system for creating and organizing person profiles (plugin for the Apostrophe CMS).
  * [sfPostMark](http://www.symfony-project.org/plugins/sfPostMarkPlugin): easy integration with postmarkapp.com.
  * [gbRememberMe](http://www.symfony-project.org/plugins/gbRememberMePlugin): changes the behavior of the "remember me" feature of the sfDoctrineGuard plugin, allowing to remember multiple browser instances on multiple computers and detecting cookie theft.

Updated plugins
---------------

  * [cleverFilesystem](http://www.symfony-project.org/plugins/cleverFilesystemPlugin):
    * added passive mode capacity for FTP filesystems

  * [sfDoctrineNestedSet](http://www.symfony-project.org/plugins/sfDoctrineNestedSetPlugin):
    * fully functional (add, delete, move nodes and subtrees) Doctrine NestedSet plugin

  * [sfCKEditor](http://www.symfony-project.org/plugins/sfCKEditorPlugin):
    * fixed bug when inserting content with special characters

  * [sfDoctrineRestGenerator](http://www.symfony-project.org/plugins/sfDoctrineRestGeneratorPlugin):
    * fixed XML and YAML unserializer in order to get the root of the data directly
    * have the XML unserializer deal correctly with collections and single records
    * removed useless underscoring of variables from the action body

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * fixed an incompatibility between preloadTags() and the Doctrine query cache
    * the trim line did not work in IE because IE doesn't have String.trim. Switched to jQuery's trim function
    * do not add empty tag names

  * [sfYandexYML](http://www.symfony-project.org/plugins/sfYandexYMLPlugin):
    * added unit tests

  * [sfProjectAnalyser](http://www.symfony-project.org/plugins/sfProjectAnalyserPlugin):
    * sdded plugin config controls so the user knows its custom config file must be upgraded
    * code cleanup
    * updated doc &amp; roadmap
    * refactored the way the plugin's config controls are done
    * started the "ignore files and objects" feature
    * implemented the "ignore" feature for the partials, applications, classes, modules, actions, templates and layouts
    * fixed wrong count of alerts when using the XML output
    * fixed the color reporting for modules
    * fixed the return code values
    * deleted the sfProjectAnanlyserPlugin from the default config

  * [sfFormButtons](http://www.symfony-project.org/plugins/sfFormButtonsPlugin):
    * changed button_to_url to only set an onclick-Handler, if there is none present

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * you can now see the embedded video at the annotation step fo the "add media" process
    * fixed useless metaDescription slots being created with no page id
    * correctly render normal script src tags for externally hosted JS files such as addthis when the minifier is active
    * fixed slideshows should not say "click for next image" if there is only one image
    * all the slots now extend aSlotActions and aSlotComponents, which are empty extensions of BaseaSlotActions and BaseaSlotComponents
    * all private items in PluginaPage are now protected so aPage can modify them as needed
    * create a lessc compiler object only when needed; let the autoloader find it
    * added $word_limit parameter to getAreaText() and getAreaBasicHtml()
    * added og-meta slot to the layout.php so og meta data can be set and tossed up into the heading from Pages, Blog Posts, and Events
    * fixed Apostrophe reaction when a video is not permitted to be played in your country
    * clear call to action to configure unconfigured media services
    * error404Success and error404Template work together to allow admins to edit / change the error404 page contents

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * migrated all events that run from 12am to 12am to have null start and end times (the new representation of an all day event)
    * fixed event slots not being ordered by start date
    * added og-meta information to the event and blog showSuccess
    * set the published_at date on a_page when it is a virtual page corresponding to an a_blog_item
    * fixed a bug that was displaying the the same time twice if the starttime and endtime were the same
    * getQuery was failing for the title search case because it wasn't returning the query
    * event slot typeahead had a refactoring-related bug


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [www.resursecrestine.ro](http://www.resursecrestine.ro/): \(Romanian\) a romanian Christian Resources website
  * [Attractiveworld](http://www.attractiveworld.net/): \(French\) singles social network
  * [msb-online](http://www.msb-online.org/): \(English\) Mediterranean School of Business academy
  * [Art-afriain.fr](http://www.art-africain.fr/): \(French\) african art gallery
  * [Webdigi Web Development](http://www.webdigi.co.uk): \(English\) Webdigi develops high performance web applications and websites


They talked about us
--------------------

  * [Introducing phpOpenNOS](http://www.leftontheweb.com/message/Introducing_phpOpenNOS)
  * [New release of tjSolrDoctrineBehaviorPlugin](http://www.miximum.fr/actus/558-new-release-of-tjsolrdoctrinebehaviorplugin)
  * [Anteprima del prossimo admin generator](http://www.symfony.it/articoli/399/anteprima-del-prossimo-admin-generator/)
  * [Allowing bulk uploads by repetitive form saving for ZIP archives in symfony](http://test.ical.ly/2011/01/04/allowing-bulk-uploads-by-repetitive-form-saving-for-zip-archives-in-symfony/)
  * [In case you wonder how to run a functional lime test in a symfony plugin](http://test.ical.ly/2011/01/05/in-case-you-wonder-how-to-run-a-functional-lime-test-in-a-symfony-plugin/)
  * [Stored functions with Symfony and Doctrine](http://www.whiteoctober.co.uk/blog/2011/01/05/stored-functions-with-symfony-and-doctrine/)
  * [Twig, template engine per PHP](http://programmazione.it/index.php?entity=eitem&amp;idItem=46178)
  * [Symfony Code'n'Coffee Minsk (Belarus) Jan 2011](http://habrahabr.ru/blogs/symfony/111242/)
  * [A continuous deployment process for symfony plugins](http://test.ical.ly/2011/01/07/a-continuous-deployment-process-for-symfony-plugins/)
  * [Adding custom information to your Doctrine schema](http://www.jnieto.org/article/adding_custom_information_to_your_doctrine_schema)
  * [Now a Sensio partner](http://www.leftontheweb.com/message/Now_a_Sensio_partner)
  * [Se publica el programa definitivo de las conferencias Symfony Live 2011](http://www.symfony.es/2011/01/07/se-publica-el-programa-definitivo-de-las-conferencias-symfony-live-2011/)
  * [Generating URL from Model or Task](http://symfony-hribo.blogspot.com/2011/01/generating-url-from-model-or-task.html)
  * [Cherokee http server and symfony 1.4](http://www.fizyk.net.pl/blog/cherokee-http-server-and-symfony-1-4-en)
  * [Passing parameters from the action to the view: Symfony vs Yii](http://www.jnieto.org/article/passing_parameters_from_the_action_to_the_view_symfony_vs_yii)
  * [[Symfony]Doctrineを使ってユーザー認証を行う](http://d.hatena.ne.jp/perezvon/20110109/1294579827)
  * [symfony backend: displaying thumbnail or photo in listing](http://www.entroducing.com/view/symfony-backend-displaying-thumbnail-or-photo-in-listing)
  * [Symfony 1.4 admin generator sort on custom column](http://stereointeractive.com/blog/2011/01/08/symfony-1-4-admin-generator-sort-on-custom-column/)
  * [Using the native MySQL ENUM type in Symfony 1.4 and Doctrine](http://imanpage.com/code/using-th-native-mysql-enum-type-symfony-14-and-doctrine)
  * [Symfonyは情報が少ない](http://blog.livedoor.jp/nakatatu2011/archives/51726224.html)
  * [Symfony Doctrine Row Count](http://www.tutorialjinni.com/2011/01/symfony-doctrine-row-count.html)
  * [phpBB 4 Meets Symfony 2 (Part 1 of 4)](http://afreeland.tk/html/phpbb-4-meets-symfony-2-part-1-of-4.html)
  * [Add multiple connections of database in Symfony and Doctrine](http://www.bloglaptrinh.info/tutorials/symfony/add-multiple-connections-of-database-in-symfony-and-doctrine/)
  * [symfony助手及助手参数](http://www.cotrun.net/blog/599.html)
  * [Database icon loss in symfony debug bar](http://www.noop.lv/2011/01/05/database-icon-loss-in-symfony-debug-bar/)
  * [Symfony 2: Evolution du code source du framework PHP](http://www.waebo.com/symfony-2-evolution-du-code-source-du-framework-php.html)
  * [How to reduce admin generator query in Symfony 1.4](http://www.techiecorner.com/1963/how-to-reduce-admin-generator-query-in-symfony-1-4/)
  * [disable csrf_token ใน form ของ symfony](http://www.meteenee.com/disable-csrf_token-%E0%B9%83%E0%B8%99-form-%E0%B8%82%E0%B8%AD%E0%B8%87-symfony)
  * [PHP: Symfony 2 e i bundle](http://francescoagati.wordpress.com/2011/01/03/php-symfony-2-e-i-bundle/)
