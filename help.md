**Ollama**
ollama start
--> NEW cmd "ollama run [model]

gemma3:4b             a2af6cc3eb7f    3.3 GB   
deepseek-r1:latest    6995872bfe4c    5.2 GB   
llama3.2:latest       a80c4f17acd5    2.0 GB   

https://medium.com/@gabrielrodewald/running-models-with-ollama-step-by-step-60b6f6125807

https://github.com/ollama/ollama-python

# ===================================================================

client = OpenAI(
    base_url = 'http://localhost:11434/v1/',
    api_key='ollama',
)

from ollama import chat
from ollama import ChatResponse

response: ChatResponse = chat(model='deepseek-r1:latest', messages=[
  {
    'role': 'user',
    'content': q,
  },
])
# print(response['message']['content'])
# or access fields directly from the response object
# print(response.message.content) - ONLY ONE "CHOICE"
print(response.message.content)

# ===================================================================

**Git**
git init
git status
git add 
git commit (with commit msg if you want)
git push

**After installing all packages (either with pip or uv)**
pip freeze > requirements.txt

If error in UV: https://github.com/astral-sh/uv/issues/**7285**

**Always start with:**
.venv\Scripts\activate

OR click on left side: "Python" --> "Open in Terminal"

If error in Powershell: https://stackoverflow.com/questions/18713086/virtualenv-wont-activate-on-windows

https://stackoverflow.com/questions/64633727/how-to-fix-running-scripts-is-disabled-on-this-system
Set-ExecutionPolicy RemoteSigned –Scope Process
--> **Needed to be able to run npm on TERMINAL safely, just for this session (DO EVERY TIME YOU RESTART).**

https://www.freecodecamp.org/news/gitignore-file-how-to-ignore-files-and-folders-in-git/#contents