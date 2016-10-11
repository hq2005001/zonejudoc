众聚app Api
***************
>说明：所有的api链接的主域名都为http://api.1.zhonju.cn,每个接口返回值都有三个参数，
    一个data,一个msg，一个status,status如果大于0说明请求成功，反之请求失败,
    如果返回值中包含count字段，表示这个接口接受page,row实现翻页功能,
    每个接口还接受一个field接收只取部分的字段的操作

目录
[TOC]

### 首页背景图
* 链接: advert.json
* 参数：
    * position => index
* 请求方式: get
* 返回值：
```json
    {
        data: [
            {
                _id: "0tykf59uil1b",
                position: "index",
                picture: "/static/upload/images/57fb0a562a4bc.png",
                link: "http://www.baidu.com",
                title: "111",
                content: "111",
                itime: 1470363233,
                utime: 1476080705,
                pos: 0,
                app: "myapp://0tykf59uil1b" //app跳转指令
            }
        ],
        msg: "",
        status: 1
    }
```

### 累计参与人数
* 链接: ordercount.json
* 参数：无
* 请求方式: get
* 返回值：
```json
{
    data: {
        count: "34886"
    },
    msg: "",
    status: 1
}
```

### 最新参与
* 链接: orderlist.json
* 参数：无
* 请求方式: get
* 返回值：
```json
{
    data: [
    {
        _id: "0wurqql5djus",
        goods_id: "0oy1ui33pg87",
        price_join: 2,
        itime: 1475224946,
        utime: 1475224975,
        member_id: "0nablzeflivw",
        member_name: "王的蔑视",
        goods_name: "无限烈焰 黛安娜",
        category_id: "0f5qnd1p4jic",
        assortments_id: [],
        ip_join: "127.0.0.1",
        state: 1,
        phase_id: "0ti6yk3ooti8",
        split_order_id: 0,
        time_genno: 1475224975,
        juker_id: null,
        juker_cid: null,
        user_agent: "pc",
        time_pay: 1475224947,
        time_calc: 164227078,
        nos_join: [],
        phase_num: 48,
        goodsphase_picture: "/static/upload/images/5723733212add.png",
        goodsphase_price: 98,
        goodsphase_price_min: 2,
        goodsphase_price_will: 90,
        goodsphase_price_cost: 69,
        goodsphase_price_yet: 8,
        goodsphase_time_genno: 0,
        goodsphase_time_pub: 0,
        goods_type: 5,
        category_english: "virtual",
        category_pinyin: "chongzhi",
        member_avatar: "/static/upload/avatar/571772b6e713f.png",
        goods_price: 98,
        goods_pictures: []
    },
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {}
    ],
    msg: "",
    status: 1,
    count: 1000
}
```

### 专区接口
* 链接: config.json
* 参数：
    * name => 'app.prefecture'
* 请求方式: get
* 返回值：
```json
{
    data: [
        {
            name: "英雄联盟",
            pic: "http://1.zhonju.cn/public/img/bg.png",
            app: "myapp://lol",
            link: "http://1.zhonju.cn/lol"
        },
        {
            name: "苹果专区",
            pic: "http://1.zhonju.cn/public/img/bg.png",
            app: "myapp://apple",
            link: "http://1.zhonju.cn/apple"
        },
        {
            name: "守望先峰",
            pic: "http://1.zhonju.cn/public/img/bg.png",
            app: "myapp://ow",
            link: "http://1.zhonju.cn/ow"
        }
    ],
    msg: "",
    status: 1
}
```

### 即将满员
* 链接: soon.json
* 参数：无
* 请求方式: get
* 返回值：
```json
{
    data: [
    {
        _id: "0o2d3ee026p1",
        goods_id: "0ldtpajmwqy4",
        utime: 1473770507,
        itime: 1460462666,
        category_id: "0k8q0l23vfzy",
        goods_name: "华硕A555LF5200",
        goods_no: 76,
        picture: "/static/upload/images/56d0014681880.png",
        price: 5388,
        price_min: 2,
        price_will: 1,
        price_cost: 4099,
        phase: 3,
        state: 1,
        price_yet: 5387,
        time_genno: 0,
        time_pub: 0,
        is_last_phase: 1,
        category_name: "潮流电脑",
        category_english: "computer",
        category_pinyin: "diannao",
        goods_title: "可根据自己喜好选择对于型号配置",
        goods_supplier_name: "盛趣网络科技有限公司",
        goods_caption: "华硕（ASUS）A555LF5200 15.6英寸笔记本电脑 新酷睿I5 930M 黑色1TB",
        goods_price_min: 2,
        goods_pictures: [
            "/static/upload/images/56d0014681880.png",
            "/static/upload/images/56d7dd1cd9bd3.png",
            "/static/upload/images/56d7dd22e2a01.png",
            "/static/upload/images/56d7dd278ca79.png"
        ],
        goods_type: 3
    },
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {}
    ],
    msg: "",
    status: 1,
    count: 603
}
```

