# go_cashe

Пакет, в котором реализован in-memory cache со следующими методами:

- `Set(key string, value interface{})` - запись значения `value` в кеш по ключу `key`
- `Get(key string)`
- `Delete(key)`

Пакет является импортируемой библиотекой, которую можно установить себе в проект с помощью `go get github.com/romixweb/go_cashe`

## ПРИМЕР #1

```package main

import (
	"fmt"

	cache "cache.go/InMemoryCache"
)

func main() {
	cache := cache.New()

	cache.Set("userId", "asdf")
	userId := cache.Get("userId")

	fmt.Println(userId)

	cache.Delete("userId")
	userId = cache.Get("userId")

	fmt.Println(userId)
}
```
