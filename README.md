## 产品需求
| 发布日期 | 12/24/2019|
| -------- | ----- |
|项目|手写文字电子化app| 
|项目状态| 完成 | 
|项目负责人| 蔡玉妹 | 
|设计师| 蔡玉妹 | 
|开发者| 蔡玉妹 | 
|测试者| 蔡玉妹 |

# 一、PRD价值主张
## 价值宣言
目前市面上的文字识别软件不少，但是针对手写文字识别的app较少，**精准度也不够高，有些手写字体依然识别不出**，并且没有自动识别文字中地址的功能；,<br>
本app主要针对手写文字的识别，
* 利用“手写文字识别api”，针对不规则的手写字体进行专项优化，更加**精准、快速**地识别 **任意排版任意手写文字**，实现将手写文字电子化的功能；<br> 
* 利用“文本纠错api”，准确识别输入文本中出现的拼写错别字及其段落位置信息，并针对性给出正确的建议文本内容；<br>
* 利用“地址识别api”，精准提取快递填单文本中的姓名、电话、地址信息，通过自然语言处理辅助地址识别做自动补充和纠正，生成标准规范的结构化信息。<br>

为用户减少一些“文字储存”的阻碍，节省用户花费在“识别文字、录入文字”的时间。

## 目标&核心价值（mvp）
本app主打”手写文字识别”功能，附加“文本纠错”“地址信息识别”次要功能，主要用到的api有：手写文字api，百度文本纠错api，百度地址识别api。
我们旨在通过该app，来为用户提供更便捷更省时的方式，实现将手稿文字电子化以及有效提取。


## 用户痛点
| 问题 | 解决 |
| -------- | ----- |
|用户想要寄快递，但是对方给出的信息是以图片形式，并且图片中文字是手写的，这用一般的图片识别的软件也识别不出来。|将图片上传至手写文字电子化app，并且开启地址识别功能，app将会对图片中的手写文字进行识别，再将其中的地址信息提取出来。| 
|用户想把手头的纸质表单内的手写文字信息整理并且上传保存，但文字信息特别多，得花费时间很长，后面又有很多工作需要完成。| 将该表单拍照上传到手写文字电子化app上，app将会自动识别出表单中的手写文字信息，用户可以直接在里面修改，再一次进行识别分析或储存| 
|用户想把小说手稿录入，但是工程量很大，可能需要花钱雇录入员，而且文本内容可能还存在一些错别字，很容易被忽略。|将文稿分段拍照上传至app，app将自动识别手稿，开启文本纠错功能，app将识别出文本中的错别字，并且标注出来，给出修改建议。| 

## 人工智能概率性
* <b>手写文字识别api:</b> 识别准确率>90%；支持对图片中的手写中文、手写数字进行检测和识别，针对不规则的手写字体进行专项优化。尽管本产品秉持着“高精准度”的原则，但一些特别潦草的手写字体可能会识别不出或者识别有误
* <b>文本纠错api:</b>精准度>90%；识别文本中有错误的片段，进行错误提示并给出正确的建议文本内容。一些文本采用的“新型网络用语”可能会被误识别为错误。
* <b>地址识别api:</b> 精准度>95%；提取快递填单文本中的姓名、电话、地址信息，通过自然语言处理辅助地址识别做自动补充和纠正。

## 需求列表与人工智能API加值
| 功能 | 用户案例 | 重要程度 |
| -------- | ----- | ------- |
|手写文字识别功能|用户进入app中,将有手写文字内容的图片上传后，图片中的手写文字将被识别出来，用户可进行修改保存处理。如：工作表单中的手写信息，地址信息等等。| 非常重要 |
|地址信息识别|在识别手写文字后，用户可以进一步获取手写文字中的地址信息，并且纠正补全地址信息，让用户得到一个正确完整规范的地址信息|次要|
|文本纠错|在识别手写文字后，用户可开启文本纠错功能，将识别出的文本进一步修正、完善。|次要|



# 二、原型
### [完整原型文档](http://nfunm002.gitee.io/apiyuanxing)
### [原型文件下载](https://github.com/ccyymm/final_api/blob/master/api%E5%8E%9F%E5%9E%8B20191224.rp)