### 分类商品
* 链接: floor.json
* 参数：无
* 请求方式: get
* 返回值：
```json
{
    data: [
    {
        _id: "0fvao95yizwh",
        name: "品牌手机",
        english: "phone",
        pinyin: "shouji",
        utime: 1456294819,
        itime: 1446696009,
        picture: "/static/upload/images/56cd4ba28904f.png",
        position: 6,
        advert: {
            _id: "0uu4qc7qrdrg",
            position: "category",
            category: "0fvao95yizwh",
            picture: "/static/upload/images/57ba6ef2af8f7.jpg",
            link: "qqq",
            title: "qqq",
            content: "qqq",
            itime: 1471835892,
            utime: 1471838491,
            pos: 0
        },
        goods: [
            {
                _id: "0np3px4ke29f",
                goods_id: "0np2c4ixtkjo",
                type: "0fvao95yizwh",
                position: 0,
                utime: 1470299834,
                itime: 1459843989,
                category_id: "0fvao95yizwh",
                goods_name: "iPhone SE 16G",
                goods_no: 143,
                picture: "/static/upload/images/5703738450f6a.png",
                price: 4278,
                price_min: 2,
                price_will: 58,
                price_cost: 3288,
                phase: 1,
                state: 1,
                price_yet: 4220,
                time_genno: 0,
                time_pub: 0,
                is_last_phase: 1,
                goods_caption: "Apple/苹果 iPhone SE 16G",
                goods_title: "正品行货 全国联保",
                goods_pictures: [],
                goods_assortment_id: "0oxzlidnmd99",
                assortment_name: "apple",
                assortment_english: "apple",
                category_english: "phone",
                goodsdetail_detail: []
            },
            {},
            {},
            {}
        ]
    },
    {},
    {},
    {},
    {},
    {}
    ],
    msg: "",
    status: 1
}
```


### 红包接口（需要登录）
* 链接: bonus.json
* 参数：
    * all => 是否取全部红包
    * status => 要与all配合使用
        * 3 -> 过期红包
        * 1 -> 未使用红包
        * 2 -> 已使用红包
    * money => 取指定money以下的红包
* 请求方式: get
* 返回值：
```json
{
    data: [
        {
            _id: "0vkf7xcf0sp8",
            type: "register",
            price: 1,
            price_cost: 10,
            expire_time: 1483401600,
            member_id: "0nablzeflivw",
            status: 1,
            itime: 1473062541,
            utime: 1473062541
        },
        {},
        {},
        {},
        {},
        {},
        {},
        {},
        {},
        {}
    ],
    msg: "",
    status: 1,
    count: 37
}
```

### 用户成功支付订单列表
* 链接: orderedlist.json
* 参数：
    * mid => 用户ID
* 请求方式: get
* 返回值：
```json
{
    data: [
        {
            _id: "0wuub3jfd5pu",
            member_id: "0nablzeflivw",
            member_name: "王的蔑视",
            phase_id: "0ti6yk3ooti8",
            phase_num: 48,
            goods_id: "0oy1ui33pg87",
            goods_name: "无限烈焰 黛安娜",
            category_id: "0f5qnd1p4jic",
            assortments_id: [
                "0ooo8a1e1uuy",
                "0ooogihb1o6b"
            ],
            price_join: 8,
            nos_join: [
            72,
            73,
            70,
            71,
            62,
            63,
            91,
            92
            ],
            time_pay: 1475224947,
            time_genno: 1475224975,
            state: 1,
            addr_id: null,
            post_info: null,
            order_ids: [
                "0wurlh5xf5sb",
                "0wurn6k1wjz5",
                "0wurpj95ib5w",
                "0wurqql5djus"
            ],
            itime: 1475228271,
            utime: 1475228542,
            goodsphase_picture: "/static/upload/images/5723733212add.png",
            goodsphase_price: 98,
            goodsphase_price_min: 2,
            goodsphase_price_will: 90,
            goodsphase_price_cost: 69,
            goodsphase_price_yet: 8,
            goodsphase_time_genno: 0,
            goodsphase_time_pub: 0,
            goods_type: 5,
            category_english: "virtual",
            category_pinyin: "chongzhi",
            member_avatar: "/static/upload/avatar/571772b6e713f.png",
            goods_price: 98,
            goods_pictures: []
        },
        {},
        {},
        {},
        {},
        {},
        {},
        {},
        {},
        {}
    ],
    msg: "",
    status: 1,
    count: 95
}
```