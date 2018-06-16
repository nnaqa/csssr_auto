"# csssr_auto" 

Инструкция по запуску скрипта для windows:

1. Установка последней версии Python 3: https://www.python.org/downloads/
2. В переменные среды занести новую переменную и указать путь к python.exe
3. Запустить командную строку, перейти в каталог с python ..Python36\Scripts
4. Выполнить установку Selenium из командной строки, запустив команду "pip install selenium" 
    (http://selenium-python.readthedocs.io/installation.html)
5. Скачать последнюю версию ChromeDriver: http://chromedriver.chromium.org/downloads
6. В переменные среды занести новую переменную и указать путь к ChromeDriver
7. Скачать файл "monosnap_link_check", либо скопировать код и указать название с расширением ".py", например "csssr.py"
8. Запустить командную строку, перейти в каталог с файлом "csssr.py"
9. Выполнить команду "python csssr.py"
10. Запустится тест и октроется браузер Chrome
11. После некоторых действий в командной строке выйдет сообщение об ошибке:
    AssertionError

 
 
 Логика теста в csssr.py:
 Тест запускает браузер Chrome, переходит по ссылке 'http://blog.csssr.ru/qa-engineer/'
 Находит элемент: "НАХОДИТЬ НЕСОВЕРШЕНСТВА"
 Кликает по нему, затем ищет ссылку с текстом 'Софт для быстрого создания скриншотов'
 Ожидает, что она ведет по следующему адресу: 'http://monosnap.com/'
 Т.к. ссылка ведёт по адресу 'http://app.prntscr.com/ru/' - тест падает в ошибку
 Дефект найден.
