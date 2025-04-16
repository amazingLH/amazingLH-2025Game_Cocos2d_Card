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

2、点击左侧底牌，可以和最右侧“主底牌”进行切换
![QQ_1744795717668](https://github.com/user-attachments/assets/af40e74f-5a08-409d-a575-2dcbf7974430)
![QQ_1744795746234](https://github.com/user-attachments/assets/426fe7b0-fe15-460e-8ccf-4efc34032370)

3、主牌中任意牌若与最右侧“主底牌”相差1，点击匹配的主牌，该主牌替换在“主底牌”的位置，匹配的“主底牌”消除
![QQ_1744795923440](https://github.com/user-attachments/assets/1566ff6d-5a9a-4eca-bcc7-61d4356fa85f)
![QQ_1744795938533](https://github.com/user-attachments/assets/9e2ff865-781b-45e6-b8bf-c2716084998d)
![QQ_1744795952808](https://github.com/user-attachments/assets/caf1a9a0-facb-444a-b9b3-1905b312a57b)
![QQ_1744795968130](https://github.com/user-attachments/assets/70eeca43-b9ad-4dea-ba6e-226c7857669a)
![QQ_1744795983776](https://github.com/user-attachments/assets/a524d26c-fdba-42fe-97b0-71eab07e3310)
![QQ_1744795991797](https://github.com/user-attachments/assets/9c1fd731-f2a7-41a5-b3b1-66154605cb84)

4、若点击底牌区右侧“back”按钮，则撤回上一步操作
![QQ_1744796041138](https://github.com/user-attachments/assets/d906eb55-cfd7-4f50-9236-87d107e8653e)
![QQ_1744796046545](https://github.com/user-attachments/assets/e4bcb4ff-b896-4ec2-b426-885c070610e3)
![QQ_1744796053819](https://github.com/user-attachments/assets/9aaaf790-2799-4f32-bef3-b0f633cd08e1)

此为棋牌消除1.0版本，后续将进行迭代，直至达到理想的动画消除效果......
