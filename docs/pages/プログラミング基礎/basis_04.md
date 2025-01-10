---
hide:
  - toc
---
# <i class="fa fa-arrow-circle-right" aria-hidden="true"></i> プログラミング基礎

## 4. ボタンを押すと数字カウントアップするように関数を追加してみよう

!!! Note
    関数とは、与えられた値をもとに、定められた独自の処理を実行し、その結果を返す命令のことです。

- 13行辺り: ``{/* 4-1 */}``	← この下にコードを追加してください
  

        // 数値型
        const [number,setNumber] = useState(0)


- 23行辺り: ``{/* 4-2 */}``	← この下にコードを追加してください
  

        const countUp = () => {

            {/* 5 */}
            // JavaScriptの基本の変数宣言
            let num = number + 1

            // 4-1の変数に代入
            setNumber(num)

            {/* 6-2 */}
            
        }


- 47行辺り: ``{/* 4-3 */}``	← この下にコードを追加してください
  

        <Text>{number}</Text>


- 50行辺り: ``{/* 3 */}{/* 4-4 */}``	← この下のコードを変更してください
  

        <Button onPress={() => countUp() }>
                <ButtonText>カウントアップ</ButtonText>
        </Button>


<img src="../../../images/プログラミング基礎/プログラミング基礎_1_06.png" width=400 ></img>

