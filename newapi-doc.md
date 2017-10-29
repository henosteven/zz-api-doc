##api-doc

common-params

* appversion  string | app版本
* ostype    int      | 1-ios 2-android
* versioncode  int   | 系统版本

## /growth/growthinfo 等级信息

| 参数名称        |说明| 类型           | 是否必填  |默认值|
| ------------- |-------------|:-------------:| -------------:|-------------|
| token     |用户token | string | 是 ||

	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "userlevelID": 1,
        "userID": 1,
        "cardNo": "123123",
        "levelID": 1,
        "levelTitle": "白金",
        "minScore": 1,
        "maxScore": 10,
        "curScore": 5
    }
	}



## /growth/curentscoreinfo 当前成长值

| 参数名称        |说明| 类型           | 是否必填  |默认值|
| ------------- |-------------|:-------------:| -------------:|-------------|
| token     |用户token | string | 是 ||
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "amount": 100
    }
	}
	
	
## /growth/scorerecord  成长值记录

| 参数名称        |说明| 类型           | 是否必填  |默认值|
| ------------- |-------------|:-------------:| -------------:|-------------|
| token     |用户token | string | 是 ||
| offset     |起始值 | int | 否 |0|
		
	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "socrerecordID": 1,
            "userID": 1,
            "incomeType": 1,
            "incomeDesc": "test",
            "summaryID": 1,
            "summaryDesc": "test",
            "amount": 10,
            "addTime": 123123123
        }
    ]
	}


## /growthreward/rewardlist 升保级奖励记录

| 参数名称        |说明| 类型           | 是否必填  |默认值|
| ------------- |-------------|:-------------:| -------------:|-------------|
| token     |用户token | string | 是 ||
| state     |状态 | int | 否 | 1 未领取  2 已领取 |
| offset     |起始值 | int | 否 |0|
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "userlevelrewardID": 1,
            "hasCatch": 1,
            "userID": 1,
            "levelrewardID": 1,
            'title':'酒店',
           'typeDesc":'白金保级',
            "addTime": 1508857597,
            "catchTime": 1508857597,
            "leveldata": {
                "title": "test",
                "iconPath": "http://"
            }
        }
    ]
	}
	
## /growthreward/catchreward 领取升保级

| 参数名称        |说明| 类型           | 是否必填  |默认值|
| ------------- |-------------|:-------------:| -------------:|-------------|
| token     |用户token | string | 是 ||
| userlevelrewardID     |奖励ID | int | 是 ||

	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "result": "success"   //failed 表示领取失败
    }
	}
	
	
## /orderreward/newstat  100%中奖统计

| 参数名称        |说明| 类型           | 是否必填  |默认值|
| ------------- |-------------|:-------------:| -------------:|-------------|
| token     |用户token | string | 是 ||	

	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "totalamount": 233,  //已领取
        "friendsupport": 456 //好友贡献
    }
}
	

## /orderreward/recordlistv2 100%用户收入列表
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| offset     |起始值  | int | 否 ||
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "userID": 1,
            "orderID": 123,
            "rewardType": 1,
            "amount": 100,
            "status": 2, //1待结算  2已结算  3 判定无效
            "statusDesc": "已结算",
            "payTime": 123,
            "addTime": 123,
            "userName": "",
            "phone": "18911547532",
            "avatar": "",
        }
    ]
	}
	
## /orderreward/recommendrewardlist 100%好友收入列表
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token  | string | 是 ||
| offset     |起始值  | int | 否 ||
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "userID": 1,
            "orderID": 123,
            "rewardType": 1,
            "amount": 100,
            "status": 2, //1待结算  2已结算  3 判定无效
            "statusDesc": "已结算",
            "payTime": 123,
            "addTime": 123,
            "userName": "",
            "phone": "18911547532",
            "avatar": "",
        }
    ]
	}
	
	
## /orderreward/recommstat 100% 好友统计
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token  | string | 是 ||
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "expectincome": 233,
        "realincome": 456,
        "recommendnum": 4
    }
	}
	
	
## /product/hotkeywords
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        "耐克"
    ]
	}	
	
## /product/tbcode
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| tbcode     |口令  | string | 是 ||
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "img": http://",
        "num_iid": 0,
        "price": 0,
        "coupon": 0,
        "title": 0
    }
 	}
 	
## /orderreward/recordlistv2
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token  | string | 是 ||
| offset     |起始值  | int | 否 ||
| status     |状态  | int | 否 ||
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "userID": 1,
            "orderID": 123,
            "rewardType": 1,
            "amount": 100,
            "status": 2, //1待结算  2已结算  3 判定无效
            "statusDesc": "已结算",
            "payTime": 123,
            "addTime": 123
        }
    ]
	}