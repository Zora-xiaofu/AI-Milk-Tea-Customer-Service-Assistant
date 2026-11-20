# 茶序奶茶助手 | AI Milk Tea Customer Service Assistant
练习-一个支持FAQ知识库问答、订单号识别和模拟订单查询的AI客服工作流项目。

基于 **Dify Chatflow** 构建的奶茶店 AI 客服演示项目，支持门店常见问题解答、订单状态与取餐号查询、制作队列查询，以及围绕同一订单的连续追问。

A milk tea customer service demo built with **Dify Chatflow**, supporting store FAQs, order status and pickup-code enquiries, production queue information, and follow-up questions about an order.

## 在线体验 | Live Demo

**[点击体验茶序奶茶助手 | Try the Live Demo](https://udify.app/chat/Vpf3yWNWTlrpbHA0)**

> **演示说明 / Demo Notice**  
> 订单查询使用工作流中预设的**模拟订单与固定制作队列数据**，不连接真实门店订单数据库。订单状态不会随时间自动更新，查询结果仅供功能演示，不代表真实订单进度。  
> Order enquiries use **predefined sample orders and a fixed queue snapshot**. The demo is not connected to a live store database; order status does not update automatically.

## 核心功能 | Features

- **意图识别 / Intent recognition：** 根据用户问题，将请求分流至FAQ问答或订单相关处理流程。
- **知识库问答 / Knowledge-based FAQ：** 检索知识库，为门店规则等常见问题生成回答。
- **订单查询 / Order lookup：** 提取订单号，查询模拟订单状态、取餐号与杯数信息。
- **制作队列 / Production queue：** 基于固定模拟队列，计算前方尚待制作的杯数和当前订单制作情况。
- **连续追问 / Follow-up questions：** 保存当前订单号，支持用户围绕同一订单继续提问。

## 体验示例 | Try These Questions

1. `你们有什么门店规则？` / `What are your store policies?`
2. `帮我查询订单 T1003` / `Check order T1003.`
3. `前面还有几杯没做？` / `How many drinks are ahead of mine?`
4. `我的取餐号是什么？` / `What is my pickup code?`

**可用演示订单号 / Sample order IDs:** `T1001`, `T1002`, `T1003`, `T1004`, `T1005`。

## 工作流设计 | Workflow

`用户输入 → LLM意图识别 → 条件分支 → FAQ知识检索 / 订单号提取 → 模拟订单与队列查询 → 回复生成`

`User input → LLM intent classification → Conditional routing → FAQ retrieval / Order ID extraction → Simulated order and queue lookup → Response generation`

项目通过 **LLM节点、条件分支、知识库检索、Python代码节点及变量赋值节点**组织客服流程。订单查询使用预设数据，不依赖实时订单API。

The workflow combines **LLM nodes, conditional routing, knowledge retrieval, Python code nodes, and variable assignment**. Order lookup uses predefined records rather than a live order API.

## 技术栈 | Tech Stack

**Dify Chatflow · LLM · Knowledge Retrieval · Prompt Design · Python · Conditional Logic**

## 项目定位 | Project Scope

这是一个用于展示 **AI应用产品设计与工作流编排** 的学习项目，不是已接入真实门店业务系统的商业客服产品。

This is a portfolio demo of **AI application design and workflow orchestration**, not a production customer service system integrated with a real store.
