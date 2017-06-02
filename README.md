# IOS-TFHppleTest
IOSHTML解析测试

```
NSString *url = @"http://www.jianshu.com/u/e163bc6048d8";

//将网址转化为data数据
NSData *data = [[NSData alloc] initWithContentsOfURL:[NSURL URLWithString:url]];

//创建解析对象
TFHpple *xpathParser = [[TFHpple alloc] initWithHTMLData:data];
NSArray *dataArr = [xpathParser searchWithXPathQuery:@"//a"];

for (TFHppleElement *element in dataArr) {

if ([[element objectForKey:@"class"] isEqualToString:@"title"]) {
NSLog(@"%@\n",element.text);

}
}
```
