
## a top title view, according to the title of a number of automatic adaptation content

### 顶部滚动视图（APP中常见顶部滚动视图，使用UIScrollView进行封装，使用起来极其简单、实用、方便）

![](https://github.com/kingsic/SGTopTitleView/raw/master/Gif/sorgle.gif)

#### * `静止状态下标题按钮的创建`<br>

#### * `滚动状态下标题按钮的创建`<br>

#### * `导航栏上标题按钮的创建`<br>

* SGTopTitleView使用方法一：

  * 将项目中SGTopTitleView文件夹拖入工程

  * 导入#import "SGTopTitleView.h"头文件

  * 通过alloc、initWithFrame或者类方法topTitleViewWithFrame去创建

  * _topTitleView.staticTitleArr = [NSArray arrayWithArray:_titles]; // 静态数组标题的设置
 
  * _topTitleView.scrollTitleArr = [NSArray arrayWithArray:_titles]; // 动态数组标题的设置
 
  * _topTitleView.isHiddenIndicator = YES; // 默认为NO, 不隐藏

  * _topTitleView.showsTitleBackgroundIndicatorStyle = YES; // 默认指示器样式在标题文字下方, 设置之后指示器在标题文字后方

  * _topTitleView.titleAndIndicatorColor = [UIColor purpleColor]; // 默认为红色
 
  * 遵循SGTopTitleViewDelegate协议的delegate_SG方法
  ```Objective-C
  - (void)SGTopTitleView:(SGTopTitleView *)topTitleView didSelectTitleAtIndex:(NSInteger)index；
  ```
  
* SGTopTitleView使用方法二：（详细使用方法，请参考Demo）

* 父子控制器的使用

* navigationItem的titleView的屏幕尺寸处理

* 通过Label创建标题并在其上添加手势（UITapGestureRecognizer）

* 根据标题内容：实现标题宽度自适应
```Objective-C
- (CGRect)boundingRectWithSize:(CGSize)size options:(NSStringDrawingOptions)options attributes:(nullable NSDictionary *)attributes context:(nullable NSStringDrawingContext *)context;
```

