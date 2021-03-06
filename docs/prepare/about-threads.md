# О потоках

Сборочная система `make` может разбивать сборку на несколько потоков, число которых регулируется флагом `-j`. Рекомендуется использовать число потоков равное количеству потоков процессора или чуть больше. Чтобы параллельную сборку, нужно добавить для `make` переменную `-jN`, где `N` - число потоков вашего процессора.
Это можно сделать двумя способами:

- Указывать при каждом вызове `make` аргумент `-jN`
- Добавить переменую окружения `MAKEFLAGS`

Для того, чтобы узнать число потоков вашего ЦП, выполните:

```bash
lscpu | grep "CPU(s):"
```

Результат выполнения будет примерно следующий. Значения будут отличаться в зависимости от характеристик вашего процессора:

```
CPU(s):                          4
NUMA node0 CPU(s):               0-3
```

`CPU(s)` - кол-во потоков.

При желании добавьте соответствующую переменную окружения, заменив `N` на нужное значение:

```bash
echo "MAKEFLAGS=\"-jN\" " >> ~/.bashrc
```
