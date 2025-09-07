# Overview

Written in the Rust language, uv is a modern utility that handles library dependencies, global tools, virtual environments and Python intepretors. This utility makes pip, pipx, venv and pyenv obsolete, due to significant speed improvement and simplification. 

When working in an environment where the proxy server blocks direct access to Python package websites, and SSL certs are self-signed, remember to set environment variables: UV_DEFAULT_INDEX, REQUESTS_CA_BUNDLE, SSL_CERT_FILE. 

The following commands are helpful

- Install uv on Windows: ```powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"```
- Install uv on MacOS or Linux: ```curl -LsSf https://astral.sh/uv/install.sh | sh```
- Review current version for uv: ```uv --version```
- Set up a Python project in an empty folder, creating core files such as pyproject.toml: ```uv init```
- For a Python project that already has pyproject.toml file, run this command to synchronize the library installation: ```uv sync```
- To add a library and its dependencies, update the top-level library dependency in pyproject.toml, run: ```uv add <package>```
- To run a python program with automatic handling of virtual environment activation ```uv run <python file>```
- To explicitly set up a virtual environment: ```uv venv```
- To set up a virtual environment using a specific python version, instead of the default one found on the PATH
```uv venv --python "<path to python exe>"```
- To switch to a different python version: update ```.python-version``` and then run ```uv run python --version```
- To install a global tool called pre-commit at Python 3.13 level: ```uv tool install pre-commit --python 3.13```

Back to [index](index.md)