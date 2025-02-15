# go-cli-template

Кравец М.А., 2025 г.

Версия 0.1

---

Шаблон проекта консольного приложения

## Установка линтера

``` shell
go get -u golang.org/x/lint/golint
```

## Установка make

### Windows

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

### Ubuntu

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

## CLI. Команды

### Запуск локально

#### 1 Compiled

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

#### 2 Cli

- Linux

``` shell
./bin/infotypecheck cli
```

- Windows

``` shell
./bin/infotypecheck.exe cli
```

### Build the code

``` shell
make -B build
```

### Test the code

``` shell
make test 
```

### Check the vetting

``` shell
make vet
```

### Check the linting

- Linux

``` shell
make lint
```

### Check the formatting

- Linux

``` shell
make fmt 
```

### Everything passes and builds

- Linux

``` shell
make 
```

