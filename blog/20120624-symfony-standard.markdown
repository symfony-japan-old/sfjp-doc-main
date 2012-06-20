Symfony スタンダード・エディション
==================================

Symfony スタンダード・エディションへようこそ。Symfony スタンダード・エディションは、完全に動く Symfony2 アプリケーションで、新しくウェブサイトを作る際のスケルトンとして使用することができます。

このドキュメントでは、Symfony2 のダウンロード方法、インストール方法、そして Symfony の始め方を説明します。より詳細な説明は、 Symfony のドキュメントの  [Installation][1] の章を参照してください。

1) スタンダード・エディションをインストールする
-----------------------------------------------

Symfony スタンダード・エディションをインストールするには以下のいくつかの方法があります。

### Composer を使用する (*推奨*)

Symfony は、依存関係を管理するために  [Composer][2] を使用しています。新しくプロジェクトを作成する際には、この Composer の使用を推奨します。

Composer をまだダウンロードしていなければ、 http://getcomposer.org/ の説明に沿ってダウンロードするか、次のコマンドを実行してください。

    curl -s http://getcomposer.org/installer | php

そして、 create-project コマンドを使用して Symfony アプリケーションを生成します。


    composer.phar create-project symfony/framework-standard-edition path/to/install

Composer は `path/to/install` ディレクトリ以下に Symfony2 と全ての依存関係のあるパッケージをインストールします。

### アーカイブファイルをダウンロードする

簡単に Symfony の動作をテストするには、スタンダード・エディションの [アーカイブ][3] をダウンロードして、ウェブサーバのルートディレクトリ以下などに展開することもできます。

“without vendors” のアーカイブをダウンロードする際には、全ての依存関係のあるパッケージをインストールする必要があります。その際には、上記の説明にあったように Composer をダウンロードして次のコマンドを実行してください。:

    php composer.phar install

2) システム設定をチェックする
-----------------------------

設定を始める前に、あなたのローカルのシステム上で Symfony が正しく動作するかチェックします。次の２つのチェックをしてください。

まず、コマンドラインから `check.php` スクリプトを実行してください。:

    php app/check.php

そして、ブラウザからも `config.php` スクリプトにアクセスしてください。:

    http://localhost/path/to/symfony/app/web/config.php

Warning や Recommendation が表示された際には、次に進む前に修正してください。

3) デモアプリケーションをブラウズする
-------------------------------------

おめでとうございます！ここまでくれば、Symfony を使用する準備ができました。

`config.php` のページから　”Bypass Configuration and go to the Welcome page” のリンクをクリックして、最初の Symfony のページをロードします。 

また、 `config.php` ページの “Configure Application online” リンクをクリックすれば、ウェブベースのコンフィギュレーターを使用することもできます。

実際に動作する Symfony のアクションを見るには、次のページへアクセスしてみてください。:

    web/app_dev.php/demo/hello/Fabien

4) Symfony を始める
-------------------

このディストリビューションは、あなたの Symfony アプリケーションのスターティングポイントとなります。また、少しサンプルコードが付いてきており、学び、遊ぶことができます。

Symfony を学び始めるのに [Quick Tour][4] を見るのが良いでしょう。 Quick Tour では、 Symfony2 の基本的な機能を全て網羅しています。

学習してみて準備ができたら、 公式の [Symfony2 book][5] を読み進めてください。

デフォルトのバンドルである `AcmeDemoBundle` で Symfony2 の動作を確認することができます。それでいくつか遊んで試したら、次のステップでこの AcmeDemoBundle を削除することができます。:

  * `src/Acme` ディレクトリを削除する

  * `app/config/routing_dev.yml` にある AcmeBundle を参照しているルーティングのエントリを削除する

  * `app/AppKernel.php` 内の登録されているバンドルから AcmeBundle を削除する

  * `web/bundles/acmedemo` ディレクトリを削除する

  * `app/config/config.yml` 内のセキュリティコンフィグレーションのインクルードを削除する（ `- { resource: security.yml}` の行を削除する）、もしくは、あなたのアプリケーションのニーズにフィットするセキュリティコンフィグレーションに修正する。


Symfony スタンダード・エディションの中身
----------------------------------------

Symfony スタンダード・エディションは次のデフォルトを使用するように設定されています。:

  * Twig がテンプレートエンジンとして設定されています

  * Doctrine ORM/DBAL が設定されています

  * Swiftmailer が設定されています

  * 全てのアノテーションが有効になっています。

そして、次のバンドルを設定してあります。:

  * **FrameworkBundle** - Symfony のコアフレームワークバンドル

  * [**SensioFrameworkExtraBundle**][6] - テンプレートとルーティングにアノテーション機能を追加するなどいくつかの便利な機能を追加

  * [**DoctrineBundle**][7] - Doctrine ORM のサポートを追加

  * [**TwigBundle**][8] - Twig テンプレートエンジンのサポートを追加

  * [**SecurityBundle**][9] - Symfony のセキュリティコンポーネントの統合によるセキュリティ機能を追加

  * [**SwiftmailerBundle**][10] - メール送信を行う Swiftmailer のサポートを追加

  * [**MonologBundle**][11] - ロギングライブラリである Monolog のサポートを追加

  * [**AsseticBundle**][12] - アセット処理のライブラリである Assetic のサポートを追加

  * [**JMSSecurityExtraBundle**][13] - アノテーションを介したセキュリティの追加を有効化

  * [**JMSDiExtraBundle**][14] - より強力なディペンデンシーインジェクション機能の追加

  * **WebProfilerBundle** (in dev/test env) - プリファイリングの機能とウェブデバッグツールバーを追加

  * **SensioDistributionBundle** (in dev/test env) - Symfony のディストリビューションでの設定と動作の機能を追加

  * [**SensioGeneratorBundle**][15] (in dev/test env) - コード生成の機能の追加

  * **AcmeDemoBundle** (in dev/test env) - サンプルコードのデモバンドル

エンジョイ!

[1]:  http://symfony.com/doc/2.1/book/installation.html
[2]:  http://getcomposer.org/
[3]:  http://symfony.com/download
[4]:  http://symfony.com/doc/2.1/quick_tour/the_big_picture.html
[5]:  http://symfony.com/doc/2.1/
[6]:  http://symfony.com/doc/2.1/bundles/SensioFrameworkExtraBundle/index.html
[7]:  http://symfony.com/doc/2.1/book/doctrine.html
[8]:  http://symfony.com/doc/2.1/book/templating.html
[9]:  http://symfony.com/doc/2.1/book/security.html
[10]: http://symfony.com/doc/2.1/cookbook/email.html
[11]: http://symfony.com/doc/2.1/cookbook/logging/monolog.html
[12]: http://symfony.com/doc/2.1/cookbook/assetic/asset_management.html
[13]: http://jmsyst.com/bundles/JMSSecurityExtraBundle/1.1
[14]: http://jmsyst.com/bundles/JMSDiExtraBundle/1.0
[15]: http://symfony.com/doc/2.1/bundles/SensioGeneratorBundle/index.html
