### Android HiBernate实体表单验证插件;利用对象属性注解，可调属性验证顺序；相对属性比较等功能;
#### 版本功能描述
```doc
1.0.0

可调整属性验证顺序；【@Order(序列)】
非空验证;	【@NotEmpty(message = "提示信息")】
长度验证;【@Length(min = 3, max = 10, message = "长度在3~10之间")】
最小值验证;【@Min(value = 1, message = "提示信息")】
最大值验证; [@Max(value = 10, message = "提示信息")]
正则验证;【@Pattern(regexp = "[\\d]+",message = "必须为整数")】
比较验证;【@CompareId("nametag")-属性1;@Compare(refId = "nametag", symbol = CompareSymbol.eq, message = "两次输入的名称不一致")-属性2】

1.0.1预发版本功能

比较验证时增加业务逻辑验证
```
#### 示例
```java
private ValidatorForm validatorForm = null;

validatorForm = ValidatorForm.getInstance(this);
validatorForm.setOnValidationListener(validationListener);

private OnValidationListener validationListener = new OnValidationListener() {
    @Override
    public void onValidationSucceeded() {
        //valid success
    }

    @Override
    public void onValidationFailed(String message) {
        //output current error message
    }
};

//获取实体并提交验证
TestModel model = new TestModel();
//这里测试需要自定义设置值
validatorForm.valid(model);
```
#### 引用
###### 项目build.gradle引用仓库地址
```doc
repositories {
    maven { url 'http://mv.slcore.com:81/content/repositories/geeasejars/' }
}
```
###### 对应模块build.gradle引用以下版本
```doc
implementation 'com.geease:ebus:1.0.0'
```

###
<font size="12" color="#041d29">如果觉得有帮助请转到右上角顺序帮忙点个星吧！！！</font>
###
<font size="12" color="#041d29">如果觉得有帮助请转到右上角顺序帮忙点个星吧！！！</font>
###
<font size="12" color="#041d29">如果觉得有帮助请转到右上角顺序帮忙点个星吧！！！</font>