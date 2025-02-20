# GliDe48
GliDe48は、Corneに丸型トラックパッドを搭載するスタイルを源流に、日本で流行ってるトラボ付きキーボード（keyball,roBa,Mona等）にインスパイアを受けたトラックパッド搭載型ワイヤレスキーボードです。
![image](https://github.com/user-attachments/assets/6d2ca347-bd2d-4d19-a1a7-67cd6367348d)
![image](https://github.com/user-attachments/assets/980e4df9-8f20-400f-a905-fab9b970171d)
※画像は開発中の物であり、製品版とはわずかに外観が異なる可能性があります。

## 製品概要

### 特徴

- **有線＆ワイヤレス対応**
- **左右分割型**
- **トラックパッド＆D-Pad搭載**：　左右の入れ替え対応
- **デュアルロータリーエンコーダー搭載**　
- **ロープロファイル**
- **48キー構成**：　ミニマルさを残しつつ、クリエイター、プログラマー向け用途を想定。
- **19mmピッチ**：　普遍的な使用感で、選べるキーキャップの幅が広い
- **ZMKファームウェア搭載**：　ワイヤレスに最適化された最強のファームウェア
- **大容量バッテリースペース**：　1000MAHクラスの3.7Vリポバッテリーを搭載可能
- **ケースにマグネット＆メタルプレート搭載**：　マグネット式スタンドや三脚によるテンティング対応（PCケースや冷蔵庫にも張り付きます
- **ケースの3Dデータを公開**：　ユーザー自身で好みのカラバリを作ったり改変したり、出力品を販売可能


## 商品詳細

### 販売ページ
- 自作キーボードキット
[販売ページへのリンク](#)

### キット内容物
- PCB（左右＋Dpad基板）
- トラックパッドモジュール
- Dパッドモジュール用カバー
- マイクロスイッチ4個
- ロータリーエンコーダー2個
- エンコーダーノブ2個
- キースイッチホットスワップソケット50個
- FFCケーブル12PIN1個、5PIN1個
- キーボードケース左右
- マグネット8個
- メタルプレート2個
- M3ネジ8本

### 追加で必要な物
- Seeed Studio XIAO nRF52840 2個：　安価で入手性が高く、通信も安定しています。
- Kail Choc V2互換スイッチ48個：　個人的にDeepSeaMiniがおすすめ。Lofreeなども適合。ChocV1も一応刺さります。
- MX軸ロープロファイルキーキャップ48個：　MX軸なら通常キーキャップも一部適合。
- 3.7Vリチウムポリマーバッテリー2個：　寸法xxxxx以下、ソケットのピッチ2.0mm　※ソケットの極性に注意！
- ケースの滑り止め：　グリップラスが評判良いです。テントするなら不要。
- USB-Cケーブル1本：　マグネット式がおすすめ。
- はんだごて一式：　アマゾンの温度調整付きはんだごてセットがおすすめ。
- プラスドライバー

### あると捗るもの
- テンティング用品：　マグネット式スタンドor三脚orクランプアーム（スマホ用カメラ用などを流用可能
- テスター：　電源投入前に配線のショートをチェックできるので怖さが減ります。


### ビルドガイドへのリンク
[ビルドガイドはこちら](#)


## ケースの3Dデータについて
[3Dモデルデータのダウンロード](#)


### 3Dプリントを外注した時の費用の目安（20250220時点
- DMM Make：　16,000円、送料無料（国内配送
- JLC3DP：　20$＋送料13$＋輸入消費税（国際配送


## 使い方

### 電源の入れ方、充電方法

- 電源スイッチをON（奥行き側）にするか、USB-Cケーブルをマイコンに接続すると起動します。
- 充電はUSB-Cポート経由で行います。電源スイッチのONOFFの状態によらず、バッテリーが充電されます。
　※キーボードを充電したままの外出や就寝は控え、絶対に目を離さないようにしてください。
- バッテリー残量はキーボード起動時にLEDインジケーター（後述）に表示されます。

### PC等デバイスへの接続と使用
- セントラル（右手側）の電源投入後、周辺（左手側）の電源を投入し、デバイス上でBLE機器を検索してペアリングします。
- 各デバイス側でキーボードの物理レイアウトをUS配列に設定してください。

### LEDインジケーターの読み方

#### バッテリーステータス（起動時）
- バッテリーレベルに応じて 🟢(100%)/🟡(30%)/🔴(10%) に点滅します。

#### 接続状態（バッテリーステータスが表示された後）
- 🔵点滅：デバイスへ接続済み、🟡：接続待ち、🔴：切断（セントラル側（右手側）のみ）
- 🔵点滅：セントラルへ接続済み、🔴：切断 （周辺側（左手側）のみ）

#### レイヤー状態（レイヤー変更時）
- 🔵点滅：アクティブにしたレイヤー番号に応じて点滅します。例えばレイヤー３を有効にした場合⇒3回点滅。


### デフォルトキーマップの解説
（キーマップ画像で説明）

### キーマップの変更
#### ZMK Studioを使用
- Webブラウザ上で簡単に編集可能
- ネイティブアプリ版を使えばBLE接続のまま編集可能
- ファームウェアのビルド不要
- 詳細はこちら

#### KeymapEditorを使用
- Webブラウザ上で簡単に編集可能
- ZMK Studioより詳細な設定が可能
- ファームウェアをビルドする為にGitHubアカウントが必要です
- 詳細はこちら

## 注意事項・免責
- 本キーボード自作キットは個人が趣味で開発した作品を頒布しているものであり、またユーザー自身がバッテリー等部品の選定や組み立てを行うという性質上、完成品に対して一般的な製品のような品質や安全性は保障されておらず、十分なサポートや保障を得られない可能性がある事をよく理解し、自己責任でご利用ください。
- 初期不良や部品の欠品などがあった場合は販売元へBoothのメッセージよりお問い合わせください。※海賊版対策の為、必ず製品を購入したアカウントから問い合わせを行ってください。
- 本キーボード自作キットを使用した際のいかなる損害についても、責任を負いかねます。
- 同梱のケースは家庭用3Dプリンターによる出力品の為、嵌め込み部分など使用者の手元で研磨が必要になる場合があります。予めご了承ください。
- 配布している3Dデータは家庭用FDM方式の3Dプリンターに最適化された物であり、発注先や使用される素材や印刷方式によって出力品の特性はわずかに異なることから、すべてのケースにおいて適合を保証するものではありません。各自で調整の上、自己責任でご利用ください。


## よくある質問

**Q: バッテリーの持ちはどれくらいですか？**  
A: 1000mahバッテリー搭載で、セントラル側が毎日デスクワークに使用して2週間前後のバッテリー持ちを確認しています。周辺側はこれの更に数倍持つと思われます。

**Q: どんなOSに対応していますか？**  
A: ZMKファームウェアが対応している各OS（Windows,Linux,Android,macOS,iOS）のキーコードが利用可能です。詳しくは[ZMKキーコードリスト](https://zmk.dev/docs/keymaps/list-of-keycodes)

**Q: 日本語配列に対応していますか？**  
A: ZMKはUS配列を前提にしたファームウェアです。一応日本語配列向けのキーコード（INT1-5、変換、無変換など）は定義されているようですが検証が不十分です。貢献をお待ちしております。

**Q: デュアルトラックパッド化できますか？**  
A: 可能です。左手側のDpadモジュールを取り外しキーボードとトラックパッドをFFCケーブル12PINで接続したらキーボードを再起動してください。追加のトラックパッドモジュールとFFCケーブルはユーザーご自身で用意して頂く必要があります。
　　※セントラル側と比較して5ms程度レスポンスが低下する可能性があります。
　　保守用部品リストはこちら

**Q: なんで片側５列にしなかったんですか？ミニマルじゃないです**  
A: 安〇先生、ゲームがしたい・・・です・・・（ゲームでは長押しで出さない物理キーとして修飾キーが必須だからです。WASDを1列右にスライドして使うのもアリだけど、そうするとTGBが消えるので某FPSゲーで困るのです・・・。


## トラブルシューティング

**Q: デバイスとのペアリングができません**  
A1:  マイコンのリセットボタンを押して、デバイスと再接続してみてください。

A2:  PCとキーボード双方のペアリング情報を一旦削除して、再度デバイスとペアリングしてみてください。
　　　キーボードのペアリング設定の削除方法：
   
**Q: BLE接続が不安定です**  
A1:  マイコンのリセットボタンを押して、デバイスと再接続してみてください。

A2: 集合住宅やオフィスなど混線しやすい環境ではUSB接続による使用を推奨します。

**Q: トラックパッドの初動がもたつきます**  
A1:  約10分間キーボードが操作されないとキーボードがアイドル状態に入り、トラックパッドがスリープします。再アクティブ化には0.3秒前後かかる仕様です。

A2: 　ファームウェアの構成を変更することで、トラックパッドの自動スリープ機能をオフにしたり、閾値を変更することができます。代わりにバッテリー持ちが悪化します。

**Q: トラックパッドの動作が不安定です**  
A1:  通信状況の悪化や、キャッシュの蓄積により不安定になる場合があります。リセットボタンを押して、キーボードを再起動してみてください。

**Q: キーボードの初動がもたつきます**  
A1:  約１時間キーボードが操作されないとキーボードがスリープ状態に入り、BLE接続が解除されます。再アクティブ化に５秒前後かかる仕様になっています。

A2: 　ファームウェアの構成を変更することで、キーボードの自動スリープ機能をオフにしたり、閾値を変更することができます。代わりにバッテリー持ちが悪化します。


## ライセンス
本プロジェクトは [xxxxライセンス](LICENS) のもとで公開されています。

[ファームウェアのライセンス](#)
[3Dモデルデータのライセンス](#)
