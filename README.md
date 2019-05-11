# Консольный визуализатор машины Тьюринга

Работает на *Python 3*.

Для работы необходима библиотека *colorama*.
(Установить `pip3 install colorama`)

`visualizer.py machine input [delay]`
`machine` -- файл с описанием машины Тьюринга.
`input` -- файл с вводом.
`delay` -- опционально, задержка между тиками в секундах, по-умолчанию -- одна секунда.

Пример запуска:
`python3 visualizer.py example empty_input`
`python3 visualizer.py zero.out 01 0.5`

Во время работы, символом `^` показывает, где находится головка, пишет позицию головки, и пишет текущую вершину в автомате.

Для прерывания исполнения, нужно нажать q. Для паузы/продолжения, нужно нажать пробел.

Поддерживает формат одноленточной машины Тьюринга из лабы и формат многоленточной машины Тьюринга с одной лентой.

---

`gen.py` -- вспомогательный скрипт, который по файлу с описанием машины Тьюринга генерирует код на *Python 3*, который ее выводит.
`gen.py machine [name]`
 
`machine` -- файл с описанием машины Тьюринга.
`name` -- опционально, название задачи, если он не указан, за название задачи будет принято название файла с описанием.

Генерирует в той же папке, где находится файл с описанием, программу на *Python 3*, которая назвается `$name.py`, которая при запуске выводит в файл `$name.out` то, что находилось в файле `$machine`.

Пример запуска:
`python3 gen.py example helloworld`
`python3 gen.py zero/zero`