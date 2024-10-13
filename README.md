# Отчет по лабораторной работе №02

## Задание лабораторной работы 
Напишите скрипт, который на вход принимает IPv4-адрес в десятичном формате, а на выходе обеспечивает данный IP-адрес в двоичном формате.

Пример входных данных:

```192.168.10.1```

Пример выходныx данных:

```11000000.10101000.00001010.00000001```
## Ход работы
1. Итак, для начала создаю файл bash.script через команду touch и открываю для редактирования через команду gedit.
2. Далее пишу скрипт, сохраняю и закрываю файл.
   
 ![изображение](https://github.com/user-attachments/assets/e29cef28-2327-4892-a746-d4269e30c0e2)
 
4. Проверяем работу скрипта в терминале.

![изображение](https://github.com/user-attachments/assets/28409935-a434-49bc-a718-818247cb0ad3)

## Объяснение скрипта

#!/bin/bash - это shebang, что указывает операционной системе, какую программу использовать для выполнения скрипта (в данном случае, bash).

read -p "Введите IPv4-адрес в десятичном формате: " ip_address - эта команда запрашивает пользователя ввести IPv4-адрес в десятичном формате и сохраняет его в переменной ip_address.

IFS='.' read -r -a ip_array <<< "$ip_address" - эта команда разбивает введенный ip_address на отдельные элементы по разделителю ".", сохраняя каждый элемент в массиве ip_array.

binary="" - создается пустая строковая переменная binary, в которую будут записываться двоичные представления октетов IP-адреса.

for octet in "${ip_array[@]}" - начало цикла for, который перебирает каждый элемент массива ip_array (октеты IP-адреса).

do - начало блока цикла

binary+="$(printf "%08d" $(echo "obase=2; $octet" | bc))" - внутри цикла формируется двоичное представление каждого октета. Команда printf использует формат %08d для преобразования числа в двоичную запись с ведущими нулями до 8 позиций. Команда echo "obase=2; $octet" | bc используется для конвертации десятичного числа (октета) в двоичное с помощью утилиты bc (научного калькулятора).

binary+="." - добавляет точку в конец каждого октета для форматирования IP-адреса.

done - конец блока цикла.

![изображение](https://github.com/user-attachments/assets/1ad08f9d-65c8-4aad-b7dc-aaac375d5cd7)
- после завершения цикла, удаляется последний лишний символ (точка) из строки binary с помощью утилиты sed.

echo "IP-адрес $ip_address в двоичном формате: $binary" - выводится сообщение с исходным IP-адресом и его двоичным представлением.
