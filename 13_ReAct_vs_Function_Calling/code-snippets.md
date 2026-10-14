# Code blocks from: What Production Deployments Taught Me About ReAct vs Function Calling

Code blocks copied from the post, in order. They are fragments, not a runnable notebook.

Source: https://www.mlwhiz.com/p/what-production-deployments-taught

## 1. Example: The Same Weather Query

```
{
  "function_call": {
    "name": "get_current_weather",
    "arguments": {
      "location": "Paris, France",
      "units": "celsius"
    }
  }
}
```

## 2. ReActAgent in LLamaIndex

```bash
pip install llama-index-llms-gemini llama-index-core
```

## 3. 1. Customizing ReAcT Prompts in LlamaIndex

```python
from llama_index.core.agent.react.formatter import ReActChatFormatter

# Create a formatter to see the default prompt
formatter = ReActChatFormatter()
print("Default ReAct System Prompt:")
print(formatter.system_header)
```

## 4. 1. Customizing ReAcT Prompts in LlamaIndex

```python
agents = ReActAgent.from_tools(
                [list_of_tools],
                llm=llm,
                verbose=True,
                react_chat_formatter=ReActChatFormatter(
                    system_header=get_react_prompt()
                ),
            )

def get_react_prompt():
    return """YOUR PROMPT with {tool_desc} and {tool_names} placeholders"""
```

## 5. 2. Tools with Type Annotations

```python
from typing import Annotated

def get_weather(
    location: Annotated[str, "The city and country, e.g., 'Paris, France'"]
) -> str:
```

## 6. 3. Preload context vs Provide Tools

```python
def get_user_favs(user_id)
```

## 7. 3. Preload context vs Provide Tools

```python
def get_user_favs(user_id):
    user_id = get_user_id_from_request_headers()
```
