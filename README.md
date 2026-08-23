from selenium import webdriver
from selenium.webdriver.firefox.options import Options

options = Options()
options.add_argument("-profile")
options.add_argument("/home/kali/whatsapp-profile")

driver = webdriver.Firefox(options=options)
driver.get("https://web.whatsapp.com")

print("العنوان:", driver.title)

input("اضغط Enter للخروج: ")
driver.quit()
