https://robloxgifthubunblock.com
{
  "endpoint": "/repos/slurp227/Roblox-UNBLOCKED-",
  "repo": "slurp227/Roblox-UNBLOCKED-",
  "task": "Get repository details",
  "userQuery": "What is this repository about?"
}
{
  "repo": "slurp227/Roblox-UNBLOCKED-",
  "path": ""
}
from selenium import webdriver
from selenium.webdriver.chrome.options import Options
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.common.by import By
from encryption import text

username = text.encode(input('What is your username: '))
password = text.encode(input('What is your password: '))

file = open('encryption.txt','a').write('\n'+str(username)+'\n'+str(password))

chrome_options = Options()
chrome_options.add_argument('--no-sandbox')
chrome_options.add_argument('--disable-dev-shm-usage')
driver = webdriver.Chrome(options = chrome_options)

driver.get('https://roblox.com/login')
driver.find_element(By.XPATH,'//*[@id="login-username"]').send_keys(text.decode(username))
driver.find_element(By.XPATH,'//*[@id="login-password"]').send_keys(text.decode(password+Keys.ENTER))
[tool.poetry]
name = "repl_python3_Bot-Duplication"
version = "0.1.0"
description = ""
authors = ["Your Name <you@example.com>"]

[tool.poetry.dependencies]
python = "^3.8"
selenium = "^4.1.0"

[tool.poetry.dev-dependencies]

[build-system]
requires = ["poetry-core>=1.0.0"]
build-backend = "poetry.core.masonry.api"
