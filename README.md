## PosturePro(日本語ver: 座ルール)
### 背景: 姿勢改善の社会的な意義とソリューション
昨今のリモートワークの普及により、私たちエンジニアはもちろん、長時間のデスクワーカーはどうしても姿勢が悪くなりがちです。
長時間の悪い姿勢は、肩こりや首こり、眼精疲労を招き、作業効率や労働意欲の低下に繋がります。
そのため、デスクワーカーの姿勢を改善するよう促すことができれば、社会全体の生産性を向上することに繋がると私たちは考えました。
そこで、AIを用いて画像から骨格を推定することで姿勢を測定し、姿勢に対する定量的な評価を可能としたサービスを考えました。
姿勢が悪くなっている場合に通知したり、総合的な姿勢に対してフィードバックを提供することでデスクワーカーの姿勢改善を目指します。

### 製品説明
私達は正しい姿勢を保つには２つのパラメータが重要だと定義しました。
- 腰の角度(Back Angle)
- 膝の角度(Knee Angle)
  
これらの角度を画像認識の技術を使い取得し、姿勢を評価します。
ユーザの疲労が溜まり、姿勢が崩れてきたと判定したときにSlackやDiscordを使ってユーザに通知を送ります。
最後に、１日の総合的な姿勢のサマリーをユーザにSlackやDiscordを使って送ります。

デスクワーク中の理想的な姿勢の例：
![deskwork_posture_002](https://github.com/jphacks/KB_2309/assets/67719334/abf8acfc-59cb-4d83-8385-5624f3f89209)

画像引用： https://www.irischitose.co.jp/blog/column/deskwork_posture/

### 特長

### 1. デスクワーカーの姿勢を常にAIが観察
- Webカメラを設置するだけですぐに観察可能。
- Webサービスなので特別なインストール不要。
- また、macOSを使用している場合、iPhoneをWebカメラとして使用することが可能。
    ![frame_145](https://github.com/jphacks/KB_2309/assets/67719334/c52b97d4-be4f-4042-afc4-63fc352b2ef0)

### 2. 姿勢が悪くなったら通知
- SlackやDiscordのようなデスクトップアプリケーションに通知を送信可能。デスクワークはもちろん趣味の時間でも姿勢改善が期待できるかも

### 3. 1日の総合的な姿勢を評価
- 最高な姿勢に対して自分の姿勢が総合的にどうであったかを視覚的にフィードバック

### 解決出来ること
- 客観的な姿勢観察および姿勢改善

### 今後の展望
- ChatGPTを用いて改善案をユーザに提案
- 時系列データから姿勢の移り変わりをグラフとして可視化
- 多方面からの姿勢を観察

## 開発技術
### システムアーキテクチャ
<img width="739" alt="image" src="https://github.com/jphacks/KB_2309/assets/67719334/222cf23b-1d2b-4900-ba05-481ebbda82c7">

### 活用した技術
- Deep Learning

### API・データ
- Discord API

### フレームワーク・ライブラリ・モジュール
- React（TypeScript）
- Flask（Python）
- OpenCV
- COCO model
