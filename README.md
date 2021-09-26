# Курс основ программирования на МКН СПбГУ
## Проект 2: key-value база данных
### Иснтрукция по использованию

Комманды для работы с базой данных:

- content - выводит на экран содержимое базы данных в формате key -> value.
- insert key -> value - вставляет в базу данных пару (key, value)
- update key -> value - изменяет значение для поля key на value
- find key - находит значение для поля key
- findRegex pattern - находит все ключи (и значения для них) которых соответсвуют regex.
- erase key - удаляет поле key
- eraseRegex pattern - удаляет все поля для которых ключ соотвтсвует regex
- exit - выход
- save - сохраняет данные в файл
- clear - очищает базу данных
- rollback - откатывает последнюю команду

База данных шифруется после каждого сохранения. Для шифровки от пользователя требуется ключ. Ключ может отличаться 
при при каждом сохранении, главное, чтобы при входе ключ совпадал с тем, который был указан при сохранении.

Присутствует возможность запускать программу для работы с командами написанными в файле. Для этого требуется указать
опцию -f (или --file) в аргументах командной строки, затем имя файла с командами, и затем (не обязательно) имя файла
куда перенаправить вывод программы.

### Тестирование
Помимо модульного тестирования к отдельным фунциям присутствует несколько наборов входных данных в папке tests.
Для тестирования требуется указать в параметрах командной строки "-f tests/testN/input.txt tests/testN/output.txt", где
N - номер теста.