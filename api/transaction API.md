# transaction API（中文为解释说明） 

用于通过接口快速进行交易

2.1委托下单

接口	描述

exapi/api/trade/order	委托下单

示例

//# Request

entrustPrice:1 价格

type:1 买

coinCode:BTC_LTC

entrustCount:1 数量

entrustWay:1

accesskey:68 K值

Sign1：d5b6c24d00b571c298b32efca4775647

entrustPrice:2 价格

type:2  卖

coinCode:BTC_LTC

entrustCount:2 数量

entrustWay:1 

accesskey:公钥 68

Sign1：hlsafc24d00b5214296dbs2efca477ada

//# Response

{"success":true,"msg":"委托成功","obj":null,"code":""}

请求参数加密顺序	String aValue =entrustPrice+type+coinCode+entrustCount

2.2取消全部委托

exapi/api/trade/cancelOrder	取消全部委托

示例

//# Request

acoinCode =BTC_LTC

accesskey=key  公钥

//# Response

{"success":true,"

msg":"撤销成功",

"obj":null,"code":""}

返回值说明	Success：状态

Message：提示信息

参数说明

coinCode: 币的代码

Accesskey：公钥

请求参数加密顺序
	
String aValue =acoinCode

2.3获取我的委托

exapi/api/user/singleExEntrust	获取我的委托

示例

//# Request

"key":"accesskey","value":"68" 供钥

"key":"limit","value":"10" 显示的条数

"key":"offset","value":"0" 从第几条开始显示

"key":"sortOrder","value":"asc" 显示的顺序

"key":"querypath","value":"current" 查询数据的类型

"key":"sign1","value":"03d674d39203432cb2af8a61e3a12fb

//# Response

{

	"success": true,

	"msg": "",

	"obj": {

		"page": 1, 页数

		"pageSize": 10, 显示的条数

		"totalPage": 1, 总页数

		"recordsTotal": 1, 总条数

		"recordsFiltered": 1,

		"rows": [{

			"entrustNum": "180122165729001585", 单号

			"entrustTime": "2018-01-22 16:57:30", 时间

			"entrustTime_long": null,

			"source": 1, 来源 1为pc 8为aip

			"entrustPrice": 1,委托价格

			"entrustCount": 1,委托数量

			"type": 1,买卖类型 1为买2为卖

			"surplusEntrustCount": 1, 为成交数量

			"status": 0,

			"transactionSum": 0, 交易总金额

			"entrustSum": 1,委托数量

			"processedPrice": null,

			"coinCode": "BTC", 交易币

			"fixPriceCoinCode": "LTC", 定价币

			"coin": null

           		 }],

		"total": 1

		},

	"code": "8888"

}

返回值说明	Success：状态

Message：提示信息

参数说明	见上

请求参数加密顺序	

String aValue =limit+offset+sortOrder+querypath

2.4获取用户信息

exapi/api/user/getAccountInfo	获取用户信息

实例

//# Request

Accesskey ：68 公钥

sign1：5b4ecb8274578e7e sign

//# Response

