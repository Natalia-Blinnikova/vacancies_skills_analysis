# vacancies_skills_analysis
Parcing of recruiting web-site (hh.ru) for discovering skills demanded from perspective teachers. 

(English version. For Russian-language version scroll down). 
**Research of the demands to perspective teachers of employers from HeadHunter.ru. **

**Aim.** To discover, which skills are in demand in teaching according to the descriptions of vacancies for teachers on recruiting website hh.ru. 
Motivation. To know online courses on which topics would be relevant to the demands of the modern labour market in area of education. As I manage the production of online-courses at the university in Moscow and want to implement data-driven approach in my work. 

**Methodology. **
The analysis was done in two parts. 

At first, I created a small database in Excel file with the information about vacancies of teachers according to the criteria I indicated. Precisely, I included such data about each vacancy as name, demanded experience, schedule, type of employment, name of the employer, salary_from, salary_to, publication date, key_skills, description. The database was of 1035 vacancies that were not archived in April 2021 and available in Moscow only. For creating the database I used request module in python script and API for hh.ru. 

At second, I downloaded the database into pandas DataFrame and implemented small exploratory data analysis (EDA). During it I analysed the demands of the most active employers (that published more than 5 vacancies) and then the demands of all employers together. Afterwards I sorted data about vacancies according to its relevance to 12 unique combinations of two parameters in vacancies descriptions namely “demanded experience” and “schedule”. The aim was to compare if the demands to teachers skills depend on these two parameters.

Basically, I counted the noticing of different skills in the section “key_skills” of several datasets (mentioned above) of my database. 
Also, I compared salaries in vacancies grouped by the mentioned above two parameters (“demanded experience” and “schedule”) and grouped by the most active employers and all employers together. 

**Results. **

Employers on hh.ru that publish vacancies in teaching want to have the following skills in their perspective employees no matter how many vacancies they publish (let’s call these demands ‘general demands’). 

•	literacy; 
•	teamwork; 
•	distant learning; 
•	English; 
•	management; 
•	presentations skills (including creating presentations); 
•	communication (including business and group communication); 
•	individual learning; 
•	creative thinking; 
•	psychology; 
•	information literacy (or ability to work with big amounts of information); 
•	programming languages: Python, JavaScript, SQL, C#, web. 

Project work doesn’t demand special skills as the range of skills there is very narrow.

In the vacancies with the demanded experience from 1 to 3 years there is a difference in the list of demanded skills depending on the schedule. Part-time job requires more specialized skills like foreign languages, programming, and also soft skills like accuracy in details and politeness, also distant learning. Full-time job requires more management, psychology skills and creative thinking. This can point that part-time employees need to show their hard skills and service skills first as they work with clients who pay hourly. And full-time employees do need to manage their everyday workflow, communicate a lot with students that demands creative thinking too. 

Interestingly, when demands for the work-experience increase from 3 to 6 years or when no experience is required, demands for the specialized hard skills decrease but general skills remain in need and are supplemented by such soft skills as responsive attitude and punctuality. 

Moreover, in the vacancies with the demanded experience of more that 6 years they demand most commonly just general skills. Perhaps, this may be because people with such a huge experience are common hired for managing positions where general soft skills might be in a high demand. 

Regarding the salaries, the analysis shown that the start salary for teachers with any work-experience except 6 years is 40 000 rubles, while the mean salary is from 40 to 80 thousand rubles. For teachers with 6-years work-experience the mean salary is between 75 and 150 thousand rubles. Besides teachers with the work-experience up to 3 years may get the salary up to 100 000 rubles. 

**Conclusion. **

The must-have skills for all teachers are teamwork, communication, psychology, presentation skills. In dependance of work schedule and work-experience employers may demand such skills as creative thinking, management, service-skills, individual and distant learning, information literacy. This may be linked to the trends for online-education and implementation of customization into education.

Thus, I recommend to develop online-course on the following topics. 
1.	Information literacy. 
2.	Digital education.
3.	Presentation skills. 
4.	Management and events in pedagogy. 
5.	Team-work, communication and services in education. 
6.	Creativity in education.


