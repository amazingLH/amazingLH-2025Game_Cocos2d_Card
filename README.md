源码文件在“release”中！！！

1、CardModel.h：定义了卡牌面值的枚举类型 CardFaceType 以及卡牌模型类 CardModel。
（1）CardFaceType 枚举类型定义了从 ACE 到 KING 的 13 种卡牌面值，每种面值对应一个 1 - 13 的数值。
（2）CardModel 类用于表示一张卡牌，包含默认构造函数、带参数的构造函数以及获取卡牌面值的函数。

2、GameModel.h：定义了游戏模型类 GameModel。
（1）GameModel 类包含构造函数和生成随机卡牌的函数 generateRandomCards。
（2）私有成员变量 allCards 用于存储所有的卡牌。

3、CardView.h：定义了卡牌视图类 CardView，继承自 cocos2d::Sprite。
（1）包含默认构造函数、静态工厂方法 create 和初始化函数 init。
（2）成员变量 cardModel 用于存储卡牌的模型。

4、GameView.h：定义了游戏视图类 GameView，继承自 cocos2d::Layer。
（1）包含静态工厂方法 create 和初始化函数 init。
（2）私有成员变量包括操作历史记录、存储卡牌指针的向量、可见区域大小和原点位置。
（3）定义了卡牌位置枚举 CardLocation 和操作信息结构体 Operation。
（4）声明了多个辅助方法，如设置卡牌布局、处理卡牌点击事件、移除卡牌视图和撤回操作等。

5、AppDelegate.h：定义了应用程序委托类 AppDelegate，继承自 cocos2d::Application。
（1）声明了构造函数、析构函数和多个虚函数，如初始化 OpenGL 上下文属性、应用程序启动完成、进入后台和进入前台等。

6、main.h：包含 Windows 相关的头文件和一些宏定义。

以下是详细功能介绍：

1、主页面
![QQ_1744795607917](https://github.com/user-attachments/assets/06130151-6f22-4686-be74-2d634471ca03)
