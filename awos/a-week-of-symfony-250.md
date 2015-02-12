---
layout: default
title: "A week of symfony #250 (10->16 October 2011)"
---

A week of symfony #250 (10->16 October 2011)
============================================

This week, all the Symfony2 components were included in [packagist.org](http://packagist.org/), a public repository for Composer, the package manager that soon will be used on Symfony2. Meanwhile, on the master branch of Symfony2 repository all the [HttpKernel event listeners were updated to implement EventSubscriberInterface](https://github.com/symfony/symfony/commit/beda03ba96b847fb6bcf2d7aed2893c978ec2565) and the official repository surpassed the 800 forks milestone.

Development mailing list
------------------------

  * [Standard Solution of serializing Doctrine Entity to json](https://groups.google.com/forum/#!topic/symfony-devs/GIOXA3GFspQ)
  * [\[Security\] ContextListener logic for persisting Tokens](https://groups.google.com/forum/#!topic/symfony-devs/ojLvh0WUbfo)

Symfony2 development highlights
-------------------------------

[Master branch changelog](http://github.com/symfony/symfony/commits/master):

  * [8f15794](http://github.com/symfony/symfony/commit/8f157942740b61a140997c3e2bfcb8326606e3b7 "8f157942740b61a140997c3e2bfcb8326606e3b7 commit on github"): moved LocaleListener and RouterListener to the HttpKernel component
  * [4539e5c](http://github.com/symfony/symfony/commit/4539e5c554e71d53ae6d4b3b48681fea60d0fd90 "4539e5c554e71d53ae6d4b3b48681fea60d0fd90 commit on github"): moved configuration of the default HTTP and HTTPS ports from RouterListener to RequestContext
  * [beda03b](http://github.com/symfony/symfony/commit/beda03ba96b847fb6bcf2d7aed2893c978ec2565 "beda03ba96b847fb6bcf2d7aed2893c978ec2565 commit on github"), [7a89d34](http://github.com/symfony/symfony/commit/7a89d34872e82fcc67efef7a709e8501351d6bac "7a89d34872e82fcc67efef7a709e8501351d6bac commit on github"): \[HttpKernel\] updated all HttpKernel event listeners to implement EventSubscriberInterface
  * [6e4269f](http://github.com/symfony/symfony/commit/6e4269f9eb944c879c563b701cbf203ac3a48056 "6e4269f9eb944c879c563b701cbf203ac3a48056 commit on github"), [3aa7582](http://github.com/symfony/symfony/commit/3aa75828b01149a8ea6fbe18f27d1fd27f96bd35 "3aa75828b01149a8ea6fbe18f27d1fd27f96bd35 commit on github"), [a2cf023](http://github.com/symfony/symfony/commit/a2cf023da1e3bc58cd1f3acae9d186cba0aea1dc "a2cf023da1e3bc58cd1f3acae9d186cba0aea1dc commit on github"): \[Form, TwigBridge, FrameworkBundle\] added the ability to specify the translation domain
  * [73312ab](http://github.com/symfony/symfony/commit/73312ab5e9321bb586fd2e7f7503b01554875969 "73312ab5e9321bb586fd2e7f7503b01554875969 commit on github"): \[Validator\] the Type constraint now accepts the Boolean type instead of boolean
  * [cc76da1](http://github.com/symfony/symfony/commit/cc76da1144bbeb57db6faafcfd2242e055276275 "cc76da1144bbeb57db6faafcfd2242e055276275 commit on github"): \[HttpKernel\] fixed file profile storage when trying to read an empty token
  * [5b69dae](http://github.com/symfony/symfony/commit/5b69dae9c8384a3e8c0cbc1a2ec5dc4fa44d05d3 "5b69dae9c8384a3e8c0cbc1a2ec5dc4fa44d05d3 commit on github"): \[HttpKernel\] fixed profiler file storage for children
  * [3ca1ccb](http://github.com/symfony/symfony/commit/3ca1ccbf6764de5e2d48b2ddabdd2f1eb7075459 "3ca1ccbf6764de5e2d48b2ddabdd2f1eb7075459 commit on github"): \[DoctrineBridge\] removed the Xml and Yaml driver as they are now part of Doctrine
  * [976f8b1](http://github.com/symfony/symfony/commit/976f8b10fa6bf4505cab6fcec07ff1d73a281994 "976f8b10fa6bf4505cab6fcec07ff1d73a281994 commit on github"): \[HttpKernel\] moved the Timer data collector to HttpKernel
  * [08285ed](http://github.com/symfony/symfony/commit/08285edef973a0c2392503ba499d761e086c49d2 "08285edef973a0c2392503ba499d761e086c49d2 commit on github"): \[SwiftmailerBundle\] fixed email display in the web profiler when the message is not in UTF-8

[2.0 branch changelog](http://github.com/symfony/symfony/commits/2.0):

  * [2270a4d](http://github.com/symfony/symfony/commit/2270a4da5ad24fec70142301ee01935efa2e78c9 "2270a4da5ad24fec70142301ee01935efa2e78c9 commit on github"): \[Bridge, Doctrine\] added a catch for when a developer uses the EntityType with multiple=false but on a hasMany relationship
  * [00cbd39](http://github.com/symfony/symfony/commit/00cbd398135b865478fa63278e667421368525c5 "00cbd398135b865478fa63278e667421368525c5 commit on github"), [d8dfca2](http://github.com/symfony/symfony/commit/d8dfca21f2a61861f3b00114d876210171be446c "d8dfca21f2a61861f3b00114d876210171be446c commit on github"): \[BrowserKit\] fixed cookie expiry discard when attribute contains capitals
  * [9d8046e](http://github.com/symfony/symfony/commit/9d8046e40739d275de3049283fe934f5de4ae98c "9d8046e40739d275de3049283fe934f5de4ae98c commit on github"): \[Doctrine\] UniqueValidator now works with associations


[New plugins](http://www.symfony-project.org/plugins/newest/)
-----------

  * [sfCacophony](http://www.symfony-project.org/plugins/sfCacophonyPlugin): implements OAuth with PECL OAuth extension (an alternative to sfMelodyPlugin)
  * [sfFacebookSlider](http://www.symfony-project.org/plugins/sfFacebookSliderPlugin): facebook slider

Updated plugins
---------------

  * [sfPEARcaptcha](http://www.symfony-project.org/plugins/sfPEARcaptchaPlugin):
    * fixed typo

  * [sfGuardSecure](http://www.symfony-project.org/plugins/sfGuardSecurePlugin):
    * tweaked allow_extra_fields

  * [dcReloadedFormExtra](http://www.symfony-project.org/plugins/dcReloadedFormExtraPlugin):
    * tweaks and fixes to chosen.js widgets
    * added the alWidgetFormTimepicker widget (wrapper for the jQueryUITimepicker) and the corresponding validator alValidatorTimepicker
    * updated README file to add timepicker explanations

  * [apostropheBlog](http://www.symfony-project.org/plugins/apostropheBlogPlugin):
    * fixed a user who was a member of the editor group but not able to edit any particular posts could edit all posts due to an empty whereIn() call

  * [apostrophe](http://www.symfony-project.org/plugins/apostrophePlugin):
    * made sure there's a full app environment (including invocation of the frontendConfiguration class configure method) in aSyncStaticFiles task
    * refactored a-admin generator filter styles
    * fixed validated type of file uploads persists properly for Office files
    * fixed mysql version of aTools::lock did not return a value properly


They talked about us
--------------------

  * [Open Sourcing LinkTuesday.com](http://www.leftontheweb.com/message/Open_Sourcing_LinkTuesdaycom)
  * [Konferenz zu beliebtem Framework: Symfony Day Cologne 2011](http://pressnetwork.de/konferenz-zu-beliebtem-framework-symfony-day-cologne-2011/)
  * [Silex, Twig und HTML5 BoilerPlate](http://nerdpress.org/2011/10/12/silex-twig-und-html5-boilerplate/)
  * [Open Source Is Powering Pretty Much Everything](http://www.efytimes.com/e1/creativenews.asp?edid=71133)
  * [Symfony 2 – Set Default Locale On Form Login #2](http://nerdpress.org/2011/10/13/symfony-2-set-default-locale-on-form-login-2/)
  * [A URL shortener in a couple of hours](http://www.leftontheweb.com/message/A_URL_shortener_in_a_couple_of_hours)
  * [La seguridad de utilizar Symfony2](http://www.symfony.es/2011/10/16/la-seguridad-de-utilizar-symfony2/)
  * [Symfony2 service container: how to make your service use tags](http://php-and-symfony.matthiasnoback.nl/2011/10/symfony2-service-container-how-to-make-your-service-use-tags/)
  * [Symfony2: How to create a UserProvider](http://php-and-symfony.matthiasnoback.nl/2011/10/symfony2-how-to-create-a-userprovider/)
  * [symfony + Doctrine でi18n](http://blog.44services.jp/?p=542)
  * [Symfony: sub-domains and front controllers](http://www.izazael.com/2011/10/symfony-sub-domains-and-front-controllers/)
  * [OpenPNE3　opFreepagePluginプラグインインストール時のエラー回避方法](http://select.rash.jp/op/710/)
  * [Symfony 2: Créer un utilisateur depuis un contrôleur avec FOSUB](http://www.dinduks.com/symfony-2-creer-un-utilisateur-depuis-un-controleur-avec-fosub)
  * [Is there a specific situation when to use a PHP micro-framework like Silex](http://test.ical.ly/2011/10/11/is-there-a-specific-situation-when-to-use-a-php-micro-framework-like-silex/)
