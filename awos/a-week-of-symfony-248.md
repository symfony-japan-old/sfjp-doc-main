---
layout: default
title: "A week of symfony #248 (26 September -> 2 October 2011)"
---

A week of symfony #248 (26 September -> 2 October 2011)
=======================================================

This week Symfony2 committed the first changes related with the new [composer component](https://github.com/symfony/symfony/commit/9ade639bb41423be611a023ab6966b855424f7be), a package manager that will greatly simplify bundle installation in symfony projects. In addition, parameters.ini configuration file was replaced by parameters.yml, a new mandatory [checklist for pull requests](http://symfony.com/doc/current/contributing/code/patches.html#check-list) was published and the [documentation of Twig](http://twig.sensiolabs.org/documentation) was significantly  improved.

Development mailing list
------------------------

  * [i18n: fallback mechanism seems is not working ok](https://groups.google.com/forum/#!topic/symfony-devs/69bIps2-CAg)
  * [Got error when creating my own firewall](https://groups.google.com/forum/#!topic/symfony-devs/Wo1ah4zYLes)
  * [ACL Memory Leak?](https://groups.google.com/forum/#!topic/symfony-devs/053aDa9c9lc)


Symfony2 development highlights
-------------------------------

[Master branch](http://github.com/symfony/symfony/commits/master):

  * [a57a4af](http://github.com/symfony/symfony/commit/a57a4aff55ef29562d4a657221ae4d01e3c53b7f "a57a4aff55ef29562d4a657221ae4d01e3c53b7f commit on github"): \[DomCrawler\] added a way to get parsing errors for Crawler::addHtmlContent() and Crawler::addXmlContent() via libxml functions
  * [258a1fd](http://github.com/symfony/symfony/commit/258a1fd7100c0e3418841d062d799debece554bc "258a1fd7100c0e3418841d062d799debece554bc commit on github"): moved makePathRelative to Filesystem
  * [bfb99bf](http://github.com/symfony/symfony/commit/bfb99bf219720f0867a9c7386fad79f8cdd998b5 "bfb99bf219720f0867a9c7386fad79f8cdd998b5 commit on github"): \[FrameworkBundle\] added a --relative option to assets:install
  * [0f7bf41](http://github.com/symfony/symfony/commit/0f7bf4155c2b2c1bf5d0aa202b7de1643b85c8e6 "0f7bf4155c2b2c1bf5d0aa202b7de1643b85c8e6 commit on github"): \[Console\] detect if interactive mode is possible at all
  * [b9ba117](http://github.com/symfony/symfony/commit/b9ba117208d170479ea9c2f7ffbe692c88a8b281 "b9ba117208d170479ea9c2f7ffbe692c88a8b281 commit on github"), [ee0fe7a](http://github.com/symfony/symfony/commit/ee0fe7a2b543bde26af63b3f162a1a5c8f2b81c5 "ee0fe7a2b543bde26af63b3f162a1a5c8f2b81c5 commit on github"): \[Validator\] added a SizeLength validator
  * [d6c4bfb](http://github.com/symfony/symfony/commit/d6c4bfb001f5f3c3847c3f7766467d16f7e8e322 "d6c4bfb001f5f3c3847c3f7766467d16f7e8e322 commit on github"), [ee0fe7a](http://github.com/symfony/symfony/commit/ee0fe7a2b543bde26af63b3f162a1a5c8f2b81c5 "ee0fe7a2b543bde26af63b3f162a1a5c8f2b81c5 commit on github"): \[Validator\] added a Size validator
  * [8b240d4](http://github.com/symfony/symfony/commit/8b240d4c22852ff76faced47ab7ab87e73c32092 "8b240d4c22852ff76faced47ab7ab87e73c32092 commit on github"): implementation of kernel.event_subscriber tag for services
  * [1467bdb](http://github.com/symfony/symfony/commit/1467bdb86837e132891dd1b5605248a736cca5fe "1467bdb86837e132891dd1b5605248a736cca5fe commit on github"): \[Routing\] added RouterInterface::getRouteCollection()

[2.0.x branch](http://github.com/symfony/symfony/commits/2.0):

  * [ed02aa9](http://github.com/symfony/symfony/commit/ed02aa9974a85c87eb2885a01af1df89312e0ade "ed02aa9974a85c87eb2885a01af1df89312e0ade commit on github"): \[Console\] fixed list 'namespace' command display all available commands
  * [72e82eb](http://github.com/symfony/symfony/commit/72e82eb595113652e6c963b46932635d634930e3 "72e82eb595113652e6c963b46932635d634930e3 commit on github"): \[Serializer\] replaced deprecated key_exists alias
  * [9ade639](http://github.com/symfony/symfony/commit/9ade639bb41423be611a023ab6966b855424f7be "9ade639bb41423be611a023ab6966b855424f7be commit on github"), [d535afe](http://github.com/symfony/symfony/commit/d535afeb9837d417d0453f6fa695bbab1ebfacba "d535afeb9837d417d0453f6fa695bbab1ebfacba commit on github"), [731b28b](http://github.com/symfony/symfony/commit/731b28bb921322e3a13f7fa98ef7e3071ee198e0 "731b28bb921322e3a13f7fa98ef7e3071ee198e0 commit on github"): \[composer\] added composer.json
  * [d6b915a](http://github.com/symfony/symfony/commit/d6b915a1746624e6fddc6e052bd8241456349a2b "d6b915a1746624e6fddc6e052bd8241456349a2b commit on github"), [369f181](http://github.com/symfony/symfony/commit/369f1810051895bf86502ffea34a3d2354ee0e16 "369f1810051895bf86502ffea34a3d2354ee0e16 commit on github"): \[FrameworkBundle\] added request scope to assets helper only if needed
  * [c13b4e2](http://github.com/symfony/symfony/commit/c13b4e2b55d88f5d93d2120b90a5155855d03daf "c13b4e2b55d88f5d93d2120b90a5155855d03daf commit on github"): fixed fallback catalogue mechanism in Framework bundle
  * [2db24c2](http://github.com/symfony/symfony/commit/2db24c264f186b50c7f3eddc923dd9f8fd4f452d "2db24c264f186b50c7f3eddc923dd9f8fd4f452d commit on github"): removed time limit for the vendors script
  * [1e7e6ba](http://github.com/symfony/symfony/commit/1e7e6ba305c4b7b66e49545d582325ed1ea5f9d7 "1e7e6ba305c4b7b66e49545d582325ed1ea5f9d7 commit on github"): \[HttpFoundation\] removed the possibility for a cookie path to set it to null (as this is equivalent to /)
  * [1284681](http://github.com/symfony/symfony/commit/128468193f5d23c8ac878f973c49ed191dd82a2a "128468193f5d23c8ac878f973c49ed191dd82a2a commit on github"), [b402835](http://github.com/symfony/symfony/commit/b4028350d26e5e47e620c3574e51daa471ec8c1c "b4028350d26e5e47e620c3574e51daa471ec8c1c commit on github"): \[BrowserKit, HttpFoundation\] standardized cookie paths (an empty path is equivalent to /)
  * [17af138](http://github.com/symfony/symfony/commit/17af13813ace8ed67221b8b185db72adc49e1040 "17af13813ace8ed67221b8b185db72adc49e1040 commit on github"): fixed usage of LIBXML_COMPACT as it is not always available
  * [d429594](http://github.com/symfony/symfony/commit/d429594afbdd2b74cf292c775582fe51cc22a317 "d429594afbdd2b74cf292c775582fe51cc22a317 commit on github"): removed separator of choice widget when the separator is null
  * [600b8ef](http://github.com/symfony/symfony/commit/600b8ef5af3ec680134527facff1a86f16f5ccf7 "600b8ef5af3ec680134527facff1a86f16f5ccf7 commit on github"): \[Validator\] added support for grapheme_strlen when mbstring is not installed but intl is installed
  * [e70c884](http://github.com/symfony/symfony/commit/e70c884f4905878d82b8b5c80d58d96f229290ab "e70c884f4905878d82b8b5c80d58d96f229290ab commit on github"): \[Bridge/Monolog\] fixed WebProcessor to accept a Request object
  * [5c8a2fb](http://github.com/symfony/symfony/commit/5c8a2fb48dfe09537db6ebdd77a52a3c90f409fe "5c8a2fb48dfe09537db6ebdd77a52a3c90f409fe commit on github"): \[Routing\] fixed route overriden mechanism when using embedded collections


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfUploadify](http://www.symfony-project.org/plugins/sfUploadifyPlugin): wraps the Uploadify library for jQuery.(http://www.uploadify.com)
  * [cpLDAPAuth](http://www.symfony-project.org/plugins/cpLDAPAuthPlugin): authenticates users against an LDAP directory.

Updated plugins
---------------

  * [sfPEARcaptcha](http://www.symfony-project.org/plugins/sfPEARcaptchaPlugin):
    * updated Text_CAPTCHA_Driver_Image
    * updated image widget
    * split the function 'render' to 'renderInputField' and 'renderCaptcha'

  * [sfTaskLogger](http://www.symfony-project.org/plugins/sfTaskLoggerPlugin):
    * fixed the "_length" partial on Nix systems

  * [sfAssetsLibrary](http://www.symfony-project.org/plugins/sfAssetsLibraryPlugin):
    * fixed bug in images filtering

  * [cpTwig](http://www.symfony-project.org/plugins/cpTwigPlugin):
    * added twig and twig-extensions as vendor libs

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * cast $user_id to integer in case it arrives as an empty string due to a busted session. Prevents SQL error
    * the new overrideLinks option to apostrophe.linkToRemote() can be used to inject an admin generator module or other really basic Symfony module that is not AJAX-aware into an AJAX container, such as a div
    * aInjectActualUrl function allows me to call it multiple times after dom ready instead of how it was structured before
    * the edit and new admin generator actions should have a title slot, just like the list action does
    * RSS Feed
    * backed out attempts to make the category admin gen classes autoload because Symfony's admin gen has a very limited way of autoloading things that looks for them in specific modulename/lib folders only
    * fixed the aAdmin theme to work when there is no filter and no custom table method
    * app_a_simple_permissions is an extremely simple alternative view permissions model
    * correctly tolerate symfony cc without the right environment settings
    * fixed bug with _menuToggle function in a.js

  * [apostropheCkEditor](http://www.symfony-project.org/plugins/apostropheCkEditorPlugin):
    * fixed source view formatting. It was being displayed in a tiny window instead of the full editor frame




They talked about us
--------------------

  * [Introducing KhepinUpdateBundle](http://sf.khepin.com/2011/09/introducing-khepinupdatebundle/)
  * [parse_ini_file 関数の INI_SCANNER_RAW モードでは DSN が適切にパースされない問題](http://blog.sarabande.jp/post/10652583954)
  * [Symfony2: Working with multiple databases](http://www.theodo.fr/blog/2011/09/symfony2-working-with-multiple-databases/)
  * [Loosening dependencies with closures in PHP](http://blog.sznapka.pl/loosening-dependencies-with-closures-in-php/)
  * [A frontend editor for Symfony2 CMF with the help of VIE](http://blog.liip.ch/archive/2011/09/27/a-frontend-editor-for-symfony2-cmf-with-the-help-of-vie.html)
  * [Noch wenige Wochen bis zum Symfony Day Cologne](http://www.artikel-presse.de/?p=409322)
  * [symfony1 sfTaskLoggerPlugin 1-0-3 released](http://www.strangebuzz.com/index.php/2011/09/29/44-symfony1-sftaskloggerplugin-1-0-3-released)
  * [October PHP Conferences](http://blog.servergrove.com/2011/09/29/october-php-conferences/)
  * [Symfony2 unit database tests](http://www.theodo.fr/blog/2011/09/symfony2-unit-database-tests/)
  * [Symfony CMF hackday October 22nd in Cologne](http://blog.liip.ch/archive/2011/09/30/symfony-cmf-hackday-october-22nd-in-cologne.html)
  * [Интеграция шаблонизатора Twig в CodeIgniter 2](http://habrahabr.ru/blogs/codeigniter/129537/)
  * [Symfony 1.4 : distance_of_time_in_words en français](http://www.jonathan-petitcolas.com/symfony-1-4-distance_of_time_in_words-en-francais/)
  * [Gushing over Web Frameworks](http://robbymillsap.com/2011/09/30/best-web-frameworks/)
  * [Smarty vs. Twig: производительность](http://habrahabr.ru/blogs/php/128083/)
  * [Symfony2でMongoDBを使ってみよう。](http://blog.livedoor.jp/hamichamp/archives/51745923.html)
  * [opCommunityTopicPlugin 1.0.2.1 リリースのお知らせ](http://www.openpne.jp/archives/6461/)
  * [Create a custom password encoder for Symfony](http://blogsh.de/2011/09/29/create-a-custom-password-encoder-for-symfony/)
  * [Symfony 2 – Events and Listeners](http://www.solidwebcode.com/web-development/oop/symfony-2-events-listeners/)
  * [Remove default CSS/Javascript in View.yml](http://imchain.com/portfolio/symfony-remove-default-cssjavascript-in-view-yml/)
  * [Reunión de programadores en PHP Barcelona Conference](http://masdigital.elperiodico.com/informatica/reunion-de-programadores-en-php-barcelona-conference)
  * [Symfony Doctrine “where in” and “where not in” Syntax](http://www.ozonesolutions.com/programming/2011/09/symfony-doctrine-where-in-and-where-not-in-syntax/)
  * [Symfony2のススメ2 ～認証とともに～](http://tech.ecnavi.co.jp/archives/4402391.html)
  * [MAMP環境でsymfony doctrine:buildに失敗する](http://studiowebnote.blogspot.com/2011/09/mampsymfony-doctrinebuild.html)
  * [Symfony 2 et Play! : Frameworks de productivité](http://www.docdoku.com/blog/2011/09/27/symfony-2-et-play-frameworks-de-productivite/)
  * [Symfony2 и основные положения HTTP](http://monsterbirth.ru/symfony-2-book-na-russkom/symfony2-i-osnovnye-polozheniya-http/)
  * [openpne3系インストール(windows版)](http://atomicheart.me/blog/2011/09/27/openpne3%E7%B3%BB%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%ABwindows/)
  * [Capifony + Symfony2 Revisited Experience](http://www.craftitonline.com/2011/09/capifony-symfony2-revisited-experience/)
