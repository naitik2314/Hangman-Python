# Hangman-Python

## Libraries Used
- Rabdom

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Let's be honest, we all have played Hangman a lot when we were in school, I mean, my whole rough book was full of Tic Tac Toe, and Hangman, those were the good old days, go to school have fun with friends, and play games in between lectures, well enough of nostalgia, hope you like this game. Cheers....!

## What can be added?
- Theme based Hangman, add a switch case, and give words based on theme, like movies, cars, bikes etc.
- More words, or do Web Scrapping for words, based on theme.
- Add a first letter and mark vowels.

## Example code for Web Scrapping:
`<from bs4 import BeautifulSoup
import requests
headers = {'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/58.0.3029.110 Safari/537.3'}

def weather(city):
    city=city.replace(" ","+")
    res = requests.get(f'https://www.google.com/search?q={city}&oq={city}&aqs=chrome.0.35i39l2j0l4j46j69i60.6128j1j7&sourceid=chrome&ie=UTF-8',headers=headers)
    print("Searching in google......\n")
    soup = BeautifulSoup(res.text,'html.parser')   
    location = soup.select('#wob_loc')[0].getText().strip()  
    time = soup.select('#wob_dts')[0].getText().strip()       
    info = soup.select('#wob_dc')[0].getText().strip() 
    weather = soup.select('#wob_tm')[0].getText().strip()
    print(location)
    print(time)
    print(info)
    print(weather+"°C") 

print("Enter the city name")
city=input()
city=city+" Weather"
weather(city)>`
