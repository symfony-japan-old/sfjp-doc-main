[Doctrine] Symfony 向けバンドルが Doctrine グループへ移管されました
===================================================================

([原文リンク](http://www.doctrine-project.org/blog/symfony-bundles-move) posted by beberlei - 2011/12/15)

> **CAUTION**
> この変更は Symfony 2.0 のアプリケーションには影響はありません。Symfony の master ブランチを使っている場合にのみ影響します。

Symfony2 の Doctrine 関係のバンドルが Doctrine グループへ移管されました。
DoctrineBundle は Symfony 2.0 リリースのコアバンドルの 1 つですが、今後はより Symfony からは独立してメンテナンスが行われます。

  - バンドルのリリースサイクルは Symfony とは独立します。
  - 実際にメンテナンスを行なっているメンバーが所属するグループにコードが移されます。
  - Symfony の提供する永続化レイヤーが Doctrine のみであるという誤解をなくします。Symfony はビューとコントローラの抽象化に特化し、モデルについては何の強制もありません。

DoctrineFixturesBundle、DoctrineMigrationsBundle、DoctrineMongoDBBundle についても、Doctrine グループへ移管されました。ただし、Symfony リポジトリにもこれらのバンドルのフォークが作られていますので、Symfony 2.0 系のアプリケーションの後方互換性は維持されています。現在お使いの Symfony が 2.0 ブランチかどうかを確認してください（Web デバッグツールバー等でバージョンを確認できます）。

新しいリポジトリの URL は次のとおりです。

  - [https://github.com/doctrine/DoctrineBundle](https://github.com/doctrine/DoctrineBundle)
  - [https://github.com/doctrine/DoctrineMongoDBBundle](https://github.com/doctrine/DoctrineMongoDBBundle)
  - [https://github.com/doctrine/DoctrineFixturesBundle](https://github.com/doctrine/DoctrineFixturesBundle)
  - [https://github.com/doctrine/DoctrineMigrationsBundle](https://github.com/doctrine/DoctrineMigrationsBundle)

コード内で書き換える必要がある箇所は多くはありません。たとえば DoctrineBundle を使っている場合は、次のようにしてください。

deps ファイルで DoctrineBundle の新しいリポジトリ URL を設定してください:

    [ini]
    [DoctrineBundle]
        git=http://github.com/doctrine/DoctrineBundle.git
        target=/bundles/Doctrine/Bundle/DoctrineBundle

AppKernel.php でバンドルクラスの FQCN を変更します:

    [PHP]
    $bundles = array(
        //..
        new Doctrine\Bundle\DoctrineBundle\DoctrineBundle(),
        //..
    );

Registry の参照を変更してください。

Symfony\Bundle\DoctrineBundle\Registry クラスがタイプヒンティングで使われているかもしれません。このようなコードでは、Doctrine\Bundle\DoctrineBundle\Registry クラスを参照するように変更してください。

新しいリポジトリを使う完全な deps ファイルは、次のようになります:

    [ini]
    [data-fixtures]
        git=http://github.com/doctrine/data-fixtures.git

    [migrations]
        git=http://github.com/doctrine/migrations.git

    [DoctrineBundle]
        git=http://github.com/doctrine/DoctrineBundle.git
        target=/bundles/Doctrine/Bundle/DoctrineBundle

    [DoctrineMigrationsBundle]
        git=http://github.com/doctrine/DoctrineMigrationsBundle.git
        target=/bundles/Doctrine/Bundle/MigrationsBundle

    [DoctrineFixturesBundle]
        git=http://github.com/doctrine/DoctrineFixturesBundle.git
        target=/bundles/Doctrine/Bundle/FixturesBundle

対応する autoload.php は次のとおりです:

    [PHP]
    $loader->registerNamespaces(array(
        'Symfony'          => array(__DIR__.'/../vendor/symfony/src', __DIR__.'/../vendor/bundles'),
        'Sensio'           => __DIR__.'/../vendor/bundles',
        'JMS'              => __DIR__.'/../vendor/bundles',
        'Doctrine\\Bundle' => __DIR__.'/../vendor/bundles',
        'Doctrine\\DBAL\\Migrations' => __DIR__.'/../vendor/migrations/lib',
        'Doctrine\\Common\\DataFixtures' => __DIR__.'/../vendor/data-fixtures/lib',
        'Doctrine\\Common' => __DIR__.'/../vendor/doctrine-common/lib',
        'Doctrine\\DBAL'   => __DIR__.'/../vendor/doctrine-dbal/lib',
        'Doctrine'         => __DIR__.'/../vendor/doctrine/lib',
        'Monolog'          => __DIR__.'/../vendor/monolog/src',
        'Assetic'          => __DIR__.'/../vendor/assetic/src',
        'Metadata'         => __DIR__.'/../vendor/metadata/src',
    ));

また、AppKernelクラスの registerBundles() メソッド内は次のようになります:

    [PHP]
    $bundles = array(
        new Symfony\Bundle\FrameworkBundle\FrameworkBundle(),
        new Symfony\Bundle\SecurityBundle\SecurityBundle(),
        new Symfony\Bundle\TwigBundle\TwigBundle(),
        new Symfony\Bundle\MonologBundle\MonologBundle(),
        new Symfony\Bundle\SwiftmailerBundle\SwiftmailerBundle(),
        new Symfony\Bundle\AsseticBundle\AsseticBundle(),
        new Sensio\Bundle\FrameworkExtraBundle\SensioFrameworkExtraBundle(),
        new JMS\SecurityExtraBundle\JMSSecurityExtraBundle(),
        new Doctrine\Bundle\DoctrineBundle\DoctrineBundle(),
        new Doctrine\Bundle\MigrationsBundle\DoctrineMigrationsBundle(),
        new Doctrine\Bundle\FixturesBundle\DoctrineFixturesBundle(),
    );
