---
title: Сведения о подсистеме Windows для Linux
description: Узнайте о подсистеме Windows для Linux, а также разных версиях и способах их использования.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
ms.date: 07/21/2020
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.localizationpriority: high
ms.openlocfilehash: 2b79473f620c39084bc9b7a385d4e16e3fe34d77
ms.sourcegitcommit: 69fc9d3ca22cf3f07622db4cdf80c8ec751fe620
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/19/2020
ms.locfileid: "90818676"
---
# <a name="what-is-the-windows-subsystem-for-linux"></a><span data-ttu-id="ea668-104">Что такое подсистема Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="ea668-104">What is the Windows Subsystem for Linux?</span></span>

<span data-ttu-id="ea668-105">Подсистема Windows для Linux позволяет разработчикам запускать среду GNU/Linux с большинством программ командной строки, служебных программ и приложений непосредственно в Windows без каких-либо изменений и необходимости использовать традиционную виртуальную машину или двойную загрузку.</span><span class="sxs-lookup"><span data-stu-id="ea668-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a traditional virtual machine or dualboot setup.</span></span>

<span data-ttu-id="ea668-106">Можно сделать следующее.</span><span class="sxs-lookup"><span data-stu-id="ea668-106">You can:</span></span>

* <span data-ttu-id="ea668-107">Выберите предпочтительные дистрибутивы GNU/Linux [из Microsoft Store](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="ea668-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
* <span data-ttu-id="ea668-108">Запускайте средства командной строки, например `grep`, `sed`, `awk`, или другие двоичные файлы ELF-64.</span><span class="sxs-lookup"><span data-stu-id="ea668-108">Run common command-line tools such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span>
* <span data-ttu-id="ea668-109">Запускайте сценарии Bash Shell и приложения командной строки GNU/Linux, включая:</span><span class="sxs-lookup"><span data-stu-id="ea668-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="ea668-110">инструменты: vim, emacs, tmux;</span><span class="sxs-lookup"><span data-stu-id="ea668-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="ea668-111">языки: [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# и F#, Rust, Go и пр.</span><span class="sxs-lookup"><span data-stu-id="ea668-111">Languages: [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="ea668-112">Службы. SSHD, [MySQL](./tutorials/wsl-database.md), Apache, lighttpd, [MongoDB](./tutorials/wsl-database.md), [PostgreSQL](./tutorials/wsl-database.md).</span><span class="sxs-lookup"><span data-stu-id="ea668-112">Services: SSHD, [MySQL](./tutorials/wsl-database.md), Apache, lighttpd, [MongoDB](./tutorials/wsl-database.md), [PostgreSQL](./tutorials/wsl-database.md).</span></span>
* <span data-ttu-id="ea668-113">Установите дополнительное программное обеспечение с помощью своего собственного диспетчера пакетов дистрибутивов GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="ea668-113">Install additional software using your own GNU/Linux distribution package manager.</span></span>
* <span data-ttu-id="ea668-114">Вызывайте приложения Windows с помощью оболочки командной строки, похожей на UNIX.</span><span class="sxs-lookup"><span data-stu-id="ea668-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
* <span data-ttu-id="ea668-115">Вызывайте приложения GNU/Linux в Windows.</span><span class="sxs-lookup"><span data-stu-id="ea668-115">Invoke GNU/Linux applications on Windows.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="ea668-116">Установка WSL</span><span class="sxs-lookup"><span data-stu-id="ea668-116">Install WSL</span></span>](install-win10.md)

<br>

> [!VIDEO https://www.youtube.com/embed/48k317kOxqg]

## <a name="what-is-wsl-2"></a><span data-ttu-id="ea668-117">Что такое WSL 2?</span><span class="sxs-lookup"><span data-stu-id="ea668-117">What is WSL 2?</span></span>

<span data-ttu-id="ea668-118">WSL 2 — это новая версия архитектуры подсистемы Windows для Linux, которая поддерживает подсистему Windows для Linux, чтобы запускать двоичные файлы Linux ELF64 в Windows.</span><span class="sxs-lookup"><span data-stu-id="ea668-118">WSL 2 is a new version of the Windows Subsystem for Linux architecture that powers the Windows Subsystem for Linux to run ELF64 Linux binaries on Windows.</span></span> <span data-ttu-id="ea668-119">Ее основными приоритетами является **увеличение производительности** файловой системы и добавление **полной совместимости системных вызовов**.</span><span class="sxs-lookup"><span data-stu-id="ea668-119">Its primary goals are to **increase file system performance**, as well as adding **full system call compatibility**.</span></span>

<span data-ttu-id="ea668-120">Эта новая архитектура изменяет способ взаимодействия этих двоичных файлов Linux с Windows и с оборудованием компьютера, но по-прежнему предоставляет то же взаимодействие с пользователем, что и WSL 1 (текущая общедоступная версия).</span><span class="sxs-lookup"><span data-stu-id="ea668-120">This new architecture changes how these Linux binaries interact with Windows and your computer's hardware, but still provides the same user experience as in WSL 1 (the current widely available version).</span></span>

<span data-ttu-id="ea668-121">Отдельные дистрибутивы Linux можно запускать с архитектурой WSL 1 или WSL 2.</span><span class="sxs-lookup"><span data-stu-id="ea668-121">Individual Linux distributions can be run with either the WSL 1 or WSL 2 architecture.</span></span> <span data-ttu-id="ea668-122">Каждый дистрибутив можно обновить или использовать на более старой версии в любое время, кроме того вы можете запустить дистрибутивы WSL 1 и WSL 2 параллельно.</span><span class="sxs-lookup"><span data-stu-id="ea668-122">Each distribution can be upgraded or downgraded at any time and you can run WSL 1 and WSL 2 distributions side by side.</span></span> <span data-ttu-id="ea668-123">WSL 2 использует совершенно новую архитектуру, которая дает преимущества от работы с реальным ядром Linux.</span><span class="sxs-lookup"><span data-stu-id="ea668-123">WSL 2 uses an entirely new architecture that benefits from running a real Linux kernel.</span></span>

<br>

> [!VIDEO https://www.youtube.com/embed/MrZolfGm8Zk]

## <a name="next-steps"></a><span data-ttu-id="ea668-124">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="ea668-124">Next steps</span></span>

* [<span data-ttu-id="ea668-125">Установка WSL 1 и обновление до WSL 2</span><span class="sxs-lookup"><span data-stu-id="ea668-125">Install WSL 1 and update to WSL 2</span></span>](./install-win10.md)

* [<span data-ttu-id="ea668-126">Сравнение WSL 2 и WSL 1</span><span class="sxs-lookup"><span data-stu-id="ea668-126">Compare WSL 2 and WSL 1</span></span>](./compare-versions.md)

* [<span data-ttu-id="ea668-127">Создание учетной записи пользователя и пароля для нового дистрибутива Linux</span><span class="sxs-lookup"><span data-stu-id="ea668-127">Create a user account and password for your new Linux distribution</span></span>](./user-support.md)

* [<span data-ttu-id="ea668-128">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="ea668-128">Read Frequently Asked Questions</span></span>](./faq.md)

* [<span data-ttu-id="ea668-129">Ознакомьтесь с часто задаваемыми вопросами о WSL 2</span><span class="sxs-lookup"><span data-stu-id="ea668-129">Read Frequently Asked Questions about WSL 2</span></span>](./wsl2-faq.md)

* [<span data-ttu-id="ea668-130">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="ea668-130">Troubleshooting</span></span>](./troubleshooting.md)

* [<span data-ttu-id="ea668-131">Выполнение команд взаимодействия между Windows и Linux</span><span class="sxs-lookup"><span data-stu-id="ea668-131">Run interoperability commands between Windows and Linux</span></span>](./interop.md)

* [<span data-ttu-id="ea668-132">Запуск команд и конфигураций запуска</span><span class="sxs-lookup"><span data-stu-id="ea668-132">Run launch commands and configurations</span></span>](./wsl-config.md)

* [<span data-ttu-id="ea668-133">Настройка разрешений для файлов</span><span class="sxs-lookup"><span data-stu-id="ea668-133">Set up file permissions</span></span>](./file-permissions.md)

* [<span data-ttu-id="ea668-134">Настройка WSL для предприятия</span><span class="sxs-lookup"><span data-stu-id="ea668-134">Set up WSL for Enterprise</span></span>](./enterprise.md)

* [<span data-ttu-id="ea668-135">Ссылки на команды WSL</span><span class="sxs-lookup"><span data-stu-id="ea668-135">Reference WSL commands</span></span>](./reference.md)

* [<span data-ttu-id="ea668-136">Создание пользовательских распределений</span><span class="sxs-lookup"><span data-stu-id="ea668-136">Build custom distributions</span></span>](./build-custom-distro.md)

* [<span data-ttu-id="ea668-137">Ознакомьтесь с заметками о выпуске WSL</span><span class="sxs-lookup"><span data-stu-id="ea668-137">Read the WSL Release Notes</span></span>](./release-notes.md)
