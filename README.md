# ITZU HUANG

## 👋 About Me

我是輔仁大學統計資訊學系的學生。大學期間，我透過統計相關課程、程式作業、資料分析專題與自主學習，逐步累積使用 **R、Python 與 SQL** 處理資料及進行統計分析的經驗。

目前有興趣並持續探索的方向包括：

- 應用統計
- 資料分析
- 生物統計
- 醫療資料分析
- 機器學習

除了課業與程式實作之外，我也有一般職場與接案工作的經驗，接觸過資料整理、文件處理、溝通、問題處理與成果交付。我希望這個 GitHub 能記錄實際完成的專案、課程成果與學習過程，清楚區分已使用過的工具與仍在學習的領域。

## 🎓 Education

**Fu Jen Catholic University**<br>
Department of Statistics and Information Science<br>
2023 – Present<br>
輔仁大學統計資訊學系

## 💼 Work Experience

### 中華郵政相關暑期外包工讀

- 使用 Excel 整理與輸入客戶寄件資料
- 使用內部系統處理或上傳郵件相關資料
- 列印寄件相關標籤，並協助行政與作業流程
- 在實際工作流程中處理資料正確性與例外問題

這段經驗讓我接觸到 **Excel-based data handling、data accuracy、internal system operation、administrative workflow** 與責任交付。

### 高中數學考卷編輯接案

- 協助整理高中數學試題與解答
- 使用 MathType 輸入數學公式，處理數學符號與版面
- 檢查內容與格式一致性，依需求進行修改
- 與委託者溝通內容與格式需求

這段經驗累積了 **attention to detail、mathematical notation、document editing、quality checking、communication** 與依需求修訂的經驗。

## 🛠️ Tools & Coursework

### Programming & Data

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=flat&logo=r&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)

### Python Data Analysis

`pandas` · `NumPy` · `scikit-learn`

### Database & Analytics

`MySQL` · `Power BI`

### Development & Applications

`Git` · `GitHub` · `Streamlit`

### Statistics Coursework

Statistical Inference · Regression Analysis · ANOVA · Experimental Design · Time Series Analysis · Multivariate Analysis · Nonparametric Statistics

## 🚀 Featured Projects

### [Diabetes Deterioration Risk Project](https://github.com/itzu-huang/Diabetes_Deterioration_Risk_Project) — Team Project

這是一個以第二型糖尿病資料為主題的團隊統計與資料分析專案，使用 100 位患者的 109 筆監測紀錄、33 項臨床摘要變數與 112,287 筆 CGM 讀數。臨床資料部分主要進行目前併發症的關聯分析與風險分層；CGM 資料部分則進行具有時間順序的短期分析與預測。

主要實作內容包括：

- 臨床併發症分類與風險分層
- HbA1c 迴歸分析
- K-means 與 Gaussian Mixture Model 分群
- CGM 指標分析與 AGP
- Markov 狀態轉移分析
- LSTM 短期血糖預測
- 臨床與 CGM 雙軸風險整合
- Monte Carlo 醫療成本情境分析

分析管線與可驗證結果包括：

- 以 `scikit-learn Pipeline` 封裝缺失值插補與標準化，並只在交叉驗證訓練折中配適
- 以患者為分組單位進行交叉驗證，避免同一患者的紀錄同時出現在訓練與測試資料
- 比較 Logistic Regression 與 XGBoost；三個併發症目標的 AUC 中位數約介於 0.805–0.862，未觀察到 XGBoost 穩定優於基準模型
- 以 SHAP 與勝算比輔助模型解釋，並比較逐人與跨患者合併訓練的 LSTM 設計
- 跨患者合併訓練的 LSTM 相對 persistence baseline 的改善中位數由 21.0% 提升至 37.2%

### Elder-friendly Decision Support App Prototype

團隊也完成高齡友善決策支援 App 原型，包含：

- Summary / CGM data input
- Risk quadrant visualization
- TIR / GMI / CV indicators
- AGP visualization
- Monte Carlo medical cost simulation
- Elder-friendly interface design

使用或實作的方法包括：

`Python` · `scikit-learn` · `Logistic Regression` · `XGBoost` · `K-means` · `Gaussian Mixture Model` · `Markov Model` · `LSTM` · `GroupKFold` · `Out-of-Fold Evaluation` · `Monte Carlo Simulation`

