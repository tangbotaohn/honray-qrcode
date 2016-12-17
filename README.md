# tp5-qrcode
thinkphp5 生成二维码类库

## 安装


> composer require honray/tp5-qrcode


##使用

###在后端生成二维码

~~~
<div>{:captcha_img()}</div>
~~~
或者
~~~
<div><img src="{:captcha_src()}" alt="captcha" /></div>
~~~
> 上面两种的最终效果是一样的

### 控制器里验证
使用TP5的内置验证功能即可
~~~
$this->validate($data,[
    'captcha|验证码'=>'required|captcha'
]);
~~~
或者手动验证
~~~
if(!captcha_check($captcha)){
 //验证失败
};
~~~