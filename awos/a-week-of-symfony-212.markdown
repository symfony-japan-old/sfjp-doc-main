---
layout: default
title: "A week of symfony #212 (17->23 January 2011)"
---

A week of symfony #212 (17->23 January 2011)
============================================

This week, [Symfony2 PR5 was released](http://www.symfony-project.org/blog/2011/01/17/symfony2-pr5-released) and the [definitive roadmap for Symfony2](http://www.symfony-project.org/blog/2011/01/17/stabilizing-symfony2) was laid out.
Meanwhile, the activity of the [developers mailing list](https://groups.google.com/forum/#!forum/symfony-devs) skyrocketed with tens of messages openly discussing every important feature of Symfony2. As a result of these discussions, the [bundle management was completely refactored](https://github.com/symfony/symfony/commit/6d1e91a1faecb1f46a781d0e4ce37ed9d3fba3cc).

Development mailing list
------------------------

  * [\[Symfony 2\] Template name format?](https://groups.google.com/forum/#!topic/symfony-devs/C8utP9PJldU)
  * [\[Symfony2\] security](https://groups.google.com/forum/#!topic/symfony-devs/d14p2oD49kI)
  * [Dependency Injection and Remoting](https://groups.google.com/forum/#!topic/symfony-devs/d5YFuY7LYZc)
  * [\[Symfony2\] a single validator for class and property level validation](https://groups.google.com/forum/#!topic/symfony-devs/JRpPUbFOdVU)
  * [Parameter converters RFC](https://groups.google.com/forum/#!topic/symfony-devs/jTE2WG2SnzY)
  * [\[Symfony2\] Directory structure, third-party code, and more](https://groups.google.com/forum/#!topic/symfony-devs/cudAyOwgWBE)
  * [\[Symfony2\] RFC: Symfony2 Autoloader in a dedicated component?](https://groups.google.com/forum/#!topic/symfony-devs/-H2hwlJDm58)
  * [\[Symfony2\] setValidationGroups() gone](https://groups.google.com/forum/#!topic/symfony-devs/SRPJ4k6bFU0)
  * [RFC - Change option naming convention to camelcase](https://groups.google.com/forum/#!topic/symfony-devs/DIFV43r1ULk)
  * [\[Symfony2\] RFC: Ability for extension to automatically register routes](https://groups.google.com/forum/#!topic/symfony-devs/s-J_Ceidj9A)
  * [Generation of Proxies and Hydrators](https://groups.google.com/forum/#!topic/symfony-devs/v66Nd5D015w)
  * [\[Symfony2\] Ordering things: first match wins or last overrides previous](https://groups.google.com/forum/#!topic/symfony-devs/djJi528v8EE)
  * [Improving the event management](https://groups.google.com/forum/#!topic/symfony-devs/dG4MTWMlSCE)
  * [\[Symfony2\] \[RFC\] Bundle namespace naming conventions](https://groups.google.com/forum/#!topic/symfony-devs/l4Cqr35cxK4)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [8235f71](http://github.com/symfony/symfony/commit/8235f71f57365397e3305371c149ab001c6d4af9 "8235f71f57365397e3305371c149ab001c6d4af9 commit on github"): \[DoctrineMongoDBBundle\] switched to compiler passes for proxy/hydrator directory creation and event listeners
  * [105d591](http://github.com/symfony/symfony/commit/105d5918bc8ab4c25cc9aa1bbd9a923979cca08f "105d5918bc8ab4c25cc9aa1bbd9a923979cca08f commit on github"): added the roles in the Security panel of the profiler
  * [d06f805](http://github.com/symfony/symfony/commit/d06f805d9555da0e3c3d522a54e5f752b0e712f2 "d06f805d9555da0e3c3d522a54e5f752b0e712f2 commit on github"): added a priority for data collectors
  * [e0050df](http://github.com/symfony/symfony/commit/e0050dfc8f14904b32c7a5b96da771429d928b88 "e0050dfc8f14904b32c7a5b96da771429d928b88 commit on github"): \[FrameworkBundle\] added a compiler pass for translation loaders
  * [c5f2ec8](http://github.com/symfony/symfony/commit/c5f2ec8d2ded195ef3a2f6c6ca5946f2b752320b "c5f2ec8d2ded195ef3a2f6c6ca5946f2b752320b commit on github"): made DIC tags only available during compilation phase
  * <del>[dba8c67](http://github.com/symfony/symfony/commit/dba8c6794184731b8e7d43e28aa08c4b3e385573 "dba8c6794184731b8e7d43e28aa08c4b3e385573 commit on github"): \[FrameworkBundle\] disabled translator if not explicitely enabled</del>
  * [d406ca0](http://github.com/symfony/symfony/commit/d406ca0d6b6cba724dfda1d2bcdf1ad78b515787 "d406ca0d6b6cba724dfda1d2bcdf1ad78b515787 commit on github"): \[FrameworkBundle\] made ESI optional (should now be enabled explicitely)
  * [ea27927](http://github.com/symfony/symfony/commit/ea279278ae722f747ef5c0ceecc9cdf99d854c33 "ea279278ae722f747ef5c0ceecc9cdf99d854c33 commit on github"): disable session if not explicitely enabled
  * [fac7885](http://github.com/symfony/symfony/commit/fac78859d53a9cfd8e2d7439f78a10639900252a "fac78859d53a9cfd8e2d7439f78a10639900252a commit on github"): \[Form\] added a row() PHP helper equivalent to the Twig form_row()
  * [15575bc](http://github.com/symfony/symfony/commit/15575bccc411b25f3f87aa4a13add1254dc6d913 "15575bccc411b25f3f87aa4a13add1254dc6d913 commit on github"): made order of template engine and data collector more predictable
  * [22aba90](http://github.com/symfony/symfony/commit/22aba900d4af21704abbcc232826584c97087e10 "22aba900d4af21704abbcc232826584c97087e10 commit on github"): \[TwigBundle\] normalized names of templates and enable cache found templates file names
  * [9f4863e](http://github.com/symfony/symfony/commit/9f4863e4dc6941d98fe535656e174002fa4f9ebb "9f4863e4dc6941d98fe535656e174002fa4f9ebb commit on github"): \[DoctrineBundle\] cleaned up doctrine:generate:entity
  * [40a70cd](http://github.com/symfony/symfony/commit/40a70cd6f4d9a0375d9a6b4a98d938a5b723556b "40a70cd6f4d9a0375d9a6b4a98d938a5b723556b commit on github"): simplified TemplateNameParser::parse() return value
  * [267a7e6](http://github.com/symfony/symfony/commit/267a7e69562cffcb3c9895c53c21120f4a2bc441 "267a7e69562cffcb3c9895c53c21120f4a2bc441 commit on github"): \[HttpKernel\] fixed Cache, to respect the  variable and trigger error handling
  * [ae40a5d](http://github.com/symfony/symfony/commit/ae40a5da5392a0d0f5252605fdbdc74222b78d51 "ae40a5da5392a0d0f5252605fdbdc74222b78d51 commit on github"): \[Form\] use HTML5 number and url input types for number and url fields
  * [5995772](http://github.com/symfony/symfony/commit/59957727e393717491f49683671996176261a2a0 "59957727e393717491f49683671996176261a2a0 commit on github"): \[Form\] allow setting the date_format option via DateTimeField
  * [de3f240](http://github.com/symfony/symfony/commit/de3f240ea4663c3fbdca8e69266767828b8d50e9 "de3f240ea4663c3fbdca8e69266767828b8d50e9 commit on github"): \[Form\] added required attribute on input field templates
  * [8f8f53d](http://github.com/symfony/symfony/commit/8f8f53d63103392ab2d7632df3caec5b9617a3db "8f8f53d63103392ab2d7632df3caec5b9617a3db commit on github"): \[Form, FrameworkBundle\] implemented FormFactory and added it to the DI container
  * [6ad22fd](http://github.com/symfony/symfony/commit/6ad22fd70236603bd14753e3d116edc7286fc8c3 "6ad22fd70236603bd14753e3d116edc7286fc8c3 commit on github"): \[Validator\] added ValidatorFactory for programmatically creating validators
  * [eed3c9a](http://github.com/symfony/symfony/commit/eed3c9a48c8c09af0321a3b191246ffd29cf1d55 "eed3c9a48c8c09af0321a3b191246ffd29cf1d55 commit on github"): \[Validator\] added abstract method Constraint::targets() to define whether constraints can be put onto properties, classes or both
  * [2d7c47e](http://github.com/symfony/symfony/commit/2d7c47e488fbeb9dbbfecc243b303b878efb7934 "2d7c47e488fbeb9dbbfecc243b303b878efb7934 commit on github"): \[Validator\] each object is now only validated once for a given group
  * [d327a90](http://github.com/symfony/symfony/commit/d327a90ff25a4d006f161d4f9616dfa7076a1819 "d327a90ff25a4d006f161d4f9616dfa7076a1819 commit on github"): \[Validator\] added namespace prefix support for XML and YAML loaders
  * [d928632](http://github.com/symfony/symfony/commit/d928632583bd109777d2b57a2b2d6896a27773de "d928632583bd109777d2b57a2b2d6896a27773de commit on github"): \[Form\] made RepeatedField sub-field names configurable
  * [1cbd0ca](http://github.com/symfony/symfony/commit/1cbd0caa8943ee7bfe8f7ba286f173ac94651287 "1cbd0caa8943ee7bfe8f7ba286f173ac94651287 commit on github"): \[DoctrineMongoDBBundle\] added unique constraint, validator and test, registered validator in DIC
  * [6d52645](http://github.com/symfony/symfony/commit/6d52645861118ad122c56158ba9445b332297d05 "6d52645861118ad122c56158ba9445b332297d05 commit on github"): \[DoctrineMongoDBBundle\] registered new validation namespace for annotations
  * [24ff22a](http://github.com/symfony/symfony/commit/24ff22af073ea8f6df74257c11c5916493526e96 "24ff22af073ea8f6df74257c11c5916493526e96 commit on github"): \[HttpFoundation\] added a directory fallback for when the class is not found in registered namespaces and class prefixes
  * [6d1e91a](http://github.com/symfony/symfony/commit/6d1e91a1faecb1f46a781d0e4ce37ed9d3fba3cc "6d1e91a1faecb1f46a781d0e4ce37ed9d3fba3cc commit on github"): refactored bundle management: 1) the registerBundleDirs() method has been removed, so you are now free to use any namespace for your bundles; 2) the bundle name is now always the short name of the bundle class; 3) a new getParent() method has been added to BundleInterface
  * [e6f1248](http://github.com/symfony/symfony/commit/e6f12481519181894073d5489ce37c1fe0b2956f "e6f12481519181894073d5489ce37c1fe0b2956f commit on github"): \[HttpKernel\] added back Bundle::getName() as it is quite useful
  * [e135c14](http://github.com/symfony/symfony/commit/e135c14538d807191331fba056d172c335e2ec12 "e135c14538d807191331fba056d172c335e2ec12 commit on github"): allow arbitrary ordering of config elements in symfony xml config
  * [0b0c15b](http://github.com/symfony/symfony/commit/0b0c15b7b6d534b13973e40debb304449c7d046e "0b0c15b7b6d534b13973e40debb304449c7d046e commit on github"): made XSD less strict when possible
  * [dd20434](http://github.com/symfony/symfony/commit/dd20434227278cae4c9b5b6e3bc5bbed066e6201 "dd20434227278cae4c9b5b6e3bc5bbed066e6201 commit on github"): fixed kernel:locateResource to loop across the bundle tree to find the first match
  * [507da2a](http://github.com/symfony/symfony/commit/507da2a1ab74a45ef8c443f70650fd0bd2549b0a "507da2a1ab74a45ef8c443f70650fd0bd2549b0a commit on github"): some performance tweaks (added lazy loading for firewall configurations and implemented re-using of RequestMatchers if all matching rules are the same)
  * [8649deb](http://github.com/symfony/symfony/commit/8649debb065b77698f52a78dcb07ffbb4151af11 "8649debb065b77698f52a78dcb07ffbb4151af11 commit on github"): \[Routing\] fixed imports from the current directory
  * [a5007fe](http://github.com/symfony/symfony/commit/a5007febdd7194409ecbcbe85cafd49c05620dc6 "a5007febdd7194409ecbcbe85cafd49c05620dc6 commit on github"), [5e9c9f4](http://github.com/symfony/symfony/commit/5e9c9f41745e5918d40ae0871e76df598bc9aa3e "5e9c9f41745e5918d40ae0871e76df598bc9aa3e commit on github"), [5ff0ded](http://github.com/symfony/symfony/commit/5ff0dedebbe8f5f47eb4a6ae0e4dbec526392b44 "5ff0dedebbe8f5f47eb4a6ae0e4dbec526392b44 commit on github"): \[FrameworkBundle\] renderer is once more the last of the templates
  * [8d19136](http://github.com/symfony/symfony/commit/8d19136a554b0e8eb6eaec1c60969336ab3bebaa "8d19136a554b0e8eb6eaec1c60969336ab3bebaa commit on github"): refactored extensions to call XXXLoad only once with all config sections
  * [bdc7ae8](http://github.com/symfony/symfony/commit/bdc7ae8c524ff26dd8fa9e4aec7a01caa79181fc "bdc7ae8c524ff26dd8fa9e4aec7a01caa79181fc commit on github"): show cookies in response headers
  * [acb19bc](http://github.com/symfony/symfony/commit/acb19bc43f556731fe23a93330da5aa83870170d "acb19bc43f556731fe23a93330da5aa83870170d commit on github"): \[FrameworkBundle\] added document_root option for File objects
  * [69f0ec3](http://github.com/symfony/symfony/commit/69f0ec3b1ad7eae01f3547fab92c235144a37923 "69f0ec3b1ad7eae01f3547fab92c235144a37923 commit on github"): added a method to normalize config entries coming from YAML and XML
  * [fedb4b4](http://github.com/symfony/symfony/commit/fedb4b4f0d2033806971a76ff138572b0345c8fc "fedb4b4f0d2033806971a76ff138572b0345c8fc commit on github"): \[TwigBundle\] started to refactor TwigExtension
  * [59a974e](http://github.com/symfony/symfony/commit/59a974e8f61f4cb038b244af6694ed9d5b66da79 "59a974e8f61f4cb038b244af6694ed9d5b66da79 commit on github"): added TemplateLocatorInterface
  * [1d5b6ed](http://github.com/symfony/symfony/commit/1d5b6ed908046d2765b585c05b7ab4697a8c2b3d "1d5b6ed908046d2765b585c05b7ab4697a8c2b3d commit on github"): added scope to the DI container
  * [c7e3b23](http://github.com/symfony/symfony/commit/c7e3b2381a5f2e4288fe9ead0fa237d5b9a6bd3a "c7e3b2381a5f2e4288fe9ead0fa237d5b9a6bd3a commit on github"): refactored Doctrine Bundle dbalLoad() to make use of config merging
  * [29888a4](http://github.com/symfony/symfony/commit/29888a4a1d91c704758667eda3ed558b06cfac14 "29888a4a1d91c704758667eda3ed558b06cfac14 commit on github"): \[DoctrineBundle\] use a Merge Config algorithm for the ORM bundle. Simplified configuration and got rid of unnecessary ways to configure the same thing in several different ways
  * [22f6307](http://github.com/symfony/symfony/commit/22f6307053f32b6bb61eb34092f79aa99d5d2892 "22f6307053f32b6bb61eb34092f79aa99d5d2892 commit on github"): \[DoctrineBundle\] changed and simplified dbalLoad() slightly. Made logging explicit with a configuration variable to avoid tons of unnecessary method calls in production environment
  * [a50f56a](http://github.com/symfony/symfony/commit/a50f56a7e94cf2590d7bfd26700ddc78dd310739 "a50f56a7e94cf2590d7bfd26700ddc78dd310739 commit on github"): \[DoctrineBundle\] reverted removal of dic parameter doctrine.orm.auto_generate_proxy_classes
  * [682e835](http://github.com/symfony/symfony/commit/682e83585be600ec731797373df2bb6bc6117639 "682e83585be600ec731797373df2bb6bc6117639 commit on github"): \[DoctrineBundle\] added new Command doctrine:mapping:info that allows to check what entities are mapped and if their metadata is specified correctly. Added exception when a mapping/bundle directory does not exist
  * [f73107c](http://github.com/symfony/symfony/commit/f73107cb9d19d2eeb0905032e371586b01912242 "f73107cb9d19d2eeb0905032e371586b01912242 commit on github"): \[FrameworkBundle\] updated XSD file for new csrf_protection configuration format
  * [0b05fe1](http://github.com/symfony/symfony/commit/0b05fe1b1fad0998b19fc1b64aa793cec020ef4b "0b05fe1b1fad0998b19fc1b64aa793cec020ef4b commit on github"): \[HttpKernel\] fixed HTTP headers when requesting a HEAD on a cached response
  * [86b357d](http://github.com/symfony/symfony/commit/86b357d70be8562da138c090214dab1da01d9605 "86b357d70be8562da138c090214dab1da01d9605 commit on github"): \[FrameworkBundle\] fixed ESI configuration
  * [b577ce6](http://github.com/symfony/symfony/commit/b577ce665a5456d893428e33698001c494fd9997 "b577ce665a5456d893428e33698001c494fd9997 commit on github"): \[HttpKernel\] fixed scope management in HttpKernel
  * [73ab687](http://github.com/symfony/symfony/commit/73ab6875217d3d137f6829cb26ddf1ee190eea2f "73ab6875217d3d137f6829cb26ddf1ee190eea2f commit on github"): moved ControllerResolver methods to HttpKernel
  * [e151580](http://github.com/symfony/symfony/commit/e15158021269842a8ff58967ad39f2d847f7c298 "e15158021269842a8ff58967ad39f2d847f7c298 commit on github"): \[HttpKernel\] removed getRequest as it is not part of the interface anymore
  * [005c1d9](http://github.com/symfony/symfony/commit/005c1d9df8630b87043db8729b38c1377183d39d "005c1d9df8630b87043db8729b38c1377183d39d commit on github"): \[Serializer\] added initial version of the Serializer component

Documentation
-------------

  * New <a href="http://trac.symfony-project.org/wiki/IRCLogs20110120">IRC Logs 2011-01-20</a> page

New [job postings](http://trac.symfony-project.com/trac/wiki/JobPostings)
----------------

  * Symfony + PHP Developer at [BARTON STUDIO s.r.o.](http://www.bartonstudio.cz) - full-time based in Pilsen, Czech Republic - Contact: info@bartonstudio.cz

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfTCPDFFPDI](http://www.symfony-project.org/plugins/sfTCPDFFPDIPlugin): allows you to easily create a pdf file. You can also import an existing pdf in the background.
  * [sfDoctrineActAsCommentable](http://www.symfony-project.org/plugins/sfDoctrineActAsCommentablePlugin): makes Doctrine objects commentable.
  * [sfSwiftMailerExtended](http://www.symfony-project.org/plugins/sfSwiftMailerExtendedPlugin): it is necesary that important emails always receive their destination. Symfony lacks a definition of different email transports. With sfSwiftMailerExtendedPlugin you are able to define different email transports.
  * [pxPropelEasyEmbeddedRelation](http://www.symfony-project.org/plugins/pxPropelEasyEmbeddedRelationPlugin): easily embed related forms and add new as well as edit and delete existing related records within one form (it's a port of ahDoctrineEasyEmbeddedRelationsPlugin for Propel).
  * [sfDoctrineCronManager](http://www.symfony-project.org/plugins/sfDoctrineCronManagerPlugin): allows users to administer cron jobs from a backend interface. Useful for users with limited admin access to the server. Jobs can be added, deleted, or run at any time for testing or other purposes.

Updated plugins
---------------

  * [ysfDimensions](http://www.symfony-project.org/plugins/ysfDimensionsPlugin):
    * fixed possible undefined index
    * added ability to specify custom cache handler
    * released 1.4.0 version

  * [sfProjectAnalyser](http://www.symfony-project.org/plugins/sfProjectAnalyserPlugin):
    * added a panel that shows all settings of the analysis

  * [sfGrid](http://www.symfony-project.org/plugins/sfGridPlugin):
    * added an option to confirm a user action
    * added an option to define when a widget can be renderable or not

  * [sfAlyssaJqGrid](http://www.symfony-project.org/plugins/sfAlyssaJqGridPlugin):
    * refactored render of link widget

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * fixed a bug with instantiating js classes for modules that start with a lower case letter
    * moved ColumnModel instantiation out of the grid prototype and into the constructor to properly resolve the ColumnModel instantiation bug
    * updated batch toolbar handler to work better when the grid is not the parent grid
    * made the getQuery method for in ExtjsPropel15Route public
    * started adding expander support for gridpanel layout
    * fixed a typo in batchHandler
    * fixed a data format bug in ux.TwinDateTimeField
    * fixed missing constructor partial in columnModel
    * fixed a bug where the primary key fieldname was different from the phpname

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * replaced Doctrine with Doctrine_Core to work with compiled doctrine version
    * replaced trim() by $.trim() to prevent IE7 error
    * replaced Doctrine with Doctrine_Core

  * [sfDoctrineGuard](http://www.symfony-project.org/plugins/sfDoctrineGuardPlugin):
    * fix to work with doctrine compiled version

  * [sfTemplating](http://www.symfony-project.org/plugins/sfTemplatingPlugin):
    * loader is now an optional parameter
    * added test setup as generated by sfTaskExtraPlugin

  * [apostropheFeedback](http://www.symfony-project.org/plugins/apostropheFeedbackPlugin):
    * there were some text phrases in here not wrapped in a_()

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * user, group and permissions filters now work reasonably well
    * the filters are now open by default if you have made any changes to the filter settings
    * the "username" filter has been relabeled "Name" and it allows you to match the user's full name or their username
    * fixed a call to getFilters() in an admin gen that had no filter form
    * apostrophe:migrate now fixes the ID size for a_media_item_to_category before trying to add constraints to it after the sizes of other IDs have already been updated
    * all slashes in tags are converted to dashes
    * added caching to SlideShare
    * successfully completed doctrine:clean task
    * removed cancel button from search services
    * autocomplete="off" for every field in the user admin form
    * default sorts for tags and categories
    * disabled PDF preview by default
    * made the videoEditSuccess save button the same as the editMultipleSuccess save button
    * fixed cropping aspect ratio for 'c' image and slideshow slots
    * fixed bug with slot cancel button not preventing the click from happening
    * added --verbose option to rebuild-search-index (it now runs quietly otherwise)
    * fixed admin generator theme was caching the CSRF between multiple admin users which means someone can't use batch actions at all
    * removed stale form class blocking i18n
    * commented out custom style default in fckconfig, need to be able to set custom styles
    * added SoundCloud integration
    * Google Analytics is supported out of the box in Apostrophe now
    * updated the cancel button to be a real anchor with a url to aMedia/resume
    * Add/Delete Pages
    * users with "Add/Delete Pages" can add pages without validation errors
    * resolved an issue with aClickOnce and the select link for Video

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * moved the JS for the blog slots to aBlog.js. Created a_js_calls
    * inserted deprecated messages into the single slots
    * light markup changes to the blog / events slots so that they work in wide columns and skinny columns
    * removed code for category class columns in blog importer
    * no more defaults for blog import: you have to specify --events=filename.xml and/or --posts=filename.xml
    * categories are correctly mirrored to the virtual page
    * tag import is now supported
    * some adjustments to disqus, added ability to enable developer mode in app.yml, added the comment count to the blog meta partial
    * fixed bug where if you don't click save on the title, it returns 'Untitled' even if you have entered a title


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [sociallynotable.com](http://sociallynotable.com/): \(English\) an Amazon.com affiliate website built with Symfony2 and Doctrine MongoDB ODM and lets you shop for products that are popular on Amazon.com ranked by what is being mentioned the most on Twitter!


They talked about us
--------------------

  * [Se publica Symfony2 PR5 (beta 1)](http://www.symfony.es/2011/01/17/se-publica-symfony2-pr5-beta-1/)
  * [Astuces de développement javascript avec symfony](http://www.lexik.fr/blog/symfony/symfony/astuces-de-developpement-javascript-avec-symfony-1382)
  * [Doctrine cache](http://xlab.pl/2011/01/doctrine-cache/)
  * [Symfony2 PR5](http://www.symfony.it/articoli/402/symfony2-pr5/)
  * [Présentation du plugin lxJavascriptPlugin](http://www.lexik.fr/blog/symfony/symfony/presentation-du-plugin-lxjavascriptplugin-1408)
  * [symony2 project from scratch](http://www.fizyk.net.pl/blog/symony2-project-from-scratch)
  * [Apostrophe 1.5, ¿el mejor CMS para Symfony?](http://www.symfony.es/2011/01/19/apostrophe-1-5-%C2%BFel-mejor-cms-para-symfony/)
  * [Symfony command line Farben unter Snow Leopard](http://nerdpress.org/2011/01/19/symfony-command-line-farben-unter-snow-leopard/)
  * [Note à moi même – Apprendre a configurer les sf_culture !!](http://blog.lombardot.fr/2011/01/19/note-a-moi-meme-apprendre-a-configurer-les-sf_culture/)
  * [Get Ready For Propel 1.6: The Beta 1 Is Released](http://propel.posterous.com/get-ready-for-propel-16-the-beta-1-is-release)
  * [Propel 1.6 publica su primera beta](http://www.symfony.es/2011/01/20/propel-1-6-publica-su-primera-beta/)
  * [Extending your Doctrine Model: Template Classes](http://www.jnieto.org/article/extending_your_doctrine_model_template_classes)
  * [La version 2.0 de Symfony annoncée pour mars, testez et commentez la beta](http://www.developpez.com/actu/27479/La-version-2-0-de-Symfony-annoncee-pour-mars-testez-et-commentez-la-beta/)
  * [Using of sfWidgetFormInputSWFUploadPlugin](http://www.symfonylab.com/using-of-sfwidgetforminputswfuploadplugin/)
  * [Refactoring queries with Doctrine](http://www.jnieto.org/article/refactoring_queries_with_doctrine)
  * [「第2回 Symfony2 勉強会」行ってきました。](http://yanchi52.blog21.fc2.com/blog-entry-34.html)
  * [Helpers full study](http://abdelmohsen.blogspot.com/2011/01/helpers-full-study.html)
  * [22 PHP Frameworks για ταχύτερη ανάπτυξη](http://www.web-resources.eu/archives/22-php-frameworks-to-shorten-your-development-time)
  * [Terceras Jornadas Nacionales del Informático](http://wi7max.wordpress.com/2011/01/22/terceras-jornadas-nacionales-del-informtico/)
  * [Хранение файлов в базе Postgres в бинарном виде](http://of.com.ua/symfony/hranenie-failov-v-baze-postgres-v-binarnom-vide/)
  * [Continous Integration with Hudson, GIT and Symfony](http://www.zipfelmaus.com/blog/continous-integration-with-hudson-git-and-symfony/)
  * [Datum- und Zeitfelder formatieren mit Doctrine 1.4](http://www.symfony-blog.de/symfony-1-4/datum-und-zeitfelder-formatieren-mit-doctrine-1-4/)
  * [symfony的sfValidatorCallback的正确写法](http://www.phpant.com/symfony_sfvalidatorcallback.html)
  * [第2回 Symfony2勉強会の復習 後半](http://blog.stripejam.jp/archives/397)
  * [A front-end developer journey into symfony...](http://www.position-absolute.com/news/a-front-end-developer-journey-into-symfony/)
  * [Symfony – I18n in Action](http://www.sebastian-heinisch.de/symfony-i18n-in-action/2011-01-18/)
  * [十大最流行最常用的PHP开发框架](http://www.sailfish.me/282.html)
  * [さくらインターネットでsymfony1.4(.8) - プロジェクトの作成](http://michelle-gf.blogspot.com/2011/01/symfony148_18.html)
  * [Symfony1.4 11日目その5](http://yuubiseiharukana.blog.shinobi.jp/Entry/448/)
