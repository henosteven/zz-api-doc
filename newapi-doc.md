##api-doc

common-params

* appversion  string | app版本
* ostype    int      | 1-ios 2-android
* versioncode  int   | 系统版本

## /growth/growthinfo

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
        "levelTitle": "白金"
    }
	}



## /growth/curentscoreinfo

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
	
	
## /growth/scorerecord

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


## /growthreward/recordlist

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
            "addTime": 1508857597,
            "catchTime": 1508857597,
            "leveldata": {
                "title": "test",
                "iconPath": "http://"
            }
        }
    ]
	}
	
## /growthreward/catchreward

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
	
	

