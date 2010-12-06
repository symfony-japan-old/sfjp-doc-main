A week of symfony #203 (15->21 November 2010)
=============================================

Symfony2 development activity got a big boost this week. Firstly, Bernhard Schussek announced that he will be again in charge of the form and validation components, which will be finished by the end of the year. Secondly, Fabien initiated two interesting discussions in the developers mailing list: <a href="http://groups.google.com/group/symfony-devs/browse_thread/thread/925d40f1cff7fe11">removing the output escaper component</a> and <a href="http://groups.google.com/group/symfony-devs/browse_thread/thread/5f09925263e9d86e">using templates for routing patterns</a>. Lastly, the <a href="http://trac.symfony-project.org/wiki/IRCLogs20101118">weekly IRC meeting</a> generated some exciting discussions, ideas, best practices and updates about Symfony2 development status.
 
Development mailing list
------------------------

  * [Chunked Responses in Symfony2](http://groups.google.com/group/symfony-devs/browse_thread/thread/47a44c763f510678)
  * [RFC - Using "URI template" for routing patterns](http://groups.google.com/group/symfony-devs/browse_thread/thread/5f09925263e9d86e)
  * [RFC - Removing the Output Escaper Component](http://groups.google.com/group/symfony-devs/browse_thread/thread/925d40f1cff7fe11)
  * [Of XML & Yaml configs](http://groups.google.com/group/symfony-devs/browse_thread/thread/e64d3eac79bb8e9a)
  * [moving redirect() to the view](http://groups.google.com/group/symfony-devs/browse_thread/thread/6a26b1f306da1d1a)

symfony 1 development highlights
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=21%2F11%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r31398](http://trac.symfony-project.org/changeset/31398 "31398 revision on trac"): \[1.3, 1.4\] fixed typo in sfRoute class
  * [r31399](http://trac.symfony-project.org/changeset/31399 "31399 revision on trac"), [r31400](http://trac.symfony-project.org/changeset/31400 "31400 revision on trac"): \[1.3, 1.4\] fixed sfViewCacheManager returns incorrect cached http_protocol

sfPropelPlugin:

  * [r31401](http://trac.symfony-project.org/changeset/31401 "31401 revision on trac"): \[1.3, 1.4\] updated translation for es

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [8b9e979](http://github.com/symfony/symfony/commit/8b9e97911848cef50636aeab89a100034a2f4921 "8b9e97911848cef50636aeab89a100034a2f4921 commit on github"): \[FrameworkBundle\] changed configuration to always include the session service
  * [f6ddeeb](http://github.com/symfony/symfony/commit/f6ddeeb36b39e02221abd9357908a0caecfa7119 "f6ddeeb36b39e02221abd9357908a0caecfa7119 commit on github"): \[HttpFoundation\] added Response::setPublic() and changed setPrivate() to not take any argument
  * [942104a](http://github.com/symfony/symfony/commit/942104a5ff1a91178a4f868bd7e96be872b5b07c "942104a5ff1a91178a4f868bd7e96be872b5b07c commit on github"), [7257571](http://github.com/symfony/symfony/commit/7257571be4017c7356c25fe1aec19c4b2eff4750 "7257571be4017c7356c25fe1aec19c4b2eff4750 commit on github"): \[HttpFoundation\] added a setCache() method to ease setting the HTTP cache headers in one simple call
  * [4aa5ef6](http://github.com/symfony/symfony/commit/4aa5ef63f5122330024d1c2801cb3703dbcdf19e "4aa5ef63f5122330024d1c2801cb3703dbcdf19e commit on github"), [6f898a5](http://github.com/symfony/symfony/commit/6f898a5008361294a751d2407ca3c2fc7bcdf68c "6f898a5008361294a751d2407ca3c2fc7bcdf68c commit on github"): \[HttpKernel\] made some tests more robust
  * [35148c5](http://github.com/symfony/symfony/commit/35148c5ac3d497df759c9aa4d600d37a828f8252 "35148c5ac3d497df759c9aa4d600d37a828f8252 commit on github"): \[FrameworkBundle\] added routing internationalization
  * [3813eec](http://github.com/symfony/symfony/commit/3813eecf173b62b2591bc96a38d68a914d6d55ec "3813eecf173b62b2591bc96a38d68a914d6d55ec commit on github"), [519cc09](http://github.com/symfony/symfony/commit/519cc094884e8aefcbab66ef14d47b9c6cf1e60c "519cc094884e8aefcbab66ef14d47b9c6cf1e60c commit on github"): \[Translation\] added YamlFileLoader
  * [9ab33e4](http://github.com/symfony/symfony/commit/9ab33e4ae4463f51e8bf26f9415531647448bb9b "9ab33e4ae4463f51e8bf26f9415531647448bb9b commit on github"): \[DoctrineMongoDBBundle\] added registration of event listeners and subscribers via service container tags
  * [da18873](http://github.com/symfony/symfony/commit/da188734d884843e68b68b0feff65b07150285f3 "da188734d884843e68b68b0feff65b07150285f3 commit on github"): \[DoctrineMongoDBBundle\] added support for multiple event managers to the DIC extension
  * [b932441](http://github.com/symfony/symfony/commit/b932441ac9270a664e20a3ca8cf4888234ea2b05 "b932441ac9270a664e20a3ca8cf4888234ea2b05 commit on github"): \[DoctrineMongoDBBundle\] added ability to register global listeners and subscribers via the DIC
  * [58a240b](http://github.com/symfony/symfony/commit/58a240baba084a862648acdbcb1be060a4ca7cd5 "58a240baba084a862648acdbcb1be060a4ca7cd5 commit on github"): \[HttpFoundation\] allowed the SERVER_PORT key of the server ParameterBag in Request to be a string value without confusing Request::getHttpHost()
  * [92f3d9e](http://github.com/symfony/symfony/commit/92f3d9e7ec0e56445b968977d17ba25d3f62a62c "92f3d9e7ec0e56445b968977d17ba25d3f62a62c commit on github"): \[DependencyInjection\] removed the leading _ for anonymous service ids (the usage of strtr() in the conversion between ids and methods does not take leading _ into account like camelize() does)
  * [53dd4e3](http://github.com/symfony/symfony/commit/53dd4e39c734934f9a3d66cd2fc62ab617243659 "53dd4e39c734934f9a3d66cd2fc62ab617243659 commit on github"): \[DependencyInjection\] changed the YAML notation for optional services from @@ to @?
  * [f6cc63c](http://github.com/symfony/symfony/commit/f6cc63c99c88de6cb2916e5a5d35be810b5d6306 "f6cc63c99c88de6cb2916e5a5d35be810b5d6306 commit on github"): removed ArrayAccess interface for Container and Controller
  * [d45954a](http://github.com/symfony/symfony/commit/d45954af07802bed51296d29b58d8e21f79760b6 "d45954af07802bed51296d29b58d8e21f79760b6 commit on github"): \[Form, TwigBundle\] made sure all field types are rendered with the proper template
  * [4e5c99d](http://github.com/symfony/symfony/commit/4e5c99dab049d73bd5cbed1c00f312ca63ccf5ce "4e5c99dab049d73bd5cbed1c00f312ca63ccf5ce commit on github"): \[EventDispatcher\] removed the possibility to remove one listener for an event
  * [3cbc99c](http://github.com/symfony/symfony/commit/3cbc99c180d8a1604ddef43fd5602677121de3de "3cbc99c180d8a1604ddef43fd5602677121de3de commit on github"): \[Translation\] added flatten method on ArrayLoader. This allows the translations to be deeply nested arrays that will be flattened, allowing for namespacing of translations easily
  * [5aeb358](http://github.com/symfony/symfony/commit/5aeb3587211517b95e1a05478fe8886008cf2279 "5aeb3587211517b95e1a05478fe8886008cf2279 commit on github"): \[Validator\] made the namespace prefix for annotations configurable
  * [23ac47e](http://github.com/symfony/symfony/commit/23ac47e0119f783b4396ebeaf682aaa465916caa "23ac47e0119f783b4396ebeaf682aaa465916caa commit on github"): \[Form\] added support for __get and __set in PropertyPath
  * [0bdb271](http://github.com/symfony/symfony/commit/0bdb27160895b08a4df476286c934b4e63290904 "0bdb27160895b08a4df476286c934b4e63290904 commit on github"): \[Form\] added parent calls to all configure() methods of Fields and Transformers
  * [3127312](http://github.com/symfony/symfony/commit/3127312139bb735663c5184ef5a0a7031c69712d "3127312139bb735663c5184ef5a0a7031c69712d commit on github"): \[Form\] added option 'value_transformer' and 'normalization_transformer' to Field class

Documentation
-------------

  * New <a href="http://trac.symfony-project.org/wiki/IRCLogs20101118">IRC Logs 2010 11 18</a> page

New [job postings](http://trac.symfony-project.com/trac/wiki/JobPostings)
----------------

  * Symfony + PHP Developer at [ProductReview.com.au](http://www.productreview.com.au) - full-time based in Sydney, Australia - Contact: jobs@productreview.com.au
  * Symfony / PHP Developer at [creative-task](http://www.creative-task.de) - freelance at our office in Darmstadt or Hamburg, Germany - Contact: info [at] creative-task [dot] de

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [majaxDoctrineMedia](http://www.symfony-project.org/plugins/majaxDoctrineMediaPlugin): a media system for video/audio/photo management within symfony.
  * [majaxJquery](http://www.symfony-project.org/plugins/majaxJqueryPlugin): an up to date jQuery and jQuery UI Plugin.
  * [sfResque](http://www.symfony-project.org/plugins/sfResquePlugin): a simple wrapper for php-resque to use symfony's configuration.
  * [sfWdCalendar](http://www.symfony-project.org/plugins/sfWdCalendarPlugin): support for wdCalendar in symfony.
  * [sfDoctrineRestBasic](http://www.symfony-project.org/plugins/sfDoctrineRestBasicPlugin): a very basic, but fully extendable REST webservice generator (includes output serialization, jsonp tunneling, and hooks to check for api keys).

Updated plugins
---------------

  * [sfThrift](http://www.symfony-project.org/plugins/sfThriftPlugin):
    * updated documentation

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * delete action does not throw an exception if the element can't be deleted now
    * updated _flashes.php partial (it now uses the i18nCatalogue instead of sf_admin)

  * [sfAdminDash](http://www.symfony-project.org/plugins/sfAdminDashPlugin):
    * installed the backend application
    * added the user manage module in the backend

  * [sfPostgresDoctrine](http://www.symfony-project.org/plugins/sfPostgresDoctrinePlugin):
    * added ability to use custom table class for all Doctrine_Table objects

  * [sfPropel15](http://www.symfony-project.org/plugins/sfPropel15Plugin):
    * updated Propel vendor to the 1.5 branch
    * changed propel external to 1.5.5 tag

  * [sfDoctrinePoll](http://www.symfony-project.org/plugins/sfDoctrinePollPlugin):
    * cleaned up the schema a bit and removing the package information which is no longer needed
    * added a plugin configuration file
    * added the generated form and filter classes which are now standard
    * fixed the routing for symfony 1.2+
    * renamed sfPoll to sfPollQuestion since it makes much more sense
    * added a new "Poll" to the model. This allows for having multiple polls and have the questions associated with a poll

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * changed foreign fields combos to not have remote stores

  * [sfPropelMigrationsLight](http://www.symfony-project.org/plugins/sfPropelMigrationsLightPlugin):
    * changed xml to include support for SF 1.4
    * updated the migrate task to allow the application param to be optional (defaults to frontend)

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * removed unnecessary rtrim call
    * added some performance tweaks
    * fixed some small toolkit bugs
    * added tests for TaggableToolkit

  * [sfFilesystemFixtures](http://www.symfony-project.org/plugins/sfFilesystemFixturesPlugin):
    * moved functionality to dedicated class
    * added load task
    * use DIRECTORY_SEPARATOR constant
    * added method and task to clean existing fixtures
    * better parameter specification

  * [sfEnvironmentFixtures](http://www.symfony-project.org/plugins/sfEnvironmentFixturesPlugin):
    * use DIRECTORY_SEPARATOR constant
    * corrected installation instructions

  * [sfGoogleAnalytics](http://www.symfony-project.org/plugins/sfGoogleAnalyticsPlugin):
    * merged work from github

  * [sfFeed2](http://www.symfony-project.org/plugins/sfFeed2Plugin):
    * fixed validator.w3c.org/feed warning about atom:link rel="self" element

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * tweaked script tags to validate for the xhtml 1.0 strict doctype
    * updated the form formatting to output a class "has-errors" on the a-form-row div of the field with errors
    * created a new formFormatter for the page settings engine forms
    * moved aTools::strtolower to aString::strtolower and added aString::substr and aString::strlen
    * removed references to the blog plugin from the sample templates in apostrophePlugin
    * fixed bug with radioToggle where it would output many times
    * commented out an apostropheLog for something in aControls

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * fixed misnamed query alias in blog rss action
    * switched the form formatter for the engine page settings forms


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [Calciomercato.com](http://www.calciomercato.com): \(English, Italian\) Since 1996, Italy's !#1 source for all Italian football fans, football journalists and professionals because of its recognized qualities
  * [www.widge.de](http://www.widge.de/): \(Deutsch\) German finance and insurance news and information website


They talked about us
--------------------

  * [Jonathan Wage abandona Sensio Labs](http://www.symfony.es/2010/11/15/jonathan-wage-abandona-sensio-labs/)
  * [symfony 1, Symfony2 et Django sont dans un bateau](http://www.amicalement-web.net/symfony-1-symfony2-et-django-sont-dans-un-bateau/2010/11/15/)
  * [Easy page composition with symfony, doctrine and the gjPositionsPlugin is now BETA!](http://test.ical.ly/2010/11/17/easy-page-composition-with-symfony-doctrine-and-the-gjpositionsplugin-is-now-beta/)
  * [Apostrope CMS: Ошибка, при добавление русских названий страниц.](http://jeka.ru/2010/11/17/apostrope-cms-oshibka-pri-dobavlenie-russkix-nazvanij-stranic/)
  * [Propel 1.5.5 released](http://propel.posterous.com/propel-155-released)
  * [When to use gjPositionsPlugin for composition in your next symfony/doctrine project](http://test.ical.ly/2010/11/18/when-to-use-gjpositionsplugin-for-composition-in-your-next-symfonydoctrine-project/)
  * [Performance tweaking for symfony plugin gjPositionsPlugin and bugfixes for doctrine behaviour LooseCoupling](http://test.ical.ly/2010/11/19/performance-tweaking-for-symfony-plugin-gjpositionsplugin-and-bugfixes-for-doctrine-behaviour-loosecoupling/)
  * [Filesystem fixtures for symfony](http://ezzatron.com/2010/11/19/filesystem-fixtures-for-symfony/)
  * [task con progress bar](http://www.symfony.it/articoli/376/task-con-progress-bar/)
  * [Ajaxify Symfony Admin Generator](http://nibsirahsieu.wordpress.com/2010/11/21/ajaxify-symfony-admin-generator/)
  * [Setting up a Symfony Project in Netbeans](http://www.learnwebdev.com/?p=372)
  * [Doctrine connection error - symfony 1.4 - PHP 5.3](http://www.metod.si/doctrine-connection-error-symfony-1-4-php-5-3/)
  * [Configuration de netbeans 6.9 pour symfony](http://plusdeplus.blogspot.com/2010/11/configuration-de-netbeans-69-pour.html)
  * [Symfony Vs. KumbiaPHP - Parte 1](http://grupoevolucion.blogspot.com/2010/11/symfony-vs-kumbiaphp-parte-1.html)
  * [Symfony2勉強会向けのセットアップ準備（Mac向け）](http://d.hatena.ne.jp/Kiske/20101118/1290031924)
  * [symfony をやってみよう　その２](http://d.hatena.ne.jp/creativeability/20101117/1290000553)
  * [symfonyで１つのフォームから複数のtableに登録する　解決](http://d.hatena.ne.jp/hiroiwa/20101117/1289986644)
  * [Apostrophe, un CMS Open source basé sur Symfony framework](http://blog.smile.fr/Apostrophe-un-CMS-Open-source-base-sur-Symfony-framework)
  * [symfonyからTwitter Streaming APIを使ってつぶやきを保存してみる](http://d.hatena.ne.jp/tech-tech/20101116/1289933486)
  * [Mes projets web à venir](http://clementguillemain.com/2010/626/mes-projets-web-a-venir.html)
  * [การ query ด้วย doctrine ใน symfony](http://www.meteenee.com/%E0%B8%81%E0%B8%B2%E0%B8%A3-query-%E0%B8%94%E0%B9%89%E0%B8%A7%E0%B8%A2-doctrine-%E0%B9%83%E0%B8%99-symfony)
  * [はじめて symfony を勉強する前に注意すること](http://weble.org/2010/11/16/symfony-install)
  * [symfonyでメールを送る（かなり強引編）](http://tech.maid-san.org/archives/321)
  * [Dialogos con Jquery y symfony](http://www.angelontheweb.com/mx/dialogos-con-jquery-y-symfony/)
  * [How to add a "Save and List" Action Button to Symfony Admin Generator Form](http://www.julianstricker.com/how-add-save-and-list-action-button-symfony-admin-generator-form)
