# TelTest
学习iOS app调用系统打电话、发短信、发邮件功能

## 介绍
在应用程序内，调用系统的功能来实现打电话、发短信和发邮件，通过电话号码或者邮箱，直接跳转到系统的功能界面。

## 方法
* 打电话
```Objective-C
UIWebView *callWebview =[[UIWebView alloc] init];  
NSURL *telURL =[NSURL URLWithString:[NSString stringWithFormat:@"tel:%@",self.phoneNumber.text]];  
[callWebview loadRequest:[NSURLRequest requestWithURL:telURL]];  
[self.view addSubview:callWebview];  
```

* 发短信
```Objective-C
UIWebView *smsWebview =[[UIWebView alloc] init];  
NSURL *telURL =[NSURL URLWithString:[NSString stringWithFormat:@"sms:%@",self.phoneNumber.text]];  
[smsWebview loadRequest:[NSURLRequest requestWithURL:telURL]];  
[self.view addSubview:smsWebview];   
```

* 发邮件
```Objective-C
UIWebView *emailWebview =[[UIWebView alloc] init];  
NSURL *emailURL =[NSURL URLWithString:[NSString stringWithFormat:@"mailto:%@",self.email.text]];  
[emailWebview loadRequest:[NSURLRequest requestWithURL:emailURL]];  
[self.view addSubview:emailWebview];  
```

详细说明查看[我的博客](http://blog.csdn.net/cloudox_/article/details/47980377)
