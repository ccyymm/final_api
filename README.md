## 产品需求
| 发布日期 | 12/24/2019|
| -------- | ----- |
|项目|手写文字电子化app| 
|项目状态| 进行中 | 
|项目负责人| 蔡玉妹 | 
|设计师| 蔡玉妹 | 
|开发者| 蔡玉妹 | 
|测试者| 蔡玉妹 |

# 一、PRD价值主张
## 价值宣言
目前市面上的文字识别软件不少，但是针对手写文字识别的app较少，**精准度也不够高，有些手写字体依然识别不出**，并且没有自动识别文字中地址的功能；
本app主要针对手写文字的识别，
* 利用“手写文字识别api”，针对不规则的手写字体进行专项优化，更加**精准、快速**地识别 **任意排版任意手写文字**，实现将手写文字电子化的功能；<br> 
* 利用“文本纠错api”，准确识别输入文本中出现的拼写错别字及其段落位置信息，并针对性给出正确的建议文本内容；<br>
* 利用“地址识别api”，精准提取快递填单文本中的姓名、电话、地址信息，通过自然语言处理辅助地址识别做自动补充和纠正，生成标准规范的结构化信息。<br>
本产品能够为用户减少一些“文字储存”的阻碍，节省用户花费在“识别文字、录入文字”的时间。

## 目标&核心价值（mvp）
本app主打”手写文字识别”功能，附加“文本纠错”“地址信息识别”功能，主要用到的api有：手写文字api，百度文本纠错api，百度地址识别api。
我们旨在通过该app，来为用户提供更便捷更省时的方式，实现将手稿文字电子化以及有效提取。


## 用户痛点
| 问题 | 解决 |
| -------- | ----- |
|用户想要寄快递，但是对方给出的信息是以图片形式，并且图片中文字是手写的，这用一般的图片识别的软件也识别不出来。|将图片上传至手写文字电子化app，并且开启地址识别功能，app将会对图片中的手写文字进行识别，再将其中的地址信息提取出来。| 
|用户想把手头的纸质表单内的手写文字信息整理并且上传保存，但文字信息特别多，得花费时间很长，后面又有很多工作需要完成。| 将该表单拍照上传到手写文字电子化app上，app将会自动识别出表单中的手写文字信息，用户可以直接在里面修改，保存为pdf格式进行分析或储存| 
|用户想把小说手稿录入，但是工程量很大，可能需要花钱雇录入员，而且文本内容可能还存在一些错别字，很容易被忽略。|将文稿分段拍照上传至app，app将自动识别手稿，开启文本纠错功能，app将识别出文本中的错别字，并且标注出来，给出修改建议。| 

## 人工智能概率性
* 手写文字识别api:识别准确率>90%；支持对图片中的手写中文、手写数字进行检测和识别，针对不规则的手写字体进行专项优化。尽管本产品秉持着“高精准度”的原则，但一些特别潦草的手写字体可能会识别不出或者识别有误
* 文本纠错api:精准度>90%；识别文本中有错误的片段，进行错误提示并给出正确的建议文本内容。一些文本采用的“新型网络用语”可能会被误识别为错误。
* 地址识别api：精准度>95%；提取快递填单文本中的姓名、电话、地址信息，通过自然语言处理辅助地址识别做自动补充和纠正。

## 需求列表与人工智能API加值
| 功能 | 用户案例 | 重要程度 |
| -------- | ----- | ------- |
|手写文字识别功能|用户进入app中,将有手写文字内容的图片上传后，图片中的手写文字将被识别出来，用户可进行修改保存处理。如：工作表单中的手写信息，地址信息等等。| 非常重要 |
|地址信息识别|在识别手写文字后，用户可以进一步获取手写文字中的地址信息，并且纠正补全地址信息，让用户得到一个正确完整规范的地址信息|重要|
|文本纠错|在识别手写文字后，用户可开启文本纠错功能，将识别出的文本进一步修正、完善。|重要|



# 二、原型
### 完整原型文档连接

### 手写字体识别界面
![手写界面](https://github.com/ccyymm/final_api/blob/master/%E6%89%8B%E5%86%99%E6%96%87%E5%AD%97%E8%AF%86%E5%88%AB.png?raw=true)
![手写界面](https://github.com/ccyymm/final_api/blob/master/%E6%89%8B%E5%86%99%E6%96%87%E5%AD%97%E8%AF%86%E5%88%AB%E7%BB%93%E6%9E%9C.png?raw=true)

### 地址识别（识别失败&成功）
![地址识别](https://github.com/ccyymm/final_api/blob/master/%E5%9C%B0%E5%9D%80%E8%AF%86%E5%88%AB.png?raw=true)

### 文本纠错
![文本纠错](https://github.com/ccyymm/final_api/blob/master/%E6%96%87%E5%AD%97%E7%BA%A0%E9%94%99.png?raw=true)

# 三、API使用
## api调用展示——流程图：
![api流程图](https://github.com/ccyymm/final_api/blob/master/api%E8%B0%83%E7%94%A8%E6%B5%81%E7%A8%8B%E5%9B%BE.png?raw=true)




## api调用（以百度api为例）：
### 百度手写文字识别api（链接）
* 输入：图片
* 输出：文字

![代码](https://github.com/ccyymm/final_api/blob/master/EC$F79EDFR9MZ%5B33%5D@(DM0E.png?raw=true)

![代码](https://github.com/ccyymm/final_api/blob/master/Y2MLJ0D@Y%25IR0B%5D5IYL1%7BSF.png?raw=true)


## 使用比较分析
（成熟度、性价比）
* 腾讯手写文字识别（链接）：图片识别比较慢，容易识别失败
* 百度手写文字识别（链接）：识别比较快，成功率较高


## api使用后风险评估报告
（市场竞争程度、输入输出限制、定价、可替代得程序库）
#### 问题：
* 手写识别api：仅支持手写汉字、数字识别，有些特别潦草的文字会识别不出或者识别有误。
* 文本纠正api：会有一些网络新型的用语会将其误识别为错别字。
#### 解决：
* 手写识别api：尽量用比较规范的手写文字，或者识别后用户自行修改，再进行其他功能或者保存。
* 文本纠正api：可不采纳修改建议。


