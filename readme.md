## 扩展功能 JSON 格式

### 说明

    artType    - 卡片类型 （3->快捷功能类型卡片；4->商品页类型卡片;5->文章类型卡片；6->视频类型卡片）
    artImage   - 预览图或者icon
    artTitle   - 标题
    artDesc    - 描述
    tookOpen   - 指定必须按照什么方式打开链接 （可选 web ，app ， wechat）（非必须，如果不填按当前环境跳转。如果指定了打开方式，openconfig中必须存在对应的url配置）
    openConfig - 配置不同打开方式需要的链接

    openConfig举例 ：
    	参数说明：
    	url  - 跳转地址
    	funcname - 需要调用的跳转方法app提供

    	示例：
        "openConfig":{
    		"wechat":{
    			"url":"/page/testvwb/test2/test2?pid=1"
    		},
    		"web":{
    			"url":http://www.baidu.com"
    		},
    		"app":{
    			url:"",
    			funcname:""
    		}
    	}

### 快捷功能举例：

    	[
    		{
    			"artType": 3,
    			"artImage": "https://v1.chayueshebao.com/upload/docImg/201712/b02a7681df9d4a79a299931b8f6747d9.png",
    			"artTitle": "社保断交后，如何进行补缴？",
    			"artDesc": "这些手续要知道，否则影响退休！",
    			"openConfig": {
    			"wechat": {
    				"url": "/page/testvwb/test2/test2?pid=1"
    			}
    			}
    		}
    	]

### 文章举例：url 的 ？号后面是文章 id （原 artid）

    	[
    		{
    			"artType": 5,
    			"artImage": "https://v1.chayueshebao.com/upload/docImg/201712/b02a7681df9d4a79a299931b8f6747d9.png",
    			"artTitle": "社保断交后，如何进行补缴？",
    			"artDesc": "这些手续要知道，否则影响退休！",
    			"tookOpen": "web",
    			"openConfig": {
    			"web": {
    				"url": "https://m.joyshebao.com/article.html?id=862"
    				}
    			}
    		}
    	]

### 视频举例： url 的 ？号后面是视频页 id（原 artid）

    	[
    		{
    			"artType": 6,
    			"artImage": "https://v1.chayueshebao.com/upload/docImg/201712/b02a7681df9d4a79a299931b8f6747d9.png",
    			"artTitle": "社保断交后，如何进行补缴？",
    			"artDesc": "这些手续要知道，否则影响退休！",
    			"tookOpen": "web",
    			"openConfig": {
    			"web": {
    				"url": "https://m.joyshebao.com/article.html?id=862"
    				}
    			}
    		}
    	]
