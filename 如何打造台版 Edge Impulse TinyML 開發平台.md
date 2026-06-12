# 如何打造台版 Edge Impulse TinyML 開發平台

演講日期：115/03/31\
演講者：許哲豪（Jack Hsu）

## 書面報告

        這次許哲豪老師主講的題目是如何打造台版Edge Impulse TinyML開發平台，內容主要介紹Edge AI、TinyML、常見的AI開發板，以及如何將人工智慧模型部署到微控制器或邊緣裝置上，最後也討論台灣如果要建立自己的Edge AI開發平台，可能需要哪些功能與會遇到哪些問題。

        老師首先介紹Edge AI與生成式AI的不同，生成式AI通常需要大量運算能力與記憶體，多數會放在雲端或GPU上執行，而Edge AI比較重視在裝置本身完成推論，例如聲音辨識、影像分類、物件偵測與異常偵測，因為邊緣裝置的Flash、RAM、電力與算力都比較有限，所以模型需要經過縮小、量化與優化，才能放到MCU或低功耗裝置上執行。

        老師接著介紹Edge AI常見的硬體，包括CPU、GPU、DSP、NPU、FPGA與ASIC，不同硬體在彈性、效能、功耗與價格上都有差異，例如CPU比較通用但AI運算效率較低，NPU則是專門用來加速神經網路推論，但在模型轉換時可能會遇到算子不支援或工具不相容的問題，所以選擇硬體不能只看算力，還要考慮開發工具與實際應用需求。

        演講中也介紹Edge Impulse平台，它將資料收集、資料標註、模型建立、訓練、測試、優化與部署整合在同一個平台中，使用者可以上傳影像、聲音或感測器資料，再選擇前處理方式與神經網路模型，訓練完成後還可以查看準確率、混淆矩陣、Flash與SRAM使用量，以及預估的推論時間，最後再將模型輸出成C++、Arduino或特定硬體可以使用的格式。

        老師最後提出打造台版Edge Impulse的想法，希望可以整合台灣本身的晶片、開發板與軟體資源，建立資料集、模型訓練、模型優化與部署的一套完整流程，但是要自己建立平台並不容易，除了需要經費與人力，也會遇到模型格式、NPU轉換、算子相容性與不同硬體工具無法共用的問題，因此可以先選擇少數常見的MCU與NPU開發板，完成一套可以實際運作的流程，再慢慢增加其他硬體與功能。

        這次聽演講的感觸是原本以為Edge AI只是把訓練好的模型放進開發板中執行，但是聽完後才發現真正困難的地方還包含資料收集、模型壓縮、硬體選擇、記憶體限制與模型轉換，不同廠商也都有各自的工具與格式，會增加開發上的困難，我認為如果台灣真的能建立一套整合國內晶片與開發板的平台，確實可以降低學生與開發者進入Edge AI的門檻，但是一開始不一定要把所有功能都做完，可以先從少數硬體與常見應用開始，讓平台能夠真正被使用，再逐步擴充。

## 關鍵字

Edge AI
TinyML
Edge Impulse
人工智慧
微控制器
NPU
模型部署
模型優化

## 參考文獻
Abadade, Y., Temouden, A., Bamoumen, H., Benamar, N., Chtouki, Y., & Hafid, A. S. (2023). A comprehensive survey on TinyML. IEEE Access, 11, 96892–96922. https://doi.org/10.1109/ACCESS.2023.3294111

David, R., Duke, J., Jain, A., Janapa Reddi, V., Jeffries, N., Li, J., Kreeger, N., Nappier, I., Natraj, M., Regev, S., Rhodes, R., Wang, T., & Warden, P. (2021). TensorFlow Lite Micro: Embedded machine learning for TinyML systems. Proceedings of Machine Learning and Systems, 3, 800–811.

Hymel, S., Banbury, C., Situnayake, D., Elium, A., Ward, C., Kelcey, M., Baaijens, M., Majchrzycki, M., Plunkett, J., Tischler, D., Grande, A., Moreau, L., Maslov, D., Beavis, A., Jongboom, J., & Janapa Reddi, V. (2023). Edge Impulse: An MLOps platform for Tiny Machine Learning. Proceedings of Machine Learning and Systems, 5, 795–811.
