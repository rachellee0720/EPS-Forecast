# Financial Report Analysis and Earnings Forecasting：Application of Machine Learning Models
### :cactus: Introduction
1. Used **historical accounting information** of **past three years** to **forecast earnings per share (EPS)** or **diluted EPS** for the **next year**
2. Research process: establish dataset -> data preprocessing -> construct model & forecast EPS -> analyze forecast results
3. This study proposd three independent variable field combinations, two dependent variables, five data feature processing methods, and three time data models, with Random Forest Regressor, eXtreme Gradient Boosting Regressor, Deep Neural Network, Long Short-Term Memory, established 156 models
4. Obtained the result of mean absolute error = 1.391





# 財務報告分析及盈餘預測：機器學習模型之應用
### :seedling: 簡介
1. 使用過去三年的歷史會計資訊，預測未來一年的每股盈餘 或 稀釋每股盈餘
2. 研究流程：建立資料集 -> 資料前處理 -> 建構模型＆預測每股盈餘 -> 分析預測結果
3. 本研究提出三種自變數欄位組合 、兩種應變數、五種資料特徵處理方法、三種時間資料模式，搭配 隨機森林回歸器 (Random Forest Regressor)、極限梯度提升回歸器 (eXtreme Gradient Boosting Regressor)、深度神經網路(Deep Neural Network)、長短期記憶模型 (Long Short-Term Memory)後，建立了156個模型
4. 獲得 平均絕對誤差 = 1.391的結果

### :seedling: 研究方法 
1. 建立資料集：
	1. 資料：西元2012 ~ 2018年上市櫃 且 不為金融業或證券業 的台灣公司
	2. 應變數  (模型預測目標) x 2：下一年的每股盈餘 或 下一年的稀釋每股盈餘
	3. 自變數組合 (模型輸入值) x 3 ：欄位來自前三年資產負債表、綜合損益表以及現金流量表中的會計科目 
	4. 時間資料模式：定義訓練、驗證和測試資料集所使用的資料時間
	   
2. 資料前處理：
	1. 缺失值：補0 (假設公司未使用該欄位) 
	2. 資料特徵處理方法 x 5：將會計科目除以資產總額、營業收入淨額或公司市值等科目 或透過標準化等方式 消除不同公司之間的規模差距
3. 建構模型 ＆ 預測每股盈餘：
	1. 建置模型 x 156：隨機森林回歸器 x 72、極限梯度提升回歸器 x 72、深度神經網路 x 6、長短期記憶模型 x 6
	2. 驗證過程 (調整超參數)：交叉驗證
	3. 損失函數：平均絕對誤差 (Mean Absolute Error, MAE)
	4. 基準預測值：以當時所處時間點的數值直接作為下一年的預測值，再與模型預測值比較

### :seedling: 分析預測結果
1. 透過基準預測值，可發現機器學習和深度學習模型有能力預測下一年的每股盈餘
2. 隨機森林回歸器和極限梯度提升回歸器偏好不同的自變數欄位和資料特徵處理方法
3. 改善方向：
	 1. 只使用歷史財務資訊 無法精準預測 突發事件所導致下一年的公司每股盈餘之數值變化 -> 增添市場、產業前景預測相關資訊
