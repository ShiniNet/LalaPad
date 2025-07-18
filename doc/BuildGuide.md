# ビルドガイド

> [!TIP]
> Github右上のリストボタン押下で目次（アウトライン）が表示され、工程全体を把握しやすくなります。
![2025-03-06_06h52_32](https://github.com/user-attachments/assets/600b59ae-39ec-4d79-b8a6-39246b630301)

　
## 準備
### キット内容物の確認

| 名前 | 数 |
|:-|:-|
|PCB（左右＋Dpad基板）|1式|
|トラックパッドモジュール|1個|
|Dパッドモジュール用カバー|1式|
|マイクロスイッチ|4個|
|ロータリーエンコーダー|2個|
|エンコーダーノブ|2個|
|ホットスワップソケット|48個|
|FFC（フレキシブルフラットケーブル）12PIN|1個|
|FFC（フレキシブルフラットケーブル）5PIN|1個|
|キーボードケース|1式|
|電源スイッチカバー|2個|
|マイコンカバー＆リセットピン|2個|
|マグネット|8個|
|メタルプレート|2個|
|滑り止めシール(2025/04/11～出荷分)|8枚|
|M3ネジ|8本|

![2025-03-07_06h03_27](https://github.com/user-attachments/assets/d0671da1-67af-4749-8326-778872f7eb3c)
<br/><br/><br/>
### 別途ご用意いただくもの

| 必須 | 名前 | 数 | 備考 |参考商品|
|:-|:-|---:|:-|:-|
|★|Seeed Studio XIAO nRF52840 |2個|マイコン本体。安価で入手性が高く、通信も安定しています。|[秋月電子](https://akizukidenshi.com/catalog/g/g117341/)|
|★|Kailh Choc V2互換スイッチ|48個|個人的にDeepSeaMiniがおすすめ。Lofreeなども適合。ChocV1も一応刺さります。|[遊舎工房](https://shop.yushakobo.jp/collections/all-switches/Kailh-Choc-V2%E3%82%B9%E3%82%A4%E3%83%83%E3%83%81) [Kailhswitch](https://kailhswitch.net/products/kailh-deep-sea-silent-min-low-profile-keyboard-switch)|
|★|MX軸ロープロファイルキーキャップ|48個|MX軸なら通常キーキャップも一部適合。|[Womier](https://womierkeyboard.com/products/skyline-r2) [Amazon](https://www.amazon.co.jp/stores/page/90526727-85E5-4BF8-AAD2-FC8A78C07BE3/search?ref_=ast_bln&store_ref=bl_ast_dp_brandLogo_sto&terms=%E3%83%AD%E3%83%BC%E3%83%97%E3%83%AD)|
|★|3.7Vリチウムポリマーバッテリー|2個|厚さ6.3mm幅47mm長さ110mm以下、JST PHコネクタ（ソケットのピッチ2.0mm）※[ソケットの極性に注意！](#%E3%83%90%E3%83%83%E3%83%86%E3%83%AA%E3%83%BC%E5%8F%96%E3%82%8A%E4%BB%98%E3%81%91)|[Amazon](https://www.amazon.co.jp/dp/B09DRJS75J/) [PHコネクタ単品](https://www.amazon.co.jp/dp/B01MXGWMS5/) |
|★|USB-Cケーブル|2本|充電、ファームウェア書き込み用。何百回と抜き差しする事になるのでマグネット式がおすすめ。||
||ケースの滑り止め|1式|グリップラスが評判良いです。テントするなら不要。4月出荷分から同梱済み|[Amazon](https://www.amazon.co.jp/dp/B08C9Z2K4C/])
||テンティング用品|2セット|マグネット式スタンドor三脚orクランプアーム。テントしないなら不要。|[Cramp](https://www.amazon.co.jp/dp/B08LCZ2X7M/) [Magnet](https://www.amazon.co.jp/dp/B0CXPR9BMF/) [Stand1](https://www.amazon.co.jp/dp/B0DKFMLWFX/) |★[Stand2](https://www.amazon.co.jp/dp/B0B6DSD1RK/)|

### 道具類

|必須| 名前 | 備考 |参考商品|
|:-|:-|:-|:-|
|★|はんだごてセット|アマゾンの温度調整付きはんだごて改善版15点セット（ピンセット、はんだ吸い取り線、フラックス、３C型のこて先入り）がおすすめ。|[amazon](https://www.amazon.co.jp/dp/B0CM1WJB5X/)|
||糸ハンダ|使用するはんだ線によっては定着がイマイチらしい。ENGINEERのSW-41が評判良いです。|[amazon](https://www.amazon.co.jp/dp/B001D7ME7Q/)|
|★|プラスドライバー|M3ネジ締める用。||
||フラックスクリーナー|フラックスで基板がべとべとになるので掃除用。||
||両面テープ|バッテリー固定用。無ければマスキングテープやビニテやガムテなどで代用可。||
||ピンセット|はんだ中のパーツ固定用。||
||マスキングテープ|はんだ中のパーツ固定用。||
||ニッパー|基板の分離用。||
||テスター|あると電源投入前に配線のショートをチェックできるので怖さが減ります。またトラブル発生時の問題の特定や、サポートのやりとりするために大変有用となっています。ワニ口タイプなら細いピン等を掴む事で細かい端子までチェックができます。|[amazon](https://www.amazon.co.jp/dp/B09S6Y9RM6/)|

※参考商品は全てアフィリエイトの含まれない直リンクです

※参考商品はあくまで参考であり、全ての商品が検証済みではないことにご注意ください



　
## PCBの組み立て
### PCBの分離
- ニッパー等で赤丸で囲ったライナー部分をカットします。（素手でも折れると思います
  
![2025-03-05_14h26_51](https://github.com/user-attachments/assets/1c5e5bdd-da6b-4275-abbe-b84fb229dd7a)
<br/><br/><br/>

### ホットスワップソケットのはんだづけ
- PCBの裏面の左右合計48箇所へホットスワップソケットを取り付けていきます。
- 温調はんだごてを使用している場合、大体３３０度ぐらいの温度設定にしておきます。 ※ご使用されるはんだに合わせて適宜調整してください。
- コテ先は2Cか3Cがおすすめ。体積が十分にあり、角度を調整すれば細かく扱うことも可能です。 ※標準装備の細いこて先は一見扱いやすそうに見えますが、パーツを十分に加熱できずはんだが弾かれやすいので非推奨です

![2025-05-18_16h28_01](https://github.com/user-attachments/assets/49421eb7-8753-42cc-b010-c76575105412)
<br/><br/>
  
> [!WARNING]
> - ソケットの向きに注意してください。ソケットのでっぱりとPCBのマークが一致するように。
> - はんだはたっぷり目で溶接してください。キースイッチ着脱中にソケットが脱落する原因になります。
  
![2025-03-05_14h10_34](https://github.com/user-attachments/assets/c9f43c88-1359-4b94-9ecb-af7309c57384)　
<br/><br/><br/>

### マイコンのはんだづけ
- PCBの表面にマイコンを仮付けします。マイコン付属のピンヘッダを装着し、PCBへ差し込んでマスキングテープ等で固定します。
- 以下左右とも同様に作業してください。
  
> [!WARNING]
> - ピンヘッダはあとで取り外します。流れではんだづけをしないように気を付けてください。

![2025-03-05_14h11_43](https://github.com/user-attachments/assets/94695031-f662-4c99-bf90-5ff79c9273cb)
<br/><br/><br/>

- マイコンのはんだ付けに苦戦する方が多いので動画を作りました。簡単です。
- https://x.com/NetShini/status/1907390264152613021
![Timeline 1_01_00_00_00](https://github.com/user-attachments/assets/915f85cf-b8ae-48f5-b45c-e734705da629)
<br/><br/><br/>

- 理想のマイコンはんだ付け例です（@shakupanさんより）
- https://x.com/shakupan_/status/1888458954734461194
- ![image](https://github.com/user-attachments/assets/8507a66c-3653-4c35-b656-78b4862213de)
<br/><br/><br/>



  
- PCB裏面にある穴からマイコンの背面パッドへはんだづけします（穴２つ、マイコンの背面パッド４つ）。
> [!TIP]
> - パッドとスルーホールにフラックスを塗布しておくことではんだの吸着が良くなります。
> - 先にはんだごてを穴に差し込んでマイコン背面パッド＆PCBのスルーホール（赤枠と青枠の金属部分）を2~3秒ほど余熱したらはんだをたっぷり流し込み、こて先を少し動かしてスルーホール＆背面パッドまではんだをなじませると良い感じになります。
> - この時、はんだがブリッジしても気にせず次に進みます。

  
![2025-03-06_06h41_05](https://github.com/user-attachments/assets/b79dbf74-fee1-403b-8209-d0a3142668b9)

<br/><br/><br/>

- ブリッジした余剰はんだを除去します。
- 穴へフラックスをたっぷり塗布し、はんだ吸い取り線をPCBの穴へ差し込み、はんだごてで十分に加熱すればはんだを除去できます。


![2025-03-06_06h43_14](https://github.com/user-attachments/assets/483b8095-c564-41a2-9119-43a3d331af84)
<br/><br/><br/>

- 仮固定用のテープとピンヘッダを取り外し、マイコンのピンホールをPCBへはんだづけします。（14か所）
> [!WARNING]
> - ピンヘッダは少しずつまっすぐ引き抜いてください。斜めに力が入ると前工程ではんだづけした箇所がはがれてしまいます。

![2025-03-05_14h14_01](https://github.com/user-attachments/assets/6964582b-b896-4b80-a3d0-869d40fc8b76)
<br/><br/><br/>

### ロータリーエンコーダーのはんだづけ
- PCBの表面からエンコーダーを差し込み、裏面から5か所はんだづけします。  
  
![2025-03-05_14h16_20](https://github.com/user-attachments/assets/3c965a6a-69f5-4381-8975-228ad65f82ce)
<br/><br/><br/>
  
この時点で7割の作業が終わりです。お疲れ様でした。　　
<br/><br/>

### PCBへトッププレートとマイコンカバーとキースイッチの取り付け
- PCBとトッププレートを張り合わせ、M3ネジを4か所締めます。
- マイコンカバー（＆リセットピン）とキースイッチを予め取り付けしておきます。

> [!WARNING]
> リセットピンは穴の形状に合わせて凸部分が外側へ来るようにマイコンカバーへ挿入してください。  
> キースイッチはこのタイミングで装着しておいてください。トッププレートがたわむ構造になっている為、組立後にキースイッチ装着の為に力をかけるとPCBが浮いてしまい、ソケットへの刺さりが甘くなってしまいます。

![2025-03-05_14h19_45](https://github.com/user-attachments/assets/3bae6b06-6a4b-4cf7-9f9a-f9544f9a9fd6)
![2025-03-07_06h07_31](https://github.com/user-attachments/assets/3e9e02fb-1a16-49c9-af80-9335025e07e3)
<br/><br/><br/>
　　
### FFC（フレキシブルフラットケーブル）をPCBに取り付け
- ソケット尾部にある爪をやさしく引き上げ、FFCの金属面が手前に見える方向に差し込み、ソケットの爪を押し下げます。
- 右手側にトラックパッドを装着する場合、右手側のPCBに太い方のFFC（トラックパッド用）、左手側に細い方のFFC（Dpad用）を装着してください。
> [!WARNING]
> ソケットの爪は大変壊れやすくなっておりますので、力を入れ過ぎないように注意してください。
> トラックパッドとDpadの左右入れ替え対応のため、FFCソケットは左右PCBにそれぞれ２つずつ搭載されています。太いFFCは太い方のFFCソケット。細いFFCは細い方のFFCソケットに差し込むようにしてください。
  
![2025-03-05_14h17_07](https://github.com/user-attachments/assets/285b2ccf-1c34-47ba-a621-3566103d62c3)
<br/><br/><br/>
　
## D-Padモジュールの組み立て
### マイクロスイッチのはんだづけ
- 青いスイッチ部分が円の外側に来るように4か所マイクロスイッチをはんだ付けします。
> [!WARNING]
> はんだ付けによってマイクロスイッチが浮き上がらないようにご注意ください。カバーが取り付けられなくなったり打鍵感の偏りが生じます。
> マイクロスイッチが基板の白枠の中に納まるように固定してください。

![2025-03-05_14h20_44](https://github.com/user-attachments/assets/ba3ddfe0-045e-4e32-8691-c76d01898ada)
<br/><br/><br/>
　　
### D-Padモジュールカバーの装着
- 十字キーパーツを仮組みします。
![2025-03-05_14h21_26](https://github.com/user-attachments/assets/f91e2ae1-883b-4a3c-ba11-48e900c39661)
<br/><br/><br/>

- DpadのPCBへDpadボトムカバーを嵌め込みます。
![2025-03-05_14h21_54](https://github.com/user-attachments/assets/e90cf2d4-0e0e-4339-8c59-39b13e86186a)
<br/><br/><br/>

- Dpadトップカバーとボトムカバーを嵌め込みます。嵌め込んだら目印の切り欠きまで時計回りに捩じってください。固定されます。
![2025-03-05_14h22_17](https://github.com/user-attachments/assets/357531fb-937c-40f5-8907-691a6c23b27e)
<br/><br/><br/>

　　　
## キーボードの組み立て
### ケースの仮組み立て
- ボトムプレートにマグネットとメタルプレートを取り付けます。
- ケースアウターの電源スイッチ穴へスイッチカバーを取り付け、ケースのアウターとボトムプレートを嵌め込んでいきます。
> [!WARNING]
> - マグネットには極性があります。ケースの左右で極性が反転するようにマグネットを装着し、ケース同士が磁力で引き合うようにしてください。  
> - 電源スイッチの部品は大変折れやすくなっております。後述の通り組立時に破損しないよう注意してください。

> [!TIP]
> ケースアウターの取り付けは先にスイッチのある方からPCBとボトムプレートを挿入して（スイッチ部分のかみ合わせに注意しながら、ケースのツメ部分が掛かるまで押し込む）、最期に反対側を押し込むと嵌め込みやすいです。
> ケースを分解するときは逆の手順で、先にスイッチとは反対側のツメから外すようにしてください。（スイッチ側はスイッチがひっかかるので先外し不可能です）

![2025-03-08_14h12_21](https://github.com/user-attachments/assets/d2af23ef-5593-4f75-8739-73fade2e1050)
<br/><br/><br/>
  
### トラックパッドとD-Pad取り付け
- ケースから伸びてるFFCにそれぞれトラックパッドとDpadを装着してください。
- ケース側の切り欠きに合わせて、各モジュールを嵌め込んでください。
![2025-03-05_14h24_44](https://github.com/user-attachments/assets/5239e8d7-7912-4432-9762-cbaa0a2b26cd)
![2025-03-05_14h25_02](https://github.com/user-attachments/assets/f9bc118b-f268-4945-bdb2-46b4f3b19548)
<br/><br/><br/>

### キーキャップとエンコーダーノブの取り付け
- 付属のエンコーダーノブとお好みのキーキャップを取り付けてください。
- 親指内側のキーは1.5U、それ以外は全て1Uサイズのキーキャップに適合します。

![2025-03-07_06h15_10](https://github.com/user-attachments/assets/ba893972-3135-4a2b-82ea-7c837c6570cf)
<br/><br/><br/>

## ファームウェアの書き込み＆動作確認(USB)
- GitHUBに公開している[ベースファームウェア（.uf2）](https://github.com/ShiniNet/LalaPad/tree/main/firmware)をダウンロードします。
  
![2025-03-16_12h55_31](https://github.com/user-attachments/assets/622aa44f-13e8-45d6-bbaf-bad7085e05db)

<br/>

- キーボードとPCをUSBに接続した状態でマイコンのリセットボタンを2回連打します。
![2025-03-08_11h57_30](https://github.com/user-attachments/assets/3b875866-41f1-4a10-88e1-2eb18f637fa2)
<br/>

- 正しく操作できていればPC側にマイコンのフォルダ(XIAO-SENSE)が表示されるので、先ほどダウンロードした.uf2ファイル（右側には"LalaPad_R.uf2"、左側には"LalaPad_L.uf2"のファイル）を１つずつコピーペーストします。
- 左右ともファームウェアの書き込みを完了させます。

![2025-03-16_12h57_06](https://github.com/user-attachments/assets/8c909d74-64e4-4c26-9a1d-1cf012d9f9e9)


<br/>

- 任意の[キーボード入力テスト用のWEBサイト](https://www.onlinemictest.com/ja/keyboard-test/)で動作確認を行います。
- 全ての物理キーが正しく判定されることを確認してください。

> [!WARNING]
> - デフォルトのキーマップではLayer1～3キーは上記サイトでは直接チェックできないので、これらはマイコンのLEDインジケーターの点滅を見て確認してください。（Layer1押下⇒1回点滅、Layer2長押し⇒2回点滅、Layer3長押し⇒3回点滅
> - 左手側を単独でテストすることはできませんので、右手側を先に起動した状態で左手側を起動しテストしてください。USB-Cケーブルが2本必要です。

> [!TIP]
> - 動作に問題がある場合、[組立のトラブルシューティング](https://github.com/ShiniNet/LalaPad/blob/main/doc/BuildGuide.md#%E7%B5%84%E7%AB%8B%E3%81%AE%E3%83%88%E3%83%A9%E3%83%96%E3%83%AB%E3%82%B7%E3%83%A5%E3%83%BC%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0)を参考にしてください。

![2025-03-08_12h21_48](https://github.com/user-attachments/assets/8bf01cfd-ec55-40e2-b00a-e12b5ed9a7f6)
<br/>
　
## バッテリー取り付け
- PCBへ用意したリポバッテリーのコネクタを接続してください。
- バッテリー接続後、軽く動作チェックをして問題なさそうなら、バッテリーをケースへ両面テープ等で固定してください。

> [!WARNING]
> バッテリーには極性があります。ソケットに差し込む方向に対して右側がプラス（赤色）になるバッテリーを使用してください。

![2025-03-06_13h06_24](https://github.com/user-attachments/assets/3a825545-507e-4575-98ae-b9a0f3ec2c2f)

<br/><br/><br/>


# 完成！！

> [!TIP]
> [使い方](https://github.com/ShiniNet/LalaPad#%E4%BD%BF%E3%81%84%E6%96%B9)を参考に、楽しい自作キーボードライフを満喫してください！


<br/><br/><br/>

# 組立のトラブルシューティング

- DiscordのHelpチャンネルでも過去のトラブルの事例を確認することができますので、是非ご参加ください！ <BR/>
  ※招待コードはパッケージに同梱されています
- キーボードの使用方法や接続に関するトラブルシューティングは[こちら](https://github.com/ShiniNet/LalaPad/tree/main?tab=readme-ov-file#%E3%83%88%E3%83%A9%E3%83%96%E3%83%AB%E3%82%B7%E3%83%A5%E3%83%BC%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0)

- マイコンへのはんだづけトラブルが増えております！以下を参考にしっかりマイコンと基板の端子が接続されるようはんだを盛りましょう。
- ![image](https://github.com/user-attachments/assets/4deb97d7-06e8-46af-8530-14b157ab06e9)

<br/><br/>

## 特定のキーが動作しない
### 行単位でキーが動作しない（TabASDFGがまるごと動作しないなど）
- マイコンのはんだづけを確認
  
![2025-04-29_13h18_261](https://github.com/user-attachments/assets/7d72705f-6988-49b6-a107-83a6ecad9943)

<br/><br/>
  
### キーの列の制御がおかしい（押した場所と関係ない列のキーが動作するなど）
- マイコンのはんだづけを確認
  
![2025-04-29_13h25_38](https://github.com/user-attachments/assets/ac41bece-0ca9-49ee-bbd4-60c04a6a650f)

<br/><br/>

  
### 特定の１キーが反応しない
- ホットスワップソケットのはんだづけを確認
- キースイッチのピンが折れ曲がって挿入されていないか確認
- PC側の物理配列がUSモードになっているか確認
- 割り当てしているキーコードを変更して動作するか確認

<br/><br/>

## トラックパッドが動作しない
- キーボードの電源再投入して改善するか確認
- USB接続では動作するか確認
- FFC（フレキシブルフラットケーブル）がねじれて反転して接続されていないか確認
- 左右付け替えて動作するか確認
- マイコンのはんだづけ確認

![2025-04-29_13h35_56](https://github.com/user-attachments/assets/7835d387-2776-4112-a7e9-087b1fc45ab0)


<br/><br/>

## Dパッド（十字キー）が動作しない
- 他のキー入力にトラブルがないかを先に確認
- マイクロスイッチのはんだづけがシビアなので要確認
- FFC（フレキシブルフラットケーブル）がねじれて反転して接続されていないか確認
- DPADケースへ基板挿入時、切り欠き部分の向きが一致しているか確認
- 左右付け替えて動作するか確認

<br/><br/>

## ロータリーエンコーダーが動作しない
- エンコーダーのはんだづけ確認
- マイコンのはんだづけ確認
  
![2025-04-29_13h18_262](https://github.com/user-attachments/assets/14de23d0-3a8e-4406-a834-6952e0e08ada)


<br/><br/><br/>

## バッテリーからの給電およびバッテリーへの充電が上手く行われない
- マイコンのはんだづけ確認
  
![2025-05-04_15h27_52](https://github.com/user-attachments/assets/e1032005-fc64-44e0-a897-65f1641c8188)

