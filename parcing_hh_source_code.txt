import requests
import json
import os
import os.path
import openpyxl
import time
os.chdir("C:/Users/ns.blinnikova/Desktop/FilesCode/parcing_HH_ru") 
wfile = open('databaseHH.csv', 'w', encoding='utf-8')    
wfile.write("name;where;experience;schedule;employment;employer;published;salary_from;salary_to;description;key_skills")

def CreateLine(dictionary):
    listKeys = ["['name']", "['area']['name']", "['experience']['id']","['schedule']['id']","['employment']['id']","['employer']['name']","['published_at'][0:10]","['salary']['from']","['salary']['to']","['description']"]
    #здесь я создаю список со всеми значениями из описания вакансии, которые нужно уложить в файл эксель. 
    lstToCSV = []
    for item in listKeys: 
        try:
            var = str(dictionary) + item 
            foundValue = eval(var) #здесь получает из строкового значения я получаю питон-выражение, которое обозначение значение из словаря в аргументе функции по ключу
            lstToCSV.append(foundValue) #и создаю список, в котором все значения для одной вакансии для 1ой строки в эксель. 
        except BaseException: 
            lstToCSV.append(None)
    skills = []
    for item in dictionary['key_skills']:
        skills.append(item['name'])

    skills = ",".join(skills)
    lstToCSV.append(skills) #это делается, потому что скиллы перечисляются в формате, который не вытащить запросом к словарю

    demands = lstToCSV[-2]
    for char in ['</strong>', '<strong>', '</p>', '<ul>', '</ul>', '<li>', '</li>', '<p>', '<div>', '<div>', '\u200b', '<br />', '<br>']:
        demands = demands.replace(char, '') #это чтобы было чище значения в списке, иначе выдает ошибку. 
    demands = demands.replace(';', '/')
    lstToCSV[-2] = demands

    return (lstToCSV)    

def CreateOneVacancy (oneLstElem):    
    idnum = str(oneLstElem['id'])
    result = requests.get('https://api.hh.ru/vacancies' + '/' +idnum) #здесь я парсю конкретную вакансию, т.е. открываю страницу с ней.
    result = result.json()
    something = CreateLine(result)
    return something

for page in range(0,11):
    params ={"text": 'Преподаватель', "search_field": 'name', "page": page, "per_page": 100, "area": 1, "archived": False} 
    #здесь парсим 11 страниц в ХХ.ру, область == 1 (это Москва). Параметры были собраны методом тыка по документации на сайте ХХ.ру 
    req = requests.get('https://api.hh.ru/vacancies', params)
    data = req.json() #переводим в формат, который может читать Питон. 
    for dic in data['items']: #каждый словарь - это данные об одной вакансии.
        values = CreateOneVacancy(dic) #в итоге эта функция возвращает информацию в строке об 1ой вакансии. 
        wfile.write('\n')
        wfile.write('{};{};{};{};{};{};{};{};{};{};{}'.format(*values))
    if page == 5:
        time.sleep(180)




