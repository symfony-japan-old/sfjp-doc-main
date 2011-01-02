A week of symfony #209 (27 December 2010 -> 2 January 2011)
===========================================================

This week marks the start of what could be the most important year of the symfony project history. For starters, in less than three months' time, Symfony2 will be published and two [official symfony conferences](http://www.symfony-live.com/) will be held at Paris and San Francisco. Therefore, symfony project wishes a very happy new year to all its supporters and developers.

Development mailing list
------------------------

  * [Symfony2 Core third party dependencies](https://groups.google.com/forum/#!topic/symfony-devs/x56tv1fOssQ)
  * [Sandbox and some Guides' improvements request](https://groups.google.com/forum/#!topic/symfony-devs/nKXPNmVwwg4)
  * [config.yml and config_dev.yml inheritance: duplicate DI Extension calls](https://groups.google.com/forum/#!topic/symfony-devs/V3mR28IWw4c)
  * [Changes to Doctrine ORM and MongoDB Bundles: Explicit Mapping necessary!](https://groups.google.com/forum/#!topic/symfony-devs/1diLYnE86OY)
  * [[Symfony2] Establishing bundle dependencies?](https://groups.google.com/forum/#!topic/symfony-devs/0mahjntCGoY)
  * [Abstract Bundles?](https://groups.google.com/forum/#!topic/symfony-devs/qe0y7FwmBLM)
  * [[Symfony2] Implementing a service controller](https://groups.google.com/forum/#!topic/symfony-devs/mdB62W3diak)

Symfony2 development highlights
-------------------------------

The [official Symfony2 repository](https://github.com/symfony/symfony) didn't receive this week any commit. Anyway, the [repository forked by Fabien Potencier](https://github.com/fabpot/symfony/) got a ton of commits.

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [SinaT](http://www.symfony-project.org/plugins/SinaTPlugin): publish Sina microblogs.
  * [sfDoctrineTableGetter](http://www.symfony-project.org/plugins/sfDoctrineTableGetterPlugin): allows you to have code completion for doctrine tables in your favorite IDE.

Updated plugins
---------------

  * [pmSuperfishMenu](http://www.symfony-project.org/plugins/pmSuperfishMenuPlugin):
    * fixed generated code to assure code is W3C valid (add type attribute to script tag and wrap content into CDATA tag)

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * improvents in _form, _form_tabbed and _form_folded templates
    * _form_tabbed, _filters and _form_folded templates refactored
    * improved stylesheets, specially for filters, folded and tabbed layouts
    * updated README
    * added a form formatter that adds the 'required' class to required widgets' label

  * [pmPDFKit](http://www.symfony-project.org/plugins/pmPDFKitPlugin):
    * updated a bunch of broken stuff

  * [pmJSCookMenu](http://www.symfony-project.org/plugins/pmJSCookMenuPlugin):
    * heavily updated documentation

  * [dcStatefulSecurity](http://www.symfony-project.org/plugins/dcStatefulSecurityPlugin):
    * better plugin organization
    * updated README and LICENSE files

  * [pmPropelWorkflowableBehavior](http://www.symfony-project.org/plugins/pmPropelWorkflowableBehaviorPlugin):
    * better plugin organization
    * removed the config directory

  * [sfAlyssaJqGrid](http://www.symfony-project.org/plugins/sfAlyssaJqGridPlugin):
    * fixed wrong page and record information

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * forced the correct character set when parsing Zend search expressions
    * the aMysql class is a lightweight wrapper for PDO (aMySql is not an ORM, it just makes working with raw SQL a lot more pleasant)
    * the a_remove_filter_button helper outputs a link that removes one or more parameters from a URL when clicked
    * search engine tags are indexed in a sensible and simple way for the benefit of plaintext searches
    * added the constraintExists method to aMigrate
    * cancel the media selection if the user browses away from the media repository by following a link
    * we now have clear error messages when the maximum post size or maximum upload size is exceeded
    * a blog posts slot with a post in the jobs category will now link to the jobs-specific engine page
    * aSecurityUser is now more convenient to override (added BaseaSecurityUser class)
    * aSecurityUser clears the apostrophe_media namespace
    * users are now restricted to assigning media to categories they have been given access to, just like blog posts and events
    * implemented double click protection for completing a slideshow or cancelling a slideshow does not produce a 404
    * worked around video search doesn't crash the browser when you search for something popular on YouTube anymore
    * no more race conditions when two people edit the same area
    * implemented: if an admin adds a category you don't have control over to your media item, blog post or event, you are not able to remove that category from the item
    * removed support for the unsustainable app_a_routes_register, which was incompatible by design with plugins like the blog plugin, and updated the wiki documentation
    * updated sample fixtures files
    * email obfuscation now uses a_js_call and is caching-friendly because random GUIDs are not involved

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * you can now combine browsing by date, tag, category and plaintext search
    * need an inner join for both the a_blog_item_to_category table and the a_category table to prevent posts with no categories from being returned when a page is restricted by category
    * forgot to pass the url parameter to the sidebar in the show actions
    * fixed "New Event" was crashing, and both posts and events were creating an extra virtual page
    * browsing events by month was showing events that have already ended by that month
    * sdded in some code to show categories for posts and events




They talked about us
--------------------

  * [Le novità di Doctrine 2, un ORM per PHP](http://programmazione.it/index.php?entity=eitem&idItem=46114)
  * [Symfony2/ESI : le code](http://sebastien.porati.me/blog/2010/12/symfony2esi-le-code/)
  * [Talking at Confoo 2010, Montreal, Canada](http://www.hugohamon.com/en/blog/talking-at-confoo-2011-montreal-canada)
  * [Se publica la primera versión estable de Doctrine 2.0](http://www.symfony.es/2010/12/28/se-publica-la-primera-version-estable-de-doctrine-2-0/)
  * [sfDoctrineGuardPlugin et l'authentification externe](http://tcuvelier.developpez.com/php/symfony/sfdoctrineguardplugin/authentification-externe/)
  * [Symfony 1.4 and SSL - playing with symfony filters](http://blog.adryjanek.eu/2010/12/30/symfony-14-and-ssl-playing-with-symfony-filters/)
  * [Symfony 2.0 : PHP comme vous ne l’avez jamais vu!](http://www.programmez.com/magazine_articles.php?titre=Symfony-20--PHP-comme-vous-ne-l%E2%80%99avez-jamais-vu-!&id_article=1490&magazine=137)
  * [symfony sfAdminDashPlugin icons](http://symfony-world.blogspot.com/2010/12/symfony-sfadmindashplugin-icons.html)
  * [Modificando el double list del sfFormExtraPlugin de Symfony](http://blog.micayael.com/2010/12/31/modificando-el-double-list-del-sfformextraplugin-de-symfony/)
  * [Symfony: własne formattery formularzy](http://lukasz.klis.pl/blog/symfony-wlasne-formattery-formularzy/)
  * [Windows下安装Symfony实践](http://www.cotrun.net/blog/577.html)
  * [Bonnes pratiques de développement PHP/symfony](http://www.sylvaindeloux.com/blog/geek/bonnes-pratiques-developpement-php-symfony)
  * [Symfony not sortable in CRUD](http://www.scottyob.com/2011/01/01/symfony-not-sortable-generate-admin-crud/)
  * [Evitando la generación de los forms y filters en Doctrine](http://www.loalf.com/2010/12/evitando-la-generacion-de-los-forms-y-filters-en-doctrine/)
  * [【PHP+symfonyでMVC】 Part6：テーブル認証 仕切りなおし](http://ameblo.jp/kurt560222/entry-10753698167.html)
  * [Symfony, wordpress o php desde 0](http://asiermarques.com/2010/12/29/symfony-wordpress-o-php-desde-0/)
  * [Grails vs Symfony Performance](http://www.makingitscale.com/2010/grails-vs-symfony-performance.html)
  * [symfony 1.4.4でjson出力をアクション固定で行う](http://d.hatena.ne.jp/d4-1977/20101228/1293527454)
  * [Symfony – Passer votre site en mode maintenance](http://blog.netha.fr/2010/12/symfony-passer-votre-site-en-mode-maintenance/)
  * [Data importer for Symfony 2](http://symfony2bundles.org/lapistano/SF2-FeedImportBundle)
