����API	  

����ͨ���ӿڿ��ٽ��н���

2.1ί���µ�

�ӿ�	����

exapi/api/trade/order	ί���µ�

ʾ��

//# Request

entrustPrice:1 �۸�

type:1 ��

coinCode:BTC_LTC

entrustCount:1 ����

entrustWay:1

accesskey:68 Kֵ

Sign1��d5b6c24d00b571c298b32efca4775647

---------------------------------------------------

entrustPrice:2 �۸�

type:2  ��

coinCode:BTC_LTC

entrustCount:2 ����

entrustWay:1 

accesskey:��Կ 68

Sign1��hlsafc24d00b5214296dbs2efca477ada

//# Response

{"success":true,"msg":"ί�гɹ�","obj":null,"code":""}

�����������˳��	String aValue =entrustPrice+type+coinCode+entrustCount

2.2ȡ��ȫ��ί��

exapi/api/trade/cancelOrder	ȡ��ȫ��ί��

ʾ��

//# Request

acoinCode =BTC_LTC

accesskey=key  ��Կ

//# Response

{"success":true,"

msg":"�����ɹ�",

"obj":null,"code":""}

����ֵ˵��	Success��״̬

Message����ʾ��Ϣ

����˵��

coinCode: �ҵĴ���

Accesskey����Կ

�����������˳��
	
String aValue =acoinCode

2.3��ȡ�ҵ�ί��

exapi/api/user/singleExEntrust	��ȡ�ҵ�ί��

ʾ��

//# Request

"key":"accesskey","value":"68" ��Կ

"key":"limit","value":"10" ��ʾ������

"key":"offset","value":"0" �ӵڼ�����ʼ��ʾ

"key":"sortOrder","value":"asc" ��ʾ��˳��

"key":"querypath","value":"current" ��ѯ���ݵ�����

"key":"sign1","value":"03d674d39203432cb2af8a61e3a12fb

//# Response

{

"success": true,

"msg": "",

"obj": {

"page": 1, ҳ��

"pageSize": 10, ��ʾ������

"totalPage": 1, ��ҳ��

"recordsTotal": 1, ������

"recordsFiltered": 1,

"rows": [

{

"entrustNum": "180122165729001585", ����

"entrustTime": "2018-01-22 16:57:30", ʱ��

"entrustTime_long": null,

"source": 1, ��Դ 1Ϊpc 8Ϊaip

"entrustPrice": 1,ί�м۸�

"entrustCount": 1,ί������

"type": 1,�������� 1Ϊ��2Ϊ��

"surplusEntrustCount": 1, Ϊ�ɽ�����

"status": 0,

"transactionSum": 0, �����ܽ��

"entrustSum": 1,ί������

"processedPrice": null,

"coinCode": "BTC", ���ױ�

"fixPriceCoinCode": "LTC", ���۱�

"coin": null

            }

        ],

"total": 1

    },

"code": "8888"

}

����ֵ˵��	Success��״̬

Message����ʾ��Ϣ

����˵��	����

�����������˳��	

String aValue =limit+offset+sortOrder+querypath

2.4��ȡ�û���Ϣ

exapi/api/user/getAccountInfo	��ȡ�û���Ϣ

ʵ��

//# Request

Accesskey ��68 ��Կ

sign1��5b4ecb8274578e7e sign

//# Response

