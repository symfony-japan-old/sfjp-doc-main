A week of symfony #214 (31 January -> 6 February 2011)
======================================================

Symfony2 boosted its development activity this week, just before the first Symfony Live 2011 conference in San Francisco. A [new SecurityBundle](https://github.com/symfony/symfony/commit/e645090423a037912ac5e0c43bc3ea104998fa2a) was introduced, class loading was moved to its own component and the Form and Validator components were vastly revamped. In addition, the first version of the [config normalizer](http://github.com/symfony/symfony/commit/b484763a7a331d68504b5b047c733ab076d266b9) was committed, although [symfony community showed no consensus](https://groups.google.com/forum/#!topic/symfony-devs/3nwwiUaT4ds) about it yet.
 
Development mailing list
------------------------

  * [\[Symfony2\] Yaml-only app config?](https://groups.google.com/forum/#!topic/symfony-devs/rjrWWYyrkRI)
  * [The directory structure does not work for model](https://groups.google.com/forum/#!topic/symfony-devs/a9nm721Ga4w)
  * [\[RFC\] Automatic class compilation](https://groups.google.com/forum/#!topic/symfony-devs/Of6FXk-wICM)
  * [\[Symfony2\] Explicit factory-class property for service definitions](https://groups.google.com/forum/#!topic/symfony-devs/6cMns13edtg)
  * [Bundle\ category for the Symfony namespace](https://groups.google.com/forum/#!topic/symfony-devs/AXI8nK4BQPw)
  * [RFC and update on Extension refactoring](https://groups.google.com/forum/#!topic/symfony-devs/3nwwiUaT4ds)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [fb889a2](http://github.com/symfony/symfony/commit/fb889a2eee33db42ba5ec6af8e5c142f2c2b6d63 "fb889a2eee33db42ba5ec6af8e5c142f2c2b6d63 commit on github"), [cd96c91](http://github.com/symfony/symfony/commit/cd96c914477fb8ee2640cf98e72a0468570a515f "cd96c914477fb8ee2640cf98e72a0468570a515f commit on github"): replaced some var_export() with json_encode() for better readability
  * [57ae50e](http://github.com/symfony/symfony/commit/57ae50e8942f1a3ee9431c320b404fc1b016b87c "57ae50e8942f1a3ee9431c320b404fc1b016b87c commit on github"): \[Security\] many improvements and fixes
  * [e645090](http://github.com/symfony/symfony/commit/e645090423a037912ac5e0c43bc3ea104998fa2a "e645090423a037912ac5e0c43bc3ea104998fa2a commit on github"): moved security related things to a new SecurityBundle (the Security component is left unchanged)
  * <del>[24c7715](http://github.com/symfony/symfony/commit/24c7715029548164f93fd671d1e3009ce590637a "24c7715029548164f93fd671d1e3009ce590637a commit on github"): \[DoctrineBundle\] created DIC params for security user provider EM/DM aliases</del>
  * [75404e6](http://github.com/symfony/symfony/commit/75404e6bd642f831efe4b976a83f7143183d99d7 "75404e6bd642f831efe4b976a83f7143183d99d7 commit on github"): renamed HttpKernel/Cache/ namespace to HttpKernel/HttpCache/
  * [cf64d2c](http://github.com/symfony/symfony/commit/cf64d2cfe7f348b6ed8dd5504f7052b5b3cbe61d "cf64d2cfe7f348b6ed8dd5504f7052b5b3cbe61d commit on github"): changed Security Component namespaces
  * [ff34f7d](http://github.com/symfony/symfony/commit/ff34f7d2816813bb1a2a2d4512e71ba11a2b1636 "ff34f7d2816813bb1a2a2d4512e71ba11a2b1636 commit on github"): \[DoctrineMongoDBBundle\] added support for multiple document managers
  * [0219ec3](http://github.com/symfony/symfony/commit/0219ec3dbcb497b469d254c3f16c9ca124cf2a46 "0219ec3dbcb497b469d254c3f16c9ca124cf2a46 commit on github"): \[DependencyInjection\] added missing methods in ContainerInterface
  * [7bd3039](http://github.com/symfony/symfony/commit/7bd30398c66c2397e3157bd886ed0583eb8ef049 "7bd30398c66c2397e3157bd886ed0583eb8ef049 commit on github"): \[FrameworkBundle\] moved some cache warmers
  * [42f9c55](http://github.com/symfony/symfony/commit/42f9c556a35af616d3239df64f42c15b98602472 "42f9c556a35af616d3239df64f42c15b98602472 commit on github"), [6997fba](http://github.com/symfony/symfony/commit/6997fbac0d4019aed2747efeb504dea0419bff6f "6997fbac0d4019aed2747efeb504dea0419bff6f commit on github"), [95e10b3](http://github.com/symfony/symfony/commit/95e10b3ed9642332547e26739c3f10a1ae81e7b4 "95e10b3ed9642332547e26739c3f10a1ae81e7b4 commit on github"): moved the class loader to its own component
  * [8ccb8eb](http://github.com/symfony/symfony/commit/8ccb8eb8c2c8a1aec2aa042366353476ca8af728 "8ccb8eb8c2c8a1aec2aa042366353476ca8af728 commit on github"): added security.interactive_login and security.switch_user events
  * [db81828](http://github.com/symfony/symfony/commit/db818284afce20c20d495422738aa797151fd429 "db818284afce20c20d495422738aa797151fd429 commit on github"): moved class compiled in cache to the FrameworkBundle
  * [2509c9d](http://github.com/symfony/symfony/commit/2509c9da4b33645f35d4bc672aa832d745d3b8be "2509c9da4b33645f35d4bc672aa832d745d3b8be commit on github"): added an autoloader that uses a class map (a class in Symfony2 can be loaded by four different mechanisms: bootstrap.php, classes.php, MapFileClassLoader and UniversalAutoloader)
  * [3c9c43d](http://github.com/symfony/symfony/commit/3c9c43d59286c46149a5f6c4bbf1ed912749d644 "3c9c43d59286c46149a5f6c4bbf1ed912749d644 commit on github"): \[DoctrineBundle\] added support to configure DBAL Types through the dbal configuration section
  * [6337506](http://github.com/symfony/symfony/commit/63375060e829b4dc2d1354250650f5d0723884aa "63375060e829b4dc2d1354250650f5d0723884aa commit on github"): \[DoctrineBundle\] refactored doctrine-1.0.xsd
  * [224e66f](http://github.com/symfony/symfony/commit/224e66f77b889db2630aa66206efba1c522da97e "224e66f77b889db2630aa66206efba1c522da97e commit on github"), [98c1056](http://github.com/symfony/symfony/commit/98c1056fbfd3a3ab3cbdc6fffc1a59929671733c "98c1056fbfd3a3ab3cbdc6fffc1a59929671733c commit on github"): \[HttpFoundation\] added static Request::fromGlobals() (the Request constructor no longer uses values from PHP's super globals. Your front controllers will need to be updated)
  * [803dd58](http://github.com/symfony/symfony/commit/803dd58002b7bb80d90a1cc09ee3112c05e58c5e "803dd58002b7bb80d90a1cc09ee3112c05e58c5e commit on github"): added definition inheritance support
  * [0c3ca26](http://github.com/symfony/symfony/commit/0c3ca26e6e660045a0a09b4f14b8c45f99a1c565 "0c3ca26e6e660045a0a09b4f14b8c45f99a1c565 commit on github"): \[Validator\] implemented traversing of \Traversable objects using the @Valid constraint
  * [ce61baf](http://github.com/symfony/symfony/commit/ce61baf7178c20d52b0889ad762e26fe4f9b0f42 "ce61baf7178c20d52b0889ad762e26fe4f9b0f42 commit on github"): \[Form\] ChoiceField now accepts closures in the 'choices' option
  * [34865a3](http://github.com/symfony/symfony/commit/34865a35330daeccfedf02f24cb3724473d1ce1e "34865a35330daeccfedf02f24cb3724473d1ce1e commit on github"): \[Form\] added a field guess for AssertType('\DateTime') constraint
  * [ebd2ca6](http://github.com/symfony/symfony/commit/ebd2ca6cfe77543c8bcd06435d87902f5f765aa3 "ebd2ca6cfe77543c8bcd06435d87902f5f765aa3 commit on github"): \[Form\] moved option 'empty_value' to ChoiceField. An empty value is displayed if the field is not required.
  * [62d52d8](http://github.com/symfony/symfony/commit/62d52d8015b0ec90077a1f5302feb58e00121651 "62d52d8015b0ec90077a1f5302feb58e00121651 commit on github"): enabled normalizeConfig() to handle irregular plural forms
  * [bdbfb44](http://github.com/symfony/symfony/commit/bdbfb44a96765a8b3d2a0898996160c1a2cc1c13 "bdbfb44a96765a8b3d2a0898996160c1a2cc1c13 commit on github"), [5014ee9](http://github.com/symfony/symfony/commit/5014ee9739d7cb741afd81371bec97f089698d44 "5014ee9739d7cb741afd81371bec97f089698d44 commit on github"): \[DoctrineBundle\] cleanup of the Command namespace in DoctrineBundle
  * [c4a2fb4](http://github.com/symfony/symfony/commit/c4a2fb41ec32af5c3fd4ecd944a75950808dc0c7 "c4a2fb41ec32af5c3fd4ecd944a75950808dc0c7 commit on github"): \[DoctrineBundle\] shortened Dependency Injection Fixture namespace to avoid Windows filepath length error
  * [65eb70d](http://github.com/symfony/symfony/commit/65eb70d3b6373ace7ba85df404e88795cf9b5fa7 "65eb70d3b6373ace7ba85df404e88795cf9b5fa7 commit on github"): \[Kernel\] tweaked bundle management
  * [e23f39c](http://github.com/symfony/symfony/commit/e23f39c42fd3b1e113d08c24bfdfefd53ad66dfb "e23f39c42fd3b1e113d08c24bfdfefd53ad66dfb commit on github"): \[Security\] config refactoring
  * [8a87953](http://github.com/symfony/symfony/commit/8a879531bdd2a4e79c51d5dcb310cecb1d80c650 "8a879531bdd2a4e79c51d5dcb310cecb1d80c650 commit on github"): \[Security\] added key normalization, and removed some conditionals
  * [2539da5](http://github.com/symfony/symfony/commit/2539da5e6a05851be9bbc7ad1b4eb7906185b4db "2539da5e6a05851be9bbc7ad1b4eb7906185b4db commit on github"): \[Security\] added AbstractFactory
  * [f2a3135](http://github.com/symfony/symfony/commit/f2a3135bd0644fa58b884d50ee4320a63e0c8029 "f2a3135bd0644fa58b884d50ee4320a63e0c8029 commit on github"): \[Security\] made a unique name required for each firewall
  * [025e142](http://github.com/symfony/symfony/commit/025e142dd474aacad7629ba5eb939f61979b7c70 "025e142dd474aacad7629ba5eb939f61979b7c70 commit on github"): removed parameter converters as decided during IRC meeting (supported is still provided by FrameworkExtraBundle)
  * [5f11e49](http://github.com/symfony/symfony/commit/5f11e49d0bfa32e28da75556e1dacad37fa548e8 "5f11e49d0bfa32e28da75556e1dacad37fa548e8 commit on github"): \[HttpKernel\] made exceptions more robust (avoid too deep nested arrays PHP errors)
  * [5e5b6f0](http://github.com/symfony/symfony/commit/5e5b6f0cf82b22b9d187b538829aaf0d42539b3d "5e5b6f0cf82b22b9d187b538829aaf0d42539b3d commit on github"): \[HttpKernel\] made sure that parent bundles are registered before their descendants
  * [b7a0f71](http://github.com/symfony/symfony/commit/b7a0f71b8745dba38be28e41c98c307b9f69f70f "b7a0f71b8745dba38be28e41c98c307b9f69f70f commit on github"): \[FrameworkBundle\] added more file to the class cache when using the PHP templating engine
  * [d1cd442](http://github.com/symfony/symfony/commit/d1cd442361bf16f1c5227ee495cbf0b549455928 "d1cd442361bf16f1c5227ee495cbf0b549455928 commit on github"): \[FrameworkBundle\] added session listener for test environment
  * [b52e282](http://github.com/symfony/symfony/commit/b52e28243d37435d88bd658e61b8cc0b77039d7a "b52e28243d37435d88bd658e61b8cc0b77039d7a commit on github"): \[HttpFoundation\] added ApacheRequest
  * [839cb02](http://github.com/symfony/symfony/commit/839cb027a66836505e856bd146702fb52c710781 "839cb027a66836505e856bd146702fb52c710781 commit on github"): \[HttpKernel\] added a bootstrap file for HTTP cache front controllers
  * [2c43554](http://github.com/symfony/symfony/commit/2c4355460e19f52ea0c1f94e91a810f7b1ad1382 "2c4355460e19f52ea0c1f94e91a810f7b1ad1382 commit on github"): \[HttpKernel\] added a StoreInterface
  * [347c069](http://github.com/symfony/symfony/commit/347c069e8d8b810726aed2688ca2a2fbab1e6926 "347c069e8d8b810726aed2688ca2a2fbab1e6926 commit on github"): \[DoctrineBundle, Form\] implemented EntityChoiceField
  * [3bf9f77](http://github.com/symfony/symfony/commit/3bf9f7782debd42bc1cd050ea0b51ef14fbf8e17 "3bf9f7782debd42bc1cd050ea0b51ef14fbf8e17 commit on github"): \[DoctrineBundle, Form\] implemented EntityFieldFactoryGuesser
  * [d152b5e](http://github.com/symfony/symfony/commit/d152b5e265541b3cde746d7ad0c59dd8d6255259 "d152b5e265541b3cde746d7ad0c59dd8d6255259 commit on github"): \[Form\] moved Doctrine2 specific files
  * [57cbd57](http://github.com/symfony/symfony/commit/57cbd572658a2169b4dfe409096852edb91422a7 "57cbd572658a2169b4dfe409096852edb91422a7 commit on github"): \[Form\] fields may now be anonymous, but anonymous fields must not be added to groups
  * [4fcb985](http://github.com/symfony/symfony/commit/4fcb98547ce20f2e1e3bfe5be52af29355974e51 "4fcb98547ce20f2e1e3bfe5be52af29355974e51 commit on github"): \[Form\] simplified Form::bind(), added convenience methods Form::bindRequest() and Form::bindGlobals()
  * [c468db5](http://github.com/symfony/symfony/commit/c468db5c5bfdba26d67ca842544b59354768d752 "c468db5c5bfdba26d67ca842544b59354768d752 commit on github"): \[Form\] merged classes FieldGroup and Form for simplicity
  * [fdbc064](http://github.com/symfony/symfony/commit/fdbc064f0610b548f015f87bacdfe71485abe62e "fdbc064f0610b548f015f87bacdfe71485abe62e commit on github"): \[Form\] removed automatic distribution of the locale in the Form component
  * [e5ed98c](http://github.com/symfony/symfony/commit/e5ed98c324819a134490455a6ee5d2d49ece744e "e5ed98c324819a134490455a6ee5d2d49ece744e commit on github"): \[Form\] added option 'data' to Field for populating a field with a fixed value
  * [fb1f991](http://github.com/symfony/symfony/commit/fb1f99137dc023d63bc7022c4788009155efa139 "fb1f99137dc023d63bc7022c4788009155efa139 commit on github"): \[Form\] changed semantics of a bound form (a form now always has to be bound, independent of whether the request is a POST request or not)
  * [a28151a](http://github.com/symfony/symfony/commit/a28151a8afd0ec11231663e1633cfd8a406df837 "a28151a8afd0ec11231663e1633cfd8a406df837 commit on github"): \[Form\] removed FormFactory and improved the form instantiation process
  * [b484763](http://github.com/symfony/symfony/commit/b484763a7a331d68504b5b047c733ab076d266b9 "b484763a7a331d68504b5b047c733ab076d266b9 commit on github"): \[DependencyInjection\] added first version of the config normalizer (this is mainly intended for complex configurations to ease the work you have with normalizing different configuration formats, such as YAML, XML, and PHP)
  * [e6dc155](http://github.com/symfony/symfony/commit/e6dc155e89f8273263d7df06e00e367423b821cc "e6dc155e89f8273263d7df06e00e367423b821cc commit on github"): fixed validator class metadata warning
  * [628a4d1](http://github.com/symfony/symfony/commit/628a4d1fd8f5e9a65bdea6adfaf43e691cea5c89 "628a4d1fd8f5e9a65bdea6adfaf43e691cea5c89 commit on github"): \[Form\] refactored validation logic into validate() method. Removed bindGlobals() to reduce API clutter
  * [4f0283a](http://github.com/symfony/symfony/commit/4f0283a508c26b3bf1f761b587eb1d2bf65a86fe "4f0283a508c26b3bf1f761b587eb1d2bf65a86fe commit on github"): \[Form\] removed Form::isBound(). Form::bind() is only a shortcut method now, use Form::isSubmitted() if you want to find out whether a form was submitted
  * [c923af2](http://github.com/symfony/symfony/commit/c923af287956c7acad12ff111c23609f72f88432 "c923af287956c7acad12ff111c23609f72f88432 commit on github"): \[Form\] adapted constructor of CollectionField to match the constructors of the other fields
  * [5e3fab2](http://github.com/symfony/symfony/commit/5e3fab214e286816bd199d86e075e8caae69ecbb "5e3fab214e286816bd199d86e075e8caae69ecbb commit on github"): \[Form\] the form is now validated seperatedly from its data
  * [7c9c7af](http://github.com/symfony/symfony/commit/7c9c7af863e355904c4eeab4de57f331bc87bbe1 "7c9c7af863e355904c4eeab4de57f331bc87bbe1 commit on github"): \[Form\] fixed arrays not to be passed to the validator
  * [5ed4d91](http://github.com/symfony/symfony/commit/5ed4d91bb864e5209938270918af95aaee5d900d "5ed4d91bb864e5209938270918af95aaee5d900d commit on github"): \[Validator\] implemented Execute constraint
  * [1a34743](http://github.com/symfony/symfony/commit/1a34743990c464b0d73d8b6aecf1d4da0145a332 "1a34743990c464b0d73d8b6aecf1d4da0145a332 commit on github"): \[Validator\] fixed Collections annotated with @Valid may contain scalar values
  * [39c1481](http://github.com/symfony/symfony/commit/39c148197f3c4f8efb4e6534259619f473292b69 "39c148197f3c4f8efb4e6534259619f473292b69 commit on github"): \[Form\] fixed form validation (separated validation of data and form had serious drawbacks)
  * [c05fb03](http://github.com/symfony/symfony/commit/c05fb03c7db973df27111434fa9643d0e130ddcc "c05fb03c7db973df27111434fa9643d0e130ddcc commit on github"): \[HttpKernel\] changed the core.view event to only be notified when the controller does not return a Response
  * [2d69369](http://github.com/symfony/symfony/commit/2d69369c69e8481c16b086341a5967a034f84e4a "2d69369c69e8481c16b086341a5967a034f84e4a commit on github"): \[ClassLoader\] added the possibility to define more than one directory for a namespace or a prefix
  * [b6f400a](http://github.com/symfony/symfony/commit/b6f400a2bc2cea1cd4fcc71b2ac66518d885328b "b6f400a2bc2cea1cd4fcc71b2ac66518d885328b commit on github"): \[DependencyInjection\] made an optimization on dumped DIC
  * [f4282ee](http://github.com/symfony/symfony/commit/f4282eea98a3cd3ec349116cd7be4b3be0beb026 "f4282eea98a3cd3ec349116cd7be4b3be0beb026 commit on github"): \[Routing\] added support for non-standard port numbers in absolute urls
  * [ea536b0](http://github.com/symfony/symfony/commit/ea536b0d9ee17ef60cd3940c88ee2b7ee3dbf26b "ea536b0d9ee17ef60cd3940c88ee2b7ee3dbf26b commit on github"): \[FrameworkBundle\] added cache warmer priority
  * [3ed4711](http://github.com/symfony/symfony/commit/3ed47114d6d447107e992941b8c866072978ec72 "3ed47114d6d447107e992941b8c866072978ec72 commit on github"), [f455700](http://github.com/symfony/symfony/commit/f455700b88b557e19c05b3408a771cc1fe6d2827 "f455700b88b557e19c05b3408a771cc1fe6d2827 commit on github"): \[Bundle\] made getPath() less error prone by allowing both backward and forward slashes
  * [710a1e5](http://github.com/symfony/symfony/commit/710a1e56b0ef5682b616ac1cd1b44844d6883421 "710a1e56b0ef5682b616ac1cd1b44844d6883421 commit on github"): \[TwigBundle\] added support for template as Twig_Template instances
  * [1e3dc14](http://github.com/symfony/symfony/commit/1e3dc1479ce2c064947dd9d10a65c655ee49076f "1e3dc1479ce2c064947dd9d10a65c655ee49076f commit on github"): \[Testing, HttpKernel\] added possibility to functional test raw body data
  * [7f6fc6f](http://github.com/symfony/symfony/commit/7f6fc6f0fbd442ee0c49673b42b5fcc8ac6824fa "7f6fc6f0fbd442ee0c49673b42b5fcc8ac6824fa commit on github"): \[TwigBundle\] fixed form template inheritance

Documentation
-------------

  * New <a href="http://trac.symfony-project.org/wiki/SfLiveSfHackday2011">Symfony Live - San Francisco Hackday 2011</a>, and <a href="http://trac.symfony-project.org/wiki/IRCLogs20110203">IRC Logs 2011-02-03</a> pages

New [job postings](http://trac.symfony-project.com/trac/wiki/JobPostings)
----------------

  * Symfony developer at [Rettet den Regenwald e.V.](http://www.regenwald.org) - full-time based in Hamburg, Germany - Contact: tobias [at] regenwald [dot] org
  * Symfony developer at [iqcleverkaufen](http://www.iqcleverkaufen.de/) - full-time based in Minsk, Belarus - Contact: rabota [at] iqcleverkaufen [dot] com

New [developers for hire](http://trac.symfony-project.com/trac/wiki/DevelopersForHire)
-----------------------

  * Amin Vijay \(vijay.virtueinfo@gmail.com\): India-based web developer with 7 years professional experience, 3 years hands-on experience with Symfony 1.0+ (and occasional project contributer), Strong PHP/MySQL/Linux application development expertise, a diverse skillset and several Symfony-based applications in production.


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [chat](http://www.symfony-project.org/plugins/chatPlugin): (no description)
  * [sfDoctrineFileStorage](http://www.symfony-project.org/plugins/sfDoctrineFileStoragePlugin): Doctrine behavior that provides an easy way to work with files, uploads and images.
  * [urAdminTheme](http://www.symfony-project.org/plugins/urAdminThemePlugin): allows some new options for admin generation: layout, row Level credentials and context level credentials.
  * [mbpDistributedCache](http://www.symfony-project.org/plugins/mbpDistributedCachePlugin): enables cross-application cache clearing on distributed servers (e.g. a cluster) that share a common database.

Updated plugins
---------------

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * added mtWidgetFormWrapper, dcWidgetI18nNumberInput, mtValidatorDateExtended and dcValidatorI18nDecimal

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * added list variable

  * [sfPropel15](http://www.symfony-project.org/plugins/sfPropel15Plugin):
    * added js escaping in sfWidgetFormSchemaOptional
    * added options to new related form
    * fixed wrong comment in js code
    * updated externals to use Propel 1.5.6
    * added propel:diff, propel:status, propel:up, propel:down and propel:migrate tasks
    * enhanced filter embedded forms with criteria

  * [sfPinba](http://www.symfony-project.org/plugins/sfPinbaPlugin):
    * check context before use for tests

  * [pmModelUtils](http://www.symfony-project.org/plugins/pmModelUtilsPlugin):
    * now choices are translated using _translate_ function

  * [sfReCaptcha](http://www.symfony-project.org/plugins/sfReCaptchaPlugin):
    * added support for AJAX to the HTML generator helper function

  * [sfProjectAnalyser](http://www.symfony-project.org/plugins/sfProjectAnalyser):
    * allowed plugin.to_ignore to ignore some plugins

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * fixed a crash if the blog post has no author
    * fixed styling conflicts with next / prev arrows in the date browsing
    * added the getRichTextForAreas call to the blog plugin
    * added a singular wrapper for the blog getRichTextForArea
    * fixed admins were losing their ownership upon saving of the blog post form because the list of allowed authors did not contain them
    * author and category filters are now alphabetically sorted
    * you can now filter by "No Author" and by "Uncategorized"
    * a blog post or event with no author displays that fact in a reasonable way
    * author and category filters can be combined with other filters properly
    * Google Calendar URLs should now work in every case because I've put a character limit rather than a word limit on the length of the summary and made it conservative enough that we don't wind up with 2,048+ byte URLs
    * aBlogItem::getTextForArea now has an options parameter, which is passed on to aString::limitWords, allowing you to specify an alternate ellipsis or the 'characters' option

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * fixed the "crop corners stuck in upper left of image" bug on first crop
    * created a wrapper around getAreaBasicHTML() for the getRichTextforArea() call that is the preferred name for this method
    * rescoped media selecting js so that you can click on the title also to make your selection
    * file slot now allows filtering by type, and lists only types that are downloadable
    * images can be selected successfully for a file slot (this downloads the original of the image)
    * moved jquery.jplayer into the /js/plugins folder, added it to the JS in BaseaTools, made sure to use_helper(a) in the partials
    * added jquery.scrollTo for the Cropper
    * aString::limitWords now has a 'characters' option, which can be used to limit by characters rather than words


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [TimeHive](http://github.com/thaberkern/timehive): \(English\) webbased project timetracking software

New [symfony bloggers](http://trac.symfony-project.com/trac/wiki/SymfonyBloggers)
--------------------

  * [Rich Sage](http://www.richsage.co.uk/category/symfony) \([feed](http://www.richsage.co.uk/category/symfony/feed)\) \(English\)
  * [Sylvain Deloux](http://www.sylvaindeloux.com/blog/tag/symfony) \([feed](http://feeds.feedburner.com/sylvaindeloux_symfony)\) \(French\)

They talked about us
--------------------

  * [Symfony2 Showcase](http://xlab.pl/2011/01/symfony2-showcase/)
  * [A positive note](http://laurent.bachelier.name/2011/01/a-positive-note/)
  * [Symfony2, PhpBB4 and Drupal8](http://www.jnieto.org/article/symfony2_phpbb4_and_drupal8)
  * [Symfony 2 &amp; Facebook: первый проект](http://habrahabr.ru/blogs/symfony/103707/)
  * [Организация работы с git submodules](http://habrahabr.ru/blogs/symfony/60860/)
  * [Тестирование контроллера в Symfony2](http://habrahabr.ru/blogs/symfony/105361/)
  * [Announcement: Symfony2 application deployment infraestructure released](http://blog.liip.ch/archive/2011/02/02/announcement-symfony2-application-deployment-infrastructure-released.html)
  * [How Can I Write This Query Using An ORM?](http://propel.posterous.com/how-can-i-write-this-query-using-an-orm)
  * [4 ways to encode a variable number of parameters in a URL using symfony routing](http://test.ical.ly/2011/02/03/4-ways-to-encode-a-variable-number-of-parameters-in-a-url-using-symfony-routing/)
  * [First Sourcecode of TimeHive online](http://www.symfony-zone.com/wordpress/2011/02/03/first-sourcecode-of-timehive-online/)
  * [Symfony Live Paris 2011](http://www.programmez.com/actualites.php?titre_actu=Symfony-Live-Paris-2011&amp;id_actu=8977)
  * [Doctrine migrations gotchas in Symfony](http://vvv.tobiassjosten.net/symfony/doctrine-migrations-gotchas-in-symfony)
  * [symfttpd 1.1.0 released](http://laurent.bachelier.name/2011/02/symfttpd-1-1-0-released/)
  * [Participa en el Hacking Weekend de Symfony2](http://www.symfony.es/2011/02/04/participa-en-el-hacking-weekend-de-symfony2/)
  * [Why Symfony2 already rocks](http://blog.servergrove.com/2011/02/04/why-symfony2-already-rocks/)
  * [sfSagePayPlugin – a work in progress](http://www.richsage.co.uk/2011/01/30/sfsagepayplugin-a-work-in-progress/)
  * [Ouvrir un fichier dans eclipse v2](http://blog.lombardot.fr/2011/02/05/ouvrir-un-fichier-dans-eclipse-v2/)
  * [Symfony2 .. bumpy ride for some](http://pooteeweet.org/blog/0/1875#m1875)
  * [Using CKeditor as AJAX](http://www.symfonylab.com/using-ckeditor-as-ajax/)
  * [[symfony][php]ECサイトをリニューアルオープン](http://d.hatena.ne.jp/brtRiver/20110206/1297005727)
  * [Practical symfony 2日目：プロジェクト](http://d.hatena.ne.jp/Chisei/20110206/p1)
  * [Instalando Synfony en Windows XP con Sandbox](http://ernesto-casique.blogspot.com/2011/02/instalando-synfony-en-windows-xp-con.html)
  * [Symfony 1.4 guardar y mostrar html de la base de datos](http://developyourdream.blogspot.com/2011/02/symfony-14-guardar-y-mostrar-html-de-la_04.html)
  * [[自宅鯖][Ubuntu]Ubuntu10.10 自宅サーバ構築手順:SNS(ソーシャル・ネットワーキング・サービス:OpenPNE3)の導入](http://d.hatena.ne.jp/absj31/20110205/1296848554)
  * [On Symfony2](http://abcphp.com/Articles/on-symfony2/)
  * [Jak uruchmoć projekt symfony na dowolnym hostingu bez shella?](http://bloger.arcode.pl/blog1.php/2011/02/04/jak-uruchmoa-263-projekt-symfony-na-dowolnym-hostingu-bez-shella)
  * [Zend Framework Tool Usage With Command Line Tool Support](http://blogs.jetbrains.com/webide/2011/02/zend-framework-tool-usage-with-command-line-tool-support/)
  * [symfony.vim demo movie2](http://www.learnwebdev.com/?p=580)
  * [symfony1.x+propel1.3+MySQL5.1/5.5で生成したSQLのCreate TableがType=InnoDBで失敗する場合の対処法](http://akimoto.jp/blog/2011/02/03/propel-mysql55-sql-error-on-type-innodb/)
  * [Symfonyのコマンド覚書](http://sand-clock.heteml.jp/blog/?p=98)
  * [家庭用ゲームのプログラマーがSNSゲームのプログラマーに転職するために必要なもの](http://labs.unoh.net/2011/02/post_152.html)
  * [Usar Helpers nas Tasks](http://dicas-symfony.blogspot.com/2011/02/usar-helpers-nas-tasks.html)
  * [Für Symfony einen eigenen Captcha schreiben](http://www.stefan-kuehn.com/2011/02/fur-symfony-einen-eigenen-captcha.html)
  * [Why Use a PHP Framework? The Benefits Explained](http://www.articles4.us/2011/01/why-use-a-php-framework-the-benefits-explained/)