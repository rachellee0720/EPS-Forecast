# Financial Report Analysis and Earnings Forecasting：Application of Machine Learning and Deep Learning Models

## :wave: Introduction
1. Used&nbsp; ***historical accounting information of past three years***&nbsp; to &nbsp;***forecast earnings per share (EPS)***&nbsp; or &nbsp;***diluted EPS***&nbsp; for the &nbsp;***next year***&nbsp;.

2. This study proposes three independent variable field combinations, two dependent variables and five data feature processing methods, adopts four kinds of models (random forest regressor, eXtreme gradient boosting regressor, deep neural network, and long short-term memory), and established a total of &nbsp;***144 machine learning models***&nbsp; and &nbsp;***12 deep learning models***&nbsp; in the end.

3. Obtained the result of mean absolute error = 1.391.


## :running_man: Process
1. **Create dataset**
	1. ```Data source:``` companies that were listed on the Taiwan Stock Exchange (TWSE) or Taipei Exchange (TPEx) from 2012 to 2017 and are not in the financial or securities industry.
	2. ```Dependent variables (aka learning objective or prediction target of model) x 2:``` next year's EPS or next year's diluted EPS.
	3. ```Independent variable field combinations (aka model's learning resource) x 3:``` use the accounting information from the previous three years' balance sheet, comprehensive income statement, and cash flow statement to form the fields of dataset.
	
2. **Data preprocessing**
	1. ```Missing value:``` fill with 0 (assuming the company didn't use those accounts).
	2. ```Data feature processing methods x 5:``` divide dataset fields by accounting information such as total assets, net operating income, company market value or outstanding shares, or standardize to eliminate the size gap between different companies.
	
3. **Build models & Forecast EPS**
	1. ```Build 156 models:``` random forest regressor x 72 + extreme gradient boosting regressor x 72 + deep neural network x 6 + long short-term memory x 6.
	2. ```Validation process (tuning hyperparameters):``` cross validation & grid search.
	3. ```Loss function:``` mean absolute error.
	4. ```Baseline forecast values:``` the value of EPS or diluted EPS in the third year is directly used as the forecast value of EPS or diluted EPS for the next year.

## :tada: Results
1. After comparing with the Baseline forecast values, it can be found that the &nbsp;***machine learning***&nbsp; and &nbsp;***deep learning models have the ability***&nbsp; to predict the EPS or diluted EPS of the next year.

2. &nbsp;***Random forest regressors***&nbsp; and &nbsp;***eXtreme gradient boosting regressors***&nbsp; prefer different data feature processing methods, and also have &nbsp;***different views on feature importance***.

3. Models &nbsp;***can't  accurately predict the huge changes in the companys' EPS or diluted EPS***&nbsp; caused by unexpected events if it &nbsp;***only learn form historical financial information***.

-----

# 財務報告分析及盈餘預測：機器學習和深度學習模型之應用

## :wave: 簡介
1. 使用&nbsp;**過去三年**&nbsp;的&nbsp;**會計資訊**&nbsp;，&nbsp;**預測未來一年**&nbsp;的&nbsp;**每股盈餘**&nbsp; 或 &nbsp;**稀釋每股盈餘**。

2. 本研究提出三種自變數欄位組合 、兩種應變數、五種資料特徵處理方法，使用四種模型(隨機森林迴歸器 Random Forest Regressor 、極限梯度提升迴歸器 eXtreme Gradient Boosting Regressor、深度神經網路 Deep Neural Network 以及 長短期記憶模型 Long Short-Term Memory)，最終共&nbsp;**建立**&nbsp;了&nbsp;**144個機器學習模型**&nbsp;和&nbsp;**12個深度學習模型**。

3. 獲得&nbsp;平均絕對誤差 = 1.391的結果。

## :running_man: 流程
1. **建立資料集**
	1. ```資料來源：```西元2012 ~ 2017年在臺灣證券交易所上市或在證券櫃檯買賣中心上櫃且不屬於金融業或證券業的公司。
	2. ```應變數 (模型學習/預測目標) x 2：```下一年的每股盈餘 或 下一年的稀釋每股盈餘。
	3. ```自變數欄位組合 (模型學習資料) x 3：```使用前三年資產負債表、綜合損益表以及現金流量表中的會計資訊以組建資料集欄位。
	
2. **資料前處理**
	1. ```缺失值：```補0 (假設公司未使用該會計科目)。
	2. ```資料特徵處理方法 x 5：```將資料集欄位除以資產總額、營業收入淨額、公司市值或流通在外股數等會計資訊 或 透過標準化等方式，以消除不同公司之間的規模差距。
	
3. **建構模型 ＆ 預測每股盈餘**
	1. ```建置模型 x 156：```隨機森林迴歸器 x 72 + 極限梯度提升迴歸器 x 72 + 深度神經網路 x 6 + 長短期記憶模型 x 6。
	2. ```驗證過程 (調整超參數)：```交叉驗證 ＆ 網格搜索。
	3. ```損失函數：```平均絕對誤差 (mean absolute error, MAE)。
	4. ```基準預測值：```以第三年每股盈餘或稀釋每股盈餘之數值直接作為對於下一年每股盈餘或稀釋每股盈餘的預測值。

## :tada: 結果
1. 與基準預測值比較後，可發現&nbsp;**機器學習**&nbsp;和&nbsp;**深度學習模型有能力預測**&nbsp;下一年的每股盈餘和稀釋每股盈餘。

2. **隨機森林迴歸器**&nbsp;和&nbsp;**極限梯度提升迴歸器**&nbsp;偏好不同的資料特徵處理方法，且&nbsp;**對欄位重要性的看法**&nbsp;也&nbsp;**不同**。

3. **只使用歷史財務資訊**&nbsp;**無法**&nbsp;使模型&nbsp;**精準預測**&nbsp;突發事件導致的公司每股盈餘的巨幅變動。
