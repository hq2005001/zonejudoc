众聚app Api
***************
>说明：所有的api链接的主域名都为http://api.1.zhonju.cn,每个接口返回值都有三个参数，
    一个data,一个msg，一个status,status如果大于0说明请求成功，反之请求失败,
    如果返回值中包含count字段，表示这个接口接受page,row实现翻页功能,
    每个接口还接受一个field接收只取部分的字段的操作

目录
*****
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


********
## 详情接口

### 商品详情
* 链接: goods.json
* 参数：
    * id => 商品ID
* 请求方式: get
* 返回值：
```json
{
    data: {
        _id: "0oxrnx8ezgj8",
        name: "极地女神 艾希",
        release_time: 20100713,
        caption: "LOL极地女神 艾希",
        title: "等值兑换1000点券 全区全服通用",
        category_id: "0f5qnd1p4jic",
        assortment_id: "0ooogihb1o6b",
        type: 5,
        tags: [
            "lol",
            "皮肤",
            "极地女神",
            "ADC",
            "辅助",
            "推进",
            "寒冰射手",
            "艾希"
        ],
        price: 18,
        price_min: 2,
        price_cost: 10,
        video_link: "",
        iconpic: "/static/upload/images/0oxol5fi2ylh.jpg",
        pictures: [
            "/static/upload/images/0oxol5fnr9j7.png",
            "/static/upload/images/0oxol5fpm1jr.jpg",
            "/static/upload/images/0oxol5fued18.jpg"
        ],
        related_goods_id: "0ovbgxbld925",
        itime: 1461927885,
        utime: 1476181200,
        phase: 9,
        state: 1,
        no: 634,
        assortments_id: [
            "0ooo8a1e1uuy",
            "0ooogihb1o6b"
        ],
        category_english: "virtual",
        goodsdetail_detail: [
            "/static/upload/images/goodsdetail/0oxol5fjenq1.jpg"
        ],
        assortment_name: "皮肤",
        assortment_english: "pifu"
    },
    msg: "",
    status: 1
}
```

### 详情页猜你喜欢
* 链接: phaserecom.json
* 参数：
    * type => 分类ID，上面商品信息里面的category_id
* 请求方式: get
* 返回值：
```json
{
    data: [
        {
            _id: "0p9h346bdwl8",
            goods_id: "0mtjv1dnfrv3",
            type: "0f5qnd1p4jic",
            position: 9,
            itime: 1462473601,
            utime: 1470299964,
            category_id: "0f5qnd1p4jic",
            assortments_id: [
                "0ooo8a1e1uuy",
                "0ooogihb1o6b"
            ],
            goods_name: "三昧真火 孙悟空",
            goods_no: 112,
            picture: "/static/upload/images/56ecfd4c19de2.png",
            price: 108,
            price_min: 2,
            price_will: 41,
            price_cost: 79,
            phase: 50,
            state: 1,
            price_yet: 67,
            time_genno: 0,
            time_pub: 0,
            is_last_phase: 1,
            goods_caption: "LOL三昧真火 孙悟空",
            goods_title: "三昧真火 孙悟空 等值兑换7900点券 全区全服通用",
            goods_pictures: [
                "/static/upload/images/56ecfd4c19de2.png",
                "/static/upload/images/5720c8c4619b7.jpg",
                "/static/upload/images/5720c8cf29587.jpg"
            ],
            goods_assortment_id: "0ooogihb1o6b",
            goods_related_goods_id: "0ou6z4esdquu",
            assortment_name: "皮肤",
            assortment_english: "pifu",
            category_english: "virtual",
            goodsdetail_detail: [
                "/static/upload/images/goodsdetail/5720b6591cc4a.jpg",
                "/static/upload/images/goodsdetail/56fa333c74cf3.png"
            ]
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
    count: 10
}
```

