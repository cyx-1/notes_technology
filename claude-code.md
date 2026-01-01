
# Claude Code

- Key concepts:
    - [skills](https://claude.ai/share/30b3ca0d-cdaa-4e1a-98c2-fd27f252fc09)
    - [hooks](https://claude.ai/share/fb7be2eb-a1d8-4b05-ac08-0c18f50ed696)
    - [subagent](https://claude.ai/share/8aa3ce3c-1e2a-4ae9-a34a-139b8ff5457d)
    - [commands](https://claude.ai/share/2f275c03-4a44-4ef2-9c39-55a70ab21e90)
- Notes
    - not a good idea to use stop hook to orchestrate autonomous agentic work to perform a series of task, unless if there are official support
        - see this [discussion](https://claude.ai/share/32c57701-9cc9-4b7c-a12c-12cb7d928daa) on the complexities of using stop hook, decision flag and the stop_hook_active flag
        - there are also complications for making hook logic prompt-based
        - it would be better for autonomous agent logic to have ability to orchestrate not just Claude Code, but also Codex and others
    - an intelligent agent needs to check against limits to maximize the usage, but /usage only works in the interactive mode 
        - [claude-monitor](https://github.com/Maciek-roboblog/Claude-Code-Usage-Monitor)
            - only displays in Rich format
            - only tracks one device
        - [ccusage](https://github.com/ryoppippi/ccusage) 
            - doesn't show reset time
            - more useful when paying by API call
    - claude chat history location: $USERPROFILE\\.claude\projects
    - Claude controls Chrome:
        - [Claude Code with Chrome](https://code.claude.com/docs/en/chrome)
        - the following prompt appears to be taking and analyzing the screenshot
        ```
        claude --model haiku --chrome --permission-mode acceptEdits -p "open https://claude.ai/settings/usage page, and tell me what percentage is used for the current session, and when does it reset. return the result in yaml with two keys: plan _usage_limit_session_pct and plan_usage_limit_reset_time. plan_usage_limit_session_pct holds a numeric value, plan_usage _limit_reset_time holds a ISO timestamp in my machine's timezone. Save the yaml into a file called ./tmp/claude_usage.yaml"
        ```


Back to [index](index.md)