{

"success": true, ����״̬

"msg": "", ������Ϣ

"obj": {

"isChongbi": "1", �Ƿ��������Ҫʵ����֤ 0 �� 1��

"coinAccount": [

            {

"id": null,

"coinCode": "USD", �Ҵ���

"hotMoney": 123123123, �����ܶ�

"coldMoney": 0,�����ܶ�

"picturePath": null,

"name": "USD",�ҵ�����

"currencyType": "USD",�ҵ�����

"accountNum": "8800020008006081",�����˺�

"tokenId": "fbba9af4-5d6b-415f-b3c7-a2cefc9c3741", Ϊ�ֻ���ʹ��

"languageCode": null,

"keepDecimalForCoin": null,

"moneyAndCoin": 0 0Ϊ����1Ϊ�������

            },

            {

"id": 534,

"coinCode": "BCC",

"hotMoney": 0,

"coldMoney": 0,

"picturePath": "hryfile/6/b/d8f068e828754a18be3c5516908e1f21.png",

"name": "���ر��ֽ�",

"currencyType": null,

"accountNum": null,

"tokenId": "fbba9af4-5d6b-415f-b3c7-a2cefc9c3741",

"languageCode": null,

"keepDecimalForCoin": 10,

"moneyAndCoin": 1

            },

        ],

"isTrade": "1",�Ƿ���������Ҫʵ����֤ 0�� 1��

"witfee": 0.5,������������

"maxWithdrawMoneyOneTime": "20000",һ���������

"languageCode": "USD",���۱�

"maxWithdrawMoney": "20000",һ���������

"user": {

"saasId": "hurong_system",

"created": null,

"modified": null,

"username": "1@1.cn"���û���

"password": "54a51aceddcd5cae153a6ae4124e28f5",

"userCode": "a8b6548e24fd4172b9fb40186b201d7f",Ψһ��ʶ

"isReal": 1,�Ƿ�ʵ��0û��ʵ����1ʵ��

"isChange": 0,�Ƿ��ܽ���  0���Խ���  1���ܽ���

"isDelete": 0,�Ƿ����  0û�н��� 1����

"isLock": 0,�Ƿ�����   0û����  1����

"accountPassWord": "",��������

"customerId": 68,

"mobile": "1@1.cn",�û�����

"truename": "��",��ʵ��

"surname": "��",��ʵ��

"customerType": 1,�ͻ�����

"salt": "32bcb9a877421ac3f7b9d1b81de700c4",

"cardcode": "123132",���֤

"email": null,

"sex": null,

"postalAddress": null,��ϸ��ַ

"googleKey": null,

"googleState": 0, �ȸ���֤״̬(0��1��)

"messIp": "127.0.0.1",

"passDate": null,

"phone": null,

"phoneState": 0,�ֻ���֤״̬(0��1��)

"states": 1,0 δʵ�� 1 ����� 2 ��ʵ�� 3 �Ѿܾ�

"tokenId": null,

"cardCurrency": null,

"uncardCurrency": null,

"company": null,

"uuid": "fbba9af4-5d6b-415f-b3c7-a2cefc9c3741",

"phone_googleState": 0

        },

"info": { ʵ����֤��Ϣ

"trueName": "��",  ��

"country": "86", ���ұ��

"cardType": "1", ֤������ 0���֤1����

"cardId": "123132",֤����

"surname": "��",��

"papersType": "����", ֤������

"type": "2"

        },

"isTibi": "1" �Ƿ��������Ҫʵ����֤ 0��1��

    },

"code": "8888" ״̬����

}

�����������˳��
	
String aValue =accesskey

2.5�ύ�û���ֵ����

exapi/api/user/rmbdeposit	�ύ�û���ֵ����

ʾ��	//Request

surname:��  ��ֵ����

remitter:�� ��ֵ����

bankCode:6222021604007927773 ��ֵ����

bankAmount:10000 ��ֵ���

bankName:�������� ��ֵ����

//Response

{

"success": true,

"msg": "",

"obj": {

"saasId": null,

"created": "2018-01-23 14:03:47", ��ֵʱ��

"modified": null,

"id": null,

"website": null,  վ�����Ĭ��cn

"transactionNum": "011801231403474227959", ��ֵ����

"userName": "1@1.cn",�û���¼��

"userId": null, �����Id  ��̨�û�

"customerId": 68,��ֵ�û���

"accountId": 65,�˻�ID

"cardHolder": "��",

"transactionType": 3,��������(1���ϳ�ֵ,2�������� 3���³�ֵ 4����ȡ�� 5֧������ֵ)

"transactionMoney": 10000,���׽��

"fee": 20,������

"status": 1,1����� 2����� 3�Է��  4��ʾ�ȴ��ɽ�

"ourAccountNumber": "123456789",�ҷ����п���     

"custromerAccountNumber": "6222021604007927773", �û�����

"currencyType": null,���׵ı�����

"surname": "��", �û���

"trueName": "��",�û���

"bankNum": "��������",��������

"bankName": "zhongguonongyeyinxing",����ƴ��

"bankProvince": null, ����ʡ��

"bankAddress": "����֧��",���������ڵ�  ������

"subBank": null,����֧�е����л�������

"readyStates": null,��̨�������޸ĵ�״̬ (��ʾ��̨������֮��  ��Ҫ�������ص��ķ�����)

"thirdPayName": null, ������֧��������

"remark": "9891", ��ע

"rejectionReason": null, ��������

"accountName": "��������", �ҷ�����

"accountNumber": "123456789",�ҷ��ʺ�

"created_long": 1516687427430,��ϵ�绰

"style": 0

    },

"code": "8888"

}

