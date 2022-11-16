---
hide:
  - toc
---
# <i class="fa fa-arrow-circle-right" aria-hidden="true"></i> 簡単なアプリを作ってみよう
  
## 4. マップを表示してみよう

- 10行辺り: ``{/* 4-1 */}``	← この下にコードを追加してください
  

        import {getLocationAsync} from '../util/Common'


- 17行辺り: ``{/* 4-2 */}``	← この下にコードを追加してください


        // 赤ピンの緯度
        const [latitude, setLatitude] = useState(0);
        // 赤ピンの経度
        const [longitude, setLongitude] = useState(0);
        // マップ中心部の緯度
        const [showLatitude, setShowLatitude] = useState(0);
        // マップ中心部の経度
        const [showLongitude, setShowLongitude] = useState(0);
        // 検索した店舗情報
        const [shopList, setShopList] = useState([])

        //　マップに表示する赤ピンの座標を変更
        const changePosition = (p) => {

            // 赤ピンの座標を変更
            setLatitude(p.latitude)
            setLongitude(p.longitude)

            // マップの中心を赤ピンの位置に変更
            setShowLocate(p)
        }

        // マップ中心部の座標を変更
        const setShowLocate = (info) => {

            // マップとホットペッパーAPIの緯度経度のパラメータ名が違うため分岐して読み取る
            if (info.lat) {
                setShowLatitude(Number(info.lat))
                setShowLongitude(Number(info.lng))
            } else if (info.latitude) {
                setShowLatitude(Number(info.latitude))
                setShowLongitude(Number(info.longitude))
            } else {
                alert('座標の変更に失敗しました')
            }

        }

        // 店舗の位置を示すピンを表示
        const displayStoreList = () => {
            return (
                shopList.map((shop, index) => {
                    return(
                        <MapView.Marker
                            key={index}
                            coordinate={{
                                latitude: Number(shop.lat),
                                longitude: Number(shop.lng),
                            }}
                            pinColor='#0000FF'    //ピンの色を指定
                            title={String(shop.name)}
                            description={String(shop.name)}
                            onPress={(e) => {
                                // マップにonPressイベントが伝播するのを止める 
                                e.stopPropagation();
                            }}
                        />
                    )
                })
            )
            }

        // 毎回のレンダリング後に実行
        useEffect(() => {
            // 現在地取得
            getLocationAsync().then(location => {
                // マップの座標を変更
                changePosition(location)
                setShowLocate(location)

            }).catch(e => {
                console.log(e)
                alert('現在地取得に失敗しました')
            })
        }, []);

        ```

        - 110行辺り: ``{/* 4-3 */}``	← この下にコードを追加してください
        ```
        <Text style={styles.text}>検索したい場所をタップしてください</Text>
        {/* マップ表示 */}
        <MapView 
            style={styles.map}
            onPress={p=>changePosition(p.nativeEvent.coordinate)}
            initialRegion={{
                latitude: latitude,
                longitude: longitude,
                latitudeDelta: 0.01, //小さくなるほどズーム
                longitudeDelta: 0.01,
            }}
            region={{
                latitude: showLatitude,
                longitude: showLongitude,
                latitudeDelta: 0.002, //小さくなるほどズーム
                longitudeDelta: 0.002,
            }}
        >
            <MapView.Marker
                coordinate={{
                    latitude: latitude,
                    longitude: longitude,
                }}
            />
            { shopList && 
                displayStoreList()
            }  
        </MapView>
        <Text style={styles.text}>緯度:{Math.floor(Number(latitude)*10000)/10000} 経度:{Math.floor(Number(longitude)*10000)/10000}</Text>



<img src="../../../images/アプリ開発/アプリ開発_1_07.png" width=300></img>