### 手写字体识别界面
![手写界面](https://github.com/ccyymm/final_api/blob/master/%E6%89%8B%E5%86%99%E6%96%87%E5%AD%97%E8%AF%86%E5%88%AB.png?raw=true)
![手写界面](https://github.com/ccyymm/final_api/blob/master/%E6%89%8B%E5%86%99%E6%96%87%E5%AD%97%E8%AF%86%E5%88%AB%E7%BB%93%E6%9E%9C.png?raw=true)

### 地址识别（识别失败&成功）
![地址识别](https://github.com/ccyymm/final_api/blob/master/%E5%9C%B0%E5%9D%80%E8%AF%86%E5%88%AB.png?raw=true)

### 文本纠错
![文本纠错](https://github.com/ccyymm/final_api/blob/master/%E6%96%87%E6%9C%AC%E7%BA%A0%E9%94%99%E5%8E%9F%E5%9E%8B.png?raw=true)
![文本保存](https://github.com/ccyymm/final_api/blob/master/%25%E6%96%87%E6%9C%AC%E7%BA%A0%E9%94%99%E4%BF%9D%E5%AD%98.png?raw=true)
![文本说明](https://github.com/ccyymm/final_api/blob/master/%E6%96%87%E6%9C%AC%E7%BA%A0%E9%94%99%E8%AF%B4%E6%98%8E.png?raw=true)

# 三、API使用
## api调用展示——流程图：
![api流程图](https://github.com/ccyymm/final_api/blob/master/api%E8%B0%83%E7%94%A8%E6%B5%81%E7%A8%8B%E5%9B%BE.png?raw=true)




## API测试
### 百度手写文字识别api

* 手写字体识别代码测试（百度api）：
* 输入：手写文字的图片<br>
* 输出：文字

![手写字体识别](https://github.com/ccyymm/final_api/blob/master/%E6%89%8B%E5%86%99%E5%AD%97%E4%BD%93%E8%AF%86%E5%88%AB%E7%BB%93%E6%9E%9C%20(4).png?raw=true)

* 识别结果
![手写字体识别结果](https://github.com/ccyymm/final_api/blob/master/%E6%89%8B%E5%86%99%E5%AD%97%E4%BD%93%E8%AF%86%E5%88%AB%E7%BB%93%E6%9E%9C%20(1).png?raw=true)

### 地址识别api：
 输入：文本文字<br>
 输出：地址信息&人物信息
 <b>输入：</b>
![地址识别测试](https://github.com/ccyymm/final_api/blob/master/%E5%9C%B0%E5%9D%80%E8%AF%86%E5%88%AB%E4%BB%A3%E7%A0%81.png?raw=true)

 <b>输出：</b>
![地址识别测试结果](https://github.com/ccyymm/final_api/blob/master/%E5%9C%B0%E5%9D%80%E8%AF%86%E5%88%AB%E8%B0%83%E7%94%A8%E7%BB%93%E6%9E%9C.jpg?raw=true)

### 文本纠错api：
* 输入：文本文字<br>
* 输出：文本文字，错别字标注&修改建议

<b>输入：</b>
![文本纠错代码](https://github.com/ccyymm/final_api/blob/master/%E6%96%87%E6%9C%AC%E7%BA%A0%E9%94%99%E4%BB%A3%E7%A0%81.png?raw=true)

<b>输出：</b>
![文本纠错返回结果](https://github.com/ccyymm/final_api/blob/master/%E6%96%87%E6%9C%AC%E7%BA%A0%E9%94%99%E8%BF%94%E5%9B%9E%E7%BB%93%E6%9E%9C.png?raw=true)

## API价格
* 注：每日50次免费调用量，免费额度用尽后按照如下价格进行计费。

| 月调用量（万次） | 手写文字识别（元/次 |
| -------- | ----- |
| 0<调用次数<=2 |	0.0100 |
| 2<调用次数<=5 |	0.0080 |
| 5<调用次数<=10 |	0.0065 |
| 10<调用次数<=20 |	0.0055 |
| 20<调用次数<=30 |	0.0050 |
| 30<调用次数	 | 0.0045 |

## 使用比较分析
* 百度api价格相较于腾讯更低一些
* [腾讯手写字体识别](https://ai.qq.com/product/ocr.shtml#handwrite)：图片识别比较慢，容易识别失败
* [百度手写字体识别](https://ai.baidu.com/tech/ocr_others/handwriting)：识别比较快，成功率较高，成熟度相对高



## api使用后风险评估报告

| 名称 | 问题 | 解决 |
| -------- | ----- | ------- |
|手写识别api | 仅支持手写汉字、数字识别，有些特别潦草的文字会识别不出或者识别有误。| 手写识别api：尽量用比较规范的手写文字，或者识别后用户自行修改，再进行其他功能或者保存。|
| 文本纠正api | 会有一些网络新型的用语会将其误识别为错别字。| 文本纠正api：可不采纳修改建议。|
| 地址识别api | 该功能很可能会被觉得可以用其他api代替如：图像识别等。| 由于我们产品主打“手写”文字识别，地址识别属于附加功能，地址识别、文字识别都是基于“精准”的“手写字体识别”后才能启用。而如果是图像识别其很可能无法识别出一些手写字体，因此识别结果可能误差较大，所以在本产品中地址识别功能的所占的优势是“更精准”，在产品后期运营比较成熟的状况下，考虑参考其他api进一步升级附加功能。|
| 市场竞争 | 市面上主打“手写”字体识别的app可能目前还是比较少，并且功能、精准度有所局限，但是后期在各种api的完善下，可能会有更多更完善、功能更加丰富的同类产品出现 | 在保证原有“精准度”的情况下进一步提高产品识别的精准度，结合其他api，将附加功能升级，一体化 |

## 目前只做
目前本产品只针对于手写字体的识别，做“专”（专业，针对性）而“精”（精确，精准度高）的APP。

 



