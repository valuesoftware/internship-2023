---
hide:
  - toc
---
# <i class="fa fa-arrow-circle-right" aria-hidden="true"></i> カスタマイズしてみよう

## ホットペッパーの表示項目を変えてみよう

- 121行目辺りに移動し、下記のコードがあることを確認してください。

        {/*<Text style={styles.colum}>自由に項目名を記入しよう</Text>
        <Text style={styles.text}>{info.要素名を入力しよう}</Text>*/}

-  ホットペッパーAPIには様々な項目が用意されています。その中から表示したい内容を以下の表から選んでください(複数可)

	| 要素名 | 内容 |
	| --- | --- |
	| id | お店ID |
	| name | 掲載店名 |
	| name_kana | 掲載店名かな|
	| address | 住所 |
	| station_name | 最寄り駅 |
	| lat | 緯度 |
	| lng | 経度 |
	| genre | ジャンル |
	| catch | お店キャッチコピー |
	| capacity | 総席数 |
	| open | 営業時間 |
	| close | 定休日 |
	| wifi | WiFi有無 |
	| free_drink | 飲み放題有無 |
	| free_food | 食べ放題有無 |
	| parking | 駐車場有無 |
	| other_memo | その他設備 |

- 選んだ要素名を入力してみましょう。※コメントアウトの削除も忘れずに

      - 例えば飲み放題有無を表示したいとき

			<Text style={styles.colum}>飲み放題の有無</Text>
			<Text style={styles.text}>{info.free_drink}</Text>
