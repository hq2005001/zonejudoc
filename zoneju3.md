# 众聚商城接口文档
> 请求的主链接：api.zoneju3.com

> 说明：对于下面的所有接口来说，都有几个公有的参数，*field*(要取得的字段),*sort*(排序规则),*page*(第几页),*row*(每页显示几条).

[TOC]

## 用户登录后相关

### 用户购物车接口
* 请求方法： get
* 参数： 无
* 请求地址：member/shopcaret.json
* 返回结果：
```javascript

```

### 用户晒单 
* 请求方法： get
* 参数： 
	+ type: 商品地址类型
* 请求地址：member/share.json
* 返回结果：
```javascript

```

### 用户地址接口
* 请求方法： get
* 参数： 
	+ type: 商品地址类型
* 请求地址：member/address.json
* 返回结果：
```javascript

```

### 用户心愿接口
* 请求方法： get
* 参数： 
	+ state: 心愿状态 【非必须参数】
* 请求地址：member/wish.json
* 返回结果：
```javascript

```



### 用户

## 首页相关

## 文章相关
### 根据文章ID得到文章内容
* 请求方法： get
* 参数：
	+ id : 文章ID
* 请求地址 ：article.json
* 返回结果：
```javascript
{
	errno: [
		0
	],
	data: {
		_id: "0z5obq2darwt",
		name: "关于我们",
		title: "关于我们",
		descr: "this is a test",
		category_id: "0z5n6zl0z937",
		category_name: "帮助文档",
		recommend: 0,
		comment: 0,
		read: 0,
		utime: 1479092966,
		itime: 1479092966
	}
}
```

### 根据文章分类id得到文章列表
* 请求方法： get
* 参数：
	+ acid : 文章分类ID
* 请求地址 ：article/list.json
* 返回结果：
```javascript
{
	errno: [
	0
	],
	data: {
		count: 1,
		page: 1,
		data: [
			{
				_id: "0z5obq2darwt",
				name: "关于我们",
				title: "关于我们",
				descr: "this is a test",
				category_id: "0z5n6zl0z937",
				category_name: "帮助文档",
				recommend: 0,
				comment: 0,
				read: 0,
				utime: 1479092966,
				itime: 1479092966
			}
		]
	}
}

```



### 文章分类列表
* 请求方法： get
* 参数： 
	+ name: 文章拼音名
* 请求地址 ：article_category.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: [
		{
			_id: "0z5n6zl0z937",
			name: "帮助文档",
			pinyin: "help",
			position: 1,
			tags: [
				"帮助"
			],
			pathsid: [
				"0z5n6zl0z937"
			],
			pathsname: [
				"帮助文档"
			],
			level: 1,
			utime: 1479091499,
			itime: 1479091499
		}
	]
}
```

## 广告相关
### 按类型取推荐商品列表
* 请求方法： get
* 参数： 
	+ type: 推荐分类
* 请求地址 goods_recom.json
* 返回结果：
```json
{
	errno: [
	0
	],
	data: {
		count: 1,
		page: 1,
		data: [
			{
				_id: "0z62y46l81kd",
				type: "0yalv79i2ep9",
				goods_id: "0ya8id4i2v93",
				category_id: "0yalv79i2ep9",
				position: 0,
				utime: 1479111916,
				itime: 1479111916,
				goods_store_id: "0y8div2tskn9",
				goods_name: "测试商品",
				goods_caption: "测试标题",
				goods_picture: "111111111111111",
				goods_price_orig: 200,
				goods_price_sale: 230,
				goods_price_min: 210,
				goods_price_max: 500,
				goods_category_ids: [
					"0yalv79i2ep9"
				],
				goods_category_name: "111",
				goods_store_name: "111"
			}
		]
	}
}
```

### 取得按组生成的分类
* 请求方法： get
* 参数： 无
* 请求地址 category.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: [
	{
		_id: "0z06kc4390eh",
		name: "手机数码",
		pinyin: "electric",
		position: 1,
		tags: [
		"手机",
		"数码"
		],
		pathsid: [
		"0z06kc4390eh"
		],
		pathsname: [
		"手机数码"
		],
		level: 1,
		utime: 1478836668,
		itime: 1478836668,
		children: [
			{
				_id: "0z0d1kkg4142",
				pid: "0z06kc4390eh",
				name: "手机通讯",
				pinyin: "phone",
				position: 1,
				tags: [],
				pathsid: [],
				pathsname: [],
				level: 2,
				utime: 1478845064,
				itime: 1478845064,
				children: [
					{
						_id: "0z0djrk5wpav",
						pid: "0z0d1kkg4142",
						name: "iphone",
						pinyin: "iphone",
						position: 1,
						tags: [],
						pathsid: [],
						pathsname: [],
						level: 3,
						utime: 1478845719,
						itime: 1478845719,
						children: [ ]
					},
				]
			}
		]
	}
	]
}
```


