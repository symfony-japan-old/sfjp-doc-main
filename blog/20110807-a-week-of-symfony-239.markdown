A week of symfony #239 (25->31 July 2011)
=========================================

Symfony 2.0.0バージョンがついに[今週リリースされました](http://symfony.com/blog/symfony-2-0), 18ヶ月前に始まった素晴らしい旅の終わりを示しています。このリリースはまた、Symfonyプロジェクトの輝かしい未来とその生態系の拡大が始まったことを示しています。 
 
開発ML
------------------------

  * [DIコンテナコンポーネントのドキュメント](https://groups.google.com/forum/#!topic/symfony-devs/I5g7lijdkWM)
  * [\[Symfony2\] ParameterBagと配列へのデータのセット](https://groups.google.com/forum/#!topic/symfony-devs/2-SWFtFKwxQ)
  * [Symfony 2.1と2.0のメンテナンスブランチ](https://groups.google.com/forum/#!topic/symfony-devs/JGYWiiUEJqw)
  * [2.0 リリースのためのバンドルのタギング](https://groups.google.com/forum/#!topic/symfony-devs/XxUz1yITBVM)

symfony 1 開発ハイライト 
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=31%2F07%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r32835](http://trac.symfony-project.org/changeset/32835 "32835 revision on trac"): \[1.4\] fixed when the renderer does not have the translate_choices option (see sfFormExtraPlugin for some examples)
  * [r32836](http://trac.symfony-project.org/changeset/32836 "32836 revision on trac"): \[1.4\] fixed guessFromFileBinary in class sfvalidatorFile does not support MIME type including dot

Symfony2 開発ハイライト
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [5219f81](http://github.com/symfony/symfony/commit/5219f81f3575277aab9263c3a64113ee632c8fb2 "5219f81f3575277aab9263c3a64113ee632c8fb2 commit on github"): use the $status parameter instead of fixed value when creating a RedirectResponse
  * [0b3ff39](http://github.com/symfony/symfony/commit/0b3ff39704a6978b6183a24081ce2eb2854eb8bd "0b3ff39704a6978b6183a24081ce2eb2854eb8bd commit on github"): fix supported cookie date formats
  * [c53c169](http://github.com/symfony/symfony/commit/c53c1692c29007fd6df23b9cb08560daac475642 "c53c1692c29007fd6df23b9cb08560daac475642 commit on github"): added a CONTRIBUTORS file
  * [3ea31a0](http://github.com/symfony/symfony/commit/3ea31a02630412b1c732ee1647a0724378f67665 "3ea31a02630412b1c732ee1647a0724378f67665 commit on github"), [85c0087](http://github.com/symfony/symfony/commit/85c0087825ccd9b8f4f25ab3120aca2820f5daa1 "85c0087825ccd9b8f4f25ab3120aca2820f5daa1 commit on github"): \[TwigBridge\] made the locale configurable for the trans and transchoice filters
  * [04ac1fd](http://github.com/symfony/symfony/commit/04ac1fdba2498d19977f8967d50b976898edeafe "04ac1fdba2498d19977f8967d50b976898edeafe commit on github"): \[Routing\] changed UrlGeneratorInterface::generate() signature to allow passing objects instead of arrays
  * [853935f](http://github.com/symfony/symfony/commit/853935fbabce601f38a477161fafcd535e1fe23d "853935fbabce601f38a477161fafcd535e1fe23d commit on github"): \[HttpFoundation\] made PHP_AUTH_PW optional
  * [c558b78](http://github.com/symfony/symfony/commit/c558b78bc61211977b31e5d26d5a150f6999547c "c558b78bc61211977b31e5d26d5a150f6999547c commit on github"): avoid rendering the ChoiceType separator if all choices are preferred_choices
  * [07298ac](http://github.com/symfony/symfony/commit/07298ac699a648e67095575f5fa2004359dbf7a9 "07298ac699a648e67095575f5fa2004359dbf7a9 commit on github"): \[Console\] changed back to fgets() in DialogHelper
  * [6773cd7](http://github.com/symfony/symfony/commit/6773cd7e05d3b19eb258c889ff0dcd030e6174ef "6773cd7e05d3b19eb258c889ff0dcd030e6174ef commit on github"): \[Serializer\] removed @api since its not yet part of the stable API
  * [e16ccaa](http://github.com/symfony/symfony/commit/e16ccaac711f5a98c6914203e6a197e1301217f0 "e16ccaac711f5a98c6914203e6a197e1301217f0 commit on github"): \[SecurityBundle\] added short description and help for the init:acl command
  * [ec9c0aa](http://github.com/symfony/symfony/commit/ec9c0aab64d7d7c5a70ac807bff774df1fac31dc "ec9c0aab64d7d7c5a70ac807bff774df1fac31dc commit on github"), [08072e4](http://github.com/symfony/symfony/commit/08072e4595cce1627daeb03cc3f8a5a873e8e2e2 "08072e4595cce1627daeb03cc3f8a5a873e8e2e2 commit on github"), [41fe826](http://github.com/symfony/symfony/commit/41fe82656b5648e195656e3d69ea5981ea12ae53 "41fe82656b5648e195656e3d69ea5981ea12ae53 commit on github"), [f2e4d35](http://github.com/symfony/symfony/commit/f2e4d359318d8d08072b310cb793dd2606dec593 "f2e4d359318d8d08072b310cb793dd2606dec593 commit on github"): harmonized commands documentation by changing ./app/console to php app/console
  * [c3ebdbf](http://github.com/symfony/symfony/commit/c3ebdbf9cceddb82cd2089aaef8c7b992e536363 "c3ebdbf9cceddb82cd2089aaef8c7b992e536363 commit on github"): prepared Symfony 2.0.0 release


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfBrowserFingerprint](http://www.symfony-project.org/plugins/sfBrowserFingerprintPlugin): a plugin to handle browser fingerprint.
  * [trSimpleTip](http://www.symfony-project.org/plugins/trSimpleTipPlugin): wraps simpletip jQuery plugin. This is as helper for generating simple tooltips.
  * [ddShoppingCart](http://www.symfony-project.org/plugins/ddShoppingCartPlugin): provides the capability to create a shopping cart based website.
  * [sfDoctrineFileTrunk](http://www.symfony-project.org/plugins/sfDoctrineFileTrunkPlugin): (no description)

Updated plugins
---------------

  * [ddOnlineStore](http://www.symfony-project.org/plugins/ddOnlineStorePlugin):
    * created the getAllCategoriesExceptRootQuery method

  * [tdCore](http://www.symfony-project.org/plugins/tdCorePlugin):
    * fixed bug in PlugintdConfig table class

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * added the action for title internacionalization and its parameters

  * [sdInteractiveChart](http://www.symfony-project.org/plugins/sdInteractiveChartPlugin):
    * added class to access Googles ScatterChart
    * updated base API to add new functions in Google's API

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * added generateTagsTask method
    * added documentation and a new option called 'tags-per-model' to the task

  * [cpDataTables](http://www.symfony-project.org/plugins/cpDataTablesPlugin):
    * added us date and formatted number sorting methods
    * added natural order sorting

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * don't crash if there is no routing object in the context when getMatchingEnginePageInfo() is invoked by createInstance() in a task
    * actAsSubmit anchor "submit buttons" now correctly submit their own name and text as an additional hidden input
    * notify an a.afterTreeMove event after moving a page in the tree via the reorganize feature
    * refactored apostrophe.updating() in a.js to only require being called once in apostrophe.smartCSS()
    * signingForm uses a_anchor_submit_button() helper with a-show-busy class
    * the title option for the button slot accepts true, false, or a string. If it's a string, it will pass it through as the title UNTIL a new one has been set by the end user in the slot edit form

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * blog heading area had no parameters for the slideshows
    * added separate apostropheGenerateBlogTags to accomodate virtual pages


They talked about us
--------------------

  * [Géolocalisation ou comment créer ses propres fonctions DQL avec Doctrine2](http://www.lexik.fr/blog/symfony/doctrine2/geolocalisation-ou-comment-creer-ses-propres-fonctions-dql-avec-doctrine2-1624)
  * [Symfony2 Launch Party w Gliwicach](http://blog.sznapka.pl/symfony2-launch-party-w-gliwicach/)
  * [Today is the day – happy birthday Symfony 2.0 final!](http://test.ical.ly/2011/07/28/today-is-the-day-symfony-2-0-is-being-released/)
  * [Symfony2 launch party à Montpellier](http://www.lexik.fr/blog/symfony/lexik-life/symfony2-launch-party-a-montpellier-1655)
  * [Symfony2 - La version stable est disponible!](http://www.lafermeduweb.net/billet/symfony2-la-version-stable-est-disponible-1162.html)
  * [Symfony 2.0 released!](http://www.zalas.eu/symfony-2-0-released)
  * [Sensio Labs eröffnet Büro in Deutschland](http://www.presseschleuder.com/2011/07/sensio-labs-eroffnet-buro-in-deutschland/)
  * [Symfony2, une nouvelle chorégraphie](http://www.siteduzero.com/news-62-39979-p1-symfony2-une-nouvelle-choregraphie.html)
  * [Symfony 2.0, finalmente!](http://www.symfony.it/articoli/507/symfony-2-0-finalmente/)
  * [Symfony2 validation in XML](http://vvv.tobiassjosten.net/symfony/symfony2-validation-in-xml)
  * [Вышла финальная версия Symfony2. Ура!](http://habrahabr.ru/blogs/symfony/125129/)
  * [Zeitgemäße PHP-Entwicklung: Symfony 2.0 veröffentlicht](http://www.heise.de/newsticker/meldung/Zeitgemaesse-PHP-Entwicklung-Symfony-2-0-veroeffentlicht-1287604.html)
  * [Mi opinión oficial sobre Symfony2](http://blog.micayael.com/2011/07/28/mi-opinion-oficial-sobre-symfony2-framework/)
  * [Symfony 2.0: początek nowej ery dla frameworków PHP](http://webhosting.pl/Symfony.2.0.poczatek.nowej.ery.dla.frameworkow.PHP)
  * [State-of-the-art PHP development: Symfony 2.0 released](http://www.h-online.com/open/news/item/State-of-the-art-PHP-development-Symfony-2-0-released-1287936.html)
  * [Get objects and related count in one shot](http://www.theodo.fr/blog/2011/07/get-objects-and-related-count-in-one-shot/)
  * [Instalando o Symfony2](http://www.symfonybr.com/2011/07/29/instalando-o-symfony2/)
  * [Symfony 2 disponible](http://www.nexen.net/actualites/php/20304-symfony_2_disponible.php)
  * [Celebrating Symfony2 With One Free Project](http://shout.setfive.com/2011/07/30/celebrating-symfony2-with-one-free-project/)
  * [Symfony 2 wydane](http://www.tarnaski.eu/blog/symfony-2-wydane/)
  * [Symfony 2: Doctrine prePersist Not Firing](http://flipforum.org/symfony-2-doctrine-prepersist-not-firing/)
  * [Symfony 2: Neue Version des MVC-Frameworks final](http://matthiasschuetz.com/symfony-2-neue-version-des-mvc-frameworks-final)
  * [Utilizar data fixtures en tus proyectos Symfony2](http://facultia.com/blog/2011/07/30/utilizar-data-fixtures-en-tus-proyectos-symfony2/)
  * [Symfony2をインストールする](http://192.jp/2011/07/30/install-symfony2/)
  * [Ya tenemos entre nosotros Symfony 2.0, ¡Aleluya!](http://www.genbetadev.com/frameworks/ya-tenemos-entre-nosotros-symfony-20-aleluya)
  * [Symfony2 writing data-fixtures](http://inchoo.net/tools-frameworks/symfony2-data-fixtures-part2/)
  * [Symfony 2.0 Released](http://turbolinux.org/2011/07/symfony-2-0-released/)
  * [Symfony 2.0 发布，PHP框架](http://1.tenking.sinaapp.com/?p=166)
  * [Symfony2 : la version finale du framework PHP est disponible, avec plusieurs améliorations de performances et de securité](http://www.developpez.com/actu/35551/Symfony2-la-version-finale-du-framework-PHP-est-disponible-avec-plusieurs-ameliorations-de-performances-et-de-securite/)
  * [Comment passer sf_user à un formulaire](http://www.blog.manit4c.com/2011/07/29/comment-passer-sf_user-a-un-formulaire/)
  * [PHP-Framework Symfony 2.0 veröffentlicht](http://t3n.de/news/symfony-20-veroffentlicht-323784/)
  * [mmRackspaceFilePlugin: A Symfony 1.4 plugin to easily maintain files hosted in Rackspace Cloud File CDN](http://blog.melimato.com/mmrackspacefileplugin-a-symfony-1-4-plugin-to-easily-maintain-files-hosted-in-rackspace-cloud-file-cdn/)
  * [Symony2 Response Object](http://www.lickmychip.com/2011/07/29/symony2-response-object/)
  * [Symfony 2.0: początek nowej ery dla frameworków PHP](http://pomoc-webmastera.com.pl/07/29/symfony-2-0-poczatek-nowej-ery-dla-frameworkow-php/)
  * [Cum sa instalez sfDoctrineGuardPlugin in Symfony 1.4](http://sandorkovacs84.wordpress.com/2011/07/29/cum-sa-instalez-sfdoctrineguardplugin-in-symfony-1-4/)
  * [Symfony Functional Testing – Form POST and AJAX Request Testing](http://xebee.xebia.in/2011/07/29/symfony-functional-testing-form-post-and-ajax-request-testing/)
  * [Symfony 2.0发布](http://www.maxmars.net/blog/2011/07/symfony-2-0%E5%8F%91%E5%B8%83/)
  * [CakePHP2 betaとSymfony2.0をパフォーマンス比較しました](http://d.hatena.ne.jp/cakephper/20110729/1311903026)
  * [Symfony 2.0 wydane!](http://www.zalas.pl/symfony-2-0-wydane)
  * [Symfony 2 est sorti](http://www.memorandom.fr/php/symfony-2-est-sorti/)
  * [Symfony 2.0 Available for Download](http://techsmashed.com/symfony-2-0-available-for-download/)
  * [Symfony2: Release-Version erschienen](http://blog.explicatis.com/2011/07/symfony2-release-version-erschienen/)
  * [Symfony 2](http://rukei.ru/symfony-2/)
  * [Une première release stable pour Symfony 2!](http://leblogduweb.fr/2011/07/28/une-premiere-release-stable-pour-symfony-2/)
  * [Išleistas Symfony 2 PHP karkasas](http://www.fwd.lt/2011/naujienos/isleistas-symfony-2-php-karkasas/)
  * [Symfony 2.0](http://codethulhu.pl/symfony-2-0/)
  * [Symfony 2.0 is now available](http://blog.squantin.fr/symfony-2-0-is-now-available-4365)
  * [Getting Symfony2 into the Cloud](http://www.collocationservers.com/getting-symfony-2-into-the-cloud_4561)
  * [Symfonyでチェックボックスにはまる (Symfony 1.2)](http://www.flatz.jp/archives/2560)
  * [Symfony and Saving Serialized Objects](http://www.ozonesolutions.com/programming/2011/07/symfony-and-saving-serialized-objects/)
  * [Symfony2 launch party in Patras!!](http://blog.tetra-bytes.gr/2011/07/symfony2-launch-party-in-patras/)
  * [Ouvrir les fichiers Symfony dans son IDE depuis Firefox](http://www.erreur500.com/2011/07/26/symfony/ouvrir-les-fichiers-symfony-dans-son-ide-depuis-firefox/)
  * [Symfony2 and .gitignore](http://0hlsson.se/2011/07/26/symfony2-and-gitignore/)
  * [10分ぐらいで学べるSymfony2 ～基本構造編～](http://d.hatena.ne.jp/taka512/20110726/1311689255)
  * [Symfony 2 from the eyes of a ZFer](http://css.dzone.com/articles/symfony-2-eyes-zfer)
  * [第2回 Symfony温泉に参加しました](http://shishithefool.blogspot.com/2011/07/2-symfony.html)
  * [例外が起きる事をテスト](http://d.hatena.ne.jp/moroto1122/20110726/1311675743)
  * [Symfony2: Custom Authentication Provider](http://tracehello.wordpress.com/2011/07/25/symfony2-custom-authentication-provider/)
  * [Utiliser CKEditor dans symfony](http://www.blog.manit4c.com/2011/07/25/utiliser-ckeditor-dans-symfony/)
  * [Symfony 学习网站](http://www.sunhaibing.com/?p=1045)
