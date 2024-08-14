# My-Paper - 應用MAMBA於CRF在中文醫學命名實體識別
Hugging Face(Private) : https://huggingface.co/UJForSchool
## 摘要
自然語言處理（NLP）領域是人工智慧(AI)中一個關鍵領域，它使機器能夠理解、分析和生成自然語言文本。近年來，深度學習和Transformer模型的崛起，以及大量可用的資料和強大的計算能力，推動了NLP的快速發展。NLP不僅在文本分類、機器翻譯和自動問答等方面取得了重要突破，還在情感分析、語音辨識和對話系統建構等領域實現了重要進展。但隨著處理序列長度和模型規模的增加，Transformer也面臨著計算效率下降的問題，基於上述原因，本研究透過Mamba模型，在命名實體辨識(NER)的問題上驗證，透過Mamba結構能夠更有效地處理長序列，並且能夠在計算上實現線性擴展，突破傳統Transformer在長序列上的計算瓶頸，並結合CRF加強序列中的依賴關係。本研究提的Mamba結合CRF模型，在中文醫療命名實體辨識資料集的測試，達到了91.9%的F1值。

## 模型架構圖
![image](https://github.com/arcaea/My-Paper/blob/main/Pic/%E6%A8%A1%E5%9E%8B%E6%9E%B6%E6%A7%8B%E5%9C%96.jpg)

## 模型訓練
![image](https://github.com/arcaea/My-Paper/blob/main/Pic/Algorithm%201%20.jpg)