### 期次列表
* 链接: phaselist.json
* 参数：
    * gid => 商品ID，上面商品信息里面的_id
    * isPub => 是否只要开了奖的，不传就表示把最新的一起取回来，要传的话传【1】
* 请求方式: get
* 返回值：
```json
{
    data: [
        {
            _id: "0xbepc3o468a",
            goods_id: "0oxrnx8ezgj8",
            itime: 1476001200,
            utime: 1476181800,
            category_id: "0f5qnd1p4jic",
            assortments_id: [
                "0ooo8a1e1uuy",
                "0ooogihb1o6b"
            ],
            goods_name: "极地女神 艾希",
            goods_no: 634,
            picture: "/static/upload/images/0oxol5fnr9j7.png",
            price: 18,
            price_min: 2,
            price_will: 0,
            price_cost: 10,
            pub_cutdown: 0,
            phase: 8,
            state: 2,
            price_yet: 18,
            time_genno: 1476181200,
            time_pub: 1476181850,
            is_last_phase: 0,
            next_phase_id: "0xf9lc5olal6",
            luck_order_id: "0xbepc3ir8hn",
            luck_member_id: "0vbjnvis66o6",
            luck_member_name: "hq2009020",
            luck_no: 9,
            luck_calc_order_ids: [
                "0xbepc3ir8hn",
                "0xbe8o3cpgqy",
                "0xbds03jrziy",
                "0xbdbc3p1te1",
                "0xbcuobem0uh",
                "0xbce05ipkwx",
                "0vd4mn70ct5r",
                "0vd4lz8xaxtv",
                "0vd4jcfshs5t",
                "0xbaxz9lgewl",
                "0xbart87hp1j",
                "0x8q0p2rb9lv",
                "0x1f1zdyz066",
                "0wqww17fg5ak",
                "0wqwr0fmk7gc",
                "0wqw8bbjap1f",
                "0wqvk40bd8a1",
                "0wqumk531sr1",
                "0wqudqdsdnbz",
                "0wqnl9gjjx5u",
                "0wqno99608y3",
                "0wqngti1smxn",
                "0wqmt3arqfxr",
                "0wqkvtd36rso",
                "0wqkc8k6wivz",
                "0wpg9mj4hgbn",
                "0wpau09sn38e",
                "0wp5mxkwyix5",
                "0wot9e293mm9",
                "0wot9dd4js7s",
                "0wosvqegtuc4",
                "0woqfq7tduyi",
                "0wnfsy2rurie",
                "0wnerb9fea5d",
                "0wner2790tau",
                "0wnd01hd2jj1",
                "0wncgp5cjbsc",
                "0wnclg99bkpz",
                "0wn9dahdigdg",
                "0wieggl377tc",
                "0widne0cpoyc",
                "0wib6sg79ovr",
                "0wi9r8alcbhh",
                "0wib78ax6mny",
                "0wiapkgac4hr",
                "0wi7qyivquzd",
                "0whypb8mrakk",
                "0whypb7veotv",
                "0wht2r0rfqxr",
                "0wht0498ry5u"
            ],
            luck_join_price: 8,
            category_name: "虚拟充值",
            category_english: "virtual",
            category_pinyin: "chongzhi",
            goods_caption: "LOL极地女神 艾希",
            goods_title: "等值兑换1000点券 全区全服通用",
            member_avatar: "http://test.zhonju.cn/public/img/avatar.png",
            order_price_join: 8,
            order_time_pay: 1475997600,
            order_nos_join: [
                9,
                10,
                11,
                12,
                13,
                14,
                15,
                16
            ],
            order_phase_num: 8,
            goods_type: 5,
            goods_price_min: 2,
            goods_pictures: [
            "/static/upload/images/0oxol5fnr9j7.png",
            "/static/upload/images/0oxol5fpm1jr.jpg",
            "/static/upload/images/0oxol5fued18.jpg"
            ]
        },
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
    count: 8
}
```

