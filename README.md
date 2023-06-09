# Log

## 3/11

土曜日15時
火曜日21時30分を目処にMTG

Google Docsに調べたことを共有
メンバーに報知したいことはDiscodeのチャットを使う

todo
- 各ゲームのルールを把握（ロジックの見通しをイメージするため）
- 必要な要件をGoogle Docsに書いていく
- 技術について調べる（調べたことはGoogle Docsに書いていく）
  - 決まったもの
    - Phaserの使い方について調べる
    - Github Actionsの使い方を調べる
  - これから決めるもの
    - Vue or Reactのメリット・デメリットを調べる
    - deploy環境（Front Backそれぞれの候補）について調べる
    - 使用するAPI候補など
- ワイヤーフレームでUIを各自作ってみる（次回MTGで共有）

次回MTG 3/14 21:30～
- 3/14に使用技術・要件の決定・ワイヤーフレームでUIのイメージを揃える

3/14以降に技術スタックの構成図・クラス図などを作成

## 3/14
- ゲーム（Black Jack）のルール・流れを確認
- Figmaによるプロトタイプを確認
- VueかReactか -> Reactを採用する方向
- deploy環境 -> Vercelを採用

todo
- クラス図・アクティビティ図を作成
  - Black Jack -> propan
  - Speed -> taisan
  - War -> Amnis
  - 参考：
    - クラス図 PlantUml
    - アクティビティ図 drawio/figma
- Vercelの使い方について調べる
- Linterは以下を試してどれを選ぶか（そもそもLinterを使う必要があるか）決定
  - eslint
  - prettier

次回MTG　3/18 15:00〜
- Sprint1（翌週末）のゴール・タスクを設定
- TypeScriptの環境共有

## 3/18
- ラミー以外のクラス図を作成・リポジトリ（class-diagram）に共有
- 3/25までの実装計画を策定（trelloに記載）

to do
- 3/19に1週目の進捗報告
- 環境は不明点あればdiscodeで共有

## 3/19進捗報告
1週目で以下を実施
- ゲーム概要把握
- 技術選定
  - TypeScript
  - Phaser
  - React
  - Cordova
  - Vercel
  
  ![image](https://user-images.githubusercontent.com/83019007/226162145-0b2bb02d-47d4-450c-9ba9-6928a3ab461a.png)

  
- 各ゲームのクラス図作成（class-diagramリポジトリに記載）
  - Black Jack
  - Speed
  - Poker
  - Texas Holdem
  - War
  - Rummy(未作成)
 
- 3/25までの予定 （詳細はtrelloに記載）
  - ロビー画面の開発
  - Black Jackの開発

# 3/21
- Black JackのModel, ロビー画面のissue割り振り
- Black Jackの開発期限を3/25 -> 3/28に延長

次回MTG 3/25 15:00〜
- Black JackのViewのisuue割り振りを行う


# 3/25

アジェンダ

- 各issueの消化状況
- pull request/ mergeの進め方
  - pull request出した人がマージする
- Tableクラスの要否　
  - あえて共通のものを作る必要性は低い
- Black JackのViewのisuue割り振り 

# 3/26

- 3/25時点の進捗
  - BlackJack作成中
  - Modelはおよそ作成した
    - 3/21〜3/25
    - テストコードも並行して作成
  - Viewは3/24に着手した
  
- 今後の予定
  - 3/28,29を目処にBlackJackをゲームとして遊べる状態にする
  - 3/30〜次のゲーム（War）に着手する

- 現状の課題認識
  - 残り約25日で全6ゲーム作成・クロスプラットフォーム対応に間に合わないかもしれない
    - 6ゲーム遊べる状態にする-> UIの改善 -> クロスプラットフォーム対応の予定
    - 特にRummyの作成が間に合わない可能性がある（設計できていない）
  - 設計に時間を使った割に、実装段階で修正することが多かった
    - クラス図でメソッドの説明やどの引数を取るのかを書いていなかった-> 認識齟齬があり、再度確認するというロスがあった
    - 今のところ、実装できなくて困るといった問題はないという認識
  - 環境の整備
    - Cordovaの環境を整えていない
    - ReactとPhaserの使い分けがわかっていない
    - Vercelへのdeployに失敗した
    
Feedback

- 全体の流れについて
  - チーム開発の目的として、複数のゲームであそべること・クロスプラットフォームに対応することが2大Topic。ゲーム数は大きな問題ではない。
  - BlackJackから作成するのは良い判断。BlackJackでトランプゲームの基礎を作ってほしい。
  - BlackJackの次はWarに取り組むことを推奨。Warでは拡張性のあるゲーム（BlackJackで作った土台が他のゲームでも利用できること）であることを確認してほしい。
  - その後Speed・Poker・TexasHoldem・Rummyの順番に作成することを推奨（これらは拡張性を確認することが目的）
  - UIは最初から作り込んだ方が良い。UIは影響範囲が大きく後から修正するのが大変になるため。
    - もし、後から修正するならゲーム自体を作成するメンバーとUIをゲーム横断で改善するメンバーに分けた方が良いかもしれない
  - BlackJackとWarをある程度の完成度で遊べるようにすることが次の2週間の目標
    - test・deployまで行うこと！
  - Warを作成したらそれぞれのメンバーがそれぞれのゲームを作る流れがいいかも。（2週間後のMTGで再確認）

- 設計について
  - 設計と実装を行き来するのは問題ない
  - 設計を変更したらクラス図も修正すること
    -　クラス図の情報量は問題ない
  - アクティビティ図はSpeedやPokerぐらいの分量がgood
    - ユーザーから見た操作を書けばok
    - 目安は10分で書ける分量
  
  
# 4/4

- ゲーム画面から前の画面の変数を呼び出してゲームを開始する

to do 


- CPUの動きを作成
- 難易度を調整できるようにする
- ゲーム画面プルリク
- 日曜日の進捗報告で困っていることを話すために、土曜日までに課題を共有する


# 4/9

現状の課題
- BlackJackがまだ完成していない
- ViewとControllerが未完成
- Reactで最初作っていたが、Phaserで作り直す必要があり、手戻りが発生した


- MVCをどうやって実現するか
  - PhaserのcreateメソッドはViewとControllerの両方が存在しており、分離が難しい
  - ViewとControllerの分離は完全にできなくても良い


feedback

- BlackJackの完成後War作成
- その後Speedを作成する
- 余裕があればPokerを作成してほしい
- ゲーム数よりはクオリティ（挙動が正しいこと）を優先してほしい
- 最低限Web上で動くようにしてほしい
- 余裕があればMobileやDesktopにデプロイする
- 苦しければDiscodeでAdminに呼びかける


BlackJack作成後、War, Speed, Pokerの作成を各自ですすめてしまうのも手？


# 4/12

- 進捗確認
  - プレイヤーからの入力を受けた後ループする処理がBlocker
  - 各画面UI統一した方が良いのではないか？

- To do
  - ゲームのループに関する仕様変更・ActionUI変更 -> Propan
  - Description/Animation/勝敗判定 -> taisan
  - プルリク確認 -> Amnis

- 次回4/14 21:30~
  - BlackJack完成
  - 次ゲームの割り振り（ゲーム単位でタスク調整）


