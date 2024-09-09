理论背景
数据不够、知识来凑。传统上，机器学习在高频上追求的是数据的深度，所谓的深度就是说同样一个交易行为反复的出现，根据统计学的大数定律，你找出其中的规律，把规律用于其中的预测，这个胜率就会比较可靠。
但是，当你没有足够多历史数据，就要通过横向的扩张来拓展数据的宽度，这个宽度就来自于各种类型的非传统的应用数据，包括各种另类数据，包括其构建的大型金融行为的知识图谱。
系统层面的复杂性，整个系统从底层的算力系统，到数据体系、知识图谱、推理引擎及最后应用的层面都比较复杂。
如果要融合海量知识，并且对于这些海量知识进行快速推理，这对系统背后的系统低延时性、高并发性、系统吞吐量、系统本身智能化的算法要求是非常高的，这也导致开发的成本比较高。


金融情绪分析
随着近十年来自然语言处理技术以及互联网社交媒体的发展，基于市场情绪提取的金融分析作为一项主要的技术手段，已经被广泛的研究并应用到多种实际的投资辅助决策系统中。

进行股票预测的指导理论主要以金融学的随机游走理论和有效市场假说为主。
有效市场假说倾向于认为投资者是理性的，所有的信息都可以即刻反应在股价中，因此市场情绪对于股市的预测价值很低。然而，行为金融学的观点认为，至少从两个方面来看，有效市场假说存在事实上的问题：
第一，交易中不可避免存在非理性交易者，这部分交易者会给价格带来额外的风险，使得理性交易者也不敢全力投入；
第二，在某些极端情绪下，专业套利者可能由于某些限制原因，例如资本限制等，而无法有效地纠正股票价格。这些因素都可能导致股票的实际价格与基本价值不一样，造成套利行为无法消除投资者情绪引入的价格漂移，因而市场情绪指标可能具有一定的预测性。

在这些研究的基础上，随后的十年里，也就是本世纪的头十年中，越来越多的研究开始投入到市场情绪与股市关系的研究中。
在这一时期，常用的方式是将新闻与股价信息结合起来进行股价预测，在技术手段上多采用独热码编码的词袋模型结合支持向量机（SVM）。
同时，一些机构通过提供金融指数或者经济学指数来间接的推断投资者市场情绪。

最近两年，随着商用大模型的成熟，市场上出现了越来越多的基于商用大模型的金融情感分析项目，比如FinBERT(Financial Sentiment Analysis with BERT)。
我们的金融情感分析模型，基于当前的大语言模型，使用用户提供的文本数据作为语料进行微调。


产品定位
对于任何一个产品来说，产品技术的高低并不一定反映到产品销售的结果上，产品的定位，即生产消费者需要的产品，才是重中之重。
产品定位的核心永远是深刻透析用户的需求，寻找用户数量和用户需求的最大公约数，然后根据公约数提供具有性价比的产品。
即：
Product=(gcd⁡(Quantity,Demand))/(Price )
（理解这个公式非常重要！！！）

iPhone 是一款极端优秀的产品，满足了数十亿用户的根本需求，充满设计感、优质的使用体验、以及刚刚够的性能。
iPhone 的所有参数并不一定是最好的，但是产品经理对iPhone 的准确定位让它成为了一个经久不衰、畅销全球的系列产品。
同时，iPhone的价格带虽一直居于市场高位，但是优秀的产品定位拉高了分子端，使其依旧成为一款“极高性价比”的产品。

同理，我们的产品也极度依赖于产品定位，即寻找用户数量和用户需求的最大公约数，gcd⁡(Quantity,Demand)。
首先，我们要理清一个事实是，我们的目标是为了给用户进行智能投资顾问，并不只是辅助用户做出 100% 正确的决策，而是让客户更加深度的体验投资这个游戏的乐趣。这听上去像是经营赌场的生意哲学，我们就是赌场的叠码仔。
我们当然承认我们的生意很大程度上是在做一个“赌场叠码仔”，但是这不是一个坏生意，更重要的是，我们的公约数显然是要高于这个追求的。

我们的产品本质，是将量化基金的策略下放到普通投资者的世界里，相当于为量化策略换了一种收费的方式。传统的量化基金是募集高净值投资者的资金，从中收取管理费和盈利提成的生意模式。
我们将量化策略下放，把生意模式变成向大量低净值投资者们收取会员费的模式。
简单来说，相当于大量低净值投资者可以通过购买我们的产品，团购原本只有高净值投资者才能享受的服务和投资策略。

从用户的角度来思考，我们的产品最核心的，是要解决中小用户在交易中的焦虑和茫然不知所措。
从交易所的角度来思考，交易所最赚钱的业务根源来自于交易量，只要市场活跃，我们的生意就兴隆。

