Я выполнял  вариант 4

4.Создать файл sh и bat, который выполняет следующее:
На вход пакетному файлу приходит число (как параметр пакетного файла). Если число не задано, то выводить сообщение в консоль “Параметр не задан”.
Создать файл 1.txt в него записать рандомные числа в количестве заданном параметром пакетного файла, каждое число на новой строке. Вывести сообщение “Рандомные числа созданы” в консоль

Код для git bush

#!/bin/bash

count=$1 

if [ -z "$count" ] 
then echo "Параметр не задан"
else 
touch 1.txt
for PROC in $(seq 1 $count)
do
	echo $RANDOM>> 1.txt 
done
echo Рандомные числа созданы 
fi


Код для командной строки windows

@echo off
setlocal enableDelayedExpansion
set /p %c="Enter number "
if NOT defined c (
  echo:undefined count  
) else (
for /L %%i in (1,1, %c%) do (
echo !random!  >> 1.txt
)
  echo:Random numbers created
)


 При выполнении этого задания я использовал условные операторы, цикл for, for, команду записи текста в файл, команду для генерации случайного числа