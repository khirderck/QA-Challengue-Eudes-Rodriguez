# QA-Challengue-Eudes-Rodriguez
El objetivo de este challenge es ejecutar satisfactoriamente todos los pasos de las pruebas en las páginas web indicadas, empezando por el análisis de las pruebas hasta reporte de los resultados.



from selenium import webdriver
from selenium.webdriver.support.ui import Select
import time

driver = webdriver.Chrome('C:/chromedriver.exe')
driver.get("http://automationpractice.com/index.php?controller=contact")

time.sleep(2)

Subject = Select(driver.find_element_by_id('id_contact'))
Subject.select_by_value("2")

time.sleep(2)

Email = driver.find_element_by_name("from")
Email.send_keys("prueba@gmail.com")

time.sleep(2)

Order = driver.find_element_by_name("id_order")
Order.send_keys("8593")

time.sleep(2)

Mensaje = driver.find_element_by_name("message")
Mensaje.send_keys("Testing Pagina Web Eudes Rodriguez")

time.sleep(2)

Enviar = driver.find_element_by_name("submitMessage")
Enviar.click()


