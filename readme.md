# go-cli-template

Кравец М.А., 2025 г.

Версия 0.1

---

Шаблон проекта консольного приложения

## Установка линтера

``` shell
go get -u golang.org/x/lint/golint
```

## CLI. Команды

### Запуск локально

#### 1 Compiled GO

``` shell
make -B build
```

#### 2 Cli

``` shell
./bin/infotypecheck cli
```

### build the code

``` shell
make -B build
```

### test the code

``` shell
make test 
```

### check the vetting

``` shell
make vet
```

### check the linting

``` shell
make lint
```

### check the formatting

``` shell
make fmt 
```

### ensure everything passes and builds

``` shell
make 
```

