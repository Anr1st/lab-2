# Отчет по лабораторной работе №02

1. Создайте файл с расширением .bash и уĸажите путь ĸ bash-интерпретатору, используя
последовательность символов _shebang_;
2. Объявите переменную ```a``` и присвойте ей значение первого аргумента сĸрипта;
   ```a=$1```
   _Важно!_ Символ присваивания = не должен содержать пробелов.
3. Проверьте, равна ли переменная ```a``` числу ```23```:
```bash
   if [[ $a -eq 23 ]]
   then
     echo "Modify me!"
   else
     echo '$a is not "23"'
   fi
```
4. Запустите скрипт с одним аргументом. Удостоверьтесь, что все работает таĸ, ĸаĸ вы
запрограммировали.

## Задание лабораторной работы (вот только его и нужно включить в отчет!)

На основе изученного материала лабораторной работы, лекций (2 и 3), дополнительных источников напишите скрипт, который на вход принимает IPv4-адрес в десятичном формате, а на выходе обеспечивает данный IP-адрес в двоичном формате.

Пример входных данных:

```192.168.10.1```

Пример выходныx данных:

```11000000.10101000.00001010.00000001```

### Как успешно сдать работу?

Создать свой репозиторий из шаблона этого. Как это делается - "Use this template" -> "Create a new repository" и сделайте его public. 

Находясь уже в своем репозитории - создайте новый файл формата .md и там оформляйте отчет. В отчете опишите все шаги которые вы делали, чтобы получить финальный результат работы. Необходимы только скриншоты скрипта и примера его выполнения!

Что вам нужно знать, чтобы успешно защитить работу:

Переменные; как выполнять операции; условные конструкции; функции; циклы; как работать с массивом; как посмотреть права доступа к файлам; как выдавать права доступа; что такое и зачем нужен ip адрес и маска подсети.

## Дополнительные источники

1. [Присваивание значений переменным.](https://se.ifmo.ru/~ad/Documentation/ABS_Guide_ru.html#VARASSIGNMENT)
2. [Подстановка переменных.](https://se.ifmo.ru/~ad/Documentation/ABS_Guide_ru.html#VARSUBN)
3. [Арифметические операции.](https://se.ifmo.ru/~ad/Documentation/ABS_Guide_ru.html#ARITHEXP)
4. [Проверка условий.](https://se.ifmo.ru/~ad/Documentation/ABS_Guide_ru.html#TESTS)
5. stackoverflow.com
6. Хорошая ĸнига по Shell/bash в Linux - "Learn Linux Shell Scripting – Fundamentals of Bash 4.4" Sebastiaan
Tammer
7. [Функции.](https://se.ifmo.ru/~ad/Documentation/ABS_Guide_ru.html#FUNCTIONS)
8. [Функции и рекурсивные функции.](https://habr.com/ru/company/ruvds/blog/327248/)
9. [Циклы.](https://se.ifmo.ru/~ad/Documentation/ABS_Guide_ru.html#LOOPS)
10. [Массивы](https://se.ifmo.ru/~ad/Documentation/ABS_Guide_ru.html#ARRAYS)
11. [Про двоичную систему и IP-адрес](https://zametkinapolyah.ru/kompyuternye-seti/4-4-dvoichnye-chisla-i-dvoichnaya-sistema-schisleniya-perevod-chisla-v-dvoichnuyu-sistemu-schisleniya-iz-desyatichnoj.html)
12.  В. Олифер, Н. Олифер "Компьютерные сети. Принципы, технологии, протоколы. Учебник" (2016)
