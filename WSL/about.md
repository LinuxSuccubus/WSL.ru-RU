---
title: Сведения о подсистеме Windows для Linux
description: Узнайте о подсистеме Windows для Linux, а также разных версиях и способах их использования.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
ms.date: 07/21/2020
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.localizationpriority: high
ms.openlocfilehash: 0c6fa3d0c5483a7ffd1fb95f13ca62666a7c1e72
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413085"
---
# <a name="what-is-the-windows-subsystem-for-linux"></a>Что такое подсистема Windows для Linux

Подсистема Windows для Linux позволяет разработчикам запускать среду GNU/Linux с большинством программ командной строки, служебных программ и приложений непосредственно в Windows без каких-либо изменений и необходимости использовать традиционную виртуальную машину или двойную загрузку.

Можно сделать следующее.

* Выберите предпочтительные дистрибутивы GNU/Linux [из Microsoft Store](https://aka.ms/wslstore).
* Запускайте средства командной строки, например `grep`, `sed`, `awk`, или другие двоичные файлы ELF-64.
* Запускайте сценарии Bash Shell и приложения командной строки GNU/Linux, включая:  
    * инструменты: vim, emacs, tmux;
    * языки: [NodeJS](/windows/nodejs/setup-on-wsl2), Javascript, [Python](/windows/python/web-frameworks), Ruby, C/C++, C# и F#, Rust, Go и пр.
    * Службы. SSHD, [MySQL](./tutorials/wsl-database.md), Apache, lighttpd, [MongoDB](./tutorials/wsl-database.md), [PostgreSQL](./tutorials/wsl-database.md).
* Установите дополнительное программное обеспечение с помощью своего собственного диспетчера пакетов дистрибутивов GNU/Linux.
* Вызывайте приложения Windows с помощью оболочки командной строки, похожей на UNIX.
* Вызывайте приложения GNU/Linux в Windows.

> [!div class="nextstepaction"]
> [Установка WSL](install-win10.md)

<br>

> [!VIDEO https://www.youtube.com/embed/48k317kOxqg]

## <a name="what-is-wsl-2"></a>Что такое WSL 2?

WSL 2 — это новая версия архитектуры подсистемы Windows для Linux, которая поддерживает подсистему Windows для Linux, чтобы запускать двоичные файлы Linux ELF64 в Windows. Ее основными приоритетами является **увеличение производительности** файловой системы и добавление **полной совместимости системных вызовов**.

Эта новая архитектура изменяет способ взаимодействия этих двоичных файлов Linux с Windows и с оборудованием компьютера, но по-прежнему предоставляет то же взаимодействие с пользователем, что и WSL 1 (текущая общедоступная версия).

Отдельные дистрибутивы Linux можно запускать с архитектурой WSL 1 или WSL 2. Каждый дистрибутив можно обновить или использовать на более старой версии в любое время, кроме того вы можете запустить дистрибутивы WSL 1 и WSL 2 параллельно. WSL 2 использует совершенно новую архитектуру, которая дает преимущества от работы с реальным ядром Linux.

<br>

> [!VIDEO https://www.youtube.com/embed/MrZolfGm8Zk]

## <a name="next-steps"></a>Дальнейшие действия

* [Установка WSL 1 и обновление до WSL 2](./install-win10.md)

* [Сравнение WSL 2 и WSL 1](./compare-versions.md)

* [Создание учетной записи пользователя и пароля для нового дистрибутива Linux](./user-support.md)

* [Часто задаваемые вопросы](./faq.md)

* [Ознакомьтесь с часто задаваемыми вопросами о WSL 2](./wsl2-faq.md)

* [Устранение неполадок](./troubleshooting.md)

* [Выполнение команд взаимодействия между Windows и Linux](./interop.md)

* [Запуск команд и конфигураций запуска](./wsl-config.md)

* [Настройка разрешений для файлов](./file-permissions.md)

* [Настройка WSL для предприятия](./enterprise.md)

* [Ссылки на команды WSL](./reference.md)

* [Создание пользовательских распределений](./build-custom-distro.md)

* [Ознакомьтесь с заметками о выпуске WSL](./release-notes.md)