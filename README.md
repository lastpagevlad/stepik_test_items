# stepik_test_items
Мы хотим, чтобы разрабатываемый нами интернет-магазин работал одинаково хорошо для пользователей из любой страны. Чтобы убедиться в работоспособности решения с поддержкой разных языков, мы планируем запускать набор автотестов для каждого языка. Вам как разработчику автотестов нужно реализовать решение, которое позволит запускать автотесты для разных языков пользователей, передавая нужный язык в командной строке.

Создайте GitHub-репозиторий, в котором будут лежать файлы conftest.py и test_items.py.
Добавьте в файл conftest.py обработчик, который считывает из командной строки параметр language.
Реализуйте в файле conftest.py логику запуска браузера с указанным языком пользователя. Браузер должен объявляться в фикстуре browser и передаваться в тест как параметр.
В файл test_items.py напишите тест, который проверяет, что страница товара на сайте содержит кнопку добавления в корзину. Например, можно проверять товар, доступный по http://selenium1py.pythonanywhere.com/catalogue/coders-at-work_207/.
Тест должен запускаться с параметром language следующей командой:
pytest --language=es test_items.py
и проходить успешно. Достаточно, чтобы код работал только для браузера Сhrome.
Отправить ссылку на данный репозиторий в качестве ответа на данное задание.
Отправить решение на рецензирование другим учащимся. Не забудьте, что решение на рецензирование можно отправить только один раз.
Проверьте решения минимум трех других учащихся, чтобы получить баллы за задание.
Это задание с peer-review, поэтому кроме формальных критериев другие учащиеся могут проверять корректность написания вашего кода. 

Важно! Если при рецензировании чужого решения вы получаете ошибку вроде: 

raise ValueError("option names %s already added" % conflict)

ValueError: option names {'--language'} already added
Перепроверьте, что у вас нет своего conftest.py в директории выше, смотри шаг 4.

 

Ваше решение будет проверяться по следующим критериям:

Тест в репозитории можно запустить командой pytest --language=es, тест успешно проходит.
Проверка работоспособности кода для разных языков. Добавьте в файл с тестом команду time.sleep(30) сразу после открытия ссылки. Запустите тест с параметром --language=fr и визуально проверьте, что фраза на кнопке добавления в корзину выглядит так: "Ajouter au panier".
Браузер должен объявляться в фикстуре browser и передаваться в тест как параметр.
В тесте проверяется наличие кнопки добавления в корзину. Селектор кнопки является уникальным для проверяемой страницы. Есть assert.
Название тестового метода внутри файла test_items.py соответствует задаче. Название test_something не удовлетворяет требованиям.