### 商品中奖晒单
* 链接: share.json
* 参数：
    * gid => 商品ID，上面商品信息里面的_id
    * comment => 是否带上评论，不传就表示把最新的一起取回来，要传的话传【1】
* 请求方式: get
* 返回值：
```json
{
    data: [
        {
            _id: "0p4pxj521b6q",
            phase_id: "0oy0is8484f5",
            descrinfo: "到账了~~~~~~~~~~~~~~~~~~~~~",
            picture: "/static/upload/share/572832bb5838e.jpg",
            itime: 1462252231,
            utime: 1462252231,
            member_id: "0p3vopjfxx92",
            member_name: "上帝淡退网络（魔法照接）",
            phase: 1,
            goods_id: "0oxrnx8ezgj8",
            goods_name: "极地女神 艾希",
            luck_order_id: "0p3vpg92kyvn",
            luck_no: 13,
            position: 0,
            status: 0,
            goodsphase_category_id: "0f5qnd1p4jic",
            goodsphase_picture: "/static/upload/images/0oxol5fnr9j7.png",
            goodsphase_price: 18,
            goodsphase_price_min: 1,
            goodsphase_time_pub: 1462222291,
            goodsphase_luck_order_id: "0p3vpg92kyvn",
            goodsphase_luck_join_price: 1,
            order_time_pay: 1462213383,
            category_english: "virtual",
            member_avatar: "http://q.qlogo.cn/qqapp/101300607/B386B250109B21CD12EECBD51CD0C808/100",
            comment_count: 0,
            comments: [ ],
            prize: 0
        }
    ],
    msg: "",
    status: 1,
    count: 1
}
```
### 正在购买的订单列表
* 链接: orderlist.json
* 参数：
    * 无