�����������˳��	String aValue =surname+remitter+bankCode+bankAmount+bankName

2.6��ȡ�û������ֵ�ַ

exapi/api/user/getWithdrawAddress	��ȡ�û������ֵ�ַ

ʾ��	//Request

Accesskey�� 68

sign1��25725b4ecb8274578e7e907d995cd79c

//Response

{

"success": true,

"msg": "",

"obj": [

        {

"saasId": "hurong_system",

"created": "2018-01-20 13:07:18",

"modified": "2018-01-20 13:07:18",

"id": 8,

"accountId": 65, �˻�ID

"customerId": 68, �û�id

"userName": "1@1.cn", �û���

"trueName": "", ��

"surName": "null", ��

"currencyType": null, ��������

"cardName": "", ���п�������

"cardNumber": "23", ���п���

"cardBank": "�й�����",  ��������

"bankAddress": "޻����",  ���������ڵ�  ������

"subBank": "23",  ����֧��

"subBankNum": "23",  ����֧�����л�������
 
"website": "",  վ�����Ĭ��cn

"bankProvince": "�ӱ�ʡ",  ����ʡ��

"signBank": null   ǩԼ����ͨ��

        }

    ],

"code": "8888"

}

�����������˳��	String aValue =accesskey

2.7��ȡ�����ʲ����ֳ�ֵ��¼

exapi/api/user/findcoinInfo

	��ȡ�����ʲ����ֳ�ֵ��¼

ʾ��	//Request

accesskey��68 

sign1��0e6035649cc82664407555de2bda1f46

"key":"accesskey","value":"68" ��Կ

"key":"limit","value":"10" ��ʾ������

"key":"offset","value":"0" �ӵڼ�����ʼ��ʾ

"key":"sortOrder","value":"asc" ��ʾ��˳��

type��1 ��1Ϊ��Ҽ�¼��2 Ϊ��Ҽ�¼��

//Response

{

"success": true,

"msg": "",

"obj": {

"page": 1, ҳ��

"pageSize": 10, ��ʾ������

"totalPage": 1, ��ҳ��

"recordsTotal": 1, ������

"recordsFiltered": 1,

"rows": [

            {

"saasId": null,

"created": "2018-01-23 15:01:57",

"modified": null,

"id": null,

"transactionMoney": 1, ���׽��

"transactionNum": "021801231501577184193", ���׶�����

"fee": 0, ������

"status": 1, ״̬ 1����� --2����� -- 3�Է��

"customerId": null, �û�id

"customerName": null,

"trueName": null,

"accountId": null, ���ֻ����˻�id

"transactionType": null, ��������(1��� ��2���)

"userId": null, ������id

"currencyType": null,

"coinCode": "BTC", �ҵ�����

"website": null,  վ����� en ,cn

"created_long": 1516690917000,

"remark": "",

"rejectionReason": null, ����ԭ��

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

�����������˳��	String aValue =limit+offset+sortOrder+type

2.8���������ʲ�

/exapi/api/user/withdraw	���������ʲ�

ʾ��

//Request

accesskey��68 

sign1��7d9d0f43c936570af49eaef904eeb4b7

btcKey��123

coinType��BTC

btcNum��0.001

pacecurrecy��0

//Response

{

"success": true,

"msg": "������ҳɹ�",

"obj": null,

"code": "8888"

}

�����������˳��	String aValue =btcKey+coinType+btcNum+pacecurrecy
