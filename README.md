# solo_code
import requests
from bs4 import BeautifulSoup

url = "http://www.vanityfair.com/society/2014/06/monica-lewinsky-humiliation-culture"
r = requests.get(url)
soup = BeautifulSoup(r.text, "lxml")
all_article = soup.select("article.article.main-content")
for article in all_article:
    print(article.text)
