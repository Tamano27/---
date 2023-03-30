al_Eu =  'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
al_Ru = 'АБВГДЕЁЖЗИЙКЛМНОПРСТУФХЦЧШЩЪЫЬЭЮЯ'
sdvig = int(input('Шаг сдвига: '))
message= input("Сообщение для дешифровки: ").upper()
itog = ''
language = input('Выберите язык Ru/Eu: ')
if language == 'Ru':
    for i in message:
        mesto = al_Ru.find(i)
        new_mesto = mesto + sdvig
        if i in al_Ru:
            itog += al_Ru[new_mesto]
        else:
            itog += i
else:
    for i in message:
        mesto = al_Eu.find(i)
        new_mesto = mesto + sdvig
        if i in al_Eu:
            itog += al_Eu[new_mesto]
        else:
            itog += i
print (itog)

