# Состав описания процесса установки пакета.

- Каталог - свойство `name` пакета. (каталог после распаковки)

## Порядок выполнения
 - `prepare` - подготовительные работы
 - `patch` - применение патчей
 - `configure` - настройка
 - `build` - сборка
 - `test` - тестирование
 - `install` - установка
 - `install-*` - специфичные файлы (применимо к любому шагу)
 - `postinstall` - действия после установки
 - `multi_prepare` - подготовительные работы
 - `multi_configure` - настройка
 - `multi_build` - сборка
 - `multi_test` - тестирование
 - `multi_install` - установка
 - `multi_postinstall` - действия после установки.