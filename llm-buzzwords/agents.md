# Buzzwords in Agentic Systems

## Agents

LLM agents are advanced AI systems designed for solving complex
tasks that requires sequential reasoning.
A basic LLM agent requires a structured plan, a reliable memory to
track progress and context, and access to necessary tools. These
components form the framework of an agentic workflow with LLMs.
LLM agents can solve advanced problems, learn from their mistakes,
use specialized tools to improve their work, and even collaborate with
other agents to improve their overall performance.
However, they have limitations, such as a short memory span and a
need for precise directions with tool calling.

## Tool/Function Calling
Tools calling is the capability of agentic systems to utilize a set of tool(s) in order to
interact with their environment, use external services such as Search APIs, Code
Interpreter, bank transaction APIs and even Gmail.
Function Calling is very similar to tool calling with just a small variation, in that it is
augmented with LLMs pre-training data for tool calling capabilities which involves
defining a set of tool APIs and providing it as part of a request.Direct tool calls consume context for each definition and result. Agents scale better by writing code to call tools instead.

## Tool Recognition
Tool recognition is a sub-set of tool calling that the user/dev  have identified. It looks
at how LLM Agents are able to recognize complex description in tool calling
parameter and use them effectively with minimal/zero false tool calls and
hallucinations.

## Reinforcement Learning

Reinforcement learning (RL) is a machine learning technique that
allows an agent to learn by interacting with an environment and
receiving rewards or punishments for its actions. The agent learns
through trial and error, adjusting its behavior to maximize its
reward.

## Model Context Protocol: MCP

It is an open standard for connecting AI agents to external systems. Connecting agents to tools and data traditionally requires a custom integration for each pairing, creating fragmentation and duplicated effort that makes it difficult to scale truly connected systems. MCP provides a universal protocol—developers implement MCP once in their agent and it unlocks an entire ecosystem of integrations. See Anthropics MCP for more details [Anthropic MCP](https://www.anthropic.com/news/model-context-protocol).

## Resources

- https://www.anthropic.com/engineering/code-execution-with-mcp
- https://python.langchain.com/docs/integrations/model_context/overview