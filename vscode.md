# VSCode
- Useful extensions
    - general
        - github.copilot
        - github.copilot-chat
        - usernamehw.errorlens
        - eamodio.gitlens
        - mechatroner.rainbow-csv
        - wayou.vscode-todo-highlight
        - vscodevim.vim
        - zenofsoftware.dc-robin
    - python
        - charliermarsh.ruff
        - ms-python.mypy-type-checker
        - ms-python.vscode-pylance
        - ms-python.python
        - ms-python.debugpy
        - ms-python.vscode-python-envs
    - java
        - vscjava.vscode-java-debug
        - vscjava.vscode-java-pack
        - vscjava.vscode-maven
        - vscjava.vscode-java-dependency
        - vscjava.vscode-java-test
        - redhat.java

- settings.json usually under %appdata%\Roaming\Code\User
```
{
    "editor.formatOnSave": true,
    "editor.lineNumbers": "relative",
    "editor.minimap.enabled": false,
    "editor.rulers": [
        165
    ],
    "vim.easymotion": true,
    "vim.easymotionMarkerBackgroundColor": "black",
    "vim.insertModeKeyBindings": [
        {
            "before": [
                "j",
                "j"
            ],
            "after": [
                "<Esc>"
            ]
        }
    ],
    "vim.leader": ",",
    "vim.normalModeKeyBindingsNonRecursive": [
        {
            "before": [
                "<leader>",
                "/"
            ],
            "commands": [
                ":s/\\\\\\\\/\\//g"
            ]
        },
        {
            "before": [
                "<leader>",
                "\\"
            ],
            "commands": [
                ":s/\\//\\\\/g"
            ]
        },
        {
            "before": [
                "<leader>",
                "t"
            ],
            "commands": [
                "workbench.action.terminal.focus"
            ]
        },
        {
            "before": [
                "<leader>",
                "r",
                "n"
            ],
            "commands": [
                ":set relativenumber"
            ]
        },
        {
            "before": [
                "<leader>",
                "n"
            ],
            "commands": [
                ":set number"
            ]
        },
        {
            "before": [
                "J"
            ],
            "after": [
                "5",
                "j"
            ]
        },
        {
            "before": [
                "K"
            ],
            "after": [
                "5",
                "k"
            ]
        },
        {
            "before": [
                "<leader>",
                "j"
            ],
            "after": [
                "J"
            ]
        },
        {
            "before": [
                "<leader>",
                "r",
                "q"
            ],
            "commands": [
                {
                    "command": "runInTerminal.run",
                    "args": {
                        "name": "q"
                    }
                }
            ]
        },
        {
            "before": [
                "<leader>",
                "r",
                "b"
            ],
            "commands": [
                {
                    "command": "runInTerminal.run",
                    "args": {
                        "name": "b"
                    }
                }
            ]
        },
        {
            "before": [
                "<leader>",
                "r",
                "t"
            ],
            "commands": [
                {
                    "command": "runInTerminal.run",
                    "args": {
                        "name": "t"
                    }
                }
            ]
        },
        {
            "before": [
                "<leader>",
                "r",
                "s"
            ],
            "commands": [
                {
                    "command": "runInTerminal.run",
                    "args": {
                        "name": "s"
                    }
                }
            ]
        },
        {
            "before": [
                "<leader>",
                "o"
            ],
            "commands": [
                "workbench.action.showEditorsInActiveGroup"
            ]
        }
    ],
    "vim.surround": true,
    "vim.useSystemClipboard": true,
    "vim.visualModeKeyBindingsNonRecursive": [
        {
            "before": [
                ">"
            ],
            "commands": [
                "editor.action.indentLines"
            ]
        },
        {
            "before": [
                "<"
            ],
            "commands": [
                "editor.action.outdentLines"
            ]
        }
    ],
    "[python]": {
        "editor.defaultFormatter": "charliermarsh.ruff",
        "editor.formatOnSave": true
    },
    "github.copilot.nextEditSuggestions.enabled": true,
    "terminal.integrated.defaultProfile.windows": "Git Bash",
    "terminal.integrated.suggest.enabled": true,
}
```

Back to [index](index.md)