Symfony 2.1: Doctrine 関係のバンドルが Doctrine グループへ移管されました
========================================================================

([原文リンク](http://symfony.com/blog/symfony-2-1-the-doctrine-bundle-has-moved-to-the-doctrine-organization))

Symfony2 の [DoctrineBundle](https://github.com/doctrine/DoctrineBundle) が Doctrine グループ（GitHub 上で１つの organization）へ[移管されました](https://github.com/symfony/symfony/commit/dcf209a4aaf27147848437bc5a505b5506116d44)。
これにより、Doctrine 関係のバンドルのメンテナンスは Symfony から独立して行われるようになります。

  - これらのバンドルのリリースサイクルが、Symfony 本体に依存しなくなります。
  - 実際にメンテナンスを行なっているメンバーが所属するグループ（organization）のリポジトリにコードが移されます。
  - Symfony の提供する永続化レイヤーが Doctrine のみであるという誤解をなくします。Symfony はビューとコントローラの抽象化に特化し、モデルについては何の強制もありません。

Symfony Standard Edition（2.1リリース向け）では、この変更はすでに反映されています（[コミット](https://github.com/symfony/symfony-standard/commit/5dee24eb280452fe46e76f99706c21ab417462ac)）。

すでに Symfony 2.1 をお使いの方は、コード内でたとえば Registry などの DoctrineBundle のクラスを使っている場合、Symfony\Bundle\DoctrineBundle\Registry から Doctrine\Bundle\DoctrineBundle\Registry に書き換えてください。

DoctrineFixturesBundle、DoctrineMigrationsBundle、DoctrineMongoDBBundle についても、Doctrine グループへ移管されました。ただし、Symfony リポジトリにもこれらのバンドルのフォークが作られていますので、Symfony 2.0 系のアプリケーションの後方互換性は維持されています。現在お使いの Symfony が 2.0 ブランチかどうかを確認してください（Web デバッグツールバー等でバージョンを確認できます）。

新しいリポジトリの URL は次のとおりです。

  - [https://github.com/doctrine/DoctrineBundle](https://github.com/doctrine/DoctrineBundle)
  - [https://github.com/doctrine/DoctrineMongoDBBundle](https://github.com/doctrine/DoctrineMongoDBBundle)
  - [https://github.com/doctrine/DoctrineFixturesBundle](https://github.com/doctrine/DoctrineFixturesBundle)
  - [https://github.com/doctrine/DoctrineMigrationsBundle](https://github.com/doctrine/DoctrineMigrationsBundle)

コードの書き換え部分などの詳細については、Doctrine の[ブログ記事](http://www.doctrine-project.org/blog/symfony-bundles-move)を参照してください。

> **NOTE**
> Symfony 2.0 ブランチ（2012年1月3日時点のステーブルリリース）を使っており、depsファイルによりvendor install/updateを行う場合は、SensioGeneratorBundleの2.0ブランチを参照するように設定を追加する必要があります。[こちらのコミット](https://github.com/symfony/symfony-standard/commit/5a2c4ba7ea07f03d1222a682d360e631dea8abdd)を参考にしてください。

