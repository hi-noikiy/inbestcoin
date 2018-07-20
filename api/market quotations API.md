# market quotations API （中文为解释说明）

接口	描述

/exapi/api/klinevtwo/message	行情,获取已开启的市场信息，包括价格、数量小数点位数

示例

//# Response

marketDetail:
	{,…
	},

productList:["BTC_LTC", "BTC_USDT", "LTC_USDT", "BTC_USD", "LTC_USD", "BCC_BTC", "ETH_BTC", "QTUM_USDT",…]

lastKLine{},

参数说明

marketDetail:市场细节

productList：产品清单

lastKLine:k线数据

marketDetail：

		{

		BCC_BTC具体产品:[
		
		｛
		
			idCur:1516340689 (时间戳)
			
			idPrev:0  (id前缀)
			
			msgType:"marketDetail0" (消息类型)
			
			payload:{...} (交易信息[单独说明见下一栏])
			
			symbolId:"BCC_BTC"( 交易对)
			
			version:1 ( 版本)
			
		 	_id:1516340689 (时间戳)
			
		 ｝
		 
	      ]}
	      
Payload 说明

amount:0 成交量

amp:null待定

asks:
	{
	
		price: 成交价格, 
		
		amount: 成交量,
		
		level: 待定
		
	}  委托卖

amount:null

level:null与最新成交价相等

price:null

bids:{price: 成交价格, amount: 成交量, level: 待定。。}  委托买

commissionRatio:0 

innerDisc:0

level:0

outerDisc:0

poor:0

priceAverage:0

priceHigh:0 最高价

priceLast:0

priceLow:0  最低价

priceNew:0 最新成交价

priceOpen:0 开盘价

symbolId:"btccny"

totalAmount:0  弃用

totalVolume:   弃用

trades:{price: 成交价格, amount: 成交量l, direction: 成交内盘外盘, time: 成交时间} 成交数据

turnVolume:0

turnoverRate:0

updownRatio:0

updownVolume:0

volumeRatio:0

yestdayPriceLast: priceLast

symbolId:"BCC_BTC"

version:1

_id:1516340689

1.1	根据交易对获取信息(7b)

/exapi/api/klinevtwo/data	根据交易对获取信息

Post请求参数	coinCode：BTC_CNY

coinCode ：｛

idCur:1516340689 (时间戳)

idPrev:0  (id前缀)

msgType:"marketDetail0" (消息类型)

payload:{

amount:0 成交量

amp:null待定。。

asks:{price: 成交价格, amount: 成交量, level: 待定}  委托卖

amount:null

level:null与最新成交价相等

price:null

bids:{price: 成交价格, amount: 成交量, level: 待定。。}  委托买

commissionRatio:0 

innerDisc:0

level:0

outerDisc:0

poor:0

priceAverage:0

priceHigh:0 最高价

priceLast:0

priceLow:0  最低价

priceNew:0 最新成交价

priceOpen:0 开盘价

symbolId:"btccny"

totalAmount:0  弃用

totalVolume:   弃用

trades:{price: 成交价格, amount: 成交量l, direction: 成交内盘外盘, time: 成交时间} 成交数据

turnVolume:0

turnoverRate:0

updownRatio:0

updownVolume:0

volumeRatio:0

yestdayPriceLast: priceLast

symbolId:"BCC_BTC"

version:1

_id:1516340689

} 

symbolId:"BCC_BTC"( 交易对)

version:1 ( 版本)

_id:1516340689 (时间戳)

｝

]}
