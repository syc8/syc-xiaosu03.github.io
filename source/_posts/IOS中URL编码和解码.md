title: IOS中URL编码和解码
entitle: 'url-encoding-iOS'
author: 小苏
avatar: /images/favicon.png
authorLink: 'https://www.tangkunyin.com'
authorAbout: 'https://about.tangkunyin.com'
authorDesc: 在写bug的康庄大道上一骑绝尘
categories: 前端
timestamp: 1528012896
date: 2018-06-03 16:01:36
tags:
    - iOS
keywords: iOS, URL编码解码
description: 来自2015.5.13的笔记：IOS中URL编码和解码。
photos:
---

```
int main(int argc, const char * argv[]) {
    
    NSString *str = @"白日依山尽";
    
    //编码
    NSString *encoderStr = [str stringByAddingPercentEscapesUsingEncoding:NSUTF8StringEncoding];
    
    //解码
    NSString *decoderStr = [encoderStr stringByReplacingPercentEscapesUsingEncoding:NSUTF8StringEncoding];
    
    //字符串打散
    for (int i = 0; i < str.length; i++) {
        NSString *word = [str substringWithRange:NSMakeRange(i, 1)];
        NSLog(@"%@",word);
    }
    
    
    NSLog(@"%@",encoderStr);
    
    NSLog(@"%@",decoderStr);
    
    return 0;
}
```


