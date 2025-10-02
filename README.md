# llm-load-dir  

[![PyPI](https://img.shields.io/pypi/v/llm-load-dir.svg)](https://pypi.org/project/llm-load-dir/)  
[![Changelog](https://img.shields.io/github/v/release/ricardovelezz09-lgtm/llm-load-dir?include_prereleases&label=changelog)](https://github.com/ricardovelezz09-lgtm/llm-load-dir/releases)  
[![Tests](https://github.com/ricardovelezz09-lgtm/llm-load-dir/actions/workflows/test.yml/badge.svg)](https://github.com/ricardovelezz09-lgtm/llm-load-dir/actions/workflows/test.yml)  
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/ricardovelezz09-lgtm/llm-load-dir/blob/main/LICENSE)  

A plugin for [LLM](https://llm.datasette.io/) that loads text files from a local directory as fragments.  
This makes it easy to include structured context from your codebase, notes, or documents when prompting LLM.  

The current implementation attempts to load only files that are UTF-8 encoded.  

---

## 🔧 Installation  

Install this plugin in the same environment as [LLM](https://llm.datasette.io/):  

```bash
llm install llm-load-dir

```
## 🚀 Usage

Use `-f dir:path/to/directory` to recursively include every text file from the specified directory as a fragment. For example:
```bash
llm -f dir:/home/user/src/repo "Suggest new features for this tool"
```

## 🛠️ Development

To set up this plugin locally, first checkout the code. Then create a new virtual environment:
```bash
cd llm-fragments-dir
python -m venv venv
source venv/bin/activate
```
Now install the dependencies and test dependencies:
```bash
llm install -e '.[test]'
```
To run the tests:
```bash
pytest .
```
