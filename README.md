![comp](data/001_comp.png)
# kaggle-Predict-Student-Performance-from-Game-Play
Predict Student Performance from Game Play コンペのリポジトリ

- directory tree
```
kaggle-Predict-Student-Performance-from-Game-Play
├── README.md
├── data <---- gitで管理するデータ
```

# Basics
## Overview(DeepL)

**コンペティションの目標**

このコンペティションの目標は、ゲームベースの学習中の学生のパフォーマンスをリアルタイムで予測することです。ゲームログの最大級のオープンデータセットで学習させたモデルを開発することになります。

あなたの仕事は、ゲームベースの学習における知識追跡手法の研究を進めることです。教育用ゲームの開発者をサポートし、生徒にとってより効果的な学習体験を提供することができます。

**文脈**

学習は楽しいものであるべきです。この教育手法では、ゲームの枠組みの中で教育コンテンツに取り組むことができるため、楽しくダイナミックに学習することができます。ゲームベースの学習は、ますます多くの教育現場で利用されていますが、ゲームベースの学習を改善するためにデータサイエンスと学習分析の原則を適用できるオープンデータセットの数は、まだ限られています。

ゲームベースの学習プラットフォームの多くは、個々の学生をサポートするための知識トレーシングを十分に活用していません。知識トレーシングの手法は、オンライン学習環境やインテリジェントチュータリングシステムの文脈で開発・研究されてきました。しかし、教育用ゲームにおけるナレッジトレーシングにはあまり焦点が当てられていません。

コンペティション主催のField Day Labは、Wisconsin Center for Educational Researchにある公的資金を使った研究室です。多くのテーマや年齢層に対応したゲームをデザインし、現代の研究を一般に紹介するとともに、ゲームデータを活用して人々の学習方法を理解しています。フィールド・デイ・ラボは、アクセシビリティに配慮し、すべてのゲームを無料で誰でも利用できるようにしています。また、Learning Agency Labのような非営利団体とも提携しており、社会貢献のための学習ベースのツールやプログラムを科学的に開発することに重点を置いています。

成功すれば、ゲーム開発者が教育用ゲームを改善できるようになり、ダッシュボードや分析ツールでゲームを利用する教育者をさらにサポートできるようになります。ひいては、ゲームベースの学習プラットフォームがより広く支持されるようになるかもしれません。

## Data(deepL)

本コンテストはKaggleの時系列APIを使用します。テストデータは、将来のデータにアクセスできないようなグループ分けで配信される予定です。本コンペティションの目的は、オンライン教育ゲームによって生成された時系列データを使用して、プレイヤーが問題に正しく答えるかどうかを判断することです。3つの問題チェックポイント（レベル4、レベル12、レベル22）があり、それぞれに問題数が設定されています。各チェックポイントでは、そのセクションの過去のすべてのテストデータにアクセスすることができます。

## Columns
|name|Explanation|
|----|----|
|session_id|イベントが行われたセッションのID|
|index|そのセッションのイベントのインデックス|
|elapsed_time|セッション開始からイベント記録までの経過時間（ミリ秒単位）|
|event_name|イベントタイプの名前|
|name|イベント名（例えば、notebook_clickがノートブックを開いているのか閉じているのかを識別する）。|
|level|どのレベルで起きたイベントか（0〜22）|
|page|イベントのページ番号（ノートブック関連イベントの場合のみ）|
|room_coor_x|ゲーム内のルームを基準としたクリックの座標（クリックイベント時のみ）|
|room_coor_y|ゲーム内のルームを基準としたクリックの座標（クリックイベント時のみ）|
|screen_coor_x|プレイヤーの画面を基準としたクリックの座標（クリックイベント時のみ）|
|screen_coor_y|プレイヤーの画面を基準としたクリックの座標（クリックイベント時のみ）|
|hover_duration|ホバーが発生した時間（ミリ秒）（ホバーイベントの場合のみ）|
|text|このイベントの間、プレーヤーに表示されるテキスト|
|fqid|イベントの完全修飾ID|
|room_fqid|イベントが開催された部屋の完全修飾ID|
|text_fqid|textの完全修飾ID|
|fullscreen|プレーヤーがフルスクリーンモードであるかどうか|
|hq|高画質かどうか|
|music|ゲーム音楽のON/OFF|
|level_group|この行がどのレベルグループ（および問題グループ）に属するか（0～4、5～12、13～22）。|

# Log
## 20280308
- join!
- 初めてKaggle日記を書いてみた。
    - Log以外の部分を書いて今日は終了
- Kaggle上でGitHubって使えるのか？
    - とりあえず、今回は（今のところは）Kaggle Notebookを利用して参加 + Kaggle日記のみGitHubで管理で行こうと思う。
    - いつか（早い段階で）自分のPC上(or クラウド)を使ってコンペに参加したい