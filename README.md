## translate-README

> 在开发个人项目时，写 README 文件一直是一件很头疼的事情，所幸辛苦写完了，想做个多语言版本更头疼，为了解决整个痛点，写了个 python + GPT 脚本，将这一切自动化处理了。

在根目录下新建俩文件 `.env` 和 `translate_md.py`，代码直接赋值即可。

把 `.env.example` 的代码复制到 `.env` 配置一下环境。

```shell
OPENAI_URL=https://api.openai.com/v1/chat/completions # base url
API_KEY=your_api_key_here # api key
MODEL=gpt-4o-mini # 模型
INPUT_FILE=README.md # 源文件
OUTPUT_FILE=README_EN.md # 生成文件
TARGET_LANGUAGE=en # 目标语言
```

个人是比较喜欢 `gpt-4o-mini` 这个模型，功能足够覆盖我日常使用，生成速度快，对 token 的消耗也比较低，作图生文、理解性也都是前排水平。

安装依赖：

```shell
pip install requests
pip install python-dotenv
```

直接运行：

```shell
py translate_md.py
```

点击 [README_EN.md](./README_EN.md) 可以翻译后的文档。