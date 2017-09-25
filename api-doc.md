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
	

## /product/productlistv2
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| category     |数据 | int | 是 ||
| offset     |起始值  | int | 是 ||	
| token     |token  | string | 是 ||
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "productlist": [
            {
                "item_url": "http://item.taobao.com/item.htm?id=552605162354",
                "nick": "娜诗恋旗舰店",
                "num_iid": "552605162354",
                "pict_url": "http://img1.tbcdn.cn/tfscom/i3/TB1w_.YRpXXXXcpaFXXXXXXXXXX_!!0-item_pic.jpg",
                "provcity": "广东 广州",
                "reserve_price": "198.00",
                "seller_id": "2937316768",
                "small_images": {
                    "string": [
                        "http://img2.tbcdn.cn/tfscom/i3/2937316768/TB27g5acwoQMeJjy0FoXXcShVXa_!!2937316768.jpg",
                        "http://img1.tbcdn.cn/tfscom/i1/2937316768/TB24HI5rY0kpuFjy0FjXXcBbVXa_!!2937316768.jpg",
                        "http://img2.tbcdn.cn/tfscom/i3/2937316768/TB2vxCJvJRopuFjSZFtXXcanpXa_!!2937316768.jpg",
                        "http://img3.tbcdn.cn/tfscom/i4/2937316768/TB2ywCwvJ0opuFjSZFxXXaDNVXa_!!2937316768.jpg"
                    ]
                },
                "title": "短裤女夏2017新款气质高腰韩版宽松显瘦学生热裤潮破洞白色牛仔裤",
                "user_type": "1",
                "volume": "27709",
                "zk_final_price": "29.00"
            },
            {
                "item_url": "http://item.taobao.com/item.htm?id=541843655780",
                "nick": "金晓晓52099",
                "num_iid": "541843655780",
                "pict_url": "http://img2.tbcdn.cn/tfscom/i4/1960542000/TB2FuFXkY8kpuFjy0FcXXaUhpXa_!!1960542000.jpg",
                "provcity": "河北 保定",
                "reserve_price": "128.00",
                "seller_id": "1960542000",
                "small_images": {
                    "string": [
                        "http://img2.tbcdn.cn/tfscom/i2/1960542000/TB2GbE7bhqK.eBjSZJiXXaOSFXa_!!1960542000.jpg",
                        "http://img1.tbcdn.cn/tfscom/i4/1960542000/TB2DL3TblyN.eBjSZFIXXXbUVXa_!!1960542000.jpg",
                        "http://img3.tbcdn.cn/tfscom/i4/1960542000/TB2m8A9kSFjpuFjSspbXXXagVXa_!!1960542000.jpg",
                        "http://img1.tbcdn.cn/tfscom/i1/1960542000/TB2Wq7SkR4lpuFjy1zjXXcAKpXa_!!1960542000.jpg"
                    ]
                },
                "title": "韩版帆布双肩包女学生休闲百搭书包校园小清新初中生可爱开学背包",
                "user_type": "0",
                "volume": "27330",
                "zk_final_price": "48.00"
            },
            {
                "item_url": "http://item.taobao.com/item.htm?id=19073181848",
                "nick": "游乐者旗舰店",
                "num_iid": "19073181848",
                "pict_url": "http://img4.tbcdn.cn/tfscom/i1/TB1C3NfRXXXXXcKXFXXXXXXXXXX_!!0-item_pic.jpg",
                "provcity": "浙江 杭州",
                "reserve_price": "339.00",
                "seller_id": "1726473375",
                "small_images": {
                    "string": [
                        "http://img3.tbcdn.cn/tfscom/i2/1726473375/TB2y16jdItnpuFjSZFvXXbcTpXa_!!1726473375.jpg",
                        "http://img4.tbcdn.cn/tfscom/i1/1726473375/TB20yWFbbxmpuFjSZJiXXXauVXa_!!1726473375.jpg",
                        "http://img4.tbcdn.cn/tfscom/i3/1726473375/TB23MKFbmFmpuFjSZFrXXayOXXa_!!1726473375.jpg",
                        "http://img3.tbcdn.cn/tfscom/i1/1726473375/TB2BZ1mkR8kpuFjSspeXXc7IpXa_!!1726473375.jpg"
                    ]
                },
                "title": "游乐者拉杆箱行李箱万向轮旅行箱男女密码箱登机箱20寸24寸28潮",
                "user_type": "1",
                "volume": "26774",
                "zk_final_price": "76.00"
            },
            {
                "item_url": "http://item.taobao.com/item.htm?id=553618355465",
                "nick": "爱恋上草莓的味道",
                "num_iid": "553618355465",
                "pict_url": "http://img2.tbcdn.cn/tfscom/i2/1027546731/TB2jh7axHBmpuFjSZFuXXaG_XXa_!!1027546731.jpg",
                "provcity": "浙江 杭州",
                "reserve_price": "85.00",
                "seller_id": "1027546731",
                "small_images": {
                    "string": [
                        "http://img2.tbcdn.cn/tfscom/i2/1027546731/TB2q5fZxNhmpuFjSZFyXXcLdFXa_!!1027546731.jpg",
                        "http://img2.tbcdn.cn/tfscom/i4/1027546731/TB2xlqaecPRfKJjSZFOXXbKEVXa_!!1027546731.jpg",
                        "http://img1.tbcdn.cn/tfscom/i1/1027546731/TB2MmbVxOpnpuFjSZFkXXc4ZpXa_!!1027546731.jpg",
                        "http://img2.tbcdn.cn/tfscom/i4/1027546731/TB2ejz5c_AKh1JjSZFDXXbKlFXa_!!1027546731.jpg"
                    ]
                },
                "title": "2017春夏季小白鞋帆布鞋女学生韩版原宿ulzzang平底布鞋百搭板鞋",
                "user_type": "0",
                "volume": "23593",
                "zk_final_price": "21.90"
            },
            {
                "item_url": "http://item.taobao.com/item.htm?id=546357276052",
                "nick": "艾莉莎箱包",
                "num_iid": "546357276052",
                "pict_url": "http://img3.tbcdn.cn/tfscom/i4/725455405/TB2y7WobS_9F1JjSZFhXXbadVXa_!!725455405.jpg",
                "provcity": "浙江 嘉兴",
                "reserve_price": "319.00",
                "seller_id": "725455405",
                "small_images": {
                    "string": [
                        "http://img2.tbcdn.cn/tfscom/i1/725455405/TB22W6ZirBmpuFjSZFAXXaQ0pXa_!!725455405.jpg",
                        "http://img1.tbcdn.cn/tfscom/i4/725455405/TB2_nt2ha8lpuFjy0FpXXaGrpXa_!!725455405.jpg",
                        "http://img3.tbcdn.cn/tfscom/i4/725455405/TB20onOiypnpuFjSZFkXXc4ZpXa_!!725455405.jpg",
                        "http://img3.tbcdn.cn/tfscom/i3/725455405/TB2jyYFitFopuFjSZFHXXbSlXXa_!!725455405.jpg"
                    ]
                },
                "title": "铝框拉杆箱密码行李箱男女旅行箱万向轮20皮箱子24韩版26学生28寸",
                "user_type": "0",
                "volume": "23283",
                "zk_final_price": "139.00"
            },
            {
                "item_url": "http://item.taobao.com/item.htm?id=37841313671",
                "nick": "dgfynet",
                "num_iid": "37841313671",
                "pict_url": "http://img2.tbcdn.cn/tfscom/i3/TB1gqYoOFXXXXbSaXXXYXGcGpXX_M2.SS2",
                "provcity": "广东 东莞",
                "reserve_price": "50.00",
                "seller_id": "355460794",
                "small_images": {
                    "string": [
                        "http://img4.tbcdn.cn/tfscom/i4/355460794/TB2HK6.XYFlpuFjy0FgXXbRBVXa_!!355460794.jpg",
                        "http://img4.tbcdn.cn/tfscom/i5/TB1chzHOFXXXXXaXVXXYXGcGpXX_M2.SS2",
                        "http://img2.tbcdn.cn/tfscom/i8/TB1wwTcOFXXXXXsaFXXYXGcGpXX_M2.SS2",
                        "http://img4.tbcdn.cn/tfscom/i4/TB13aG1QpXXXXcPXVXXYXGcGpXX_M2.SS2"
                    ]
                },
                "title": "外搭宽松早秋女装新款2017针织衫开衫短款薄款春秋天毛衣长袖外套",
                "user_type": "0",
                "volume": "20910",
                "zk_final_price": "29.00"
            },
            {
                "item_url": "http://item.taobao.com/item.htm?id=42186460554",
                "nick": "桃太郎旗舰店",
                "num_iid": "42186460554",
                "pict_url": "http://img3.tbcdn.cn/tfscom/i2/TB1LR0lLXXXXXaGXVXXXXXXXXXX_!!0-item_pic.jpg",
                "provcity": "浙江 金华",
                "reserve_price": "68.00",
                "seller_id": "902777980",
                "small_images": {
                    "string": [
                        "http://img3.tbcdn.cn/tfscom/i4/902777980/TB21FxZb9Y9F1JjSZFFXXaBKXXa_!!902777980.jpg",
                        "http://img2.tbcdn.cn/tfscom/i1/902777980/TB2wci_ayGO.eBjSZFEXXcy9VXa_!!902777980.jpg",
                        "http://img4.tbcdn.cn/tfscom/i3/902777980/TB2chKobeEJL1JjSZFGXXa6OXXa_!!902777980.jpg",
                        "http://img1.tbcdn.cn/tfscom/i3/902777980/TB2bQXYaUifF1JjSspdXXclLpXa_!!902777980.jpg"
                    ]
                },
                "title": "加绒仿皮打底裤加厚外穿长裤显瘦黑色小脚裤皮裤弹力大码女裤秋冬",
                "user_type": "1",
                "volume": "20259",
                "zk_final_price": "6.90"
            },
            {
                "item_url": "http://item.taobao.com/item.htm?id=554623954444",
                "nick": "魅思莹旗舰店",
                "num_iid": "554623954444",
                "pict_url": "http://img2.tbcdn.cn/tfscom/i1/TB1MIpASXXXXXb6XpXXXXXXXXXX_!!0-item_pic.jpg",
                "provcity": "江苏 苏州",
                "reserve_price": "98.00",
                "seller_id": "3204149102",
                "small_images": {
                    "string": [
                        "http://img4.tbcdn.cn/tfscom/i3/3204149102/TB2qcaJtJhvOuFjSZFBXXcZgFXa_!!3204149102.jpg",
                        "http://img2.tbcdn.cn/tfscom/i1/3204149102/TB2RK24zNxmpuFjSZFNXXXrRXXa_!!3204149102.jpg",
                        "http://img4.tbcdn.cn/tfscom/i4/3204149102/TB2FH3nvCFjpuFjSszhXXaBuVXa_!!3204149102.jpg",
                        "http://img3.tbcdn.cn/tfscom/i3/3204149102/TB25ULWzOpnpuFjSZFIXXXh2VXa_!!3204149102.jpg"
                    ]
                },
                "title": "夏装新款V领针织小吊带镂空背心女 短款外穿无袖t恤女打底衫韩版",
                "user_type": "1",
                "volume": "20236",
                "zk_final_price": "18.90"
            },
            {
                "item_url": "http://item.taobao.com/item.htm?id=549310039411",
                "nick": "影麦旗舰店",
                "num_iid": "549310039411",
                "pict_url": "http://img3.tbcdn.cn/tfscom/i2/TB1iOEJQFXXXXcOXFXXXXXXXXXX_!!0-item_pic.jpg",
                "provcity": "浙江 杭州",
                "reserve_price": "100.00",
                "seller_id": "1891886484",
                "small_images": {
                    "string": [
                        "http://img3.tbcdn.cn/tfscom/i3/1891886484/TB2k5XcphtmpuFjSZFqXXbHFpXa_!!1891886484.jpg",
                        "http://img2.tbcdn.cn/tfscom/i2/1891886484/TB2kreKmHRkpuFjSspmXXc.9XXa_!!1891886484.jpg",
                        "http://img4.tbcdn.cn/tfscom/i4/1891886484/TB2rFVYmSXlpuFjy0FeXXcJbFXa_!!1891886484.jpg",
                        "http://img3.tbcdn.cn/tfscom/i4/1891886484/TB2GzbNeY_0UKFjy1XaXXbKfXXa_!!1891886484.jpg"
                    ]
                },
                "title": "打底裤外穿薄款女裤子秋季2017新款韩版百搭九分夏季显瘦黑小脚裤",
                "user_type": "1",
                "volume": "19641",
                "zk_final_price": "19.90"
            },
            {
                "item_url": "http://item.taobao.com/item.htm?id=555811282418",
                "nick": "魔袖旗舰店",
                "num_iid": "555811282418",
                "pict_url": "http://img4.tbcdn.cn/tfscom/i1/TB1eE_5SpXXXXXRaXXXXXXXXXXX_!!0-item_pic.jpg",
                "provcity": "江苏 苏州",
                "reserve_price": "98.00",
                "seller_id": "3010208181",
                "small_images": {
                    "string": [
                        "http://img2.tbcdn.cn/tfscom/i4/3010208181/TB2f6xiceZkyKJjSszgXXcpMpXa_!!3010208181.jpg",
                        "http://img1.tbcdn.cn/tfscom/i1/3010208181/TB2Z7BGcj7jyKJjy1XaXXblnFXa_!!3010208181.jpg",
                        "http://img2.tbcdn.cn/tfscom/i4/3010208181/TB2FNZIdQonyKJjSZFtXXXNaVXa_!!3010208181.jpg",
                        "http://img4.tbcdn.cn/tfscom/i1/3010208181/TB2k4cXa77myKJjSZFzXXXgDpXa_!!3010208181.png"
                    ]
                },
                "title": "高领套头毛衣女装秋冬新款韩版宽松原宿加厚百搭打底针织衫潮外套",
                "user_type": "1",
                "volume": "19531",
                "zk_final_price": "21.90"
            }
        ],
        "luckydata": {
            "type": 1,
            "amount": 0
        }
    }
	}

	