### 取得文章评论
* 请求方法： get
* 参数： 
	+ id: 评论的文章ID或者评论ID
* 请求地址 comment.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		count: 1,
		page: 1,
		data: [
			{
			_id: "0z669jhcfu9y",
			for: "0z64n080pqtg",
			member_id: "1111",
			content: "测试",
			is_reply: 0,
			utime: 1479116215,
			itime: 1479116215
			}
		]
	}
}

```

### 取得商品详情
* 请求方法： get
* 参数： 
	+ gid: 商品ID
* 请求地址 goods.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		_id: "0ya8id4i2v93",
		category_id: "0yalv79i2ep9",
		store_id: "0y8div2tskn9",
		name: "测试商品",
		caption: "测试标题",
		picture: "111111111111111",
		price_orig: 200,
		price_sale: 230,
		price_min: 210,
		price_max: 500,
		post_type: "1",
		category_ids: [
			"0yalv79i2ep9"
		],
		category_name: "111",
		category_pinyin: "111",
		store_name: "111",
		status: 1,
		utime: 1477626133,
		itime: 1477626133,
		detail: false,
		specification: {
			color: [
				{
					_id: "0yaqsdhdhq91",
					value: "红",
					name: "颜色",
					english: "color"
				}
			],
			size: [
				{
					_id: "0yaqsdhdo3bm",
					value: "xl",
					name: "大小",
					english: "size"
				}
			]
		}
	}
}
```

### 根据商品ID得到详情数据
* 请求方法： get
* 参数： 
	+ gid: 商品ID
* 请求地址 goods.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
	_id: "0z68us050o56",
	goods_id: "0ya8id4i2v93",
	declare: "1111111111111111111111111111",
	param: "产品名称：Apple/苹果 iPhone 6s Plus CPU型号: 其他 Apple型号: iPhone 6s Plus 机身颜色: 玫瑰金色 深空灰色 金色 银色 运行内存RAM: 不详 机身内存: 16GB 64GB 128GB 网络模式: 无需合约版 电池容量: 2750mAh",
	detail: [
		"/static/upload/images/goodsdetail/56dd48b243214.png",
		"/static/upload/images/goodsdetail/56dd2e7c634a7.png",
		"/static/upload/images/goodsdetail/56dd2e7f7a3f6.png",
		"/static/upload/images/goodsdetail/56dd2e82b7be0.png",
		"/static/upload/images/goodsdetail/56dd2e85f0593.png",
		"/static/upload/images/goodsdetail/56fa49d82834a.png"
	],
	utime: 1479119572,
	itime: 1479119572
	}
}
```

### 根据广告类型取出广告数据
* 请求方法： get
* 参数： 
	+ type: 广告类型
* 请求地址 recom.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		count: 1,
		page: 1,
		data: [
			{
				_id: "0z6b3w0zsqpx",
				type: "main_category",
				title: "广告标题",
				content: "广告内容",
				picture: "/static/upload/images/goodsdetail/56fa49d82834a.png",
				link: "http://www.baidu.com",
				position: 0,
				utime: 1479122492,
				itime: 1479122492
			}
		]
	}
}
```

