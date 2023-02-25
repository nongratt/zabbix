# Zabbix
How to up zabbix 

 - [Building monitoring](#Сборка-приложения-в-DOCKER-с-помощью-Jenkins-pipline)
   - [What](#what)
   - [Все о Zabbix](#Все-о-Zabbix)
     - [Основы Zabbix](#Теория-Zabbix)
     - [Архитектура](#Основые-компоненты)
   - [So, what is next ?](#So-,-what-is-next-?)
   - [Linux](#linux-bashzsh)
     - [Docker (with bash)](#Docker)
     - [Prometheus (with bash)](#Prometheus-NodeExporter)
     - [Grafana (with bash)](#Grafana)
     - [AlertManager (with bash)](#Alertmanager)
     - [Blackbox (with bash)](#BlackBox)
   - [Заключение](#Заключение)

## What

Prometheus — это бесплатное программное приложение, используемое для мониторинга и оповещения о событиях. Он записывает метрики в реальном времени в базу данных временных рядов, созданную с использованием модели извлечения HTTP, с гибкими запросами и оповещениями в реальном времени

## Все о Zabbix

### Теория Zabbix


### Основные компоненты


## So, what is next ?

## Linux bash/zsh

### Docker

```
Установка репозитория

sudo apt-get update #Обновляем состав устанолвенных пакетов 

sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
sudo mkdir -m 0755 -p /etc/apt/keyrings

curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg  #Ключ для работы с официальным репозиторием Docker  (дергаем из ранее созданной папки по пути  /etc/apt/keyrings)

 echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null     #Настройка репозитория

Установка DOCKER

sudo apt-get update

sudo chmod a+r /etc/apt/keyrings/docker.gpg

sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin  #Установка всего необходимо из ранее добавленного репозитория докер

sudo systemctl start docker #Запуск

sudo systemctl enable docker #Добавление в загрузчик 

```
### Prometheus NodeExporter

```

```

### Grafana

```

```
### Alertmanager

```

```
### BlackBox

```

```

## Заключение
