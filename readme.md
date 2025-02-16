# go-cli-template ![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white) 

Шаблон проекта консольного приложения с примением библиотеки [Cobra](https://github.com/spf13/cobra).

Структура проекта

```bash
├───Dockerfile
├───LICENSE
├───Makefile
├───bin
├───cmd
│       ├───cli.go
│       └───root.go
├───go.mod
├───go.sum
├───main.go
├───readme.md
└───vendor
        ├───github.com
        └───modules.txt
```

## Сборка и запуск приложения

### 1 Сборка приложения

- Linux

``` shell
go mod vendor
make -B build
```

- Windows

``` shell
go mod vendor
make -B buildWindows
```

### 2 Запуск cli-приложения

- Linux

``` shell
./bin/goclitmpl cli
```

- Windows

``` shell
./bin/goclitmpl.exe cli
```

### 3 Опции

- ```help```          глобальная справка

```bash
./bin/goclitmpl help
```

- ```cli```           консольное приложение

```bash
./bin/goclitmpl cli
```

- ```cli -h```        справка консольного приложения

```bash
./bin/goclitmpl cli -h
```

## Test the code

``` shell
make test 
```

## Check the vetting

``` shell
make vet
```

## Check the linting

- Linux

``` shell
make lint
```

## Check the formatting

- Linux

``` shell
make fmt 
```

## Everything passes and builds

- Linux

``` shell
make 
```

## Установка дополнительных пакетов и утилит

### Установка make

#### Windows

1. Откройте PowerShell от имени администратора
2. Вставьте следующую команду и нажмите Enter

```bash
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

3. Установка make с помощью Chocolatey

```bash
choco install make
```

4. Проверка установки

```bash
make -v
```

#### Ubuntu

1. Обновить все пакеты в системе с помощью команды

```bash
sudo apt update
```

2. Установите с помощью команды

```bash
sudo apt install make -y
```

3. Проверить установку

```bash
make -version
```

### Установка линтера

``` shell
go get -u golang.org/x/lint/golint
```
