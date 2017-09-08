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
	
	
	
## /redpacket/userredpacket
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- 
| offset     |起始值 | int | 是 |0|


	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "redpacketconfID": "1",
            "userID": "277",
            "amount": "1",
            "addTime": "0",
            "userName": "",
            "phone": "15210694268",
            "avatar": "",
            "bindwx": "0"
        },
        {
            "redpacketconfID": "5",
            "userID": "277",
            "amount": "1",
            "addTime": "0",
            "userName": "",
            "phone": "15210694268",
            "avatar": "",
            "bindwx": "0"
        },
        {
            "redpacketconfID": "5",
            "userID": "289",
            "amount": "1",
            "addTime": "0",
            "userName": "",
            "phone": "18911547532",
            "avatar": "",
            "bindwx": "0"
        },
        {
            "redpacketconfID": "6",
            "userID": "277",
            "amount": "1",
            "addTime": "0",
            "userName": "",
            "phone": "15210694268",
            "avatar": "",
            "bindwx": "0"
        },
    ]
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
    	"glodamount": 10,
    	"isBigLucky" : 0,  1表示是天降鸿运  0表示不是
    	"memo":""  备注,天降鸿运的备注
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
	
	
	
## /useraccount/withdrawlist
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
| offset     |起始值 | int | 是 ||
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "widthdrawID": "330",
            "accountID": "278",
            "amount": "1",
            "status": "1",
            "addTime": "1503639650"
        },
        {
            "widthdrawID": "329",
            "accountID": "278",
            "amount": "1",
            "status": "1",
            "addTime": "1503639649"
        },
        {
            "widthdrawID": "328",
            "accountID": "278",
            "amount": "1",
            "status": "0",
            "addTime": "1503639276"
        },
        {
            "widthdrawID": "327",
            "accountID": "278",
            "amount": "1",
            "status": "0",
            "addTime": "1503639174"
        }
    ]
	}
	
## /useraccount/withdraw
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
| amount     |金额 | int | 是 ||

	{
    "errorno": 0,
    "errormsg": "",   失败返回no-money
    "data": []
    }
    
    
## /useraccount/transaction
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
| offset     |起始值 | int | 是 ||


	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "transactionID": "331",
            "accountID": "278",
            "amount": "1",
            "transactionType": "1",
            "summaryID": "1",
            "memo": "红包收入",
            "addTime": "1503641890"
        }
    ]
	}
	
## /config/biglucky


	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "imgpath": "abc",
        "desc": ""
    }
	}

## /config/glodext


	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "glod": 340,
        "money": 20
    }
	}
	

## /user/setthriddata
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
| thrid_data     |数据 | string（json） | 是 ||
| thrid     |数据标记(wx,tb) | string | 是 ||


	{
    "errorno": 0,
    "errormsg": "",
    "data": []
	}
	
## /product/addhistory
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
| product_id|产品ID | int | 是 ||


	{
    "errorno": 0,
    "errormsg": "",
    "data": []
	}

## /product/visithistory
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| offset     |起始值  | int | 是 ||	

	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "item_url": "http://item.taobao.com/item.htm?id=552216589108",
            "nick": "u670du88c5u6279u53d1u5546",
            "num_iid": "552216589108",
            "pict_url": "http://img2.tbcdn.cn/tfscom/i4/TB1cHOCQVXXXXbYXpXXXXXXXXXX_!!0-item_pic.jpg",
            "provcity": "u6d59u6c5f u676du5dde",
            "reserve_price": "220.50",
            "seller_id": "23419634",
            "small_images": {
                "string": [
                    "http://img1.tbcdn.cn/tfscom/i1/28689/TB2AlYQnmFjpuFjSszhXXaBuVXa_!!28689.jpg",
                    "http://img2.tbcdn.cn/tfscom/i4/28689/TB2Fm.lpHlmpuFjSZFlXXbdQXXa_!!28689.jpg",
                    "http://img4.tbcdn.cn/tfscom/i2/28689/TB2tmQjpNxmpuFjSZFNXXXrRXXa_!!28689.jpg",
                    "http://img1.tbcdn.cn/tfscom/i2/28689/TB2I7fqngJlpuFjSspjXXcT.pXa_!!28689.jpg"
                ]
            },
            "title": "X41717u5b57u6bcdu523au7ee3u5916u5957 u957fu8896u8584u9632u6652u670du6237u5916u8fd0u52a8u9632u6652u8863u65b0BESTBAOu6b63u5973u88c5",
            "user_type": "0",
            "volume": "0",
            "zk_final_price": "220.50"
        }
    ]
	}

	
