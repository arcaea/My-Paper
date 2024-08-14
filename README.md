# My-Paper \ 
應用MAMBA於CRF在中文醫學命名實體識別 \ 
Applying MAMBA with CRF in Chinese Medical Named Entity Recognition
Hugging Face(Model is Private) : https://huggingface.co/UJForSchool

## 摘要
自然語言處理（NLP）領域是人工智慧(AI)中一個關鍵領域，它使機器能夠理解、分析和生成自然語言文本。近年來，深度學習和Transformer模型的崛起，以及大量可用的資料和強大的計算能力，推動了NLP的快速發展。NLP不僅在文本分類、機器翻譯和自動問答等方面取得了重要突破，還在情感分析、語音辨識和對話系統建構等領域實現了重要進展。但隨著處理序列長度和模型規模的增加，Transformer也面臨著計算效率下降的問題，基於上述原因，本研究透過Mamba模型，在命名實體辨識(NER)的問題上驗證，透過Mamba結構能夠更有效地處理長序列，並且能夠在計算上實現線性擴展，突破傳統Transformer在長序列上的計算瓶頸，並結合CRF加強序列中的依賴關係。本研究提的Mamba結合CRF模型，在中文醫療命名實體辨識資料集的測試，達到了91.9%的F1值。

## 資料集
![image](https://github.com/arcaea/My-Paper/blob/main/Pic/%E4%B8%AD%E6%96%87%E9%86%AB%E7%99%82%E5%91%BD%E5%90%8D%E5%AF%A6%E9%AB%94%E8%BE%A8%E8%AD%98%E8%B3%87%E6%96%99%E9%9B%86%E5%91%BD%E5%90%8D%E5%AF%A6%E9%AB%94%E9%A1%9E%E5%88%A5%E7%9A%84%E6%8F%8F%E8%BF%B0%E3%80%81%E6%95%B8%E9%87%8F%E4%BB%A5%E5%8F%8A%E6%AF%94%E4%BE%8B.jpg) \
REF：(Lee et al., 2023)

## 模型架構圖
![image](https://github.com/arcaea/My-Paper/blob/main/Pic/%E6%A8%A1%E5%9E%8B%E6%9E%B6%E6%A7%8B%E5%9C%96.jpg)

## 模型訓練
![image](https://github.com/arcaea/My-Paper/blob/main/Pic/Algorithm%201%20.jpg)

## 結果比較
![image](https://github.com/arcaea/My-Paper/blob/main/Pic/%E6%A8%A1%E5%9E%8B%E5%9C%A8%E4%B8%AD%E6%96%87%E9%86%AB%E7%99%82%E5%91%BD%E5%90%8D%E5%AF%A6%E9%AB%94%E8%BE%A8%E8%AD%98%E8%B3%87%E6%96%99%E9%9B%86%E7%9A%84%E6%AF%94%E8%BC%83.jpg)

## 結論
透過本研究成功提出了一種創新的方法，將Mamba模型與CRF進行結合，並在中文醫療命名實體辨識資料集上顯示了其良好的性能，達到了91.9%的Micro average F1-score。這項研究不僅突顯了Mamba結合CRF模型的優勢，同時也強調了模型架構在處理特定任務時的重要性。

首先，本研究發現Mamba模型在訓練初期即迅速達到了89%以上的準確率，顯示出其對資料特徵的快速學習能力。透過調整迭代次數和優化器，本研究有效控制了模型的過擬合情況，從而進一步提升了模型效能。具體的方式是將Adam優化器替換為AdamW優化器改善了訓練結果的穩定性。

其次，在將Mamba結合CRF模型後，顯著改善了各類別的辨識效果，尤其是在資料量較少的實體類別如「I-DRUG」和「I-SUPP」上，F1-score有了顯著提升。這證明了CRF在增強模型對序列依賴性的能力方面的有效性，特別是在處理長距離依賴問題時的表現更為出色。CRF的引入使模型能夠更好地捕捉實體類別之間的資訊，從而提高了對實體類別的辨識能力。

相較於傳統的LSTM或最新的Transformer模型，Mamba結合CRF的模型在處理資料集中的不平衡類別分佈方面展現了顯著的優勢。儘管Macro average F1-score的提升幅度未達到預期，但Micro average F1-score的顯著提高顯示了整體效能的顯著進步。尤其是在處理「O」類別等資料的情況下，這一模型能夠有效地提高整體辨識精確度，為實際應用中的資料不平衡問題提供初步的解決方案。

本模型在醫療文本分析、臨床決策支援系統以及電子病歷自動標籤等應用場景中顯示了巨大的潛力。其良好的辨識能力能夠幫助醫療專業人員更有效率地提取關鍵資訊，提高資料處理的準確性和效率。特別是對於包含多種類別和複雜文字結構的醫療資料，此模型的效能能夠顯著提升，為實際應用中的挑戰提供有效解決方案。

## 貢獻
本研究的貢獻如下：首先，本研究提出了一種創新的Mamba模型與CRF結合的全新架構。其次，本研究成功地克服了Mamba模型在特定資訊擷取任務中效能不佳的問題。第三，通過與主流模型如LSTM和Transformer的比較，本研究清楚展示了Mamba模型結合CRF所帶來的獨特效能優勢。特別值得注意的是，本研究的模型不僅極大地減少了計算資源的使用，同時利用CRF強化了對序列依賴性的準確建模。這一點在處理資料集中實體類別不平衡且稀少的情況下顯得尤為關鍵。
