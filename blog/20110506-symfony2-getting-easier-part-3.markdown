Symfony2: よりかんたんになりました (パート 3)
==============================================

  - [原文リンク](http://symfony.com/blog/symfony2-getting-easier-part-3)

by Fabien Potencier – May 06, 2011

「[Symfony2 がかんたんになった](http://symfony.com/blog/symfony2-getting-easier)」ことに関する以前のブログ投稿において、Nathan さんが次の価値あるコメントをしてくださりました。

    **すばらしい**！この方向性を賞賛します。Doctrine のスキーマファイルの場所を短くする機会はありますか？エンティティごとにファイルを次のようにしたいです: src/Mycompany/MyBundle/Resources/config/doctrine/metadata/orm/Mycompany.MyBundle.Entity.Orderset.dcm.yml
しかし、「本気ですか？config/schema.yml はどうなりましたか？」と同じ意見です。Larry Wall の Perl に対する哲学が好きです - 「かんたんなことをかんたんに、困難なことを実現可能に」

Nathan さん、話は聞きましたよ！。次の beta2 において、不要な metadata/orm/ の部分を削除することでパスを短くしました。ですので、Orderset クラスのマッピングを定義することは src/Mycompany/MyBundle/Resources/config/doctrine/metadata/orm/Mycompany.MyBundle.Entity.Orderset.dcm.yml の代わりに src/Mycompany/MyBundle/Resources/config/doctrine/Mycompany.MyBundle.Entity.Orderset.orm.yml において実現可能です。
ほんの少しはよくなりましたが、それほどではないですよね？ 不幸なことに、Doctrine2 はクラスごとに1つのファイルのルールを強制し、ファイルの名前のルールを完全修飾クラス名に強制します。しかしかつての Perl ディベロッパとして、そしてファイルの名前が短いことはつねによいことなので、このルールを避ける方法をいくつか探してみたところ、とてもかんたんであることが判明し、DoctrineBundle はメタデータを単独のファイルにマッピングする複数の定義をサポートするようになりました。ですので、src/Mycompany/MyBundle/Resources/config/doctrine/mapping.orm.yml のなかでデータをマッピングする Orderset クラスを定義することもできます。これは以前よりもずっと短くなり、もちろん、完全なオプションです。両方の可能性を混在させて１つのバンドルにマッチさせることができます: define most of マッピングデータの大半を1つのメインファイルに定義し、たくさんのメタデータの情報を含むエンティティに対して個別のファイルを使い続けます。しかしすべてのマッピングデータを中心的な場所で定義する可能性はどうでしょうか？筆者のように、Symfony2 のコンテキストの外側で Model を再利用できるようにしたい; 特定のバンドルのもとで Entity クラスとマッピングデータを保存したくないとします。では、たとえば、app/config/mapping.orm.yml にすべてを保存するのはどうでしょうか？うん、これも実現可能で、シンプルに動くコンフィギュレーションは次のようになります。


    doctrine:
      orm:
        mappings:
          global:
            type:   yml
            dir:    %kernel.root_dir%/config
            prefix: Blog\Entity
                
吉報は doctrine:generate:entities コマンドはこれをネイティブに扱うことができます。

    ./app/console doctrine:generate:entities Blog/Entity --path=src/

古い src/Mycompany/MyBundle/Resources/config/doctrine/metadata/orm/Mycompany.MyBundle.Entity.Orderset.dcm.yml ファイルに別れを告げ、app/config/mapping.orm.yml を使うことを楽しみましょう。
フィードバックは Symfony2 を改善させる秘訣です。