---
hide:
  - toc
---
# <i class="fa fa-arrow-circle-right" aria-hidden="true"></i> 簡単なアプリを作ってみよう

## 5. 星座、店舗情報を表示してみよう


- 13行辺り: ``{/* 5-1 */}``	← この下にコードを追加してください

        import ContentsTab from '../components/Molecules/tab/ContentsTab';


- 143行辺り: ``{/* 5-2 */}``	← この下にコードを追加してください

        {/* タブ表示 */}
        <ContentsTab 
            latitude={latitude} // 緯度
            longitude={longitude} // 経度
            setShowLocate={(l)=>setShowLocate(l)}
            setShopList={(list)=>setShopList(list)} // 店舗情報
        />


<img src="../../../images/アプリ開発/アプリ開発_1_08.png" width=300></img>

