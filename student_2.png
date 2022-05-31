import requests 
from bs4 import BeautifulSoup

url = f"http://www.musinsa.com/ranking/keyword"

response  = requests.get(url)

if response.status_code == 200 :  
  html = response.text
  soup = BeautifulSoup(html, 'html.parser')     
  test = soup.find_all('p', {'class':'p_srank_last'})
  for code in test :
    print(code.get_text())

else : 
  print("연결되지않음")
  print(response.status_code)