* 请求方式: get
* 返回值：
```json
{
    data: [
        {
            _id: "0xiu18851hx4",
            goods_id: "0oxrnx8ezgj8",
            price_join: 2,
            itime: 1476347660,
            utime: 1476348000,
            member_id: "0xisvbd5et3f",
            member_name: "HUZHY09",
            goods_name: "极地女神 艾希",
            category_id: "0f5qnd1p4jic",
            assortments_id: [
                "0ooo8a1e1uuy",
                "0ooogihb1o6b"
            ],
            ip_join: "218.6.242.42",
            state: 1,
            phase_id: "0xf9lc5olal6",
            split_order_id: 0,
            time_genno: 1476348000,
            juker_id: null,
            juker_cid: null,
            user_agent: "pc",
            time_pay: 1476347660,
            time_calc: 163420454,
            nos_join: [
                4,
                5
            ],
            phase_num: 9,
            goodsphase_picture: "/static/upload/images/0oxol5fnr9j7.png",
            goodsphase_price: 18,
            goodsphase_price_min: 2,
            goodsphase_price_will: 12,
            goodsphase_price_cost: 10,
            goodsphase_pub_cutdown: 0,
            goodsphase_price_yet: 6,
            goodsphase_time_genno: 0,
            goodsphase_time_pub: 0,
            goods_type: 5,
            category_english: "virtual",
            category_pinyin: "chongzhi",
            member_avatar: "http://1.zhonju.cn/public/img/avatar.png",
            goods_price: 18,
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
### 参与记录
* 链接: phaseorder.json
* 参数：
    * gid => 商品ID，上面商品信息里面的_id
    * phase => 期数
* 请求方式: get
* 返回值：
```json
{
    data: [
        {
            _id: "0p42rh5pzhcl",
            goods_id: "0oxrnx8ezgj8",
            price_join: 3,
            itime: 1462222205,
            utime: 1468986313,
            buyer_id: "0p40bs4wjq2z",
            buyer_name: "王子",
            user_id: [
                "0p40bs4wjq2z"
            ],
            type: 0,
            member_id: "0p40bs4wjq2z",
            member_name: "王子",
            goods_name: "极地女神 艾希",
            category_id: "0f5qnd1p4jic",
            assortments_id: [
                "0ooo8a1e1uuy",
                "0ooogihb1o6b"
            ],
            ip_join: "121.33.202.146",
            state: 5,
            phase_id: "0oy0is8484f5",
            split_order_id: 0,
            time_genno: 1462222241,
            juker_id: "0o1z48j3yo4l",
            juker_cid: 0,
            time_pay: 1462222240,
            time_calc: 45040824,
            nos_join: [
                16,
                17,
                18
            ],
            maxno_join: 18,
            phase_num: 1,
            is_phase_last: 1,
            addr_join: "广东省广州市",
            member_nickname: "王子",
            member_avatar: "http://q.qlogo.cn/qqapp/101300607/3E3E4653CC4CADB31205339CA57DA92F/100",
            member_mobile: "13247398306",
            category_english: "virtual"
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
    count: 15
}
```

### 最新一期信息
* 链接: phaselast.json
* 参数：
    * gid => 商品ID，上面商品信息里面的_id
* 请求方式: get
* 返回值：
```json
{
    data: {
        _id: "0xf9lc5olal6",
        goods_id: "0oxrnx8ezgj8",
        itime: 1476181200,
        utime: 1476348000,
        category_id: "0f5qnd1p4jic",
        assortments_id: [
            "0ooo8a1e1uuy",
            "0ooogihb1o6b"
        ],
        goods_name: "极地女神 艾希",
        goods_no: 634,
        picture: "/static/upload/images/0oxol5fnr9j7.png",
        price: 18,
        price_min: 2,
        price_will: 12,
        price_cost: 10,
        pub_cutdown: 0,
        phase: 9,
        state: 1,
        price_yet: 6,
        time_genno: 0,
        time_pub: 0,
        is_last_phase: 1,
        goods_caption: "LOL极地女神 艾希",
        goods_title: "等值兑换1000点券 全区全服通用",
        category_name: "虚拟充值",
        category_english: "virtual"
    },
    msg: "",
    status: 1
}
```

### 某一期用户购买信息(需要用户登录)
* 链接: memberordered.json
* 参数：
    * id => 期数ID
* 请求方式: get
* 返回值：
```json

```

### 计算详情
* 链接: phasecalc.json
* 参数：
    * phase_id => 期数ID
    * phase => 期数
* 请求方式: get
* 返回值：
```json
{
    data: {
        calc: [
            {
                _id: "0nuops5nfdgy",
                goods_id: "0ldn94k0f6yd",
                price_join: 1816,
                utime: 1468986320,
                itime: 1460104480,
                buyer_id: "0nacjz19f4yr",
                buyer_name: "我要中奖",
                type: 0,
                member_id: "0nacjz19f4yr",
                member_name: "我要中奖",
                goods_name: "iPhone 6s 64G",
                category_id: "0fvao95yizwh",
                ip_join: "180.173.182.208",
                state: 5,
                phase_id: "0na9p67zkf5j",
                split_order_id: "0nuorualyr8y",
                time_genno: 1460104554,
                juker_id: null,
                time_pay: 1460104554,
                time_calc: 163554150,
                nos_join: [],
                maxno_join: 7988,
                phase_num: 1,
                split_order_price: 184,
                is_phase_last: 1,
                addr_join: "上海市浦东新区",
                user_id: [],
                goods_title: "正品行货 全国联保",
                goods_pictures: [],
                goods_supplier_name: "盛趣网络科技有限公司",
                goods_caption: "Apple/苹果 iPhone 6s 4.7英寸 64G",
                goods_assortment_id: "0oxzlidnmd99",
                assortment_name: "apple",
                assortment_english: "apple",
                category_english: "phone",
                goodsdetail_detail: []
            },
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
            {},
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
        sum: 8105600257,
        luck_no: 922,
        price: 7988,
        time_pay: 1460104554,
        time_calc: 163554150
    },
    msg: "",
    status: 1
}

```