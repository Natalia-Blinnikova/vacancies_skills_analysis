# vacancies_skills_analysis
Parcing of recruiting web-site (hh.ru) for discovering skills demanded from perspective teachers. 

For Russian-language version scroll down.

# Research of the demands to perspective teachers of employers from HeadHunter.ru.

## Product aim. 
To know online courses on which topics would be relevant to the demands of the modern labour market in area of education. 
### Tasks 
To create a small database in Excel file with the information about vacancies with features: name, demanded experience, schedule, type of employment, name of the employer, salary_from, salary_to, publication date, key_skills, description.
Implement exploratory data analysis (EDA) to know the employers demands. 
### What has been done
</br> I built a database of 1035 vacancies using request module in Python and API for hh.ru. 
</br> I analysed the demands of the most active employers (that published more than 5 vacancies) and then the demands of all employers together. 
</br> I compared salaries in vacancies grouped by various combinations of two parameters (“demanded experience” and “schedule”). 
</br> I counted the noticing of different skills in the section “key_skills” of several datasets (mentioned above) of my database. 
### Results.
The must-have skills for all teachers are teamwork, communication, psychology, presentation skills. In dependance of work schedule and work-experience employers may demand such skills as creative thinking, management, service-skills, individual and distant learning, information literacy. This may be linked to the trends for online-education and implementation of customization into education.

Thus, I recommend to develop online-course on the following topics. 
1.	Information literacy. 
2.	Digital education.
3.	Presentation skills. 
4.	Management and events in pedagogy. 
5.	Team-work, communication and services in education. 
6.	Creativity in education.

### Expanded discussion
In the vacancies with the demanded experience from 1 to 3 years there is a difference in the list of demanded skills depending on the schedule. Part-time job requires more specialized skills like foreign languages, programming, and also soft skills like accuracy in details and politeness, also distant learning. Full-time job requires more management, psychology skills and creative thinking. This can point that part-time employees need to show their hard skills and service skills first as they work with clients who pay hourly. And full-time employees do need to manage their everyday workflow, communicate a lot with students that demands creative thinking too. 

Interestingly, when demands for the work-experience increase from 3 to 6 years or when no experience is required, demands for the specialized hard skills decrease but general skills remain in need and are supplemented by such soft skills as responsive attitude and punctuality. 

Moreover, in the vacancies with the demanded experience of more that 6 years they demand most commonly just general skills. Perhaps, this may be because people with such a huge experience are common hired for managing positions where general soft skills might be in a high demand. 

Regarding the salaries, the analysis shown that the start salary for teachers with any work-experience except 6 years is 40 000 rubles, while the mean salary is from 40 to 80 thousand rubles. For teachers with 6-years work-experience the mean salary is between 75 and 150 thousand rubles. Besides teachers with the work-experience up to 3 years may get the salary up to 100 000 rubles. 



РУССКОЯЗЫЧНОЕ ОПИСАНИЕ

