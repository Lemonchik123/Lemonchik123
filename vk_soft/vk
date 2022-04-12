from seleniumwire import webdriver
import time
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.webdriver.common.keys import Keys
import random
from selenium.webdriver.common.keys import Keys
from url import *


#Chromedriver
s = Service(executable_path="C:\\Users\\Administrator\\Desktop\\bo\\chromedriver.exe" )
driver = webdriver.Chrome(service=s)
driver.maximize_window()

try:
    driver.get("https://id.vk.com/auth?app_id=7913379&v=1.44.0&redirect_uri=https%3A%2F%2Fvk.com%2Ffeed&uuid=SMNyu5TPJQvxdZwuvW6Qn&action=eyJuYW1lIjoibm9fcGFzc3dvcmRfZmxvdyIsInBhcmFtcyI6eyJ0eXBlIjoic2lnbl9pbiJ9fQ%3D%3D")
    WebDriverWait(driver, 90).until(EC.presence_of_element_located((By.XPATH,"/html/body/div/div/div/div[2]/div/form/div[1]/section/div/div/div/input")))
    driver.find_element(By.NAME, "login").send_keys("nomer phone")#EMail
    WebDriverWait(driver, 90).until(EC.presence_of_element_located((By.XPATH,"//button[@type='submit']")))
    driver.find_element(By.CLASS_NAME,"vkc__Button__title").click()#Log
    
    WebDriverWait(driver, 90).until(EC.presence_of_element_located((By.XPATH,"/html/body/div/div/div/div[2]/div/form/div[1]/div[3]/div[2]/div[1]/div/input")))
    driver.find_element(By.XPATH,"/html/body/div/div/div/div[2]/div/form/div[1]/div[3]/div[2]/div[1]/div/input").send_keys("serg2781")#Password
    driver.find_element(By.CLASS_NAME,"vkc__Button__title").click()#Log
    time.sleep(9)
	#начало ворка
    while True: 
        for i in range(len(url)):
            try:
                driver.get(url[i])
                WebDriverWait(driver, 10).until(EC.presence_of_element_located((By.ID,"submit_post_box")))
                driver.find_element(By.ID,"submit_post_box").click()
                time.sleep(10)
                WebDriverWait(driver, 1).until(EC.presence_of_element_located((By.ID,"post_field")))
                driver.find_element(By.ID,"post_field").send_keys("Ищу команду бета тестеров в игру, ЗП - 20.000-50.000 руб, вложения не требуются, все что нужно - интернет и время!. Мой телеграм - https://t.me/Dim1253")   
                time.sleep(10)
                WebDriverWait(driver, 1).until(EC.presence_of_element_located((By.ID,"send_post")))
                driver.find_element(By.ID,"send_post").click()
                time.sleep(10)

                print(сделано)
            except:
                pass

except Exception as _ex:
    print(_ex)
finally:
    driver.close()
    driver.quit()
