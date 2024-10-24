# 2024Q4_cross_ex_arbitrager_release


## 項目概述
此程式接受輸入`binance`, `bybit`, `okx`, `bitget`, `bingx` 等交易所 兩相同合約交易對以及匯率，並且在偵測滿足價差的情況下使用api進行雙邊下單，以達成跨交易所對沖部位下單。


## 使用說明
1. 下載執行檔及secrets.json(下載該電腦系統即可)
2. 用記事本開啟secrets.json並填寫所需交易所的key及secret, 請確認綁定IP是否正確
3. 輸入摳頂貓帳密打開程式、登入，輸入標的->點擊"設定"->選取交易所1、 2的
4. 待程式讀取一下，會抓到合約1、2 的買賣 & 溢價資訊
5. 點選"瀏覽", 選擇secrets.json的儲存位址->"啟動API連線"
6. 若連線成功會出現交易所1,2的該幣種倉位
7. 設定交易所1.2目標倉位(一正一負)->點選"設定目標倉位"
8. 若設定成功會出現類似"[設定目標倉位] binance: 0.001, bybit: -0.001"的log紀錄
9. 設定單次下單數量、下單間隔、溢價指數小於x%(確認方向是否正確)
10. 點選"啟動套利" (windows看不到該按鈕請把視窗往右下角拉大)

## 注意事項
1. 請預先估算好兩邊交易所的目標倉位, 因為頻寬限制, 沒有偵測當下保證金餘額, 需使用者自己注意.
2. 多空方向由當下倉位與目標倉位兩者比較決定, 因此設定目標倉位之前, 須先進行 API 連線.
3. 完成交易後, 若要加倉也是要先計算出兩邊新的目標倉位, 並且再次設定
4. 途中可點擊"停止套利", 系統會在完全對沖後停止, 若要重新設定請重新填寫目標倉位並點擊"設定目標倉位"以及完成下單數量, 溢價等設定
5. windows請注意在每次開始程式之前都先同步時間以避免程式無法正常運行(開始 -> 設定 -> 時間與語言 ->立即同步)


## 更新日誌
詳情請查看 [CHANGELOG.md](CHANGELOG.md)。

## 版權信息
Copyright (c) 2024 Murmurcats NFT 社團，所有權利保留 [LICENSE](LICENSE)。

## 開發者
[hyctw](https://github.com/hyc5566)

## 協作者
[jeffrey1167](https://github.com/jeffrey1167)
[godgiraffe](https://github.com/godgiraffe)
[RRRobert](https://github.com/yuying990718)
[0xCatduck](https://github.com/0xCatduck)
