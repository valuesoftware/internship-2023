---
hide:
  - toc
---
# <i class="fa fa-arrow-circle-right" aria-hidden="true"></i> カスタマイズしてみよう

## 文字の色やサイズを変えよう

- 176行目辺りに移動し、下記のコードがあることを確認してください。この部分が文字やレイアウト等の見た目を変えます。

        const styles = StyleSheet.create({
                container: {
                        flex:1,
                        backgroundColor: '#fff',
                        alignItems: 'center',
                        justifyContent: 'center',
                        paddingTop: Platform.OS === "android" ? StatusBar.currentHeight : 0
                },
                colum: {
                        fontSize:14,
                        fontWeight: "bold",
                        marginTop:10
                },
                text: {
                        fontSize:20,
                },
        });

!!! Note
    スタイルの書き方

                // 基本構文
                セレクタ {
                        プロパティ:値;
                }


    container、colum、textがセレクタと呼ばれる部分で、どの要素の見た目を変えるのか定義しています。<br>
    fontSizeやfontWeightがプロパティと呼ばれる部分で、そのセレクタのどこを変えるのか定義しています。

- 文字をどう変更したいか決めてみましょう。下記以外にもいっぱいあります。

    | 変える内容 | プロパティ | 値の書き方 |
    | --- | --- | --- |
    | 文字のサイズ | fontSize | 数字 |
    | 文字の色 | color |"#FF00FF"や"red" <br>[色を調べたいときは](https://developer.mozilla.org/ja/docs/Web/CSS/color_value) |
    | 文字の背景色 | backgroundColor| colorと同じ |
    | テキストの配置 | textAlign | "center","left","right" |
    | 文字を太字にする | fontWeight | "bold" |

!!! Note
	色のコードについて<br>
	`#`の後ろに6桁の16進数で色を指定することができます。この6桁は前から2桁ごとに、赤・緑・青の濃淡が決まります。<br>
	例えば赤にしたい場合は`#FF0000`

- 選んだプロパティをセレクタ`columと`、`text`に反映してみよう
    - テキストの背景色を変えたい時

			colum: {
				fontSize:14,
				fontWeight: "bold",
				marginTop:10,
				backgroundColor: "#FF00FF" ←を追加
			}

	- テキストの配置を真ん中にしたい時

			colum: {
				fontSize:14,
				fontWeight: "bold",
				marginTop:10,
				textAlign: "center" ←を追加
			}