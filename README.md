from selenium import webdriver
from selenium.webdriver.common.keys import Keys
import time

# Инициализация драйвера
driver = webdriver.Chrome()  # Предварительно необходимо установить ChromeDriver

# Открытие веб-страницы
driver.get("https://www.example.com")  # Замените на URL, который нужно прокрутить

# Прокрутка страницы вниз
driver.find_element_by_tag_name("body").send_keys(Keys.END)  # Можно использовать Keys.PAGE_DOWN для прокрутки на одну страницу вниз

# Дополнительная пауза, чтобы дать странице прокрутиться
time.sleep(2)

# Закрытие браузера
driver.quit()
