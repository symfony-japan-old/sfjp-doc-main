A week of symfony #246 (12->18 September 2011)
==============================================

[Symfony 1.4.14 was released](http://symfony.com/blog/symfony-1-4-14-released) this week, containing several enhancements and fixes proposed by community members. Meanwhile, the official [Symfony2 repository](https://github.com/symfony/symfony/) surpassed the 3,000th watcher milestone.
 
Development mailing list
------------------------

  * [Doctrine query in custom class](https://groups.google.com/forum/#!topic/symfony-devs/ANhemHPnFXk)

symfony 1 development highlights
--------------------------------

[Changelog](http://trac.symfony-project.com/trac/timeline?from=18%2F09%2F2011&daysback=6&milestone=on&ticket=on&changeset=on&update=Update):

  * [r33021](http://trac.symfony-project.org/changeset/33021 "33021 revision on trac"): \[1.4\] fixed sfCacheSessionStorage does not serialize properly, also uses wrong option name for httponly
  * [r33022](http://trac.symfony-project.org/changeset/33022 "33022 revision on trac"): \[1.4\] fixed auto_link_text() when an email address is already linked
  * [r33025](http://trac.symfony-project.org/changeset/33025 "33025 revision on trac"): \[1.4\] fixed sfCacheSessionStorage does not always check whether HTTP_USER_AGENT is set
  * [r33026](http://trac.symfony-project.org/changeset/33026 "33026 revision on trac"): \[1.4\] made sfCacheSessionStorage class code faster
  * [Milestone 1.4.14 completed](http://trac.symfony-project.org/milestone/1.4.14)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [aecfd0a](http://github.com/symfony/symfony/commit/aecfd0a8917370edd237120352749141ffa85362 "aecfd0a8917370edd237120352749141ffa85362 commit on github"): \[HttpFoundation\] support user and password in url
  * [e6e5146](http://github.com/symfony/symfony/commit/e6e5146ccba6ac80f6a3823ff6ce89bb3667aa39 "e6e5146ccba6ac80f6a3823ff6ce89bb3667aa39 commit on github"): \[Translation\] now support ResourceBundle
  * [cfc202b](http://github.com/symfony/symfony/commit/cfc202be93f98a0addf0e907b45b73566265c897 "cfc202be93f98a0addf0e907b45b73566265c897 commit on github"), [27dcc18](http://github.com/symfony/symfony/commit/27dcc187f6f4eacfefee4fad908212d31c75153b "27dcc187f6f4eacfefee4fad908212d31c75153b commit on github"): bumped versions of Twig and Swiftmailer
  * [73c8d2b](http://github.com/symfony/symfony/commit/73c8d2ba744d8a74df512f730a67e8c9f8a123c6 "73c8d2ba744d8a74df512f730a67e8c9f8a123c6 commit on github"): \[Form\] fixed error bubbling for Date and Time types when rendering as multiple choices
  * [53b4cd8](http://github.com/symfony/symfony/commit/53b4cd8c9c963c9f6cea41a1fd68a118dd0f7870 "53b4cd8c9c963c9f6cea41a1fd68a118dd0f7870 commit on github"): \[FrameworkBundle\] made code more robust
  * [400159d](http://github.com/symfony/symfony/commit/400159de4f1d2ace9eefa77962e7cb1f95d3ea37 "400159de4f1d2ace9eefa77962e7cb1f95d3ea37 commit on github"), [fabec37](http://github.com/symfony/symfony/commit/fabec37edcc8f34eeff82fbf84ef0fdf9ea4f2d9 "fabec37edcc8f34eeff82fbf84ef0fdf9ea4f2d9 commit on github"): \[FrameworkBundle\] made DIC placeholders replacement in route defaults only when the parameter exists in the container
  * [f9ecdfe](http://github.com/symfony/symfony/commit/f9ecdfeb0559448c598294b5740fdb3b4213ca13 "f9ecdfeb0559448c598294b5740fdb3b4213ca13 commit on github"): \[FrameworkBundle\] added sc parameters replacement in route requirements
  * [c5e0c80](http://github.com/symfony/symfony/commit/c5e0c80a76e78994e0d6e6fed07091c01349a04c "c5e0c80a76e78994e0d6e6fed07091c01349a04c commit on github"): \[HttpFoundation\] made FileBinaryMimeTypeGuesser command configurable
  * [c985ffa](http://github.com/symfony/symfony/commit/c985ffaa99fcdc6baa6eb94a2dd059cf2428aac4 "c985ffaa99fcdc6baa6eb94a2dd059cf2428aac4 commit on github"): \[Translation\] fixed message selector when the message is empty
  * [c50a3a1](http://github.com/symfony/symfony/commit/c50a3a194d5d2d1108aa32df830b9107039b4416 "c50a3a194d5d2d1108aa32df830b9107039b4416 commit on github"): \[Translation\] fixed transchoice when used with a fallback
  * [79710ed](http://github.com/symfony/symfony/commit/79710edb8abeda71b0991669cbd5059385aaf241 "79710edb8abeda71b0991669cbd5059385aaf241 commit on github"), [9ffd8ca](http://github.com/symfony/symfony/commit/9ffd8ca99c32cb0d463ea56a59bf61ecce7e0e22 "9ffd8ca99c32cb0d463ea56a59bf61ecce7e0e22 commit on github"): \[Translation\] added a MessageCatalogue::defines() method to check if a string has a translation (but without taking into account the fallback mechanism)
  * [5526072](http://github.com/symfony/symfony/commit/5526072dba59602d4eb11a2695fa925dc975ecde "5526072dba59602d4eb11a2695fa925dc975ecde commit on github"): \[Translation\] added support for more than one fallback locale
  * [9fb15c7](http://github.com/symfony/symfony/commit/9fb15c7cb2a48588cec40d78b9d6c6482bc9f1e3 "9fb15c7cb2a48588cec40d78b9d6c6482bc9f1e3 commit on github"): \[Process\] workaround a faulty implementation of is_executable on Windows
  * [43b55ef](http://github.com/symfony/symfony/commit/43b55efd04d26396043cab0b3525a4051e219dee "43b55efd04d26396043cab0b3525a4051e219dee commit on github"): \[Locale\] added support for yy format in StubIntlDateFormatter
  * [bede420](http://github.com/symfony/symfony/commit/bede42065eb528eaeab52dc509e34da0df1d0823 "bede42065eb528eaeab52dc509e34da0df1d0823 commit on github"): \[Config\] fixed FileResource usage of is_file (we must use file_exists here as the resource can be a file or a directory)
  * [046a125](http://github.com/symfony/symfony/commit/046a125ef763bb909103c1506b48692cde175e78 "046a125ef763bb909103c1506b48692cde175e78 commit on github"): \[FrameworkBundle\] set the file storage as default storage for Symfony2
  * [0826d1c](http://github.com/symfony/symfony/commit/0826d1c717c5e35ee9840ae5b38844ab727c6a1c "0826d1c717c5e35ee9840ae5b38844ab727c6a1c commit on github"): \[WebProfilerBundle\] added a way to filter logs by priority

[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [DoctrineJSONColumnBehavior](http://www.symfony-project.org/plugins/DoctrineJSONColumnBehaviorPlugin): provides a Doctrine behavior to ease the manipulation of columns that store values as JSON.
  * [cpAddressableDoctrine](http://www.symfony-project.org/plugins/cpAddressableDoctrinePlugin): defines an 'Addressable' behavior.

Updated plugins
---------------

  * [sfSwiftMailerExtended](http://www.symfony-project.org/plugins/sfSwiftMailerExtendedPlugin):
    * added extended logging

  * [cpAws](http://www.symfony-project.org/plugins/cpAwsPlugin):
    * updated video mime types

  * [sfTaskLogger](http://www.symfony-project.org/plugins/sfTaskLoggerPlugin):
    * fixed event dispatcher object in order to avoid core log messages

  * [sfAssetsLibrary](http://www.symfony-project.org/plugins/sfAssetsLibraryPlugin):
    * fixed TinyMCE popup navigation issues

  * [cpTcpdf](http://www.symfony-project.org/plugins/cpTcpdfPlugin):
    * added support for 'fill' param in generateTable
    * updated watermark printing

They talked about us
--------------------

  * [Symfony2\SecurityBundle](http://habrahabr.ru/blogs/symfony/128159/)
  * [Adding a task/command in Symfony2](http://shout.setfive.com/2011/09/09/adding-a-taskcommand-in-symfony2/)
  * [Prezentacja o Symfony2 i oprogramowaniu dedykowanym na InternetBeta 2011 w Rzeszowie](http://blog.sznapka.pl/prezentacja-o-symfony2-i-oprogramowaniu-dedykowanym-na-internetbeta-2011-w-rzeszowie/)
  * [http://www.kamiladryjanek.com/2009/10/symfony-12-i-extjs-wyswietlanie-danych-w-gridzie/](http://toni.uebernickel.info/development/behavior-driven-development-in-symfony2-with-behat-mink-and-zombie-js/)
  * [Countdown: Noch wenige Wochen bis zum Symfony Day Cologne](http://relevant.at/wirtschaft/pr/238197/countdown-noch-wenige-wochen-bis-zum-symfony-day-cologne.story)
  * [[Symfony 2] Twig – Global Variables](http://nerdpress.org/2011/09/12/symfony-2-twig-global-variables/)
  * [Первый трениг по Symfony2 на Украинских просторах – Я иду!](http://451f.com.ua/symfony2-training-kiev/388)
  * [Faire un formulaire de recherche avec Symfony2](http://www.clever-age.com/veille/blog/faire-un-formulaire-de-recherche-avec-symfony2.html)
  * [Propel 1.6.2 is Released](http://propel.posterous.com/propel-162-is-released)
  * [国外十大最流行PHP框架排名](http://fantanwu.tk/index.php/article/java/2011-09-18/20673.html)
  * [symfony: Błąd When using the attribute ATTR_AUTO_ACCESSOR_OVERRIDE you cannot use the field name](http://blog.kowalczyk.cc/2011/09/16/symfony-blad-when-using-the-attribute-attr_auto_accessor_override-you-cannot-use-the-field-name/)
  * [Le helper format_date de symfony](http://www.petitstrucs.fr/2011/09/le-helper-format_date-de-symfony/)
  * [Mini Curso Symfony Tecsul 2011](http://fabriciokerber.blogspot.com/2011/09/mini-curso-symfony-tecsul-2011.html)
  * [让 symfony 的应用程序支持 i18n 国际化](http://www.cheungfei.com/?p=8640)
  * [【php】【symfony】【doctrine】各種マニュアルを読んでみる(6日目)](http://kichon.net/blog/?p=1959)
  * [KnpPaginatorBundle with JQuery partial postback](http://0hlsson.se/2011/09/14/knppaginatorbundle-with-jquery-partial-postback/)
  * [CentOS: PHP PEAR and Symfony installation using source package](http://acsenthil.wordpress.com/2011/09/15/centos-php-pear-and-symfony-installation-using-source-package/)
  * [Symfony2 translating validator messages](http://inchoo.net/tools-frameworks/symfony2-translating-validator-messages/)
  * [Частичное сохранение многоязычных форм Symfony 1.4 в стиле python django-multilingual](http://ajc.su/web-razrabotka/php/chastichnoe-soxranenie-mnogoyazychnyx-form-symfony-1-4-v-stile-python-django-multilingual/)
  * [Symfony: Propel Custom Query](http://synt4x3rr0r.blogspot.com/2011/09/symfony-propel-custom-query.html)
  * [Symfony 2.0: Embedded Forms for Collections](http://www.scott-sherwood.com/?p=90)
  * [2.0 からはじめる MongoDB - 第0回 #mongodbjp](http://blog.madapaja.net/2011/09/20-mongodb-0.html)
  * [Symfony2: от Новичка до Ниндзя](http://symfony.org.ua/2011/09/training-symfony2-ukraine/)
  * [Конференция Symfony Camp UA 2011](http://www.smartme.com.ua/konferenciya-symfony-camp-ua-2011/)
  * [Symfony2のススメ1.5 ～コンポーネントちょい話～](http://tech.ecnavi.co.jp/archives/4536275.html)
  * [Introducing the Los Angeles Symfony User Group](http://www.phpframeworks.com/news/p/33082/introducing-the-los-angeles-symfony-user-group)
  * [Create a Symfony Super-Task that Runs Other Tasks](http://www.ozonesolutions.com/programming/2011/09/create-a-symfony-super-task-that-runs-other-tasks/)
