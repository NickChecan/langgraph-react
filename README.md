# langgraph-react

ReAct is going to be the reasoning engine for this agent.

```mermaid
%%{init: {'flowchart': {'curve': 'linear'}}}%%
graph TD;
	__start__([<p>__start__</p>]):::first
	agent_reason(agent_reason)
	act(act)
	__end__([<p>__end__</p>]):::last
	__start__ --> agent_reason;
	act --> agent_reason;
	agent_reason -.-> act;
	agent_reason -.-> __end__;
	classDef default fill:#f2f0ff,line-height:1.2
	classDef first fill-opacity:0
	classDef last fill:#bfb6fc
```

### Install Dependencies
```sh
poetry add langchain langgraph langchain-openai langchainhub black isort python-dotenv grandalf langchain_community
```

### Environment
Here is the template for the .env file:
```
OPENAI_API_KEY=<API Key from openai>
TAVILY_API_KEY=<Tavily API Key>
LANGCHAIN_API_KEY=<API Key from langsmith>
LANGCHAIN_TRACING_V2=true
LANGCHAIN_PROJECT=<name that will show up in the langsmith dashboard>
```