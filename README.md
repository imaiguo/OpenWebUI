
# Open WebUI 👋

## Windows环境部署

准备独立的python环境

```bash
> cmd
> cd D:\devtools\PythonVenv
> python -m venv OpenWebUI
> D:\devtools\PythonVenv\OpenWebUI\Scripts\activate.bat
```

## Debian环境部署

设置python虚拟环境
```bash
> cd /opt/Data/PythonVenv
> python3 -m venv OpenWebUI
> source /opt/Data/PythonVenv/OpenWebUI/bin/activate
```

部署推理环境
```bash
> pip install open-webui -i https://pypi.tuna.tsinghua.edu.cn/simple
> sudo apt install ffmpeg
```


## 服务运行

参考 https://docs.openwebui.com/getting-started/env-configuration

```bash
> # 默认Embedding model set: sentence-transformers/all-MiniLM-L6-v2
> # 参考文件 D:\devtools\PythonVenv\OpenWebUI\Lib\site-packages\open_webui\retrieval\utils.py
> cmd
> export OFFLINE_MODE=True
> export HF_HUB_OFFLINE=True
> export RAG_EMBEDDING_MODEL="openai"
> export ENABLE_OPENAI_API=False
>
> open-webui serve
```

## OpenWebUI卡顿

https://github.com/open-webui/open-webui/discussions/2171

Same here. I solved the issue by using postgres (via DATABASE_URL environment variable) instead of default SQLite. Now api request to /chats (which performed when you open OpenWebUI) is much faster.
