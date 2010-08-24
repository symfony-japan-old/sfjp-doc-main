A week of symfony #190 (16->22 August 2010)
==========================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/08/22/a-week-of-symfony-190-16-22-august-2010)）

<br />
<br />
<hr />

今週のSymfony2の開発は、loggerと例外管理のリファクタリングに集中しました。テンプレートヘルパーは構文を修正し、[多くの人からの要望](http://groups.google.com/group/symfony-devs/browse_thread/thread/78251d7e40d0bd34)により名前空間Symfony\ComponentsはSymfony\Componentに変更されました。また、Symfony2はニューヨークで今週開催されたLibertyvasionカンファレンスでphpBBコミュニティに紹介されました。

開発メーリングリスト
--------------------

- [Symfony2におけるComponents vs Componentについての議論](http://groups.google.com/group/symfony-devs/browse_thread/thread/78251d7e40d0bd34)<br />
- [sfSassyCssPlugin(sass in symfony)がベータテスターを募集している（主にWindowsユーザ）](http://groups.google.com/group/symfony-devs/browse_thread/thread/abd616f5b07b017b)<br />
- [sf1プラグインはapp.ymlを使用できないデフォルト構成になっている？](http://groups.google.com/group/symfony-devs/browse_thread/thread/dc23d5907db83ede)<br />

開発ハイライト
--------------

### Symfony 2.Xブランチ：
- [714fa6f](http://github.com/symfony/symfony/commit/714fa6f652340620fce8c0f10d1109b32b574fe5): [FrameworkBundle] コントローラを修正
- [0da7295](http://github.com/symfony/symfony/commit/0da7295a9c26e90267f7ee0ec699e020a9f9d024): [FrameworkBundle] フォワードの前にリクエストをクリーンアップするように変更
- [917da00](http://github.com/symfony/symfony/commit/917da00763b31e290cc18ae61068d17d731844a8)[cbdde58](http://github.com/symfony/symfony/commit/cbdde58ddd9101cdbe0b49624709c9dbcfa15784): [FrameworkBundle] error_log()呼び出しをloggerの呼び出しに変更
- [509bfb8](http://github.com/symfony/symfony/commit/509bfb8940adfd67c4617174ec8bc990c57d0e42): [FrameworkBundle] ExceptionFormatterのContainerへの依存性をなくすよう修正
- [42c2aff](http://github.com/symfony/symfony/commit/42c2affbb151c728e9579dd606da3358797c6e87): [FrameworkBundle] RequestListenerのContainerへの依存性をなくすよう修正
- [4ed65d0](http://github.com/symfony/symfony/commit/4ed65d026ed5960ae3d41e58af5f35a0aeba8352): Controller::redirectが必ずレスポンスを返すよう変更
- [f48aeb1](http://github.com/symfony/symfony/commit/f48aeb1021587e6beff1cf47d7cfe3cf543061ee): [FrameworkBundle] 現在とは異なるフォーマットのテンプレートを指定できるように修正
- [5ea4b34](http://github.com/symfony/symfony/commit/5ea4b348c033cfa1c24e15c29a20a444be10f005): [ZendBundle] DebugLoggerInterfaceを追加
- [955fd40](http://github.com/symfony/symfony/commit/955fd40dd87264731f2175f95a8ad814d8ba6b55): 名前空間LoggerInterfaceをHttpKernel\Logの下に移動
- [d5069fc](http://github.com/symfony/symfony/commit/d5069fc594598916ffdabe7329f81367278c3423)[42cad4e](http://github.com/symfony/symfony/commit/42cad4e57e78a9e8285399b80291b25882bbb81a): [FrameworkBundle] 例外管理を修正
- [e03642d](http://github.com/symfony/symfony/commit/e03642dfa6370f8f52429a7873bb1d88b6ecea20): ClassCollectionLoaderをよりスマートに修正
- [54c3603](http://github.com/symfony/symfony/commit/54c36030e8612803a0da393ceaae5b5fbef3cf48): [Framework] Kernel::getBundleForClass()を追加
- [7514177](http://github.com/symfony/symfony/commit/7514177b51a51e05c1dc7a6d170debd121c48636): [Templating] Engineヘルパのプロパティを配列アクセス形式で取得するよう変更。例えば、現在$view['slots']->output(…)と呼び出している部分は$view->slots->output(…)となる
- [d5a61e3](http://github.com/symfony/symfony/commit/d5a61e3bc5082f63e0e5c78cd584b2196b6a8e1d): アセットのベースURLを提供する方法を追加
- [a506f2a](http://github.com/symfony/symfony/commit/a506f2ade8a303f8a15f551de5f0847f2bd23cf8): [FrameworkBundle] エラーページをより自然にするためにデフォルトのレイアウトを変更
- [bf82cf4](http://github.com/symfony/symfony/commit/bf82cf42dda099f8c0b6648b7dbd8e8ea7397c1e): 名前空間 Symfony\Components を Symfony\Componentにリネーム
- [2746bcc](http://github.com/symfony/symfony/commit/2746bcc84cad53c125494ae141ca0a8147fff24f): [HttpFoundation] セッションに何かの変更があったときに、自動でセッションスタートするように追加。アクセサメソッドの名前変更。remove()/has()メソッドを追加。


[その他多数](http://trac.symfony-project.com/trac/timeline?from=08%2F22%2F2010&daysback=6&milestone=on&ticket=on&changeset=on&update=Update)

<hr />
<br />

> **NOTE**
> 翻訳者コメント<br />
>
>この時期になってComponentsの名前が変更になったりと色々驚きもありますが、年末のリリースに向けて活発な議論と開発が行われているようです。実運用ではまだまだ使えませんが、symfony1.4からの以降も見据えつつ動向をしっかり追って行かなければと思いました。[yuchimiri]

