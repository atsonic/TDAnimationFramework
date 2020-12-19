# TDAnimationFramework
* 最小単位のアニメーションコンポーネントを連続再生するためのシステムです。
* TouchDesigner製
<br>

## バージョン
* TouchDesigner Commercial 2020.27390
<br>

## 概要
アニメーションを最小単位のコンポーネントで作成していく際のシステム考察です。
再利用可能で、複数人のチームで作成する際に役立つフレームワークの作成を目的としています。
またTouchDesignerにおけるメソッドチェーンの実装考察も兼ねています。
<br>

### コンポーネント概要
* `animationタグ`の付いたCOMP同士のみnodeを繋げることができるコンポーネント
* `animationタグ`が付いていないOPを繋ごうとするとアラートが表示される
* アニメーションはFPSと同じフレーム数で定義されるため1秒で完結する
* アニメーションの数値は-1~1と正規化した範囲で編集する
* 以下コンポーネントの共通パラメーター  
	`Play`・・・Toggle式で**On**にして一度再生すると**Off**になる。最終フレームで止まる。  
	`Loop`・・・Toggle式で**On**にして`Play`するとループ再生になる  
	`Init When finishded`・・・Toggle式でOnにして`Play`すると**Off**になったタイミングでアニメーションが初期化される  
	`Speed`・・・この値を変更することでアニメーションの再生時間を変化させる  
* 上記以外は作成者の自由にアニメーションをつけることを許可する
<br>

## Document Info
* Last Update：2020/12/17
* Author：Mao Takagi

## References
- [Animation COMP](https://docs.derivative.ca/Animation_COMP "Animation COMP")
- [Timer CHOP](https://docs.derivative.ca/Timer_CHOP "Timer CHOP")
- [OP Class](https://docs.derivative.ca/OP_Class "OP Class")
- [Connector Class](https://docs.derivative.ca/Connector_Class "Connector Class")
- [Animation COMP Callbacks](https://forum.derivative.ca/t/animation-comp-callbacks/6925 "Animation COMP Callbacks")
