1.有哪些池化方法
===
- Max Pooling: 輸出局部區域的最大值
- Average Pooling: 輸出局部區域的平均值
- Spatial Pyramid Pooling: 對輸入不同尺度的特徵圖，輸出相同尺度的特徵

2.卷積層與池化層差異
===
- 卷積層Kernel可訓練，池化層規則固定
- 卷積層作用是提取更深層的特徵；池化層作用是保留有效特徵減少特徵數量。PS:卷積層亦可透過Stride參數達到downsample作用
