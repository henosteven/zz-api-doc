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
        "system_time": 1503472224,
        "conf": [
            {
                "redpacketconfID": "9",
                "title": "9-clock",
                "onlineTime": "1503450000",
                "onlineDate": "1503417600",
                "status": "1",
                "userget": 0  //1表示抢到红包
            },
            {
                "redpacketconfID": "10",
                "title": "12-clock",
                "onlineTime": "1503460800",
                "onlineDate": "1503417600",
                "status": "1",
                "userget": 0
            },
            {
                "redpacketconfID": "11",
                "title": "15-clock",
                "onlineTime": "1503471600",
                "onlineDate": "1503417600",
                "status": "1",
                "userget": 0
            },
            {
                "redpacketconfID": "12",
                "title": "19-clock",
                "onlineTime": "1503486000",
                "onlineDate": "1503417600",
                "status": "1",
                "userget": 0
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
                "redpacketconfID": "8",
                "userID": "289",
                "amount": "1",
                "addTime": "0",
                "userName": "",
                "phone": "18911547532",
                "avatar": "",
                "bindwx": "0"
            },
            {
                "redpacketconfID": "8",
                "userID": "277",
                "amount": "1",
                "addTime": "0",
                "userName": "",
                "phone": "15210694268",
                "avatar": "",
                "bindwx": "0"
            }
        ],
        "userdata": {
            "redpacketconfID": "8",
            "userID": "277",
            "amount": "1",
            "userName": "",
            "phone": "15210694268",
            "avatar": "",
            "bindwx": "0"
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
	
	
## /redpacket/redpacketstat
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
| redpacket_id     |红包ID | int | 是 ||
	
	
	{
	 "errorno": 0,
	 "errormsg": "",
	"data": {
    "totalCount": "4", //红包总数
    "isDone": 1, //1 表示已经抢完   0 表示没有
    "timecount": 1, // 抢完了有分钟显示 1分钟
    "doneCount": "4" //红包已抢个数
    }
	}
	
	
	
## /glod/setflag
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
| product_id     |产品ID | int | 是 ||

	{
	"errorno": 0,
	"errormsg": "",
	"data": []
	}
	

## /glod/catchglod
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
| product_id     |产品ID | int | 是 ||


	{
	"errorno": 0,
	"errormsg": "",
	"data": {
		"status": "success",
    	"glodamount": 10
    	}
	}

## /glod/glodinfo
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||


	{
	"errorno": 0,
	"errormsg": "",
	"data": {
		"userID": "277",
		"status": "1",
    	"amount": "30"
		}
	}



## /glod/glodrecord
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
| offset     |起始值 | int | 是 ||


	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "amount": "10",
            "sourceType": "1",
            "memo": "",
            "addTime": "1503499383"
        },
        {
            "amount": "10",
            "sourceType": "1",
            "memo": "",
            "addTime": "1503498772"
        }
    ]
	}