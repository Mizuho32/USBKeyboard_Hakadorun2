# USBKeyboard_Hakadorun2

同人誌「キーボード配列変換ハードウエアの作成」 (初出イベント 技術書典14) と、同人ハードウエア 「キーボード配列変換ハードウエア」のソースコードなど。

https://techbookfest.org/product/gU35fVzeBgVe7x7rqXSVYe


## キーボード配列変換ハードウエア (Hakadorun2) 使い方

### 接続
1. Hakadroun2の基板上のDIPSWを ON 側 に設定してください。
2. USBキーボードを直接Hakadorun2に接続してください (間にUSBハブを入れないでください)
3. Hakadorun2をPCなどに接続してください (PCとHakadorun2の間にUSBハブを入れることはできます)

認識しない場合、または認識するがキーの反応がおかしい場合は、Hakadorn2をいったん抜いて再度PCなどに接続してみてください。

### 設定
Hakadorun2の設定は、　Hakadorun2_Client.exe　を用いて行います。
Hakadorun2_Client.exe は リリースパッケージ (zip) ファイル内に含まれています。
Hakadorun2をPCに接続した状態で、Hakadorun2_Client.exeを以下いずれかの引数をつけて実行してください。

#### version
Hakadorun2のファームウエアバージョンを表示します。

#### update
キー配列の変更を行います。

1. "Enter the src key" と表示されたら変換対象のキーを入力してください
2. "Enter the dst key" と表示された変換先のキーを入力してください

以上により、1.で入力したキーを押下すると、代わりに2.のキーがPCなどに送られるようになります。

必要な変換の数だけ、この作業を繰り返してください。

#### reset
キー配列の変換設定をリセットします。

#### lang_ja_en / lang_en_ja / lang_none
英語キーボード / 日本語キーボードの変換設定を行います。

* lang_ja_en : USBキーボードが日本語配列 / PC(OS)の設定が英語 の場合に選択すると、日本語キーボードの刻印通りのキー入力でOSへの入力ができます
* lang_en_ja : USBキーボードが英語配列 / PC(OS)の設定が日本語 の場合に選択すると、英語キーボードの刻印通りのキー入力でOSへの入力ができます
* lang_none : 英語/日本語の切り替えを行いません。

#### macroX (X=0～3)
キーボードマクロの設定を行います。

1. "Enter keys to run macro..." と表示されたらマクロを発動させるためのキーを入力してください。複数のキーの同時押しに対応しています。複数のキーを同時におして、すべてのキーを押すのをやめると、キーが確定します。
2. "Enter key sequence for macro" と表示されたら、記録したキー操作を入力してください。5秒間入力が止まった場合、または記録上限に達した場合に記録は終了します。

以上により、1.で入力したキーを押すと、2.で行ったキー操作が実行されるようになります。

## Hakadorun2のファーム書き換え方法

後日記載・・・ (新しいファームを公開するタイミングまでには)