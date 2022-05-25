# Курсовая работа «Компьютерная проверка анаграмматичности русских поэтических текстов» («Anagramma in Verse, Computer Check»)

### В репозитории находятся 3 файла:
1. main.ipynb - препроцессинг текстов и тренировка модели, результаты сохраняются в базу данный (db-файл);
2. ph_kuc_baev.csv - частотное распределение фонем в речи, эмпирически найденное Генри Кучера (перевод в кириллицу, частоты парных мягких и твердых согласных объединены, ударение обозначено знаком "+"); 
3. data.db - база данных, содержащая результаты анализа: словарь из лемм и фонетического разбора этих лемм (таблица dictionary), 88 стихотворений и их авторы (таблица poems) собранные анаграммы 4 типов с 3 уровнями значимости: 0.1, 0.05, 0.01:
  +уровень значимости 0.1 - таблица anagrams
  +уровень значимости 0.05 - таблица anagrams_two
  +уровень значимости 0.01 - таблица anagrams_three

Четыре типа анаграмм:
  +полные анаграммы (учитываются все фонемы ключевого слова) - таблица anagrams
  +неполные анаграммы:
    -анаграммы без учета гласных - таблица anagrams_two
    -анаграммы без учета гласных и одной из согласных - таблица anagrams_three
    -анаграммы без учета одной фонемы

*Основные источники:*
1. В. С. Баевский, А. Д. Кошелев. Поэтика А. Блока: анаграммы // З. Г. Минц (ред.) *Ученые записки Тартуского ГУ* 459. Тарту: Тартуский государственный университет, 1979. С. 50–75.
2. H. Kučera. Entropy, redundancy and functional load in Russian and Czech // American Contr. to the 5th International Congress of Slavists 1. The Hague: Mouton, 1963. P. 191–218.
3. Малый академический словарь (Евгеньева А. П.). [Электронный ресурс]. URL: http://rus-yaz.niv.ru/doc/small-academic-vocabulary/index.htm (Дата обращения: 17.10.2021).

А также модули:
4. [ru_accent_poet](https://github.com/yuliya1324/ru_accent) - разметка ударения
5. [RusPhonetic](https://github.com/NyashniyVladya/RusPhonetic) - фонетический разбор 
