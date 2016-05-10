### 浅谈iOS架构设计

- 浅谈iOS架构设计
	- 表示层开发
	- 客户端业务逻辑的剥离
    - App组件SDK化(插件化之路)
	- 网络层DNS预解析
	- 图片资源服务器
	

之前市面上有大量的关于讨论iOS架构的一些问题，各式各样 百家争鸣。有关于设计模式的、业务划分的、app内部各种实现手段的。整体来说就我个人理解而言，架构的产生只是为了解决某种特定需求、特定场景下的特殊问题。架构无处不在，但是好的架构确不尽唯一。就像这个世界没有绝对的好与坏，每个人都有自己的特定需求。整体来说一个好的架构会决定着软件的后期的维护、开发是否具有可持续集成的可行性。作为一个设计师我们要做的学百家之所长，不断的完善自己，不意味的盲目的崇拜、推崇，做到手中无构，世间万物皆无构...

>
序言：随着iOS工程化的进度愈发加深，越来越多的团队面临的问题不在是如何为现有的软件追加一些新得功能模块，随着业务的拓展，对软件自身框架方面的问题也显得势在必行，模块与模块的之间的解耦合、模块间的相互独立，工程的组件化等显得越来越重要，本篇文章主要基于京东App当前工程中使用到的一些规范外加一些个人的理解总结，希望能够给予大家以学习上的帮助。

#### 表示层开发模式
##### 表示层的开发
客户端就表现层而言基本大家基本都采用MVC方式来开发，随着业务的演化可能逐步转变成MVVM，相对来说这些都是基于页面层的。无论是哪一种设计原则都是由MVC演变而来，

基础组建


[蘑菇街 App 的组件化之路](http://www.360doc.com/content/16/0316/13/25724933_542663459.shtml)

[糯米移动组件架构演进之路－	邱晨](http://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=2651112195&idx=1&sn=27fa638e90b09a107057e4a5e8d01ab1&scene=23&srcid=0509XYc90zRgbglPF6AVbmkh#rd)

[滴滴iOS客户端的架构演变之路－李贤辉](http://www.infoq.com/cn/news/2016/03/lixianhui-interview)

[iOS遗留系统重构实践-李剑](http://www.infoq.com/cn/articles/ios-legacy-codebase-refactor?utm_campaign=rightbar_v2&utm_source=infoq&utm_medium=articles_link&utm_content=link_text)

[App域名劫持之DNS高可用 - 开源版HttpDNS方案详解](http://www.tuicool.com/articles/7nAJBb)

[【鹅厂网事】全局精确流量调度新思路-HttpDNS服务详解](http://mp.weixin.qq.com/s?__biz=MzA3ODgyNzcwMw==&mid=201837080&idx=1&sn=b2a152b84df1c7dbd294ea66037cf262&scene=2&from=timeline&isappinstalled=0&utm_source=tuicool)