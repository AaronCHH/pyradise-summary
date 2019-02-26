整理 [Yao-Jen Kuo](https://medium.com/@tonykuoyj) 在 Medium 上發表關如何在 jupyter notebook環境下, 運用 nbconvert 將 .ipynb 輸出為適合簡報的投影片格式的文章。
內容摘要如下。

文章連結：
[Link](https://medium.com/pyradise/jupyter-notebook-tricks-slideshows-a057a39c0a23)

- [1. 播放模式](#1-%E6%92%AD%E6%94%BE%E6%A8%A1%E5%BC%8F)
- [2. 攜行模式](#2-%E6%94%9C%E8%A1%8C%E6%A8%A1%E5%BC%8F)
- [3. 輸出為 PDF](#3-%E8%BC%B8%E5%87%BA%E7%82%BA-pdf)
- [4. 在簡報時進行 Live Coding](#4-%E5%9C%A8%E7%B0%A1%E5%A0%B1%E6%99%82%E9%80%B2%E8%A1%8C-live-coding)


## 1. 播放模式
```
jupyter nbconvert my-nb-slide.ipynb --to slides --post serve
```


## 2. 攜行模式
* ### 將 reveal.js 下載至資料夾（透過 Git）
```
git clone https://github.com/hakimel/reveal.js.git
```
* ### 轉換為 HTML 投影片
```      
jupyter nbconvert my-nb-slide.ipynb --to slides --reveal-prefix reveal.js
```


## 3. 輸出為 PDF

啟動投影片模式簡報時將網址列
由 http://127.0.0.1:8000/my-nb-slide.slides.html#/   
改為 http://127.0.0.1:8000/my-nb-slide.slides.html?print-pdf   
就可以點選瀏覽器列印 (ctrl + p)，另存為 PDF 文件。


## 4. 在簡報時進行 Live Coding
* ### 使用 conda 安裝 RISE 模組
```
conda install -c conda-forge rise
```   
完成 RISE 模組的安裝之後，重新啟動 Jupyter Notebook 將會在工具列看見一個新的按鈕（Enter/Exit RISE Slideshow）。

<!-- ![RISE_Slideshow.PNG](RISE_Slideshow.PNG =400x) -->

<center>
<img src="RISE_Slideshow.PNG">
</center>