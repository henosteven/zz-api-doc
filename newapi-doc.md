##api-doc

common-params

* appversion  string | app版本
* ostype    int      | 1-ios 2-android
* versioncode  int   | 系统版本

## /user/login

| 参数名称        |说明| 类型           | 是否必填  |默认值|
| ------------- |-------------|:-------------:| -------------:|-------------|
| phone     |手机 | string | 是 ||
| authcode  |验证码| string |   是 ||
| channel |渠道|int|否 ||
| register_ip |ip|string|否 ||
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "token": "Mjc3JDE1MjEwNjk0MjY4XzBiYzc4ZjAyYTEyZTQ1NzA4MzdhYzcwZWE1MzBiODRm"
    }
	}

