---
layout: default
title: "A week of symfony #247 (19->25 September 2011)"
---

A week of symfony #247 (19->25 September 2011)
==============================================

Symfony2 published this week its [2.0.3 maintenance version](http://symfony.com/blog/symfony-2-0-3-released), which fixed some minor bugs. Meanwhile, 2.1 branch added cool new tweaks and features, such as a new [validator for user password](https://github.com/symfony/symfony/commit/7d3c2df98d993f5406e712e39b7b5a1b1059f814), the ability to set [different options for repeating fields](https://github.com/symfony/symfony/commit/8819db3923e9a2ea8b73b3d0eafcedc4ab899c6b) and [PHP 5.4 traits support](https://github.com/symfony/symfony/commit/e5a23dbdaa0f33a282d425d706c8622f58776016) for ClassLoader. Lastly, symfony developers gathered this week for another symfony meeting and discussed [lots of interesting topics](https://gist.github.com/1235987).

Development mailing list
------------------------

  * [Packaging Symfony with an IDE](https://groups.google.com/forum/#!topic/symfony-devs/PLKiBU3HEQk)
  * [Sf2 HTTP CACHE - ESI problem](https://groups.google.com/forum/#!topic/symfony-devs/93LdIp0rRAE)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [903ab81](http://github.com/symfony/symfony/commit/903ab81434269ec776030a25b3dbadf789c991a5 "903ab81434269ec776030a25b3dbadf789c991a5 commit on github"): \[Translation\] support Ini file format
  * [83199ae](http://github.com/symfony/symfony/commit/83199aec0093918c1820e738a8c3e2be9842c71f "83199aec0093918c1820e738a8c3e2be9842c71f commit on github"): \[FrameworkBundle\] fixed unintuitive merging behavior for assets_base_urls
  * [a0329c3](http://github.com/symfony/symfony/commit/a0329c37c9a00c594bd41fc178ad444926a86da3 "a0329c37c9a00c594bd41fc178ad444926a86da3 commit on github"): added lifetime/cleanup support for MongoDbProfilerStorage
  * [bca551e](http://github.com/symfony/symfony/commit/bca551e86fdba47064454fbabcaf88801aa5da7f "bca551e86fdba47064454fbabcaf88801aa5da7f commit on github"), [cf736cc](http://github.com/symfony/symfony/commit/cf736ccde38465dce8355c7ff2d9d69ef2deded6 "cf736ccde38465dce8355c7ff2d9d69ef2deded6 commit on github"): \[DomCrawler\] ChoiceFormField should take the content when value is unavailable
  * [022a9a7](http://github.com/symfony/symfony/commit/022a9a7a6e8af993957a490561e9ba0c0d4a804f "022a9a7a6e8af993957a490561e9ba0c0d4a804f commit on github"): \[Security\] made saving target_path extendible
  * [7d3c2df](http://github.com/symfony/symfony/commit/7d3c2df98d993f5406e712e39b7b5a1b1059f814 "7d3c2df98d993f5406e712e39b7b5a1b1059f814 commit on github"): \[SecurityBundle\] added a validator for the user password (this validator is useful when you want to validate that an input value is equal to the user current password)
  * [64d44fb](http://github.com/symfony/symfony/commit/64d44fbb9332f7973a21ca9c428d64b3c29ba23d "64d44fbb9332f7973a21ca9c428d64b3c29ba23d commit on github"): \[Translator\] fixed recursion when using a fallback that is the same as the locale
  * [3e90ba4](http://github.com/symfony/symfony/commit/3e90ba4f76ba231f828c50f5e22168e1ceb28e73 "3e90ba4f76ba231f828c50f5e22168e1ceb28e73 commit on github"), [56b6d53](http://github.com/symfony/symfony/commit/56b6d537d6f803e3b497292c14f16fdfd1514126 "56b6d537d6f803e3b497292c14f16fdfd1514126 commit on github"): \[WebProfileBundle\] added missing position attribute in XSD
  * [e98584e](http://github.com/symfony/symfony/commit/e98584e2f3aa931192642e5179cd9919330c612b "e98584e2f3aa931192642e5179cd9919330c612b commit on github"): \[WebProfilerBundle\] tweaked some templates
  * [c9ddd6f](http://github.com/symfony/symfony/commit/c9ddd6fd8b647764f2d2bca64d97cff2cab1ea34 "c9ddd6fd8b647764f2d2bca64d97cff2cab1ea34 commit on github"): \[WebProfilerBundle\] moved the token not found error to the new info page
  * [e5a23db](http://github.com/symfony/symfony/commit/e5a23dbdaa0f33a282d425d706c8622f58776016 "e5a23dbdaa0f33a282d425d706c8622f58776016 commit on github"): \[ClassLoader\] added support for PHP 5.4 traits
  * [98abc8e](http://github.com/symfony/symfony/commit/98abc8ed050d831b9a93b8da31c6453662d80d04 "98abc8ed050d831b9a93b8da31c6453662d80d04 commit on github"): \[DependencyInjection\] changed the default YAML indentation to 4 spaces instead of 2
  * [b6c8f63](http://github.com/symfony/symfony/commit/b6c8f639f071b0baa52dcfac3322a41dd26d1aa4 "b6c8f639f071b0baa52dcfac3322a41dd26d1aa4 commit on github"): \[TwigBridge\] fixed message keys extraction when no domain is defined in the template
  * [e0ace8e](http://github.com/symfony/symfony/commit/e0ace8eaee2756c60d79681d907b01875d06e7dc "e0ace8eaee2756c60d79681d907b01875d06e7dc commit on github"), [b8e5a15](http://github.com/symfony/symfony/commit/b8e5a155e4f0dad7e1d7a687e6e99e48d6447696 "b8e5a155e4f0dad7e1d7a687e6e99e48d6447696 commit on github"): \[DependencyInjection\] fixed array support for the ini loader
  * [ae3aded](http://github.com/symfony/symfony/commit/ae3aded83fbb03a0b043a8c13851c53f8086ed6d "ae3aded83fbb03a0b043a8c13851c53f8086ed6d commit on github"), [d830253](http://github.com/symfony/symfony/commit/d83025387636487163a96d37336be89885e452a0 "d83025387636487163a96d37336be89885e452a0 commit on github"), [e2945c9](http://github.com/symfony/symfony/commit/e2945c9f9b886d19d67291a5bce1ca6da572ae64 "e2945c9f9b886d19d67291a5bce1ca6da572ae64 commit on github"): added PCRE_DOTALL modifier to RouteCompiler to allow urlencoded linefeed in route parameters
  * [8819db3](http://github.com/symfony/symfony/commit/8819db3923e9a2ea8b73b3d0eafcedc4ab899c6b "8819db3923e9a2ea8b73b3d0eafcedc4ab899c6b commit on github"), [0679220](http://github.com/symfony/symfony/commit/0679220b45f9d1f541afbc238a972c15f4276c4e "0679220b45f9d1f541afbc238a972c15f4276c4e commit on github"), [f8a6a4b](http://github.com/symfony/symfony/commit/f8a6a4b1e56f4f3d8e7c32f5a6b6e3884c462945 "f8a6a4b1e56f4f3d8e7c32f5a6b6e3884c462945 commit on github"), [78ebe11](http://github.com/symfony/symfony/commit/78ebe11a0c74cde826c93c3da7228f0d34e1e16d "78ebe11a0c74cde826c93c3da7228f0d34e1e16d commit on github"): \[Form\] allow setting different options to repeating fields

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfPEARcaptcha](http://www.symfony-project.org/plugins/sfPEARcaptchaPlugin): (no description)

Updated plugins
---------------

  * [ddOnlineStore](http://www.symfony-project.org/plugins/ddOnlineStorePlugin):
    * changed configure to setup method

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * top batch actions are now fixed

  * [sfAssetsLibrary](http://www.symfony-project.org/plugins/sfAssetsLibraryPlugin):
    * missing function number for CKEditor

  * [sfTaskLogger](http://www.symfony-project.org/plugins/sfTaskLoggerPlugin):
    * fixed event dispatcher object in order to avoid core log messages
    * added lib folder to make a file specific ignore
    * ignored default generated model files
    * added PlugintlTaskTableExtended.class.php in order to avoid hack or sample file
    * added the 1.4 doctrine admin generator module
    * fixed and updated the documentation

  * [cpTcpdf](http://www.symfony-project.org/plugins/cpTcpdfPlugin):
    * fixed TCPDF

  * [sfTCPDF](http://www.symfony-project.org/plugins/sfTCPDFPlugin):
    * updated TCPDF constants for version 5_9_120
    * updated README and examples
    * tested plugin with TCPDF 5_9_120 (2011-09-22)
    * fixed CS and typos
    * removed 1.1 symfony version from suported versions

  * [cpDatePicker](http://www.symfony-project.org/plugins/cpDatePickerPlugin):
    * fixed date picker

  * [apostrophePeople](http://www.symfony-project.org/plugins/apostrophePeoplePlugin):
    * added more flexible filterNameParams to people Plugin

  * [apostropheS3Storage](http://www.symfony-project.org/plugins/apostropheS3StoragePlugin):
    * behold the best Amazon S3 stream wrapper ever, with full support for subdirectory listings (not just at the bucket level)
    * fixed many bugs in rename(), wrote unit tests for many rename() scenarios

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * added an optional callback to the linkToRemote function
    * re-wrote the content style exceptions for the Rich Text slot
    * aActAsSubmit will trigger a custom event just before .submit() is called: aActAsSubmitCallback
    * togglePageOverlay lets the overlay fadein/out rather that switch on.off


They talked about us
--------------------

  * [My PHP framework winner predictions](http://pooteeweet.org/blog/0/1987#m1987)
  * [Kiedy i dlaczego tworzyć oprogramowanie pod klucz i dlaczego framework Symfony2 pasuje tu jak ulał?](http://xlab.pl/2011/09/kiedy-i-dlaczego-tworzyc-oprogramowanie-pod-klucz-i-dlaczego-framework-symfony2-pasuje-tu-jak-ulal/)
  * [Twig extensions – name them correctly!](http://www.richsage.co.uk/2011/09/20/twig-extensions-name-them-correctly/)
  * [Sensio : « Nous voulons créer un réseau européen d’expertise Symfony »](http://www.silicon.fr/sensio-%C2%AB%C2%A0nous-voulons-creer-un-reseau-europeen-d%E2%80%99expertise-symfony%C2%A0%C2%BB-61340.html)
  * [メソッドの可視性の方針](http://blog.sarabande.jp/post/10537789689)
  * [Функциональное тестирование в Symfony2 с помощью Behat и Mink](http://habrahabr.ru/blogs/symfony/125618/)
  * [Installer Symfony(2) sur linux via le terminal](http://scofred.com/2011/09/24/installer-symfony2-sur-linux-via-le-terminal/)
  * [Using static pages in Symfony](http://www.seattleveggieburgers.com/blog/?p=110)
  * [Symfony2 GraphvizでDIコンテナをグラフィカルに表示](http://blog.stripejam.jp/archives/465)
  * [Symfony 2: Getting Current Route in Twig](http://www.ismailasci.com/blog/symfony-2-getting-current-route-in-twig.html)
  * [Integrating Magento into Symfony2](http://blog.liip.ch/archive/2011/09/21/integrating-magento-into-symfony2.html)
  * [opFavoritePlugin 1.0.1 リリースのお知らせ](http://www.openpne.jp/archives/6418/)
  * [Großes kündigt sich an: Drupal 8 goes Symfony2](http://www.guido-muehlwitz.de/2011/09/drupal-8-goes-symfony2/)
  * [Популярность PHP фреймворков](http://tarlyun.com/php/populyarnost-php-frejmvorkov/)
  * [Symfony 2.0: Server Setup](http://www.scott-sherwood.com/?p=209)
  * [Instalar el plugin de twig para netbeans](http://desarrolla2.com/php-symfony/instalar-el-plugin-de-twig-para-netbeans/)
  * [How to create Links between Applications](http://fengyin.name/2011/09/20/how-to-create-links-between-applications.html)
  * [Symfony 1.4 – Trimite email din linie de comanda](http://sandorkovacs84.wordpress.com/2011/09/20/symfony-1-4-trimite-email-din-linie-de-comanda/)
  * [Zend Framework Vs Symfony](http://www.mti.epita.fr/blogs/2011/09/20/zend-framework-vs-symfony/)
  * [Creating embedded forms in Symfony 2.0](http://www.reecefowell.com/2011/09/19/creating-embedded-forms-in-symfony-2-0/)
  * [Частичное сохранение многоязычных форм Symfony 1.4 в стиле python django-multilingual](http://xn--80ajjboungj8a.com.ua/%D1%87%D0%B0%D1%81%D1%82%D0%B8%D1%87%D0%BD%D0%BE%D0%B5-%D1%81%D0%BE%D1%85%D1%80%D0%B0%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BC%D0%BD%D0%BE%D0%B3%D0%BE%D1%8F%D0%B7%D1%8B%D1%87%D0%BD%D1%8B%D1%85-%D1%84.html)
  * [Assetic & LESS](http://blogsh.de/2011/09/18/assetic-less/)
