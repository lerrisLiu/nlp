## 根据用户历史输入，给出下一个输入词汇

### 如何运行脚本

stop_words=stopWords('stop_words.txt')  #读取停用词表   
word_freq=cal_dict('questions.txt',2)  #计算每个词接下来的3-grams词汇和对应的词频   
word_top=word_rec(word_freq,5) #选出最有可能出现的5个组合   
word_top
  
### 输入信息
define.txt  #用户自定义词汇表  
stop_words.txt  #停用词表  
questions.txt  #用户历史输入句子信息  

### 函数参数
cal_dict('questions.txt',n) #n为n-grams的预测长度  
word_rec(word_freq,k) #k为最终推荐的预测词汇数量  

### 输出样式为一个字典表，key为当前用户输入的最后一个词，values为下面最有可能出现的词汇列表，并且按照可能性大小做降序排列   

{'查询': ['寿险', '车险'],
 '寿险': ['分公司'],
 '分公司': ['电话'],
 '电子': ['发票']}
 
