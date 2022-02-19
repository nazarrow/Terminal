### GitBash, Terminal

#### Задание

1. Посмотреть где я:

   + `pwd`

2. Создать папку:

   + `mkdir folder`

   + `rm -r folder` (удалить папку с файлами)

3. Зайти в папку:

   + `cd folder`
  
4. Создать 3 папки:

   + `mkdir folder1 folder2 folder3`

   + или `mkdir folder{1..3}`
  
5. Зайти в любоую папку:

   + `cd folder`
  
6. Создать 5 файлов (3 txt, 2 json):

   + `touch file1.txt file2.txt file3.txt file1.json file2.json`
  
   + или `touch file{1..3}.txt file{1..2}.json`
  
7. Создать 3 папки:

   + `mkdir folder_1 folder_2 folder_3`

   + или `mkdir folder{1..3}`
  
8. Вывести список содержимого папки:

   + `ls -la` (вывод всех данных, в т.ч. скрытых)
  
9. Открыть любой txt файл:

   + `vim file1.txt`

10. Написать туда что-нибудь, любой текст:

    + нажать `"i"` (режим редактирования)

    + `ввести текст`

    + нажать `"esc"`
  
11. Сохранить и выйти:

    + `:wq`
  
12. Выйти из папки на уровень выше:

     + `cd ..`

     + `cd ../..` (выйти на 2 уровня выше)
  
13. Переместить любые 2 файла, которые вы создали, в любую другую папку:

    + `mv folder1/{file2.txt,file1.json} folder1/folder_1`
  
14. Скопировать любые 2 файла, которые вы создали, в любую другую папку:

    + `cp folder1/{file3.txt,file2.json} folder1/folder_2`
  
15. Найти файл по имени:

    + `find . -name "file1*"`
  
16. Просмотреть содержимое в реальном времени (команда grep) изучите как она работает:

    + `tail -f file1.txt | grep pattern` (редактируем, сохраняем и смотрим в текстовом редакторе)

    + `tail -f file1.txt | grep --line-buffered pattern >> 1_log.txt | tail -f 1_log.txt` (запись в файл с отображением в терминале)
  
17. Вывести несколько первых строк из текстового файла:

    + `head -3 file1.txt`
  
18. Вывести несколько последних строк из текстового файла:

    + `tail -3 file1.txt`
  
19. Просмотреть содержимое длинного файла (команда less) изучите как она работает:

    + `less file1.txt`

    + нажать `"q"`
  
20. Вывести дату и время:

    + `date`

#### Задание *

1. Отправить http запрос на сервер. `<http://162.55.220.72:5005/terminal-hw-request>`

    + `curl <http://162.55.220.72:5005/terminal-hw-request>`
  
Ответ:

{"Intro":"Hello!! This is your the first response from server","Tasks":{"Task_1":"Send the next URL in terminal: `<http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number>)","result":["Your_String","Your_number"]`}}

выполняем Task1:

+ `curl "<http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number>)"`

+ `(set_your_String) --> "Aleksei", (set_your_number) --> 28`
  
Ответ:

+ `["Aleksei","28"]`

1. Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

   + `cat > script.sh`

   + `vim script.sh`
  
   + нажать `"i"`

````bash

# !/bin/bash

pwd

mkdir folder_script

cd folder_script

mkdir folder1 folder2 folder3

cd folder3

touch {f1.txt,f2.txt,f3.txt,f4.json,f5.json}

mkdir script_folder1 script_folder2 script_folder3

ls -la

mv f1.txt f4.json script_folder2

./script.sh

````
