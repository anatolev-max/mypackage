# Внешние зависимости

## Задание 3

Есть модуль ```main```, состоящий из одного файла ```main.go```:

```
package main

import (
    "fmt"

    "yourpackage" // ваш пакет
)

func main() {
    if sum := yourpackage.Add(1, 2); sum != 3 {
        panic(fmt.Sprintf("sum expected to be 3; got %d", sum))
    }

    fmt.Println("Well done!")
}
```

Создайте собственный модуль и используйте его в данном примере вместо ```yourpackage```.

Для выполнения этого задания нужно:

1. Опубликовать на GitHub свой модуль, в котором определена функция ```func Add(a, b int) int```.
2. Создать файл ```main/go.mod```, где будут прописаны все необходимые зависимости.
3. Заменить строчку ```yourpackage``` на настоящий путь импорта созданного модуля.

```
// File: main/go.mod
module main

go 1.16

require (
    github.com/anatolev-max/mypackage latest
)
```
