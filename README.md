# CJCalendar

## 这是一个可以显示农历和公历的日历控制器

![image](https://github.com/chjsun/readmeImage/blob/master/CJCalendar/modal.gif)

![image](https://github.com/chjsun/readmeImage/blob/master/CJCalendar/selecttitle.gif)

![image](https://github.com/chjsun/readmeImage/blob/master/CJCalendar/chuanzhi.gif)

使用这个日历灰常简单
只要把calendar拖到你的项目中，就可以直接用了

### 步骤：
#### 一 初始化

初始化控制器，代理监听，设置大小
```
  CJCalendarViewController *calendarController = [[CJCalendarViewController alloc] init];
  calendarController.view.frame = self.view.frame;
  calendarController.delegate = self;

```
#### 二 添加控制器
```
  [self presentViewController:calendarController animated:YES completion:nil];
```

#### 三 实现代理方法

可选代理方法，用来接受返回的年月日
```
-(void)CalendarViewController:(CJCalendarViewController *)controller didSelectActionYear:(NSString *)year month:(NSString *)month day:(NSString *)day;
```

### 可选的方法
#### 一 指定初始时间
默认不指定就是当前时间

```
/** 直接指定时间 */
@property (nonatomic, strong) NSDate *Date;
/** 传入年、月、日 ，设置时间 */
-(void) setYear:(NSString *)year month:(NSString *)month day:(NSString *)day;

```

#####目前，这个控制器还是相对简陋的，还有完善的空间
      - 控制器中的"取消"按钮只是实现了 modal的推出，
      - 还没有做缓存相关的操作
      - 目前只是在单线程中完成所有工作
      
      
      
学习阶段，请各位大神指点一二 (抱拳)