> 本專案屬於研究與方法實作原型，主要用於資料分析與模型探索，不應直接作為臨床診斷或治療依據。

### New Taipei City Building Permit Clustering Analysis

這是課程中的自主學習成果，使用新北市建築執照公開資料，資料約包含 13,072 筆建築案件與 10 個主要變數，涵蓋連續與類別資料。分析從公開資料選擇、欄位理解與整理開始，再進行分群與結果解釋。

實作流程包括：

- 以中位數處理缺失值，並對不同尺度的數值變數進行標準化
- 使用 K-means 探索建築案件的群組結構，並以 elbow method 輔助選擇群數
- 使用 PCA 將標準化資料降至二維進行視覺化
- 以階層式分群與抽樣 dendrogram 作為補充探索

在 K = 3 的設定下，分群將建築執照紀錄分成三個概略的規模群組：

- Small-scale buildings: 9,782 cases
- Medium-to-large buildings: 3,092 cases
- Very large buildings: 198 cases

此成果主要用於課程中的探索性資料分析練習。

## 📊 Data Mining & Selected Coursework

透過資料採礦課程與自主學習，我曾使用不同資料集練習資料前處理、特徵處理、分類、分群、關聯法則與模型評估。

### Data Preprocessing

Missing value handling · Label Encoding · One-Hot Encoding · Standardization · Discretization / Binning · Train/Test Split · Data transformation

主要使用 `Python`、`pandas` 與 `scikit-learn`。

### Classification

曾練習 Decision Tree、Random Forest 與 Support Vector Machine，並比較 Entropy、Gini、Accuracy 與 F1 Score 等概念。

### Feature Selection

曾接觸 Chi-square feature selection、SelectKBest、model-based feature selection 與 feature importance。課堂練習著重於比較不同特徵選擇方法與模型設定，並觀察特徵選擇對分類結果的影響。

### Association Rule Mining

曾練習 Support、Confidence、Lift、Association Rules 與 rule interpretation。除了尋找較高的 confidence，也會與單一條件的 baseline confidence 比較，判斷組合規則是否真的帶來額外資訊；例如組合規則的 confidence 若只略高於其中一個條件本身的 confidence，其額外解釋力可能有限。

### Clustering

曾使用 K-means 與 Standardization 探索資料中可能存在的群組結構，並練習 cluster interpretation。

### 📐 Survey Sampling — US Population Data

使用 USPOP 資料練習抽樣估計與誤差評估，包括：

- 以 ratio estimator 與 simple average 估計 65 歲以上人口比例及貧窮人口比例
- 比較不同估計方法的估計值與 bound on the error of estimation
- 練習 two-stage cluster sampling，以抽樣行政區與行政區內州別估計總人口及其變異數
- 討論 ratio estimation、stratified random sampling 與 two-stage cluster sampling 的適用情境

## 📚 Currently Learning / Exploring

- Applied Statistics
- Biostatistics
- Healthcare Data Analytics
- Longitudinal Data Analysis
- Predictive Modeling
- Machine Learning
- Statistical Computing
- Model Interpretation

## 📈 GitHub Activity

<div>
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=itzu-huang&show_icons=true&hide_title=true&hide_rank=true&hide=issues&include_all_commits=false&count_private=false&card_width=420" alt="GitHub overall statistics" />
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=itzu-huang&layout=compact&hide_title=true&langs_count=6&card_width=320" alt="Top languages" />
</div>

GitHub statistics reflect public repository activity and code composition and should not be interpreted as a ranking of technical proficiency.

## 🎯 What I Care About

**Statistics → Modeling → Interpretation → Real-world Problems**

在學習資料分析與建模時，我不只在意模型得到多少 Accuracy、AUC 或 R²，也希望逐步理解：

- 為什麼選擇這個方法？
- 方法建立在哪些假設之上？
- 資料是否支持這個結論？
- 是否可能存在 data leakage？
- 評估方式是否合理？
- 模型結果應該如何解釋？
- 哪些結論是資料可以支持的？
- 哪些結論超出目前資料可以回答的範圍？

我希望逐步將統計思維、程式工具與真實世界資料結合，做出具有實用性、可重現性與可解釋性的分析。

Thanks for visiting my profile! 👋
