# Cookiecutter

[Cookiecutter](https://github.com/cookiecutter/cookiecutter) is a command-line utility that helps developer create projects from predefined templates. 
It is a python utility that is typically installed [uv](uv.md) via ```uv tool install``` so that cookiecutter command is available everywhere. 

Use these command to create a new project from the existing template

```
# create a simple python project that supports uv, pytest and pre-commit
cookiecutter https://github.com/cyx-1/cookiecutter --directory simple_python

# create a project that deploys code to AWS Lambda, with support for uv, pyttest, and pre-commit
cookiecutter https://github.com/cyx-1/cookiecutter --directory aws_python_lambda

# create a simple Java project
cookiecutter https://github.com/cyx-1/cookiecutter --directory simple_java

```

Back to [index](index.md)