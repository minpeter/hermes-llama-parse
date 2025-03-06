# hermes-llama parser (vllm)

This code is a hermes tool call parser for llama that works on vllm.
It adds a buffer function that prevents fragmentation with the "<", "tool", "_call", ">" tokens when training or prompting the llama model with the format defined in NousResearch/Hermes-Function-Calling without additional tokens.
You can check the original hermes parser at the link below.

https://github.com/vllm-project/vllm/blob/fa82b9385330319619ddb293a9f01ccd96fd0faf/vllm/entrypoints/openai/tool_parsers/hermes_tool_parser.py#L26