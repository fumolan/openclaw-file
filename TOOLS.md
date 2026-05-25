# TOOLS.md - Local Notes

Skills define _how_ tools work. This file is for _your_ specifics — the stuff that's unique to your setup.

## Container Runtime

- **Podman** — 已安装，可用于容器化任务

## Sandbox

- **CubeSandbox** — `/home/fumolan/claude/softhub/CubeSandbox`
- 用于代码沙箱执行

## Local LLM (llama.cpp)

- **路径:** `/home/fumolan/claude/llama.cpp`
- **模型文件:** `/home/fumolan/claude/llama.cpp/gguf/`
  - `granite-4.1-8b-Q4_K_S.gguf` (4.7GB) — IBM Granite 4.1 8B
  - `Qwen3.5-9B-Q4_K_S.gguf` (5.0GB) — 通义千问 3.5 9B
  - `Qwen3.6-27B-Q4_K_S.gguf` (14.8GB) — 通义千问 3.6 27B (最大最强)

## Notes

- 所有工具以 `fumolan` 用户运行
- 模型量化格式均为 Q4_K_S（4-bit量化，速度与质量平衡）
- 按需调用，27B模型需要足够内存
