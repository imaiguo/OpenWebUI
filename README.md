
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
> open-webui serve
```


### 设置环境变量

```bash
> # 默认Embedding model set: sentence-transformers/all-MiniLM-L6-v2
> # 参考文件 D:\devtools\PythonVenv\OpenWebUI\Lib\site-packages\open_webui\retrieval\utils.py
> cmd
> set SENTENCE_TRANSFORMERS_HOME = ""
```