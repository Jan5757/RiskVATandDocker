# Приложение для расчета риска. 
### Необходимо выявить объекты с рисками по следующему правилу: если разница сумм НДС за указанный период менее заданного значения (5000), то риск есть.
Исходные данные: две таблицы .tsv, расположенные в /app/db. 
Результат вычисления возвращается в виде файла response.json.

Инструкция для Windows

1. Установить Docker Desktop согласно инструкции (https://www.docker.com/)
2. Cоздать папку на локальном компьютере и клонировать репозиторий:
    ```
    ### git clone https://github.com/Jan5757/RiskVATandDocker.git
    ``` 
3. Открыть эту папку в командной строке и выполнить в ней
### docker-compose up
4. Проверить в Docker Desktop, что все контейнеры запустились. Если нет - перезапустить.
5. В Docker Desktop (или командной строке) перейти в терминал контейнера "master-1" и выполнить:
### jps
6. Проверить, что вывод содержит следующие значения:
    #### NameNode
    #### ResourceManager
    #### SecondaryNameNode
    #### Jps
    #### HistoryServer
    #### JobHistoryServer
    #### Master
Если что-то не запустилось, подождать (особенно Master)

7. Далее выполнить:
### cd app/quest
### java -jar questinspring.jar
8. Ждём результата
9. Проверяем результат в папке /app/quest/output


##### Ссылка на репозиторий, с которого взяты Hadoop, Hive, Spark контейнеры Docker (https://github.com/panovvv/bigdata-docker-compose)