РУССКОЯЗЫЧНОЕ ОПИСАНИЕ
**Исследование требований работодателей с HeadHunter.ru к преподавателям. **

**Исследовательский вопрос:** Какие навыки требуют от преподавателей работодатели, публикующие вакансии на сайте HeadHunter.ru?

**Цель исследования.** Определить навыки, которые требуют от преподавателей работодатели на сайте HeadHunter.ru.

**Применение выводов исследования.**
На основе полученных данных можно понять, какие навыки следует формировать у обучающихся педагогических вузов, в том числе, с помощью онлайн-курсов.

**Методология.**

Процесс сбора и анализа данных состоял из двух частей.

Первая часть – это создание базы данных с информацией о вакансиях преподавателя, размещенных на сайте HeadHunter.ru. Для этого с помощью программного кода на языке программирования python был осуществлен парсинг HeadHunter.ru.

В результате работы кода была собрана информация о 1035 вакансиях, отобранных по следующим признакам:

1.	место работы – Москва;
2.	вакансия не находится в архиве;
3.	в тексте названия вакансии содержится слово «преподаватель» (или «учитель», «педагог», «воспитатель» и аналогичные).
4.	
По каждой вакансии в таблицу Excel были собраны следующие данные:

1.	название;
2.	требуемый опыт работы;
3.	график работы;
4.	тип занятости;
5.	название организации-работодателя;
6.	дата публикации;
7.	нижнее значение зарплаты;
8.	верхнее значение зарплаты;
9.	описание вакансии;
11.	ключевые навыки.

Затем эта таблица была преобразована в формат Pandas DataFrame (далее – таблица), который анализировался с помощью библиотеки Python по работе с большими данными Pandas, что являлось второй частью исследования.

Анализ проводился в три этапа.

На первом этапе данные были разделены на два датасета:

1.	Ключевые навыки, которые требуют самые активные работодатели из выбранных, т.е. те, которые опубликовали более пяти вакансий.
2.	Навыки, которые требуют все работодатели, представленные в таблице.
3.	
В обоих датасетах были посчитаны упоминания тех или иных навыков и представлены в виде сводной таблицы.

На втором этапе был создан датасет, в котором ключевые навыки были отсортированы в зависимости от их двух признаков:
1.	требуемый опыт работы (возможные значения признаков: «без опыта», «от 1 до 3 лет», «от 3 до 6 лет», «более 6 лет»);
2.	график работы по вакансии (возможные значения признаков: «частичная занятость», «полный рабочий день», «проектная работа»).

То есть было получено 12 наборов ключевых навыков с уникальными комбинациями указанных выше признаков.
В каждом наборе были посчитаны упоминания тех или иных навыков и представлены в виде сводной таблицы. При этом включались только те навыки, которые упоминаются более трех раз в наборе.

На третьем этапе были проанализированы значения зарплат. Были проанализированы зарплаты по всем вакансиям, а также зарплаты по вакансиям по наборам, которые описаны выше (вакансиям, отсортированным по сочетаниям признаков «требуемый опыт работы» и «график работы по вакансии»).

**Интерпретация результатов.**

Работодатели на сайте HeadHunter.ru, которые публикуют вакансии преподавателей, заинтересованы в наличии у соискателей следующих компетенций (вне зависимости от того, как много вакансий они публикуют): 

•	грамотность (сюда же включается грамотная речь); 
•	работа в команде; 
•	дистанционное обучение (сюда же можно включить навыки пользования ПК); 
•	английский язык; 
•	организаторские навыки; 
•	выступление на презентациях (ораторские навыки), включая создание презентаций с помощью программных средств; 
•	коммуникация (деловая, межличностная, групповая); 
•	индивидуальное обучение; 
•	творческое мышление; 
•	психология; 
•	работа с большими объемами информации; 
•	а также владение языками программирования: Python, JavaScript, SQL, C#, веб-языками. 

Для удобства дальнейшей интерпретации результатов будем называть этот набор требуемых навыков общими требованиями. 

Вторая часть анализа показывает, что при проектной работе вне зависимости от требуемого опыта работы нет каких-либо ярко-выраженных требований к гибким навыкам, так как ничтожно малое количество навыков упоминается чаще трех раз. 

