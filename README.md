import requests
from bs4 import BeautifulSoup

url = "https://example.com"
page = requests.get(url)
soup = BeautifulSoup(page.content, "html.parser")

for title in soup.find_all("h2"):
    print(title.text)
