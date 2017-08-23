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



## /user/getinfo

| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||


	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "userinfo": {
            "userID": "277",
            "userName": "",
            "phone": "15210694268",
            "avatar": "",
            "bindwx": "0"
        },
        "accountinfo": {
            "accountID": "278",
            "status": "1",
            "amount": "0"
        },
        "glodinfo": {
            "userglodID": "279",
            "status": "1",
            "amount": "0"
        }
    }
	}




## /user/sendauthcode

| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- |---------|:---------:| ---------:|---------|
| phone     |手机 | string | 是 ||

	{
    "errorno": 0,
    "errormsg": "",
    "data": []
	}


## /redpacket/current

| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- |---------|:---------:| ---------:|---------|
|      | |  |  ||

	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "system_time": 1503320917,
        "conf": [
            {
                "title": "9-clock",
                "onlineTime": "1503277200",
                "onlineDate": "1503244800",
                "status": "1"
            },
            {
                "title": "12-clock",
                "onlineTime": "1503288000",
                "onlineDate": "1503244800",
                "status": "1"
            },
            {
                "title": "15-clock",
                "onlineTime": "1503298800",
                "onlineDate": "1503244800",
                "status": "1"
            },
            {
                "title": "21-clock",
                "onlineTime": "1503320400",
                "onlineDate": "1503244800",
                "status": "1"
            }
        ]
    }
	}
	

## /redpacket/fight
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
| redpacket_id     |红包ID | int | 是 ||

	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "fightresult": {
            "result": "success",
            "data": {
                "redpacketconfID": "1",
                "userID": "277",
                "amount": "1"
            }
        }
    }
	}


## /redpacket/record
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
| redpacket_id     |红包ID | int | 是 ||
| offset     |翻页 | int | 是 |0|


	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "recordlist": [
            {
                "redpacketconfID": "1",
                "userID": "277",
                "amount": "1",
                "addTime": "0"
            },
            {
                "redpacketconfID": "1",
                "userID": "1",
                "amount": "1",
                "addTime": "0"
            },
            {
                "redpacketconfID": "1",
                "userID": "2",
                "amount": "1",
                "addTime": "0"
            },
            {
                "redpacketconfID": "1",
                "userID": "3",
                "amount": "3",
                "addTime": "0"
            }
        ],
        "userdata": {
            "redpacketconfID": "1",
            "userID": "277",
            "amount": "1"
        },
        "userinfo": {
            "277": {
                "userID": "277",
                "userName": "",
                "phone": "15210694268",
                "avatar": "",
                "bindwx": "0"
            }
        }
    }
	}	
	
## /redpacket/maxrecord
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
| redpacket_id     |红包ID | int | 是 ||

	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "userID": "3",
        "amount": "3",
        "userData":{
         	"avatar": "",
         	"bindwx": "0"
         }
    }
	}