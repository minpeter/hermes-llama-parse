# hermes-llama parser (vllm)

This code is a hermes tool call parser for llama that works on vllm.
It adds a buffer function that prevents fragmentation with the "<", "tool", "_call", ">" tokens when training or prompting the llama model with the format defined in NousResearch/Hermes-Function-Calling without additional tokens.
You can check the original hermes parser at the link below.

https://github.com/vllm-project/vllm/blob/fa82b9385330319619ddb293a9f01ccd96fd0faf/vllm/entrypoints/openai/tool_parsers/hermes_tool_parser.py#L26


### Example launch command

```sh
vllm serve meta-llama/Llama-3.2-3B-Instruct \
--enforce-eager \
--enable-auto-tool-choice --tool-call-parser llama_hermes --tool-parser-plugin <<this_cloned_repo_path>>/lh_tool_parser.py  \
--port 4000 --enable-lora --lora-modules tool=minpeter/m-3b-v1-iteration-00-sf-xlam-10
```
