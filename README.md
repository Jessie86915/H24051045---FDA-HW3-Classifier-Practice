# H24051045---FDA-HW3-Classifier-Practice

### 資料類型
    股票相關資料（時序資料）

### 資料預處理
    1. 將 Close Price （與前一天比較的）漲跌，存成新的 Column，做為分析項
    2. 切割資料：將 02-Jan-2009 ~ 29-Dec-2017 的資料設定為 Training_Data，將 02-Jan-2018 ~ 31-Dec-2018 的資料設定為 Testing_Data
    3. 資料視覺化：繪製散布圖與熱圖，做為選擇變數的依據
    4. 新增潛在變數：將 Open Price、High Price、Low Price （與前一天比較的）漲跌，存成新的 Column
    5. 重新繪製熱圖：做為選擇變數的依據
    6. 變數選取：選取相關係數 > 0.05 的變數為預測變數，最終以 Open Price、High Price、Low Price 的漲跌做為預測依據
    7. 切割資料：將資料分割成 train_X, train_y, test_X, test_y

### 結果分析
| Model               | Parameter                                  | Accuracy     |
| ------------------- | ------------------------------------------ | ------------:|
| SVC                 | C = 0.01, kernal = "rbf"                   | 82.14 %      |
| SVR                 | C = 0.1, gamma = 0.01, kernel = "rbf"      | 80.95 %      |
| Logistic Regression |                                            | 81.75 %      |
| Neural Network      | hidden_units = 10 , activation = 'sigmoid', l2 = 0.001, learning_rate = 0.01, epochs = 50, batch_size = 32 | 81.75 %      |
