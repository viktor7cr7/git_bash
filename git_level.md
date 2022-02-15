 *     Задание 1.

1) Посмотреть где я -- `pwd`

2) Создать папку --  `mkdir test1`

3) Зайти в папку -- `cd test1`

4) Создать 3 папки -- `mkdir test2 test3 test4`

5) Зайти в любую папку -- `cd test2`

6) Создать 5 файлов (3 txt, 2 json) -- `touch file.txt file1.txt file2.txt name.json name1.json`

7) Создать 3 папки -- `mkdir class1 class2 class3`

8) Вывести список содержимого папки -- `ls -la`

9) +Открыть любой txt файл --  `vim file1.txt `

10) +написать туда что-нибудь, любой текст -- `ставим  "i" в редакторе  - для возможности написания текста `

11) +сохранить и выйти -- `Esc (сохранить данные) + Shift:wq `

12) Выйти из папки на уровень выше -- `cd ..`

13) Переместить любые 2 файла, которые вы создали, в любую другую папку -- `mv file1.txt file.txt class1`

14) скопировать любые 2 файла, которые вы создали, в любую другую папку -- `cp {file1.txt,file.txt} /d/flou/class2`


15) Найти файл по имени -- `find -name "file2.txt" `

16) Просмотреть содержимое в реальном времени (команда grep) изучите как она работает -- `tail -f file1.txt | grep о`

17) Вывести несколько первых строк из текстового файла --  `head -3 file2.txt`

18) вывести несколько последних строк из текстового файла -- ` tail -2 file2.txt`

19) просмотреть содержимое длинного файла (команда less) изучите как она работает -- `less file2.txt`

20) вывести дату и время -- ` date`     

*     Задание 2 

***Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13***

**`nano myscript.sh`**

``` 
#!/bin/bash

mkdir lesson

cd lesson

mkdir name name1 name2

cd name

touch file1.txt file2.txt file3.txt dvd.json dvd1.json

mkdir flou1 flou2 flou3

ls -la

mv file1.txt dvd.json flou1 
-----------------------------------------------------------------
Сохраняем скрипт ctrl + x + y + ent
```

    Задание 3 
Отправить http запрос на сервер.
http://162.55.220.72:5005/terminal-hw-request 

```
curl http://162.55.220.72:5005/terminal-hw-request 
```
Response :
``` 
Intro":"Hello!! This is your the first response from server","Tasks":{"Task_1":"Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)","result":["Your_String","Your_number"]}}
```

Request: 
```  
curl  "http://162.55.220.72:5005/get_method?name=Viktor&age=24"
```
Response : 
``` 
["Viktor","24"]
```