В вакансиях, где требуется опыт работы от 1 до 3 лет есть небольшие различия в списке требуемых навыков. Так, в вакансиях с частичной занятостью наблюдается большее разнообразие специализированных навыков, таких, как знание иностранных языков (немецкий, испанский), языков программирования (самых разных), а также отмечается необходимость таких качеств, как доброжелательность, точность к деталям. Также среди частых навыков – это организация дистанционного обучения.

В то же время в вакансиях на полный рабочий день и с таким же требуемым опытом работы особо выделяются организаторские навыки, знание психологии, творческое мышление. В обеих группах вакансий требуются навыки общения и работы в команде.

Предположительно, небольшая разница в требуемых навыках объясняется тем, что при частичной занятости требуются, вероятно, специалисты-репетиторы с почасовой оплатой, поэтому работодателям нужны, в первую очередь, их знания, а также некоторые навыки клиентоориентированности. В то время как преподаватели с полным рабочим днем сталкиваются с необходимостью организовывать свой рабочий процесс и много взаимодействовать с обучающимися, для чего и требуются навыки в психологии, организации и творческое мышление.

Интересно, что при увеличении «спроса» на опыт работы (от 3 до 6 лет) из списка необходимых навыков исчезают специализированные навыки. В дополнение к общим требованиям, добавляется требования ответственности и пунктуальности. Проведенный анализ не позволяет предположить, почему так меняются требования к ключевым навыкам, и для ответа на этот вопрос требуются дополнительные исследования.

В вакансиях без опыта работы набор навыков соответствует общим требованиям, а при полном рабочем дне добавляется требование ответственности и творческого мышления.
Также интересно, что в вакансиях с требуемым опытом более шести лет список навыков очень короткий и укладывается в общие требования. Вероятно, это можно объяснить тем, что работодатели «верят» в компетентность таких опытных педагогов и не считают нужным перечислять много требований.

Третья часть анализа, связанная с анализом зарплат, показывает, что средняя зарплата преподавателя в Москве составляет от 40 до 80 тысяч рублей, при этом есть выбросы в виде зарплат от 120 до 240 тысяч рублей. При полной занятости с опытом работы от 1 до 3 лет зарплаты составляют от 50 до 100 тысяч, а при росте опыта до 6 лет самые частые зарплаты - 75 000 рублей и 150 000 рублей. Так можно предполагать, что при росте опыта работы растет и размер зарплат. При опыте от 6 лет и полном рабочем дне зарплаты стартуют от 60 000 рублей.

Количество вакансий с проектной работой очень низкое в выборке, чтобы можно было делать какие-либо выводы об объеме зарплат. Без опыта работы начинающий специалист может рассчитывать на зарплату в 50 000 рублей при частичной занятости и даже доходить до 100 000 рублей при полном рабочем дне. 
Подытоживая, преподаватель в целом может рассчитывать на зарплату от 50 000 рублей при полной или частичной занятости и вне зависимости от своего профессионального опыта. 

**Выводы. **

Обучающимся педагогических направлений подготовки или практикующим преподавателям, которые хотят совершенствовать свои компетенции, обязательно требуются такие навыки, как: работа в команде, навыки коммуникации, знания психологии и навыки презентаций (выступления и создания). В зависимости от типа занятости и опыта работодатели требуют творческое мышление и организаторские навыки, а также клиентоориентированность. Требования к индивидуализации обучения и дистанционному обучению продиктованы, вероятно, тенденциями перехода обучения в онлайн. Также среди требований - умение работать с большими объемами информации, что, вероятно, также продиктовано переходом обучения в онлайн и открытым и широким доступом к любой информации. 


Таким образом, целесообразно создавать онлайн-курсы по следующим темам: 
1.	Информационная грамотность. 
2.	Цифровизация образования (включая методики дистанционного обучения).
3.	Создание и проведение презентаций. 
4.	Управление и организация мероприятий в педагогике. 
5.	Командная работа и виды коммуникаций в педагогике, включая клиентоориентированность. 
6.	Необычные подходы к организации учебного контента.






