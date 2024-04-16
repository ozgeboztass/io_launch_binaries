# IO-Net Official Binaries

Этот репозиторий содержит официальные двоичные файлы для io.net - Следуйте приведенным ниже инструкциям, чтобы установить и запустить двоичные файлы на соответствующей операционной системе.

## Предварительные условия

### Для Linux
- Docker
- Драйверы Nvidia (в случае GPU Worker) (запуск io-setup автоматически установит их, если это необходимо)
- Nvidia container toolkit (В случае GPU Worker) (запуск io-setup автоматически установит его, если необходимо)

### Для Mac
- Docker Desktop
 - [Download Docker Desktop for Mac](https://www.docker.com/products/docker-desktop/) - выберите для загрузки версию для mac - apple chip

## Установка

### Linux

1. **Выполните IO-Setup (один раз для оборудования)** (пропустите, если докер и драйверы Nvidia уже установлены и настроены).
 - Скачайте скрипт установки: 
```
 curl -L https://github.com/ionet-official/io-net-official-setup-script/raw/main/ionet-setup.sh -o ionet-setup.sh
 ```
 - Запустите скрипт:
 ```
 chmod +x ionet-setup.sh && ./ionet-setup.sh
 ```
 ##### Примечание - на случай, если команда curl не сработает: 
- Установите `curl`: 
```
 sudo apt install curl
 ```

2. **Для систем с графическими процессорами**.
 - Дождитесь перезапуска.
 - После перезапуска повторно запустите установку с помощью команды выше.

### Запуск контейнеров с помощью бинарных файлов

3. **Скачайте и запустите бинарник**:
 ```
 curl -L https://github.com/ionet-official/io_launch_binaries/raw/main/launch_binary_linux -o launch_binary_linux
 chmod +x launch_binary_linux
 ```

- Запустите в интерактивном режиме или скопируйте сгенерированную команду с сайта.
 ```
 ./launch_binary_linux
 ```


### Mac

- **Скачать и запустить двоичный файл**:
 ```
 curl -L https://github.com/ionet-official/io_launch_binaries/raw/main/launch_binary_mac -o launch_binary_mac
 chmod +x launch_binary_mac
 ```

- Запустите в интерактивном режиме или скопируйте сгенерированную команду с сайта.
 ```
 ./launch_binary_mac
 ```

- Поиск и устранение неисправностей (необязательно)

 - Если вы столкнулись с сообщением об ошибке типа ``неправильный тип процессора в исполняемом файле``, это, скорее всего, означает, что вы запускаете программное обеспечение, предназначенное для процессора Intel, на устройстве Apple Silicon. Чтобы решить эту проблему, вам нужно установить Rosetta 2, которая обеспечивает поддержку процессоров Intel для запуска в Docker на устройствах Apple Silicon.
 
```
 softwareupdate --install-rosetta
 ```

 - После завершения установки Rosetta повторно запустите команду excute.
 
```
 ./launch_binary_mac
 ```

<!-- ### Windows

1. **Скачать двоичный файл**:
- Зайдите в браузер и вставьте:
 ```
 wget https://github.com/ionet-official/io_launch_binaries/raw/main/launch_binary_windows
 ```
- Дважды щелкните по загруженному файлу и заполните данные в интерактивном режиме. -->


## Поддержка

Для получения поддержки, пожалуйста, откройте вопрос или свяжитесь с нашей командой поддержки на [discord](https://discord.gg/kqFzFK7fg2)
