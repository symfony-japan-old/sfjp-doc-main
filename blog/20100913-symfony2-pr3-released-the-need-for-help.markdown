Symfony2 PR3 リリース; 手を貸してください
=========================================

([原文リンク](http://www.symfony-project.org/blog/2010/09/13/symfony2-pr3-released-the-need-for-help))

本日Symfony2 PR3(Preview Release3)をリリースしました。今回のブログがSymfony2のプレビューリリースにおける最初の告知となります。アルファバージョンがリリースできる段階まで迫っており、それに向けて皆さんの協力が必要です。


What's new?
-------------

Symfony2 PR2以降、これまでの機能の改良を集中的に行いました。Symfony2 PR3では、コードのリファクタリング、柔軟性、わかりやすさ、拡張性、使い勝手の向上に多くの時間を費やす結果となりました。

すべての変更をリストアップはしませんが、大きな変更の1つとして、Symfony2 プロファイラーが挙げられます。[プロファイラー](http://docs.symfony-reloaded.org/guides/internals/profiler.html)はリクエストごとの情報を保存・分析し、開発時における有用な情報として集積したものです。プロファイラーを活用することで、開発時にはデバッグしやすさの向上やパフォーマンスの改良につながります。運用環境では問題が発生した後にそれを追求するためのツールとしても使えます。また、集積した情報に直接アクセスするわけではなく、Webデバッグツールバーや、新たに実装されたWebプロファイラーによって視覚的に閲覧できます:

![The Symfony2 Web Profiler](http://symfony-reloaded.org/images/webprofiler.jpg)


より詳しい情報については、Symfony2のデベロッパー[ツール](http://symfony-reloaded.org/tools)についてのクイックイントロダクションを読むか、[プロファイラー](http://docs.symfony-reloaded.org/guides/internals/profiler.html)の詳細なドキュメントを読んでください。

それに加えてドキュメントの整備も行いました。新しい[ドキュメント](http://docs.symfony-reloaded.org/)のWebサイトは、[索引](http://docs.symfony-reloaded.org/genindex.htmlhttp://docs.symfony-reloaded.org/genindex.html)、[検索](http://docs.symfony-reloaded.org/search.html)エンジン、[用語集](http://docs.symfony-reloaded.org/glossary.html)など多くの機能を持って再設計されました。Symfony2の[API](http://api.symfony-reloaded.org/PR3/index.html)もWebサイト上で利用可能です。

この他にもいくつもの章を公式ドキュメントに追加しました。Symfony2の[内部](http://docs.symfony-reloaded.org/guides/internals/overview.html)について様々な情報を記したドキュメントなどが閲覧できます。

ドキュメントについてはまだ欠けている箇所があるので、皆さんぜひ協力してください。


Symfony2を試してみるには？
---------------------------

Symfony2を試してみるには、[サンドボックス](http://symfony-reloaded.org/code)をダウンロードして、[クイックツアー](http://docs.symfony-reloaded.org/quick_tour/the_big_picture.html)チュートリアルを読むことが手早く試す方法です。


どのように協力するか？
------------------------

Symfony2の開発がスタートしてから、50名以上の人々が様々な形で貢献してくれました。([http://github.com/visionmedia/git-extras](http://github.com/visionmedia/git-extras) にて集計)

- 646 Fabien Potencier
- 40 Jonathan H. Wage
- 39 Kris Wallsmith
- 28 Pascal Borreli
- 18 Bernhard Schussek
- 18 Jordi Boggiano
- 16 Jeremy Mikola
- 16 Brandon Turner
- 16 ornicar
- 12 Francois Zaninotto
- 8 Dennis Benkert
- 5 Bongiraud Dominique
- 5 geoffrey
- 4 Bulat Shakirzyanov
- 4 Greg Thornton
- 4 fivestar
- 4 Noël GUILBERT
- 3 Fabian Lange
- 2 wodkaist
- 2 Daniel Cestari
- 2 Fabien Pennequin
- 2 Justin Hileman
- 2 Matthieu Bontemps
- 2 Nils Adermann
- 2 Sebastian Bergmann
- 2 Thibault Duplessis
- 2 Antoine Hérault
- 1 Nicolas Fabre
- 1 IamPersistent
- 1 Gordon Franke
- 1 Pierre Minnieur
- 1 Romain Dorgueil
- 1 sensio
- 1 Sergiy Sokolenko
- 1 Sébastien HOUZE
- 1 tirnanog06
- 1 avalanche123
- 1 catchamonkey
- 1 ever.zet
- 1 Damon Jones
- 1 Christian Stocker
- 1 henrikbjorn
- 1 Katsuhiro OGAWA
- 1 Marc Weistroff
- 1 Bulat (Hacker) Shakirzyanov
- 1 Nathanael d. Noblet
- 1 Benjamin Eberlei

GitとGitHubのおかげでこれだけの貢献を得ることができました。どう行えばよいかわからない方は、[貢献](http://docs.symfony-reloaded.org/contributing/code/index.html)のドキュメント読んでください。

この他にもSymfony2のテストを行ってくれた方や、Symfony2に関する様々な決定においてフィードバックをくれた方もいました。Symfony2に影響を与えられる機会をぜひ逃さないでください。


何をしなければならないか？
------------------------------

Symfony2のベータ/RCリリースサイクルに入る前に、やらなければならないことが山ほどあります。

- *セキュリティ (authentication, authorization)*: 既に着手しており、10月中に最初のバージョンをリリース予定
- *I18N*: 基礎的な国際化サポートはZend Framework 2を通して行えますが、それの改善(ZF2のリファクタリング待ち)
- *フォーム/バリデーション*: Bernhardがすばらしいフォーム/バリデーションフレームワークを作成してくれたが、現状は未完成。しかし残念なことにBernhardが開発に着手する時間がないため、引き継いでくれる開発者を募集中
- *インストール*: symfony plugin:install 関連のコマンドをリプレースしたく、これについていくつかのアイディアはあるものの開発に着手する時間がない。最初のステップとして、Pyrusを使いたい

協力してくれる方は、[デベロッパー](http://groups.google.com/group/symfony-devs)メーリングリストに参加し、どういったことに協力可能かを伝えてください。それについて話し合いましょう。数日のうちに、行ってほしいタスクを[チケット](http://trac.symfony-project.org/report/24)にして追加します。この方法であれば全員が残っているタスクを共有できますし、動いている物も確認できます。


野生に潜むSymfony2
----------------------

Symfony2はまだまだ完成していませんが、多くの方が既にWebサイト作成に利用し始めています。彼らは大変クレイジーですが、実際に起こったSymfony2の挙動に関する大変有益なフィードバックを与えてくれ、感謝しています。

> **CAUTION**
> 実際のプロジェクトではSymfony2を盲目的に使わないでください。Symfony2はまだ開発中で、時に大幅な変更が入ることもあります。そのことを留意してください。

<br />

> **NOTE**
> 翻訳者コメント<br />
> いよいよSymfony2もPR3がリリースされました。正式リリース予定日が来年の3月に延期されましたが、それに間に合わせるため多くの協力者を募っている状態です。
> バグがあればGitHubでPull requestを出すと問題なければ取り込まれますし、テストの追加やドキュメントの追加、修正など、協力できることはたくさんあります。
> Symfony2を本当によい物にするためにも、変化させられる"今"、皆さんで協力していきましょう！英語が苦手でコミュニケーションがとれないということであれば、ユーザー会のMLに相談してください。 [fivestar]
