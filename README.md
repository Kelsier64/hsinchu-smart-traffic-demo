# 竹行先知｜作品展示

通勤壅塞預警與容量感知分流，2026新竹縣智慧沙盒創新計畫學生組作品。

[線上Demo](https://kelsier64.github.io/hsinchu-smart-traffic-demo/demo/) · [初選報告](report/proposal.pdf)

## Demo操作

1. 選擇路段、方向與日期。
2. 切換15／30分鐘預測及全日／通勤時段。
3. 選擇時點，查看預測、旅行時間曲線與MAE／RMSE。
4. 勾選「揭露事後實際值」比較結果。

使用國道1號六個有向門架配對、五個工作日、8,640筆真實觀測。9月2日提供測試預測，其他日期提供觀測回放。三種方法為維持目前值、歷史同時段與殘差校正；本次以維持目前值表現最佳。

## 本地執行

需要Python 3.10以上。在repository根目錄執行：

~~~bash
python scripts/serve_demo.py
~~~

開啟http://127.0.0.1:8765/。無需安裝套件或提供API金鑰。

## 資料與作品範圍

來源：[交通部高速公路局「交通資料庫」M04A](https://tisvcloud.freeway.gov.tw/history/TDCS/M04A/)。資料日期為2026/8/27、8/28、8/31、9/1及9/2，小客車代碼31。

這是歷史資料與統計基準的展示，使用事後更新資料並假設區間結束即可取得。市區AI預警、實地分流與交通改善仍屬後續開發。AI使用範圍見初選報告第六章。

此repo保留Demo、必要CSV、報告與本地啟動程式。[完整研究與驗證程式](https://github.com/Kelsier64/hsinchu-smart-traffic-sandbox/tree/codex/submission-replay-audit)另行保存。
