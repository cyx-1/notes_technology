
# Notes on Claude Code

- not a good idea to use stop hook to orchestrate autonomous agentic work to perform a series of task, unless if there are official support
    - see this [discussion](https://claude.ai/share/32c57701-9cc9-4b7c-a12c-12cb7d928daa) on the complexities of using stop hook, decision flag and the stop_hook_active flag
    - there are also complications for making hook logic prompt-based
    - it would be better for autonomous agent logic to have ability to orchestrate not just Claude Code, but also Codex and others
    - although the [Ralph for Claude Code](https://github.com/frankbria/ralph-claude-code) looks attractive but it is not sustainable due to reasons above
- an intelligent agent needs to check against limits to maximize the usage, but Claude slash command /usage only works in the interactive mode. 
    - Open source solution are also not suitable:
        - [claude-monitor](https://github.com/Maciek-roboblog/Claude-Code-Usage-Monitor) only displays in Rich format and only tracks one device
        - [ccusage](https://github.com/ryoppippi/ccusage) doesn't show reset time, more useful when paying by API call
        - while forking and enhancing the open source solution is one route, a robust route is to use Claude control over Chrome
- Claude controls Chrome:
    - [Claude Code with Chrome](https://code.claude.com/docs/en/chrome)
    - the following prompt takes the Claude usage website with existing cookie and session credential and analyzes the screenshot for retrieving key information
    ```
    claude --model haiku --chrome --permission-mode acceptEdits -p "open https://claude.ai/settings/usage page, and tell me what percentage is used for the current session, and when does it reset. return the result in yaml with two keys: plan _usage_limit_session_pct and plan_usage_limit_reset_time. plan_usage_limit_session_pct holds a numeric value, plan_usage _limit_reset_time holds a ISO timestamp in my machine's timezone. Save the yaml into a file called ./tmp/claude_usage.yaml"
    ```
    - other solutions are not suitable:
        - playwright tries to reuse the cookies and session, but runs into cloudflare blocker
        - selenium would not offer reuse of cookies and session information
- claude chat history location: $USERPROFILE\\.claude\projects


Back to [index](index.md)