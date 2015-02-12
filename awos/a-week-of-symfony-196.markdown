---
layout: default
title: A week of symfony#196 (27 September -> 3 October 2010)
---

A week of symfony #196 (27 September -> 3 October 2010)
=======================================================

Symfony2 focused this week on internationalization: a new <a href="http://github.com/symfony/symfony/commit/a7537906b4e6e370e5911448f41d6d2552f6832b">Translation component</a> was introduced and the Twig bundle added helpers for translations. Meanwhile, the templating notation was modified to always include the renderer name and the Validator component eased its validation annotations.

Development mailing list
------------------------

  * [RFC - config file by host](http://groups.google.com/group/symfony-devs/browse_thread/thread/2d29f16e073d0c93)
  * [Anybody know how used Route Collection?](http://groups.google.com/group/symfony-devs/browse_thread/thread/32282c009eab91df/1cb677bcdf984326)
  * [|safe confusing](http://groups.google.com/group/symfony-devs/browse_thread/thread/b927063310c74411)
  * [Will AOP ever be part of SF2?](http://groups.google.com/group/symfony-devs/browse_thread/thread/8547bebaf4dbe0f0)

symfony 1 development highlights
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=03%2F10%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r31002](http://trac.symfony-project.org/changeset/31002 "31002 revision on trac"): \[1.3, 1.4\] added call to parent::preExecute() to generated admin action classes

Activity summary: 48 changesets, 16 bugs reported, 1 enhancement closed, 5 documentation defects reported, and 6 documentation edits

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [866c306](http://github.com/symfony/symfony/commit/866c306dc860b6b5bf436d9dc9a67c5764bfe504 "866c306dc860b6b5bf436d9dc9a67c5764bfe504 commit on github"): removed the message interpolator system in the Validator component (i18n management should be done globally, not in a specific component)
  * [eb942c8](http://github.com/symfony/symfony/commit/eb942c8f18021d1f42d88f17082a99e00828ab39 "eb942c8f18021d1f42d88f17082a99e00828ab39 commit on github"): \[ZendBundle\] fixed translator configuration
  * [86b6aff](http://github.com/symfony/symfony/commit/86b6aff5b6104e4c55b6d675d72522d22d69c1ac "86b6aff5b6104e4c55b6d675d72522d22d69c1ac commit on github"): \[Form\] fixed bug that prevented setLocale from working
  * [a305eb0](http://github.com/symfony/symfony/commit/a305eb063d40f0a01d77792e7b502a95a89be86f "a305eb063d40f0a01d77792e7b502a95a89be86f commit on github"): \[Form\] added support for rounding-mode option on NumberFields
  * [9e84f45](http://github.com/symfony/symfony/commit/9e84f450c21093391a29f25fd3b9dc38c8d50829 "9e84f450c21093391a29f25fd3b9dc38c8d50829 commit on github"): \[Form\] fixed decimal rounding in IntegerField (instead of rounding half-up, act as an integer cast would and always round down)
  * [b2e4b45](http://github.com/symfony/symfony/commit/b2e4b452a43e1b82286b972960e806ffc3014deb "b2e4b452a43e1b82286b972960e806ffc3014deb commit on github"): \[Form\] added support for stdClass objects
  * [aaba52d](http://github.com/symfony/symfony/commit/aaba52d92816bdc9ce27b491dc8d28c2587c2c2c "aaba52d92816bdc9ce27b491dc8d28c2587c2c2c commit on github"): \[FrameworkBundle\] made all Router options configurable
  * [b890c34](http://github.com/symfony/symfony/commit/b890c3429df5e929d11af2dedebfec15a885c550 "b890c3429df5e929d11af2dedebfec15a885c550 commit on github"): \[FrameworkBundle\] fixed file detection and formatting in Code helper
  * [6317ddf](http://github.com/symfony/symfony/commit/6317ddfbe144ed9ca16928d9bf80e7b2e41714f1 "6317ddfbe144ed9ca16928d9bf80e7b2e41714f1 commit on github"): \[ZendBundle\] removed translator support
  * [a753790](http://github.com/symfony/symfony/commit/a7537906b4e6e370e5911448f41d6d2552f6832b "a7537906b4e6e370e5911448f41d6d2552f6832b commit on github"): \[Translation\] added the component
  * [d6f55c3](http://github.com/symfony/symfony/commit/d6f55c31d14db014a1596cdcfcce598985598e42 "d6f55c31d14db014a1596cdcfcce598985598e42 commit on github"): \[TwigBundle\] added helpers for translations
  * [d3aca1c](http://github.com/symfony/symfony/commit/d3aca1c04a102b1358cf8cf350764051adee94ab "d3aca1c04a102b1358cf8cf350764051adee94ab commit on github"): \[FrameworkBundle\] added support for the Translation component
  * [9580c74](http://github.com/symfony/symfony/commit/9580c74f0bb55fd837fe0745982630ac847d6c3a "9580c74f0bb55fd837fe0745982630ac847d6c3a commit on github"): \[Validator\] changed the convention for placeholders in messages to be compatible with Twig (from %limit% to {{ limit }})
  * [7072054](http://github.com/symfony/symfony/commit/707205410e1c95c176ee35db04c89e31610e9c43 "707205410e1c95c176ee35db04c89e31610e9c43 commit on github"): added an IdentityTranslator to make it possible to always relies on the translator service, even if none is configured
  * [9e50782](http://github.com/symfony/symfony/commit/9e50782b9d3b1724e2f9aca6515c773f6461cec0 "9e50782b9d3b1724e2f9aca6515c773f6461cec0 commit on github"): fixed request data collector
  * [4ac65ce](http://github.com/symfony/symfony/commit/4ac65cebcf69b78ba7560a78a81e2839d18a7861 "4ac65cebcf69b78ba7560a78a81e2839d18a7861 commit on github"): \[Translation\] renamed Range to Interval
  * [a6dc10c](http://github.com/symfony/symfony/commit/a6dc10c31ae78744ecd513263270f309651c42b0 "a6dc10c31ae78744ecd513263270f309651c42b0 commit on github"): changed templating name notation (old notation: bundle:section:name.format:renderer, where both format and renderer are optional; new notation: bundle:section:name.format.renderer, where only format is optional)
  * [6aa190b](http://github.com/symfony/symfony/commit/6aa190b2a6c61e1700a3375d4ed245774b8f111f "6aa190b2a6c61e1700a3375d4ed245774b8f111f commit on github"): \[OutputEscaper\] added SafeDecoratorInterface
  * [3b1e833](http://github.com/symfony/symfony/commit/3b1e83380b927017e6e9d2a8d88d67e78343c0ae "3b1e83380b927017e6e9d2a8d88d67e78343c0ae commit on github"): \[Validator\] removed the convention that error parameters are delimited with %%
  * [7b9a523](http://github.com/symfony/symfony/commit/7b9a523a43d9026de7725ad734a65774a60bfcbe "7b9a523a43d9026de7725ad734a65774a60bfcbe commit on github"), [6dc6d4a](http://github.com/symfony/symfony/commit/6dc6d4a7d3bbc101d700506e81b68c0dd8b66db0 "6dc6d4a7d3bbc101d700506e81b68c0dd8b66db0 commit on github"), [68bff2d](http://github.com/symfony/symfony/commit/68bff2d21460d222621f71c216e5ee9790cbfe53 "68bff2d21460d222621f71c216e5ee9790cbfe53 commit on github"): \[TwigBundle\] fixed trans tag
  * [4297609](http://github.com/symfony/symfony/commit/42976091563c59cd9c8f9f87e8c2a8dcdc3a4f40 "42976091563c59cd9c8f9f87e8c2a8dcdc3a4f40 commit on github"), [3ce8ad1](http://github.com/symfony/symfony/commit/3ce8ad17189e98596a7535c0139b1dd3e03727a3 "3ce8ad17189e98596a7535c0139b1dd3e03727a3 commit on github"): \[TwigBundle\] moved translator helpers to their own extension (removed usage of the magic _view variable context)
  * [eff1bdf](http://github.com/symfony/symfony/commit/eff1bdf50fa523eccb38e01b59747b09de2a3d87 "eff1bdf50fa523eccb38e01b59747b09de2a3d87 commit on github"): \[TwigBundle\] made trans and transchoice tags more flexible by accepting variables
  * [416bd78](http://github.com/symfony/symfony/commit/416bd7872ec7fb4df5676280414b7e41872b62d8 "416bd7872ec7fb4df5676280414b7e41872b62d8 commit on github"): \[TwigBundle\] optimized calls to helpers
  * [0fc8906](http://github.com/symfony/symfony/commit/0fc8906feb5865705dfd61c31e871420dcec2bd3 "0fc8906feb5865705dfd61c31e871420dcec2bd3 commit on github"): \[Validator\] forced all validation annotations to be in the validation namespace to avoid collisions, removed the need for the wrapping @Validation annotation

New [job postings](http://trac.symfony-project.com/trac/wiki/JobPostings)
----------------

  * Symfony Developer/LAMP Developer at [lighthousecatholicmedia.org](http://www.lighthousecatholicmedia.org) - full-time based in Sycamore, IL, USA - Contact: jeff.pipas [at] lighthousecatholicmedia.org

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfPropel15ActAsSignableBehavior](http://www.symfony-project.org/plugins/sfPropel15ActAsSignableBehaviorPlugin): adds support for "created_by", "updated_by" and "deleted_by" columns in your Propel 1.5.x model.
  * [sfDoctrineChoiceChain](http://www.symfony-project.org/plugins/sfDoctrineChoiceChainPlugin): provides a helpful sfWidgetFormDoctrineChoiceChain widget with the corresponding validator and module.
  * [brFormExtra](http://www.symfony-project.org/plugins/brFormExtraPlugin): widgets and validator suited for Brazilian users (sfWidgetFormChoiceUFBR, sfWidgetFormSelectCheckboxStates, sfValidatorCpfCnpj, sfValidatorChoiceStates, sfValidatori18nDate).
  * [sfToodledo](http://www.symfony-project.org/plugins/sfToodledoPlugin): a Toodledo API plugin.
  * [drTwitterFeed](http://www.symfony-project.org/plugins/drTwitterFeedPlugin): makes fetching status updates from a user by accessing the Twitter API really easy.

Updated plugins
---------------

  * [sfDatagrid](http://www.symfony-project.org/plugins/sfDatagridPlugin):
    * added list.formatter option into new admin generator

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * added toggle functions to groupinglistview
    * fixed ux.progresscolumn for IE7 not in quirksmode
    * removed hardcoded objectActions column header
    * progresscolumn tweaks
    * added config for objectActions
    * added config option to disable bottom_toolbar
    * started adding isDisabled and getExtends config methods to all javascript components
    * fixed ability to turn of rowstriping and trackmouseover with listview
    * rowactions tweaks
    * fixed some routing issues

  * [bhLDAPAuth](http://www.symfony-project.org/plugins/bhLDAPAuthPlugin):
    * updated security config file values

  * [lyMediaManager](http://www.symfony-project.org/plugins/lyMediaManagerPlugin):
    * added icons for audio and video assets

  * [sfTrafficCMS](http://www.symfony-project.org/plugins/sfTrafficCMSPlugin):
    * added output of title
    * added some SEO tweaks

  * [sfDoctrineJCroppable](http://www.symfony-project.org/plugins/sfDoctrineJCroppablePlugin):
    * force image quality of 95
    * fixed bug to not crop if image exactly right size already

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):

  * [tdVisualFactory](http://www.symfony-project.org/plugins/tdVisualFactoryPlugin):
    * fixed bug when adding image to a new album

  * [pmModuleEnabler](http://www.symfony-project.org/plugins/pmModuleEnablerPlugin):
    * fixed generator class

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * added external column sorting and multi sorting
    * added per action fieldsets and per action layout

  * [sfCryptoCaptcha](http://www.symfony-project.org/plugins/sfCryptoCaptchaPlugin):
    * added support for sf 1.3, 1.4

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * fixed slashes were allowed in media item slugs due to an undocumented feature of the Doctrine sluggable behavior
    * media item delete links now reference the item by id rather than by slug
    * extended the flexibility of _mediaItem so that it is behaves differently in indexSuccess
    * create a new apostrophe.mediaEmbeddableToggle() function that runs once in indexSuccess creating the behavior for the thumbnail to toggle the embeddable item
    * persistent global toolbar option in app.yml
    * media can now be edited with ajax
    * sdded tag/categories button
    * updated gradient on buttons to use white and not grey
    * made the description box smaller on the Media Item form and removed the lable
    * added visual feedback for replace file dialog
    * fixed a bug with linkAttributes and the ajax edit in place
    * added merging to aCategoryAdmin
    * renamed apostrophe.get_categorizables in PluginaCategoryForm to a.get_categorizables
    * cleaned up the media edit form
    * extended the media top bar through most of the Success views for consistency
    * abstracted uploadAllowed and embedAllowed to BaseaMediaTools so it can be used with aforementioned
    * Apostrophe now recognizes JPEGs with an EXIF orientation hint

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * getEngineCategories fix for when aPage.admin is null
    * renamed the category-related events for consistency with our other events


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [Generation One](http://generationone.org.au/): \(English\) Not for profit organisation set up to end the disparity between indigenous and non-indigenous Australians
  * [Küchen Atlas](http://www.kuechen-atlas.de): \(Deutsch\) Küchen Atlas Portal Betriebs GmbH, backend powered by Symfony


They talked about us
--------------------

  * [How to implement a flexible home page composition admin tool with LooseCoupling?](http://test.ical.ly/2010/09/27/symfony-workshop-how-to-implement-a-flexible-home-page-composition-admin-tool-with-loosecoupling/)
  * [Symfony2 podría retrasase hasta marzo](http://www.symfony.es/2010/09/27/symfony2-podria-retrasase-hasta-marzo/)
  * [Uporządkowane wysyłanie e-maili w projekcie symfony](http://xlab.pl/2010/09/uporzadkowane-wysylanie-e-maili-w-projekcie-symfony/)
  * [Deploying symfony projects to ServerGrove shared hosting accounts](http://blog.servergrove.com/2010/09/27/deploying-symfony-projects-to-servergrove-shared-hosting-accounts/)
  * [Generador de pruebas para modulos symfony](http://joaquinnunez.cl/blog/2010/09/27/generador-de-pruebas-para-modulos-symfony/)
  * [sfImageTransformExtraPlugin used on bikesoup.co.uk – first site I know of but haven’t been working on myself](http://test.ical.ly/2010/09/28/sfimagetransformextraplugin-used-on-bikesoup-co-uk-first-site-i-know-of-but-havent-been-working-on-myself/)
  * [Magic has a price, but it doesn't need to be your life](http://pooteeweet.org/blog/0/1835)
  * [gjPositionsPlugin – homepage composition in a nutshell. First iteration is done](http://test.ical.ly/2010/09/29/gjpositionsplugin-homepage-composition-in-a-nutshell-first-iteration-is-done/)
  * [Dynamic Propel/Doctrine connection](http://www.symfonylab.com/dynamic-propeldoctrine-connection/)
  * [Did you know that you can sort your doctrine relations by setting an orderBy option in your schema?](http://test.ical.ly/2010/09/30/did-you-know-that-you-can-sort-your-doctrine-relations-by-setting-an-orderby-option-in-your-schema/)
  * [Upgrading a Symfony2 application to PR3](http://blog.servergrove.com/2010/09/30/upgrading-a-symfony2-application-to-pr3/)
  * [Where to define ON DELETE CASCADE in your Doctrine schema.yml to avoid #1451 foreign key constraint fails](http://test.ical.ly/2010/10/01/where-to-define-on-delete-cascade-in-your-doctrine-schema-yml-to-avoid-1451-foreign-key-constraint-fails/)
  * [update record changes with sfDoctrineActAsSignablePlugin: Signable behavior](http://symfony-world.blogspot.com/2010/10/update-record-changes-with.html)
  * [MongoDB + Symfony – jak skorzystać ze świetnego NOSQL?](http://trylik.pl/mongodb-symfony-jak-skorzystac-ze-swietnego-nosql/)
  * [symfonyで携帯端末用のテンプレート切り替えを実装する](http://blog.loadlimits.info/2010/09/symfony%E3%81%A7%E6%90%BA%E5%B8%AF%E7%AB%AF%E6%9C%AB%E7%94%A8%E3%81%AE%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E5%88%87%E3%82%8A%E6%9B%BF%E3%81%88%E3%82%92%E5%AE%9F%E8%A3%85%E3%81%99/)
  * [PHPの開発フレームワーク、symfonyでの開発手順って、ぶっちゃけ、大雑把にいうと、こんなかんじ？ と思った（symfonyのバージョン、1.4）](http://blog.goo.ne.jp/xmldtp/e/366b52bafc812d5b5919761dc5d52cf4)
  * [Formulario de contacto](http://symfony.cl/blog/2010/09/formulario-de-contacto/)
  * [Autenticación LDAP en Symfony](http://www.congdegnu.es/2010/09/27/autenticacion-ldap-en-symfony/)
  * [Антипаттерны Symfony](http://symfony.info/2010/10/02/89/)
  * [Gource software version control visualization – Symfony 1.4](http://www.learnwebdev.com/?p=171)
  * [Symfony Tip: Decimals in your schema.yml](http://dev.bigandbest.com/symfony-tip-decimals-in-your-schemayml/)
  * [Nächste Woche: Symfony Day 2010 in Köln](http://www.ausgebloggt.de/2010/09/30/nachste-woche-symfony-day-2010-in-koln/)
  * [Symfony2 : Présentation et notions de base](http://www.berejeb.com/2010/09/symfony-2-presentation-et-notions-de-base/)
  * [Instalar y generar Proyecto en Symfony STEP III](http://es.debugmodeon.com/articulo/instalar-y-generar-proyecto-en-symfony-step-iii-configurando-apache-local-parte-1)
  * [Symfony использование миграций doctrine](http://allweeks.ru/2010/09/27/symfony-using-migrations/)
  * [Symfonyでの開発手順って、ぶっちゃけ、こんなかんじ？](http://www.edita.jp/tkagawa2/one/tkagawa260872055.html)
  * [symfonyでのプロジェクトの作成 | PHPプログラマのバリ・ポジ情報ブログ](http://www.propel.nn168.bytom.pl/315/symfony-php.html)
  * [Symfony: Comment corriger l’erreur « Can’t create table (errno: 150) »?](http://www.mcherifi.org/developpement-web/symfony/symfony-comment-corriger-lerreur-cant-create-table-errno-150.html)
  * [symfonyのアプリケーションの作成](http://blog.veryposi.info/programing/php/symfony-generate-app/)
  * [Actualización de Symfony 1.3.8 y 1.4.8](http://www.elcodigok.com.ar/2010/09/actualizacion-de-symfony-1-3-8-y-1-4-8/)
  * [Symfony2 Controller Testing](http://avalanche123.com/post/1215273326/symfony2-controller-testing)