## /product/search
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| keyword     |数据 | string | 否 ||
| offset     |起始值  | int | 否 ||	
	
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




## /orderreward/reward
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| order_id     |订单 | string | 是 ||
| token     |token  | string | 是 ||
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "type": 1, //1 金币  2 红包
        "amount": 100
    }
	}
	
## /orderreward/recordlist
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
            "addTime": 123
        }
    ]
	}
 	

## /orderreward/recommendstat
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
            "username": "测试",
            "phone": "15210694268",
            "avatar": "http://xxx",
            "paied": {
                "1": 100,
                "2": 200
            },
            "notpay": {
                "1": 105,
                "2": 205
            }
        }
    ]
	}


## /orderreward/banner
	
	{
    "errorno": 0,
    "errormsg": "",
    "data": {
        "banner": "http://xxx"
    }
	}	
	
	
## /useraccount/withdrawconf
| 参数名称        |说明| 类型           | 是否必填  |默认值|
| --------- | ---------|:---------:|---------:|--------- |
| token     |token  | string | 是 ||

	{
    "errorno": 0,
    "errormsg": "",
    "data": [
        {
            "amount": 3000, //提现金额
            "enable": 0,  //0 不可用 1可用   
            "recomcount": 10 //推荐人数
        },
        {
            "amount": 5000,
            "enable": 1,
            "recomcount": 8
        },
        {
            "amount": 10000,
            "enable": 1,
            "recomcount": 5
        }
    ]
	}