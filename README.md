# practiceFinalAndStatic
【Java】finalとstatic修飾子の勉強メモ
# static修飾子

## static修飾子とは
「**[インスタンス]化しなくても、[クラス]から直接[メソッド]や変数にアクセスすることができるようにする修飾子**」です。

## 用語 
### クラスフィールド / クラスメソッド ( staticあり )
主に、[mainメソッド]などがそうですが

- staticな [メソッド]を「 **クラスメソッド / 静的メソッド** 」
- staticな 変数 を「**クラスフィールド / クラス変数 / 静的変数**」 

とよびます。

※ クラスメソッド から 下記の**「インスタンスメソッド」や「インスタンスフィールド」にアクセスはできません。**

### インスタンスフィールド / インスタンスメソッド ( staticなし )

- static をつけない [メソッド]を「 **インスタンスメソッド / 動的メソッド** 」
- static をつけない 変数 を「**インスタンスフィールド / インスタンス変数 / 動的変数 **」 

※こちらはインスタンス化が必要ですが、「**インスタンスクラスからクラスメソッド、クラスフィールドにアクセスすることは可能**」です。

##  static変数
変数に static修飾子をつけると、その変数が含まれる[クラス]を[インスタンス]化せずに変数にアクセスできるようになる。
static変数は「**その[クラス] から生成されたすべての [インスタンス] で共有される値」なので、グローバル変数のように使うことができます。

## static変数　の宣言と呼び出し方

static変数 の宣言の仕方はこちらです。

```
アクセス修飾子 static 型名 変数名
```

宣言した static変数,  の呼び出し方はこちらです。

```
クラス名.変数名
```
※ ちなみに、クラスフィールド・メソッド を [インスタンス]生成した上で呼び出すと、「作らなくてもいいよ」的なワーニングが表示されます。


## staticメソッド

### staticメソッド とは

そのクラスでどんなにインスタンスの生成をしても、「唯一の [メソッド]」であることを指します。



### staticメソッド の使い方

staticメソッドは、「**[new演算子]を使ってインスタンスを生成することなく呼び出すことができる」[メソッド]**です。

クラスフィールドと、インスタンスフィールドの違いで

- **インスタンスフィールド :  [インスタンス]ごとに値を保存できる。**
- **クラスフィールド : [インスタンス]を複数生成しても値が共有される**

ただ一つのクラスフィールドにアクセスするようになっています。

[インスタンス]を生成しなくても[メソッド]を呼び出すことが可能なため、「 **コードを短く書ける** 」というメリットがあります。
### staticメソッドの注意点

- staticメソッド内で扱う変数は、全てクラス変数かローカル変数でなければならない
- staticメソッドは、サブクラスに[継承]されない
- staticメソッドは [オーバーライド]することができない

## 参考文献・記事

- [Progate]
- [ドットインストール]
- [【Java入門】static修飾子の使い方総まとめ](https://www.sejuku.net/blog/24797)

[Progate]:https://prog-8.com/
[ドットインストール]:https://dotinstall.com/



[インスタンス]:https://qiita.com/takahirocook/items/ec01cdcbb440cf0d1cc4
[インスタンス化]:https://qiita.com/takahirocook/items/ec01cdcbb440cf0d1cc4
[アクセス修飾子]:https://qiita.com/takahirocook/items/e51b0b9d37d95ad587fe
[フィールド]:https://qiita.com/takahirocook/items/28df75a133049a74ece1
[フィールド変数]:https://qiita.com/takahirocook/items/28df75a133049a74ece1
[new演算子]:https://qiita.com/takahirocook/items/00f9f97592bf50831d39
[カプセル化]:https://qiita.com/takahirocook/items/e469a7c0539a0012868e
[クラス]:https://qiita.com/takahirocook/items/50cbbdca8e21539170e9
[メソッド]:https://qiita.com/takahirocook/items/5bfe43576d87a2a4006c
[mainメソッド]:https://qiita.com/takahirocook/items/f4635915337303de338c
[メソッドの呼び出し]:https://qiita.com/takahirocook/items/f4635915337303de338c
[コンストラクタ]:https://qiita.com/takahirocook/items/fa1822f2f22c3786593e
[引数]:https://qiita.com/takahirocook/items/5e5b0ba79e869f4a592e
[戻り値]:https://qiita.com/takahirocook/items/3b6fa670a1d6dd4a9386
[this]:https://qiita.com/takahirocook/items/d251ec4693c68f6b9538
[getter・setter]:https://qiita.com/takahirocook/items/27828bc8477735612021
[setter]:https://qiita.com/takahirocook/items/27828bc8477735612021
[getter]:https://qiita.com/takahirocook/items/27828bc8477735612021
[オブジェクト指向]:https://qiita.com/takahirocook/items/041ba7a096b71ab8ffd4
[継承]:https://qiita.com/takahirocook/items/6c84ea66a6e2ad536a37
[オーバーライド]:https://qiita.com/takahirocook/items/09dd8e5f56d6617ce45a
[オーバーロード]:https://qiita.com/takahirocook/items/b937c3c07126fe7e02a4
[this]:https://qiita.com/takahirocook/items/d251ec4693c68f6b9538
[super]:https://qiita.com/takahirocook/items/75a07131e7e791c8442c
[final]:https://qiita.com/takahirocook/items/5e0916d9bf28bcf68d0c
[final修飾子]:https://qiita.com/takahirocook/items/5e0916d9bf28bcf68d0c
[定数]:https://qiita.com/takahirocook/items/5e0916d9bf28bcf68d0c