{

	"success": true, 请求状态

	"msg": "", 返回消息

	"obj": {

		"isChongbi": "1", 是否开启充币需要实名认证 0 开 1关

		"coinAccount": [

           		 {

			"id": null,

			"coinCode": "USD", 币代码

			"hotMoney": 123123123, 可用总额

			"coldMoney": 0,冻结总额

			"picturePath": null,

			"name": "USD",币的名字

			"currencyType": "USD",币的类型

			"accountNum": "8800020008006081",虚拟账号

			"tokenId": "fbba9af4-5d6b-415f-b3c7-a2cefc9c3741", 为手机端使用

			"languageCode": null,

			"keepDecimalForCoin": null,

			"moneyAndCoin": 0 0为法币1为虚拟货币

           		 },

           		 {

			"id": 534,

			"coinCode": "BCC",

			"hotMoney": 0,

			"coldMoney": 0,

			"picturePath": "hryfile/6/b/d8f068e828754a18be3c5516908e1f21.png",

			"name": "比特币现金",

			"currencyType": null,

			"accountNum": null,

			"tokenId": "fbba9af4-5d6b-415f-b3c7-a2cefc9c3741",

			"languageCode": null,

			"keepDecimalForCoin": 10,

			"moneyAndCoin": 1

            		},

        			],

		"isTrade": "1",是否开启交易需要实名认证 0开 1关

		"witfee": 0.5,提现手续费率

		"maxWithdrawMoneyOneTime": "20000",一次最大提现

		"languageCode": "USD",定价币

		"maxWithdrawMoney": "20000",一天最大提现

		"user": {

			"saasId": "hurong_system",

			"created": null,

			"modified": null,

			"username": "1@1.cn"，用户名
	
			"password": "54a51aceddcd5cae153a6ae4124e28f5",

			"userCode": "a8b6548e24fd4172b9fb40186b201d7f",唯一标识

			"isReal": 1,是否实名0没有实名，1实名

			"isChange": 0,是否能交易  0可以交易  1不能交易

			"isDelete": 0,是否禁用  0没有禁用 1禁用

			"isLock": 0,是否锁定   0没锁定  1锁定

			"accountPassWord": "",交易密码

			"customerId": 68,

			"mobile": "1@1.cn",用户邮箱

			"truename": "啊",真实名

			"surname": "啊",真实姓

			"customerType": 1,客户类型

			"salt": "32bcb9a877421ac3f7b9d1b81de700c4",

			"cardcode": "123132",身份证

			"email": null,

			"sex": null,

			"postalAddress": null,详细地址

			"googleKey": null,

			"googleState": 0, 谷歌认证状态(0否，1是)

			"messIp": "127.0.0.1",

			"passDate": null,

			"phone": null,

			"phoneState": 0,手机认证状态(0否，1是)

			"states": 1,0 未实名 1 待审核 2 已实名 3 已拒绝

			"tokenId": null,

			"cardCurrency": null,

			"uncardCurrency": null,

			"company": null,

			"uuid": "fbba9af4-5d6b-415f-b3c7-a2cefc9c3741",

			"phone_googleState": 0

       			 },

		"info": { 实名认证信息

			"trueName": "啊",  名

			"country": "86", 国家编号

			"cardType": "1", 证件类型 0身份证1护照

			"cardId": "123132",证件号

			"surname": "啊",姓

			"papersType": "护照", 证件名称

			"type": "2"

        		},

		"isTibi": "1" 是否开启提币需要实名认证 0开1关

   		 },

	"code": "8888" 状态编码

}

请求参数加密顺序
	
String aValue =accesskey

2.5提交用户充值请求

exapi/api/user/rmbdeposit	提交用户充值请求

示例	//Request

surname:啊  充值人姓

remitter:啊 充值人名

bankCode:6222021604007927773 充值卡号

bankAmount:10000 冲值金额

bankName:招商银行 冲值银行

//Response

{

	"success": true,

	"msg": "",

	"obj": {

		"saasId": null,

		"created": "2018-01-23 14:03:47", 充值时间

		"modified": null,

		"id": null,

		"website": null,  站点类别默认cn

		"transactionNum": "011801231403474227959", 充值单号

		"userName": "1@1.cn",用户登录名

		"userId": null, 审核人Id  后台用户

		"customerId": 68,充值用户名

		"accountId": 65,账户ID

		"cardHolder": "啊",

		"transactionType": 3,交易类型(1线上充值,2线上提现 3线下充值 4线下取现 5支付宝充值)

		"transactionMoney": 10000,交易金额

		"fee": 20,手续费

		"status": 1,1待审核 2已完成 3以否决  4表示等待成交

		"ourAccountNumber": "123456789",我方银行卡号     

		"custromerAccountNumber": "6222021604007927773", 用户卡号

		"currencyType": null,交易的币类型

		"surname": "啊", 用户姓

		"trueName": "啊",用户名

		"bankNum": "招商银行",银行名称

		"bankName": "zhongguonongyeyinxing",银行拼音

		"bankProvince": null, 开户省份

		"bankAddress": "北京支行",开户行所在地  开户市

		"subBank": null,开户支行的银行机构代码

		"readyStates": null,后台处理后的修改的状态 (表示后台申请了之后  需要第三方回调的方法。)

		"thirdPayName": null, 第三方支付的名字

		"remark": "9891", 备注

		"rejectionReason": null, 驳回理由

		"accountName": "北京瓦力", 我方名称

		"accountNumber": "123456789",我方帐号

		"created_long": 1516687427430,联系电话

		"style": 0

		},

	"code": "8888"

}

