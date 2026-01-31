# git-basics-demo
---- This is a demo repositoryy to understand the flow of the code and learning git ------
--- by Vijay Kumar Moka
--- Tirupati


******************* Git details ***************

---------------- github browser ----------------
1. create a git
2. Download git and extract after .exe file install 
3. create a repository on git and add code
4. download zip / git clone https 
5. after it will take copy from cloud to local pc repository will save on local machine
6. make changes to code locally
7. git add test.py
8. git status
9. git commit -m " purpose of the commit "
10. git push 
11. git config --global user.email "mvijaykumar1424@gmail.com"
-------------- The very first time commit you should authenticate your email and password-----------
12. git push origin main
-- it will ask url browser email and password authentication ------
-- Access token thru will push the code from local machine to github browser --
---------------------------------------------------------------------------------

_______________________  Virtual environment----------------------------------------------------
This is few env variable installation steps when ever we ran the code it should ask interpreter popup we need to set the .venv platform----------------------------------
take one file names as test.ipnb and run one print command. it should be popup need to select the interpreter
select interpreter --> create virtual environment(.ven) -->select python version
vnev/conda --> cli
LLM (Large language models) -- pipelines

---------------------------------------------------------------------------------------------------
How to create a access token key 
1. go to profile below setting and go to developer settings
2. personal access token
3. token classic
4. generate new token key --> generate new token (classic)
5. note --> give name for using different projects
6. Scope --> select tick all check boxes and create a genertae a token it will show key save that file safely.
7. copy the token key when we push the code it will ask password or tokenkey for authentication.
------------------------------------------------------
How to call the api key without showing any token to anyone.
we should call that function by import 
1. install the dotenv package
2. pip install dotenv
it will show the the below packages extraction
Collecting dotenv
  Downloading dotenv-0.9.9-py2.py3-none-any.whl.metadata (279 bytes)
Collecting python-dotenv (from dotenv)
  Downloading python_dotenv-1.2.1-py3-none-any.whl.metadata (25 kB)
Downloading dotenv-0.9.9-py2.py3-none-any.whl (1.9 kB)
Downloading python_dotenv-1.2.1-py3-none-any.whl (21 kB)
Installing collected packages: python-dotenv, dotenv

   ---------------------------------------- 0/2 [python-dotenv]
   ---------------------------------------- 0/2 [python-dotenv]
   ---------------------------------------- 0/2 [python-dotenv]
   ---------------------------------------- 0/2 [python-dotenv]
   ---------------------------------------- 2/2 [dotenv]

Successfully installed dotenv-0.9.9 python-dotenv-1.2.1
Note: you may need to restart the kernel to use updated packages.

we should create a .env file . this is required to define the nam of the token what should we call from the code.
git_token=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

---
from code we should call the tokenkey
--
from dotenv import load_dotenv
import os
load_dotenv(dotenv_path=".env")
print(os.getenv("name of the token key"))

---
it will run the code you should run and pick and authorize the token access key without showing anyone.
token api key will save only google colab have a feature to save api key in secrets we can call that key below program
#bad practice
api_key = "Aguihfhugyhiljiyg589790ghjhjkhh"
response = call_api(api_key)
---
# good practice
how to access secret code in google oolab
from google.colab import userdata
api_key = userdata.get("GEMINI_API_KEY")
----



