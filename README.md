# GunViolence_DataMining

数据来源为kaggle：https://www.kaggle.com/jameslko/gun-violence-data
主要分析13-18年美国枪支暴力事件的特征，以及使用时间序列预测下一年枪支暴力事件发生数量。

主要用到以下数据包  
**Basemap**是python中一个利用地图的库  
**plotly**是开挂的作图神器，可以供js, python, R, DB等使用  
**Seaborn**是基于matplotlib的python数据可视化库，提供更高层次的API封装，使用起来更加方便快捷。  
**Fbprophet **：facebook开源的时间序列预测框架prophet，目前支持R语言和python语言。托管在github上:https://github.com/facebookincubator/prophet。

  
#可能会出现的问题及解决方案 
  
**1.pip install XXX报错：**
parse() got an unexpected keyword argument 'transport_encoding'
解决：conda install pip

**2.No matching distribution found for  mpl_toolkits**
解决：
pip install --upgrade matplotlib
  
**下载停用词表出错**  
Resource 'corpora/stopwords.zip/stopwords/' not found.  Please
  use the NLTK Downloader to obtain the resource:  >>>
  nltk.download()
  Searched in:
    - 'C:\\Users\\liang/nltk_data'
    - 'C:\\nltk_data'
    - 'D:\\nltk_data'
    - 'E:\\nltk_data'
    - 'j:\\Anaconda3\\nltk_data'
    - 'j:\\Anaconda3\\lib\\nltk_data'
    - 'C:\\Users\\liang\\AppData\\Roaming\\nltk_data'

解决方案：
nltk.download("stopwords")

成功提示：
[nltk_data] Downloading package stopwords to
[nltk_data]     C:\Users\liang\AppData\Roaming\nltk_data...
[nltk_data]   Unzipping corpora\stopwords.zip.
Out[7]:
True

**去掉DataFrame中某个特征里面符合某条件的数据（如去掉“年份”中为“2013”的数据）**
解决方法：
使用df=df.loc[年份=2013]

注：df.iloc[]可以很方便的截取要是用哪些数据
如df.iloc[:, 1:] 表示使用所有行，第一列以后的数据

