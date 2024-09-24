# OpenAI/ChatGPT 免翻墙代理

Fork from https://github.com/justjavac/openai-proxy

## 自己部署
Fork this repo

### Deno

https://dash.deno.com/new
Deploy like following


<img width="543" alt="image" src="https://github.com/gaxxx/openai-proxy/assets/471881/61deaeab-b701-4888-9db3-8d7ec20b6eda">


## 使用

```diff
  import openai

  openai.api_key = os.getenv("OPENAI_API_KEY")
+ openai.api_base = "<your deno instance>/v1"
```
