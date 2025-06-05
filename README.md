# AI-Search

产品名称：萝卜投研AI搜索



AiSearch（萝卜投研） 是一款强大的智能投研搜索引擎。它能帮助用户一站式查找研报、财报、会议纪要、公告、资讯及关键数据指标，整合来自券商、交易所、公司、媒体等多源异构数据。覆盖股票（个股深度分析）、行业（产业链分析）、基金（产品评价及深度分析）及宏观市场等核心投资研究维度。
7、分类标签：搜索，研报，股票，基金，公告，资讯

MCP Server Url：https://mcp.datayes.com/ai/mcp/

可适配平台：方舟,vscode,python,Cherry Studio,Claude

## 支持Tools：


### Tool1: AiSearch 
从萝卜投研搜索研报、会议纪要、财报、资讯、公告和数据指标等信息，覆盖股票、行业、基金及市场等多维度
调试所需要的参数

#### 输入:
query: 搜索词(必填)
queryScope : 搜索指定范围[research-研报, announcement-公告, news-新闻, researchTable-研报图表, meetingSummary-会议纪要, indicator-数据指标,默认为全部all]

### Tool2: EtfAssistant
EtfAssistant（萝卜投研） 提供专业的ETF基金深度分析。整合海量结构化数据（如实时行情、历史K线、技术指标、收益风险指标、持仓明细、持有人结构、跟踪误差、资金流向、折溢价率、基金费率）与非结构化文本数据（如标的指数成分股行业基本面分析、市场情绪解读、相关论坛讨论热度），覆盖基金经理履历及基金公司实力评估。为用户提供从量化交易信号捕捉到基本面透彻研究，再到市场情绪感知的一站式ETF投资研究支持

#### 输入:
query: 搜索词(必填)

鉴权方式
API Key

## MCP配置例子
{
  "mcpServers": {
    "datayes-ai-search": {
      "name": "AiSearch",
      "type": "streamableHttp",
      "description": "ai search assistant",
      "isActive": true,
      "timeout": "120",
      "baseUrl": "https://mcp.datayes.com/ai/mcp/",
      "headers": {
        "Content-Type": "application/json",
        "Authorization": "Bear xxx"
      }
    }
  }
}

xxx 需要替换为自己获取到的token
