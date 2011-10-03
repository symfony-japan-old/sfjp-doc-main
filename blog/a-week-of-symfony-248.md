A week of symfony #248 (26 September -> 2 October 2011)
=======================================================

先週、Symfony2 に新しい[composer コンポーネント](https://github.com/symfony/symfony/commit/9ade639bb41423be611a023ab6966b855424f7be)の最初のコミットが投稿されました。このコンポーネントは、Symfony プロジェクトへのバンドルのインストールをとても手軽にするパッケージマネージャです。また、parameters.ini コンフィギュレーションファイルは parameters.yml に変更されました。[pull request前のチェックリスト](http://symfony.com/doc/current/contributing/code/patches.html#check-list)が公開され、[Twig のドキュメント](http://twig.sensiolabs.org/documentation)が大幅に改善されました。
 
開発メーリングリスト
--------------------

  * [i18n: フォールバック機構が正常に動作していない](https://groups.google.com/forum/#!topic/symfony-devs/69bIps2-CAg)
  * [独自のファイアウォールを定義するとエラーが発生する](https://groups.google.com/forum/#!topic/symfony-devs/Wo1ah4zYLes)
  * [ACLのメモリーリーク?](https://groups.google.com/forum/#!topic/symfony-devs/053aDa9c9lc)


Symfony2 開発ハイライト
-----------------------

[Master branch](http://github.com/symfony/symfony/commits/master):

  * [a57a4af](http://github.com/symfony/symfony/commit/a57a4aff55ef29562d4a657221ae4d01e3c53b7f "a57a4aff55ef29562d4a657221ae4d01e3c53b7f commit on github"): \[DomCrawler\] added a way to get parsing errors for Crawler::addHtmlContent() and Crawler::addXmlContent() via libxml functions
  * [258a1fd](http://github.com/symfony/symfony/commit/258a1fd7100c0e3418841d062d799debece554bc "258a1fd7100c0e3418841d062d799debece554bc commit on github"): moved makePathRelative to Filesystem
  * [bfb99bf](http://github.com/symfony/symfony/commit/bfb99bf219720f0867a9c7386fad79f8cdd998b5 "bfb99bf219720f0867a9c7386fad79f8cdd998b5 commit on github"): \[FrameworkBundle\] added a --relative option to assets:install
  * [0f7bf41](http://github.com/symfony/symfony/commit/0f7bf4155c2b2c1bf5d0aa202b7de1643b85c8e6 "0f7bf4155c2b2c1bf5d0aa202b7de1643b85c8e6 commit on github"): \[Console\] detect if interactive mode is possible at all
  * [b9ba117](http://github.com/symfony/symfony/commit/b9ba117208d170479ea9c2f7ffbe692c88a8b281 "b9ba117208d170479ea9c2f7ffbe692c88a8b281 commit on github"), [ee0fe7a](http://github.com/symfony/symfony/commit/ee0fe7a2b543bde26af63b3f162a1a5c8f2b81c5 "ee0fe7a2b543bde26af63b3f162a1a5c8f2b81c5 commit on github"): \[Validator\] added a SizeLength validator
  * [d6c4bfb](http://github.com/symfony/symfony/commit/d6c4bfb001f5f3c3847c3f7766467d16f7e8e322 "d6c4bfb001f5f3c3847c3f7766467d16f7e8e322 commit on github"), [ee0fe7a](http://github.com/symfony/symfony/commit/ee0fe7a2b543bde26af63b3f162a1a5c8f2b81c5 "ee0fe7a2b543bde26af63b3f162a1a5c8f2b81c5 commit on github"): \[Validator\] added a Size validator
  * [8b240d4](http://github.com/symfony/symfony/commit/8b240d4c22852ff76faced47ab7ab87e73c32092 "8b240d4c22852ff76faced47ab7ab87e73c32092 commit on github"): implementation of kernel.event_subscriber tag for services
  * [1467bdb](http://github.com/symfony/symfony/commit/1467bdb86837e132891dd1b5605248a736cca5fe "1467bdb86837e132891dd1b5605248a736cca5fe commit on github"): \[Routing\] added RouterInterface::getRouteCollection()

[2.0.x branch](http://github.com/symfony/symfony/commits/2.0):

  * [ed02aa9](http://github.com/symfony/symfony/commit/ed02aa9974a85c87eb2885a01af1df89312e0ade "ed02aa9974a85c87eb2885a01af1df89312e0ade commit on github"): \[Console\] fixed list 'namespace' command display all available commands
  * [72e82eb](http://github.com/symfony/symfony/commit/72e82eb595113652e6c963b46932635d634930e3 "72e82eb595113652e6c963b46932635d634930e3 commit on github"): \[Serializer\] replaced deprecated key_exists alias
  * [9ade639](http://github.com/symfony/symfony/commit/9ade639bb41423be611a023ab6966b855424f7be "9ade639bb41423be611a023ab6966b855424f7be commit on github"), [d535afe](http://github.com/symfony/symfony/commit/d535afeb9837d417d0453f6fa695bbab1ebfacba "d535afeb9837d417d0453f6fa695bbab1ebfacba commit on github"), [731b28b](http://github.com/symfony/symfony/commit/731b28bb921322e3a13f7fa98ef7e3071ee198e0 "731b28bb921322e3a13f7fa98ef7e3071ee198e0 commit on github"): \[composer\] added composer.json
  * [d6b915a](http://github.com/symfony/symfony/commit/d6b915a1746624e6fddc6e052bd8241456349a2b "d6b915a1746624e6fddc6e052bd8241456349a2b commit on github"), [369f181](http://github.com/symfony/symfony/commit/369f1810051895bf86502ffea34a3d2354ee0e16 "369f1810051895bf86502ffea34a3d2354ee0e16 commit on github"): \[FrameworkBundle\] added request scope to assets helper only if needed
  * [c13b4e2](http://github.com/symfony/symfony/commit/c13b4e2b55d88f5d93d2120b90a5155855d03daf "c13b4e2b55d88f5d93d2120b90a5155855d03daf commit on github"): fixed fallback catalogue mechanism in Framework bundle
  * [2db24c2](http://github.com/symfony/symfony/commit/2db24c264f186b50c7f3eddc923dd9f8fd4f452d "2db24c264f186b50c7f3eddc923dd9f8fd4f452d commit on github"): removed time limit for the vendors script
  * [1e7e6ba](http://github.com/symfony/symfony/commit/1e7e6ba305c4b7b66e49545d582325ed1ea5f9d7 "1e7e6ba305c4b7b66e49545d582325ed1ea5f9d7 commit on github"): \[HttpFoundation\] removed the possibility for a cookie path to set it to null (as this is equivalent to /)
  * [1284681](http://github.com/symfony/symfony/commit/128468193f5d23c8ac878f973c49ed191dd82a2a "128468193f5d23c8ac878f973c49ed191dd82a2a commit on github"), [b402835](http://github.com/symfony/symfony/commit/b4028350d26e5e47e620c3574e51daa471ec8c1c "b4028350d26e5e47e620c3574e51daa471ec8c1c commit on github"): \[BrowserKit, HttpFoundation\] standardized cookie paths (an empty path is equivalent to /)
  * [17af138](http://github.com/symfony/symfony/commit/17af13813ace8ed67221b8b185db72adc49e1040 "17af13813ace8ed67221b8b185db72adc49e1040 commit on github"): fixed usage of LIBXML_COMPACT as it is not always available
  * [d429594](http://github.com/symfony/symfony/commit/d429594afbdd2b74cf292c775582fe51cc22a317 "d429594afbdd2b74cf292c775582fe51cc22a317 commit on github"): removed separator of choice widget when the separator is null
  * [600b8ef](http://github.com/symfony/symfony/commit/600b8ef5af3ec680134527facff1a86f16f5ccf7 "600b8ef5af3ec680134527facff1a86f16f5ccf7 commit on github"): \[Validator\] added support for grapheme_strlen when mbstring is not installed but intl is installed
  * [e70c884](http://github.com/symfony/symfony/commit/e70c884f4905878d82b8b5c80d58d96f229290ab "e70c884f4905878d82b8b5c80d58d96f229290ab commit on github"): \[Bridge/Monolog\] fixed WebProcessor to accept a Request object
  * [5c8a2fb](http://github.com/symfony/symfony/commit/5c8a2fb48dfe09537db6ebdd77a52a3c90f409fe "5c8a2fb48dfe09537db6ebdd77a52a3c90f409fe commit on github"): \[Routing\] fixed route overriden mechanism when using embedded collections


