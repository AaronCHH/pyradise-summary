- [以 IPyKernel 建置 Python 2 核心](#%E4%BB%A5-ipykernel-%E5%BB%BA%E7%BD%AE-python-2-%E6%A0%B8%E5%BF%83)
- [以 IRkernel 建置 R 語言核心](#%E4%BB%A5-irkernel-%E5%BB%BA%E7%BD%AE-r-%E8%AA%9E%E8%A8%80%E6%A0%B8%E5%BF%83)
- [以 IJulia 建置 Julia 核心](#%E4%BB%A5-ijulia-%E5%BB%BA%E7%BD%AE-julia-%E6%A0%B8%E5%BF%83)
- [以 spylon-kernel 建置 Scala 核心](#%E4%BB%A5-spylon-kernel-%E5%BB%BA%E7%BD%AE-scala-%E6%A0%B8%E5%BF%83)
## 以 IPyKernel 建置 Python 2 核心

* Windows 啟動虛擬環境
```{py}
activate python2
```
* 安裝 ipykernel
```{py}
pip install ipykernel
```
* 將虛擬環境新增至 Jupyter Notebook 的核心清單
```{py}
python -m ipykernel install --user --name python2 --display-name "Python 2"
```
* 啟動 Jupyter Notebook
```{py}
jupyter notebook
```

## 以 IRkernel 建置 R 語言核心

* 安裝 IRkernel 套件
```{py}
install.packages('IRkernel', repos = 'https://cloud.r-project.org/')
```
* 新增 R 語言至 Jupyter Notebook 的核心清單
```{py}
IRkernel::installspec(user = FALSE)
```
* 啟動 Jupyter Notebook
```{py}
jupyter notebook
```
* 並且以 sessionInfo() 函數來驗證這個筆記本確實能執行 R 程式碼
```{py}
sessionInfo()
```
## 以 IJulia 建置 Julia 核心

* 啟動 Julia
```{py}
julia
```
* 引用 Pkg
```{py}
using Pkg
```
* 安裝 IJulia 套件
```{py}
Pkg.add("IJulia")
```
* 啟動 Jupyter Notebook
```{py}
jupyter notebook
```
## 以 spylon-kernel 建置 Scala 核心
* 安裝 scala for Windows
```
https://www.scala-lang.org/download/
```
* 安裝 pyspark
```
pip install pyspark
```
* 安裝 spylon-kernel 模組
```{py}
conda install -c conda-forge spylon-kernel
```
* 將 spylon-kernel 新增至 Jupyter Notebook 的核心清單中
```{py}
python -m spylon_kernel install
```
* 啟動 Jupyter Notebook
```{py}
jupyter notebook
```
* 以 util.Properties.versionString 屬性來驗證這個筆記本確實能執行 Scala 程式碼
```{py}
println(util.Properties.versionString)
```