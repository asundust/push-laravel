企业微信应用消息推送插件 Laravel客户端
======
> 本项目为客户端，服务端请查看[https://github.com/asundust/wechat-work-push(Laravel-Admin版)](https://github.com/asundust/wechat-work-push) [https://github.com/asundust/dcat-wechat-work-push(Dcat-Admin版)](https://github.com/asundust/dcat-wechat-work-push)

![StyleCI build status](https://github.styleci.io/repos/338733529/shield)
<a href="https://packagist.org/packages/asundust/push-laravel"><img src="https://img.shields.io/packagist/dt/asundust/push-laravel" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/asundust/push-laravel"><img src="https://img.shields.io/packagist/v/asundust/push-laravel" alt="Latest Stable Version"></a>

## 安装

### 安装

```
composer require asundust/push-laravel
```

### 发布配置文件

```
php artisan vendor:publish --provider="Asundust\PushLaravel\PushLaravelServiceProvider"
```

- 配置文件在`config/push-laravel.php`文件里

## 配置

可以配置多组配置

```
PUSH_URL=
PUSH_SECRET=
```

## 使用

```
// use Asundust\PushLaravel\Facades\PushLaravel;

$title = '我是测试标题';
$content = '我是测试内容';
$url = 'https://www.baidu.com/';
$urlTitle = '我是链接';

// 其中 $content $url $urlTitle 可不传
// 默认配置
app('push-laravel')->send($title, $content, $url, $urlTitle);
// 指定配置
app('push-laravel.xxxxxx')->send($title, $content, $url, $urlTitle);
// 默认配置
PushLaravel::send($title, $content, $url, $urlTitle);
// 指定配置
PushLaravel::config('xxxxxx')->send($title, $content, $url, $urlTitle);
```

## 支持

如果觉得这个项目帮你节约了时间，不妨支持一下呗！

![alipay](https://user-images.githubusercontent.com/6573979/91679916-2c4df500-eb7c-11ea-98a7-ab740ddda77d.png)
![wechat](https://user-images.githubusercontent.com/6573979/91679913-2b1cc800-eb7c-11ea-8915-eb0eced94aee.png)

## License

[The MIT License (MIT)](https://opensource.org/licenses/MIT)