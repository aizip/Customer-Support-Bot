# DIY-Customer-Support-Bot

![License](https://img.shields.io/badge/license-MIT-blue.svg) ![Version](https://img.shields.io/badge/version-1.0.0-green.svg)

## Introduction

Welcome to **Customer-Support-Bot**!
It's a nice demo of an AI Agent in business scenarios. 
This Project is built upon one of the langgraph examples: 
[GitHub](github.com/langchain-ai/langgraph/blob/main/examples/customer-support/customer-support.ipynb)

The project is built on langgraph. 

## Features

- **Feature 1:** [Memory and Context]
- **Feature 2:** [Continuous Conversation]
- **Feature 3:** [Parallel Function Calling]
- **Feature 4:** [Checkpointing And Interruption Before Calling Tools]

## Installation

To get started with **Customer Support Bot**, follow these steps:

•  You may pick one of the three demos

• The url in the jupyter notebook will fetch a preexisting sqlite database for RAG. 

• There is a list of example questions for your reference. 


### Prerequisites

Ensure you have the following installed:

- [Python] - Version 3.10
- [langgragh] - Newest Version

You can install required packages running:

```
%%capture --no-stderr
%pip install -U langgraph langsmith

# Used for this tutorial; not a requirement for LangGraph, Or you can use OPENAI
%pip install -U langchain_anthropic
#or
%pip install -U langchain_openai
```

### Important Concepts

#### Graph:

Agents are built in stucture of graphs in langgraph. 
The most commonly used graph is StatefulGraph: 

• Nodes are functions or object instances of Runnable Class

• Edges that direct information between nodes

#### State Object:
```python
# State Object are structures that carries information flow between nodes and through edges. Usually inherits TypedDict class

class State(TypedDict):
    messages: Annotated[list[AnyMessage], add_messages]
    user_info: str

# add_messages are a function that updates the State Object, appending new messages to the state. 

```

### Clone the Repository

```bash
git clone https://github.com/aizip/Customer-Support-Bot.git
cd Customer-Support-Bot

```



