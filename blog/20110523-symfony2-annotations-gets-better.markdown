---
layout: default
title: Symfony2: アノテーションが改善されました
---

Symfony2: アノテーションが改善されました
========================================

  - [原文リンク](http://symfony.com/blog/symfony2-annotations-gets-better)

by Fabien Potencier – May 23, 2011


今日のこの後で、Symfony2 beta2 がリリースされます。しかし、最初に、昨日 master リポジトリに取り込まれた大きな変更について話したいと思います。ご存じかと思いますが、Symfony2 は Doctrine のマッピング情報とバリデーションのコンフィギュレーションのためにアノテーションを利用しています。もちろん、これは完全なオプションで、XML、YAML もしくは PHP でさえも同じ内容を実現できます。アノテーションは便利なもので、1つの同じファイルの中ですべてを定義することができます。


Symfony Standard Edition は2つの追加バンドル: SensioFrameworkExtraBundle と JMSSecurityExtraBundle 経由でアノテーションのよりすぐれたサポートを提供します。これらによってコントローラコンフィギュレーションのアノテーションを使うことができるようになります (ルーティング、キャッシュ、セキュリティ、テンプレートなど)。


異なるライブラリ/バンドルが新しいアノテーションを定義しているときにあいまいさを避けるためには、コンフィギュレーションの変更が可能な「プレフィックス」を使うことが必須です。


    /**
     * @orm:Entity
     */
    class User
    {
        /**
         * @orm:Column(type="string", nullable=false)
         * @assert:NotBlank
         */
        private $name;
    }

しかしすぐに複数の問題が発生します。

  - Doctrine のドキュメントを見ると、@orm:Column の代わりに @Column が使われていることがわかります。プレフィックスがオプションだからです。ですので、Doctrine のドキュメントはプレフィックスを使っていませんが、Symfony2 はプレフィックスとして orm を使うことを強制します。このコンフィギュレーションは変更可能で、任意の別のプレフィックス (@doctrine:Column)を使うことができます
  - アノテーションライブラリはオートロードの機能とうまく連動しませんでした。
  - SensioFrameworkExtraBundle と JMSSecurityExtraBundle は同じプレフィックスを共有していましたが、これはハックであり、本当はスケーラブルなやり方ではありませんでした。

Johannes はこの問題のエレガントなソリューションを見つけるためにこの数週間熱心に取り組んでいました。それぞれのアノテーションは1つのクラスとして定義されるので、クラスのショートネームだけを使う代わりに、完全修飾クラス名 (FQCN) を使うことを決めました。これはグローバルコンフィギュレーションとして定義された任意のプレフィックスの必要性を取り除き、複数のライブラリにまたがる曖昧性を避け、オートロードの問題も一緒に取り除きます。


    /**
     * @Doctrine\ORM\Mapping\Entity
     */
    class User
    {
        /**
         * @Doctrine\ORM\Mapping\Column(type="string", nullable=false)
         * @Symfony\Component\Validator\Constraints\NotBlank
         */
        private $name;
    }

もちろん、FQCN をあらゆる場所で使うことはとても冗長ですが、さいわいなことに、PHP には use 文によるソリューションがすでに用意されています。


    use Doctrine\ORM\Mapping as ORM;
    use Symfony\Component\Validator\Constraints as Assert;

    /**
     * @ORM\Entity
     */
    class User
    {
        /**
         * @ORM\Column(type="string", nullable=false)
         * @Assert\NotBlank
         */
        private $name;
    }

これでアノテーションはより「ネイティブ」に感じられます。Symfony2 のコンテキストの外側からアノテーションを使いたいのであれば、Doctrine Common の[リポジトリ](https://github.com/doctrine/common/tree/3.0.x) (version 3.0) をご覧ください。
