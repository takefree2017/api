`这是数据格式的定义，在api文档里统一使用变量名的方式引用这些数据格式，假设定义了"myobject": {"id": 1111,"name": “123abc”}，文档里可以使用三种方式引用demo这种数据格式*myobject*、*{myobject}*、*{myobject(anotherName)}*，分别表示：`
`*myobject* -> "id": 1111,"name": “123abc”`
`*{myobject}* -> "demo": {"id": 1111,"name": “123abc”}`
`*{myobject(anotherName)}* -> "anotherName": {"id": 1111,"name": “123abc”}`

# 1. 分享/草稿
`"share":{
                "id": 1000001,
                "title": "title",
                "ownerId": 100001,
                "shareDescPreview": "description preview",
                "categoryIds": "11,22,33",
                "status": "10",
                "longitude": "10",
                "latitude": "10",
                "viewCount": 10,
                "viewCountLastView": 10,
                "commentCount": 10,
                "commentCountLastView": 10,
                "applyCount": 10,
                "applyCountLastView": 10,
                "likeCount": 10,
                "likeCountLastView": 10,
	        "picHomepage": "http://img0.qianbao.com/4,0f20b97296"
            }`

# 2. 分享的详情图片
`"sharePicUrls": {
            "0": "http://img0.qianbao.com/4,0f20b97296",
            "1": "http://img0.qianbao.com/4,0f20b97296",
            "2": "http://img0.qianbao.com/4,0f20b97296",
            "3": "http: //img0.qianbao.com/40f20b97296",
            "4": "http://img0.qianbao.com/4,0f20b97296",
            "5": "http://img0.qianbao.com/4,0f20b97296",
            "6": "http://img0.qianbao.com/4,0f20b97296",
            "7": "http: //img0.qianbao.com/40f20b97296",
            "8": "http://img0.qianbao.com/4,0f20b97296"
        }`

# 3. 用户
`"user": {
        "id": 1111,
        "nickName": “nick_name”,
        "realName": “real_name”,
        "mobile": "18800000000",
        "email": “email@163.com”,
        "password": “********”,
        "description": “111111111111”,
        "icon": "http://img0.qianbao.com/4,0f20b97296"
    }`

# 4. 申请
`"application": {
                "id": 10001,
                "shareId": 20001,
                "ownerId": 20001,
                "applyTime": 1504077543058,
                "applyType": 10,
                "status": 20,
                "address": "address"
            }`

# 5. 地址
`"address": {
                "id": 10001,
                "province": "province",
                "city": "city",
                "address": "address",
                "default": 0
            }`

# 6. 我关注谁
`"followee": {
                "userId": 20001,
                "nickName": "nick_name",
                "province": "",
                "city": "",
                "isFollower": 1,
                "icon": "http://img0.qianbao.com/4,0f20b97296"
            }`

# 7. 谁关注我
`"follower": {
                "userId": 20001,
                "nickName": "nick_name",
                "province": 300001,
                "city": 2000002,
                "isFollowee": 2000002,
                "icon": "http://img0.qianbao.com/4,0f20b97296"
            }`

# 8. 订单
`"takeOrder": {
                "id": 100001,
                "shareId": 100001,
                "ownerId": 100001,
                "applicantId": 100001,
                "applicationId": 100001,
                "takeTime": 1504077543058,
                "takeType": 10,
                "addressId": 100001,
                "orderStatus": 60,
            }`

# 9. 分享的评论
`"shareComment": {
                "id": 10002,
                "parentCommentId": 10001,
                "userId": 20004,
                "shareId": 1000001,
                "content": "content2"
            }`

# 10. 显摆
`"show": {
        "id": 111,
        "orderId": 1000001,
        "receiverId": 100001,
        "giverId": 100001,
        "viewCount": 10,
        "commentCount": 10,
        "applyCount": 10,
        "likeCount": 10,
        "showContentPreview": "show_content_preview",
        "moodIconUrl": "http://img0.qianbao.com/4,0f20b97296",
        "showPicUrls": {
            "0": "http://img0.qianbao.com/4,0f20b97296",
            "1": "http://img0.qianbao.com/4,0f20b97296",
            "2": "http://img0.qianbao.com/4,0f20b97296",
            "3": "http: //img0.qianbao.com/40f20b97296",
            "4": "http://img0.qianbao.com/4,0f20b97296",
            "5": "http://img0.qianbao.com/4,0f20b97296",
            "6": "http://img0.qianbao.com/4,0f20b97296",
            "7": "http: //img0.qianbao.com/40f20b97296",
            "8": "http://img0.qianbao.com/4,0f20b97296"
        }
    }`

# 11. 分享的评论
`"showComment": {
                "id": 10002,
                "parentCommentId": 10001,
                "userId": 20004,
                "content": "content2"
            }`