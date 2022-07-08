# BUG-XL-AKRAB-UNLIMTED
BUG INI TELAH DI ENCRYPT KAALU MAU PAKE SILAHKAN EMAIL SAYA xxkenxxyz@gmail.com

ENGAK USAH COBA DECODE KALAU GAK MAU EROR


from bs4 import BeautifulSoup
import requests

url = "https://www.gov.br/planalto/pt-br/acompanhe-o-planalto/discursos"

r = requests.get(url)
print(f"The encoding is {r.encoding}")
soup = BeautifulSoup(r.text, 'html.parser')

lista_de_discursos = soup.find_all(name="a", attrs={"class": "summary"})

for x in lista_de_discursos:
    print(x.text)
    print("---"
