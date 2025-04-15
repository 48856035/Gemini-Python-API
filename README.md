#  [HW1](https://github.com/48856035/Gemini-Python-API/blob/main/HW1.ipynb):健身日程機器人

#  [HW2](https://github.com/48856035/Gemini-Python-API/blob/main/HW2.ipynb):全球氣溫變化視覺化分析

本專案使用 NOAA（GCAG）與 NASA（GISTEMP）提供的全球氣溫資料，透過 Python 視覺化全球暖化趨勢，並進行三種圖表分析。

資料來源：[DataHub - Global Temperature](https://datahub.io/core/global-temp)

---

##  視覺化圖表與分析說明

### 1️⃣ 折線圖：全球年平均氣溫變化趨勢（GCAG）

![](path/to/line_chart.png) <!-- 你可以上傳圖後貼這張圖的相對路徑 -->

**趨勢說明：**  
自1880年至今，全球年平均氣溫呈穩定上升趨勢。尤其自1980年後，升溫速度明顯加快，顯示全球暖化問題持續惡化。

---

### 2️⃣ 長條圖：每10年全球平均氣溫變化（GCAG）

![](path/to/bar_chart.png)

**趨勢說明：**  
1950年代以來，每個十年的氣溫平均都比前一個十年更高，特別是近30年（1990s～2020s）上升幅度顯著，證實氣候變遷正加速發生。

---

### 3️⃣ 雙線圖：GCAG vs GISTEMP 氣溫趨勢比較

![](path/to/double_line_chart.png)

**變數關係說明：**  
比較 NOAA（GCAG）與 NASA（GISTEMP）兩大機構的全球氣溫資料。雖數值略有不同，但整體趨勢高度一致，顯示資料具有良好一致性與可信度。

---

# [HW3](https://github.com/48856035/Gemini-Python-API/blob/main/HW3.ipynb)顧客分群分析：KMeans + PCA

本專案使用 Python 對隨機生成的顧客資料進行分群分析，透過 **KMeans 聚類** 與 **PCA 降維** 來探索顧客行為特徵，並進行視覺化呈現，最後根據分析結果提出實務應用建議。

---

## 專案內容簡介

### 分析步驟

1. **資料生成與預處理**
   - 隨機產生 50 筆顧客資料，包括：
     - 年消費額（annual_spending）
     - 購買頻率（purchase_frequency）
     - 顧客年齡（customer_age）
     - 會員年資（membership_years）
     - 偏好類別（preferred_category）
   - 對數值型欄位進行標準化處理（StandardScaler）

2. **聚類分析（KMeans）**
   - 使用肘部法則（Elbow Method）與輪廓係數（Silhouette Score）雙重驗證最佳群數（K 值）
   - 自動選擇最佳 K（根據 Silhouette Score 最大值）
   - 套用 KMeans 模型進行聚類

3. **群體特徵分析**
   - 計算每個群體的平均特徵值，分析消費行為模式與背景差異

4. **PCA 降維與視覺化**
   - 使用 PCA 將高維數據降至 2 維
   - 繪製顧客在 2D 空間中的分布圖，觀察群體邊界與關係

---

## 📈 視覺化成果

### 1️⃣ 肘部法則圖（Elbow Plot）
> 幫助判斷聚類數量的「拐點」，K 越大誤差越小，但收益遞減。

### 2️⃣ 輪廓係數圖（Silhouette Score）
> 衡量分群的「內聚性」與「分離性」，數值越接近 1 表示分群效果越佳。

### 3️⃣ PCA 2D 分布圖
> 使用兩個主成分顯示每個顧客在空間中的群體位置，不同顏色代表不同群組。

---

## 分群洞察與應用建議

以下為模型分出的三個顧客群體與可能的行銷策略：

### 🟣 群組 0：高價值常客
- 高年消費、高頻率、會員年資長
- **建議策略**：提供專屬優惠、提早通知新品、舉辦會員回饋活動

### 🟡 群組 1：新進高潛力顧客
- 消費額中高、頻率不穩定、會員年資短
- **建議策略**：發送歡迎禮包、推播提醒促銷、提升回購率

### 🔵 群組 2：低互動顧客
- 消費額與頻率偏低、年齡較高
- **建議策略**：寄送折價券、針對特定品類推播內容、提供客服關懷以提升黏著度

---

## 使用套件

- `pandas`：資料操作
- `numpy`：隨機數與數據處理
- `matplotlib`：視覺化圖表
- `scikit-learn`：
  - `StandardScaler`（標準化）
  - `KMeans`（聚類分析）
  - `PCA`（降維）
  - `silhouette_score`（群組效能評估）

---

## 結語

本分析展示了如何透過簡單但有效的機器學習技術對顧客進行分群，並藉由視覺化與解釋深入理解顧客行為，進而應用於實際行銷策略。適用於顧客關係管理（CRM）、行銷活動設計、推薦系統等場景。




