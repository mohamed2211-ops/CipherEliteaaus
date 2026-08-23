from selenium import webdriver
from selenium.webdriver.firefox.options import Options

options = Options()
options.add_argument("-profile")
options.add_argument("/root/whatsapp-profile")

driver = webdriver.Firefox(options=options)
driver.get("https://web.whatsapp.com")

input("اضغط Enter بعد ما تتأكد أن واتساب ظاهر: ")




python3 -c "from selenium import webdriver; from selenium.webdriver.firefox.options import Options; o=Options(); o.add_argument('-profile'); o.add_argument('/home/kali/whatsapp-profile'); d=webdriver.Firefox(options=o); d.get('https://web.whatsapp.com'); input('اضغط Enter بعد ظهور واتساب: ')"
