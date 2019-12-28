# 针对多动症和残障者设计的博物馆APP

> 在我们开始项目之前，我们先了解什么是多动症患者和残障者。
> 
>  **多动症** 全称注意缺陷多动障碍。
>  
> 临床表现：
> - 1、注意缺陷：患者做任何活动时注意力难以持久，容易因外界刺激而分心，不能注意到细节，常粗心而发生错误，注意维持困难，常有意或不愿意从事较长时间持续集中注意的活动，常丢三落四。
> - 2、活动过多：患者手足小动作多，不能安静停留，擅自离开座位，到处乱跑或攀爬，难以从事安静活动。
> - 3、行为冲动：表现冲动，做事不顾及后果，凭一时兴趣行事，打断别人谈话，不能耐心排队。
> - 4、品行障碍：表现为攻击性行为，如辱骂、打伤同学、破坏物品等。
> 
>  行为治疗：
> 利用操作性条件放射原理，及时对患者的行为给予正性或负性强化。
> 
>  **残障者** 以社会功能障碍来划分残疾，我国目前分为六级：
> - 视力残疾：指双眼视力障碍或视野缩小。
> - 听力残疾：双耳听力丧失或听觉障碍。
> - 语言残疾：语言障碍或不能说话。
> - 智力残疾：指人的智力活动能力明显低于一般人的水平，并显示出适应行为的障碍。
> - 肢体残疾：指人的四肢的病损和残缺或四肢、躯干麻痹、畸形、导致人体运动系统不同程度的功能丧失或功能障碍。
> - 精神残疾：指患者患精神障碍的病情持续一年以上未愈，从而影响其社交能力和在家庭、社会应尽职能上出现不同程度的紊乱和障碍。

## 加值宣言：
市面上有很多博物馆的APP，但是很多都是为该博物馆定制的APP，无法在各大博物馆流通使用；有个博物馆自助智能讲解神器，其汇集了全球的博物馆信息，但是无法在博物馆内部导航。人工智能在今天的使用愈发频繁，根据市场上已有的博物馆APP，我们将结合人工智能API进行加值，对现有的博物馆功能进行改进和优化。本APP相应的配合智能耳机使用。

## 核心价值 ：
室内导览，实时的语音合成阅读。

## 核心价值与用户痛点：
#### 用户
进入图书馆的用户
#### 具体场景
-  **用户一：** 一位老师带着几个学生想去博物馆学习参观，但又害怕有小孩不受管制，碰坏博物馆物品。带领小朋友去领取耳机，并打开振动提醒装置，伴随着振动和耳机的语音提示，能有效的确保小孩不要到处乱跑。
-  **用户二：** 去博物馆，但是很容易在博物馆里绕圈圈，总找不到的目的地。此时打开APP，点开楼层分布图，确定自己的目的楼层，点进去直接到页面的楼层图，最后定点进行位置导航。
-  **用户三：** 希望有个实时的导游可以讲解我所到达的区域，此时打开专设的耳机，该耳机可实时定位和语音讲解。
-  **用户四：** 想先去人少的位置，打开APP看楼层分布图，看到红色区域证明此区域人流量多，绿色区域为人流量少。

## 需求列表与人工智能API加值：
#### 用户需求

| 用户需求 | API加值         | 重要程度 |
| -------- | --------------- | -------- |
| 室内地图 | 室内地图 JS API | 重要     |
| 位置定位 | 高德地图 JS API | 重要     |
| 语音阅读 | 语音合成        | 重要     |
|步行导航|室内步行导航|重要|

