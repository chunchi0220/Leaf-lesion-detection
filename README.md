# Leaf-lesion-detection
使用yolov5模型來去將葉片上面的病變做偵測並分類
* 在github中有在exp34中存放模型訓練的結果，該次是訓練效果最佳的
* 可以先去yolov5的github git他下來，並準備好模型的執行環境
* 在yolo裡面的檔案最主要修改的是detect.py和train.py
* 剩下就可以針對模型辨識的結果作資料的後處理
## 系統概述
這個系統是將帶有葉枯病 (leaf blight) 與角斑病 (angular spot)的草莓葉片,透過 Yolov5 來辨別病變種類及位置的功能,找出在資料中草莓葉片疾病發生位置、並在兩種疾病中進行分類。
## 系統環境建置
要將yolov5成功on起來需要安裝好以下軟體：
* python
* pycharm
* CUDA
* cuDNN
* Anaconda
* pytorch
## 圖片標記-labelme
透過標記程式將圖片中要辨識的目標標記起來。標記完後會得到.json的標記檔。
資料集為草莓葉片圖片，有葉枯病 (leaf blight) 與角斑病 (angular spot)之葉片，Label 為 0 代表葉枯病，1 代表角斑病。
### 資料分割
將training data資料夾中的.jpg檔的圖片以及經由上個步驟剛轉完的.txt的標記檔，經由手動的方式，將資料集拆分為9：1的訓練集和測試集。
## yolov5
### 模型概述
模型採用的是 yolov5 的模型， yolov5 是一個非常適合用來做 object detection 的模型。
