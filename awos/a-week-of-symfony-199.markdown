A week of symfony #199 (18->24 October 2010)
============================================

The symfony project celebrated this week its fith anniversary publishing the last major component of Symfony2 framework: the <a href="http://github.com/fabpot/symfony/commit/f216f313e8909015fe9961a5604d179f64c35a90">Security Component</a>. In addition, the Form and Validation components also received lots of commits and patches.
 
Development mailing list
------------------------

  * [Symfony2: forms and databinding](http://groups.google.com/group/symfony-devs/browse_thread/thread/9ac2eade1d4a1603)
  * [Functional test including a GET parameter](http://groups.google.com/group/symfony-devs/browse_thread/thread/937f10994a5829f6)
  * [Flash message best practice](http://groups.google.com/group/symfony-devs/browse_thread/thread/514d9653cf068725)
  * [Symfony2: some random thoughts about the new security layer](http://groups.google.com/group/symfony-devs/browse_thread/thread/cfba48ca5c4f756b)
  * [Improving integration of 3rd party Bundles](http://groups.google.com/group/symfony-devs/browse_thread/thread/e46e5bb74fc3a78b)

Symfony2 development highlights
-------------------------------

[Changelog](http://github.com/symfony/symfony/commits/master):

  * [ef4f61b](http://github.com/symfony/symfony/commit/ef4f61bb9fcbfcb5bd7c5a0e2340a8dd30db8651 "ef4f61bb9fcbfcb5bd7c5a0e2340a8dd30db8651 commit on github"): \[DependencyInjection\] added TaggedContainerInterface to signature of generated container classes
  * [5d4c80f](http://github.com/symfony/symfony/commit/5d4c80f27b68b8ac568e5bb0ca74b07aadcdbafd "5d4c80f27b68b8ac568e5bb0ca74b07aadcdbafd commit on github"): \[Validator\] removed DependencyInjection integration
  * [e1f8423](http://github.com/symfony/symfony/commit/e1f842344eedc796133f78dd6015c39507422926 "e1f842344eedc796133f78dd6015c39507422926 commit on github"), [7639fde](http://github.com/symfony/symfony/commit/7639fde3f247f28ccb85b3050478e3a0b97218b9 "7639fde3f247f28ccb85b3050478e3a0b97218b9 commit on github"): \[FrameworkBundle\] added a DIC tag-based constraint validator factory
  * [7225cf6](http://github.com/symfony/symfony/commit/7225cf64b1854753f6713664ac2a97ea6941f6dd "7225cf64b1854753f6713664ac2a97ea6941f6dd commit on github"), [c543692](http://github.com/symfony/symfony/commit/c543692891947a0ba694855ff3449e4501eab98c "c543692891947a0ba694855ff3449e4501eab98c commit on github"), [71ace34](http://github.com/symfony/symfony/commit/71ace348222348eda7bf0007ce2e4b6dfc0c6e51 "71ace348222348eda7bf0007ce2e4b6dfc0c6e51 commit on github"), [dbfa06c](http://github.com/symfony/symfony/commit/dbfa06c54feb81eecfc64d4e44447cbed5919df0 "dbfa06c54feb81eecfc64d4e44447cbed5919df0 commit on github"): added more unit tests
  * [2dc357d](http://github.com/symfony/symfony/commit/2dc357d3a8233672997240d6c619a9e4c28cd2c4 "2dc357d3a8233672997240d6c619a9e4c28cd2c4 commit on github"): \[WebProfilerBundle\] fixed label reference, fixed markup, optimized css and images
  * [4a18624](http://github.com/symfony/symfony/commit/4a186249275f4c8b410714f0b892e318fe22c238 "4a186249275f4c8b410714f0b892e318fe22c238 commit on github"): \[Validator\] removed ftp and ftps from default url protocols
  * [56d9830](http://github.com/symfony/symfony/commit/56d98305ca314c65ea9277f68f4c9892a35b4100 "56d98305ca314c65ea9277f68f4c9892a35b4100 commit on github"): fixed form field groups rendering
  * [94347f7](http://github.com/symfony/symfony/commit/94347f73c5bff3040410605eb5de02dd14c2e60a "94347f73c5bff3040410605eb5de02dd14c2e60a commit on github"): \[HttpFoundation\] added a way to generate a URI based on the current one and a path
  * [0fc6b15](http://github.com/symfony/symfony/commit/0fc6b15c1729035890cd137686f142b92c5f9650 "0fc6b15c1729035890cd137686f142b92c5f9650 commit on github"): \[HttpFoundation\] added a way to clear the session attributes
  * [f216f31](http://github.com/symfony/symfony/commit/f216f313e8909015fe9961a5604d179f64c35a90 "f216f313e8909015fe9961a5604d179f64c35a90 commit on github"), [82f8ab8](http://github.com/symfony/symfony/commit/82f8ab839f13c30beaf29bb256a3b01e9e0320fe "82f8ab839f13c30beaf29bb256a3b01e9e0320fe commit on github"), [4027f75](http://github.com/symfony/symfony/commit/4027f751e39c8e96f7f960df49e5ddde736a3d02 "4027f751e39c8e96f7f960df49e5ddde736a3d02 commit on github"): added the Security Component and its integration into the MVC framework
  * [71228b5](http://github.com/symfony/symfony/commit/71228b5f29321b78be71912d2ea2f354c9abc79a "71228b5f29321b78be71912d2ea2f354c9abc79a commit on github"): \[FrameworkBundle\] added a way to configure the logout paths
  * [4b32114](http://github.com/symfony/symfony/commit/4b321141f9b76eea4bbd4cce3f9f2cb1bf704f83 "4b321141f9b76eea4bbd4cce3f9f2cb1bf704f83 commit on github"): \[FrameworkBundle\] added a way to configure the switch-user behavior
  * [bdb0510](http://github.com/symfony/symfony/commit/bdb051083cc686832dc3359d7f2ec1504bafbab4 "bdb051083cc686832dc3359d7f2ec1504bafbab4 commit on github"): \[FrameworkBundle\] removed default controller for login
  * [dd4f87b](http://github.com/symfony/symfony/commit/dd4f87b8c24de204897926bcff478fc04865c140 "dd4f87b8c24de204897926bcff478fc04865c140 commit on github"): made form login configurable
  * [dd7e33a](http://github.com/symfony/symfony/commit/dd7e33af6bcb135d00fa008da0a0188713df615b "dd7e33af6bcb135d00fa008da0a0188713df615b commit on github"): \[TwigBundle\] fixed the include tag to behave like the standard Twig include tag
  * [0ccc980](http://github.com/symfony/symfony/commit/0ccc9805f54ca46d4ea9fdda026b0779e858c616 "0ccc9805f54ca46d4ea9fdda026b0779e858c616 commit on github"): fixed UniversalClassLoader issues with leading slashes
  * <del>[e8bcbcb](http://github.com/symfony/symfony/commit/e8bcbcba57b210246a1d6b5d0fcf688b0a2d8afc "e8bcbcba57b210246a1d6b5d0fcf688b0a2d8afc commit on github"): \[Routing\] allowed multiple routing requirement with xml loader</del>
  * [0749038](http://github.com/symfony/symfony/commit/0749038e73b0def26abfefa5cc40f30683c7b460 "0749038e73b0def26abfefa5cc40f30683c7b460 commit on github"): \[Security\] changed the way passwords are compared to avoid timing attacks
  * [acfd09e](http://github.com/symfony/symfony/commit/acfd09eeb31dbf8592da44e0d3aa1091fc6076db "acfd09eeb31dbf8592da44e0d3aa1091fc6076db commit on github"): \[FrameworkBundle\] generate a random password if none is provided in the configuration
  * [eaef939](http://github.com/symfony/symfony/commit/eaef939141b0b62cdbab9cba5271a1c486cbcdd7 "eaef939141b0b62cdbab9cba5271a1c486cbcdd7 commit on github"): \[Form\] changed value transformers to be responsible for processing empty values to be able to chain them properly (this change fixes the bug that DateField did not return NULL when submitted without values)
  * [733290c](http://github.com/symfony/symfony/commit/733290c112a86b7147b0c477d28bde6f74e702ef "733290c112a86b7147b0c477d28bde6f74e702ef commit on github"): \[Form\] implemented UrlField
  * [e4c2170](http://github.com/symfony/symfony/commit/e4c21708caedfaf7d3fc78a43003972ad7e66d9d "e4c21708caedfaf7d3fc78a43003972ad7e66d9d commit on github"): \[Form\] separated value transformers from normalization transformers
  * [6c7fab2](http://github.com/symfony/symfony/commit/6c7fab212b1f715945001ca95616877b6d70570e "6c7fab212b1f715945001ca95616877b6d70570e commit on github"): \[Form\] added validation of years, months and days to DateField
  * [72dcee5](http://github.com/symfony/symfony/commit/72dcee594a321a758bc5ee22c403ccdc0f32ddab "72dcee594a321a758bc5ee22c403ccdc0f32ddab commit on github"): \[Form\] added validation of hours, minutes and seconds to TimeField
  * [96a0bff](http://github.com/symfony/symfony/commit/96a0bff9151d45660cfda178142a7851b7a0cccc "96a0bff9151d45660cfda178142a7851b7a0cccc commit on github"): \[Form\] made InputField instantiable so that simple input fields can be created on the fly
  * [d077ac4](http://github.com/symfony/symfony/commit/d077ac415887b2b8561ce9604d876b57b646c455 "d077ac415887b2b8561ce9604d876b57b646c455 commit on github"): \[Security\] changed encoders to use hash() function whenever possible and replaced sha1 with sha256 as default algorithm


New [job postings](http://trac.symfony-project.com/trac/wiki/JobPostings)
----------------

  * Symfony developer at [openwaternet.com](http://www.openwaternet.com) - Contact: james.skarie [at] openwaternet.com

New [developers for hire](http://trac.symfony-project.com/trac/wiki/DevelopersForHire)
-----------------------

  * [http://www.singleton.mn](Singleton LLC): is a Mongolia-based web application development company, specialized in Web 2.0, eCommerce and Social application development.


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfFlattr](http://www.symfony-project.org/plugins/sfFlattrPlugin): makes it easy to integrate the Flattr service.
  * [sfSmartContext](http://www.symfony-project.org/plugins/sfSmartContextPlugin): simple SmartContext integration.
  * [sfAdTaily](http://www.symfony-project.org/plugins/sfAdTailyPlugin): simple AdTaily integration helper.
  * [sfAmazonS3](http://www.symfony-project.org/plugins/sfAmazonS3Plugin): allows you to connect to Amazon s3 services.
  * [zsDoctrineRecordBuilder](http://www.symfony-project.org/plugins/zsDoctrineRecordBuilderPlugin): helps you to build, create and stub records for testing purpose.
  * [sfJunaioBackend](http://www.symfony-project.org/plugins/sfJunaioBackendPlugin): is an application to manage Point Of Interest (POI) data. It serves as a management tool for the sfJunaioChannelPlugin.
  * [sfJunaioChannel](http://www.symfony-project.org/plugins/sfJunaioChannelPlugin): provides a channel for the Junaio Augmented Reality Browser.
  * [idlDoctrineMigration](http://www.symfony-project.org/plugins/idlDoctrineMigrationPlugin): provides two useful task to help managing your model migration. This is specially useful when multiple developers works on the same project.
  * [sfGemiusTraffic](http://www.symfony-project.org/plugins/sfGemiusTrafficPlugin): easily adds Gemius Traffic to your symfony project.

Updated plugins
---------------

  * [sfSocial](http://www.symfony-project.org/plugins/sfSocialPlugin):
    * fixed a bug in read messages

  * [acHostDependant](http://www.symfony-project.org/plugins/acHostDependantPlugin):
    * refactored code
    * added i18n host folder
    * added i18n section in README file
    * added config/settings.yml file

  * [ExtjsGenerator](http://www.symfony-project.org/plugins/ExtjsGeneratorPlugin):
    * added initial support for grid editing
    * added new checkcolumn ux from Extjs3.3.0
    * improved efficient of foreign field widgets
    * moved routing into routing.yml
    * reorganized the javascript includes
    * refactored ComponentMgr interceptors and component synchronous loading to remove the jit.js requirement
    * added ptype loading to the component loading
    * added extends configuration option to all extjs generated components
    * fixed bug with multiselect

  * [ddOnlineStore](http://www.symfony-project.org/plugins/ddOnlineStorePlugin):
    * minor fixes
    * added methods to ProductTable

  * [sfAssetsLibrary](http://www.symfony-project.org/plugins/sfAssetsLibraryPlugin):
    * fixed a bug on folder delete

  * [sfDoctrineAssetsLibrary](http://www.symfony-project.org/plugins/sfDoctrineAssetsLibraryPlugin):
    * sfAssetFolderTest and sfAssetTest work
    * changed sfPropelPlugin to sfDoctrinePlugin
    * fixed image path to sfAssetsLibraryPlugin
    * fixed getChildren in sfAsset module

  * [pmPropelGenerator](http://www.symfony-project.org/plugins/pmPropelGeneratorPlugin):
    * added _save_and_list action in generator

  * [sfGeshi](http://www.symfony-project.org/plugins/sfGeshiPlugin):
    * added sfGeshi::$ignore, which contains strings to be ignore while parsing
    * added sfGeshi::$methods, which contains name of methods for changing behaviour of Geshi object

  * [sfTangoIcons](http://www.symfony-project.org/plugins/sfTangoIconsPlugin):
    * added model class of icon sizes
    * modified the sequence of parameters
    * if size is not set, use the configuration. If configuration is not set, user small icons
    * added function to normalize icon size

  * [sfDoctrineActAsTaggable](http://www.symfony-project.org/plugins/sfDoctrineActAsTaggablePlugin):
    * it now uses the official jQuery UI autocomplete plugin rather than the old deprecated version found in sfJqueryReloadedPlugin

  * [sfFCKEditor](http://www.symfony-project.org/plugins/sfFCKEditorPlugin):
    * bugfixed custom config path handling

  * [sfI18nFormExtractor](http://www.symfony-project.org/plugins/sfI18nFormExtractorPlugin):
    * updated the tasks long description

  * [sfTaskExtra](http://www.symfony-project.org/plugins/sfTaskExtraPlugin):
    * excluded task classes from runtime autoloader

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * when you recrop something you have cropped before your existing settings are preserved properly
    * fixed setFlash error message that occurs when merging tags
    * combined engine widget and template widget via progressive enhancement
    * apostrophe:import-files now supports any filetype that is supported via the GUI
    * cleaned up help message, corrected description of what can be uploaded, fixed --verbose so it really works
    * added button helpers
    * updated the button slot to allow for descriptions and allow for link-only scenarios
    * created base classes for the Video slot
    * updated base classes for multiple slots so that they all use an options array() instead of passing the options individually
    * stopped using sfJqueryReloadedPlugin
    * refractored that 'Placeholder' box so that it's a single piece of shared code that lives with the choose button in aImageSlot
    * engine routes now support the relative_root_url factories.yml option to sfWebRequest
    * fixed our FCK widget not to apply the prefix URL twice
    * fixed some absolute image src URLs in templates

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * updated the sidebar filters so that they only allow you to filter by one item, Tags, Categories, Dates
    * moved apostrophe widgets to the apostrophe plugin
    * added param for adjusting the amount of blog / events displayed per page with indexSuccess


New [symfony powered websites](http://trac.symfony-project.org/wiki/ApplicationsDevelopedWithSymfony)
----------------------------

  * [Saitta](http://www.saitta.it): \(Italian\) Web Development, Safety, VOIP Avaya
  * [AllianceFrancaise](http://www.alliancefrancaise.trieste.it): \(French, Italian\) French Lesson, French Speacking Centification, Delf Dalf Examinations
  * [gowiro.it](http://www.gowiro.it): \(Italian\) e-commerce for natural pine oil and products for body and skin
  * [fruttaverduradaroccia.it](http://www.fruttaverduradaroccia.it): \(Italian\) health food: fruit and vegetables
  * [iptras.it](http://www.iptras.it): \(Italian\) e-commerce for office products, paper, Logistics
  * [saiudine.it](http://www.saiudine.it): \(Italian\) assurance


They talked about us
--------------------

  * [You Should Be Testing Your Symfony Plugins](http://brentertainment.com/2010/10/18/you-should-be-testing-your-symfony-plugins/)
  * [Symfony cumple 5 años](http://www.symfony.es/2010/10/18/symfony-cumple-5-anos/)
  * [Some helping hands when working with embedded doctrine relations in symfony forms](http://test.ical.ly/2010/10/19/some-helping-hands-when-working-with-embedded-doctrine-relations-in-symfony-forms/)
  * [symfony系列文章归档](http://www.foolbirds.com/symfony-archives.html)
  * [lyMediaManagerPlugin 0.5.6](http://www.lyra-cms.com/blog/2010/10/lymediamanagerplugin-0-5-6.html)
  * [How to create a custom admin theme for the symfony/doctrine admin generator](http://test.ical.ly/2010/10/20/how-to-create-a-custom-admin-theme-for-the-symfonydoctrine-admin-generator/)
  * [History of frameworks](http://www.symfonylab.com/history-of-frameworks/)
  * [Enforcing unique key constraints with Doctrine ODM for MongoDB & Symfony2](http://blog.servergrove.com/2010/10/20/enforcing-unique-key-constrains-with-doctrine-odm-for-mongodb-symfony-2/)
  * [Symfony plugin for Flattr](http://vvv.tobiassjosten.net/symfony/symfony-plugin-for-flattr)
  * [More on debugging the saving process of a symfony/doctrine form](http://test.ical.ly/2010/10/22/more-on-debugging-the-saving-process-of-a-symfony-doctrine-form/)
  * [Konfiguracja projektu w symfony pod Test Driven Development](http://xlab.pl/2010/10/konfiguracja-projektu-w-symfony-pod-test-driven-development/)
  * [Keep a trim autoloader](http://kriswallsmith.net/post/1389089654/keep-a-trim-autoloader)
  * [Symfony Eclipse integration plugin](http://blog.o-x-t.com/2010/10/24/symfony-eclipse-integration-plugin/)
  * [Symfony and Doctrine: Behaviors](http://dsyph3r.blogspot.com/2010/10/symfony-and-doctrine-behaviors_24.html)
  * [Symfony 1.4, Doctrine and the csDoctrineActAsGeolocateablePlugin Example](http://www.fragmentedcode.com/2010/10/23/symfony-14-doctrine-csdoctrineactasgeolocateableplugin/)
  * [symfony Day 2010](http://www.learnwebdev.com/?p=270)
  * [Un blog en Symfony](http://clementguillemain.com/2010/533/un-blog-en-symfony.html)
  * [get installed plugin in symfony](http://www.meteenee.com/get-installed-plugin-in-symfony)
  * [Imagemagick sfThumbnail Plugin Fix for Scaling under Symfony](http://chris.sedlmayr.co.uk/archives/49-imagemagick-sfthumbnail-plugin-fix-for-scaling-under-symfony/)
