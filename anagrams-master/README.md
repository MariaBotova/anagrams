# Быстрый поиск анаграмм в словаре

## Установка

- `go get`
- `go run main.go`

## Описание эндпоинтов

### Получение версии приложения
```
curl --request GET \
  --url http://localhost:8080/
```

### Загружаем список анаграмм
```
curl --request POST \
  --url http://localhost:8080/load \
  --header 'content-type: application/json' \
  --data '["foobar", "aabb", "baba", "boofar", "test", null]'
```

### Получаем анаграммы слов
```
curl --request GET \
  --url 'http://localhost:8080/get?word=aabb'
```