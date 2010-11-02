A week of symfony #198 (11->17 October 2010)
============================================

This week, symfony project unveiled all the details for the upcoming <a href="http://www.symfony-live.com/">Symfony Live 2011</a> conferences in Paris and San Francisco. Meanwhile, Symfony2 development showed an impressive activity boosted by lots of patches committed by the community. Lastly, as a proof that time flies when you're having fun programming, the next week symfony turns 5 years old (on October 18).
 
Development mailing list
------------------------

  * [Polymorphic Route in Sf2?](http://groups.google.com/group/symfony-devs/browse_thread/thread/74bdcfdad018cd10)
  * [Symfony2 - Validator framework and external constraints dependencies](http://groups.google.com/group/symfony-devs/browse_thread/thread/944d9d42f7de4ba9)
  * [Where to switch to a theme](http://groups.google.com/group/symfony-devs/browse_thread/thread/f7894031a34aa966)
  * [RFC - hardcoded route classes](http://groups.google.com/group/symfony-devs/browse_thread/thread/dd4049cffdf81207)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [af8cb48](http://github.com/symfony/symfony/commit/af8cb480a3e9f77a8788ea1b80b2bba4399c337f "af8cb480a3e9f77a8788ea1b80b2bba4399c337f commit on github"): \[FrameworkBundle\] changed Template renderers to be lazy-loaded
  * [dbde494](http://github.com/symfony/symfony/commit/dbde494424d89f50b8614f2e50040dcd21c17f7a "dbde494424d89f50b8614f2e50040dcd21c17f7a commit on github"): made locale determination for translation lazy-loaded (this allows to have a stateless-website, without any cookie)
  * [f033fc5](http://github.com/symfony/symfony/commit/f033fc5578b0a2953fe5e95bac6c99766c28625e "f033fc5578b0a2953fe5e95bac6c99766c28625e commit on github"): refactor ValueTransformers to recieve the original value when reverseTransform() is called
  * [0d9d4ac](http://github.com/symfony/symfony/commit/0d9d4ac583ad73859880973d3ffcc8f90866cbf3 "0d9d4ac583ad73859880973d3ffcc8f90866cbf3 commit on github"): Optimize some code in Form/Configurable, Have ChoiceField always pass data to transformers, implemented and fully unit-tested two Doctrine ORM specific transformers that do Collection to String/Choice Transformations
  * [ec3b3f7](http://github.com/symfony/symfony/commit/ec3b3f7637c94be6e9be4c8061b35f9e10129a6d "ec3b3f7637c94be6e9be4c8061b35f9e10129a6d commit on github"): added and tested EntityToIDTransformer to transform Many-To-One and One-To-One entities into their identifier values
  * [db3476a](http://github.com/symfony/symfony/commit/db3476aeaa74a6b888e60381929dda8a92c7491a "db3476aeaa74a6b888e60381929dda8a92c7491a commit on github"): \[WebProfilerBundle\] simplified DIC extension
  * [bf1eb56](http://github.com/symfony/symfony/commit/bf1eb56a34cf8aa809150f28c5dfc2ca04593c73 "bf1eb56a34cf8aa809150f28c5dfc2ca04593c73 commit on github"): \[EventDispatched\] event doesn't need to implement ArrayAccess
  * [d8f4cb7](http://github.com/symfony/symfony/commit/d8f4cb79c92f631d3de2bcc719a8a38245c42c14 "d8f4cb79c92f631d3de2bcc719a8a38245c42c14 commit on github"): \[Form\] turned FieldGroup::getFields() into 4 specialized methods for more flexibility
  * [fafcd02](http://github.com/symfony/symfony/commit/fafcd02684ef4029beb40b11ca72dabe2eabff2f "fafcd02684ef4029beb40b11ca72dabe2eabff2f commit on github"): \[HttpFoundation\] changed RequestMatcher pattern syntax
  * [7ad510d](http://github.com/symfony/symfony/commit/7ad510d6ef66ba7471d8d4e7fee003752c0618f9 "7ad510d6ef66ba7471d8d4e7fee003752c0618f9 commit on github"): added --symlink option to assets:install command
  * [aa1cb87](http://github.com/symfony/symfony/commit/aa1cb87f603ef87f5b5c0506ffa92e0387debf39 "aa1cb87f603ef87f5b5c0506ffa92e0387debf39 commit on github"): \[FrameworkBundle\] clarified exception message in InitBundleCommand.php
  * [ade5fd6](http://github.com/symfony/symfony/commit/ade5fd6574d8c17537a058d055d78489505e6992 "ade5fd6574d8c17537a058d055d78489505e6992 commit on github"): fixed the bug of request_panel.php in WebProfiler
  * [f667b69](http://github.com/symfony/symfony/commit/f667b6928fa481745ca4c942b79b66a7b394a5ad "f667b6928fa481745ca4c942b79b66a7b394a5ad commit on github"): \[TwigBundle\] added a template block to render CollectionField fields
  * [1fab031](http://github.com/symfony/symfony/commit/1fab031d4d91719d49d42e6edcdc8d6da4f10339 "1fab031d4d91719d49d42e6edcdc8d6da4f10339 commit on github"): added missing EntityToIDTransformer files
  * [e1be4e9](http://github.com/symfony/symfony/commit/e1be4e96899bfb03193c83b0c979c45e462e0436 "e1be4e96899bfb03193c83b0c979c45e462e0436 commit on github"): \[Form\] refactored logic to read and set values from Field to PropertyPath
  * [a66d883](http://github.com/symfony/symfony/commit/a66d883afd1cf69f5879734e7b6d7a2b75ebbfcd "a66d883afd1cf69f5879734e7b6d7a2b75ebbfcd commit on github"): \[Form\] removed CSRF setters because they have no effect once CSRF protection is enabled. Re-enable CSRF protection with the desired values instead
  * [2a9ddee](http://github.com/symfony/symfony/commit/2a9ddee162e184efc862b557673b17640d2fa83a "2a9ddee162e184efc862b557673b17640d2fa83a commit on github"): \[HttpFoundation\] added Session::invalidate()
  * [30cf086](http://github.com/symfony/symfony/commit/30cf0868281fa2e34ce347ea0fb1201842bf1d6e "30cf0868281fa2e34ce347ea0fb1201842bf1d6e commit on github"): overrides the default {% include %} token parser since it loads through the right template renderer
  * [d376596](http://github.com/symfony/symfony/commit/d376596f7e490257db04ce307c60f1ef33767672 "d376596f7e490257db04ce307c60f1ef33767672 commit on github"): \[EventDispatcher\] fixed bug in EventDispatcher::disconnect if the second argument is null or ommitted
  * [df9ef79](http://github.com/symfony/symfony/commit/df9ef799536a68c23367e11ebdd6e13947b57bb5 "df9ef799536a68c23367e11ebdd6e13947b57bb5 commit on github"): \[Form\] readPropertyPath should return null instead of empty array
  * [7e66933](http://github.com/symfony/symfony/commit/7e669338761f1b856efa0ecd01a91cc1e1180996 "7e669338761f1b856efa0ecd01a91cc1e1180996 commit on github"): fixed inconsistency when calling the Http Kernel instance from an event

New [job postings](http://trac.symfony-project.com/trac/wiki/JobPostings)
----------------

  * Symfony developer at [Tigre Blanc](http://www.tigreblanc.fr) - full-time based in Douai, France - Contact: yoann@tigreblanc.fr

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [themeBlueprint](http://www.symfony-project.org/plugins/themeBlueprintPlugin): Blueprint CSS Grid Framework theme under symfony sfThemePlugin, is based on Blueprint CSS Grid Framework.
  * [sfDoctrineNestedSetEasyManager](http://www.symfony-project.org/plugins/sfDoctrineNestedSetEasyManagerPlugin): Plugin to manage nested set models using Doctrine. Inspired by sfDoctrineNestedSetManagerPlugin.
  * [euzeoCDN](http://www.symfony-project.org/plugins/euzeoCDNPlugin): this plugin adds a helper for parallel content delivery.
  * [sfHostAwareRouting](http://www.symfony-project.org/plugins/sfHostAwareRoutingPlugin): add subdomains to your routing rules.
  * [tmcContact](http://www.symfony-project.org/plugins/tmcContactPlugin): plugin to send e-mail after submitting a contact form.
  * [tmcI18n](http://www.symfony-project.org/plugins/tmcI18nPlugin): replaces the XLIFF files with a MySQL backend. Depends on doctrine.
  * [sfHttpHeaderCache](http://www.symfony-project.org/plugins/sfHttpHeaderCachePlugin): provides a means to facilitate caching by reverse proxies like nginx or Varnish, using cache.yml for configuration, as well as using an alternative cache (like sfApcCache or sfMemcacheCache) for partials.
  * [xwsWidgets](http://www.symfony-project.org/plugins/xwsWidgetsPlugin): adds some jQuery UI powered widgets.
  * [sfAltCaptcha](http://www.symfony-project.org/plugins/sfAltCaptchaPlugin): easily protects your forms with different kind of captchas (random code, math captcha).

Updated plugins
---------------

  * [sfDatagrid](http://www.symfony-project.org/plugins/sfDatagridPlugin):
    * added order_by_for_filters option for propel admin generator
    * added lcfirst definition for no php5.3 and Jquery
    * updated formatter propel for non automatic phpName FK tables
    * fixed XHTML formatter
    * include is model generator for more options
    * added modal thickbox formatter
    * prepare a new show action for generator

  * [sfSocial](http://www.symfony-project.org/plugins/sfSocialPlugin):
    * moved Propel classes to plugin classes
    * fixed javascript bug in message
    * improved Doctrine schema and classes
    * improved Propel schema
    * added some translations
    * fixed regression after Doctrine schema change

  * [sfAssetsLibrary](http://www.symfony-project.org/plugins/sfAssetsLibraryPlugin):
    * avoid of use sfContext inside helper
    * rewriting helper to Symfony Conventions
    * resigning from not needed rewrite rule

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * fixed generated route problem
    * removed catchall route
    * fixed bug with form validator options generation
    * fixed bug with routing for export action link
    * added checkcolumn plugin by default for boolean fields
    * fixed a problem with combo validators when using combo for local columns
    * fixed routing problem for formpanel combos
    * fixed a bug with list.sort configuration

  * [sfTrafficCMS](http://www.symfony-project.org/plugins/sfTrafficCMSPlugin):
    * check for existance of hasAccess method on sfGuardUser before calling it
    * added auto-hiding of deleted_at

  * [sfDoctrineRestGenerator](http://www.symfony-project.org/plugins/sfDoctrineRestGeneratorPlugin):
    * fixed bug on many to many relations loading
    * fixed a bug in n-n relation display

  * [ddOnlineStore](http://www.symfony-project.org/plugins/ddOnlineStorePlugin):
    * created a gallery for the product images using Sortable and JCroppeable behaviors
    * created the ddOnlineStoreProduct module
    * added the capacity field in product

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * updated the getPopulars method to take a limit parameter so I can easily ask for less tags where appropriate
    * fixed wrong encoding when charset of site is not UTF-8
    * changed 'tagsLabel' to 'tags-label'
    * added a preference for an allTags array if it is present (over the ajax typeahead)
    * provided some default error-checking for empty arrays
    * eliminated the need to provide an array of existing tags
    * added the commit-event option

  * [sfErrorNotifier](http://www.symfony-project.org/plugins/sfErrorNotifierPlugin):
    * added a new report404 option to specifically target 404 errors
    * fixed a bug when page_not_found event was fired a PHP error was fired

  * [sfDoctrineGuard](http://www.symfony-project.org/plugins/sfDoctrineGuardPlugin):
    * documented migration procedure from 4.0.0 to 5.0.0

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * show context where re-implemented accepting a layout and the possibility of using partials
    * added support for actions above the form and above the list. The paginator also can be put before the list
    * updated show context templates
    * added support for canNew conditions
    * updated readme

  * [sfExtjs3](http://www.symfony-project.org/plugins/sfExtjs3Plugin):
    * switched external definition to Extjs 3.3.0 tag

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * timepicker2() is now part of timepicker.js. The widget has been updated to call the timepicker2 function with some good default options
    * all IDs and foreign key IDs use Doctrine's default integer size now
    * fixed a bug with disqus comments
    * fixed bug that required two saves before title of a blog post or event was saved

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * started debugging media in ie7
    * enabled the 'Add' functionality for multiple select for media
    * apostrophe:import-files is alive again
    * limited Popular Tags to 10
    * fixed a bug with the Multiple Select markup for a-btns
    * styled the media edit for some more
    * no more hardcoded 4-byte integer IDs for tables
    * apostrophe:migrate now converts your existing database from 4-byte IDs to Doctrine's new 8-byte IDs for compatibility with sfDoctrineGuardPlugin
    * apostrophe:migrate also stubs in unique (although not usable) email addresses
    * addressed case changes in relation names
    * added first name and last name to users list view
    * added email address, first name, last name to users edit form
    * removed space-wasting 'updated_at' field from list views
    * changed language for saving selections so that it doesn't always say slideshow
    * styled the create page form so simplify the process
    * made the radioToggleButton into an a.js function
    * updated search success to display the number of results
    * slideshow slot and new smart slideshow slot have been disentangled
    * you can now template out the global buttons in the admin bar. The new aTools::getGlobalButtonsByName() method makes it easy to fetch the possibilities in a ready-to-go form
    * added tag admin to standard list of buttons

New [symfony bloggers](http://trac.symfony-project.com/trac/wiki/SymfonyBloggers)
--------------------

  * [Tobias Sjösten](http://vvv.tobiassjosten.net/) \([feed](http://vvv.tobiassjosten.net/symfony.atom)\) \(English\)
  * [Lyra CMS Blog](http://lyra-cms.com/blog) \([feed](http://feeds.feedburner.com/lyracms-blog)\) \(English\)

They talked about us
--------------------

  * [symfony day 2010 – a review](http://test.ical.ly/2010/10/11/symfony-day-2010%E2%80%93a-review/)
  * [Presentaciones del Symfony Day 2010](http://www.symfony.es/2010/10/11/presentaciones-del-symfony-day-2010/)
  * [Twitter and Emails are good; Postcards are better](http://fabien.potencier.org/article/46/twitter-and-emails-are-good-postcards-are-better)
  * [Conditional presentation of symfony forms](http://test.ical.ly/2010/10/12/conditional-presentation-of-symfony-forms/)
  * [Tracking Google Analytics events with Symfony](http://vvv.tobiassjosten.net/symfony/tracking-google-analytics-events-with-symfony)
  * [Symfony CLI helper script](http://vvv.tobiassjosten.net/symfony/symfony-cli-helper-script)
  * [A word about Doctrine Record Behaviours](http://test.ical.ly/2010/10/13/a-word-about-doctrine-record-behaviours/)
  * [symfony Day 2010: PHP-Entwicklerkonferenz übertrifft Erwartungen](http://www.presseanzeiger.de/meldungen/it-computer-internet/399436.php)
  * [Ofertas de trabajo Symfony en España](http://www.symfony.es/2010/10/13/ofertas-de-trabajo-symfony-en-espana/)
  * [iPhone style checkboxes for Symfony](http://shout.setfive.com/2010/10/13/iphone-style-checkboxes-for-symfony/)
  * [So you want a clean and easy way to manage dynamic doctrine relations in your symfony forms?](http://test.ical.ly/2010/10/14/so-you-want-a-clean-and-easy-way-to-manage-dynamic-doctrine-relations-in-your-symfony-forms/)
  * [Creating console commands with Symfony2](http://blog.servergrove.com/2010/10/14/creating-console-commands-with-symfony2/)
  * [International PHP Conference 2010](http://www.leftontheweb.com/message/International_PHP_Conference_2010)
  * [A simple way to debug your embedded symfony forms](http://test.ical.ly/2010/10/15/a-simple-way-to-debug-your-embedded-symfony-forms/)
  * [Symfony Day](http://blog.liip.ch/archive/2010/10/15/symfony-day.html)
  * [Conferencias Symfony Live 2011 en París y San Francisco](http://www.symfony.es/2010/10/16/conferencias-symfony-live-2011-en-paris-y-san-francisco/)
  * [Symfony genUrl method](http://www.jnieto.org/article/symfony_genurl_method)
  * [New symfony plugin, sfAltCaptchaPlugin](http://www.lyra-cms.com/blog/2010/10/new-symfony-plugin-sfaltcaptchaplugin.html)
  * [Symfony: Symfony Day 2010 в Кёльне](http://www.charnad.com/blog/symfony-day-2010-in-cologne/)
  * [sfDoctrineGuardPlugin: Ajout de permissions et de groupes après un register](http://www.funstaff.ch/2010/10/12/sfdoctrineguardplugin-ajout-de-permissions-et-de-groupes-apres-un-register)