### 根据晒单类型得到晒单数据
* 请求方法： get
* 参数： 
	+ type: 晒单类型 [goods, wish]
* 请求地址 share.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		count: 1,
		page: 1,
		data: [
			{
				_id: "0z6cdd4myj9f",
				descrinfo: "晒单内容",
				picture: "/static/upload/images/goodsdetail/56fa49d82834a.png",
				status: 0,
				type: "goods",
				favourite: 0,
				utime: 1479124129,
				itime: 1479124129
			}
		]
	}
}
```

### 得到心愿列表
* 请求方法： get
* 参数： 
	+ state : 心愿状态 【0为添加心愿成功，1审核通过，2为积够人数，等待上架 3为上架，默认为添加心愿成功 -1表示过期】
* 请求地址 wish.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		count: 1,
		page: 1,
		data: [
			{
				_id: "0z6czee5ycfq",
				goods_name: "我的心愿",
				picture: [
					"/static/upload/images/goodsdetail/56fa49d82834a.png"
				],
				price: 500,
				link: "http://www.baidu.com",
				member_id: null,
				member_name: null,
				user_ids: [
					null
				],
				count: 1,
				state: 0,
				utime: 1479124922,
				itime: 1479124922
			}
		]
	}
}
```


### 通过ID得到夺宝商品信息
* 请求方法： get
* 参数： 
	+ id : 夺宝商品ID
	+ detail： 是否加载详情[非必须]
* 请求地址 goods_indiana.json
* 返回结果：
```json
{
	errno: [
	0
	],
	data: {
		_id: "0z7kpthqzl8r",
		name: "测试商品1",
		title: "我是标题",
		caption: "我是caption",
		category_id: "0z06kc4390eh",
		tags: [
			"手机",
			"iphone"
		],
		type: 1,
		price: 200,
		price_cost: 198,
		price_min: 1,
		phase: 1,
		state: 0,
		no: 1,
		release_time: 0,
		utime: 1479183305,
		itime: 1479181601,
		detail: {
		_id: "0z7kvvhde9t9",
		goods_id: "0z7kpthqzl8r",
		declare: "1111111111111111111111111111",
		param: "产品名称：Apple/苹果 iPhone 6s Plus CPU型号: 其他 Apple型号: iPhone 6s Plus 机身颜色: 玫瑰金色 深空灰色 金色 银色 运行内存RAM: 不详 机身内存: 16GB 64GB 128GB 网络模式: 无需合约版 电池容量: 2750mAh",
		detail: [
			"/static/upload/images/goodsdetail/56dd48b243214.png",
			"/static/upload/images/goodsdetail/56dd2e7c634a7.png",
			"/static/upload/images/goodsdetail/56dd2e7f7a3f6.png",
			"/static/upload/images/goodsdetail/56dd2e82b7be0.png",
			"/static/upload/images/goodsdetail/56dd2e85f0593.png",
			"/static/upload/images/goodsdetail/56fa49d82834a.png"
		],
		utime: 1479181819,
		itime: 1479181819
		}
	}
}
```

### 通过ID得到夺宝商品信息
* 请求方法： get
* 参数： 
	+ key : 要取的配置文件键名[默认为ddic,可以不用填]
