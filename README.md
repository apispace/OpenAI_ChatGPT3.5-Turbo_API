# APISpace 介绍
**本 API 服务由 [APISpace（apispace.com）](https://www.apispace.com/?utm_source=github&utm_term=chatgptturbo) 提供。**

APISpace 是 Eolink 旗下专业的 API 开放与交易平台，为广大企业以及个人开发者提供多维度、全方位的API接口，覆盖短信验证、天气查询、快递物流、OCR文字识别等海量 API 服务，帮助用户快速获取数据，降低获取数据的成本和难度，提升开发效率。

APISpace 提供15种开发语言的代码示例，分别是：
- Java(OK HTTP)
- HTTP
- cURL
- 微信小程序
- PHP(pecl_http)、PHP(cURL)
- Python(http.client)、Python(Requests)
- JavaScript(Jquery AJAX)、JavaScript(XHR)
- NodeJS(Native)、NodeJS(Request)
- Ruby(Net:Http)
- Shell(Httpie)、Shell(cUrl)

# OpenAI-ChatGPT 3.5 Turbo
ChatGPT-3.5 Turbo 模型是 ChatGPT 所使用的模型，现 OpenAI 已正式开放ChatGPT 的 API 能力供广大开发者使用，它可以提供超高准确性、可靠性和可扩展性，让机器学习和自然语言处理的开发者以极低的成本获取精准的结果。

**使用该产品前，您需要通过 [https://www.apispace.com/eolink/api/chatgpt-turbo/introduction](https://www.apispace.com/eolink/api/chatgpt-turbo/introduction?utm_source=github&utm_term=chatgptturbo) 申请API服务**

本文档末尾提供了 Python(Requests) 的调用代码示例，可以前往文档末尾查看。

更多代码示例：[https://www.apispace.com/eolink/api/chatgpt-turbo/guidence/](https://www.apispace.com/eolink/api/chatgpt-turbo/guidence/?utm_source=github&utm_term=chatgptturbo)

**使用注意事项：** 严禁提问政治敏感信息，请遵守相关法律法规。目前该API可 **正常调用**。

ChatGPT-3.5 Turbo 模型是 ChatGPT 所使用的模型，现已正式开放 API 能力供广大开发者使用。为了方便广大国内开发者体验最新的 GPT-3.5 Turbo 模型的能力，APISpace 通过官方渠道直接接入 OpenAI 的 GPT-3.5 Turbo 模型的 API。

注册 APISpace 即可免费获得 30 次调用，并且无需注册 OpenAI 海外账号、无需海外信用卡、快速测试、快速接入。


温馨提示：体验 ChatGPT-3.5 Davinci API，点击试用 [Davinci 的 GPT-3.5 API](https://www.apispace.com/eolink/api/chatgpt/introduction?utm_source=github&utm_term=chatgpt)

### 扣费标准

OpenAI 目前把单次的 **提问+回答** 限定在 4096 Tokens 以内，1 token=0.5个汉字=2个英文字符。也就是单次的提问+回答最多约 2048 个汉字的长度。


### GPT3.5 与 GPT3.5 Turbo

GPT 3.5 与 GPT 3.5 Turbo 的使用方式基本相同，但其功能上有一些可观察到的差异：

1.  GPT 3.5 主要用于自然语言处理、机器翻译等任务，而 GPT 3.5 Turbo 拥有更强大的强度，可用于更复杂的语言分析，比如情感分析、语法结构分析。
1.  GPT 3.5 支持更多的语言模型，可以更准确地解释自然语言输入；GPT 3.5 Turbo 只有一种语言模型，支持基于语料库的解释，但准确性会相应降低。
1.  GPT 3.5 的计算效率比 GPT 3.5 Turbo 要低，但其测试数据的准确性要高。因此，GPT 3.5 和 GPT 3.5 Turbo 各有各自的适用场景，具体选择视应用场景而定。


### 免责声明

本服务仅供个人学习、学术研究目的使用，未经许可，请勿分享、传播输入及生成的文本、图片内容。您在从事与本服务相关的所有行为（包括但不限于访问浏览、利用、转载、宣传介绍）时，必须以善意且谨慎的态度行事；您确保不得利用本服务故意或者过失的从事危害国家安全和社会公共利益、扰乱经济秩序和社会秩序、侵犯他人合法权益等法律、行政法规禁止的活动，并确保自定义输入文本不包含违反法律法规、政治相关、侵害他人合法权益的内容。

### Python(Requests) 调用代码示例

```
import requests

url = "https://eolink.o.apispace.com/chatgpt-turbo/create"

payload = {"system":"你是一个小助手","message":["user:我是孙悟空","assistant:你好,悟空","user:今天师傅有没有被抓走？"],"temperature":"0.9"}

headers = {
    "X-APISpace-Token":"",
    "Authorization-Type":"apikey",
    "Content-Type":""
}

response=requests.request("POST", url, data=json.dumps(payload), headers=headers)

print(response.text)

```
