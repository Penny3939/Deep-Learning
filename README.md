# Deep Learning
練習&amp;實作_ 使用TensorFlow套件
![image](https://github.com/Penny3939/Deep-Learning/assets/125810833/f65706e4-dbca-41f9-b2ba-faee7bfff91c)
![image](https://github.com/Penny3939/Deep-Learning/assets/125810833/a2606394-fd85-4c6f-97d4-3b3821220bb4)


## 如何安裝 DLIB  
(1)pip install Cmake  
(2)pip install boost  
(3)下載你需要安裝 dlib 的版本  
(可到https://github.com/sachadee/Dlib 下載)
(4)將下載的檔案放置你要執行的目錄底下 (例如我放在C:\Users\Penny 下)
(5)執行 pip install dlib-19.22.99-cp38-cp38-win_amd64.whl
(6)執行 import dlib 是否成功


## 人臉矩形框(圖片 vs WebCam)
![image](https://github.com/Penny3939/Deep-Learning/assets/125810833/39033055-4f48-4695-8f83-3daefd4324be)\
![image](https://github.com/Penny3939/Deep-Learning/assets/125810833/6b4eb668-5639-41ce-b0f9-8e2684ade972)\
利用Dlib函數庫的正向人臉檢測器get_frontal_face_detector進行人臉檢測，提取人臉外部矩形框，利用訓練好的Dlib的68點特徵預
測器，進行人臉68點面部輪廓特徵提取，把所辨識出來的人臉輪廓點給標記出來。其程式處理流程如圖下所示。  



## 人臉辨識實戰(加上了控制時間的參數）
人臉辨識實際上是對人臉進行編碼後再去計算兩張人臉的相似度，每張人臉
是一個128維的特徵向量，最後利用兩個向量的內積來衡量相似度。
• 首先先安裝 face_recognition
• 直接執行命令即可：pip --default-timeout=1000 install 
• face_ recognition人臉辨識的方法：
  (1)將想要辨識人臉的圖片進行編碼, 並將這些不同的人臉編碼建構成一個串列。編碼其實就是將人臉圖片映射成一個128維的特徵向量。
  (2)OpenCV讀取視訊並迴圈每一幀圖片，將每一幀圖片編碼後的128維特徵向量與前面輸入的人臉函數庫編碼串列裡的每個向量內積來衡量相似度，根據設定值來計算是否是同一個人。
  (3）對辨識出來的人臉打標籤。