## /product/productlist
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| category     |数据 | int | 是 ||
| offset     |起始值  | int | 是 ||	
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "item_url": "http://item.taobao.com/item.htm?id=552216589108",
            "nick": "u670du88c5u6279u53d1u5546",
            "num_iid": "552216589108",
            "pict_url": "http://img2.tbcdn.cn/tfscom/i4/TB1cHOCQVXXXXbYXpXXXXXXXXXX_!!0-item_pic.jpg",
            "provcity": "u6d59u6c5f u676du5dde",
            "reserve_price": "220.50",
            "seller_id": "23419634",
            "small_images": {
                "string": [
                    "http://img1.tbcdn.cn/tfscom/i1/28689/TB2AlYQnmFjpuFjSszhXXaBuVXa_!!28689.jpg",
                    "http://img2.tbcdn.cn/tfscom/i4/28689/TB2Fm.lpHlmpuFjSZFlXXbdQXXa_!!28689.jpg",
                    "http://img4.tbcdn.cn/tfscom/i2/28689/TB2tmQjpNxmpuFjSZFNXXXrRXXa_!!28689.jpg",
                    "http://img1.tbcdn.cn/tfscom/i2/28689/TB2I7fqngJlpuFjSspjXXcT.pXa_!!28689.jpg"
                ]
            },
            "title": "X41717u5b57u6bcdu523au7ee3u5916u5957 u957fu8896u8584u9632u6652u670du6237u5916u8fd0u52a8u9632u6652u8863u65b0BESTBAOu6b63u5973u88c5",
            "user_type": "0",
            "volume": "0",
            "zk_final_price": "220.50"
        },
        {
            "item_url": "http://item.taobao.com/item.htm?id=552216589108",
            "nick": "u670du88c5u6279u53d1u5546",
            "num_iid": "552216589108",
            "pict_url": "http://img2.tbcdn.cn/tfscom/i4/TB1cHOCQVXXXXbYXpXXXXXXXXXX_!!0-item_pic.jpg",
            "provcity": "u6d59u6c5f u676du5dde",
            "reserve_price": "220.50",
            "seller_id": "23419634",
            "small_images": {
                "string": [
                    "http://img1.tbcdn.cn/tfscom/i1/28689/TB2AlYQnmFjpuFjSszhXXaBuVXa_!!28689.jpg",
                    "http://img2.tbcdn.cn/tfscom/i4/28689/TB2Fm.lpHlmpuFjSZFlXXbdQXXa_!!28689.jpg",
                    "http://img4.tbcdn.cn/tfscom/i2/28689/TB2tmQjpNxmpuFjSZFNXXXrRXXa_!!28689.jpg",
                    "http://img1.tbcdn.cn/tfscom/i2/28689/TB2I7fqngJlpuFjSspjXXcT.pXa_!!28689.jpg"
                ]
            },
            "title": "X41717u5b57u6bcdu523au7ee3u5916u5957 u957fu8896u8584u9632u6652u670du6237u5916u8fd0u52a8u9632u6652u8863u65b0BESTBAOu6b63u5973u88c5",
            "user_type": "0",
            "volume": "0",
            "zk_final_price": "220.50"
        },
        {
            "item_url": "http://item.taobao.com/item.htm?id=552216589108",
            "nick": "u670du88c5u6279u53d1u5546",
            "num_iid": "552216589108",
            "pict_url": "http://img2.tbcdn.cn/tfscom/i4/TB1cHOCQVXXXXbYXpXXXXXXXXXX_!!0-item_pic.jpg",
            "provcity": "u6d59u6c5f u676du5dde",
            "reserve_price": "220.50",
            "seller_id": "23419634",
            "small_images": {
                "string": [
                    "http://img1.tbcdn.cn/tfscom/i1/28689/TB2AlYQnmFjpuFjSszhXXaBuVXa_!!28689.jpg",
                    "http://img2.tbcdn.cn/tfscom/i4/28689/TB2Fm.lpHlmpuFjSZFlXXbdQXXa_!!28689.jpg",
                    "http://img4.tbcdn.cn/tfscom/i2/28689/TB2tmQjpNxmpuFjSZFNXXXrRXXa_!!28689.jpg",
                    "http://img1.tbcdn.cn/tfscom/i2/28689/TB2I7fqngJlpuFjSspjXXcT.pXa_!!28689.jpg"
                ]
            },
            "title": "X41717u5b57u6bcdu523au7ee3u5916u5957 u957fu8896u8584u9632u6652u670du6237u5916u8fd0u52a8u9632u6652u8863u65b0BESTBAOu6b63u5973u88c5",
            "user_type": "0",
            "volume": "0",
            "zk_final_price": "220.50"
        }
    ]
	}
	
	
## /user/adduserext
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
| area_id     |地区 | int | 是 ||
| grand     |性别 | int | 是 |1男 2女 0保密|
| birthday     |生日时间戳 | int | 是 ||

	{
    "errorno": 0,
    "errormsg": "",   
    "data": []
    }
    
    
