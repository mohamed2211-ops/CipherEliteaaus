from selenium import webdriver
from selenium.webdriver.firefox.options import Options

options = Options()
options.add_argument("-profile")
options.add_argument("/root/whatsapp-profile")

driver = webdriver.Firefox(options=options)
driver.get("https://web.whatsapp.com")

input("اضغط Enter بعد ما تتأكد أن واتساب ظاهر: ")
