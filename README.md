python3 -c "
from selenium import webdriver
from selenium.webdriver.firefox.options import Options
from selenium.webdriver.firefox.service import Service

options = Options()
options.add_argument('-profile')
options.add_argument('/home/kali/whatsapp-profile')

service = Service(executable_path='/usr/local/bin/geckodriver', log_output='/dev/null')

driver = webdriver.Firefox(service=service, options=options)
driver.get('https://web.whatsapp.com')
input('امسح الـ QR كود واضغط Enter هنا في التيرمنال عندما تجهز واتساب: ')
driver.quit()
"
