A week of symfony #249 (3->9 October 2011)
==========================================

Symfony 2.0.4 version was [released this week](http://symfony.com/blog/symfony-2-0-4-released), maintaining the fast pace of Symfony2 upgrades. In addition, the independent [security audit of Symfony2](http://symfony.com/blog/symfony2-security-audit) and Twig code was disclosed. Lastly, an important, and backwards incompatible change, was committed to the Symfony2 master branch: locale management was moved from the Session class to the Request class ([see details](https://github.com/symfony/symfony/commit/74bc699b270122b70b1de6ece47c726f5df8bd41)).
 
Development mailing list
------------------------

  * [Sessions](https://groups.google.com/forum/#!topic/symfony-devs/0j1IdfekOHQ)
  * [\[RFC\] \[AsseticBundle\] configuring bundles](https://groups.google.com/forum/#!topic/symfony-devs/nWddMcXLbh8)
  * [symfony 2 - reusable distribution](https://groups.google.com/forum/#!topic/symfony-devs/1HyK24Zs0I8)
  * [supporting API versioning](https://groups.google.com/forum/#!topic/symfony-devs/O2EClN1-Q-I)

symfony 1 development highlights
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=09%2F10%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r33121](http://trac.symfony-project.org/changeset/33121 "33121 revision on trac"): \[1.4\] fixed protocol relative URL in the asset helper
  * [r33122](http://trac.symfony-project.org/changeset/33122 "33122 revision on trac"): \[1.4\] fixed include|get_component when sfPartialView class is customized
  * [r33125](http://trac.symfony-project.org/changeset/33125 "33125 revision on trac"): \[1.4\] fixed the possibility to include files included in an exclude rule in the deploy task

sfDoctrinePlugin:

  * [r33123](http://trac.symfony-project.org/changeset/33123 "33123 revision on trac"): \[1.4\] fixed virtual columns in sfFormFilterDoctrine

Symfony2 development highlights
-------------------------------

[2.0 branch](http://github.com/symfony/symfony/commits/2.0):

  * [cf4a91e](http://github.com/symfony/symfony/commit/cf4a91e923c1192308311c390f42485d27721d10 "cf4a91e923c1192308311c390f42485d27721d10 commit on github"): \[ClassLoader\] fixed usage of trait_exists()
  * [92d1906](http://github.com/symfony/symfony/commit/92d19063a843c53537e49a3c74a052287b4792b2 "92d19063a843c53537e49a3c74a052287b4792b2 commit on github"): \[Translation\] changed some unit tests for PHPUnit 3.6.0 compatibility
  * [828b18f](http://github.com/symfony/symfony/commit/828b18f4673f09832be1692bd99bfe6de9112689 "828b18f4673f09832be1692bd99bfe6de9112689 commit on github"): \[Form\] fixed lacking attributes in DateTimeType
  * [a74ae9d](http://github.com/symfony/symfony/commit/a74ae9d325e23747e274448c69d688bcc2705d42 "a74ae9d325e23747e274448c69d688bcc2705d42 commit on github"): \[HttpFoundation\] made X_REWRITE_URL only available on Windows platforms
  * [95049ef](http://github.com/symfony/symfony/commit/95049ef902fa4818bb4c221dc2ed2d582e792cc9 "95049ef902fa4818bb4c221dc2ed2d582e792cc9 commit on github"): \[Form\] added type check to ScalarToChoiceTransformer
  * [18a83c6](http://github.com/symfony/symfony/commit/18a83c67f41c2052cb1037f629838371d2aea202 "18a83c67f41c2052cb1037f629838371d2aea202 commit on github"): \[Form\] simplified a bit FormUtil and extended test coverage
  * [ae0685a](http://github.com/symfony/symfony/commit/ae0685a3142a2c58866f6dcde4145258e673d0c1 "ae0685a3142a2c58866f6dcde4145258e673d0c1 commit on github"): \[Translation\] loader should only load local files

[Master branch](http://github.com/symfony/symfony/commits/master):

  * [6b16757](http://github.com/symfony/symfony/commit/6b16757199000a53d733d5568828e3f6e5b038ab "6b16757199000a53d733d5568828e3f6e5b038ab commit on github"): \[Security\] changed a RuntimeException to LogicException for consistencies between the different Token classes
  * [3f567b8](http://github.com/symfony/symfony/commit/3f567b82089e2bdeb6fb731231d398e416cc38a5 "3f567b82089e2bdeb6fb731231d398e416cc38a5 commit on github"): \[FrameworkBundle\] moved a parameter in the same file as the one where the service is defined for better consistency
  * [d7c9644](http://github.com/symfony/symfony/commit/d7c9644d291ff17b430912b67cc295dbf15200f2 "d7c9644d291ff17b430912b67cc295dbf15200f2 commit on github"): \[Validator\] extend and fix DateValidator & TimeValidator tests
  * [deb6dea](http://github.com/symfony/symfony/commit/deb6dea76dec7d38671afa5ff3f2c278ea28dd65 "deb6dea76dec7d38671afa5ff3f2c278ea28dd65 commit on github"): \[Translation\] added failing tests to verify that UTF-8 lang files can't be used with another charset
  * [5473d3b](http://github.com/symfony/symfony/commit/5473d3b6c94ac38d0658f9745c582f840d49464e "5473d3b6c94ac38d0658f9745c582f840d49464e commit on github"): \[Translation\] allowed use of UTF-8 encoded catalogues into non-UTF-8 applications
  * [395f580](http://github.com/symfony/symfony/commit/395f580fd7e9fd49ba850198da0c333bc6d28d3b "395f580fd7e9fd49ba850198da0c333bc6d28d3b commit on github"): rebuilt resource files with genrb from ICU 4.2. as ICU 4.4 by default builds them in newer format
  * [8b55541](http://github.com/symfony/symfony/commit/8b55541aeefc78366daa0296fc67151edd1977c9 "8b55541aeefc78366daa0296fc67151edd1977c9 commit on github"): added an UPGRADE file
  * [74bc699](http://github.com/symfony/symfony/commit/74bc699b270122b70b1de6ece47c726f5df8bd41 "74bc699b270122b70b1de6ece47c726f5df8bd41 commit on github"): [BC BREAK] moved management of the locale from the Session class to the Request class


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfRestProxy](http://www.symfony-project.org/plugins/sfRestProxyPlugin): great REST plugin

Updated plugins
---------------

  * [sfSimplePage](http://www.symfony-project.org/plugins/sfSimplePagePlugin):
    * added new configuration option to disable routes generation
    * MOD document new option

  * [sfXssSafe](http://www.symfony-project.org/plugins/sfXssSafePlugin):
    * released 1.1.0 version
    * fixed sfXssSafePlugin 0.95 fails to utilize HTML Purifier caching and generates PHP warnings

  * [sfGuardSecure](http://www.symfony-project.org/plugins/sfGuardSecurePlugin):
    * allowes CAPTCHA extra field

  * [sfFormExtra](http://www.symfony-project.org/plugins/sfFormExtraPlugin):
    * fixed recaptcha URLs

  * [apostropheS3Storage](http://www.symfony-project.org/plugins/apostropheS3StoragePlugin):
    * moved the task out to apostrophePlugin
    * debugged the cache feature (read-only cache of the first 8K & results of stat())
    * tests pass when the -aux and -aux2 buckets already exist

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * workaround for potential XSS attack in page titles due to framework bug
    * made Apostrophe load-balancing and cloud-storage friendly
    * button slot no longer does last-minute str_replace on getEmbedCode, which is the old no-longer-supported DOS-friendly thing to do
    * existing video thumbnails are correctly accepted as a default for the file widget again
    * single-image slot no longer relies on the str_replace technique to generate media URLs
    * removed lots of error_log calls
    * new 'absolute' option to getScaledUrl allows absolute URLs to be retrieved
    * if an 'authorize' request is sent to getScaledUrl, return an array with just the URL for the image, rather than just returning true
    * added a context to the symfony cc task during the preCommand event rather than postCommand so that it benefits all postCommand handlers that need a context
    * made very sure we don't try to delete the original when a crop is removed
    * call getOriginalPath when rendering
    * use real routing to generate the local media URLs so that overrides of the routes work as expected
    * added options parameter and prependToRootRelative option to Minify_CSS_UriRewriter::prepend()




They talked about us
--------------------

  * [Cupon, una nueva aplicación de ejemplo de Symfony2](http://www.symfony.es/2011/10/03/cupon-una-nueva-aplicacion-de-ejemplo-de-symfony2/)
  * [symfony1 sfTCPDFPlugin 1-6-3 released](http://www.strangebuzz.com/post/2011/10/05/symfony1-sfTCPDFPlugin-1-6-3-released)
  * [Usare Symfony2 con subversion](http://www.symfony.it/articoli/520/usare-symfony2-con-subversion/)
  * [About your job opening...](http://www.leftontheweb.com/message/About_your_job_opening)
  * [Propel2 has begun!](http://propel.posterous.com/propel2-has-begun)
  * [Se anuncian grandes novedades para la próxima versión de Propel](http://www.symfony.es/2011/10/06/se-anuncian-grandes-novedades-para-la-proxima-version-de-propel/)
  * [symfony1 sfTaskLoggerPlugin 1-0-3 released](http://www.strangebuzz.com/post/2011/09/29/symfony1-sfTaskLoggerPlugin-1-0-3-released)
  * [Quelques bonnes raisons (et pas uniquement techniques!) de remplacer votre vieux framework](http://www.clever-age.com/veille/blog/quelques-bonnes-raisons-et-pas-uniquement-techniques-de-remplacer-votre-vieux-framework.html)
  * [Resumen de la reunión de desarrolladores del 6-10-2011](http://www.symfony.es/2011/10/07/resumen-de-la-reunion-de-desarrolladores-del-6-10-2011/)
  * [Optimising A PHP (Symfony 1.X/Doctrine 1.X) Application](http://eatmymonkeydust.com/2011/10/optimising_a_php_symfony_doctrine_application/)
  * [About 'rel' attribute from a web developer's point of view](http://avalanche123.com/post/11210600073/about-rel-attribute-from-a-web-developers-point-of)
  * [Codeigniter vs. Other Frameworks](http://borayalcin.me/2011/10/09/codeigniter-vs-other-frameworks/)
  * [Symfony 2 – Listener logowania użytkowników](http://dariussadowski.com/2011/10/symfony-2-listener-logowania-uzytkownikow.html)
  * [OpenPNE 3.6 の新機能について](http://www.openpne.jp/archives/6511/)
  * [Symfony Blog: Symfony2 Security Audit](http://www.php-boutique.de/symfony-blog-symfony2-security-audit)
  * [Optimising a PHP (symfony 1.x/Doctrine 1.x) application](http://elephpants.blog.redpill-linpro.com/2011/10/07/optimising_a_php_symfony_doctrine_application-2/)
  * [【转】 主流PHP框架间的比较（Zend Framework，CakePHP，CodeIgniter，Symfony，ThinkPHP，FleaPHP）](http://hi.baidu.com/avauntage/blog/item/2600d9fd4dc9b459d7887dd1.html)
  * [Symfony2 – Ce qui change](http://clycks.fr/2011/10/296-symfony2-ce-qui-change)
  * [はじめるよ！](http://symfony.outputstudy.info/2011/10/start/)
  * [Configurer les VirtualHosts pour Symfony](http://mikinfo.free.fr/index.php/configurer-les-virtualhosts-pour-symfony/)
  * [Update symfony](http://www.meteenee.com/update-symfony)
  * [几款主流PHP框架的优缺点评比](http://blog.chedushi.com/archives/223)
  * [Customizing Symfony form rendering by using form formatter](http://tomislavsantek.iz.hr/2011/10/customizing-symfony-form-rendering-by-using-form-formatter/)
  * [PHP環境構築 on Ubuntu(10) symfony 空アプリケーションにモジュールとアクションを追加してみる](http://d.hatena.ne.jp/ux00ff/20111004/1317683245)
  * [A short article on how to setup a symfony 1.4 project with SVN](http://www.totophe.com/2011/10/03/a-short-article-on-how-to-setup-a-symfony-1-4-project-with-svn/)
  * [Symfony2 против Flat PHP](http://monsterbirth.ru/symfony-2-book-na-russkom/symfony2-protiv-flat-php/)
  * [Deploy Symfony application with capifony](http://www.screenfony.com/blog/deploy-symfony-application-with-capifony)
  * [Generación de reportes PDF con Symfony 1.4, Doctrine y FPDF](http://blog.datasolutions.pe/index.php/20111002/generacion-de-reportes-pdf-con-symfony-1-4-doctrine-fpdf/)
  
