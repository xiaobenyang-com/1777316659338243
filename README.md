# AI人格服务器 AI Persona

一个支持多AI人格召唤与协作的MCP协议服务器，可用于代码分析、产品设计等多场景智能协作。
An MCP protocol server that supports multi-AI personality summoning and collaboration, which can be used for intelligent collaboration in multiple scenarios such as code analysis and product design.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| summon_persona | 召唤指定人格来处理任务 |
| list_personas | 列出所有可用的人格 |
| version | 获取当前MCP服务版本信息 |
| interactive_persona | 智能人格协作分析 - 根据当前对话上下文自动选择合适的人格进行逐步分析 |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659338243](https://mcp.xiaobenyang.com/inspector/1777316659338243)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659338243](https://mcp.xiaobenyang.com/inspector/1777316659338243)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "AI人格服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659338243/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "AI人格服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659338243/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "AI人格服务器": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659338243",
          },
          "transport": "stdio"
        }
      }
}

```