# Исследование требований работодателей с HeadHunter.ru к преподавателям. 
## Продуктовая цель.
Понять, какие навыки следует формировать у обучающихся педагогических вузов, в том числе, с помощью онлайн-курсов. 
### Задачи.
Первая часть – это создание базы данных с информацией о вакансиях преподавателя, размещенных на сайте HeadHunter.ru, каждая вакансия содержит следующие характеристики: 
1. название;
2.	требуемый опыт работы;
3.	график работы;
4.	тип занятости;
5.	название организации-работодателя;
6.	дата публикации;
7.	нижнее значение зарплаты;
8.	верхнее значение зарплаты;
9.	описание вакансии;
11.	ключевые навыки.
Вторая часть – разведочный анализ данных. 
### Что я сделала.
</br> Сформировала базу данных из 1035 вакансий с помощью библиотеки requests Python и API для hh.ru. 
</br> Проанализировала требования наиболее активных работодателей (опубликовали более 5 вакансий) и отдельно требования всех работодателей.  
</br> Сравнила зарплаты в 12 группах вакансий, сформированных комбинированием значений двух признаков: «требуемый опыт» и «график работы». 
</br> Посчитала упоминания разных навыков в секции «ключевые навыки».
### Выводы. 
Обучающимся педагогических направлений подготовки или практикующим преподавателям, которые хотят совершенствовать свои компетенции, обязательно требуются такие навыки, как: работа в команде, навыки коммуникации, знания психологии и навыки презентаций (выступления и создания). В зависимости от типа занятости и опыта работодатели требуют творческое мышление и организаторские навыки, а также клиентоориентированность. Требования к индивидуализации обучения и дистанционному обучению продиктованы, вероятно, тенденциями перехода обучения в онлайн. Также среди требований - умение работать с большими объемами информации, что, вероятно, также продиктовано переходом обучения в онлайн и открытым и широким доступом к любой информации. 
Таким образом, целесообразно создавать онлайн-курсы по следующим темам: 
1.	Информационная грамотность. 
2.	Цифровизация образования (включая методики дистанционного обучения).
3.	Создание и проведение презентаций. 
4.	Управление и организация мероприятий в педагогике. 
5.	Командная работа и виды коммуникаций в педагогике, включая клиентоориентированность. 
6.	Необычные подходы к организации учебного контента.
### Расширенные выводы
В вакансиях, где требуется опыт работы от 1 до 3 лет есть небольшие различия в списке требуемых навыков. Так, в вакансиях с частичной занятостью наблюдается большее разнообразие специализированных навыков, таких, как знание иностранных языков (немецкий, испанский), языков программирования (самых разных), а также отмечается необходимость таких качеств, как доброжелательность, точность к деталям. Также среди частых навыков – это организация дистанционного обучения.

В то же время в вакансиях на полный рабочий день и с таким же требуемым опытом работы особо выделяются организаторские навыки, знание психологии, творческое мышление. В обеих группах вакансий требуются навыки общения и работы в команде.

Предположительно, небольшая разница в требуемых навыках объясняется тем, что при частичной занятости требуются, вероятно, специалисты-репетиторы с почасовой оплатой, поэтому работодателям нужны, в первую очередь, их знания, а также некоторые навыки клиентоориентированности. В то время как преподаватели с полным рабочим днем сталкиваются с необходимостью организовывать свой рабочий процесс и много взаимодействовать с обучающимися, для чего и требуются навыки в психологии, организации и творческое мышление.

Интересно, что при увеличении «спроса» на опыт работы (от 3 до 6 лет) из списка необходимых навыков исчезают специализированные навыки. В дополнение к общим требованиям, добавляется требования ответственности и пунктуальности. Проведенный анализ не позволяет предположить, почему так меняются требования к ключевым навыкам, и для ответа на этот вопрос требуются дополнительные исследования.

В вакансиях без опыта работы набор навыков соответствует общим требованиям, а при полном рабочем дне добавляется требование ответственности и творческого мышления.
Также интересно, что в вакансиях с требуемым опытом более шести лет список навыков очень короткий и укладывается в общие требования. Вероятно, это можно объяснить тем, что работодатели «верят» в компетентность таких опытных педагогов и не считают нужным перечислять много требований.

Третья часть анализа, связанная с анализом зарплат, показывает, что средняя зарплата преподавателя в Москве составляет от 40 до 80 тысяч рублей, при этом есть выбросы в виде зарплат от 120 до 240 тысяч рублей. При полной занятости с опытом работы от 1 до 3 лет зарплаты составляют от 50 до 100 тысяч, а при росте опыта до 6 лет самые частые зарплаты - 75 000 рублей и 150 000 рублей. Так можно предполагать, что при росте опыта работы растет и размер зарплат. При опыте от 6 лет и полном рабочем дне зарплаты стартуют от 60 000 рублей.

Количество вакансий с проектной работой очень низкое в выборке, чтобы можно было делать какие-либо выводы об объеме зарплат. Без опыта работы начинающий специалист может рассчитывать на зарплату в 50 000 рублей при частичной занятости и даже доходить до 100 000 рублей при полном рабочем дне. 
Подытоживая, преподаватель в целом может рассчитывать на зарплату от 50 000 рублей при полной или частичной занятости и вне зависимости от своего профессионального опыта. 





