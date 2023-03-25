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
- Tableクラスの要否
- Black JackのViewのisuue割り振り
