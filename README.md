# BonDriver_FSUSB2i

trinity19683氏が作成した[BonDriver_FSUSB2i][link_wiki]に以下の対応を追加したものです。

* WinUSBドライバインストール用infファイルの追加
* VisualStudioバージョンの更新

[IT917x][link_it9170]を採用した以下のデバイスに対応しています。

| Vendor | Product        |  Vid   |  Pid   | Remarks                     |
| :----- | :------------- | :----: | :----: | :-------------------------- |
| KEIAN  | [KTV-FSUSB2N/V3][link_fsusb2v3] | 0x0511 | 0x0046 | 販売終了 S/N:K1212以降  |
| KEIAN  | [KTV-FSMINI][link_fsmini]     | 0x0511 | 0x0046 | 販売終了                    |
| MyGica | [PT275][link_pt275]       | 0x048d | 0xe275 |                             |

## インストール

### ビルド

リポジトリをクローンし、Visual Studio 2022で`src\FSUSB2i.sln`を開いてビルドします。

### ドライバのインストール

ドライバー署名の強制を無効にした状態でinfファイルを使用しWinUSBドライバをインストールします。

#### ドライバー署名の強制を無効にする方法

1. スタートメニューからキーボードのShiftキーを押しながら再起動をクリックします
2. 再起動後に表示されるメニューから以下の順に選択し再起動します
   1. トラブルシューティング
   2. 詳細オプション
   3. スタートアップ設定
   4. 再起動
3. 再起動後に表示されるオプション一覧から以下を選択します
   * 7)ドライバー署名の強制を無効にする

#### ドライバーのインストール方法

1. デバイスマネージャーを起動します
2. ほかのデバイス
3. ISDB-T 2045、ISDB-T USB Stickの右クリック
4. ドライバーの更新
5. コンピューターを参照してドライバーを検索
6. 参照ボタンからinfファイルのあるディレクトリを指定
7. このドライバーソフトウェアをインストールします
8. サウンド、ビデオ、およびゲーム コントロール
   * KEIAN KTV-FSUSB2V3/FSMINI ISDB-T Receiver Device (WinUSB)
   * MyGica PT275 ISDB-T Receiver Device (WinUSB)

## ライセンス

GNU General Public License Version 3.0

オリジナルドキュメントは`doc`ディレクトリ以下にあります。

[link_wiki]: https://ktvwiki.22web.org/?BonDriver_FSUSB2i&i=1
[link_it9170]: https://www.ite.com.tw/en/product/cate4/IT9170
[link_fsusb2v3]: https://www.keian.co.jp/archives/products/ktv-fsusb2v3
[link_fsmini]: https://www.keian.co.jp/archives/products/ktv-fsmini
[link_pt275]: https://www.mygica.com/product/isdbt-tuner/