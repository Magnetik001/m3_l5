import random

kol_st = 0
name_st = []
last_name_st = []

name = ['Аня','Ваня','Юля','Дима','Саша','Глаша','Егор','Денис','Вася','Миша']
last_name = ['Анин(а)','Ванин(а)','Юлин(а)','Димин(а)','Сашин(а)','Глашин(а)','Егоин(а)',\
'Денисин(а)','Васяин(а)','Мишаин(а)']


kol_st = random.randint(10,20)

def named(lst,k):
    end_lst = []
    for i in range(k):
        ind = random.choice(lst)
        end_lst.append(ind)
    return end_lst

name_st = named(name,kol_st)
last_name = named(last_name,kol_st)

def univercity():
    for i in range(kol_st):
        in_out = False
        year_inside = random.randint(2010,2023)
        outside = year_inside + 5
        if outside > 2023:
            in_out = True

        if in_out == False:
            in_out = f'Выпустился в {year_inside + 5}'
        else:
            if year_inside == 2023:
                in_out = '1 курс'
            if year_inside == 2022:
                in_out = '2 курс'
            if year_inside == 2021:
                in_out = '3 курс'
            if year_inside == 2020:
                in_out = '4 курс'
            if year_inside == 2019:
                in_out = '5 курс'
        print(f'{i + 1} - {name_st[i]}, {last_name[i]}, {year_inside} - {in_out}')

univercity()
