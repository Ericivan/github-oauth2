
# 基本配置

> app.php 加入 \Github\GithubServiceProvider::class,

> aliases 加入 Facade  'Github' => \Github\Facades\Github::class,

> serives.php 中加入配置项

```php
        'github'=>[
            'client_id' => 'client_id',
            'client_secret' => 'client_secret',
            'redirect_url' => 'redirect_url',
    ]
```

### 基本使用

>获取登录跳转地址


```php
    Github::with('github')->redirect();
```


>回调地址获取登录用户

```php
    $user=Github::with('github')->user();
```