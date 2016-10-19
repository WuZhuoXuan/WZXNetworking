# WZXNetworking（麻烦给个星star）


封装网络请求(AFNetworking 3.0.4版本)

## 使用方法

```objc

/**
 *  GET请求接口，若不指定baseurl，可传完整的url
 *
 *  @param url     接口路径
 *  @param success 接口成功请求到数据的回调
 *  @param fail    接口请求数据失败的回调
 *
 *  @return 返回的对象中可取消请求的API
 */

+ (WZXURLSessionTask *)getWithUrl:(NSString *)url success:(WZXResponseSuccess)success fail:(WZXResponseError)fail;

、、、

/**
 *  POST请求接口
 *
 *  @param url     接口路径
 *  @param params  接口所需的参数
 *  @param success 接口成功请求到数据的回调
 *  @param fail    接口请求数据失败的回调
 *
 *  @return 返回的对象中有可能取消请求的API
 */
+ (WZXURLSessionTask *)postWithUrl:(NSString *)url params:(NSDictionary *)params success:(WZXResponseSuccess)success fail:(WZXResponseError)fail;


/**
 *  图片上传调用方法
 *
 *  @param url                请求的URL地址
 *  @param params             额外的参数
 *  @param arrImage           图片集合数组
 *  @param compressionQuality 压缩比例
 */
+ (void)updataVideoWithUrl:(NSString *)url withParams:(NSDictionary *)params withImage:(NSArray *)arrImage withCompressionQuality:(CGFloat)compressionQuality success:(WZXResponseSuccess)success fail:(WZXResponseError)fail;


```
