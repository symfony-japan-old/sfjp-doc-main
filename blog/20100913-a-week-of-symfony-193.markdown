A week of symfony #193 (6->12 September 2010)
======================================

Symfony公式ブログで毎週公開される、Symfony関連の活動まとめ記事の翻訳です。
この翻訳では、Symfony本体に関連したアップデートなどのみを取り上げます。
プラグインの更新等も含む全文は、以下のリンクからご確認ください。

（[原文リンク](http://www.symfony-project.org/blog/2010/09/12/a-week-of-symfony-193-6-12-september-2010)）

<br />
<br />
<hr />

今週 Symfony2 のルーティングコンポーネントに[アノテーションローダーが追加](http://github.com/symfony/symfony/commit/130494066d7ef69ce0b5ac48e82b5f150bee0357)され、
コントローラーに対してアノテーションをサポートするために新しい実験的な[FrameworkExtraBundle](http://bundles.symfony-reloaded.org/frameworkextrabundle/)がリリースされました。
開発メーリングリストでは[アノテーションの働き](http://groups.google.com/group/symfony-devs/browse_thread/thread/19c04caa20bc8dc9)に関する議論が行われました。
また残念なことに、Symfony2のローンチは次回のSymfony Live カンファレンス(2011年3月3日〜5日)まで延期されることになりました。

開発メーリングリスト
----------------------

- [アノテーションに関する規定](http://groups.google.com/group/symfony-devs/browse_thread/thread/19c04caa20bc8dc9)
- [ベンダバンドルで定められたエンティティの対応付けがされない](http://groups.google.com/group/symfony-devs/browse_thread/thread/48ce8e16346ac86a)

開発ハイライト
----------------

### Symfony2開発ハイライト

[チェンジログ](http://github.com/symfony/symfony/commits/master):

- [2914c44](http://github.com/symfony/symfony/commit/2914c443441bf5ea84e166934b7e23f6d97042d6): [DoctrineBundle] "Entities" を "Entity" に変更  
- [e71eec3](http://github.com/symfony/symfony/commit/e71eec3f5d95f849052aa113776808e37113b63a): [DoctrineMongoDBBundle] ロガーにおける、json_encodeへの不必要な変換部分を削除
- [7c1b42e](http://github.com/symfony/symfony/commit/7c1b42e81b7e63423607200ae08911ca58bcdcae): [DependencyInjection] Extensionの設定に、無名サービスを導入する方法を追加
- [4f33761](http://github.com/symfony/symfony/commit/4f337615e3b465f5f325a4ef50dac1def32fdda9): [HttpFoundation] RequestMatcherを追加
- [0b378d1](http://github.com/symfony/symfony/commit/0b378d1b3e93416dcf6b1737a87ab631b286f3dd): リクエストに基づきプロファイラーを使用可能にするための方法を追加
- [1719bfb](http://github.com/symfony/symfony/commit/1719bfb871e1f923185efda47a319385c2f5a793): [DomCrawler] URIsが誤って生成される問題を解消
- [26e4b2e](http://github.com/symfony/symfony/commit/26e4b2e2ef094472598fcbc3ff80a2245dc3d294): [Finder] テストケースにおいて、ファイルシステムから読み込んだデータを正しくソートした状態で照らし合わせるよう修正
- [179fe8e](http://github.com/symfony/symfony/commit/179fe8e6237589d06dceed177f726484ae675d12): Symfony\Component\Routing\Route::setRequirements() において、必須条件に配列が指定できるよう修正
- [1443d4a](http://github.com/symfony/symfony/commit/1443d4a0baea7add0e190d9d78ba7cadf10dc585): [HttpFoundation] getQueryString()を更新し、より多くのシナリオで動作することを確認
- [eb7cbb7](http://github.com/symfony/symfony/commit/eb7cbb77ec9ff4ca8143679ed66c0c9b94e08413): HTMLマークアップに関する問題を解消
- [2f8db91](http://github.com/symfony/symfony/commit/2f8db9135a25a32fc77a9f8387f1f4b350f02cff): Windowsでwebprofilerページを表示した際に例外が発生するバグを解消
- [df98a22](http://github.com/symfony/symfony/commit/df98a229f3dbc7acf45531250cc6f524a6456ae6): [DoctrineMongoDBBundle] MongoとODMタイプのためにより多くのサポート項目を追加
- [1304940](http://github.com/symfony/symfony/commit/130494066d7ef69ce0b5ac48e82b5f150bee0357), [b753ea4](http://github.com/symfony/symfony/commit/b753ea45b24bf84c3285de91e684974006e9ef81), [c39534e](http://github.com/symfony/symfony/commit/c39534e258c8f08a47f6a6c5cf0b623a20f176e1): [Routing] アノテーションローダーを追加
- [4d669d1](http://github.com/symfony/symfony/commit/4d669d106ed8ac5dcd98e34c3d1d8ca7bd08ebf7): [Validator] XSDを内部で取得するようXliffローダーを変更
- [5155321](http://github.com/symfony/symfony/commit/51553211f3da2f9d73030847600e6e2543003d1f), [e6b0d54](http://github.com/symfony/symfony/commit/e6b0d5453187b66fd16700a98ec82b7340f21490): [DoctrineMongoDBBundle] DoctrineのODMコマンドにcreateとdropを追加
- [c53ebe7](http://github.com/symfony/symfony/commit/c53ebe7a8e8f8af1ed7b5bacf6b2bebefbe696b6): [Form] Form::bind()で空の値をsubmitされたときの挙動を変更
- [40c0fe8](http://github.com/symfony/symfony/commit/40c0fe854f8b102a7d450c4700af3d391e70f70e): [Form] FileFieldを追加
- [fc9325a](http://github.com/symfony/symfony/commit/fc9325a737f0c9764b2315484ef59646f841bf58): ファイルアップロード時の挙動を修正
- [a141c98](http://github.com/symfony/symfony/commit/a141c98917ded11f43239e30189ca76f9271455a): [HttpFoundation] ファイルコンポーネントをHttpFoundation以下に移動
- [6fc9b68](http://github.com/symfony/symfony/commit/6fc9b68fa7b54c916d0d6d3fa527eeda10569b6f): [Form] unset()を廃止し、"choices"オプションがオブジェクトであっても破壊されないようなロジックに変更
- [2b776bf](http://github.com/symfony/symfony/commit/2b776bf2e8b3d4c1003b12655f43b4fca1172ccf), [e52cf7a](http://github.com/symfony/symfony/commit/e52cf7afe0d266256e3b78db8cb9eb305e075710), [b3648b2](http://github.com/symfony/symfony/commit/b3648b219b3f354fa0932e492adc8b92b841c1d7), [9f5469f](http://github.com/symfony/symfony/commit/9f5469f62d2096bc486ecd31202dc2931bfd040f): [Form] ユニットテストを追加
- [9be7cbb](http://github.com/symfony/symfony/commit/9be7cbb115a81193e2b15222c3d4630821589d72): [Form] CollectionField::setData() は新しいデータから無効な古いフィールドを削除しなければならない
- [fb24b29](http://github.com/symfony/symfony/commit/fb24b291c826c55497b2daa1d56a978de5425146): [Form] FieldGroup::addError() はFieldGroups内のフィールドを対応付けることが出来る
- [b9a7b7e](http://github.com/symfony/symfony/commit/b9a7b7e51a89119b8a9bfc9d1bfd529060f04539), [c537fb9](http://github.com/symfony/symfony/commit/c537fb9eb231d63c06584077c9b3b3c0cdec7907): [DoctrineBundle, DoctrineMongoDBBundle] ディレクトリーの対応付けを変更
- <del>[d326c39](http://github.com/symfony/symfony/commit/d326c398e2721c996d9f45108c1ab0cdfceb8ea6): [Form] デフォルトのCSRFトークン生成について、必ずユーザーとの結びつけを試すように変更</del>
- [226277f](http://github.com/symfony/symfony/commit/226277fd0ed37181e967abf5043a389e355079fc): CSRF保護の設定を行えるように追加
- [74bc9d4](http://github.com/symfony/symfony/commit/74bc9d461bb60e7fedd6ddf8abf2454a7e312c48): [FrameworkBundle] csrf_secretパラメーターのオプションへの追加ロジックを修正


> **NOTE**
> 翻訳者コメント<br />
> 当初から予想されていましたが、Symfony2のローンチが来年3月に延期となりました。<br />
> 開発のスピードも上がってきているようなので、これから半年の間にどんな魅力的な機能が追加されるか楽しみですね。[yuchimiri]
