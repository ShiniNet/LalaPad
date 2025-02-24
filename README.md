# GliDe48
GliDe48は、Corneに丸型トラックパッドを搭載するスタイルを源流に、日本で流行ってるトラボ付きキーボード（keyball,roBa,Mona等）にインスパイアを受けたトラックパッド搭載型ワイヤレスキーボードです。
![image](https://github.com/user-attachments/assets/6d2ca347-bd2d-4d19-a1a7-67cd6367348d)
![image](https://github.com/user-attachments/assets/980e4df9-8f20-400f-a905-fab9b970171d)
※画像は開発中の物であり、製品版とはわずかに外観が異なる可能性があります。

　
## 特徴

- **有線＆ワイヤレス対応**
- **トラックパッド＆D-Pad搭載**：　左右の入れ替え対応
- **デュアルロータリーエンコーダー搭載**　
- **ロープロ48キー構成**：　ミニマルさを残しつつ、クリエイター、プログラマー向け用途を想定。
- **19mmピッチ**：　普遍的な使用感で、選べるキーキャップの幅が広い
- **ZMKファームウェア搭載**：　ワイヤレスに最適化された最強のファームウェア
- **大容量バッテリースペース**：　1000MAHクラスの3.7Vリポバッテリーを搭載可能
- **ケースの3Dデータを公開**：　ユーザー自身で好みのカラバリを作ったり改変したり、出力品を販売可能
<br/><br/>

## 製品の詳細

### 販売ページ
- 自作キーボードキット
[販売ページへのリンク](#)

## ビルドガイド
[ビルドガイドはこちら](https://github.com/ShiniNet/GliDe48/blob/main/doc/BuildGuide.md)


## ケースの3Dデータについて
[3Dモデルデータのダウンロード](#)


### 3Dプリント発注費用の目安（20250220時点
- DMM Make：　16,000円、送料無料（国内配送
- JLC3DP：　20$＋送料13$＋輸入消費税（国際配送

## 工事設計認証(技適)番号
- 秋月電子のモジュールを使用する場合：211-220207
<br/><br/>

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
- [右手側]🔵点滅：デバイスへ接続済み、🟡：接続待ち、🔴：切断
- [左手側]🔵点滅：セントラルへ接続済み、🔴：切断

#### レイヤー状態（レイヤー変更時）
- [右手側]🔵点滅：アクティブにしたレイヤー番号に応じて点滅します。


### デフォルトキーマップの概要
赤文字：長押しで出力  
青文字：Ctrl押しながら押下で出力  
空白：デフォルトレイヤーから変化なし  
Layer1~3キー：押してる間だけレイヤー変更  
2文字刻印されているキー：SHIFT押しながら押下で右を出力（一般的なキーボードと同様）
- デフォルトレイヤー（Windows向け）
![image](https://github.com/user-attachments/assets/e8ab12d1-77c2-4717-bbf9-fceb7991e168)


- セカンダリレイヤー（左：数字、右：テンキー）
![image](https://github.com/user-attachments/assets/e7eb257a-3ec5-4c90-b457-6c793b8db246)

- ターシャリレイヤー（予備）

- システムレイヤー（BLE接続先選択＆プロファイルクリア、ブートローダー、ZMK Studioロック解除Etc…）
![image](https://github.com/user-attachments/assets/11167f13-e23a-4041-ba2b-bdcc3217b17e)



### トラックパッドの機能
- マウスポインターの操作
- カーソル操作でマウスレイヤーに自動切替
- マウススクロールモード
- 低速モード
  
![image](https://github.com/user-attachments/assets/acd9b2de-2bcc-4bee-848d-981af18d1684)  

### キーマップの変更
#### ZMK Studioを使用
- Webブラウザ上で簡単に編集可能
- ネイティブアプリ版を使えばBLE接続のまま編集可能
- ファームウェアのビルド不要

　[ZMK Studioの詳細はこちら](#)

#### KeymapEditorを使用
- Webブラウザ上で簡単に編集可能
- ZMK Studioより詳細な設定が可能
- ファームウェアをビルドする為にGitHubアカウントが必要です

　[準備中](#)


### ファームウェアのカスタマイズ
　[準備中](#)
<br/><br/>

## よくある質問

**Q: バッテリーの持ちはどれくらいですか？**  
A: 1000mahバッテリー搭載で、セントラル側が毎日デスクワークに使用して1~2週間のバッテリー持ちを確認しています。周辺側はこれの更に数倍持つと思われます。

**Q: どんなOSに対応していますか？**  
A: ZMKファームウェアが対応している各OS（Windows,Linux,Android,macOS,iOS）のキーコードが利用可能です。詳しくは[ZMKキーコードリスト](https://zmk.dev/docs/keymaps/list-of-keycodes)

**Q: 日本語配列に対応していますか？**  
A: ZMKはUS配列を前提にしたファームウェアです。一応日本語配列向けのキーコード（INT1-5、変換、無変換など）は定義されているようですが検証が不十分です。貢献をお待ちしております。

**Q: デュアルトラックパッド化できますか？**  
A: 可能です。左手側のDpadモジュールを取り外しキーボードとトラックパッドをFFCケーブル12PINで接続したらキーボードを再起動してください。追加のトラックパッドモジュールとFFCケーブルはユーザーご自身で用意して頂く必要があります。
　　※セントラル側と比較して5ms程度レスポンスが低下する可能性があります。

**Q: なんで片側５列にしなかったんですか？ミニマルじゃないです**  
A: 僕がゲームしたいからです。
<br/><br/>

## トラブルシューティング

**Q: デバイスとのペアリングができません**  
A1:  マイコンのリセットボタンを押して、デバイスと再接続してみてください。

A2:  PCとキーボード双方のペアリング情報を一旦削除（BLE_CLR_ALL）して、再度デバイスとペアリングしてみてください。
   
**Q: BLE接続が不安定です**  
A1:  マイコンのリセットボタンを押して、デバイスと再接続してみてください。

A2: 集合住宅やオフィスなど混線しやすい環境ではUSB接続による使用を推奨します。

**Q: トラックパッドの初動がもたつきます**  
A1:  約5分間キーボードが操作されないとキーボードがアイドル状態に入り、トラックパッドがスリープします。再アクティブ化には0.3秒前後かかる仕様です。

**Q: トラックパッドの動作が不安定です**  
A1:  本キーボードは静電容量式トラックパッドを採用しています。周囲からの電磁ノイズやキャリブレーションのズレにより動作が不安定になる場合があります。その場合、マイコンのリセットボタンを押してキーボードを再起動するか、スイッチをOFFにして電荷を十分に抜いてからONにしてください。起動時にトラックパッドが再キャリブレーション(0.1秒)されます。※キャリブレーション中にトラックパッドに触れるとキャリブレーションが正しく行われない可能性があります。  
A2:　一般的な静電容量パネル（スマホ等）でありがちなゴーストタッチ対策をお試しください。

**Q: キーボードの初動がもたつきます**  
A1:  約１時間キーボードが操作されないとキーボードがスリープ状態に入り、BLE接続が解除されます。再アクティブ化に５秒前後かかる仕様になっています。
<br/><br/>

## 注意事項・免責
- 本キーボード自作キットは個人が趣味で開発した作品を頒布しているものであり、またユーザー自身がバッテリー等部品の選定や組み立てを行うという性質上、完成品に対して一般的な製品のような品質や安全性は保障されておらず、十分なサポートや保障を得られない可能性がある事をよく理解し、自己責任でご利用ください。
- 本キーボード自作キットを使用した際のいかなる損害についても、開発者は責任を負いかねます。
- 明らかな初期不良や、部品の欠品などがあった場合は販売元へBoothのメッセージよりお問い合わせください。※転売や海賊版対策の為、必ず製品を購入したアカウントから問い合わせを行ってください。
- 部品等を破損・紛失してしまった場合に備え、[BOM](doc/partsList.md)を一部公開していますのでご活用ください。※在庫情報が日々変動する為、具体的な調達先についてはこちらではご案内しておりません。
- [リポバッテリーの取り扱いにおける一般的な注意事項](doc/LipoWarn.md)を遵守してください。
- 同梱のケースは家庭用3Dプリンターによる出力品の為、嵌め込み部分など使用者の手元で研磨が必要になる場合があります。予めご了承ください。
- 配布している3Dデータは家庭用FDM方式の3Dプリンターに最適化された物であり、発注先や使用される素材や印刷方式によって出力品の特性はわずかに異なることから、すべてのケースにおいて適合を保証するものではありません。各自で調整の上、自己責任でご利用ください。
<br/><br/>

