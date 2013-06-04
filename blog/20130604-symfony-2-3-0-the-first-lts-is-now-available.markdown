Symfony 2.3.0 - 最初のLTS（長期サポート） - がリリースされました
================================================================

[原文](http://symfony.com/blog/symfony-2-3-0-the-first-lts-is-now-available)

Symfony バージョン 2 で最初のLTS（長期サポート）リリースとなる Symfony 2.3.0 がリリースされました。

Symfony で採用した[リリースプロセス](http://symfony.com/doc/current/contributing/community/releases.html)では、6 ヶ月ごとに新しいリリースを行います。これらのメンテナンス期間は 8 ヶ月です。2 年に 1 度、[LTS](http://symfony.com/doc/current/contributing/community/releases.html#long-term-support-releases) バージョンをリリースします。LTS バージョンは 3 年間メンテナンスを行います。

これにより、小さなチームやアジャイル企業は 6 ヶ月ごとにフレームワークのアップグレード（2 ヶ月の移行期間）を行い、より大きなチームや大企業では 3 年ごとにアップグレードを行う（1 年の移行期間）ことができます。
2.3.0 は Symfony2 で最初の LTS リリースです。2016 年 5 月まで、このバージョンのメンテナンスを行います。

統計
----

Symfony 2.3 向けにはプルリクエストが 437 件あり、1,260 個のコミットが 50 名の開発者から送られました。ドキュメントに対しては 839 個のコミットが 44 名の編集者から送られました。
3 ヶ月で 1,260 件のコミットということは、平均すると 1 日あたり 14 コミットが行われたことになります。437 件のプルリクエストは 1 日あたり 5 件がマージされたことになります。これは新記録です！

機能
----

 - DomCrawler: [相対スキーマ URL](http://symfony.com/blog/new-in-symfony-2-3-domcrawler-enhancements#schema-relative-urls)
 - DomCrawler: [HTML5 フォーム](http://symfony.com/blog/new-in-symfony-2-3-domcrawler-enhancements#html5-forms)
 - Console: [Console コンポーネントでのイベント](http://symfony.com/blog/new-in-symfony-2-3-events-in-the-console-component)
 - Console: [プログレスヘルパーの改善](http://symfony.com/blog/new-in-symfony-2-3-great-new-features-in-the-console-component#progress-helper-enhancements)
 - Console: [テーブルヘルパー](http://symfony.com/blog/new-in-symfony-2-3-great-new-features-in-the-console-component#tablehelper)
 - Console: [Console 出力におけるフォーマットの追加](http://symfony.com/blog/new-in-symfony-2-3-great-new-features-in-the-console-component#console-output-in-more-formats)
 - Console: [警告表示レベルの追加](http://symfony.com/blog/new-in-symfony-2-3-great-new-features-in-the-console-component#more-verbosity-levels)
 - HttpFoundation: [信頼するプロキシの設定にサブネットを使用](http://symfony.com/blog/new-in-symfony-2-3-use-sub-networks-to-configure-trusted-proxies)
 - Validator: [新しいバリデーター](http://symfony.com/blog/new-in-symfony-2-3-new-validators)
 - Validator: [比較バリデーター](http://symfony.com/blog/new-in-symfony-2-3-what-else#comparison-validators)
 - Form: [フォームのボタンサポート](http://symfony.com/blog/new-in-symfony-2-3-buttons-support-in-forms)
 - Dependency Injection: [Lazy サービス](http://symfony.com/blog/new-in-symfony-2-3-what-else#lazy-services)
 - Dependency Injection: [Synchronized サービス](http://symfony.com/blog/new-in-symfony-2-3-what-else#synchronized-services)
 - CssSelector: [CSS セレクタのリファクタリング](http://symfony.com/blog/new-in-symfony-2-3-what-else#css-selector)
 - Intl: [国際化のリファクタリング](http://symfony.com/blog/new-in-symfony-2-3-what-else#internationalization)
 - Debug: [Fatal Error ロギング](http://symfony.com/blog/new-in-symfony-2-3-what-else#fatal-error-logging)
 - Standard Edition: [parameters.yml をインタラクティブに編集](http://symfony.com/blog/new-in-symfony-2-3-interactive-management-of-the-parameters-yml-file)
 - その他多数の改善点

Symfony 2.3 には、2 つの新しいコンポーネントと 1 つの新しいブリッジが追加されました。

 - [Debug コンポーネント](http://symfony.com/blog/new-in-symfony-2-3-new-debug-component)
 - [Intl コンポーネント](http://symfony.com/doc/current/components/intl.html)
 - [proxy manager ブリッジ](http://symfony.com/doc/master/components/dependency_injection/lazy_services.html)

アップグレード
--------------

2.2 から 2.3 へのアップグレードは簡単です。
Symfony Standard Edition では、いくつかのバンドルがライセンスの問題のため削除されました。2.3 以降では、Standard Edition に同梱されるコードと、直接依存するコードのすべてが MIT 系のライセンスになっています。composer.json ファイルの diff は次のとおりです。

    diff --git a/composer.json b/composer.json
    index c2d7588..5705d76 100644
    --- a/composer.json
    +++ b/composer.json
    @@ -1,32 +1,35 @@
     {
         "name": "symfony/framework-standard-edition",
    +    "license": "MIT",
    +    "type": "project",
         "description": "The \"Symfony Standard Edition\" distribution",
         "autoload": {
             "psr-0": { "": "src/" }
         },
         "require": {
             "php": ">=5.3.3",
    -        "symfony/symfony": "2.2.*",
    -        "doctrine/orm": "~2.2,>=2.2.3",
    +        "symfony/symfony": "2.3.*",
    +        "doctrine/orm": ">=2.2.3,<2.4-dev",
             "doctrine/doctrine-bundle": "1.2.*",
             "twig/extensions": "1.0.*",
    -        "symfony/assetic-bundle": "2.1.*",
    -        "symfony/swiftmailer-bundle": "2.2.*",
    -        "symfony/monolog-bundle": "2.2.*",
    -        "sensio/distribution-bundle": "2.2.*",
    -        "sensio/framework-extra-bundle": "2.2.*",
    -        "sensio/generator-bundle": "2.2.*",
    -        "jms/security-extra-bundle": "1.4.*",
    -        "jms/di-extra-bundle": "1.3.*"
    +        "symfony/assetic-bundle": "2.3.*",
    +        "symfony/swiftmailer-bundle": "2.3.*",
    +        "symfony/monolog-bundle": "2.3.*",
    +        "sensio/distribution-bundle": "2.3.*",
    +        "sensio/framework-extra-bundle": "2.3.*",
    +        "sensio/generator-bundle": "2.3.*",
    +        "incenteev/composer-parameter-handler": "~2.0"
         },
         "scripts": {
             "post-install-cmd": [
    +            "Incenteev\\ParameterHandler\\ScriptHandler::buildParameters",
                 "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::buildBootstrap",
                 "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::clearCache",
                 "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::installAssets",
                 "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::installRequirementsFile"
             ],
             "post-update-cmd": [
    +            "Incenteev\\ParameterHandler\\ScriptHandler::buildParameters",
                 "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::buildBootstrap",
                 "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::clearCache",
                 "Sensio\\Bundle\\DistributionBundle\\Composer\\ScriptHandler::installAssets",
    @@ -36,12 +39,15 @@
         "config": {
             "bin-dir": "bin"
         },
    -    "minimum-stability": "alpha",
    +    "minimum-stability": "stable",
         "extra": {
             "symfony-app-dir": "app",
             "symfony-web-dir": "web",
    +        "incenteev-parameters": {
    +            "file": "app/config/parameters.yml"
    +        },
             "branch-alias": {
    -            "dev-master": "2.2-dev"
    +            "dev-master": "2.3-dev"
             }
         }
     }

以前のバージョンからの後方互換レイヤーはすべて削除されています。UPGRADE ファイルを確認し、コードをすべて移行してください。2.3 リリースにおける変更点は、[UPGRADE ドキュメント](https://github.com/symfony/symfony/blob/2.3/UPGRADE-2.3.md)にある移行方法を参照してください。

インストール
------------

Symfony 2.3 のフルスタックフレームワークを使って新規プロジェクトを開始するには、いくつかの方法があります。

 - （推奨）Composer で新規プロジェクトを作成する。

      $ php composer.phar create-project symfony/framework-standard-edition somewhere/ 2.3.0``


 - Symfony Standard Edition のアーカイブを[ダウンロード](http://symfony.com/download)する。

詳しくは、インストールドキュメントも参照してください。

 - [Symfony のインストールと設定](http://docs.symfony.gr.jp/symfony2/book/installation.html)


アプリケーションで Symfony コンポーネントを使っている場合は、2.3.0 バージョン、もしくは 2.3 ブランチを使うように切り替えます。

 - [Composer パッケージ](https://packagist.com/packages/symfony)から

 - GitHub から
   https://github.com/symfony/{COMPONENT_NAME}/archive/v2.3.0.zip.


