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

### New Taipei City Building Permit Classification & Clustering Analysis
**Data Mining Final Project**

[🔗 View Final Project](https://github.com/itzu-huang/Data_Mining_Coursework/tree/main/final-project/new-taipei-building-permit)

這是一份以新北市政府開放資料平台建築執照紀錄為資料來源的 Data Mining 課程期末專案。原始資料包含 14,243 筆紀錄與 29 個變數（29 variables）；清理後保留 13,072 筆有效 target 資料，以 `whether_for_public`（Public / Non-public）作為分類目標，並以建築規模、土地使用、建築用途、停車位與日期等資訊練習 supervised learning 與 clustering。

資料準備包括移除 identifier／high-cardinality 欄位、清理 numeric 欄位文字與異常格式、處理百分比欄位、轉換 ROC dates，以及建立 `licensing_year`、`licensing_month`、`permit_wait_days`、`construction_duration_days`、`total_parking_spaces`、`land_use_group` 與 `building_use_group` 等衍生變數。數值欄位使用 training-set median、類別欄位使用 training-set mode；target 缺失或無效值則移除。需要 train/test separation 時，preprocessing 只使用 training data fitted，以避免 data leakage。

監督式學習比較 Decision Tree（Gini、Entropy、tree complexity、feature selection 與 cross-validation）、Support Vector Machine（SVM；scaling、Linear／RBF concepts 與 C comparison）、Random Forest（number of trees、tree depth 與參數比較）、K-Nearest Neighbors（KNN；scaling 與 K comparison），以及 Hard Voting 與 Soft Voting。最終比較中，Random Forest 在 supervised models 中呈現較強的 testing performance；Soft Voting 顯示結合多個分類器的可能性，但不一定勝過最佳單一模型。

非監督式學習則以 K-Means、Elbow Method、SSE、Silhouette Score、Cluster Profile、Cluster Interpretation 與 majority-vote comparison 探索資料結構。這裡的 K-Means 較適合用來探索 building profiles / groups，而不是取代主要的 supervised classification。

## 📈 Regression Analysis Coursework

**Statistical Modeling Coursework in R**

Coursework progression from simple and multiple linear regression to statistical inference, categorical predictors, model diagnostics, remedial measures, model selection, polynomial regression, and interaction effects.

The repository emphasizes the statistical modeling workflow:

**Model specification → Inference → Assumption checking → Diagnostics → Remedial measures → Model comparison → Interpretation**

[🔗 View Regression Analysis Coursework Repository](https://github.com/itzu-huang/Regression_Analysis_Coursework)

## 📊 Data Mining Coursework & Learning Progression

這些課程作業與練習逐步建立資料前處理、模型評估、分類、分群與關聯法則的基礎，最後整合到上述 Data Mining Final Project。

[🔗 View Full Data Mining Coursework Repository](https://github.com/itzu-huang/Data_Mining_Coursework)

### Data Handling & Preprocessing

曾使用 `pandas` / DataFrame 處理 CSV、以 XML parsing 讀取資料，並練習 mean／median／mode imputation、identifier removal、data type transformation、equal-width／equal-frequency discretization、Label Encoding、One-Hot Encoding 與 Standardization。Bank、Titanic、ProductSales 與 YouBike 等資料集是逐步建立 preprocessing 基礎的 coursework exercises。

### Decision Tree Foundations & Feature Selection

練習 Gini impurity、Entropy、Information Gain、continuous-variable split points、Gini vs Entropy、tree depth 與 number of leaves，也比較 Chi-square feature selection、SelectKBest 與 model-based feature importance。比較 all features、Chi-square selected features 與 model-based selected features 時，觀察到減少特徵不一定會改善 testing performance。

### Validation, Overfitting & Evaluation

曾接觸 optimistic／pessimistic estimate、holdout validation、cross-validation、Leave-One-Out concept 與 parameter tuning。透過比較不同 `min_samples_split` 下的 training accuracy、testing accuracy、tree leaves 與 tree depth，觀察 training performance 上升而 testing performance 開始下降時，可能是 overfitting 的警訊；也練習 10-fold cross-validation 與 train/test performance comparison。

### Model Evaluation & Class Imbalance

練習 Confusion Matrix、Accuracy、Precision、Recall、F1 Score 與 Cost Matrix，並接觸 Random Under-sampling、Random Over-sampling 與 SMOTE。當 class distribution 或錯誤成本重要時，Accuracy 不一定足夠。

### KNN, SVM & Random Forest

- **K-Nearest Neighbors (KNN)**：One-Hot Encoding、scaling、distance-based classification，以及探索 K 如何影響 KNN performance。
- **SVM**：Label Encoding／numeric representation、StandardScaler、Linear SVM、RBF SVM concepts、C parameter 與 weighted F1 evaluation。
- **Random Forest**：ensemble of decision trees、`n_estimators`、`max_depth`、training/testing comparison 與 overfitting awareness。

### Ensemble Learning

以 Decision Tree、Random Forest、KNN 與 SVM 練習 Hard Voting 與 Soft Voting。在一次 Titanic coursework comparison 中，兩種 voting 方法改善了部分模型的表現，但最佳單一模型仍可能有較好的 testing performance；這是該次課堂比較的觀察，不延伸為普遍結論。

### Clustering & Interpretation

練習 K-Means、Elbow Method、SSE、Silhouette Score、cluster centroid、cluster profiling、cluster interpretation 與 majority-class mapping。Titanic clustering coursework 曾以 survival rate、fare、passenger class、sex 與 family-related variables 進行群組描述與命名。

### Association Rule Mining

保留 Support、Confidence、Lift、Association Rules 與 rule interpretation 的練習，也比較單一條件的 baseline confidence。一條組合規則即使有較高 confidence，也不代表組合本身一定提供大量額外資訊；若只比其中一個條件略高，其 incremental information 可能有限。

### Key Learning Takeaways

- Feature selection does not automatically improve predictive performance.
- Higher training accuracy does not necessarily mean better generalization.
- Preprocessing must be designed carefully to avoid data leakage.
- Accuracy should be considered together with Precision, Recall, F1, class balance, and error cost when appropriate.
- Ensemble models do not always outperform the strongest individual model.
- Clustering and classification answer different types of questions.

## 📐 Selected Statistical Coursework

### Survey Sampling — US Population Data

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
