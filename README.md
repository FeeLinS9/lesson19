## Настройка PXE сервера для автоматической установки

### Цель:
Отрабатываем навыки установки и настройки DHCP, TFTP, PXE загрузчика и автоматической загрузки.
_____________________

В качестве образа для Vagrant я использовал `bento/centos-8.4`. Плюсом этого Vagrant Box является то, что по умолчанию он создаёт ОС с размером диска 60ГБ. При использовании данного образа нам не придётся подключать дополнительный диск.\
В качестве образа для установки с помощью PXE, рекомендуют использовать DVD(полную) версию дистрибутива. В этом задании, чтобы не качать DVD образ(12G), я указал boot образ(1G) и в файле ks.cfg изменил репозиторий на http://mirror.centos.org/centos/8-stream/BaseOS/x86_64/os/, так как в boot его нет. Также отдельно установил пакет syslinux, чтобы оттуда скопировать нужные файлы.