* 请求地址 config.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		exchange_scale: 100,
		advert_type: {
			expirence_banner: "发烧体验banner",
			main_banner: "首页banner",
			main_zone: "首页专区"
		},
		recom_type: {
			expirence: "评测推荐",
			main_hot: "首页热门推荐",
			main_recom: "首页精品推荐",
			indiana_recom: "首页夺宝推荐"
		}
	}
}
```

### 得到推荐的夺宝商品列表
* 请求方法： get
* 参数： 
	+ type : 推荐类型[indiana_recom]
* 请求地址 goods_recom/phase.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		count: 1,
		page: 1,
		data: [
			{
				_id: "0z7ukf8x62nr",
				type: "indiana_recom",
				goods_id: "0z7kpthqzl8r",
				position: 0,
				utime: 1479194367,
				itime: 1479194367,
				phase: [
					{
						_id: "0z7m15l9raf4",
						goods_id: "0z7kpthqzl8r",
						category_id: "0z06kc4390eh",
						goods_name: "测试商品1",
						goods_no: 1,
						price: 200,
						price_min: 1,
						price_will: 200,
						price_cost: 198,
						phase: 1,
						state: 1,
						price_yet: 0,
						time_genno: 0,
						time_pub: 0,
						is_last_phase: 1,
						padding: "00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
						utime: 1479183305,
						itime: 1479183305,
						goods_indiana_title: "我是标题",
						goods_indiana_caption: "我是caption",
						category_pinyin: "electric"
					}
				]
			}
		]
	}
}
```

### 得到期数据详情
* 请求方法： get
* 参数： 
	+ gid : 商品ID
	+ phase: 期数【可以不用填，不填默认为最新一期】
* 请求地址 phase.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		_id: "0z7m15l9raf4",
		goods_id: "0z7kpthqzl8r",
		category_id: "0z06kc4390eh",
		goods_name: "测试商品1",
		goods_no: 1,
		price: 200,
		price_min: 1,
		price_will: 200,
		price_cost: 198,
		phase: 1,
		state: 1,
		price_yet: 0,
		time_genno: 0,
		time_pub: 0,
		is_last_phase: 1,
		padding: "00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
		utime: 1479183305,
		itime: 1479183305,
		goods_title: "我是标题",
		goods_caption: "我是caption",
		goods_category_id: "0z06kc4390eh",
		goods_tags: [
			"手机",
			"iphone"
		],
		goods_type: 1,
		goods_price: 200,
		goods_price_cost: 198,
		goods_price_min: 1,
		goods_phase: 1,
		goods_state: 0,
		goods_release_time: 0,
		goods_utime: 1479183305,
		goods_itime: 1479181601
	}
}
```


## 登录相关
### 取QQ登录链接
* 请求方法： get
* 参数：无
* 请求地址 member/qq.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		status: "success",
		data: {
			qq_url: "http://i.snqu.com/api3/api3/qq/login.html?cid=0wshnr2vs3pb&s=db19e26bc8fb6a061479204952"
		}
	}
}
```

### 取微信登录链接
* 请求方法： get
* 参数：无
* 请求地址 member/wechat.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		status: "success",
		data: {
			wechat_url: "http://i.snqu.com/api3/api3/wechat/login.html?cid=0wshnr2vs3pb&s=361d52be529b45d21479205071"
		}
	}
}
```

### 取hmac值
* 请求方法： get
* 参数：
	+ username: 用户名
* 请求地址 member/hmac.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		key: "hmac0z82vccot9u3",
		username: "hq2005001"
	}
}
```

### 取用户信息
* 请求方法： get
* 参数：
	+ username/mobile/id: 用户名/手机号码/用户id
	+ fields	需要获取的字段	[可以不填]	 多个字段请用 " , " 隔开
