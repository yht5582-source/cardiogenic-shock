# 心因性休克 SCAI 分期

依 **SCAI SHOCK 分期（2019）** 與 **2022 更新及床邊檢核表**製作的互動分期判定器：輸入床邊、檢驗、支持治療與血行動力學數值，自動判定 Stage A–E 與心跳停止修飾詞（CA），並依分期提示處置，可記錄每次重新分期追蹤病程。

線上版：https://yht5582-source.github.io/cardiogenic-shock/

> ⚠️ **僅供臨床評估輔助與教學，不取代臨床判斷。** SCAI 分期只描述嚴重度，本身不規定治療；處置提示綜合其他指引與試驗，請依院內休克團隊流程。

## 分期判定邏輯

| 分期 | 判定 |
|---|---|
| E Extremis | CPR 進行中、乳酸 >8、最大支持下仍嚴重低血壓、需推注升壓劑、多次電擊，或灌流不足且已有支持下 pH <7.2 |
| D Deteriorating | 灌流不足＋已有支持，且需要 ≥2 種升壓或強心劑、加上 MCS、劑量持續增加、初始治療 ≥30 分鐘後惡化，或乳酸上升且 >2 |
| C Classic | 灌流不足：乳酸 >2、尿量 <30 mL/h、肌酸酐 ≥1.5 倍、四肢冰冷濕黏、意識改變或肝功能上升 |
| B Beginning | 相對低血壓（SBP <90、MAP <60 或較平時下降 >30 mmHg）或心率 >100，但沒有灌流不足 |
| A At risk | 以上皆無；可勾選高風險背景 |
| CA 修飾詞 | 心跳停止後昏迷（GCS <9），擔心缺氧性腦傷（2022 修訂） |

其他功能：
- **血行動力學計算**：MAP、休克指數、CPO（MAP × CO ÷ 451）、PAPi、RAP/PCWP；超出門檻會標紅。
- **五期對照表**：依 2022 床邊檢核表列出各期的身體檢查、檢驗與血行動力學。
- **處置提示**：依分期列出建議，並標註 CULPRIT-SHOCK、IABP-SHOCK II、ECLS-SHOCK、DanGer Shock 等試驗。
- **病程追蹤**：每次重新評估時記錄分期，顯示分期變化軌跡。
- **一鍵複製摘要**：可貼到病歷。

## 使用方式

直接用瀏覽器開啟 `index.html` 即可，不需安裝或建置。

## 在地化設定

| 項目 | 位置 |
|---|---|
| 分期判定 | `<script>` 內 `calc()` |
| 處置提示 | `MG` |
| 床號 | 網頁右側「床號設定」 |

## 資料與隱私

- 所有資料只存在該瀏覽器的 `localStorage`，不會上傳。
- 只記錄床號，請勿輸入姓名或病歷號。

## 依據

1. Baran DA, Grines CL, Bailey S, et al. SCAI clinical expert consensus statement on the classification of cardiogenic shock. *Catheter Cardiovasc Interv* 2019;94:29–37.
2. Naidu SS, Baran DA, Jentzer JC, et al. SCAI SHOCK stage classification expert consensus update: a review and incorporation of validation studies. *J Am Coll Cardiol* 2022;79:933–946；SCAI SHOCK Bedside Checklist 2022.
3. van Diepen S, et al. Contemporary management of cardiogenic shock: a scientific statement from the AHA. *Circulation* 2017;136:e232–e268.
4. Byrne RA, et al. 2023 ESC Guidelines for the management of acute coronary syndromes. *Eur Heart J* 2023;44:3720–3826.
5. CULPRIT-SHOCK（*N Engl J Med* 2017）、IABP-SHOCK II（*N Engl J Med* 2012）、ECLS-SHOCK（*N Engl J Med* 2023）、DanGer Shock（*N Engl J Med* 2024）.

## 授權

請依使用單位規定自行選擇授權方式（例如 MIT）。
