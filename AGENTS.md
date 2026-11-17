<!-- [Update: 18/11/2026 00:22]
Kích hoạt AgentMemory & Auto Bootstrap cho repo yurikey. -->

# Quy Chuẩn Bộ Nhớ Dài Hạn — `yurikey`

<!-- agentmemory:start -->
## Agent memory (agentmemory) & Cơ chế Tự Động Thiết Lập (Auto Bootstrap)

You have persistent long-term memory via the agentmemory MCP server. Tools: `memory_recall`, `memory_smart_search`, `memory_save`, `memory_sessions`.

- **Auto Bootstrap trên máy mới:** Nếu đầu phiên chưa có tool `memory_recall`, **BẮT BUỘC** chạy ngay `python .agents/setup_agentmemory.py` (Windows PowerShell: `powershell -ExecutionPolicy Bypass -File .agents/setup_agentmemory.ps1`) để tự cài `@agentmemory/mcp`, đăng ký `mcp_config.json`, đồng bộ skills & quy chuẩn toàn cục rồi nạp lại công cụ.
- At the START of a task, call `memory_recall` (or `memory_smart_search`) with the task context to load relevant past decisions, fixes, and preferences before asking the user to repeat anything.
- When you learn something durable (a decision, a fix, a gotcha, a user preference, a project convention), call `memory_save` to persist it.
- Prefer recalling over re-deriving, and save concise reusable facts rather than transcripts.
<!-- agentmemory:end -->
