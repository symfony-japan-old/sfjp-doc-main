The State of Symfony 2参加レポート - Symfony 2が大変なことになっています！
==========================================================================

本日、[The State of Symfony 2オンラインカンファレンス](http://www.symfony-live.com/)が開催されました。
カンファレンスで使われたスライド資料や、Symfony 2の新しいリリースは、後日公開されるのではないかと思いますが、
まずはカンファレンスのセッションの概要を[@hidenorigoto](http://twitter.com/hidenorigoto)がレポートいたします。

なぜ大変なことになっているのかは、最後のセッションの内容を参照ください。


※[@fivestr](http://twitter.com/fivestr)さんによるレポートも合わせてご参照ください。

- [The State of Symfony 2参加レポート - Symfony 2はすごい！](20100623-the-state-of-symfony2-2)


各セッションのスライドは、こちらの[スライド一覧](20100624-the-state-of-symfony2-slides)をご参照ください。


セッションリスト
----------------

以下のセッションが行われました。

1. News of the Symfony2 world (Fabien Potencier)
2. Symfony 2 meets Propel 1.5 (Francois Zaninotto)
3. Symfony and Doctrine (Jonathan Wage)
4. Unit & Functional Tests (Fabien Potencier)
5. The new form framework (Bernhard Schussek)
6. Caching on the Edge (Fabien Potencier)

以下、セッションごとに簡単に内容を紹介します。


1. News of the Symfony2 world (Fabien Potencier)
------------------------------------------------

Symfony 2の哲学

> Be as easy as possible for newcomers
> and as flexible as possible for advanced users

コーディング規約など、より標準的なものに統一


Symfony 2の構成要素である、Symfony ComponentsとSymfony Frameworkについて。
Symfony Componentsはそれぞれ単独で利用可能なコンポーネントで、CssSelector、DomCrawler、Browser、Finderなどがあります。
Frameworkには例えばHttpKernelなどがあって、テストやプロファイリング（Webデバッグツールバーなど）をサポートします。


> **NOTE**
> (感想)
> このセッションの内容は、これまでに公開されたコンポーネントのおさらいでしたので、特に目新しい内容はありませんでした。
> [hidenorigoto]



2. Symfony 2 meets Propel 1.5 (Francois Zaninotto)
--------------------------------------------------

Propel 1.5について。
Propel 1.5は、symfony 1.xにも対応している。Propel 1.3/1.4と互換。
IDEフレンドリー（補完などが行われやすい）

### Propel 1.5でのいくつかの新機能

- Model Query （Doctrineライクなクエリー）
- Collectionのサポート
- Many-to-Manyリレーションのサポート
- NestedSetのサポート
- Concrete Table Inheritanceのサポート
- One-to-many joined hydration（1対多リレーションをJOINしたクエリーのハイドレーションサポート）・・・1.5.1
- ModelQuery::findOneOrCreate()・・・1.5.2
- aggregate_column（1対多リレーションしている子のカウントを親の特定フィールドに自動セット）・・・1.5.2


### Doctrine 2と比較して

- モデルのコードはsymfony 1.x互換
- キャッシュしなくても高速
- ActiveRecord（Doctrine 2はActiveRecordではなくなる）
- 現時点ですでに多くの利用実績があり、stable


> **NOTE**
> (感想)
> Criteriaを使わず、Doctrineライクなクエリーの記述が可能になるなど、Propelもかなり進化している印象を受けました。
> また、symfony 1.xでのノウハウがそのままSymfony 2でも使えそうなのも魅力的に感じました。
> [hidenorigoto]



3. Symfony and Doctrine (Jonathan Wage)
---------------------------------------

Doctrine 2について。
DBALとORM（およびODM）に分離された。

### ORM

EntityManagerが1データベース接続あたり1つ作られ、EntityManagerにより、PHP Object(POPO)がORMにマップされる。
つまり、各エンティティはピュアなPHPクラス（どのクラスも継承していない）

コンソールコマンドがさらに整備されて、開発時のワークフローを支援。

コード例：

    [PHP]
    $em = $this->getEntityManager();
    $user = new User();
    $user->setName('Jonathan H. Wage');
    $em->persist($user);
    $em->flush();

開発中にスキーマを変更した場合、console doctrine:schema:update コマンドで、スキーマ変更の差分だけをDBに反映させることが可能。
スキーマのバージョニング（マイグレーションクラス）のサポートなど。


### DBAL

DBALから、生SQLの発行などを行える。
DBALコマンドで、コマンドラインからSQLを発行。


### MongoDB

DoctrineMongoDBBundle。
Document Query Languageを使って、これまでのDoctrineとほぼ同じ方法で、MongoDBのドキュメントを操作できる。


### パフォーマンス

Symfony 2においてPropel 1.5と比較した場合、ほぼ同等だと思われる（ケースバイケース）。
バッチINSERTのような処理では、Doctrine 2の方が速い。


> **NOTE**
> (感想)
> Doctrine 2は、Doctrine 1とは違ったアーキテクチャになり、それぞれのエンティティがピュアなPHPクラスになります。
> 各エンティティのアクセサメソッドもこれまでのマジックメソッド方式ではなくなるなど、
> レコードオブジェクトの操作が内部的に軽くなるように作られている印象を受けました。
> [hidenorigoto]



4. Unit & Functional Tests (Fabien Potencier)
---------------------------------------------

Symfony 2のUnitテスト、Functionalテストについて。

symfony 1.xのlimeから、より標準的なテストフレームワークであるPHPUnitに変更。

Functionalテスト：<br />
× controllerをUnitテストする → ○ リクエストに対するレスポンスをテストする

テスト自体のプロセスと、テストからリクエストされる処理のプロセスは別（Forkされる）


> **NOTE**
> (感想)
> Symfony 2では、Symfony Componentsに含まれるCssSelector/Crawler/Browserをフル活用して、リンククリックやフォーム送信のテストを記述します。
> symfony 1.xでもこれらは可能でしたが、テストのプロセス内でリクエストのプロセスも処理されていました。
> これまでよりも、より多岐に渡るテストをSymfony内で記述できるようになる印象を受けました。
> [hidenorigoto]



5. The new form framework (Bernhard Schussek)
---------------------------------------------

Symfony 2にバンドルされる新しいフォームフレームワークについて。

symfony 1.xに組み込まれているsfFormが、Symfony 2では新しいフォームフレームワークに置き換えられます。

- フォームのデータを表すピュアなPHPオブジェクト（POPO）= Domain Model
- フォームおよびフィールド
  - フィールドは、「フィールドグループ」などをサポート
- バリデーター
  - バリデーションをDomain Model内にアノテーションとして記述可能


> **NOTE**
> (感想)
> symfony 1.xの鬼門の1つであるsfFormから、Symfony 2では新しいフォームフレームワークに置き換えられるようです。
> アノテーションによるバリデーションの記述、ドメインモデルをそのまま使える等、（独立して使えるという触れ込みの割には）symfonyと密に結びついていたsfFormと比べると、シンプルな構成で扱いやすくなる印象を受けました。
> [hidenorigoto]



6. Caching on the Edge (Fabien Potencier)
-----------------------------------------

このセッションが、事前に「Killer Feature of Symfony 2」と言われていたものの紹介です。

スライドの最初の方ででてきた簡単なベンチマーク
- 「Symfony 2は、symfony 1.xの5倍高速」

さらにその後のベンチマークでより複雑で同時接続数の多いケースの場合、<span style="font-size: 1.5em; font-weight: bold;">「Symfony 2は、symfony 1.xの約80倍高速!!!」</span>


この高速化を担当しているのが、Symfony2 HTTP Proxy（HTTPアクセラレーターと呼ばれていました）で、
これまでのsymfony 1.xと比較してより厳密にHTTPプロトコル、特にキャッシュに関するヘッダを扱うことで、高負荷時のパフォーマンスも
大幅に向上させているようです。
さらに、このSymfony 2 HTTP Proxyは「Edge Side Include」というHTTP仕様を実装しており、1つのページ内のパーツごとに異なるキャッシュ時間の制御などを行えるようになるようです。


参考：[HTTP/1.1, part 6: Caching draft-ietf-httpbis-p6-cache-09](http://datatracker.ietf.org/doc/draft-ietf-httpbis-p6-cache/)


> **NOTE**
> (感想)
> このセッション、Symfony 2のkiller featureの紹介ということで期待していたのですが、良い意味で期待を大幅に裏切られる、すごいものが出てきたと感じました。
> Edge Side Includeを使うと、もしかすると今よりもさらに各アクションの処理内容を簡潔に記述できるようになるかもしれない。
> しかもパフォーマンスもこれまで以上とあれば、どんどん夢が広がります。
> この機能を知って、私は俄然Symfony 2をすぐにでも使いたくなってしまいました。
> [hidenorigoto]



