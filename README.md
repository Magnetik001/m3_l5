ans = 0
lst = []


while True:
    ans = input('Введите слово: ')
    if ans == '':
        break
    ans.strip()
    ans = ans.replace(' ','')
    lst.append(ans)
    print('Слово добавлено в список!')
    


def double(words):
    
    double_words = []
    singles_word = []
    end_lst = []
    for i in words:
        double_sym = []
        for j in i:
            if j not in double_sym:
                double_sym.append(j)
            else:
                if i not in double_words:
                    double_words.append(i)
    for i in words:
        if i not in double_words:
            singles_word.append(i)
    end_lst.append(double_words)
    end_lst.append(singles_word)
    return end_lst

print(double(lst))
