卷積層有哪些類型及作用
===

1. Dilation Convolution 
- 作用是維持相同數量的卷積權重下增加視野範圍
- 做法是在兩個權重之間插入數個零值(參數: dilated rate)

2. Depthwise Separable Convolution
- 作用是降低計算量
- 其假設是特徵圖每個通道是統計獨立，因此每個通道用獨立的kxk大小filter再搭配1x1大小filter去逼近傳統卷積層
- 計算步驟:(假設輸入圖大小是NxNxC1, 輸出圖大小是NxNxC2)
  - 1. 輸入圖每一個通道各別以kxk的filter作掃描，再concat在一起，得到NxNxC1大小的特徵圖
  - 2. 再用C2個1x1xC1大小filter掃描前述特徵圖，最後得到NxNxC2特徵圖

3. Deconvolution
- 作用是Upsample
