# OpenAI/ChatGPT 免翻墙代理

据很多网友反应，**OpenAI 检测到中国的 API
访问时，会直接封号**。所以我在国外的服务器上搭建了一个代理，用于访问
OpenAI/ChatGPT 的 API。

---

## 自己部署
Fork this repo

### Deno

https://dash.deno.com/new
Deploy like following


<img width="543" alt="image" src="https://github.com/gaxxx/openai-proxy/assets/471881/61deaeab-b701-4888-9db3-8d7ec20b6eda">


## 使用

使用 OpenAI/ChatGPT 官方 npm 包：

```diff
import { Configuration } from "openai";

const configuration = new Configuration({
  apiKey: OPENAI_API_KEY,
+ basePath: "https://<your deno instance>/v1",
});
```

使用 OpenAI/ChatGPT 官方 Python 包：

```diff
  import openai

  openai.api_key = os.getenv("OPENAI_API_KEY")
+ openai.api_base = "<your deno instance>/v1"
```

## 相关仓库

- [ChatGPT 从入门到精通](https://github.com/justjavac/chatgpt)

## 本地开发

```bash
deno run --allow-net --allow-read --allow-env --watch deno.ts
```

[1]: https://dash.deno.com/new?url=https://raw.githubusercontent.com/justjavac/openai-proxy/main/deno.ts
