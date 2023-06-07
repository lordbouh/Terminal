#Linux terminal (GitBash) commands  

1) Посмотреть где я  
pwd  

2) Создать папку  
mkdir  
3) Зайти в папку  
cd foldername  

4) Создать 3 папки  
mkdir foldername1 foldername2 foldername3  

5) Зайти в любую папку  
cd foldername

6) Создать 5 файлов (3 txt, 2 json)  
touch 1.txt 2.txt 3.txt 4.json 5.json  

7) Создать 3 папки  
mkdir subfoldername_1 subfoldername_2 subfoldername_3  

8) Вывести список содержимого папки  
ls  

9) Открыть любой txt файл  
cat / vim редактор  

10) написать туда что-нибудь, любой текст.  
cat > filename с чистого листа;  
vim редактор  

11) сохранить и выйти.  
для cat ctrl+c; vim ctrl+c :wq;  

12) Выйти из папки на уровень выше  
cd ..  

13) переместить любые 2 файла, которые вы создали, в любую другую папку.  
mv foldername_source/filename foldername_destination    

14) скопировать любые 2 файла, которые вы создали, в любую другую папку.  
cp foldername_source/filename foldername_destination  

15) Найти файл по имени  
find -name filename  

16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает.  
head/tail/less filename | grep "required_text"  

17) вывести несколько первых строк из текстового файла  
head (default 10 lines)  

18) вывести несколько последних строк из текстового файла  
tail (default 10 lines)  

19) просмотреть содержимое длинного файла (команда less) изучите как она работает.  
less -N less.txt -> покажет # строк; -s удалить лишние пустые строчки  
утилиту less зачастую используют не для чтения текста, а для поиска определенных участков в больших документах.  
Если вам нужно найти то или иное слово, напечатайте в поле с мигающим курсором /текст (для поиска вниз по тексту)  
или ?текст (чтобы выполнить поиск less вверх по тексту)   
sed -n number_line_start , number_line_end +p filename  
sed -n 1,3p less.txt  

20) вывести дату и время  
date  
=========  

Задание *  
1) Отправить http запрос на сервер. http://162.55.220.72:5005/terminal-hw-request  
curl get http://162.55.220.72:5005/terminal-hw-request  

2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13
script -> chmod +x script  
#!/bin/bash  
#Testing script  
mkdir folder1  
cd folder1  
mkdir subfolder1 subfolder2 subfolder3  
cd subfolder1  
touch 1.txt 2.txt 3.txt 4.json 5.json  
mkdir ssf1 ssf2 ssf3  
ls -la  
mv 1.txt 2.txt ssf2  