请求参数加密顺序	String aValue =surname+remitter+bankCode+bankAmount+bankName

2.6获取用户的提现地址

exapi/api/user/getWithdrawAddress	获取用户的提现地址

示例	//Request

Accesskey： 68

sign1：25725b4ecb8274578e7e907d995cd79c

//Response

{

	"success": true,

	"msg": "",

	"obj": 
	[{

		"saasId": "hurong_system",

		"created": "2018-01-20 13:07:18",

		"modified": "2018-01-20 13:07:18",

		"id": 8,

		"accountId": 65, 账户ID

		"customerId": 68, 用户id

		"userName": "1@1.cn", 用户名

		"trueName": "", 名

		"surName": "null", 姓

		"currencyType": null, 货币类型

		"cardName": "", 银行卡持有人

		"cardNumber": "23", 银行卡号

		"cardBank": "中国银行",  开户银行

		"bankAddress": "藁城市",  开户行所在地  开户市

		"subBank": "23",  开户支行

		"subBankNum": "23",  开户支行银行机构代码
 
		"website": "",  站点类别默认cn

		"bankProvince": "河北省",  开户省份

		"signBank": null   签约银行通道

        }],

	"code": "8888"

}

请求参数加密顺序	String aValue =accesskey

2.7获取数字资产提现充值记录

exapi/api/user/findcoinInfo

	获取数字资产提现充值记录

示例	//Request

accesskey：68 

sign1：0e6035649cc82664407555de2bda1f46

"key":"accesskey","value":"68" 供钥

"key":"limit","value":"10" 显示的条数

"key":"offset","value":"0" 从第几条开始显示

"key":"sortOrder","value":"asc" 显示的顺序

type：1 （1为充币记录，2 为提币记录）

//Response

{

	"success": true,

	"msg": "",

	"obj": {

		"page": 1, 页数

		"pageSize": 10, 显示的条数

		"totalPage": 1, 总页数

		"recordsTotal": 1, 总条数

		"recordsFiltered": 1,

		"rows": [

           		 {

			"saasId": null,

			"created": "2018-01-23 15:01:57",

			"modified": null,

			"id": null,

			"transactionMoney": 1, 交易金额

			"transactionNum": "021801231501577184193", 交易订单号

			"fee": 0, 手续费

			"status": 1, 状态 1待审核 --2已完成 -- 3以否决

			"customerId": null, 用户id

			"customerName": null,

			"trueName": null,

			"accountId": null, 数字货币账户id

			"transactionType": null, 交易类型(1充币 ，2提币)

			"userId": null, 操作人id

			"currencyType": null,

			"coinCode": "BTC", 币的类型

			"website": null,  站点类别 en ,cn

			"created_long": 1516690917000,

			"remark": "",

			"rejectionReason": null, 驳回原因

			"inAddress": null,

			"outAddress": null,

			"confirmations": null,

			"blocktime": null,

			"time": null,

			"timereceived": null,

			"ourAccountNumber": null,

			"orderNo": null

           		 }

        		],

		"total": 1

   		 },

	"code": "8888"

}

请求参数加密顺序	String aValue =limit+offset+sortOrder+type

2.8提现数字资产

/exapi/api/user/withdraw	提现数字资产

示例

//Request

accesskey：68 

sign1：7d9d0f43c936570af49eaef904eeb4b7

btcKey：123

coinType：BTC

btcNum：0.001

pacecurrecy：0

//Response

{

	"success": true,

	"msg": "申请提币成功",

	"obj": null,

	"code": "8888"

}

请求参数加密顺序	String aValue =btcKey+coinType+btcNum+pacecurrecy
