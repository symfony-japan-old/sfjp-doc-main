The State of Symfony 2参加レポート - Symfony 2はすごい！
==========================================================================

6月22日に、[The State of Symfony 2オンラインカンファレンス](http://www.symfony-live.com/)が開催されました。
このブログエントリーはセッションの概要の[@fivestr](http://twitter.com/fivestr)によるレポートになります。
[The State of Symfony 2参加レポート - Symfony 2が大変なことになっています！](http://www.symfony.gr.jp/blog/20100622-the-state-of-symfony2-1)もあわせてご覧ください。


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
なお、自分はUnit & Functional Testsから見始めたので、それ以降のセッションのみのレポートとなります


4. Unit & Functional Tests (Fabien Potencier)
---------------------------------------------

Symfony 2のUnitテスト、Functionalテストについて。

Unitテスト:<br />

- PHPUnitを利用
- 各BundleのTestsディレクトリにテストを配置する

Functionalテスト:<br />

- コントローラのテストではなく、レスポンスに対してテストを行う
- リクエストを別のPHPプロセスとして処理することも可能
  - 1つのテストで同時に2つ以上のリクエストを送信してテストが可能
- BrowerKit, CssSelector, DomCrawler, ProcessなどのComponentsを利用
- 流れとしては次の3階層
  - ClientオブジェクトがSymfony 2のアプリケーションにリクエストを送る
  - 返ってきたレスポンスを元にCrawlerオブジェクトが作られる
  - PHPUnitでレスポンスのテストを行う
- レスポンスのプロファイリングも可能


> **NOTE**
> (感想)
> 特筆すべきはFunctionalテストです。Processにより別プロセスで処理が行えるため、
> より高度なFunctionalテストも可能になりました。symfony 1.xのころから
> 非常にテストを重要視してきただけに、今回も力を入れてきているなと感じました。
> [fivestar]



5. The new form framework (Bernhard Schussek)
---------------------------------------------

Symfony 2で採用される新しいフォームフレームワークについて。

### Form Component

- フォームのデータを表すピュアなPHPオブジェクト= Domain Model
- FieldとFieldGroup
  - 単一のフィールドを表すFieldと、複数フィールドを扱うFieldGroup
    - 両方とも同じインターフェイスを持つ
  - FormもFieldGroup
    - FormにはCSRF対策が含まれる
  - TextFieldやDateFieldなど様々なFieldがある
    - 多くのFieldは国際化対応がされている

### Validator Component

- Domain Modelの各プロパティなどに対して、Constraint(制約)を定義する
  - Domain Model内にアノテーションを記述したり、YAMLなどでマッピングを行う
- Validationのグルーピングが可能
  - グループを切り替えることで、バリデーション内容を動的に切り替えることが可能
    - たとえばUserグループはあるフィールドが必須だが、Adminグループでは必須ではないなど


> **NOTE**
> (感想)
> 今となっては欠かせない機能であるフォームフレームワークが一新されます。
> Doctrineもそうですが、ピュアなPHPオブジェクトに対してメタデータのマッピングを行う
> 方式なので、ドメインモデルを柔軟に扱えるのは大きなメリットかなと思います。
> [fivestar]



6. Caching on the Edge (Fabien Potencier)
-----------------------------------------

このセッションが、事前に「Killer Feature of Symfony 2」と言われていたものの紹介です。

まずSymfony 2とsymfony 1.xのパフォーマンス比較ですが、

- Symfony 2は、symfony 1.xの5倍高速
- 同時接続数が多い状況ではsymfony 1.xの<span style="color: red; font-weight: bold;">85倍高速</span> ....!?

と、驚愕な数値がでています。なぜそれほどまでにパフォーマンスの改善が行われているかというと

- Symfony 2にはHTTPアクセラレータと呼ばれるものを搭載する
  - HTTPのキャッシュヘッダーの制御
  - HTTP Proxy
  - Proxyパターンを利用してKernelをラッピングする？
- ESI(Edge Side Includes)の実装
  - 1つのページ内で部分ごとに異なるキャッシュ制御をする仕組み


> **NOTE**
> (感想)
> この日最後のセッションとなったChaching on the Edgeでは、Symfony 2に搭載されるキャッシュの機構についての紹介です。
> こうした仕組みを扱う裏側には、RequestをHttpKernelに渡してResponseが返ってくるというSymfony 2のシンプルなアーキテクチャの存在があります。
> 高機能ながらシンプルで柔軟、そして高速に。大幅に進化したSymfony 2に期待が膨らむばかりです！
> [fivestar]

