# scrapy
project

from bs4 import BeautifulSoup
import requests,openpyexcel

try:
    response = requests.get("https://www.booking.com/searchresults.en-gb.html?ss=Salem%2C+Tamil+Nadu%2C+India&ssne=Salemalivetech%2C+Salem%2C+Tamil+Nadu%2C+India&ssne_untouched=Salemalivetech%2C+Salem%2C+Tamil+Nadu%2C+India&label=gen173nr-1FCAEoggI46AdIM1gEaGyIAQGYAQm4ARfIAQzYAQHoAQH4AQOIAgGoAgO4Atjgx7AGwAIB0gIkMmZmYTIwNTMtOWVjZS00ZDVjLWFkMmUtNGJiNDFmN2NhNGRj2AIG4AIB&aid=304142&lang=en-gb&sb=1&src_elem=sb&src=searchresults&dest_id=-2109974&dest_type=city&ac_position=0&ac_click_type=b&ac_langcode=en&ac_suggestion_list_length=5&search_selected=true&search_pageview_id=055b0a0af63e01dd&ac_meta=GhAwNTViMGEwYWY2M2UwMWRkIAAoATICZW46B3NhbGVtLHRAAEoAUAA%3D&checkin=2024-04-26&checkout=2024-04-27&group_adults=2&no_rooms=1&group_children=0")
    soup = BeautifulSoup(response.text,'html.parser')
    hotels = soup.find('div',class_="bcbf33c5c3").find_all("div")
    '''for hotel in hotels:
        print(hotel)
        break'''

except Exception as e:
  print(e)