## API使用比较分析 

 [**百度地图室内地图** ](http://lbsyun.baidu.com/index.php?title=androidsdk/guide/create-map/indoormap)

- 优势：高精度室内图（国内首家高精度室内图）、高精度定位（1-3米）定位、多种定位方式融合（结合WI-FI、气压计、蓝牙、地磁传感器等定位技术）、低成本（无部署成本、覆盖快）

- API 输入

![百度室内地图输入](https://images.gitee.com/uploads/images/2019/1217/161611_6c693dda_1648228.jpeg "室内地图 百度输入.JPG")

- API 输出

![输出](https://images.gitee.com/uploads/images/2019/1217/161701_618610de_1648228.jpeg "室内地图 百度 输出.JPG")

- [价目](http://lbsyun.baidu.com/cashier/quota#/home)

    | 访问次数1000次内 | 访问次数1千-1万次内 | 访问次数1万-10万次内 |
    | ---------------- | ------------------- | -------------------- |
   | 30元/万次        | 24元/万次           | 18元/万次            |

[ **百度地图室内步行导航** ](http://lbsyun.baidu.com/index.php?title=androidsdk/guide/navigation/indoorwalknavi)

- 室内步行导航需要语音播报需语音识别服务的开发包

- API输入

![输入](https://images.gitee.com/uploads/images/2019/1217/173952_2ed3111a_1648228.jpeg "路径规划 代码.JPG")

- API输出

![输出](https://images.gitee.com/uploads/images/2019/1217/174014_632799db_1648228.jpeg "路径规划 结果.JPG")

[ **百度地图显示定位** ](http://lbsyun.baidu.com/index.php?title=androidsdk/guide/create-map/location)

- 优势：

定位精度圈大小，是根据当前定位精度自动控制的，无法手动控制大小。精度圈越小，代表当前定位精度越高；反之圈越大，代表当前定位精度越低。
定位指针方向，是通过获取手机系统陀螺仪数据，控制定位指针的方向，需要开发者自己实现，并不在地图实现范畴。

- API输入

![输入](https://images.gitee.com/uploads/images/2019/1217/174346_1287d7d1_1648228.jpeg "百度 地位显示.JPG")

-  [**高德室内地图**](https://lbs.amap.com/api/javascript-api/reference/indoormap) 
- 优势：高精度室内定位体验（提供1-8米的平均定位精度，平滑跟随的定位效果，精准的方向指示，精益求精的位置体验。）、精确的垂直维度定位（突破传统二维坐标定位局限，在室内快速、精准的提供精确到楼层的定位结果。）、多种定位方式融合（基于wifi、ble、pdr、地磁等多种室内定位技术综合定位，定位精度更高、应用场景更广。）

- API输入

![输入](https://images.gitee.com/uploads/images/2019/1217/180317_94230ae1_1648228.jpeg "高德室内图层输入.JPG")

- [输出](https://lbs.amap.com/api/javascript-api/example/indoormap/indoormap)

#### 语音合成

 [**腾讯云**](https://cloud.tencent.com/document/product/1073/37995) 

- 优势：提供多种音色选择，支持自定义音量、语速，为企业客户提供个性化音色定制服务，让发音更自然、更专业、更符合场景需求。语音合成广泛应用于语音导航、有声读物、机器人、语音助手、自动新闻播报等场景，提升人机交互体验，提高语音类应用构建效率。 

- API 输入

![输入](https://images.gitee.com/uploads/images/2019/1217/183239_fc06b027_1648228.jpeg "腾讯云 语音输入.JPG")

- API 输出

![输出](https://images.gitee.com/uploads/images/2019/1217/183251_40db2428_1648228.jpeg "腾讯云 语音输出.JPG")

- 价目

1. 语音合成免费额度为每月100万字符，相当于一本《西游记》的字数。每月1日重置免费额度。
2. 语音合成按合成的字符数计费，每月超过免费额度部分0.2元\单价（元/万字符）。

 [**阿里云**](https://help.aliyun.com/document_detail/120699.html?spm=a2c4g.11186623.6.594.54b153d5puMBne) 

- 优势：

1. 技术领先
技术上兼顾了多级韵律停顿，达到自然的合成韵律目的，综合利用声学参数和语言学参数，建立基于深度学习的多重自动预测模型。
2. 多领域覆盖
在智能家居、车载、导航、金融、银行、保险、证券、运营商、物流、房地产、教育等众多领域积累了大量的词库，让阿里语音合成技术对各领域、各行业的词汇发音更准确。
3. 听感自然
使用海量的音频数据训练合成数据，合成音真实饱满、抑扬顿挫、富有表现力，MOS评分达到业内顶级水准。
4. 深度定制
可根据用户需求定制音库，满足用户的个性化应用需求，提供标准男女声，温柔甜美女声等多风格的选择，支持标记语言（SSML）方式的合成方式，音量、语速、音高等参数也支持动态调整。

- API输入

![输入](https://images.gitee.com/uploads/images/2019/1217/190153_9a0d773b_1648228.jpeg "阿里云 语音合成输出.JPG")

- API输出


- 价目

![阿里云语音合成价格](https://images.gitee.com/uploads/images/2019/1209/154238_46aee6f2_1648228.jpeg "阿里云 语音合成价格.JPG")

 [**百度AI**](https://ai.baidu.com/ai-doc/SPEECH/fk38y8hqo) 
- 优势：

1. 提供多场景音库

提供基础音库和精品音库共9种音库供您选择，适用于泛阅读、订单播报、智能硬件等应用场景，即将推出更多特色音库。

2. 语速、音调可调节

支持多种参数配置，可根据场景需求对音库的语速、音调、音量进行灵活设置，满足个性化需求

3. 支持多音字标注

中文多音字可通过标注拼音、音调自行定义发音，例如“轻舟已过万重（chong2）山”、“脑筋急转（zhuan3）弯”

4. 多种调用方式，满足多场景需求

提供REST API接口、在线离线融合SDK，满足不同网络环境下的语音合成需求，提供流畅自然的合成体验

- API输入

![输入](https://images.gitee.com/uploads/images/2019/1217/184846_faeb3603_1648228.png "语音合成代码1.png")
![输入](https://images.gitee.com/uploads/images/2019/1217/184902_035a13f4_1648228.png "语音合成代码2.png")
![输出](https://images.gitee.com/uploads/images/2019/1217/184917_7f999b25_1648228.png "语音合成代码3.png")

- API输出

![输出](https://images.gitee.com/uploads/images/2019/1217/184934_e5b22fa8_1648228.png "语音合成输出.png")

- 价目

![在线使用免费额度](https://images.gitee.com/uploads/images/2019/1209/153523_3dbe764f_1648228.jpeg "百度AI 在线语音合成 免费.JPG")

![语音合成价目表](https://images.gitee.com/uploads/images/2019/1209/153556_ac3a9856_1648228.jpeg "百度AI 在线语音合成 付费.JPG")

 **Microsoft Azure** 

- 优势：

1. 逼真的语音
生成符合人类重音模式和语调的流畅自然的语音。
2. 全球参与
以超过 80 种语音、45 种语言和变体与全球受众交互。
3. 自定义体验
只需先花几分钟来训练数据，即可为你的应用生成独特的品牌声音。
4. 优化音频
通过轻松调整速率、音量和发音等属性，为你的方案优化语音输出。

- API输入

![输入](https://images.gitee.com/uploads/images/2019/1217/191125_b95447bc_1648228.jpeg "Microsoft 语音合成输入.JPG")

- API输出

- 价目

Microsoft Azure 没有前期服务，只有使用的服务付费，且按小时付费。

![Azure的价目表](https://images.gitee.com/uploads/images/2019/1209/153845_4a8e5c4d_1648228.jpeg "Azure 的价格付费.JPG")

- [详情](https://github.com/Azure-Samples/Cognitive-Speech-TTS/tree/master/Samples-Http/Python)

## 人工智能概率性与用户痛点：## 百度地图、高德地图、腾讯云、阿里云、Microsoft Azure和百度AI，六家平台API使用比较分析
经过人工智能API的使用情况以及价格对比进行分析，考量识存学APP属于初期阶段，通过性价比和输入反馈，我们发现百度地图的结果反馈最精准，其高精度（1-3米）定位。阿里云则聚积大量的词库，Microsoft Azure则是涵盖多种语言，腾讯云的优点是多样化和定制化的语音选择，高德地图的高精度室内定位体验（提供1-8米的平均定位精度，平滑跟随的定位效果，精准的方向指示，精益求精的位置体验）。根据我们的产品目标定位和价格的综合考量分析，我们最终选择百度地图的API平台，其定位精准且成本低，符合我们初期产品使用。

## 人工智能概率性与用户痛点：

-  **语音合成：** 远离拾音器、明显噪声、严重口音等因素会影响语音识别准确率。返回结果受网络和音频长度等因素影响，具体时间需要根据参数来决定。
-  **室内地图：** 返回结果受网络、蓝牙等影响。
-  **室内步行导航：** 目前仅支持检索起点、终点坐标在同一室内图上的线路规划，即仅支持同一商场，不支持两个不同的商场内的起、终点。
-  **室内定位：** 需要现场有WIFI部署或蓝牙部署，并通过定位数据采集工具进行定位指纹数据采集，数据准备完成后上传到服务器则可使用SDK实现室内定位。需要确保程序编译通过，定位时需要连接网络，定位成功率在99.5%以上。建议打开Wi-Fi，或者尝试走到别的地方，多试几次即可成功定位。用户自行完成定位数据更新。

## API使用后风险报告
目前选择的百度地图API平台，其服务高效稳定，助力业务发展的定位符合前期的产品发展需求，服务响应速度极快，平均响应时长不超过200ms。如今百度地图API是相当成熟的平台方，在使用期间需注意的是使用额度的调用。


## 原型

- 产品原型

![注册页](https://images.gitee.com/uploads/images/2019/1215/214008_ba938f28_1648228.jpeg "注册页.JPG")

![当前定位展示](https://images.gitee.com/uploads/images/2019/1215/214039_4f720eef_1648228.jpeg "当前定位展示.JPG")

![振动提醒](https://images.gitee.com/uploads/images/2019/1215/214115_013e04cf_1648228.jpeg "打开振动 信息提示.JPG")

![产品展示信息](https://images.gitee.com/uploads/images/2019/1215/214141_70d0fbbd_1648228.jpeg "产品展示信息.JPG")

![功能页](https://images.gitee.com/uploads/images/2019/1215/214203_2ab9835b_1648228.jpeg "功能页.JPG")

![楼层分布](https://images.gitee.com/uploads/images/2019/1215/214225_2230c6ff_1648228.jpeg "楼层分布.JPG")

![定位人群显示](https://images.gitee.com/uploads/images/2019/1215/214246_4bc2e7e8_1648228.jpeg "当前定位 显示人群.JPG")

![关闭人群定位显示](https://images.gitee.com/uploads/images/2019/1215/214324_3036bac8_1648228.jpeg "关闭定位显示.JPG")

![卫生间路线导航](https://images.gitee.com/uploads/images/2019/1215/214350_c2b55aa6_1648228.jpeg "卫生间路线导航.JPG")

- 博物馆功能结构图

![功能结构图](https://images.gitee.com/uploads/images/2019/1215/214458_1db1eb1b_1648228.jpeg "博物馆功能结构图.JPG")

- 博物馆信息结构图

![信息结构图](https://images.gitee.com/uploads/images/2019/1215/214530_dbe331d3_1648228.jpeg "博物馆信息结构图.JPG")

- 博物馆APP产品框架图

![原型框架图](https://images.gitee.com/uploads/images/2019/1215/214604_ef710007_1648228.jpeg "原型框架图.JPG")

- [ **原型交互** ](http://nfunm026.gitee.io/museum)

- [ **原型文档** ](https://github.com/VickyCN/museum)


 

