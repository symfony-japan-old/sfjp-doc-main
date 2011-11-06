A week of symfony #253 (31 October -> 6 November 2011)
======================================================

This week, [Symfony 2.0.5 was released](http://symfony.com/blog/symfony-2-0-5-released), fixing tens of minor bugs and introducing some tweaks ([view changelog](https://github.com/symfony/symfony/blob/2.0/CHANGELOG-2.0.md)). Meanwhile, in the [last weekly IRC meeting](https://groups.google.com/forum/#!topic/symfony-devs/MDi_Yw-7cIY), it was announced a big push for Symfony2 components, including a revamped documentation.
 
Development mailing list
------------------------

  * [Sonata Admin Bundle Split](https://groups.google.com/forum/#!topic/symfony-devs/15xCDUR9tGs)
  * [Week #44 IRC meeting](https://groups.google.com/forum/#!topic/symfony-devs/MDi_Yw-7cIY)
  * [ACL/Pager concerns](https://groups.google.com/forum/#!topic/symfony-devs/7g75BvgukPA)
  * [Symfony2 + Smarty](https://groups.google.com/forum/#!topic/symfony-devs/fQ78BPyr30E)

Symfony2 development highlights
-------------------------------

[2.0 branch](http://github.com/symfony/symfony/commits/2.0):

  * [c9d05d7](http://github.com/symfony/symfony/commit/c9d05d72365aa2e20e17e3322b82d7a75f542b88 "c9d05d72365aa2e20e17e3322b82d7a75f542b88 commit on github"): let NumberFormatter handle integer type casting
  * [89cd64a](http://github.com/symfony/symfony/commit/89cd64a4a512009d11b027014fcb56e0a8fad104 "89cd64a4a512009d11b027014fcb56e0a8fad104 commit on github"): set error code when number cannot be parsed
  * [c5e2def](http://github.com/symfony/symfony/commit/c5e2defe5f6019bdd24ffa4ccb73b78afac90e47 "c5e2defe5f6019bdd24ffa4ccb73b78afac90e47 commit on github"): fixed ternary operator usage in RequestMatcher::checkIpv6()
  * [af6f0d5](http://github.com/symfony/symfony/commit/af6f0d55489e8cff5d9b753bf5e9e67f4657461e "af6f0d55489e8cff5d9b753bf5e9e67f4657461e commit on github"): \[Form\] removed some incomplete unit tests, added some new ones
  * [dbba796](http://github.com/symfony/symfony/commit/dbba79651ab8109c1337967a457d94966f76ee74 "dbba79651ab8109c1337967a457d94966f76ee74 commit on github"): \[Yaml\] fixed dumper for floats when the locale separator is not a dot


[Master branch](http://github.com/symfony/symfony/commits/master):

  * [cbd0c3c](http://github.com/symfony/symfony/commit/cbd0c3c8e98c55299066711f6a642cfe2e87dd23 "cbd0c3c8e98c55299066711f6a642cfe2e87dd23 commit on github"): \[Config\] implemented Serializable on resources
  * [d7a5351](http://github.com/symfony/symfony/commit/d7a5351aaa9a8f523b0ec90eb87a32115a0ddcf1 "d7a5351aaa9a8f523b0ec90eb87a32115a0ddcf1 commit on github"), [fc97472](http://github.com/symfony/symfony/commit/fc97472f64cd5494f1ec481cec762817cf638464 "fc97472f64cd5494f1ec481cec762817cf638464 commit on github"): updated composer.json files to contain information about autoloading and target dirs
  * [05a4e9d](http://github.com/symfony/symfony/commit/05a4e9d3861e0a561401ea495f95ee561ee81bfb "05a4e9d3861e0a561401ea495f95ee561ee81bfb commit on github"): \[Validators\] added support for ctype_* functions + tests
  * [149bdb9](http://github.com/symfony/symfony/commit/149bdb962b97e72fd788adf3c3008c3cc2320933 "149bdb962b97e72fd788adf3c3008c3cc2320933 commit on github"): enhanced error messages with regard to form type properties

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [lapeGravatar](http://www.symfony-project.org/plugins/lapeGravatarPlugin): helpers to gravatar service and behavior for doctrine ORM.
  * [lapeQRCode](http://www.symfony-project.org/plugins/lapeQRCodePlugin): (no description)
  * [sfBeSocial](http://www.symfony-project.org/plugins/sfBeSocialPlugin): adds Facebook and Twitter connect to your project.
  * [cpCurrencyDoctrine](http://www.symfony-project.org/plugins/cpCurrencyDoctrinePlugin): provides a model for worldwide currencies to use in your application.
  * [sfFlexbox](http://www.symfony-project.org/plugins/sfFlexboxPlugin): a symfony 1.4 simple widget for jquery flexbox plugin.

Updated plugins
---------------

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * added new widgets for everybody

  * [sfGuardSecure](http://www.symfony-project.org/plugins/sfGuardSecurePlugin):
    * clear attributes holder on logout

  * [sfTools](http://www.symfony-project.org/plugins/sfToolsPlugin):
    * added the sfFileTools class + unit tests
    * lowercase iconv result for eur symbol
    * added the sfArrayPager class

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * added selectable max_per_page

  * [cpTcpdf](http://www.symfony-project.org/plugins/cpTcpdfPlugin):
    * fixed TCPDFX

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * refactored linkToRemote, extracting loadRemote, which loads a URL and updates a container with it immediately, setting loading and loaded classes etc. in the way we've come to rely on
    * turned off some apostrophe.log called that happen every page load that we don't need to hear from
    * apostrophe's stylesheets and javascripts triggered by loading the aHelper now load first
    * the standardArea component's list of standard slots and the standard set of options for those slots, as well as the options for the area itself, can now be overridden via app.yml
    * the video slot template files are now overrideable
    * refactored the actual header in _uploadMultiple to a separate partial so it can be overridden easily without copying a lot of scary code
    * added aString::implodeWithAnd() which uses commas and 'and' as appropriate
    * made the array of Office extensions and mime types public for convenience elsewhere
    * added 'ESC' to close menuToggles. You can now use the ESC key to close page settings, add content, etc.
    * files that should not be minified now load after files that are

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * no longer show a "google maps" button next to the address (simply show the first line of the address as a link to google maps)
    * blog/event excerpt length shortened to 50 words
    * fixed a bug with the event admin popular tags listing


They talked about us
--------------------

  * [symfony dynamic max_per_page](http://symfony-world.blogspot.com/2011/10/symfony-dynamic-maxperpage.html)
  * [Symfony Day Cologne and CMF hackday](http://blog.liip.ch/archive/2011/11/01/symfony-day-cologne-and-cmf-hackday.html)
  * [Why Mockery is better than PHPUnit Mock Builder and how to integrate it with Symfony2](http://blog.sznapka.pl/why-mockery-is-better-than-phpunit-mock-builder-and-how-to-integrate-it-with-symfony2/)
  * [Отзыв о Symfony Camp UA 2011](http://tigor.com.ua/blog/2011/11/02/symfony-camp-ua-2011-report/)
  * [Jornadas sobre Symfony2 en Galicia](http://www.symfony.es/2011/11/02/jornadas-sobre-symfony2-en-galicia/)
  * [D-Day is coming to Finland](http://www.leftontheweb.com/message/DDay_is_coming_to_Finland)
  * [Symfony2: define your bundle’s configuration values using the TreeBuilder](http://php-and-symfony.matthiasnoback.nl/2011/11/symfony2-define-your-bundles-configuration-values-using-the-treebuilder/)
  * [Resumen de la reunión de desarrolladores (3-11-2011)](http://www.symfony.es/2011/11/04/resumen-de-la-reunion-de-desarrolladores-3-11-2011/)
  * [Please Welcome the D-Day Conference in Finland](http://www.hugohamon.com/en/blog/dday-conference-2012-helsinki-finland)
  * [Silex Starter Stubs](http://nerdpress.org/2011/11/04/silex-starter-stubs/)
  * [How to use Symfony2 validator component without forms (Entities and data arrays)](http://www.ricardclau.com/2011/11/how-to-use-symfony2-validator-component-without-forms-entities-and-data-arrays/)
  * [Email jako login w Symfony 2](http://dariussadowski.com/2011/11/email-jako-login-w-symfony-2.html)
  * [symfony 1.4 : Fatal error: Class ‘sfGuardUserFormFilter’ not found](http://www.davidbl.com/?p=176)
  * [Routing (RUS)](http://monsterbirth.ru/symfony-2-book-na-russkom/routing-rus/)
  * [Symfony Developer Meetup in Stockholm](http://developer.e-butik.se/2011/11/symfony-developer-meetup-in-stockholm/)
  * [The state of Symfony2 support in IDEs](http://www.symfony-zone.com/wordpress/2011/11/04/the-state-of-symfony2-support-in-ides/)
  * [« Первый трениг по Symfony2 на Украинских просторах – Я иду!](http://451f.com.ua/symfony-camp-ua-2011-as-it-was/397)
  * [Symfony Conf 2011 в Киеве – небольшой отчет](http://symfony.org.ua/2011/11/symfony-conf-2011-v-kieve-nebolshoj-otchet/)
  * [Définir la hauteur d’une iframe selon son contenu au chargement de la page](http://www.erreur500.com/?p=143)
  * [Modificando el sistema de login de Symfony2](http://roberto.costumero.es/2011/11/03/modificando-el-sistema-de-login-de-symfony2/)
  * [Twig Extensions in Symfony 2](http://www.solidwebcode.com/web-development/twig-extensions-symfony-2/)
  * [Symfony Madrid en El Site](http://www.elsite.es/symfony-madrid/)
  * [Starten mit Symfony 2 – Teil 2: Hello World!](http://webmanufaktur.org/2011/11/02/starten-mit-symfony-2-teil-2-hello-world/)
  * [Отзыв о Symfony Camp UA 2011](http://tigor.com.ua/blog/2011/11/02/symfony-camp-ua-2011-report/)
  * [Which framework is best?](http://hasin.wordpress.com/2011/11/02/which-framework-is-best/)
  * [Symfony - Download file bị thừa ký tự xuống dòng](http://code.huypv.net/2011/11/symfony-download-file-bi-thua-ky-tu.html)
  * [Symfony 1.0 開発版(dev) アクセス制限](http://mmj.99ing.net/Entry/1085/)
  * [Symfony – Standard API for Logging Using __callStatic](http://melikedev.com/2011/10/31/symfony-standard-api-for-logging-using-__callstatic/)
  * [Personnalisation avancé des pages d’erreurs, Symfony 2](http://www.mon-beulogue.com/2011/10/31/personnalisation-avance-des-page-derreur-symfony-2/)
  * [Débugger un projet Symfony 2 avec Xdebug et Netbeans](http://www.symfony-grenoble.fr/17/debugger-un-projet-symfony-2-avec-xdebug-et-netbeans/)
  * [Symfony Camp UA 2011](http://kronus.me/2011/10/symfony-camp-ua-2011/)
  * [Symfony2: how to redirect user to a previous page correctly (without using HTTP_REFERER)](http://www.fractalizer.ru/frpost_658/symfony2-how-redirect-user-to-a-previous-page-correctly/)
  * [10分ぐらいで学べるSymfony2 ～データベース接続設定編～](http://d.hatena.ne.jp/taka512/20111030/1319982146)