所以，我们的业务有两个核心目标：增值和游戏。
增值，就是赚钱，大量的基金就在干这件事。但是显然市场遵守二八定律，绝大部分基金产品都不赚钱，甚至亏钱。
我们要做的就是通过技术，通过我们独特的数据源和飞轮效应，获取市场的阿尔法，为我们的用户尽可能提供资产增值的可能性。
游戏也很好理解，就是激发人们肾上腺素带来的游戏快感，俗话说，赌场的生意始终是永赚不赔的，只是这个生意只属于交易所，是持牌机构们的游戏。
那么非持牌的我们，要参与这个生意，需要做的是就是尽可能将交易游戏化，把交易的体验做好，让参与者们持续参与交易。
这两项业务对标的生意模式，分别为基金和交易所。我们首要的任务是，要分清什么时候做基金的事情，什么时候做交易所的事情。

大语言模型的成熟，就给我们带来了一种生意上的可能性：
如果一个交易参与者愿意将手机中的部分群聊（交易群）数据上传，那么交易者就可以获得一张使用我们量化交易程序的点券，我们的量化交易程序就根据所有交易者上传的数据进行情感分析。
参与这个游戏的人越多，那么我们模型预测的能力就越强，预测结果就会越准确，就会形成飞轮效应。
另外，游戏化的体验上，应该让用户更深度参与盯盘，盯盘的体验是与肾上腺素直接相关的。如果用户能上传一部分实时的数据，就给另一张点券，能够让用户获得实时的市场情感分析功能。


不完全对标的竞品——水母量化
水母量化，为客户增值的能力弱，仅适合部分半专业交易者定制自己的准量化策略，非专业交易者有使用门槛，且无法形成长期的增值能力，导致用户量级不足；
游戏化能力也偏弱，交易游戏给人带来快感的核心是交易频率，一切不能提升交易频率的游戏化策略都是失败的。
成熟交易所成功的游戏化策略包括：合约和杠杆，期货期权衍生品。不过，水母也有比较不错的跟单交易功能。
 

市场与营销
在市场方面，在demo模型推出后，就应当大量投入营销费用，迅速收集用户，迅速收集数据，反哺模型。在这个阶段，资本投入尽可能集中于市场营销，用资本换用户，同时换数据。让飞轮尽可能转起来。
为什么不强调前期技术的投入？
根据我对创业团队和生意的理解，前期技术的投入只能通过股权和股权激励的形式来完成的，而不是现金。
技术是最核心的长期生产资料，无法通过现金这类即时激励来完成绑定，唯有在创业团队中巩固“要穷一起穷，要富一起富”的理念，才能让团队走得更远。因此，股权和股权激励是撬动技术的最好工具。
降低对技术的现金投入，也有利于用现金获取前期更重要的生产要素——用户和数据上。
于是，我们的策略逐渐清晰起来，尽可能用现金撬动用户和数据，尽可能用股权和股权激励撬动团队和技术。

可以参考的是，水母量化的使用定价最低是 300 元一个月，如果有效留存客户的话，一年的客单价是在 3600 元以上。如果有 1000人订阅服务的话，一年收入 360 万元，如果有 10000 人订阅服务的话，一年收入 3600 万元。
如果未来拿到证券投资咨询业务资格，采取类似的定价，一年稳定的 10000 用户订阅即有可能达到收支平衡。


法律风险
深圳证监局指出，2016年至2019年期间，云财经（“水母量化”母公司）通过公司网站、APP、微信公众号等渠道经营“涨停先驱者”“早盘捉妖”“N型反转大师”“搓揉优选大师”“研报大师”等软件产品（以下统称软件产品），
向客户提供具体证券投资品种的选择建议或买卖时机建议，属于《关于加强对利用“荐股软件”从事证券投资咨询业务监管的暂行规定》第一条第一款第（二）、（三）项规定的具有证券投资咨询服务功能的软件产品。
根据《暂行规定》，向投资者销售或者提供“荐股软件”，并直接或者间接获取经济利益的，属于从事证券投资咨询业务，应当经中国证监会许可，取得证券投资咨询业务资格。
没有证券投资咨询业务资格的单位和个人代理销售“荐股软件”属于非法行为。根据《暂行规定》，“荐股软件”的销售、协议签订、服务提供、客户回访以及投诉处理等业务环节不得委托未取得证券投资咨询业务资格的机构和个人代理。
所以，在取得证券投资咨询业务资格以前，这个生意模式一定首先是免费的，免费的不违法，同时降低了传播营销的门槛。其次，不对个股或具体的投资标的进行分析。

参考资料：
《郭健发声！Quant 4.0：量化投资站在AI新风口上》，中国基金报，2023
《熵简技术谈 | 金融情绪分析真的有用吗？一起来看金融情绪分析的研究进展及应用实践》，熵简科技，2020