## /user/areainfo
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| parent_id     |上级id默认0 | int | 是 ||

	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "areaID": "11",
            "name": "北京",
            "parentid": "0",
            "vieworder": "1"
        },
        {
            "areaID": "31",
            "name": "上海",
            "parentid": "0",
            "vieworder": "2"
        },
        {
            "areaID": "44",
            "name": "广东",
            "parentid": "0",
            "vieworder": "3"
        },
        {
            "areaID": "34",
            "name": "安徽",
            "parentid": "0",
            "vieworder": "4"
        },
        {
            "areaID": "50",
            "name": "重庆",
            "parentid": "0",
            "vieworder": "5"
        },
        {
            "areaID": "35",
            "name": "福建",
            "parentid": "0",
            "vieworder": "6"
        },
        {
            "areaID": "46",
            "name": "海南",
            "parentid": "0",
            "vieworder": "7"
        },
        {
            "areaID": "13",
            "name": "河北",
            "parentid": "0",
            "vieworder": "8"
        },
        {
            "areaID": "41",
            "name": "河南",
            "parentid": "0",
            "vieworder": "9"
        },
        {
            "areaID": "23",
            "name": "黑龙江",
            "parentid": "0",
            "vieworder": "10"
        },
        {
            "areaID": "42",
            "name": "湖北",
            "parentid": "0",
            "vieworder": "11"
        },
        {
            "areaID": "43",
            "name": "湖南",
            "parentid": "0",
            "vieworder": "12"
        },
        {
            "areaID": "62",
            "name": "甘肃",
            "parentid": "0",
            "vieworder": "13"
        },
        {
            "areaID": "45",
            "name": "广西",
            "parentid": "0",
            "vieworder": "14"
        },
        {
            "areaID": "52",
            "name": "贵州",
            "parentid": "0",
            "vieworder": "15"
        },
        {
            "areaID": "22",
            "name": "吉林",
            "parentid": "0",
            "vieworder": "16"
        },
        {
            "areaID": "36",
            "name": "江西",
            "parentid": "0",
            "vieworder": "17"
        },
        {
            "areaID": "32",
            "name": "江苏",
            "parentid": "0",
            "vieworder": "18"
        },
        {
            "areaID": "21",
            "name": "辽宁",
            "parentid": "0",
            "vieworder": "19"
        },
        {
            "areaID": "15",
            "name": "内蒙古",
            "parentid": "0",
            "vieworder": "20"
        },
        {
            "areaID": "64",
            "name": "宁夏",
            "parentid": "0",
            "vieworder": "21"
        },
        {
            "areaID": "63",
            "name": "青海",
            "parentid": "0",
            "vieworder": "22"
        },
        {
            "areaID": "37",
            "name": "山东",
            "parentid": "0",
            "vieworder": "23"
        },
        {
            "areaID": "14",
            "name": "山西",
            "parentid": "0",
            "vieworder": "24"
        },
        {
            "areaID": "61",
            "name": "陕西",
            "parentid": "0",
            "vieworder": "25"
        },
        {
            "areaID": "51",
            "name": "四川",
            "parentid": "0",
            "vieworder": "26"
        },
        {
            "areaID": "12",
            "name": "天津",
            "parentid": "0",
            "vieworder": "27"
        },
        {
            "areaID": "54",
            "name": "西藏",
            "parentid": "0",
            "vieworder": "28"
        },
        {
            "areaID": "65",
            "name": "新疆",
            "parentid": "0",
            "vieworder": "29"
        },
        {
            "areaID": "53",
            "name": "云南",
            "parentid": "0",
            "vieworder": "30"
        },
        {
            "areaID": "33",
            "name": "浙江",
            "parentid": "0",
            "vieworder": "31"
        },
        {
            "areaID": "71",
            "name": "台湾",
            "parentid": "0",
            "vieworder": "32"
        },
        {
            "areaID": "81",
            "name": "香港",
            "parentid": "0",
            "vieworder": "33"
        },
        {
            "areaID": "82",
            "name": "澳门",
            "parentid": "0",
            "vieworder": "34"
        }
     ]
 	}
 
   
## /actredpacketrecomm/getinfo
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token | string | 是 ||
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "actredpacketID": "922",
            "userID": "87",
            "totalAmount": "20",
            "totalCount": "3",
            "leftCount": "3"
        },
        {
            "actredpacketID": "926",
            "userID": "87",
            "totalAmount": "25",
            "totalCount": "4",
            "leftCount": "4"
        },
        {
            "actredpacketID": "931",
            "userID": "87",
            "totalAmount": "35",
            "totalCount": "5",
            "leftCount": "5"
        },
        {
            "actredpacketID": "937",
            "userID": "87",
            "totalAmount": "40",
            "totalCount": "6",
            "leftCount": "6"
        },
        {
            "actredpacketID": "944",
            "userID": "87",
            "totalAmount": "68",
            "totalCount": "9",
            "leftCount": "9"
        }
    ]
	}
