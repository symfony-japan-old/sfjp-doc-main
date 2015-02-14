---
layout: default
title: 第2回 Symfony2勉強会 参考情報
---

第2回 Symfony2勉強会 参考情報
=============================

1月15日に開催する、[第2回Symfony2勉強会](http://atnd.org/events/10869)のワークショップを進めるにあたって、参考となるURLなどを紹介します。
勉強会の当日も、随時こちらを参照しながら進めていただきます。

  - [ルーティングとアクションの基本](http://docs.symfony-reloaded.org/master/quick_tour/the_controller.html)<br />
    特定のアクションへのルーティングの書き方、アクションの書き方、リダイレクトの仕方、セッション、flashメッセージなど

  - [config.ymlへのORMの設定（マッピング）](http://docs.symfony-reloaded.org/master/guides/doctrine/orm/configuration.html#mapping-configuration)<br />
    バンドルごとにマッピングタイプを別々に指定できるようになりました

  - [Doctrine Annotations Reference](http://www.doctrine-project.org/docs/orm/2.0/en/reference/annotations-reference.html)<br />
    Doctrine2のアノテーションのリファレンス

  - [Doctrine Mapping Types](http://www.doctrine-project.org/docs/orm/2.0/en/reference/basic-mapping.html#doctrine-mapping-types)<br />
    Doctrine2で使えるデータ型

  - [Doctrine2 ORM向けのコマンド](http://docs.symfony-reloaded.org/master/guides/doctrine/orm/console.html)<br />
    ワークショップでは、
    - php app/console doctrine:database:create
    - php app/console doctrine:schema:create
    - php app/console doctrine:schema:update
    あたりを使います。

  - [Twig 基本構文](http://www.twig-project.org/doc/templates.html#variables)
  - [Twig 組み込みfilter](http://www.twig-project.org/doc/templates.html#list-of-built-in-filters)<br />
    テンプレートを記述する際に

  - [フォームの処理の基礎](http://docs.symfony-reloaded.org/master/guides/forms/overview.html)<br />
    Form処理の基本。この記述のとおりか、またはフォーム部分を別途フォームクラスにまとめます。

  - [バリデーター](http://docs.symfony-reloaded.org/master/guides/validator/constraints.html)<br />
    これらのバリデーションを、アノテーションを使ってEntityへ記述します

  - [メール](http://docs.symfony-reloaded.org/master/guides/emails.html)<br />
    sendmailトランスポートで手軽に送信します


参考になるバンドル
------------------

以下のバンドルは、Symfony2のコア開発にも関わっているメンバーで作られたグループ「FriendsOfSymfony」で開発されている「UserBundle」です。コードの書き方の参考になります。

  - [UserBundle](https://github.com/FriendsOfSymfony/UserBundle)


