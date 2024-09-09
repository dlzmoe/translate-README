## translate-README

> Writing a README file has always been a headache when developing personal projects. Fortunately, after struggling to finish it, creating a multilingual version became even more challenging. To solve this problem, I wrote a Python + GPT script to automate the entire process.

Create two files in the root directory: `.env` and `translate_md.py`, and simply assign the code directly.

Copy the code from `.env.example` into `.env` to configure the environment.

```shell
OPENAI_URL=https://api.openai.com/v1/chat/completions # base url
API_KEY=your_api_key_here # api key
MODEL=gpt-4o-mini # model
INPUT_FILE=README.md # source file
OUTPUT_FILE=README_EN.md # generated file
TARGET_LANGUAGE=en # target language
```

Personally, I prefer the `gpt-4o-mini` model. It provides sufficient coverage for my daily usage, offers fast generation speeds, and consumes tokens relatively efficiently, while excelling in both content creation and understanding.

Install the dependencies:

```shell
pip install requests
pip install python-dotenv
```

Run the script directly:

```shell
py translate_md.py
```

Click on [README_EN.md](./README_EN.md) to see the translated document.