* 请求地址 member/member.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		status: "success",
		data: {
			_id: "0nablzeflivw",
			username: "hq2005001",
			utime: 1479109791,
			itime: 1459154375,
			status: 1,
			nickname: "王的蔑视",
			mobile: "18888888888",
			loginnum: 903,
			lastlogin: 1479109791,
			prevlogin: 1479109791,
			loginip: "218.6.242.42",
			failnum: 0,
			lastfail: 1478845505,
			avatar: "/static/upload/avatar/57ff209e81028.jpg",
			sex: 1,
			age: 22,
			qqid: "BF6C62738E9593842430FA059D57DE4B",
			email: ""
		}
	}
}
```

### 修改用户信息
* 请求方法： put
* 参数：
	+ username	    用户名	是	用户名
	+ nickname   	昵称	 否	 用户昵称
	+ sex	        性别	 否   性别 1:男 2:女
	+ age	        年龄	 否	 年龄14-99
	+ reusername	用户名	否	修改后的用户名，utemp开头的用户允许修改
* 请求地址 member/member.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		status: "success",
		data: {
			_id: "0nablzeflivw",
			username: "hq2005001",
			utime: 1479209898,
			itime: 1459154375,
			status: 1,
			nickname: "我是王",
			mobile: "18888888888",
			loginnum: 903,
			lastlogin: 1479109791,
			prevlogin: 1479109791,
			loginip: "218.6.242.42",
			failnum: 0,
			lastfail: 1478845505,
			avatar: "/static/upload/avatar/57ff209e81028.jpg",
			sex: 1,
			age: 22,
			qqid: "BF6C62738E9593842430FA059D57DE4B",
			email: ""
		}
	}
}
```

### 注册新用户
* 请求方法： post
* 参数：
	+ 请求参数（用户名注册）
		- 参数名称	类型	是否必须	描述
		- username	用户名	是	用户名
		- password	密码	是	密码(不要md5加密)
	+ 请求参数（手机注册）
		- 参数名称	类型	是否必须	描述
		- mobile	手机	是	11位手机号码
		- password	密码	是	密码(不要md5加密)
		- captcha	短信验证码	是	验证码
	+ 请求参数（三方注册）
		- 参数名称      	类型	            是否必须	描述
		- qqid/wechatid	   openid/unionid	是	        QQ openid或 Wecaht unionid
		- qq_access_token/wechat_access_token	access_token	是	QQ或微信的 access_token
		- sex	性别	是	1：男2：女
		- avatar	头像	是	QQ或微信头像
		- nickname	昵称	是	QQ或微信昵称
* 请求地址 member/member.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		status: "success",
		data: {
			_id: "0z87ou8al6q7",
			username: "huangqiang2333",
			prevlogin: 1479211374,
			lastlogin: 1479211374,
			itime: 1479211374,
			utime: 1479211374,
			loginnum: 1,
			status: 1,
			nickname: "huangqiang2333",
			failnum: 0,
			loginip: "218.6.242.42"
		}
	}
}
```

### 获得验证码
* 请求方法： post
* 参数：
	+ mobile 手机号
* 请求地址 member/smscaptcha.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		status: "success",
		msg: "验证码发送成功",
		data: {
			captcha: "988244"
		}
	}
}
```


### 修改用户信息
* 请求方法： post
* 参数：
	- 参数名称	类型	是否必须	描述
	- mobile	手机	是	11位手机号
	- username	用户名	是	需要绑定的用户名
	- captcha	短信验证码	是	短信验证码6位
	- password	密码	加密后的密码 md5($hmac . md5($username . $password))
	- hmackey	hmac	是	之前获取到的Hmac
* 请求地址 member/mobile.json
* 返回结果：
```json
{
	errno: [
		0
	],
	data: {
		status: "success",
		data: {
			_id: "0z87rak8cie2",
			username: "huangqiang2311",
			prevlogin: 1479211462,
			lastlogin: 1479211462,
			itime: 1479211462,
			utime: 1479211462,
			loginnum: 1,
			status: 1,
			nickname: "huangqiang2311",
			failnum: 0,
			loginip: "218.6.242.42",
			mobile: "17308017603"
		}
	}
}
```

### 重置密码
* 请求方法： post
* 参数：
	- 参数名称	类型	是否必须	描述
	- password	密码	是	新密码
	- mobile	手机	是	帐号绑定的手机
	- captcha	验证码	是	短信验证码
* 请求地址 member/password.json
* 返回结果：
```json

```

