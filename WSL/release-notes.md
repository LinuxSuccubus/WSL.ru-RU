---
title: Заметки о выпуске подсистемы Windows для Linux
description: См. заметки о выпуске подсистемы Windows для Linux. Эти заметки о выпуске содержат исправленные проблемы и обновляются еженедельно.
keywords: заметки о выпуске, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: f79acbbc7f6436bae54c5160e769cababa76a341
ms.sourcegitcommit: 69fc9d3ca22cf3f07622db4cdf80c8ec751fe620
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/19/2020
ms.locfileid: "90818696"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="71c90-105">Заметки о выпуске подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="71c90-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-20211"></a><span data-ttu-id="71c90-106">Сборка 20211</span><span class="sxs-lookup"><span data-stu-id="71c90-106">Build 20211</span></span>
<span data-ttu-id="71c90-107">Общие сведения о сборке Windows 20211 доступны в [блоге о Windows](https://blogs.windows.com/windows-insider/2020/09/10/announcing-windows-10-insider-preview-build-20211/).</span><span class="sxs-lookup"><span data-stu-id="71c90-107">For general Windows information on build 20211 visit the [Windows blog](https://blogs.windows.com/windows-insider/2020/09/10/announcing-windows-10-insider-preview-build-20211/).</span></span>

* <span data-ttu-id="71c90-108">Представлена новая команда `wsl.exe --mount` для подключения физических или виртуальных дисков.</span><span class="sxs-lookup"><span data-stu-id="71c90-108">Introduce `wsl.exe --mount` for mounting physical or virtual disks.</span></span> <span data-ttu-id="71c90-109">Дополнительные сведения см. в статье [Доступ к файловым системам Linux в Windows и WSL 2](https://devblogs.microsoft.com/commandline/access-linux-filesystems-in-windows-and-wsl-2/).</span><span class="sxs-lookup"><span data-stu-id="71c90-109">For more information see [Access Linux filesystems in Windows and WSL 2](https://devblogs.microsoft.com/commandline/access-linux-filesystems-in-windows-and-wsl-2/).</span></span>
* <span data-ttu-id="71c90-110">Устранен сбой в службе LxssManager при проверке активности виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="71c90-110">Fix crash in LxssManager service when checking if the VM is idle.</span></span> <span data-ttu-id="71c90-111">[GH 5768]</span><span class="sxs-lookup"><span data-stu-id="71c90-111">[GH 5768]</span></span>
* <span data-ttu-id="71c90-112">Включена поддержка сжатых VHD-файлов.</span><span class="sxs-lookup"><span data-stu-id="71c90-112">Support for compressed VHD files.</span></span> <span data-ttu-id="71c90-113">[GH 4103]</span><span class="sxs-lookup"><span data-stu-id="71c90-113">[GH 4103]</span></span>
* <span data-ttu-id="71c90-114">Убедитесь, что библиотеки пользовательского режима Linux, установленные в c:\windows\system32\lxss\lib, сохраняются при обновлении ОС.</span><span class="sxs-lookup"><span data-stu-id="71c90-114">Ensure that Linux user mode libs installed to c:\windows\system32\lxss\lib are preserved across OS upgrade.</span></span> <span data-ttu-id="71c90-115">[GH 5848]</span><span class="sxs-lookup"><span data-stu-id="71c90-115">[GH 5848]</span></span>
* <span data-ttu-id="71c90-116">Включена возможность получить список дистрибутивов, доступных для установки, с помощью команды `wsl --install --list-distributions`.</span><span class="sxs-lookup"><span data-stu-id="71c90-116">Added the ability to list available distributions that can be installed with `wsl --install --list-distributions`.</span></span>
* <span data-ttu-id="71c90-117">Теперь, когда пользователь выходит из системы, работа экземпляров WSL завершается.</span><span class="sxs-lookup"><span data-stu-id="71c90-117">WSL instances are now terminated when the user logs off.</span></span>

## <a name="build-20190"></a><span data-ttu-id="71c90-118">Сборка 20190</span><span class="sxs-lookup"><span data-stu-id="71c90-118">Build 20190</span></span>
<span data-ttu-id="71c90-119">Общие сведения о сборке Windows 20190 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2020/08/12/announcing-windows-10-insider-preview-build-20190/).</span><span class="sxs-lookup"><span data-stu-id="71c90-119">For general Windows information on build 20190 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/08/12/announcing-windows-10-insider-preview-build-20190/).</span></span>

* <span data-ttu-id="71c90-120">Исправлена ошибка, препятствующая запуску экземпляров WSL 1.</span><span class="sxs-lookup"><span data-stu-id="71c90-120">Fix bug preventing WSL1 instances from launching.</span></span> <span data-ttu-id="71c90-121">[GH 5633]</span><span class="sxs-lookup"><span data-stu-id="71c90-121">[GH 5633]</span></span>
* <span data-ttu-id="71c90-122">Исправлена ошибка, приводившая к зависанию при перенаправлении выходных данных процесса Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-122">Fix hang when redirecting Windows process output.</span></span> <span data-ttu-id="71c90-123">[GH 5648]</span><span class="sxs-lookup"><span data-stu-id="71c90-123">[GH 5648]</span></span>
* <span data-ttu-id="71c90-124">Добавлен параметр %userprofile%\\.wslconfig для управления временем ожидания при простое виртуальной машины (wsl2.vmIdleTimeout=<время_в_миллисекундах>).</span><span class="sxs-lookup"><span data-stu-id="71c90-124">Add %userprofile%\\.wslconfig option to control the VM idle timeout (wsl2.vmIdleTimeout=<time_in_ms>).</span></span>
* <span data-ttu-id="71c90-125">Включена поддержка запуска псевдонимов выполнения приложений из WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-125">Support launching app execution aliases from WSL.</span></span>
* <span data-ttu-id="71c90-126">Включена поддержка установки ядра WSL2 и дистрибутивов с помощью команды wsl.exe --install.</span><span class="sxs-lookup"><span data-stu-id="71c90-126">Added support for installing the WSL2 kernel and distributions to wsl.exe --install.</span></span>

## <a name="build-20175"></a><span data-ttu-id="71c90-127">Сборка 20175</span><span class="sxs-lookup"><span data-stu-id="71c90-127">Build 20175</span></span>
<span data-ttu-id="71c90-128">Общие сведения о сборке Windows 20175 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2020/07/22/announcing-windows-10-insider-preview-build-20175/).</span><span class="sxs-lookup"><span data-stu-id="71c90-128">For general Windows information on build 20175 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/07/22/announcing-windows-10-insider-preview-build-20175/).</span></span>

* <span data-ttu-id="71c90-129">В качестве выделяемого по умолчанию объема памяти виртуальной машины WSL2 теперь используется 50 % от памяти узла или 8 ГБ в зависимости от того, что меньше [GH 4166].</span><span class="sxs-lookup"><span data-stu-id="71c90-129">Adjust default memory assignment of WSL2 VM to be 50% of host memory or 8GB, whichever is less [GH 4166].</span></span>
* <span data-ttu-id="71c90-130">Префикс \\\\wsl$ изменен на \\\\wsl для поддержки синтаксического анализа URI.</span><span class="sxs-lookup"><span data-stu-id="71c90-130">Change \\\\wsl$ prefix to \\\\wsl to support URI parsing.</span></span> <span data-ttu-id="71c90-131">Старый путь \\\\wsl$ по-прежнему поддерживается.</span><span class="sxs-lookup"><span data-stu-id="71c90-131">The old \\\\wsl$ path is still supported.</span></span>
* <span data-ttu-id="71c90-132">В архитектуре AMD64 вложенная виртуализация для WSL2 включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71c90-132">Enable nested virtualization for WSL2 by default on amd64.</span></span> <span data-ttu-id="71c90-133">Вы можете отключить ее с помощью команды %userprofile%\\.wslconfig ([wsl2] nestedVirtualization=false).</span><span class="sxs-lookup"><span data-stu-id="71c90-133">You can disable this via %userprofile%\\.wslconfig ([wsl2] nestedVirtualization=false).</span></span>
* <span data-ttu-id="71c90-134">По запросу wsl.exe --update запускается Центр обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="71c90-134">Make wsl.exe --update demand start Microsoft Update.</span></span>
* <span data-ttu-id="71c90-135">В DrvFs поддерживается переименование файлов, доступных только для чтения.</span><span class="sxs-lookup"><span data-stu-id="71c90-135">Support renaming over a read-only file in DrvFs.</span></span>
* <span data-ttu-id="71c90-136">Сообщения об ошибках всегда выводятся на правильной странице кода.</span><span class="sxs-lookup"><span data-stu-id="71c90-136">Ensure error messages are always printed in the correct codepage.</span></span>

## <a name="build-20150"></a><span data-ttu-id="71c90-137">Сборка 20150</span><span class="sxs-lookup"><span data-stu-id="71c90-137">Build 20150</span></span>
<span data-ttu-id="71c90-138">Общие сведения о сборке Windows 20150 см. в [блоге о Windows](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).</span><span class="sxs-lookup"><span data-stu-id="71c90-138">For general Windows information on build 20150 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).</span></span>

* <span data-ttu-id="71c90-139">Сведения о вычислениях GPU WSL2 см. в [блоге о Windows](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).</span><span class="sxs-lookup"><span data-stu-id="71c90-139">WSL2 GPU compute see [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/) for more information.</span></span>
* <span data-ttu-id="71c90-140">Добавлен параметр wsl.exe --install командной строки для быстрой настройки WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-140">Introduce wsl.exe --install command line option to easily set up WSL.</span></span>
* <span data-ttu-id="71c90-141">Добавлен параметр командной строки wsl.exe --update для управления обновлениями ядра WSL2.</span><span class="sxs-lookup"><span data-stu-id="71c90-141">Introduce wsl.exe --update command line option to manage updates to the WSL2 kernel.</span></span> 
* <span data-ttu-id="71c90-142">Используйте WSL2 в качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71c90-142">Set WSL2 as the default.</span></span>
* <span data-ttu-id="71c90-143">Увеличено время ожидания корректного завершения работы виртуальной машины WSL2.</span><span class="sxs-lookup"><span data-stu-id="71c90-143">Increase WSL2 vm graceful shutdown timeout.</span></span>
* <span data-ttu-id="71c90-144">Исправлено состояние гонки virtio-9p при сопоставлении памяти устройства.</span><span class="sxs-lookup"><span data-stu-id="71c90-144">Fix virtio-9p race condition when mapping device memory.</span></span>
* <span data-ttu-id="71c90-145">Не запускайте сервер 9p с повышенными привилегиями, если контроль учетных записей отключен.</span><span class="sxs-lookup"><span data-stu-id="71c90-145">Don't run an elevated 9p server if UAC is disabled.</span></span>

## <a name="build-19640"></a><span data-ttu-id="71c90-146">Сборка 19640</span><span class="sxs-lookup"><span data-stu-id="71c90-146">Build 19640</span></span>
<span data-ttu-id="71c90-147">Общие сведения о сборке Windows 19640 см. в [блоге о Windows](https://blogs.windows.com/windowsexperience/2020/06/03/announcing-windows-10-insider-preview-build-19640/).</span><span class="sxs-lookup"><span data-stu-id="71c90-147">For general Windows information on build 19640 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/03/announcing-windows-10-insider-preview-build-19640/).</span></span>

* <span data-ttu-id="71c90-148">[WSL2] Улучшения стабильности для virtio-9p (drvfs).</span><span class="sxs-lookup"><span data-stu-id="71c90-148">[WSL2] Stability improvements for virtio-9p (drvfs).</span></span>

## <a name="build-19555"></a><span data-ttu-id="71c90-149">Сборка 19555</span><span class="sxs-lookup"><span data-stu-id="71c90-149">Build 19555</span></span>
<span data-ttu-id="71c90-150">Общие сведения о сборке Windows 19555 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span><span class="sxs-lookup"><span data-stu-id="71c90-150">For general Windows information on build 19555 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span></span>

* <span data-ttu-id="71c90-151">[WSL2] Применение memory cgroup для ограничения объема памяти, используемой операциями установки и преобразования [GH 4669].</span><span class="sxs-lookup"><span data-stu-id="71c90-151">[WSL2] Use a memory cgroup to limit the amount of memory used by install and conversion operations [GH 4669]</span></span>
* <span data-ttu-id="71c90-152">Предоставление команды wsl.exe для улучшения обнаружения компонентов, если дополнительный компонент подсистемы Windows для Linux не включен.</span><span class="sxs-lookup"><span data-stu-id="71c90-152">Make wsl.exe present when the Windows Subsystem for Linux optional component is not enabled to improve feature discoverability.</span></span>
* <span data-ttu-id="71c90-153">Изменение wsl.exe для вывода текста справки, если дополнительный компонент WSL не установлен.</span><span class="sxs-lookup"><span data-stu-id="71c90-153">Change wsl.exe to print help text if the WSL optional component is not installed</span></span>
* <span data-ttu-id="71c90-154">Устранение состояния гонки при создании экземпляров.</span><span class="sxs-lookup"><span data-stu-id="71c90-154">Fix race condition when creating instances</span></span>
* <span data-ttu-id="71c90-155">Создание файла wslclient.dll, который содержит все функции командной строки.</span><span class="sxs-lookup"><span data-stu-id="71c90-155">Create wslclient.dll that contains all command line functionality</span></span>
* <span data-ttu-id="71c90-156">Предотвращение аварийного завершения при остановке службы LxssManagerUser.</span><span class="sxs-lookup"><span data-stu-id="71c90-156">Prevent crash during LxssManagerUser service stop</span></span>
* <span data-ttu-id="71c90-157">Исправление завершения работы wslapi.dll при первой ошибке, если значение параметра distroName равно NULL.</span><span class="sxs-lookup"><span data-stu-id="71c90-157">Fix wslapi.dll fast fail when distroName parameter is NULL</span></span>

## <a name="build-19041"></a><span data-ttu-id="71c90-158">Сборка 19041</span><span class="sxs-lookup"><span data-stu-id="71c90-158">Build 19041</span></span>
<span data-ttu-id="71c90-159">Общие сведения о сборке Windows 19041 см. в [блоге Windows](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span><span class="sxs-lookup"><span data-stu-id="71c90-159">For general Windows information on build 19041 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span></span>

* <span data-ttu-id="71c90-160">[WSL2] Очищение маски сигналов перед запуском процессов.</span><span class="sxs-lookup"><span data-stu-id="71c90-160">[WSL2] Clear the signal mask before launching the processes</span></span>
* <span data-ttu-id="71c90-161">[WSL2] Обновление ядра Linux до версии 4.19.84.</span><span class="sxs-lookup"><span data-stu-id="71c90-161">[WSL2] Update Linux kernel to 4.19.84</span></span>
* <span data-ttu-id="71c90-162">Обработка созданной символической ссылки /etc/resolv.conf, если символическая ссылка не является относительной.</span><span class="sxs-lookup"><span data-stu-id="71c90-162">Handle creation of /etc/resolv.conf symlink when the symlink is non-relative</span></span>

## <a name="build-19028"></a><span data-ttu-id="71c90-163">Сборка 19028</span><span class="sxs-lookup"><span data-stu-id="71c90-163">Build 19028</span></span>
<span data-ttu-id="71c90-164">Общие сведения о сборке Windows 19028 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span><span class="sxs-lookup"><span data-stu-id="71c90-164">For general Windows information on build 19028 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span></span>

* <span data-ttu-id="71c90-165">[WSL2] Ядро Linux обновлено до версии 4.19.81</span><span class="sxs-lookup"><span data-stu-id="71c90-165">[WSL2] Update Linux kernel to 4.19.81</span></span>
* <span data-ttu-id="71c90-166">[WSL2] Разрешение по умолчанию /dev/net/tun изменено на 0666 [GH 4629]</span><span class="sxs-lookup"><span data-stu-id="71c90-166">[WSL2] Change the default permission of /dev/net/tun to 0666 [GH 4629]</span></span>
* <span data-ttu-id="71c90-167">[WSL2] Объем памяти, назначенный виртуальной машине Linux по умолчанию, оптимизирован до 80 % памяти узла</span><span class="sxs-lookup"><span data-stu-id="71c90-167">[WSL2] Tweak default amount of memory assigned to Linux VM to be 80% of host memory</span></span>
* <span data-ttu-id="71c90-168">[WSL2] Внесены исправления в работу сервера взаимодействия для обработки запросов со временем ожидания, чтобы сервер не перестал отвечать на запросы из-за неправильных вызовов</span><span class="sxs-lookup"><span data-stu-id="71c90-168">[WSL2] fix interop server to handle requests with a timeout so bad callers cannot hang the server</span></span>

## <a name="build-19018"></a><span data-ttu-id="71c90-169">Сборка 19018</span><span class="sxs-lookup"><span data-stu-id="71c90-169">Build 19018</span></span>
<span data-ttu-id="71c90-170">Общие сведения о сборке Windows 19018 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span><span class="sxs-lookup"><span data-stu-id="71c90-170">For general Windows information on build 19018 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span></span>

* <span data-ttu-id="71c90-171">[WSL2] Для исправления неполадок с приложениями .NET по умолчанию используется параметр cache=mmap для подключения ресурсов 9p.</span><span class="sxs-lookup"><span data-stu-id="71c90-171">[WSL2] Use cache=mmap as the default for 9p mounts to fix dotnet apps</span></span>
* <span data-ttu-id="71c90-172">[WSL2] Исправления для ретранслятора localhost [GH 4340].</span><span class="sxs-lookup"><span data-stu-id="71c90-172">[WSL2] Fixes for localhost relay [GH 4340]</span></span>
* <span data-ttu-id="71c90-173">[WSL2] Добавлен подключаемый общедоступный ресурс tmpfs для передачи состояний между дистрибутивами.</span><span class="sxs-lookup"><span data-stu-id="71c90-173">[WSL2] Introduce a cross-distro shared tmpfs mount for sharing state between distros</span></span>
* <span data-ttu-id="71c90-174">Исправлено восстановление постоянного сетевого диска для \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="71c90-174">Fix restoring persistent network drive for \\\\wsl$</span></span>

## <a name="build-19013"></a><span data-ttu-id="71c90-175">Сборка 19013</span><span class="sxs-lookup"><span data-stu-id="71c90-175">Build 19013</span></span>
<span data-ttu-id="71c90-176">Общие сведения о сборке Windows 19013 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span><span class="sxs-lookup"><span data-stu-id="71c90-176">For general Windows information on build 19013 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span></span>

* <span data-ttu-id="71c90-177">[WSL2] Повышение производительности памяти служебной виртуальной машины WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-177">[WSL2] Improve memory performance of WSL utility VM.</span></span> <span data-ttu-id="71c90-178">Память, которая больше не используется, будет освобождена для узла.</span><span class="sxs-lookup"><span data-stu-id="71c90-178">Memory that is no longer in use will be freed back to the host.</span></span>
* <span data-ttu-id="71c90-179">[WSL2] Ядро обновлено до версии 4.19.79.</span><span class="sxs-lookup"><span data-stu-id="71c90-179">[WSL2] Update kernel version to 4.19.79.</span></span> <span data-ttu-id="71c90-180">(Добавлены модули CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK и CONFIG_BRIDGE_VLAN_FILTERING.)</span><span class="sxs-lookup"><span data-stu-id="71c90-180">(add CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK, and CONFIG_BRIDGE_VLAN_FILTERING).</span></span>
* <span data-ttu-id="71c90-181">[WSL2] Исправлен ретранслятор ввода для обработки ситуаций, когда STDIN является незакрытым обработчиком канала [GH 4424].</span><span class="sxs-lookup"><span data-stu-id="71c90-181">[WSL2] Fix input relay to handle cases where stdin is a pipe handle that is not closed [GH 4424]</span></span>
* <span data-ttu-id="71c90-182">При проверке наличия \\\\wsl$ не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="71c90-182">Make the check for \\\\wsl$ case-insensitive.</span></span>
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a><span data-ttu-id="71c90-183">Сборка 19002</span><span class="sxs-lookup"><span data-stu-id="71c90-183">Build 19002</span></span>
<span data-ttu-id="71c90-184">Общие сведения о сборке Windows 19002 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span><span class="sxs-lookup"><span data-stu-id="71c90-184">For general Windows information on build 19002 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span></span>

* <span data-ttu-id="71c90-185">[WSL] Устранена проблема с обработкой некоторых знаков Юникода: https://github.com/microsoft/terminal/issues/2770</span><span class="sxs-lookup"><span data-stu-id="71c90-185">[WSL] Fix issue with handling of some Unicode characters: https://github.com/microsoft/terminal/issues/2770</span></span>
* <span data-ttu-id="71c90-186">[WSL] Исправлена редко возникавшая проблема, приводившая к отмене регистрации дистрибутива, если он запускался сразу после обновления сборки новой сборкой.</span><span class="sxs-lookup"><span data-stu-id="71c90-186">[WSL] Fix rare cases where distros could be unregistered if launched immediately after a build-to-build upgrade.</span></span>
* <span data-ttu-id="71c90-187">[WSL] Устранена незначительная проблема с wsl.exe --shutdown, из-за которой таймеры бездействия экземпляра не отменялись.</span><span class="sxs-lookup"><span data-stu-id="71c90-187">[WSL] Fix minor issue with wsl.exe --shutdown where instance idle timers were not cancelled.</span></span>

## <a name="build-18995"></a><span data-ttu-id="71c90-188">Сборка 18995</span><span class="sxs-lookup"><span data-stu-id="71c90-188">Build 18995</span></span>
<span data-ttu-id="71c90-189">Общие сведения о сборке Windows 18995 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span><span class="sxs-lookup"><span data-stu-id="71c90-189">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="71c90-190">[WSL2] Устранена проблема, из-за которой подключения DrvFs прекращали работать после прерывания операции (например, нажатия клавиш CTRL+C) [GH 4377].</span><span class="sxs-lookup"><span data-stu-id="71c90-190">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="71c90-191">[WSL2] Исправлена обработка очень больших сообщений hvsocket [GH 4105].</span><span class="sxs-lookup"><span data-stu-id="71c90-191">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="71c90-192">[WSL2] Устранена проблема с взаимодействием, возникавшая, если в качестве stdin использовался файл [GH 4475].</span><span class="sxs-lookup"><span data-stu-id="71c90-192">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="71c90-193">[WSL2] Устранено аварийное завершение службы при обнаружении непредвиденного состояния сети [GH 4474].</span><span class="sxs-lookup"><span data-stu-id="71c90-193">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="71c90-194">[WSL2] Запрос имени дистрибутива с сервера взаимодействия, если текущий процесс не имеет переменной среды.</span><span class="sxs-lookup"><span data-stu-id="71c90-194">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="71c90-195">[WSL2] Устранена проблема с взаимодействием, возникавшая, если в качестве stdin использовался файл.</span><span class="sxs-lookup"><span data-stu-id="71c90-195">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="71c90-196">[WSL2] Ядро Linux обновлено до версии 4.19.72.</span><span class="sxs-lookup"><span data-stu-id="71c90-196">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="71c90-197">[WSL2] Добавлена возможность указать дополнительные параметры командной строки ядра с помощью wslconfig.</span><span class="sxs-lookup"><span data-stu-id="71c90-197">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a><span data-ttu-id="71c90-198">Сборка 18990</span><span class="sxs-lookup"><span data-stu-id="71c90-198">Build 18990</span></span>
<span data-ttu-id="71c90-199">Общие сведения о сборке Windows 18990 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span><span class="sxs-lookup"><span data-stu-id="71c90-199">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="71c90-200">Ускорен вывод списка каталогов в \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="71c90-200">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="71c90-201">[WSL2] Внедрена дополнительная энтропия загрузки [GH 4416].</span><span class="sxs-lookup"><span data-stu-id="71c90-201">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="71c90-202">[WSL2] Исправлено взаимодействие с Windows при использовании su или sudo [GH 4465].</span><span class="sxs-lookup"><span data-stu-id="71c90-202">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>

## <a name="build-18980"></a><span data-ttu-id="71c90-203">Сборка 18980</span><span class="sxs-lookup"><span data-stu-id="71c90-203">Build 18980</span></span>
<span data-ttu-id="71c90-204">Общие сведения о сборке Windows 18980 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span><span class="sxs-lookup"><span data-stu-id="71c90-204">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="71c90-205">Исправлено чтение символических ссылок, которые запрещают FILE_READ_DATA.</span><span class="sxs-lookup"><span data-stu-id="71c90-205">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="71c90-206">Сюда входят все символические ссылки Windows, создаваемые для обеспечения обратной совместимости, такие как "C:\Document and Settings", а также множество символических ссылок в каталоге профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="71c90-206">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="71c90-207">Непредвиденное состояние файловой системы перестало быть неустранимым [GH 4334, 4305].</span><span class="sxs-lookup"><span data-stu-id="71c90-207">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="71c90-208">[WSL2] Добавлена поддержка arm64, если ЦП или встроенное ПО поддерживает виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="71c90-208">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="71c90-209">[WSL2] Непривилегированным пользователям разрешено просматривать журнал ядра.</span><span class="sxs-lookup"><span data-stu-id="71c90-209">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="71c90-210">[WSL2] Исправлена ретрансляция вывода при закрытии сокетов stdout и stderr [GH 4375].</span><span class="sxs-lookup"><span data-stu-id="71c90-210">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="71c90-211">[WSL2] Поддержка сквозного режима батареи и адаптера питания.</span><span class="sxs-lookup"><span data-stu-id="71c90-211">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="71c90-212">[WSL2] Ядро Linux обновлено до версии 4.19.67.</span><span class="sxs-lookup"><span data-stu-id="71c90-212">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="71c90-213">Добавлена возможность задать имя пользователя по умолчанию в /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="71c90-213">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="71c90-214">Сборка 18975</span><span class="sxs-lookup"><span data-stu-id="71c90-214">Build 18975</span></span>
<span data-ttu-id="71c90-215">Общие сведения о сборке Windows 18975 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span><span class="sxs-lookup"><span data-stu-id="71c90-215">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="71c90-216">[WSL2] Исправлен ряд проблем с надежностью localhost [GH 4340].</span><span class="sxs-lookup"><span data-stu-id="71c90-216">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="71c90-217">Сборка 18970</span><span class="sxs-lookup"><span data-stu-id="71c90-217">Build 18970</span></span>
<span data-ttu-id="71c90-218">Общие сведения о сборке Windows 18970 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span><span class="sxs-lookup"><span data-stu-id="71c90-218">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="71c90-219">[WSL2] Синхронизация времени с временем узла при выходе системы из спящего режима [GH 4245].</span><span class="sxs-lookup"><span data-stu-id="71c90-219">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="71c90-220">[WSL2] Создание символических ссылок NT на тома Windows, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="71c90-220">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="71c90-221">[WSL2] Создание дистрибутивов в пространствах имен UTS, IPC, PID и Mount.</span><span class="sxs-lookup"><span data-stu-id="71c90-221">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="71c90-222">[WSL2] Исправлена ретрансляция портов localhost при привязке сервера к localhost напрямую [GH 4353].</span><span class="sxs-lookup"><span data-stu-id="71c90-222">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="71c90-223">[WSL2] Исправлено взаимодействие при перенаправлении вывода [GH 4337].</span><span class="sxs-lookup"><span data-stu-id="71c90-223">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="71c90-224">[WSL2] Поддержка преобразования абсолютных символических ссылок NT.</span><span class="sxs-lookup"><span data-stu-id="71c90-224">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="71c90-225">[WSL2] Ядро обновлено до версии 4.19.59.</span><span class="sxs-lookup"><span data-stu-id="71c90-225">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="71c90-226">[WSL2] Правильное задание маски подсети для eth0.</span><span class="sxs-lookup"><span data-stu-id="71c90-226">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="71c90-227">[WSL2] Изменение логики для выхода из циклов консольного рабочего процесса при получении сигнала о событии выхода.</span><span class="sxs-lookup"><span data-stu-id="71c90-227">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="71c90-228">[WSL2] Если дистрибутив не работает, то его VHD-файл можно извлечь.</span><span class="sxs-lookup"><span data-stu-id="71c90-228">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="71c90-229">[WSL2] Исправлена библиотека анализа конфигурации, чтобы правильно обрабатывать пустые значения.</span><span class="sxs-lookup"><span data-stu-id="71c90-229">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="71c90-230">[WSL2] Поддержка рабочего стола Docker путем создания подключений между дистрибутивами.</span><span class="sxs-lookup"><span data-stu-id="71c90-230">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="71c90-231">Дистрибутив можно настроить для такого режима, добавив следующую строку в файл /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="71c90-231">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="71c90-232">Сборка 18945</span><span class="sxs-lookup"><span data-stu-id="71c90-232">Build 18945</span></span>
<span data-ttu-id="71c90-233">Общие сведения о сборке Windows 18945 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span><span class="sxs-lookup"><span data-stu-id="71c90-233">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-234">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-234">WSL</span></span>
* <span data-ttu-id="71c90-235">[WSL2] Разрешен доступ к ожидающим передачи данных TCP-сокетам в WSL2 с узла по адресу localhost:<порт>.</span><span class="sxs-lookup"><span data-stu-id="71c90-235">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="71c90-236">[WSL2] Устранены сбои при установке и преобразовании. Добавлена дополнительная диагностика для отслеживания будущих проблем [GH 4105].</span><span class="sxs-lookup"><span data-stu-id="71c90-236">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="71c90-237">[WSL2] Улучшена диагностируемость проблем с сетью WSL2.</span><span class="sxs-lookup"><span data-stu-id="71c90-237">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="71c90-238">[WSL2] Ядро обновлено до версии 4.19.55.</span><span class="sxs-lookup"><span data-stu-id="71c90-238">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="71c90-239">[WSL2] Ядро обновлено с помощью параметров конфигурации, необходимых для Docker [GH 4165].</span><span class="sxs-lookup"><span data-stu-id="71c90-239">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="71c90-240">[WSL2] Увеличено число ЦП, назначаемых упрощенной служебной виртуальной машине, чтобы оно совпадало с числом ЦП узла (ранее это значение было ограничено 8 ЦП с помощью параметра CONFIG_NR_CPUS в конфигурации ядра) [GH 4137].</span><span class="sxs-lookup"><span data-stu-id="71c90-240">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="71c90-241">[WSL2] Создание файла подкачки для упрощенной виртуальной машины WSL2.</span><span class="sxs-lookup"><span data-stu-id="71c90-241">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="71c90-242">[WSL2] Разрешено отображение подключений пользователей в \\\\wsl$\\<имя_дистрибутива> (например, sshfs) [GH 4172].</span><span class="sxs-lookup"><span data-stu-id="71c90-242">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="71c90-243">[WSL2] Повышена производительность файловой системы 9p.</span><span class="sxs-lookup"><span data-stu-id="71c90-243">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="71c90-244">[WSL2] Предотвращение неограниченного роста списка ACL виртуального жесткого диска [GH 4126].</span><span class="sxs-lookup"><span data-stu-id="71c90-244">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="71c90-245">[WSL2] Обновлена конфигурации ядра для поддержки squashfs и xt_conntrack [GH 4107, 4123].</span><span class="sxs-lookup"><span data-stu-id="71c90-245">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="71c90-246">[WSL2] Исправлен параметр interop.enabled в /etc/wsl.conf [GH 4140].</span><span class="sxs-lookup"><span data-stu-id="71c90-246">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="71c90-247">[WSL2] Если файловая система не поддерживает EA, возвращается ENOTSUP.</span><span class="sxs-lookup"><span data-stu-id="71c90-247">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="71c90-248">[WSL2] CopyFile больше не прекращает отвечать на запросы при работе с \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="71c90-248">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="71c90-249">Параметр umask по умолчанию переключен на значение 0022, и добавлен параметр filesystem.umask в /etc/wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="71c90-249">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="71c90-250">Исправлен wslpath, чтобы правильно разрешать символические ссылки, что повторно происходило в 19h1 [GH 4078].</span><span class="sxs-lookup"><span data-stu-id="71c90-250">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="71c90-251">Введен файл %UserProfile%\\.wslconfig для настройки параметров WSL2.</span><span class="sxs-lookup"><span data-stu-id="71c90-251">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a><span data-ttu-id="71c90-252">Сборка 18917</span><span class="sxs-lookup"><span data-stu-id="71c90-252">Build 18917</span></span>
<span data-ttu-id="71c90-253">Общие сведения о сборке Windows 18917 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="71c90-253">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-254">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-254">WSL</span></span>
* <span data-ttu-id="71c90-255">Уже доступна версия WSL 2!</span><span class="sxs-lookup"><span data-stu-id="71c90-255">WSL 2 is now available!</span></span> <span data-ttu-id="71c90-256">Дополнительные сведения см. в [блоге](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/).</span><span class="sxs-lookup"><span data-stu-id="71c90-256">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="71c90-257">Устранена регрессия, из-за которой запуск процессов Windows через символические ссылки выполнялся некорректно [GH 3999].</span><span class="sxs-lookup"><span data-stu-id="71c90-257">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="71c90-258">Добавлены следующие параметры wsl.exe: wsl.exe --list --verbose, wsl.exe --list --quiet и wsl.exe --import --version.</span><span class="sxs-lookup"><span data-stu-id="71c90-258">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="71c90-259">Добавлен параметр wsl.exe --shutdown.</span><span class="sxs-lookup"><span data-stu-id="71c90-259">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="71c90-260">Plan 9: для успешной работы разрешено открытие каталога для записи.</span><span class="sxs-lookup"><span data-stu-id="71c90-260">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="71c90-261">Сборка 18890</span><span class="sxs-lookup"><span data-stu-id="71c90-261">Build 18890</span></span>
<span data-ttu-id="71c90-262">Общие сведения о сборке Windows 18890 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="71c90-262">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-263">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-263">WSL</span></span>
* <span data-ttu-id="71c90-264">Утечка сокетов не блокирует работу [GH 2913].</span><span class="sxs-lookup"><span data-stu-id="71c90-264">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="71c90-265">Ввод EOF в терминал может заблокировать последующие операции чтения [GH 3421].</span><span class="sxs-lookup"><span data-stu-id="71c90-265">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="71c90-266">В заголовок resolv.conf добавлена ссылка на wsl.conf [рассмотрено в GH 3928].</span><span class="sxs-lookup"><span data-stu-id="71c90-266">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="71c90-267">Взаимоблокировка в коде epoll delete [GH 3922].</span><span class="sxs-lookup"><span data-stu-id="71c90-267">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="71c90-268">Обработка пробелов в аргументах параметров --import и --export [GH 3932].</span><span class="sxs-lookup"><span data-stu-id="71c90-268">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="71c90-269">Расширение файлов, обработанных с помощью mmap, не работает должным образом [GH 3939].</span><span class="sxs-lookup"><span data-stu-id="71c90-269">Extending mmap'd files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="71c90-270">Устранена проблема с доступом ARM64 к \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="71c90-270">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="71c90-271">Улучшен значок по умолчанию для wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="71c90-271">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="71c90-272">Сборка 18342</span><span class="sxs-lookup"><span data-stu-id="71c90-272">Build 18342</span></span>
<span data-ttu-id="71c90-273">Общие сведения о сборке Windows 18342 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="71c90-273">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-274">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-274">WSL</span></span>
* <span data-ttu-id="71c90-275">Мы добавили возможность доступа пользователей к файлам Linux в дистрибутиве WSL из Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-275">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="71c90-276">Доступ к этим файлам можно получить с помощью командной строки. Кроме того, такие приложения для Windows, как проводник, VSCode и т. д., могут взаимодействовать с этими файлами.</span><span class="sxs-lookup"><span data-stu-id="71c90-276">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="71c90-277">Чтобы получить доступ к файлам, перейдите в папку \\\\wsl$\\<имя_дистрибутива>, или просмотрите список выполняющихся дистрибутивов, перейдя в \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="71c90-277">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="71c90-278">Добавлены дополнительные теги сведений о ЦП и исправлены значения Cpus_allowed[_list] [GH 2234].</span><span class="sxs-lookup"><span data-stu-id="71c90-278">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="71c90-279">Поддержка выполнения из ведомого потока [GH 3800].</span><span class="sxs-lookup"><span data-stu-id="71c90-279">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="71c90-280">Ошибки обновления конфигурации не считаются критическими [GH 3785].</span><span class="sxs-lookup"><span data-stu-id="71c90-280">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="71c90-281">Подсистема binfmt обновлена для правильной обработки смещений [GH 3768].</span><span class="sxs-lookup"><span data-stu-id="71c90-281">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="71c90-282">Включено сопоставление сетевых дисков для Plan 9 [GH 3854].</span><span class="sxs-lookup"><span data-stu-id="71c90-282">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="71c90-283">Поддержка преобразования путей Windows в Linux и наоборот для подключения привязок.</span><span class="sxs-lookup"><span data-stu-id="71c90-283">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="71c90-284">Создание разделов только для чтения для сопоставлений файлов, открытых только для чтения.</span><span class="sxs-lookup"><span data-stu-id="71c90-284">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="71c90-285">Сборка 18334</span><span class="sxs-lookup"><span data-stu-id="71c90-285">Build 18334</span></span>
<span data-ttu-id="71c90-286">Общие сведения о сборке Windows 18334 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="71c90-286">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-287">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-287">WSL</span></span>
* <span data-ttu-id="71c90-288">Перепроектирован способ сопоставления часового пояса Windows с часовым поясом Linux [GH 3747].</span><span class="sxs-lookup"><span data-stu-id="71c90-288">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="71c90-289">Устранены утечки памяти и добавлены новые функции преобразования строк [GH 3746].</span><span class="sxs-lookup"><span data-stu-id="71c90-289">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="71c90-290">Выполнение SIGCONT для группы потоков без потоков является холостой командой [GH 3741].</span><span class="sxs-lookup"><span data-stu-id="71c90-290">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="71c90-291">Правильное отображение дескрипторов файлов socket и epoll в /proc/self/fd.</span><span class="sxs-lookup"><span data-stu-id="71c90-291">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="71c90-292">Сборка 18305</span><span class="sxs-lookup"><span data-stu-id="71c90-292">Build 18305</span></span>
<span data-ttu-id="71c90-293">Общие сведения о сборке Windows 18305 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="71c90-293">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-294">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-294">WSL</span></span>
* <span data-ttu-id="71c90-295">Когда основной поток завершает работу, pthreads утрачивает доступ к файлам [GH 3589].</span><span class="sxs-lookup"><span data-stu-id="71c90-295">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="71c90-296">Команда TIOCSCTTY должна игнорировать параметр force, если он не является обязательным [GH 3652].</span><span class="sxs-lookup"><span data-stu-id="71c90-296">TIOCSCTTY should ignore the "force" parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="71c90-297">Усовершенствована командная строка wsl.exe и добавлены функции импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="71c90-297">wsl.exe command line improvements and addition of import / export functionality.</span></span>
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a><span data-ttu-id="71c90-298">Сборка 18277</span><span class="sxs-lookup"><span data-stu-id="71c90-298">Build 18277</span></span>
<span data-ttu-id="71c90-299">Общие сведения о сборке Windows 18277 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="71c90-299">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-300">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-300">WSL</span></span>
* <span data-ttu-id="71c90-301">Устранена ошибка "Интерфейс не поддерживается" в сборке 18272 [GH 3645].</span><span class="sxs-lookup"><span data-stu-id="71c90-301">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="71c90-302">Игнорируется флаг MNT_FORCE для umount syscall [GH 3605].</span><span class="sxs-lookup"><span data-stu-id="71c90-302">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="71c90-303">Переключено взаимодействие WSL для использования официального API CreatePseudoConsole.</span><span class="sxs-lookup"><span data-stu-id="71c90-303">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="71c90-304">При перезапуске FUTEX_WAIT значение времени ожидания не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="71c90-304">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="71c90-305">Сборка 18272</span><span class="sxs-lookup"><span data-stu-id="71c90-305">Build 18272</span></span>
<span data-ttu-id="71c90-306">Общие сведения о сборке Windows 18272 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="71c90-306">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-307">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-307">WSL</span></span>
* <span data-ttu-id="71c90-308">**Предупреждение**. В этой сборке есть проблема, делающая компонент WSL неработоспособным.</span><span class="sxs-lookup"><span data-stu-id="71c90-308">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="71c90-309">При попытке запустить дистрибутив появится сообщение об ошибке "Интерфейс не поддерживается".</span><span class="sxs-lookup"><span data-stu-id="71c90-309">When trying to launch your distribution you will see a "No such interface supported" error.</span></span> <span data-ttu-id="71c90-310">Эта проблема устранена, и соответствующее исправление будет добавлено в сборку для предварительной оценки с ранним доступом, выпускаемую на следующей неделе.</span><span class="sxs-lookup"><span data-stu-id="71c90-310">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="71c90-311">Если вы установили эту сборку, можно вернуться к предыдущей сборке Windows, выбрав "Параметры" > "Обновление и безопасность" > "Восстановление" и щелкнув "Вернуться к предыдущей версии Windows 10".</span><span class="sxs-lookup"><span data-stu-id="71c90-311">If you've installed this build you can roll back to the previous Windows build using "Go back to the previous version of Windows 10" in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="71c90-312">Сборка 18267</span><span class="sxs-lookup"><span data-stu-id="71c90-312">Build 18267</span></span>
<span data-ttu-id="71c90-313">Общие сведения о сборке Windows 18267 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="71c90-313">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-314">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-314">WSL</span></span>
* <span data-ttu-id="71c90-315">Устранена проблема, из-за которой зомби-процесс мог быть не удален и существовал неограниченное время.</span><span class="sxs-lookup"><span data-stu-id="71c90-315">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="71c90-316">WslRegisterDistribution переставал отвечать на запросы, если сообщение об ошибке превышало максимальную длину [GH 3592].</span><span class="sxs-lookup"><span data-stu-id="71c90-316">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="71c90-317">Разрешено использование fsync с файлами только для чтения в DrvFs [GH 3556].</span><span class="sxs-lookup"><span data-stu-id="71c90-317">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="71c90-318">Перед созданием символических ссылок в каталогах /bin и /sbin убедитесь, что эти каталоги существуют [GH 3584].</span><span class="sxs-lookup"><span data-stu-id="71c90-318">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="71c90-319">Добавлен механизм времени ожидания завершения экземпляра для экземпляров WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-319">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="71c90-320">Сейчас время ожидания равно 15 секундам, то есть работа экземпляра завершается через 15 секунд после завершения последнего процесса WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-320">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="71c90-321">Чтобы немедленно завершить дистрибутив, используйте следующую команду.</span><span class="sxs-lookup"><span data-stu-id="71c90-321">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="71c90-322">Сборка 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="71c90-322">Build 17763 (1809)</span></span>
<span data-ttu-id="71c90-323">Общие сведения о сборке Windows 17763 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="71c90-323">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-324">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-324">WSL</span></span>
* <span data-ttu-id="71c90-325">Проверка разрешения SetPriority для syscall была слишком строгая для изменения приоритета того же потока [GH 1838].</span><span class="sxs-lookup"><span data-stu-id="71c90-325">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="71c90-326">Убедитесь, что для времени загрузки используется несмещенное время прерывания, чтобы избежать возврата отрицательных значений clock_gettime (CLOCK_BOOTTIME) [GH 3434].</span><span class="sxs-lookup"><span data-stu-id="71c90-326">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="71c90-327">Обработка символических ссылок в интерпретаторе binfmt для WSL [GH 3424].</span><span class="sxs-lookup"><span data-stu-id="71c90-327">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="71c90-328">Улучшена обработка очистки дескриптора файла ведущего потока группы потоков.</span><span class="sxs-lookup"><span data-stu-id="71c90-328">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="71c90-329">Чтобы избежать переполнения, переключите WSL на использование KeQueryInterruptTimePrecise вместо KeQueryPerformanceCounter [GH 3252].</span><span class="sxs-lookup"><span data-stu-id="71c90-329">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="71c90-330">Подключение Ptrace могло вызывать неправильное возвращаемое значение из системных вызовов [GH 1731].</span><span class="sxs-lookup"><span data-stu-id="71c90-330">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="71c90-331">Устранено несколько проблем, связанных с AF_UNIX [GH 3371].</span><span class="sxs-lookup"><span data-stu-id="71c90-331">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="71c90-332">Устранена проблема, которая могла привести к сбою взаимодействия WSL, если длина текущего рабочего каталога была меньше 5 знаков [GH 3379].</span><span class="sxs-lookup"><span data-stu-id="71c90-332">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="71c90-333">Предотвращена задержка в 1 секунду при сбое замыкания на себя подключений к несуществующим портам (GH 3286).</span><span class="sxs-lookup"><span data-stu-id="71c90-333">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="71c90-334">Добавлен файл заглушки /proc/sys/fs/file-max [GH 2893].</span><span class="sxs-lookup"><span data-stu-id="71c90-334">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="71c90-335">Уточнены сведения об области действия IPv6.</span><span class="sxs-lookup"><span data-stu-id="71c90-335">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="71c90-336">Поддержка PR_SET_PTRACER [GH 3053].</span><span class="sxs-lookup"><span data-stu-id="71c90-336">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="71c90-337">Канальная файловая система необоснованно очищала событие epoll, активируемое переходом [GH 3276].</span><span class="sxs-lookup"><span data-stu-id="71c90-337">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="71c90-338">Исполняемый файл Win32, запущенный с помощью символической ссылки NTFS, не учитывал имя символической ссылки [GH 2909].</span><span class="sxs-lookup"><span data-stu-id="71c90-338">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="71c90-339">Улучшена поддержка зомби [GH 1353].</span><span class="sxs-lookup"><span data-stu-id="71c90-339">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="71c90-340">Добавлены записи wsl.conf для управления поведением взаимодействия с Windows [GH 1493].</span><span class="sxs-lookup"><span data-stu-id="71c90-340">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="71c90-341">Устранена проблема, из-за которой команда getsockname не всегда возвращала тип семейства сокетов UNIX [GH 1774].</span><span class="sxs-lookup"><span data-stu-id="71c90-341">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="71c90-342">Добавлена поддержка TIOCSTI [GH 1863].</span><span class="sxs-lookup"><span data-stu-id="71c90-342">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="71c90-343">Неблокирующие сокеты в процессе подключения должны возвращать EAGAIN для попыток записи [GH 2846].</span><span class="sxs-lookup"><span data-stu-id="71c90-343">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="71c90-344">Поддержка взаимодействия с подключенными виртуальными жесткими дисками [GH 3246, 3291].</span><span class="sxs-lookup"><span data-stu-id="71c90-344">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="71c90-345">Устранена проблема с проверкой разрешений для корневой папки [GH 3304].</span><span class="sxs-lookup"><span data-stu-id="71c90-345">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="71c90-346">Ограниченная поддержка вызовов ioctl с аргументами KDGKBTYPE, KDGKBMODE и KDSKBMODE для клавиатуры tty.</span><span class="sxs-lookup"><span data-stu-id="71c90-346">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="71c90-347">Приложения пользовательского интерфейса Windows должны выполняться, даже если они запущены в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="71c90-347">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="71c90-348">Добавлен параметр wsl --u или --user [GH 1203].</span><span class="sxs-lookup"><span data-stu-id="71c90-348">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="71c90-349">Устранены проблемы с запуском WSL, когда включен быстрый запуск [GH 2576].</span><span class="sxs-lookup"><span data-stu-id="71c90-349">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="71c90-350">Сокеты UNIX должны хранить учетные данные отключенных одноранговых узлов [GH 3183].</span><span class="sxs-lookup"><span data-stu-id="71c90-350">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="71c90-351">Работа неблокирующих сокетов UNIX неограниченное время завершалась сбоем и возвращалось значение EAGAIN [GH 3191].</span><span class="sxs-lookup"><span data-stu-id="71c90-351">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="71c90-352">Новый тип подключения drvfs по умолчанию case=off [GH 2937, 3212, 3328].</span><span class="sxs-lookup"><span data-stu-id="71c90-352">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="71c90-353">Дополнительные сведения см. в [этом блоге](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="71c90-353">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="71c90-354">Добавлен параметр wslconfig /terminate для остановки выполнения дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="71c90-354">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="71c90-355">Устранена проблема с пунктами в контекстном меню оболочки WSL, из-за которой неправильно обрабатывались пути с пробелами.</span><span class="sxs-lookup"><span data-stu-id="71c90-355">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="71c90-356">Учет регистра в именах каталогов реализован в качестве расширенного атрибута.</span><span class="sxs-lookup"><span data-stu-id="71c90-356">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="71c90-357">ARM64: имитация операций обслуживания кэша.</span><span class="sxs-lookup"><span data-stu-id="71c90-357">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="71c90-358">Устранена [проблема с dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="71c90-358">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="71c90-359">DrvFs: в частном диапазоне допускаются только неэкранированные знаки, которые соответствуют экранированному знаку.</span><span class="sxs-lookup"><span data-stu-id="71c90-359">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="71c90-360">Устранена ошибка завышения или занижения на единицу при проверке длины интерпретатором анализатора ELF [GH 3154].</span><span class="sxs-lookup"><span data-stu-id="71c90-360">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="71c90-361">Абсолютные таймеры WSL со временем в прошлом не срабатывали [GH 3091].</span><span class="sxs-lookup"><span data-stu-id="71c90-361">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="71c90-362">Убедитесь, что вновь созданные точки повторного анализа указаны как таковые в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="71c90-362">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="71c90-363">Атомарное создание каталогов с учетом регистра в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-363">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="71c90-364">Устранена дополнительная проблема, из-за которой многопоточные операции могли возвращать ENOENT, даже если файл существовал.</span><span class="sxs-lookup"><span data-stu-id="71c90-364">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="71c90-365">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="71c90-365">[GH 2712]</span></span>
* <span data-ttu-id="71c90-366">Устранена ошибка запуска WSL при включенном режиме UMCI.</span><span class="sxs-lookup"><span data-stu-id="71c90-366">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="71c90-367">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="71c90-367">[GH 3020]</span></span>
* <span data-ttu-id="71c90-368">Добавлено контекстное меню обозревателя для запуска WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="71c90-368">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="71c90-369">Чтобы открыть его, нажмите и удерживайте клавишу SHIFT и щелкните правой кнопкой мыши в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="71c90-369">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="71c90-370">Устранено неблокирующее поведение сокетов UNIX [GH 2822, 3100].</span><span class="sxs-lookup"><span data-stu-id="71c90-370">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="71c90-371">Устранена проблема, из-за которой команда NETLINK переставала отвечать на запросы, как было сообщено в GH 2026.</span><span class="sxs-lookup"><span data-stu-id="71c90-371">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="71c90-372">Добавлена поддержка флагов распространения подключения [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="71c90-372">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="71c90-373">Устранена проблема, из-за которой усечение не вызывало события inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="71c90-373">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="71c90-374">Добавлен параметр --exec для wsl.exe, позволяющий вызвать отдельный двоичный файл без оболочки.</span><span class="sxs-lookup"><span data-stu-id="71c90-374">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="71c90-375">Добавлен параметр --distribution для wsl.exe, позволяющий выбрать конкретный дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="71c90-375">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="71c90-376">Ограниченная поддержка dmesg.</span><span class="sxs-lookup"><span data-stu-id="71c90-376">Limited support for dmesg.</span></span> <span data-ttu-id="71c90-377">Теперь приложения могут входить в dmesg.</span><span class="sxs-lookup"><span data-stu-id="71c90-377">Applications can now log to dmesg.</span></span> <span data-ttu-id="71c90-378">Драйвер WSL записывает ограниченные сведения в dmesg.</span><span class="sxs-lookup"><span data-stu-id="71c90-378">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="71c90-379">В будущем эти возможности можно будет расширить, чтобы записывать другие сведения и данные диагностики из драйвера.</span><span class="sxs-lookup"><span data-stu-id="71c90-379">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="71c90-380">Примечание. Сейчас dmesg поддерживается через интерфейс устройства `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="71c90-380">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="71c90-381">Интерфейс syscall `syslog` пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="71c90-381">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="71c90-382">Поэтому некоторые параметры командной строки `dmesg`, такие как `-S` и `-C`, не работают.</span><span class="sxs-lookup"><span data-stu-id="71c90-382">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="71c90-383">Изменены GID и режим по умолчанию для последовательных устройств, чтобы обеспечить соответствие собственному режиму [GH 3042].</span><span class="sxs-lookup"><span data-stu-id="71c90-383">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="71c90-384">Теперь DrvFs поддерживает расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="71c90-384">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="71c90-385">Примечание. В DrvFs были некоторые ограничения для имен расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="71c90-385">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="71c90-386">Некоторые знаки (например, "/", ":" и "\*") не допускаются, а в именах расширенных атрибутов в DrvFs не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="71c90-386">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="71c90-387">Сборка 18252 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="71c90-387">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="71c90-388">Общие сведения о сборке Windows 18252 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="71c90-388">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-389">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-389">WSL</span></span>
* <span data-ttu-id="71c90-390">Двоичные файлы init и bsdtar перемещены из библиотеки DLL lxssmanager в отдельную папку tools.</span><span class="sxs-lookup"><span data-stu-id="71c90-390">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="71c90-391">Устранено состязание при закрытии дескриптора файла в случае использования CLONE_FILES.</span><span class="sxs-lookup"><span data-stu-id="71c90-391">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="71c90-392">Обработка необязательных полей в /proc/pid/mountinfo при преобразовании путей DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-392">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="71c90-393">Допускается успешное выполнение mknod DrvFs без поддержки метаданных для S_IFREG.</span><span class="sxs-lookup"><span data-stu-id="71c90-393">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="71c90-394">Файлы только для чтения, созданные в DrvFs, должны иметь атрибут readonly [GH 3411].</span><span class="sxs-lookup"><span data-stu-id="71c90-394">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="71c90-395">Добавлено вспомогательное приложение /sbin/mount.drvfs для управления подключением DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-395">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="71c90-396">Использование переименования POSIX в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-396">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="71c90-397">Разрешено преобразование путей в томах без GUID тома.</span><span class="sxs-lookup"><span data-stu-id="71c90-397">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="71c90-398">Сборка 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="71c90-398">Build 17738 (Fast)</span></span>
<span data-ttu-id="71c90-399">Общие сведения о сборке Windows 17738 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="71c90-399">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-400">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-400">WSL</span></span>
* <span data-ttu-id="71c90-401">Проверка разрешения SetPriority для syscall была слишком строгая для изменения приоритета того же потока [GH 1838].</span><span class="sxs-lookup"><span data-stu-id="71c90-401">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="71c90-402">Убедитесь, что для времени загрузки используется несмещенное время прерывания, чтобы избежать возврата отрицательных значений clock_gettime (CLOCK_BOOTTIME) [GH 3434].</span><span class="sxs-lookup"><span data-stu-id="71c90-402">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="71c90-403">Обработка символических ссылок в интерпретаторе binfmt для WSL [GH 3424].</span><span class="sxs-lookup"><span data-stu-id="71c90-403">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="71c90-404">Улучшена обработка очистки дескриптора файла ведущего потока группы потоков.</span><span class="sxs-lookup"><span data-stu-id="71c90-404">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="71c90-405">Сборка 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="71c90-405">Build 17728 (Fast)</span></span>
<span data-ttu-id="71c90-406">Общие сведения о сборке Windows 17728 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="71c90-406">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-407">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-407">WSL</span></span>
* <span data-ttu-id="71c90-408">Чтобы избежать переполнения, переключите WSL на использование KeQueryInterruptTimePrecise вместо KeQueryPerformanceCounter [GH 3252].</span><span class="sxs-lookup"><span data-stu-id="71c90-408">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="71c90-409">Подключение Ptrace могло вызывать неправильное возвращаемое значение из системных вызовов [GH 1731].</span><span class="sxs-lookup"><span data-stu-id="71c90-409">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="71c90-410">Устранен ряд проблем, связанных с AF_UNIX [GH 3371].</span><span class="sxs-lookup"><span data-stu-id="71c90-410">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="71c90-411">Устранена проблема, которая могла привести к сбою взаимодействия WSL, если длина текущего рабочего каталога была меньше 5 знаков [GH 3379].</span><span class="sxs-lookup"><span data-stu-id="71c90-411">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="71c90-412">Сборка 18204 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="71c90-412">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="71c90-413">Общие сведения о сборке Windows 18204 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="71c90-413">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-414">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-414">WSL</span></span>
* <span data-ttu-id="71c90-415">Канальная файловая система необоснованно очищала событие epoll, активируемое переходом [GH 3276].</span><span class="sxs-lookup"><span data-stu-id="71c90-415">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="71c90-416">Исполняемый файл Win32, запущенный с помощью символической ссылки NTFS, не учитывал имя символической ссылки [GH 2909].</span><span class="sxs-lookup"><span data-stu-id="71c90-416">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="71c90-417">Сборка 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="71c90-417">Build 17723 (Fast)</span></span>
<span data-ttu-id="71c90-418">Общие сведения о сборке Windows 17723 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="71c90-418">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-419">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-419">WSL</span></span>
* <span data-ttu-id="71c90-420">Предотвращена задержка в 1 секунду при сбое замыкания на себя подключений к несуществующим портам (GH 3286).</span><span class="sxs-lookup"><span data-stu-id="71c90-420">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="71c90-421">Добавлен файл заглушки /proc/sys/fs/file-max [GH 2893].</span><span class="sxs-lookup"><span data-stu-id="71c90-421">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="71c90-422">Уточнены сведения об области действия IPv6.</span><span class="sxs-lookup"><span data-stu-id="71c90-422">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="71c90-423">Поддержка PR_SET_PTRACER [GH 3053].</span><span class="sxs-lookup"><span data-stu-id="71c90-423">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="71c90-424">Канальная файловая система необоснованно очищала событие epoll, активируемое переходом [GH 3276].</span><span class="sxs-lookup"><span data-stu-id="71c90-424">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="71c90-425">Исполняемый файл Win32, запущенный с помощью символической ссылки NTFS, не учитывал имя символической ссылки [GH 2909].</span><span class="sxs-lookup"><span data-stu-id="71c90-425">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="71c90-426">Сборка 17713</span><span class="sxs-lookup"><span data-stu-id="71c90-426">Build 17713</span></span>
<span data-ttu-id="71c90-427">Общие сведения о сборке Windows 17713 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="71c90-427">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-428">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-428">WSL</span></span>
* <span data-ttu-id="71c90-429">Улучшена поддержка зомби [GH 1353].</span><span class="sxs-lookup"><span data-stu-id="71c90-429">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="71c90-430">Добавлены записи wsl.conf для управления поведением взаимодействия с Windows [GH 1493].</span><span class="sxs-lookup"><span data-stu-id="71c90-430">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="71c90-431">Устранена проблема, из-за которой команда getsockname не всегда возвращала тип семейства сокетов UNIX [GH 1774].</span><span class="sxs-lookup"><span data-stu-id="71c90-431">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="71c90-432">Добавлена поддержка TIOCSTI [GH 1863].</span><span class="sxs-lookup"><span data-stu-id="71c90-432">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="71c90-433">Неблокирующие сокеты в процессе подключения должны возвращать EAGAIN для попыток записи [GH 2846].</span><span class="sxs-lookup"><span data-stu-id="71c90-433">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="71c90-434">Поддержка взаимодействия с подключенными виртуальными жесткими дисками [GH 3246, 3291].</span><span class="sxs-lookup"><span data-stu-id="71c90-434">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="71c90-435">Устранена проблема с проверкой разрешений для корневой папки [GH 3304].</span><span class="sxs-lookup"><span data-stu-id="71c90-435">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="71c90-436">Ограниченная поддержка вызовов ioctl с аргументами KDGKBTYPE, KDGKBMODE и KDSKBMODE для клавиатуры tty.</span><span class="sxs-lookup"><span data-stu-id="71c90-436">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="71c90-437">Приложения пользовательского интерфейса Windows должны выполняться, даже если они запущены в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="71c90-437">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="71c90-438">Сборка 17704</span><span class="sxs-lookup"><span data-stu-id="71c90-438">Build 17704</span></span>
<span data-ttu-id="71c90-439">Общие сведения о сборке Windows 17704 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="71c90-439">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-440">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-440">WSL</span></span>
* <span data-ttu-id="71c90-441">Добавлен параметр wsl --u или --user [GH 1203].</span><span class="sxs-lookup"><span data-stu-id="71c90-441">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="71c90-442">Устранены проблемы с запуском WSL, когда включен быстрый запуск [GH 2576].</span><span class="sxs-lookup"><span data-stu-id="71c90-442">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="71c90-443">Сокеты UNIX должны хранить учетные данные отключенных одноранговых узлов [GH 3183].</span><span class="sxs-lookup"><span data-stu-id="71c90-443">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="71c90-444">Работа неблокирующих сокетов UNIX неограниченное время завершалась сбоем и возвращалось значение EAGAIN [GH 3191].</span><span class="sxs-lookup"><span data-stu-id="71c90-444">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="71c90-445">Новый тип подключения drvfs по умолчанию case=off [GH 2937, 3212, 3328].</span><span class="sxs-lookup"><span data-stu-id="71c90-445">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="71c90-446">Дополнительные сведения см. в [этом блоге](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="71c90-446">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="71c90-447">Добавлен параметр wslconfig /terminate для остановки выполнения дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="71c90-447">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="71c90-448">Сборка 17692</span><span class="sxs-lookup"><span data-stu-id="71c90-448">Build 17692</span></span>
<span data-ttu-id="71c90-449">Общие сведения о сборке Windows 17692 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="71c90-449">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-450">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-450">WSL</span></span>
* <span data-ttu-id="71c90-451">Устранена проблема с пунктами в контекстном меню оболочки WSL, из-за которой неправильно обрабатывались пути с пробелами.</span><span class="sxs-lookup"><span data-stu-id="71c90-451">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="71c90-452">Учет регистра в именах каталогов реализован в качестве расширенного атрибута.</span><span class="sxs-lookup"><span data-stu-id="71c90-452">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="71c90-453">ARM64: имитация операций обслуживания кэша.</span><span class="sxs-lookup"><span data-stu-id="71c90-453">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="71c90-454">Устранена [проблема с dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="71c90-454">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="71c90-455">DrvFs: в частном диапазоне допускаются только неэкранированные знаки, которые соответствуют экранированному знаку.</span><span class="sxs-lookup"><span data-stu-id="71c90-455">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="71c90-456">Сборка 17686</span><span class="sxs-lookup"><span data-stu-id="71c90-456">Build 17686</span></span>
<span data-ttu-id="71c90-457">Общие сведения о сборке Windows 17686 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="71c90-457">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-458">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-458">WSL</span></span>
* <span data-ttu-id="71c90-459">Устранена ошибка завышения или занижения на единицу при проверке длины интерпретатором анализатора ELF [GH 3154].</span><span class="sxs-lookup"><span data-stu-id="71c90-459">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="71c90-460">Абсолютные таймеры WSL со временем в прошлом не срабатывали [GH 3091].</span><span class="sxs-lookup"><span data-stu-id="71c90-460">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="71c90-461">Убедитесь, что вновь созданные точки повторного анализа указаны как таковые в родительском каталоге.</span><span class="sxs-lookup"><span data-stu-id="71c90-461">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="71c90-462">Атомарное создание каталогов с учетом регистра в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-462">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="71c90-463">Сборка 17677</span><span class="sxs-lookup"><span data-stu-id="71c90-463">Build 17677</span></span>
<span data-ttu-id="71c90-464">Общие сведения о сборке Windows 17677 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="71c90-464">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-465">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-465">WSL</span></span>
* <span data-ttu-id="71c90-466">Устранена дополнительная проблема, из-за которой многопоточные операции могли возвращать ENOENT, даже если файл существовал.</span><span class="sxs-lookup"><span data-stu-id="71c90-466">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="71c90-467">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="71c90-467">[GH 2712]</span></span>
* <span data-ttu-id="71c90-468">Устранена ошибка запуска WSL при включенном режиме UMCI.</span><span class="sxs-lookup"><span data-stu-id="71c90-468">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="71c90-469">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="71c90-469">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="71c90-470">Сборка 17666</span><span class="sxs-lookup"><span data-stu-id="71c90-470">Build 17666</span></span>
<span data-ttu-id="71c90-471">Общие сведения о сборке Windows 17666 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="71c90-471">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-472">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-472">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="71c90-473">ПРЕДУПРЕЖДЕНИЕ! Существует проблема, препятствующая запуску WSL на некоторых наборах микросхем AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="71c90-473">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="71c90-474">Исправление готово и находится в процессе добавления в ветвь сборок для программы предварительной оценки Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-474">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="71c90-475">Добавлено контекстное меню обозревателя для запуска WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="71c90-475">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="71c90-476">Чтобы открыть его, нажмите и удерживайте клавишу SHIFT и щелкните правой кнопкой мыши в окне проводника.</span><span class="sxs-lookup"><span data-stu-id="71c90-476">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="71c90-477">Устранено неблокирующее поведение сокетов UNIX [GH 2822, 3100].</span><span class="sxs-lookup"><span data-stu-id="71c90-477">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="71c90-478">Устранена проблема, из-за которой команда NETLINK переставала отвечать на запросы, как было сообщено в GH 2026.</span><span class="sxs-lookup"><span data-stu-id="71c90-478">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="71c90-479">Добавлена поддержка флагов распространения подключения [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="71c90-479">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="71c90-480">Устранена проблема, из-за которой усечение не вызывало события inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="71c90-480">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="71c90-481">Добавлен параметр --exec для wsl.exe, позволяющий вызвать отдельный двоичный файл без оболочки.</span><span class="sxs-lookup"><span data-stu-id="71c90-481">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="71c90-482">Добавлен параметр --distribution для wsl.exe, позволяющий выбрать конкретный дистрибутив.</span><span class="sxs-lookup"><span data-stu-id="71c90-482">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="71c90-483">Сборка 17655 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="71c90-483">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="71c90-484">Общие сведения о сборке Windows 17655 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="71c90-484">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-485">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-485">WSL</span></span>
* <span data-ttu-id="71c90-486">Ограниченная поддержка dmesg.</span><span class="sxs-lookup"><span data-stu-id="71c90-486">Limited support for dmesg.</span></span> <span data-ttu-id="71c90-487">Теперь приложения могут входить в dmesg.</span><span class="sxs-lookup"><span data-stu-id="71c90-487">Applications can now log to dmesg.</span></span> <span data-ttu-id="71c90-488">Драйвер WSL записывает ограниченные сведения в dmesg.</span><span class="sxs-lookup"><span data-stu-id="71c90-488">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="71c90-489">В будущем эти возможности можно будет расширить, чтобы записывать другие сведения и данные диагностики из драйвера.</span><span class="sxs-lookup"><span data-stu-id="71c90-489">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="71c90-490">Примечание. Сейчас dmesg поддерживается через интерфейс устройства `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="71c90-490">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="71c90-491">Интерфейс sycall `syslog` еще не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="71c90-491">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="71c90-492">Поэтому некоторые параметры командной строки `dmesg`, такие как `-S` и `-C`, не работают.</span><span class="sxs-lookup"><span data-stu-id="71c90-492">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="71c90-493">Устранена проблема, из-за которой многопоточные операции могли возвращать ENOENT, даже если файл существовал.</span><span class="sxs-lookup"><span data-stu-id="71c90-493">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="71c90-494">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="71c90-494">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="71c90-495">Сборка 17639 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="71c90-495">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="71c90-496">Общие сведения о сборке Windows 17639 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="71c90-496">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-497">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-497">WSL</span></span>
* <span data-ttu-id="71c90-498">Изменены GID и режим по умолчанию для последовательных устройств, чтобы обеспечить соответствие собственному режиму [GH 3042].</span><span class="sxs-lookup"><span data-stu-id="71c90-498">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="71c90-499">Теперь DrvFs поддерживает расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="71c90-499">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="71c90-500">Примечание. В DrvFs были некоторые ограничения для имен расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="71c90-500">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="71c90-501">В частности, некоторые знаки (например, "/", ":" и "\*") не допускаются, а в именах расширенных атрибутов в DrvFs не учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="71c90-501">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="71c90-502">Сборка 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="71c90-502">Build 17133 (Fast)</span></span>
<span data-ttu-id="71c90-503">Общие сведения о сборке Windows 17133 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="71c90-503">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-504">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-504">WSL</span></span>
* <span data-ttu-id="71c90-505">Устранено прекращение ответа на запросы в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-505">Fix for hang in WSL.</span></span> <span data-ttu-id="71c90-506">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="71c90-506">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="71c90-507">Сборка 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="71c90-507">Build 17128 (Fast)</span></span>
<span data-ttu-id="71c90-508">Общие сведения о сборке Windows 17128 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="71c90-508">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-509">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-509">WSL</span></span>
* <span data-ttu-id="71c90-510">Нет</span><span class="sxs-lookup"><span data-stu-id="71c90-510">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="71c90-511">Сборка 17627 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="71c90-511">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="71c90-512">Общие сведения о сборке Windows 17627 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="71c90-512">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-513">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-513">WSL</span></span>
* <span data-ttu-id="71c90-514">Добавлена поддержка фьютексных операций с поддержкой числа пи.</span><span class="sxs-lookup"><span data-stu-id="71c90-514">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="71c90-515">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="71c90-515">[GH 1006]</span></span>
    * <span data-ttu-id="71c90-516">Обратите внимание на то, что приоритеты в настоящее время не поддерживаются компонентом WSL, так что существуют ограничения, но стандартное использование должно быть доступно.</span><span class="sxs-lookup"><span data-stu-id="71c90-516">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="71c90-517">Поддержка брандмауэра Windows для процессов WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-517">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="71c90-518">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="71c90-518">[GH 1852]</span></span>
    * <span data-ttu-id="71c90-519">Например, чтобы разрешить процессу Python в WSL ожидать передачи данных через какой-либо порт, используйте командную строку Windows с повышенными привилегиями: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="71c90-519">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="71c90-520">Дополнительные сведения о добавлении правил брандмауэра доступны по [этой ссылке](https://support.microsoft.com/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh).</span><span class="sxs-lookup"><span data-stu-id="71c90-520">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="71c90-521">При использовании wsl.exe учитывается оболочка по умолчанию пользователя.</span><span class="sxs-lookup"><span data-stu-id="71c90-521">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="71c90-522">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="71c90-522">[GH 2372]</span></span>
* <span data-ttu-id="71c90-523">Все сетевые интерфейсы отображаются как Ethernet.</span><span class="sxs-lookup"><span data-stu-id="71c90-523">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="71c90-524">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="71c90-524">[GH 2996]</span></span>
* <span data-ttu-id="71c90-525">Улучшена обработка поврежденного файла /etc/passwd.</span><span class="sxs-lookup"><span data-stu-id="71c90-525">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="71c90-526">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="71c90-526">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="71c90-527">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-527">Console</span></span>
* <span data-ttu-id="71c90-528">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-528">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-529">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-529">LTP Results:</span></span>
<span data-ttu-id="71c90-530">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-530">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="71c90-531">Сборка 17618 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="71c90-531">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="71c90-532">Общие сведения о сборке Windows 17618 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="71c90-532">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-533">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-533">WSL</span></span>
* <span data-ttu-id="71c90-534">Введена функция псевдоконсоли для взаимодействия с NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="71c90-534">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="71c90-535">Устаревший механизм установки (lxrun.exe) является нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="71c90-535">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="71c90-536">Для установки дистрибутивов используется Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="71c90-536">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="71c90-537">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-537">Console</span></span>
* <span data-ttu-id="71c90-538">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-538">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-539">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-539">LTP Results:</span></span>
<span data-ttu-id="71c90-540">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-540">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="71c90-541">Сборка 17110</span><span class="sxs-lookup"><span data-stu-id="71c90-541">Build 17110</span></span>
<span data-ttu-id="71c90-542">Общие сведения о сборке Windows 17110 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="71c90-542">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-543">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-543">WSL</span></span>
* <span data-ttu-id="71c90-544">Разрешено завершение /init из Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="71c90-544">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="71c90-545">Теперь DrvFs по умолчанию учитывает регистр в имени отдельно для каждого каталога (аналогично параметру подключения case=dir).</span><span class="sxs-lookup"><span data-stu-id="71c90-545">DrvFs now uses per-directory case sensitivity by default (equivalent to the "case=dir" mount option).</span></span>
    * <span data-ttu-id="71c90-546">Для использования параметра case=force (прежнее поведение) требуется задать раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="71c90-546">Using "case=force" (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="71c90-547">Выполните следующую команду, чтобы включить режим case=force, если его необходимо использовать: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="71c90-547">Run the following command to enable "case=force" if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="71c90-548">Если у вас есть каталоги, созданные с помощью WSL в более ранней версии Windows, в которых должен учитываться регистр, используйте fsutil.exe, чтобы пометить их как каталоги с учетом регистра: fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="71c90-548">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="71c90-549">Строки, возвращаемые из uname syscall, завершаются значением NULL.</span><span class="sxs-lookup"><span data-stu-id="71c90-549">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="71c90-550">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-550">Console</span></span>
* <span data-ttu-id="71c90-551">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-551">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-552">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-552">LTP Results:</span></span>
<span data-ttu-id="71c90-553">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-553">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="71c90-554">Сборка 17107</span><span class="sxs-lookup"><span data-stu-id="71c90-554">Build 17107</span></span>
<span data-ttu-id="71c90-555">Общие сведения о сборке Windows 17107 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="71c90-555">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-556">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-556">WSL</span></span>
* <span data-ttu-id="71c90-557">Поддержка TCSETSF и TCSETSW на главных конечных точках PTY [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="71c90-557">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="71c90-558">Запуск одновременных процессов взаимодействия мог привести к возвращению EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="71c90-558">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="71c90-559">Устранена проблема с PTRACE_ATTACH для отображения правильного состояния трассировки в /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="71c90-559">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="71c90-560">Устранено состязание, когда кратковременные процессы, клонированные с флагами CLEARTID и SETTID, могли завершиться без очистки адреса TID.</span><span class="sxs-lookup"><span data-stu-id="71c90-560">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="71c90-561">Отображается сообщение, если при переходе со сборки, предшествующей сборке 17093, выполняется обновление каталогов файловой системы Linux.</span><span class="sxs-lookup"><span data-stu-id="71c90-561">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="71c90-562">Дополнительные сведения об изменениях в файловой системе в сборке 17093 доступны в заметках о выпуске [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="71c90-562">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="71c90-563">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-563">Console</span></span>
* <span data-ttu-id="71c90-564">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-564">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-565">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-565">LTP Results:</span></span>
<span data-ttu-id="71c90-566">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-566">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="71c90-567">Сборка 17101</span><span class="sxs-lookup"><span data-stu-id="71c90-567">Build 17101</span></span>
<span data-ttu-id="71c90-568">Общие сведения о сборке Windows 17101 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="71c90-568">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-569">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-569">WSL</span></span>
* <span data-ttu-id="71c90-570">Поддержка signalfd.</span><span class="sxs-lookup"><span data-stu-id="71c90-570">Support for signalfd.</span></span> <span data-ttu-id="71c90-571">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="71c90-571">[GH 129]</span></span>
* <span data-ttu-id="71c90-572">Поддержка имен файлов, содержащих недопустимые знаки NTFS, благодаря их кодированию в виде частных знаков Юникода.</span><span class="sxs-lookup"><span data-stu-id="71c90-572">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="71c90-573">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="71c90-573">[GH 1514]</span></span>
* <span data-ttu-id="71c90-574">Функция автоматического подключения будет переключаться в режим только для чтения, если запись не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="71c90-574">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="71c90-575">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="71c90-575">[GH 2603]</span></span>
* <span data-ttu-id="71c90-576">Допускается вставка суррогатных пар Юникода (например, знаков эмодзи).</span><span class="sxs-lookup"><span data-stu-id="71c90-576">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="71c90-577">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="71c90-577">[GH 2765]</span></span>
* <span data-ttu-id="71c90-578">Псевдофайлы в /proc и /sys должны возвращаться готовыми для чтения и записи после выполнения команд select, poll, epoll и т. д. [GH 2838].</span><span class="sxs-lookup"><span data-stu-id="71c90-578">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="71c90-579">Устранена проблема, из-за которой служба могла уйти в бесконечный цикл, если реестр был незаконно изменен или поврежден.</span><span class="sxs-lookup"><span data-stu-id="71c90-579">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="71c90-580">Сообщения NETLINK исправлены для работы с более новой версией iproute2 (начиная с версии 4.14).</span><span class="sxs-lookup"><span data-stu-id="71c90-580">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="71c90-581">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-581">Console</span></span>
* <span data-ttu-id="71c90-582">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-582">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-583">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-583">LTP Results:</span></span>
<span data-ttu-id="71c90-584">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-584">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="71c90-585">Сборка 17093</span><span class="sxs-lookup"><span data-stu-id="71c90-585">Build 17093</span></span>
<span data-ttu-id="71c90-586">Общие сведения о сборке Windows 17093 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-586">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="71c90-587">Важно!</span><span class="sxs-lookup"><span data-stu-id="71c90-587">Important:</span></span>
<span data-ttu-id="71c90-588">При запуске WSL в первый раз после обновления до этой сборки необходимо выполнить некоторые действия, чтобы обновить каталоги файловой системы Linux.</span><span class="sxs-lookup"><span data-stu-id="71c90-588">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="71c90-589">Это может занять несколько минут, поэтому может показаться, что WSL медленно запускается.</span><span class="sxs-lookup"><span data-stu-id="71c90-589">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="71c90-590">Это должно произойти только один раз для каждого дистрибутива, установленного из Store.</span><span class="sxs-lookup"><span data-stu-id="71c90-590">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="71c90-591">Улучшена поддержка учета регистра в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-591">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="71c90-592">Теперь DrvFs поддерживает учет регистра отдельно для каждого каталога.</span><span class="sxs-lookup"><span data-stu-id="71c90-592">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="71c90-593">Это новый флаг, который можно задать для каталогов, чтобы указать, что все операции в этих каталогах должны выполняться с учетом регистра, что позволит даже приложениям для Windows правильно открывать файлы, отличающиеся только регистром в именах.</span><span class="sxs-lookup"><span data-stu-id="71c90-593">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="71c90-594">В DrvFs есть новые параметры подключения, управляющие учетом регистра для каждого каталога:</span><span class="sxs-lookup"><span data-stu-id="71c90-594">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="71c90-595">case=force: для всех каталогов учитывается регистр (за исключением корневого диска).</span><span class="sxs-lookup"><span data-stu-id="71c90-595">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="71c90-596">Новые каталоги, созданные с помощью WSL, помечаются как каталоги с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="71c90-596">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="71c90-597">Это устаревшее поведение, за исключением пометки новых каталогов как каталогов с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="71c90-597">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="71c90-598">case=dir: регистр учитывается только для каталогов с флагом учета регистра; для других каталогов регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="71c90-598">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="71c90-599">Новые каталоги, созданные с помощью WSL, помечаются как каталоги с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="71c90-599">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="71c90-600">case=off: регистр учитывается только для каталогов с флагом учета регистра; для других каталогов регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="71c90-600">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="71c90-601">Новые каталоги, созданные с помощью WSL, помечаются как каталоги без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="71c90-601">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="71c90-602">Примечание. Каталоги, созданные WSL в предыдущих выпусках, не имеют этого флага, поэтому для них регистр не будет учитываться, если задан параметр case=dir.</span><span class="sxs-lookup"><span data-stu-id="71c90-602">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the "case=dir" option.</span></span> <span data-ttu-id="71c90-603">Способ задания этого флага для существующих каталогов будет реализован в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="71c90-603">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="71c90-604">Пример подключения с этими параметрами (существующие диски необходимо сначала отключить, чтобы подключить их с другими параметрами): sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="71c90-604">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="71c90-605">Пока что параметр "case=force" все еще используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71c90-605">For now, case=force is still the default option.</span></span> <span data-ttu-id="71c90-606">В будущем по умолчанию будет использоваться параметр case=dir.</span><span class="sxs-lookup"><span data-stu-id="71c90-606">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="71c90-607">Теперь вы можете использовать косую черту в путях Windows при подключении DrvFs, например: sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="71c90-607">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="71c90-608">WSL теперь обрабатывает файл /etc/fstab во время запуска экземпляра [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="71c90-608">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="71c90-609">Это делается до автоматического подключения дисков DrvFs. Все диски, которые уже были подключены fstab, не будут автоматически подключаться. Это позволит вам изменить точку подключения для конкретных дисков.</span><span class="sxs-lookup"><span data-stu-id="71c90-609">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="71c90-610">Это поведение можно отключить с помощью wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="71c90-610">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="71c90-611">Файлы mount, mountinfo и mountstats в /proc правильно экранируют специальные знаки, такие как символы обратной косой черты и пробелы [GH 2799].</span><span class="sxs-lookup"><span data-stu-id="71c90-611">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="71c90-612">Теперь можно копировать и перемещать из Windows специальные файлы, созданные с помощью DrvFs, такие как символьные ссылки WSL, или файлы FIFO и сокеты, если метаданные включены.</span><span class="sxs-lookup"><span data-stu-id="71c90-612">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="71c90-613">Можно настроить больше параметров WSL с помощью wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="71c90-613">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="71c90-614">Мы добавили метод для автоматической настройки определенных функций в WSL, которые будут применяться при каждом запуске подсистемы.</span><span class="sxs-lookup"><span data-stu-id="71c90-614">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="71c90-615">Сюда входят параметры автоподключения и конфигурация сети.</span><span class="sxs-lookup"><span data-stu-id="71c90-615">This includes automount options and network configuration.</span></span> <span data-ttu-id="71c90-616">Дополнительные сведения об этом можно получить из нашей записи блога: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="71c90-616">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="71c90-617">AF_UNIX позволяет устанавливать подключения через сокет между процессами Linux в собственных процессах WSL и Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-617">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="71c90-618">Теперь приложения WSL и приложения для Windows могут взаимодействовать друг с другом через сокеты UNIX.</span><span class="sxs-lookup"><span data-stu-id="71c90-618">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="71c90-619">Представьте, что вы хотите запустить службу в Windows и сделать ее доступной для приложений для Windows и приложений WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-619">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="71c90-620">Теперь это возможно благодаря сокетам UNIX.</span><span class="sxs-lookup"><span data-stu-id="71c90-620">Now, that's possible with Unix sockets.</span></span> <span data-ttu-id="71c90-621">Узнайте больше в записи блога https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="71c90-621">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-622">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-622">WSL</span></span>
* <span data-ttu-id="71c90-623">Поддержка mmap() с MAP_NORESERVE [GH 121, 2784].</span><span class="sxs-lookup"><span data-stu-id="71c90-623">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="71c90-624">Поддержка CLONE_PTRACE и CLONE_UNTRACED [GH 121, 2781].</span><span class="sxs-lookup"><span data-stu-id="71c90-624">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="71c90-625">Обработка сигнала завершения без SIGCHLD в клоне [GH 121, 2781].</span><span class="sxs-lookup"><span data-stu-id="71c90-625">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="71c90-626">Добавлены заглушки /proc/sys/fs/inotify/max_user_instances и /proc/sys/fs/inotify/max_user_watches [GH 1705].</span><span class="sxs-lookup"><span data-stu-id="71c90-626">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="71c90-627">Устранена ошибка при загрузке двоичных файлов ELF, содержащих заголовки загрузки с ненулевыми смещениями [GH 1884].</span><span class="sxs-lookup"><span data-stu-id="71c90-627">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="71c90-628">Заполнение нулями конечных байтов страниц при загрузке образов.</span><span class="sxs-lookup"><span data-stu-id="71c90-628">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="71c90-629">Сокращены случаи, когда execve автоматически завершает процесс.</span><span class="sxs-lookup"><span data-stu-id="71c90-629">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="71c90-630">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-630">Console</span></span>
* <span data-ttu-id="71c90-631">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-631">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-632">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-632">LTP Results:</span></span>
<span data-ttu-id="71c90-633">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-633">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="71c90-634">Сборка 17083</span><span class="sxs-lookup"><span data-stu-id="71c90-634">Build 17083</span></span>
<span data-ttu-id="71c90-635">Общие сведения о сборке Windows 17083 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-635">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-636">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-636">WSL</span></span>
* <span data-ttu-id="71c90-637">Исправлена критическая ошибка, связанная с epoll [GH 2798, 2801, 2857].</span><span class="sxs-lookup"><span data-stu-id="71c90-637">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="71c90-638">Исправлено прекращение реагирования на запросы при отключении ASLR [GH 1185, 2870].</span><span class="sxs-lookup"><span data-stu-id="71c90-638">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="71c90-639">Обеспечена атомарность операций mmap [GH 2732].</span><span class="sxs-lookup"><span data-stu-id="71c90-639">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="71c90-640">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-640">Console</span></span>
* <span data-ttu-id="71c90-641">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-641">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-642">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-642">LTP Results:</span></span>
<span data-ttu-id="71c90-643">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-643">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="71c90-644">Сборка 17074</span><span class="sxs-lookup"><span data-stu-id="71c90-644">Build 17074</span></span>
<span data-ttu-id="71c90-645">Общие сведения о сборке Windows 17074 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-645">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-646">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-646">WSL</span></span>
* <span data-ttu-id="71c90-647">Исправлен формат хранения метаданных DrvFs [GH 2777].</span><span class="sxs-lookup"><span data-stu-id="71c90-647">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="71c90-648">**Важно!** Метаданные DrvFs, созданные до выпуска этой сборки, будут отображаться неправильно или вообще не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="71c90-648">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="71c90-649">Чтобы исправить затронутые файлы, используйте chmod и chown для повторного применения метаданных.</span><span class="sxs-lookup"><span data-stu-id="71c90-649">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="71c90-650">Устранена проблема с несколькими сигналами и перезапускаемыми вызовами syscall.</span><span class="sxs-lookup"><span data-stu-id="71c90-650">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="71c90-651">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-651">Console</span></span>
* <span data-ttu-id="71c90-652">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-652">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-653">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-653">LTP Results:</span></span>
<span data-ttu-id="71c90-654">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-654">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="71c90-655">Сборка 17063</span><span class="sxs-lookup"><span data-stu-id="71c90-655">Build 17063</span></span>
<span data-ttu-id="71c90-656">Общие сведения о сборке Windows 17063 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-656">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="71c90-657">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-657">WSL</span></span>
* <span data-ttu-id="71c90-658">DrvFs поддерживает дополнительные метаданные Linux.</span><span class="sxs-lookup"><span data-stu-id="71c90-658">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="71c90-659">Это позволяет задать владельца и режим файлов с помощью chmod или chown, а также создать специальные файлы, такие как FIFO, сокеты UNIX и файлы устройств.</span><span class="sxs-lookup"><span data-stu-id="71c90-659">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="71c90-660">Сейчас эта функция отключена по умолчанию, так как еще является экспериментальной.</span><span class="sxs-lookup"><span data-stu-id="71c90-660">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="71c90-661">**Примечание**.  Исправлена ошибка в формате метаданных, используемом DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-661">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="71c90-662">Хотя метаданные используются в этой сборке в качестве эксперимента, будущие сборки не будут правильно считывать метаданные, созданные этой сборкой.</span><span class="sxs-lookup"><span data-stu-id="71c90-662">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="71c90-663">Возможно, потребуется вручную обновить владельца измененных файлов, а устройства с пользовательским идентификатором устройства потребуется создать заново.</span><span class="sxs-lookup"><span data-stu-id="71c90-663">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="71c90-664">Чтобы включить эту функцию, подключите DrvFs с параметром metadata (чтобы включить эту функцию для существующего подключения, его необходимо сначала отключить):</span><span class="sxs-lookup"><span data-stu-id="71c90-664">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="71c90-665">Разрешения Linux добавляются в файл в качестве дополнительных метаданных; они не влияют на разрешения Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-665">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="71c90-666">Помните, что изменение файла с помощью редактора Windows может привести к удалению метаданных.</span><span class="sxs-lookup"><span data-stu-id="71c90-666">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="71c90-667">В этом случае будут восстановлены разрешения этого файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71c90-667">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="71c90-668">Добавлены параметры подключения к DrvFs для управления файлами без метаданных.</span><span class="sxs-lookup"><span data-stu-id="71c90-668">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="71c90-669">uid: идентификатор пользователя, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="71c90-669">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="71c90-670">gid: идентификатор группы, используемый для владельца всех файлов.</span><span class="sxs-lookup"><span data-stu-id="71c90-670">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="71c90-671">umask: восьмеричная маска разрешений, исключаемых для всех файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="71c90-671">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="71c90-672">fmask: восьмеричная маска разрешений, исключаемых для всех обычных файлов.</span><span class="sxs-lookup"><span data-stu-id="71c90-672">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="71c90-673">dmask: восьмеричная маска разрешений, исключаемых для всех каталогов.</span><span class="sxs-lookup"><span data-stu-id="71c90-673">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="71c90-674">Например:</span><span class="sxs-lookup"><span data-stu-id="71c90-674">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="71c90-675">Используйте вместе с параметром metadata, чтобы указать разрешения по умолчанию для файлов без метаданных.</span><span class="sxs-lookup"><span data-stu-id="71c90-675">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="71c90-676">Появилась новая переменная среды, `WSLENV`, позволяющая настроить поток переменных среды между WSL и Win32.</span><span class="sxs-lookup"><span data-stu-id="71c90-676">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="71c90-677">Например:</span><span class="sxs-lookup"><span data-stu-id="71c90-677">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="71c90-678">`WSLENV` — разделенный двоеточиями список переменных среды, которые могут быть добавлены при запуске процессов WSL из Win32 или при запуске процессов Win32 из WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-678">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="71c90-679">Каждая переменная может иметь суффикс с косой чертой, за которой следуют флаги для указания способа преобразования.</span><span class="sxs-lookup"><span data-stu-id="71c90-679">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="71c90-680">p: значение — это путь, который должен быть преобразован между WSL и Win32.</span><span class="sxs-lookup"><span data-stu-id="71c90-680">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="71c90-681">l: значение — это список путей.</span><span class="sxs-lookup"><span data-stu-id="71c90-681">l: The value is a list of paths.</span></span> <span data-ttu-id="71c90-682">В WSL это список, разделенный двоеточиями.</span><span class="sxs-lookup"><span data-stu-id="71c90-682">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="71c90-683">В Win32 это список, разделенный точками с запятой.</span><span class="sxs-lookup"><span data-stu-id="71c90-683">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="71c90-684">u: это значение должно добавляться только при вызове WSL из Win32.</span><span class="sxs-lookup"><span data-stu-id="71c90-684">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="71c90-685">w: это значение должно добавляться только при вызове Win32 из WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-685">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="71c90-686">Вы можете задать `WSLENV` в bashrc или в пользовательской среде Windows для пользователя.</span><span class="sxs-lookup"><span data-stu-id="71c90-686">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="71c90-687">Подключения DrvFs правильно сохраняют метки времени из tar, cp -p (GH 1939).</span><span class="sxs-lookup"><span data-stu-id="71c90-687">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="71c90-688">Символические ссылки DrvFs сообщают правильный размер (GH 2641).</span><span class="sxs-lookup"><span data-stu-id="71c90-688">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="71c90-689">Операции чтения и записи могут обрабатывать очень большие объемы ввода-вывода (GH 2653).</span><span class="sxs-lookup"><span data-stu-id="71c90-689">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="71c90-690">Функция waitpid работает с идентификаторами групп процессов (GH 2534).</span><span class="sxs-lookup"><span data-stu-id="71c90-690">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="71c90-691">Значительно улучшена производительность mmap для больших резервных регионов. Повышена производительность ghc (GH 1671).</span><span class="sxs-lookup"><span data-stu-id="71c90-691">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="71c90-692">Personality поддерживает READ_IMPLIES_EXEC; реализованы исправления для maxima и clisp (GH 1185).</span><span class="sxs-lookup"><span data-stu-id="71c90-692">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="71c90-693">Mprotect поддерживает PROT_GROWSDOWN; реализованы исправления для clisp (GH 1128).</span><span class="sxs-lookup"><span data-stu-id="71c90-693">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="71c90-694">Устранены сбои страниц в режиме перегрузки; реализованы исправления для sbcl (GH 1128).</span><span class="sxs-lookup"><span data-stu-id="71c90-694">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="71c90-695">Функция clone поддерживает больше сочетаний флагов.</span><span class="sxs-lookup"><span data-stu-id="71c90-695">clone supports more flags combinations</span></span>
* <span data-ttu-id="71c90-696">Поддержка select/epoll для файлов epoll (ранее это считалось холостой командой).</span><span class="sxs-lookup"><span data-stu-id="71c90-696">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="71c90-697">Уведомление ptrace о нереализованных вызовах syscall.</span><span class="sxs-lookup"><span data-stu-id="71c90-697">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="71c90-698">Игнорирование интерфейсов, которые не выполняются, при создании серверов имен resolv.conf [GH 2694].</span><span class="sxs-lookup"><span data-stu-id="71c90-698">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="71c90-699">Перечисление сетевых интерфейсов без физического адреса.</span><span class="sxs-lookup"><span data-stu-id="71c90-699">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="71c90-700">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="71c90-700">[GH 2685]</span></span>
* <span data-ttu-id="71c90-701">Дополнительные исправления ошибок и улучшения.</span><span class="sxs-lookup"><span data-stu-id="71c90-701">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="71c90-702">Инструменты Linux, доступные для разработчиков в Windows</span><span class="sxs-lookup"><span data-stu-id="71c90-702">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="71c90-703">Цепочка инструментов командной строки Windows включает в себя bsdtar (tar) и curl.</span><span class="sxs-lookup"><span data-stu-id="71c90-703">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="71c90-704">Ознакомьтесь с [этим блогом](https://aka.ms/tarcurlwindows), чтобы узнать больше о добавлении этих двух новых инструментов и о том, как они меняют возможности разработки в Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-704">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they're shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="71c90-705">`AF_UNIX` доступен в пакете SDK для программы предварительной оценки Windows (начиная со сборки 17061).</span><span class="sxs-lookup"><span data-stu-id="71c90-705">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="71c90-706">Ознакомьтесь с [этим блогом](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/), чтобы узнать больше о `AF_UNIX` и способах его использования разработчиками в Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-706">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="71c90-707">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-707">Console</span></span>
* <span data-ttu-id="71c90-708">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-708">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-709">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-709">LTP Results:</span></span>
<span data-ttu-id="71c90-710">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-710">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="71c90-711">Сборка 17046</span><span class="sxs-lookup"><span data-stu-id="71c90-711">Build 17046</span></span>

<span data-ttu-id="71c90-712">Общие сведения о сборке Windows 17046 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="71c90-712">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="71c90-713">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-713">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="71c90-714">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-714">WSL</span></span>
- <span data-ttu-id="71c90-715">Разрешено выполнение процессов без активного терминала.</span><span class="sxs-lookup"><span data-stu-id="71c90-715">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="71c90-716">[GH 709, 1007, 1511, 2252, 2391 и т. д.]</span><span class="sxs-lookup"><span data-stu-id="71c90-716">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="71c90-717">Улучшена поддержка CLONE_VFORK и CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="71c90-717">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="71c90-718">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="71c90-718">[GH 1878, 2615]</span></span>
- <span data-ttu-id="71c90-719">Пропуск драйверов фильтра TDI для сетевых операций WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-719">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="71c90-720">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="71c90-720">[GH 1554]</span></span>
- <span data-ttu-id="71c90-721">DrvFs создает символические ссылки NT при выполнении определенных условий.</span><span class="sxs-lookup"><span data-stu-id="71c90-721">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="71c90-722">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="71c90-722">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="71c90-723">Цель ссылки должна быть относительной, не должна пересекать точки подключения или символические ссылки и должна существовать.</span><span class="sxs-lookup"><span data-stu-id="71c90-723">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="71c90-724">Пользователь должен иметь разрешение SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (обычно для этого требуется запустить wsl.exe с повышенными привилегиями), если режим разработчика не включен.</span><span class="sxs-lookup"><span data-stu-id="71c90-724">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="71c90-725">Во всех остальных случаях DrvFs по-прежнему создает символические ссылки WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-725">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="71c90-726">Разрешено одновременное выполнение экземпляров WSL с повышенными привилегиями и без повышенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="71c90-726">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="71c90-727">Поддержка /proc/sys/kernel/yama/ptrace_scope.</span><span class="sxs-lookup"><span data-stu-id="71c90-727">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="71c90-728">Добавлена функция wslpath для преобразования путей WSL в пути Windows и наоборот.</span><span class="sxs-lookup"><span data-stu-id="71c90-728">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="71c90-729">[GH 522, 1243, 1834, 2327 и т. д.]</span><span class="sxs-lookup"><span data-stu-id="71c90-729">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with '/' instead of '\\'

      EX: wslpath 'c:\users'
  ```
  #### <a name="console"></a><span data-ttu-id="71c90-730">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-730">Console</span></span>
- <span data-ttu-id="71c90-731">Исправления отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-731">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-732">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-732">LTP Results:</span></span>
<span data-ttu-id="71c90-733">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-733">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="71c90-734">Сборка 17040</span><span class="sxs-lookup"><span data-stu-id="71c90-734">Build 17040</span></span>

<span data-ttu-id="71c90-735">Общие сведения о сборке Windows 17040 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="71c90-735">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-736">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-736">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="71c90-737">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-737">WSL</span></span>
- <span data-ttu-id="71c90-738">Исправления с момента выпуска сборки 17035 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-738">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="71c90-739">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-739">Console</span></span>
- <span data-ttu-id="71c90-740">Исправления с момента выпуска сборки 17035 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-740">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-741">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-741">LTP Results:</span></span>
<span data-ttu-id="71c90-742">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-742">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="71c90-743">Сборка 17035</span><span class="sxs-lookup"><span data-stu-id="71c90-743">Build 17035</span></span>

<span data-ttu-id="71c90-744">Общие сведения о сборке Windows 17035 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="71c90-744">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-745">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-745">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="71c90-746">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-746">WSL</span></span>
- <span data-ttu-id="71c90-747">Иногда не удавалось получить доступ к файлам в DrvFs с ошибкой EINVAL.</span><span class="sxs-lookup"><span data-stu-id="71c90-747">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="71c90-748">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="71c90-748">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="71c90-749">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-749">Console</span></span>
- <span data-ttu-id="71c90-750">Устранена небольшая потеря цветов при вставке или удалении строк в режиме VT.</span><span class="sxs-lookup"><span data-stu-id="71c90-750">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-751">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-751">LTP Results:</span></span>
<span data-ttu-id="71c90-752">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-752">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="71c90-753">Сборка 17025</span><span class="sxs-lookup"><span data-stu-id="71c90-753">Build 17025</span></span>

<span data-ttu-id="71c90-754">Общие сведения о сборке Windows 17025 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="71c90-754">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-755">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-755">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="71c90-756">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-756">WSL</span></span>
- <span data-ttu-id="71c90-757">Запуск начальных процессов в новой группе процессов переднего плана [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="71c90-757">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="71c90-758">Исправления доставки SIGHUP [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="71c90-758">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="71c90-759">Создание имени виртуального моста по умолчанию, если оно не указано [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="71c90-759">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="71c90-760">Реализовано /proc/sys/kernel/Random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="71c90-760">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="71c90-761">Дополнительные исправления взаимодействия с каналом stdout/stderr.</span><span class="sxs-lookup"><span data-stu-id="71c90-761">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="71c90-762">Заглушка системного вызова syncfs.</span><span class="sxs-lookup"><span data-stu-id="71c90-762">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="71c90-763">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-763">Console</span></span>
- <span data-ttu-id="71c90-764">Исправление входного преобразования VT для консолей сторонних разработчиков [GH 111].</span><span class="sxs-lookup"><span data-stu-id="71c90-764">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-765">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-765">LTP Results:</span></span>
<span data-ttu-id="71c90-766">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-766">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="71c90-767">Сборка 17017</span><span class="sxs-lookup"><span data-stu-id="71c90-767">Build 17017</span></span>

<span data-ttu-id="71c90-768">Общие сведения о сборке Windows 17017 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="71c90-768">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-769">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-769">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="71c90-770">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-770">WSL</span></span>
- <span data-ttu-id="71c90-771">Пропуск пустых заголовков программы ELF [GH 330].</span><span class="sxs-lookup"><span data-stu-id="71c90-771">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="71c90-772">LxssManager разрешено создавать экземпляры WSL для неинтерактивных пользователей (поддержка SSH и запланированных задач) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="71c90-772">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="71c90-773">Поддержка сценариев WSL > Win32 > WSL ("порождение") [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="71c90-773">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="71c90-774">Ограниченная поддержка завершения работы консольных приложений, вызванных посредством взаимодействия [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="71c90-774">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="71c90-775">Поддержка параметров подключения для devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="71c90-775">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="71c90-776">Устранена блокировка Ptrace запуска дочерних процессов [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="71c90-776">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="71c90-777">В EPOLLET отсутствовали некоторые события [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="71c90-777">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="71c90-778">PTRACE_GETSIGINFO возвращает больше данных.</span><span class="sxs-lookup"><span data-stu-id="71c90-778">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="71c90-779">Функция getdents с lseek выдавала неправильные результаты.</span><span class="sxs-lookup"><span data-stu-id="71c90-779">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="71c90-780">Устранены некоторые сценарии, в которых взаимодействующее приложение Win32 переставало отвечать на запросы, ожидая входных данных в канале, который больше не содержал данные.</span><span class="sxs-lookup"><span data-stu-id="71c90-780">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="71c90-781">Поддержка O_ASYNC для файлов tty и pty.</span><span class="sxs-lookup"><span data-stu-id="71c90-781">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="71c90-782">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="71c90-782">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="71c90-783">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-783">Console</span></span>
- <span data-ttu-id="71c90-784">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="71c90-784">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-785">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-785">LTP Results:</span></span>
<span data-ttu-id="71c90-786">выполняется тестирование.</span><span class="sxs-lookup"><span data-stu-id="71c90-786">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="71c90-787">Обновление Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="71c90-787">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="71c90-788">Сборка 16288</span><span class="sxs-lookup"><span data-stu-id="71c90-788">Build 16288</span></span>

<span data-ttu-id="71c90-789">Общие сведения о сборке Windows 16288 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="71c90-789">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-790">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-790">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="71c90-791">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-791">WSL</span></span>
- <span data-ttu-id="71c90-792">Правильная инициализация и отображение UID, GID и режима для дескрипторов файлов сокетов [GH 2490].</span><span class="sxs-lookup"><span data-stu-id="71c90-792">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="71c90-793">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="71c90-793">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="71c90-794">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-794">Console</span></span>
- <span data-ttu-id="71c90-795">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="71c90-795">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-796">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-796">LTP Results:</span></span>
<span data-ttu-id="71c90-797">Изменения с момента выпуска сборки 16273 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-797">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="71c90-798">Сборка 16278</span><span class="sxs-lookup"><span data-stu-id="71c90-798">Build 16278</span></span>

<span data-ttu-id="71c90-799">Общие сведения о сборке Windows 162738 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="71c90-799">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-800">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-800">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="71c90-801">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-801">WSL</span></span>
- <span data-ttu-id="71c90-802">Явная отмена сопоставления сопоставленных представлений разделов с файлами при завершении состояния LX MM [GH 2415].</span><span class="sxs-lookup"><span data-stu-id="71c90-802">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="71c90-803">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="71c90-803">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="71c90-804">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-804">Console</span></span>
- <span data-ttu-id="71c90-805">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="71c90-805">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-806">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-806">LTP Results:</span></span>
<span data-ttu-id="71c90-807">Изменения с момента выпуска сборки 16273 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-807">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="71c90-808">Сборка 16275</span><span class="sxs-lookup"><span data-stu-id="71c90-808">Build 16275</span></span>

<span data-ttu-id="71c90-809">Общие сведения о сборке Windows 162735 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="71c90-809">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-810">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-810">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="71c90-811">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-811">WSL</span></span>
- <span data-ttu-id="71c90-812">В этом выпуске нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-812">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="71c90-813">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-813">Console</span></span>
- <span data-ttu-id="71c90-814">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="71c90-814">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-815">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-815">LTP Results:</span></span>
<span data-ttu-id="71c90-816">Изменения с момента выпуска сборки 16273 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-816">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="71c90-817">Сборка 16273</span><span class="sxs-lookup"><span data-stu-id="71c90-817">Build 16273</span></span>

<span data-ttu-id="71c90-818">Общие сведения о сборке Windows 16273 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-818">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-819">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-819">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="71c90-820">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-820">WSL</span></span>
- <span data-ttu-id="71c90-821">Исправлена проблема, из-за которой DrvFs иногда сообщал о неправильном типе файла для каталогов [GH 2392].</span><span class="sxs-lookup"><span data-stu-id="71c90-821">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="71c90-822">Разрешено создание сокетов NETLINK_KOBJECT_UEVENT для разблокирования программ, использующих uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637].</span><span class="sxs-lookup"><span data-stu-id="71c90-822">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="71c90-823">Добавлена поддержка неблокирующего подключения [GH 903, 1391, 1584, 1585, 1829, 2290, 2314].</span><span class="sxs-lookup"><span data-stu-id="71c90-823">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="71c90-824">Реализован флаг системного вызова клонирования CLONE_FS [GH 2242].</span><span class="sxs-lookup"><span data-stu-id="71c90-824">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="71c90-825">Устранены проблемы, связанные с неправильной обработкой знаков табуляции или кавычек при взаимодействии с NT [GH 1625, 2164].</span><span class="sxs-lookup"><span data-stu-id="71c90-825">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="71c90-826">Устранена ошибка отказа в доступе при попытке повторного запуска экземпляров WSL [GH 651, 2095].</span><span class="sxs-lookup"><span data-stu-id="71c90-826">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="71c90-827">Реализованы фьютексные операции FUTEX_REQUEUE и FUTEX_CMP_REQUEUE [GH 2242].</span><span class="sxs-lookup"><span data-stu-id="71c90-827">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="71c90-828">Исправлены разрешения для различных файлов SysFs [GH 2214].</span><span class="sxs-lookup"><span data-stu-id="71c90-828">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="71c90-829">Устранена проблема, из-за которой стек Haskell переставал отвечать на запросы во время установки [GH 2290].</span><span class="sxs-lookup"><span data-stu-id="71c90-829">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="71c90-830">Реализованы флаги binfmt_misc "C", "O" и "P" [GH 2103].</span><span class="sxs-lookup"><span data-stu-id="71c90-830">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="71c90-831">Добавлены /proc/sys/kernel, /shmmax, /shmmni и /threads-max [GH 1753].</span><span class="sxs-lookup"><span data-stu-id="71c90-831">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="71c90-832">Добавлена частичная поддержка системного вызова ioprio_set [GH 498].</span><span class="sxs-lookup"><span data-stu-id="71c90-832">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="71c90-833">Реализована заглушка SO_REUSEPORT и добавлена поддержка SO_PASSCRED для сокетов NETLINK [GH 69].</span><span class="sxs-lookup"><span data-stu-id="71c90-833">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="71c90-834">Возвращение разных кодов ошибок из RegisterDistribuiton, если дистрибутив в данный момент устанавливается или удаляется.</span><span class="sxs-lookup"><span data-stu-id="71c90-834">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="71c90-835">Обеспечена отмена регистрации частично установленных дистрибутивов WSL с помощью wslconfig.exe.</span><span class="sxs-lookup"><span data-stu-id="71c90-835">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="71c90-836">Устранена ошибка, из-за которой сокет Python переставал отвечать на запросы при выполнении udp::msg_peek.</span><span class="sxs-lookup"><span data-stu-id="71c90-836">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="71c90-837">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="71c90-837">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="71c90-838">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-838">Console</span></span>
- <span data-ttu-id="71c90-839">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="71c90-839">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-840">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-840">LTP Results:</span></span>
<span data-ttu-id="71c90-841">Всего тестов: 1904.</span><span class="sxs-lookup"><span data-stu-id="71c90-841">Total Tests: 1904</span></span><br/>
<span data-ttu-id="71c90-842">Всего пропущенных тестов: 209.</span><span class="sxs-lookup"><span data-stu-id="71c90-842">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="71c90-843">Всего сбоев: 229.</span><span class="sxs-lookup"><span data-stu-id="71c90-843">Total Failures: 229</span></span><br/>
[<span data-ttu-id="71c90-844">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-844">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="71c90-845">Сборка 16257</span><span class="sxs-lookup"><span data-stu-id="71c90-845">Build 16257</span></span>

<span data-ttu-id="71c90-846">Общие сведения о сборке Windows 16257 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-846">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-847">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-847">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="71c90-848">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-848">WSL</span></span>
- <span data-ttu-id="71c90-849">Реализован системный вызов prlimit64.</span><span class="sxs-lookup"><span data-stu-id="71c90-849">Implement prlimit64 system call</span></span>
- <span data-ttu-id="71c90-850">Добавлена поддержка ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688].</span><span class="sxs-lookup"><span data-stu-id="71c90-850">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="71c90-851">Заглушка MSG_MORE для TCP-сокетов [GH 2351].</span><span class="sxs-lookup"><span data-stu-id="71c90-851">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="71c90-852">Исправлено недопустимое поведение вспомогательного вектора AT_EXECFN [GH 2133].</span><span class="sxs-lookup"><span data-stu-id="71c90-852">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="71c90-853">Исправлено поведение копирования и вставки для консоли и tty и добавлена улучшенная обработка полного буфера [GH 2204, 2131].</span><span class="sxs-lookup"><span data-stu-id="71c90-853">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="71c90-854">Установка AT_SECURE в дополнительном векторе для программ set-user-ID и set-group-ID [GH 2031].</span><span class="sxs-lookup"><span data-stu-id="71c90-854">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="71c90-855">Главная конечная точка псевдотерминала не обрабатывала TIOCPGRP [GH 1063].</span><span class="sxs-lookup"><span data-stu-id="71c90-855">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="71c90-856">Исправлена проблема lseek с перемоткой каталогов в LxFs [GH 2310].</span><span class="sxs-lookup"><span data-stu-id="71c90-856">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="71c90-857">Исправлена блокировка /dev/ptmx после интенсивного использования [GH 1882].</span><span class="sxs-lookup"><span data-stu-id="71c90-857">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="71c90-858">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="71c90-858">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="71c90-859">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-859">Console</span></span>
- <span data-ttu-id="71c90-860">Исправлено отображение горизонтальных линий и знаков подчеркивания везде [GH 2168].</span><span class="sxs-lookup"><span data-stu-id="71c90-860">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="71c90-861">Исправлено изменение порядка процессов, усложнявшее закрытие NPM [GH 2170].</span><span class="sxs-lookup"><span data-stu-id="71c90-861">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="71c90-862">Добавлена новая цветовая схема: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/.</span><span class="sxs-lookup"><span data-stu-id="71c90-862">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-863">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-863">LTP Results:</span></span>
<span data-ttu-id="71c90-864">Изменения с момента выпуска сборки 16251 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-864">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="71c90-865">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="71c90-865">Syscall Support</span></span>
<span data-ttu-id="71c90-866">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-866">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="71c90-867">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="71c90-867">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="71c90-868">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="71c90-868">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a>[<span data-ttu-id="71c90-869">Проблема GitHub 2392: WSL не распознает папки Windows…</span><span class="sxs-lookup"><span data-stu-id="71c90-869">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="71c90-870">В сборке 16257 в WSL возникли проблемы при перечислении файлов и папок Windows с помощью `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="71c90-870">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="71c90-871">Эта проблема устранена, и исправление будет выпущено в сборке для программы предварительной оценки в течение недели после 14 августа 2017 года.</span><span class="sxs-lookup"><span data-stu-id="71c90-871">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="71c90-872">Сборка 16251</span><span class="sxs-lookup"><span data-stu-id="71c90-872">Build 16251</span></span>

<span data-ttu-id="71c90-873">Общие сведения о сборке Windows 16251 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-873">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-874">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-874">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="71c90-875">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-875">WSL</span></span>
- <span data-ttu-id="71c90-876">Удален тег бета-версии из дополнительного компонента WSL. Дополнительные сведения см. в этой [записи блога](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/).</span><span class="sxs-lookup"><span data-stu-id="71c90-876">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="71c90-877">Правильная инициализация сохраненных заданных UID и GID для двоичных файлов set-user-ID и set-group-ID при выполнении [GH 962, 1415, 2072].</span><span class="sxs-lookup"><span data-stu-id="71c90-877">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="71c90-878">Добавлена поддержка PTRACE_O_TRACEEXIT в ptrace [GH 555].</span><span class="sxs-lookup"><span data-stu-id="71c90-878">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="71c90-879">В ptrace добавлена поддержка PTRACE_GETFPREGS и PTRACE_GETREGSET с NT_FPREGSET [GH 555].</span><span class="sxs-lookup"><span data-stu-id="71c90-879">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="71c90-880">Исправлена проблема, из-за которой выполнение ptrace останавливалось на пропущенных сигналах.</span><span class="sxs-lookup"><span data-stu-id="71c90-880">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="71c90-881">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="71c90-881">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="71c90-882">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-882">Console</span></span>
- <span data-ttu-id="71c90-883">В этом выпуске нет изменений, связанных с консолью.</span><span class="sxs-lookup"><span data-stu-id="71c90-883">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-884">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-884">LTP Results:</span></span>
<span data-ttu-id="71c90-885">Число пройденных тестов: 768</span><span class="sxs-lookup"><span data-stu-id="71c90-885">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="71c90-886">Число непройденных тестов: 244.</span><span class="sxs-lookup"><span data-stu-id="71c90-886">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="71c90-887">Число пропущенных тестов: 96</span><span class="sxs-lookup"><span data-stu-id="71c90-887">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="71c90-888">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-888">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="71c90-889">Сборка 16241</span><span class="sxs-lookup"><span data-stu-id="71c90-889">Build 16241</span></span>

<span data-ttu-id="71c90-890">Общие сведения о сборке Windows 16241 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-890">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-891">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-891">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="71c90-892">WSL</span><span class="sxs-lookup"><span data-stu-id="71c90-892">WSL</span></span>
- <span data-ttu-id="71c90-893">В этом выпуске нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-893">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="71c90-894">Консоль</span><span class="sxs-lookup"><span data-stu-id="71c90-894">Console</span></span>
- <span data-ttu-id="71c90-895">Исправлено вывода неправильного знака для пересечения линий DEC, о котором первоначально было сообщено [здесь](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/).</span><span class="sxs-lookup"><span data-stu-id="71c90-895">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="71c90-896">Исправлено отсутствие вывода текста в кодовой странице 65001 (UTF8).</span><span class="sxs-lookup"><span data-stu-id="71c90-896">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="71c90-897">Изменения, внесенные в значения RGB одного цвета, не переносятся в другие части палитры при изменении выбора.</span><span class="sxs-lookup"><span data-stu-id="71c90-897">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="71c90-898">Это заметно облегчит использование страницы свойств консоли.</span><span class="sxs-lookup"><span data-stu-id="71c90-898">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="71c90-899">Нажатие клавиш Ctrl+S не работало правильно.</span><span class="sxs-lookup"><span data-stu-id="71c90-899">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="71c90-900">Un-Bold и -Dim полностью отсутствуют в escape-кодах ANSI [GH 2174].</span><span class="sxs-lookup"><span data-stu-id="71c90-900">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="71c90-901">Консоль неправильно поддерживала цветовые темы Vim [GH 1706].</span><span class="sxs-lookup"><span data-stu-id="71c90-901">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="71c90-902">Не удавалось вставить определенные знаки [GH 2149].</span><span class="sxs-lookup"><span data-stu-id="71c90-902">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="71c90-903">Изменение размера расплавления приводило к необычному изменению размера окна Bash, когда что-то было введено в строке редактирования или командной строке [GH ConEmu 1123].</span><span class="sxs-lookup"><span data-stu-id="71c90-903">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="71c90-904">Нажатие клавиш CTRL+L не очищало экран [GH 1978].</span><span class="sxs-lookup"><span data-stu-id="71c90-904">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="71c90-905">Устранена ошибка отрисовки консоли при отображении VT в HDPI [GH 1907].</span><span class="sxs-lookup"><span data-stu-id="71c90-905">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="71c90-906">Японские знаки выглядели необычно со знаком Юникода U+30FB [GH 2146].</span><span class="sxs-lookup"><span data-stu-id="71c90-906">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="71c90-907">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="71c90-907">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="71c90-908">Сборка 16237</span><span class="sxs-lookup"><span data-stu-id="71c90-908">Build 16237</span></span>

<span data-ttu-id="71c90-909">Общие сведения о сборке Windows 16237 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-909">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-910">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-910">Fixed</span></span>
- <span data-ttu-id="71c90-911">Использование атрибутов по умолчанию для файлов без EA в lxfs (root, root, 0000).</span><span class="sxs-lookup"><span data-stu-id="71c90-911">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="71c90-912">Добавлена поддержка дистрибутивов, использующих расширенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="71c90-912">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="71c90-913">Исправлено заполнение записей, возвращаемых getdents и getdents64.</span><span class="sxs-lookup"><span data-stu-id="71c90-913">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="71c90-914">Исправлена проверка разрешений для системного вызова shmctl SHM_STAT [GH 2068].</span><span class="sxs-lookup"><span data-stu-id="71c90-914">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="71c90-915">Исправлено неправильное начальное состояние epoll для tty [GH 2231].</span><span class="sxs-lookup"><span data-stu-id="71c90-915">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="71c90-916">Устранена проблема в DrvFs, из-за которой команда readdir не возвращала все записи [GH 2077].</span><span class="sxs-lookup"><span data-stu-id="71c90-916">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="71c90-917">Исправлена операция LxFs readdir с несвязанными файлами [GH 2077].</span><span class="sxs-lookup"><span data-stu-id="71c90-917">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="71c90-918">Допускается повторное открытие несвязанных файлов DrvFs с помощью procfs.</span><span class="sxs-lookup"><span data-stu-id="71c90-918">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="71c90-919">Добавлено переопределение глобального раздела реестра для отключения функций WSL (взаимодействие и монтирование дисков).</span><span class="sxs-lookup"><span data-stu-id="71c90-919">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="71c90-920">Исправлено неправильное число блокировок в "stat" для DrvFs (и LxFs) [GH 1894].</span><span class="sxs-lookup"><span data-stu-id="71c90-920">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="71c90-921">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="71c90-921">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="71c90-922">Сборка 16232</span><span class="sxs-lookup"><span data-stu-id="71c90-922">Build 16232</span></span>

<span data-ttu-id="71c90-923">Общие сведения о сборке Windows 16232 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-923">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-924">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-924">Fixed</span></span>
- <span data-ttu-id="71c90-925">В этом выпуске нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-925">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="71c90-926">Сборка 16226</span><span class="sxs-lookup"><span data-stu-id="71c90-926">Build 16226</span></span>

<span data-ttu-id="71c90-927">Общие сведения о сборке Windows 16226 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-927">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-928">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-928">Fixed</span></span>
- <span data-ttu-id="71c90-929">Поддержка системных вызовов, связанных с xattr (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="71c90-929">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="71c90-930">Поддержка security.capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="71c90-930">security.capablity xattr support.</span></span>
- <span data-ttu-id="71c90-931">Улучшена совместимость с некоторыми файловыми системами и фильтрами, включая серверы SMB сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="71c90-931">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="71c90-932">[GH 1952]</span><span class="sxs-lookup"><span data-stu-id="71c90-932">[GH #1952]</span></span>
- <span data-ttu-id="71c90-933">Улучшена поддержка заполнителей OneDrive, заполнителей GVFS и сжатых файлов Compact OS.</span><span class="sxs-lookup"><span data-stu-id="71c90-933">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="71c90-934">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="71c90-934">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="71c90-935">Сборка 16215</span><span class="sxs-lookup"><span data-stu-id="71c90-935">Build 16215</span></span>

<span data-ttu-id="71c90-936">Общие сведения о сборке Windows 16215 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-936">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-937">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-937">Fixed</span></span>
- <span data-ttu-id="71c90-938">Для WSL больше не требуется режим разработчика.</span><span class="sxs-lookup"><span data-stu-id="71c90-938">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="71c90-939">Поддержка соединений каталогов в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-939">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="71c90-940">Обработка удаления пакетов appx дистрибутивов WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-940">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="71c90-941">Обновление procfs для отображения частных и общих сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="71c90-941">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="71c90-942">В wslconfig.exe добавлена возможность очистки частично установленных или частично удаленных дистрибутивов.</span><span class="sxs-lookup"><span data-stu-id="71c90-942">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="71c90-943">Добавлена поддержка IP_MTU_DISCOVER для TCP-сокетов.</span><span class="sxs-lookup"><span data-stu-id="71c90-943">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="71c90-944">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="71c90-944">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="71c90-945">Вывод семейства протоколов для маршрутов к AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="71c90-945">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="71c90-946">Улучшения для последовательных устройств [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="71c90-946">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="71c90-947">Сборка 16199</span><span class="sxs-lookup"><span data-stu-id="71c90-947">Build 16199</span></span>

<span data-ttu-id="71c90-948">Общие сведения о сборке Windows 16199 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-948">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-949">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-949">Fixed</span></span>
- <span data-ttu-id="71c90-950">В этих выпусках нет изменений, связанных с WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-950">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="71c90-951">Сборка 16193</span><span class="sxs-lookup"><span data-stu-id="71c90-951">Build 16193</span></span>

<span data-ttu-id="71c90-952">Общие сведения о сборке Windows 16193 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-952">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-953">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-953">Fixed</span></span>
- <span data-ttu-id="71c90-954">Исправлено состояние состязания между отправкой SIGCONT и завершением группы потоков [GH 1973].</span><span class="sxs-lookup"><span data-stu-id="71c90-954">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="71c90-955">Устройства tty и pty изменены для передачи FILE_DEVICE_NAMED_PIPE вместо FILE_DEVICE_CONSOLE [GH 1840].</span><span class="sxs-lookup"><span data-stu-id="71c90-955">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="71c90-956">Исправление SSH для IP_OPTIONS.</span><span class="sxs-lookup"><span data-stu-id="71c90-956">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="71c90-957">Подключение DrvFs перемещено в управляющую программу инициализации [GH 1862, 1968, 1767, 1933].</span><span class="sxs-lookup"><span data-stu-id="71c90-957">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="71c90-958">Добавлена поддержка в DrvFs приведенных ниже символических ссылок NT.</span><span class="sxs-lookup"><span data-stu-id="71c90-958">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="71c90-959">Сборка 16184</span><span class="sxs-lookup"><span data-stu-id="71c90-959">Build 16184</span></span>

<span data-ttu-id="71c90-960">Общие сведения о сборке Windows 16184 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-960">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-961">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-961">Fixed</span></span>
- <span data-ttu-id="71c90-962">Удалена задача обслуживания пакета apt (lxrun.exe /update).</span><span class="sxs-lookup"><span data-stu-id="71c90-962">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="71c90-963">Исправлено отсутствие выходных данных из процессов Windows в Node.js [GH 1840].</span><span class="sxs-lookup"><span data-stu-id="71c90-963">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="71c90-964">Смягчены требования к соответствию в lxcore [GH 1794].</span><span class="sxs-lookup"><span data-stu-id="71c90-964">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="71c90-965">Исправлена обработка флага AT_EMPTY_PATH в ряде системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="71c90-965">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="71c90-966">Исправлена проблема, из-за которой удаление файлов DrvFs с открытыми дескрипторами приводило к неопределенному поведению файла [GH 544, 966, 1357, 1535, 1615].</span><span class="sxs-lookup"><span data-stu-id="71c90-966">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="71c90-967">Теперь /etc/hosts будет наследовать записи из файла hosts Windows (%windir%\System32\Drivers\Etc\hosts) [GH 1495].</span><span class="sxs-lookup"><span data-stu-id="71c90-967">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="71c90-968">Сборка 16179</span><span class="sxs-lookup"><span data-stu-id="71c90-968">Build 16179</span></span>

<span data-ttu-id="71c90-969">Общие сведения о сборке Windows 16179 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-969">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-970">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-970">Fixed</span></span>
- <span data-ttu-id="71c90-971">На этой неделе изменения в WSL отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-971">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="71c90-972">Сборка 16176</span><span class="sxs-lookup"><span data-stu-id="71c90-972">Build 16176</span></span>

<span data-ttu-id="71c90-973">Общие сведения о сборке Windows 16176 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-973">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-974">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-974">Fixed</span></span>

- <span data-ttu-id="71c90-975">[Включена поддержка последовательных устройств](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/).</span><span class="sxs-lookup"><span data-stu-id="71c90-975">[Enabled serial support](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)</span></span>
- <span data-ttu-id="71c90-976">Добавлен параметр IP-сокета IP_OPTIONS [GH 1116].</span><span class="sxs-lookup"><span data-stu-id="71c90-976">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="71c90-977">Реализована функция pwritev (при передаче файла в nginx/PHP-FPM) [GH 1506].</span><span class="sxs-lookup"><span data-stu-id="71c90-977">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="71c90-978">Добавлены параметры IP-сокета IP_MULTICAST_IF и IPV6_MULTICAST_IF [GH 990].</span><span class="sxs-lookup"><span data-stu-id="71c90-978">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="71c90-979">Поддержка параметров сокета IP_MULTICAST_LOOP и IPV6_MULTICAST_LOOP [GH 1678].</span><span class="sxs-lookup"><span data-stu-id="71c90-979">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="71c90-980">Добавлен параметр сокета IP(V6)_MTU для приложений node, traceroute, dig, nslookup, host.</span><span class="sxs-lookup"><span data-stu-id="71c90-980">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="71c90-981">Добавлен параметр IP-сокета IPV6_UNICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="71c90-981">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- <span data-ttu-id="71c90-982">[Улучшения файловой системы](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/).</span><span class="sxs-lookup"><span data-stu-id="71c90-982">[Filesystem Improvements](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)</span></span>
    * <span data-ttu-id="71c90-983">Разрешено подключение путей UNC.</span><span class="sxs-lookup"><span data-stu-id="71c90-983">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="71c90-984">Включена поддержка CDFS в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-984">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="71c90-985">Правильная обработка разрешений для сетевых файловых систем в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-985">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="71c90-986">Добавлена поддержка удаленных дисков в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-986">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="71c90-987">Включена поддержка файловой системы FAT в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-987">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="71c90-988">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="71c90-988">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-989">Результаты LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-989">LTP Results</span></span>
<span data-ttu-id="71c90-990">Изменения с момента выпуска сборки 15042 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-990">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="71c90-991">Сборка 16170</span><span class="sxs-lookup"><span data-stu-id="71c90-991">Build 16170</span></span>

<span data-ttu-id="71c90-992">Общие сведения о сборке Windows 16170 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-992">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="71c90-993">Мы опубликовали новую[запись блога](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/), в которой обсуждаем наши усилия по тестированию WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-993">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="71c90-994">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-994">Fixed</span></span>

- <span data-ttu-id="71c90-995">Поддержка параметров сокета IP_ADD_MEMBERSHIP и IPV6_ADD_MEMBERSHIP [GH 1678].</span><span class="sxs-lookup"><span data-stu-id="71c90-995">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="71c90-996">Добавлена поддержка PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="71c90-996">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="71c90-997">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="71c90-997">[GH 1692]</span></span>
- <span data-ttu-id="71c90-998">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="71c90-998">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-999">Результаты LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-999">LTP Results</span></span>
<span data-ttu-id="71c90-1000">Изменения с момента выпуска сборки 15042 отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="71c90-1000">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="71c90-1001">Сборка 15046 для Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="71c90-1001">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="71c90-1002">В обновление Creators Update для Windows 10 больше не планируется добавлять какие-либо исправления или функции WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1002">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="71c90-1003">Публикация заметок о выпуске WSL будет возобновлена в ближайшие недели, чтобы охватить дополнения, запланированные в следующих основных версиях в Центре обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-1003">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="71c90-1004">Общие сведения о сборке Windows 15046 и будущих выпусках для программы предварительной оценки доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1004">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="71c90-1005">Сборка 15042</span><span class="sxs-lookup"><span data-stu-id="71c90-1005">Build 15042</span></span>

<span data-ttu-id="71c90-1006">Общие сведения о сборке Windows 15042 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1006">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1007">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1007">Fixed</span></span>

- <span data-ttu-id="71c90-1008">Устранена взаимоблокировка при удалении пути, завершающегося "..".</span><span class="sxs-lookup"><span data-stu-id="71c90-1008">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="71c90-1009">Устранена проблема, из-за которой функция FIONBIO не возвращала 0 при успешном выполнении [GH 1683].</span><span class="sxs-lookup"><span data-stu-id="71c90-1009">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="71c90-1010">Устранена проблема с чтением сокетов датаграмм INET нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="71c90-1010">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="71c90-1011">Устранена возможная взаимоблокировка из-за состояния состязания при поиске DrvFs в DrvFs [GH 1675].</span><span class="sxs-lookup"><span data-stu-id="71c90-1011">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="71c90-1012">Расширена поддержка вспомогательных данных сокетов UNIX, SCM_CREDENTIALS и SCM_RIGHTS [GH 514, 613, 1326].</span><span class="sxs-lookup"><span data-stu-id="71c90-1012">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="71c90-1013">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="71c90-1013">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1014">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1014">LTP Results:</span></span>
<span data-ttu-id="71c90-1015">Число пройденных тестов: 737.</span><span class="sxs-lookup"><span data-stu-id="71c90-1015">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="71c90-1016">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="71c90-1016">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="71c90-1017">Сборка 15031</span><span class="sxs-lookup"><span data-stu-id="71c90-1017">Build 15031</span></span>

<span data-ttu-id="71c90-1018">Общие сведения о сборке Windows 15031 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1018">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1019">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1019">Fixed</span></span>

- <span data-ttu-id="71c90-1020">Исправлена ошибка, из-за которой поведение time(2) иногда было неправильным.</span><span class="sxs-lookup"><span data-stu-id="71c90-1020">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="71c90-1021">Исправлена проблема, из-за которой системный вызов \*SIGPROCMASK мог повредить маску сигнала.</span><span class="sxs-lookup"><span data-stu-id="71c90-1021">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="71c90-1022">Теперь в уведомлении о создании процесса WSL возвращается полная длина командной строки.</span><span class="sxs-lookup"><span data-stu-id="71c90-1022">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="71c90-1023">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="71c90-1023">[GH 1632]</span></span>
- <span data-ttu-id="71c90-1024">Теперь WSL сообщает о выходе из потока посредством ptrace, если GDB перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="71c90-1024">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="71c90-1025">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="71c90-1025">[GH 1196]</span></span>
- <span data-ttu-id="71c90-1026">Исправлена ошибка, из-за которой устройства pty переставали отвечать на запросы после интенсивного ввода-вывода tmux.</span><span class="sxs-lookup"><span data-stu-id="71c90-1026">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="71c90-1027">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="71c90-1027">[GH 1358]</span></span>
- <span data-ttu-id="71c90-1028">Исправлена проверка времени ожидания во многих системных вызовах (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create).</span><span class="sxs-lookup"><span data-stu-id="71c90-1028">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="71c90-1029">Добавлена поддержка eventfd EFD_SEMAPHORE [GH 452].</span><span class="sxs-lookup"><span data-stu-id="71c90-1029">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="71c90-1030">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="71c90-1030">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1031">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1031">LTP Results:</span></span>
<span data-ttu-id="71c90-1032">Число пройденных тестов: 737.</span><span class="sxs-lookup"><span data-stu-id="71c90-1032">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="71c90-1033">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="71c90-1033">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="71c90-1034">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1034">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="71c90-1035">Сборка 15025</span><span class="sxs-lookup"><span data-stu-id="71c90-1035">Build 15025</span></span>

<span data-ttu-id="71c90-1036">Общие сведения о сборке Windows 15025 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1036">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1037">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1037">Fixed</span></span>

- <span data-ttu-id="71c90-1038">Исправлена ошибка, которая нарушала работу grep 2.27 [GH 1578].</span><span class="sxs-lookup"><span data-stu-id="71c90-1038">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="71c90-1039">Реализован флаг EFD_SEMAPHORE для системного вызова eventfd2 [GH 452].</span><span class="sxs-lookup"><span data-stu-id="71c90-1039">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="71c90-1040">Реализован файл /proc/[pid]/net/ipv6_route [GH 1608].</span><span class="sxs-lookup"><span data-stu-id="71c90-1040">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="71c90-1041">Поддержка управляемого сигналами ввода-вывода для сокетов потоков UNIX [GH 393, 68].</span><span class="sxs-lookup"><span data-stu-id="71c90-1041">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="71c90-1042">Поддержка F_GETPIPE_SZ и F_SETPIPE_SZ [GH 1012].</span><span class="sxs-lookup"><span data-stu-id="71c90-1042">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="71c90-1043">Реализация системного вызова recvmmsg() [GH 1531].</span><span class="sxs-lookup"><span data-stu-id="71c90-1043">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="71c90-1044">Исправлена ошибка, из-за которой функция epoll_wait() не ожидала выполнения [GH 1609].</span><span class="sxs-lookup"><span data-stu-id="71c90-1044">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="71c90-1045">Реализация /proc/version_signature.</span><span class="sxs-lookup"><span data-stu-id="71c90-1045">Implement /proc/version_signature</span></span>
- <span data-ttu-id="71c90-1046">Теперь системный вызов Tee возвращает ошибку, если оба дескриптора файла ссылаются на один и тот же канал.</span><span class="sxs-lookup"><span data-stu-id="71c90-1046">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="71c90-1047">Реализовано правильное поведение SO_PEERCRED для сокетов UNIX.</span><span class="sxs-lookup"><span data-stu-id="71c90-1047">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="71c90-1048">Исправлена недопустимая обработка параметров системного вызова tkill.</span><span class="sxs-lookup"><span data-stu-id="71c90-1048">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="71c90-1049">Внесены изменения для увеличения производительности DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-1049">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="71c90-1050">Незначительное исправление блокировки ввода-вывода Ruby.</span><span class="sxs-lookup"><span data-stu-id="71c90-1050">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="71c90-1051">Исправлена проблема, из-за которой функция recvmsg() возвращала EINVAL для флага MSG_DONTWAIT для сокетов INET [GH 1296].</span><span class="sxs-lookup"><span data-stu-id="71c90-1051">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="71c90-1052">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="71c90-1052">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1053">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1053">LTP Results:</span></span>
<span data-ttu-id="71c90-1054">Число пройденных тестов: 732.</span><span class="sxs-lookup"><span data-stu-id="71c90-1054">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="71c90-1055">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="71c90-1055">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="71c90-1056">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1056">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="71c90-1057">Сборка 15019</span><span class="sxs-lookup"><span data-stu-id="71c90-1057">Build 15019</span></span>

<span data-ttu-id="71c90-1058">Общие сведения о сборке Windows 15019 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1058">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1059">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1059">Fixed</span></span>

- <span data-ttu-id="71c90-1060">Исправлена ошибка, из-за которой отображались неправильные данные об использовании ЦП в procfs для таких инструментов, как htop [GH 823, 945, 971].</span><span class="sxs-lookup"><span data-stu-id="71c90-1060">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="71c90-1061">Теперь при вызове Open() с O_TRUNC для существующего файла inotify теперь создает IN_MODIFY до IN_OPEN.</span><span class="sxs-lookup"><span data-stu-id="71c90-1061">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="71c90-1062">Исправление getsockopt SO_ERROR в сокетах UNIX для включения возможностей postgress [GH 61, 1354].</span><span class="sxs-lookup"><span data-stu-id="71c90-1062">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="71c90-1063">Реализация /proc/sys/net/core/somaxconn для языка GO.</span><span class="sxs-lookup"><span data-stu-id="71c90-1063">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="71c90-1064">Теперь фоновая задача обновления пакета apt-get запускается из представления в скрытом режиме.</span><span class="sxs-lookup"><span data-stu-id="71c90-1064">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="71c90-1065">Очищена область для IPv6-адреса localhost (сбой (Spring-Framework(Java)).</span><span class="sxs-lookup"><span data-stu-id="71c90-1065">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="71c90-1066">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="71c90-1066">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1067">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1067">LTP Results:</span></span>
<span data-ttu-id="71c90-1068">Число пройденных тестов: 714.</span><span class="sxs-lookup"><span data-stu-id="71c90-1068">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="71c90-1069">Число непройденных тестов (неудачных, пропущенных и т. д.): 249.</span><span class="sxs-lookup"><span data-stu-id="71c90-1069">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="71c90-1070">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1070">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="71c90-1071">Сборка 15014</span><span class="sxs-lookup"><span data-stu-id="71c90-1071">Build 15014</span></span>

<span data-ttu-id="71c90-1072">Общие сведения о сборке Windows 15014 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="71c90-1072">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1073">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1073">Fixed</span></span>

- <span data-ttu-id="71c90-1074">Нажатие клавиш CTRL+C теперь работает ожидаемым образом.</span><span class="sxs-lookup"><span data-stu-id="71c90-1074">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="71c90-1075">Теперь htop и ps auxw показывают правильные данные об использовании ресурсов (GH 516).</span><span class="sxs-lookup"><span data-stu-id="71c90-1075">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="71c90-1076">Простое преобразование исключений NT в сигналы.</span><span class="sxs-lookup"><span data-stu-id="71c90-1076">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="71c90-1077">(GH 513)</span><span class="sxs-lookup"><span data-stu-id="71c90-1077">(GH #513)</span></span>
- <span data-ttu-id="71c90-1078">Теперь при нехватке пространства fallocate завершается ошибкой ENOSPC вместо EINVAL (GH 1571).</span><span class="sxs-lookup"><span data-stu-id="71c90-1078">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="71c90-1079">Добавлен /proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="71c90-1079">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="71c90-1080">Реализованы системные вызовы semop и semtimedop.</span><span class="sxs-lookup"><span data-stu-id="71c90-1080">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="71c90-1081">Устранены ошибки nslookup, связанные с параметрами сокета IP_RECVTOS и IPV6_RECVTCLASS (GH 69).</span><span class="sxs-lookup"><span data-stu-id="71c90-1081">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="71c90-1082">Поддержка параметров сокета IP_RECVTTL и IPV6_RECVHOPLIMIT.</span><span class="sxs-lookup"><span data-stu-id="71c90-1082">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="71c90-1083">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="71c90-1083">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1084">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1084">LTP Results:</span></span>
<span data-ttu-id="71c90-1085">Число пройденных тестов: 709.</span><span class="sxs-lookup"><span data-stu-id="71c90-1085">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="71c90-1086">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="71c90-1086">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="71c90-1087">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1087">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="71c90-1088">Сводка по системным вызовам</span><span class="sxs-lookup"><span data-stu-id="71c90-1088">Syscall Summary</span></span>
<span data-ttu-id="71c90-1089">Всего системных вызовов: 384</span><span class="sxs-lookup"><span data-stu-id="71c90-1089">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="71c90-1090">Всего реализовано: 235.</span><span class="sxs-lookup"><span data-stu-id="71c90-1090">Total Implemented: 235</span></span> </br>
<span data-ttu-id="71c90-1091">Всего заглушено: 22</span><span class="sxs-lookup"><span data-stu-id="71c90-1091">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="71c90-1092">Всего не реализовано: 127</span><span class="sxs-lookup"><span data-stu-id="71c90-1092">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="71c90-1093">Подробная разбивка</span><span class="sxs-lookup"><span data-stu-id="71c90-1093">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="71c90-1094">Сборка 15007</span><span class="sxs-lookup"><span data-stu-id="71c90-1094">Build 15007</span></span>

<span data-ttu-id="71c90-1095">Общие сведения о сборке Windows 15007 доступны в [блоге о Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="71c90-1095">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="71c90-1096">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="71c90-1096">Known Issue</span></span>

- <span data-ttu-id="71c90-1097">Существует известная ошибка, из-за которой консоль не распознает некоторые клавиши CTRL+<key>.</span><span class="sxs-lookup"><span data-stu-id="71c90-1097">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="71c90-1098">Например, это может быть сочетание CTRL+C, которое будет функционировать как обычное нажатие клавиши C.</span><span class="sxs-lookup"><span data-stu-id="71c90-1098">This includes the ctrl-c command which will act as a normal 'c' keypress.</span></span>

  - <span data-ttu-id="71c90-1099">Возможное решение. Сопоставьте альтернативную клавишу с клавишами CTRL+C.</span><span class="sxs-lookup"><span data-stu-id="71c90-1099">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="71c90-1100">Например, чтобы сопоставить клавиши CTRL+K с CTRL+C, выполните следующее: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="71c90-1100">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="71c90-1101">Это сопоставление действует в пределах терминала и должно выполняться *при каждом* запуске Bash.</span><span class="sxs-lookup"><span data-stu-id="71c90-1101">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="71c90-1102">Пользователи могут изучить этот параметр, чтобы включить его в `.bashrc`.</span><span class="sxs-lookup"><span data-stu-id="71c90-1102">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="71c90-1103">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1103">Fixed</span></span>

- <span data-ttu-id="71c90-1104">Исправлена ошибка, из-за которой подсистема WSL потребляла 100 % ресурсов ядра ЦП.</span><span class="sxs-lookup"><span data-stu-id="71c90-1104">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="71c90-1105">Теперь поддерживаются параметры сокета IP_PKTINFO и IPV6_RECVPKTINFO.</span><span class="sxs-lookup"><span data-stu-id="71c90-1105">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="71c90-1106">(GH 851, 987)</span><span class="sxs-lookup"><span data-stu-id="71c90-1106">(GH #851, 987)</span></span>
- <span data-ttu-id="71c90-1107">Усечение физического адреса сетевого интерфейса до 16 байтов в lxcore (GH #1452, 1414, 1343, 468, 308).</span><span class="sxs-lookup"><span data-stu-id="71c90-1107">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="71c90-1108">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="71c90-1108">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1109">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1109">LTP Results:</span></span>
<span data-ttu-id="71c90-1110">Число пройденных тестов: 709.</span><span class="sxs-lookup"><span data-stu-id="71c90-1110">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="71c90-1111">Число непройденных тестов (неудачных, пропущенных и т. д.): 255.</span><span class="sxs-lookup"><span data-stu-id="71c90-1111">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="71c90-1112">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1112">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="71c90-1113">Сборка 15002</span><span class="sxs-lookup"><span data-stu-id="71c90-1113">Build 15002</span></span>

<span data-ttu-id="71c90-1114">Общие сведения о сборке Windows 15002 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1114">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="71c90-1115">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="71c90-1115">Known Issue</span></span>

<span data-ttu-id="71c90-1116">Две известные проблемы:</span><span class="sxs-lookup"><span data-stu-id="71c90-1116">Two known issues:</span></span>
- <span data-ttu-id="71c90-1117">Существует известная ошибка, из-за которой консоль не распознает некоторые клавиши CTRL+<key>.</span><span class="sxs-lookup"><span data-stu-id="71c90-1117">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="71c90-1118">Например, это может быть сочетание CTRL+C, которое будет функционировать как обычное нажатие клавиши C.</span><span class="sxs-lookup"><span data-stu-id="71c90-1118">This includes the ctrl-c command which will act as a normal 'c' keypress.</span></span>

  - <span data-ttu-id="71c90-1119">Возможное решение. Сопоставьте альтернативную клавишу с клавишами CTRL+C.</span><span class="sxs-lookup"><span data-stu-id="71c90-1119">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="71c90-1120">Например, чтобы сопоставить клавиши CTRL+K с CTRL+C, выполните следующее: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="71c90-1120">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="71c90-1121">Это сопоставление действует в пределах терминала и должно выполняться *при каждом* запуске Bash.</span><span class="sxs-lookup"><span data-stu-id="71c90-1121">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="71c90-1122">Пользователи могут изучить этот параметр, чтобы включить его в `.bashrc`.</span><span class="sxs-lookup"><span data-stu-id="71c90-1122">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="71c90-1123">Во время выполнения WSL системный поток потребляет 100 % ресурсов ядра ЦП.</span><span class="sxs-lookup"><span data-stu-id="71c90-1123">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="71c90-1124">Первопричина устранена и исправлена внутри компонента.</span><span class="sxs-lookup"><span data-stu-id="71c90-1124">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="71c90-1125">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1125">Fixed</span></span>

- <span data-ttu-id="71c90-1126">Все сеансы Bash теперь должны создаваться на одном уровне разрешений.</span><span class="sxs-lookup"><span data-stu-id="71c90-1126">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="71c90-1127">Попытка запустить сеанс на другом уровне будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="71c90-1127">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="71c90-1128">Это означает, что консоль администратора и консоль пользователя, не являющегося администратором, не могут работать одновременно.</span><span class="sxs-lookup"><span data-stu-id="71c90-1128">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="71c90-1129">(GH 626)</span><span class="sxs-lookup"><span data-stu-id="71c90-1129">(GH #626)</span></span>
<br/>
- <span data-ttu-id="71c90-1130">Реализованы следующие сообщения NETLINK_ROUTE (требуются права администратора Windows):</span><span class="sxs-lookup"><span data-stu-id="71c90-1130">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="71c90-1131">RTM_NEWADDR (поддерживает `ip addr add`);</span><span class="sxs-lookup"><span data-stu-id="71c90-1131">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="71c90-1132">RTM_NEWROUTE (поддерживает `ip route add`);</span><span class="sxs-lookup"><span data-stu-id="71c90-1132">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="71c90-1133">RTM_DELADDR (поддерживает `ip addr del`);</span><span class="sxs-lookup"><span data-stu-id="71c90-1133">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="71c90-1134">RTM_DELROUTE (поддерживает `ip route del`).</span><span class="sxs-lookup"><span data-stu-id="71c90-1134">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="71c90-1135">Проверка запланированных задач для пакетов, которые необходимо обновить, больше не будет выполняться при лимитном подключении (GH 1371).</span><span class="sxs-lookup"><span data-stu-id="71c90-1135">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="71c90-1136">Исправлена ошибка, из-за которой канал переставал отвечать на запросы, например bash -c "ls -alR /" | bash -c "cat" (GH 1214).</span><span class="sxs-lookup"><span data-stu-id="71c90-1136">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="71c90-1137">Реализован параметр сокета TCP_KEEPCNT (GH 843).</span><span class="sxs-lookup"><span data-stu-id="71c90-1137">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="71c90-1138">Реализован параметр сокета INET IP_MTU_DISCOVER (GH 720, 717, 170, 69).</span><span class="sxs-lookup"><span data-stu-id="71c90-1138">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="71c90-1139">Удалены устаревшие функции для запуска двоичных файлов NT из init с помощью поиска по пути NT.</span><span class="sxs-lookup"><span data-stu-id="71c90-1139">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="71c90-1140">(GH 1325)</span><span class="sxs-lookup"><span data-stu-id="71c90-1140">(GH #1325)</span></span>
- <span data-ttu-id="71c90-1141">Исправлен режим /dev/kmsg для разрешения группового и другого доступа на чтение (0644) (GH 1321).</span><span class="sxs-lookup"><span data-stu-id="71c90-1141">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="71c90-1142">Реализован файл /proc/sys/kernel/random/uuid [GH 1092].</span><span class="sxs-lookup"><span data-stu-id="71c90-1142">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="71c90-1143">Исправлена ошибка, из-за которой время начала процесса отображалось как 2432 год (GH 974).</span><span class="sxs-lookup"><span data-stu-id="71c90-1143">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="71c90-1144">Переменная среды TERM по умолчанию заменена xterm-256color (GH 1446).</span><span class="sxs-lookup"><span data-stu-id="71c90-1144">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="71c90-1145">Изменен способ вычисления фиксации процесса во время ветвления процесса.</span><span class="sxs-lookup"><span data-stu-id="71c90-1145">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="71c90-1146">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="71c90-1146">(GH #1286)</span></span>
- <span data-ttu-id="71c90-1147">Реализован файл /proc/sys/VM/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="71c90-1147">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="71c90-1148">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="71c90-1148">(GH #1286)</span></span>
- <span data-ttu-id="71c90-1149">Реализован файл /proc/net/route (GH 69).</span><span class="sxs-lookup"><span data-stu-id="71c90-1149">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="71c90-1150">Исправлена ошибка, из-за которой имя ярлыка было неправильно локализовано (GH 696).</span><span class="sxs-lookup"><span data-stu-id="71c90-1150">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="71c90-1151">Исправлена логика анализа ELF, которая неправильно проверяла заголовки программ, которые должны быть меньше или равны PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="71c90-1151">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="71c90-1152">(GH 1048)</span><span class="sxs-lookup"><span data-stu-id="71c90-1152">(GH #1048)</span></span>
- <span data-ttu-id="71c90-1153">Реализован обратный вызов statfs для procfs, sysfs, cgroupfs и binfmtf (GH 1378).</span><span class="sxs-lookup"><span data-stu-id="71c90-1153">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="71c90-1154">Исправлена проблема, из-за которой окна AptPackageIndexUpdate не закрывались (GH 1184, также обсуждается в GH 1193).</span><span class="sxs-lookup"><span data-stu-id="71c90-1154">Fixed AptPackageIndexUpdate windows that won't close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="71c90-1155">Добавлена поддержка ADDR_NO_RANDOMIZE в ASLR personality.</span><span class="sxs-lookup"><span data-stu-id="71c90-1155">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="71c90-1156">[GH 1148, 1128]</span><span class="sxs-lookup"><span data-stu-id="71c90-1156">(GH #1148, 1128)</span></span>
- <span data-ttu-id="71c90-1157">Улучшена функция PTRACE_GETSIGINFO для SIGSEGV для обеспечения правильных трассировок стека GDB во время операций AV (GH 875).</span><span class="sxs-lookup"><span data-stu-id="71c90-1157">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="71c90-1158">Анализ ELF больше не завершается ошибкой для двоичных файлов patchelf.</span><span class="sxs-lookup"><span data-stu-id="71c90-1158">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="71c90-1159">(GH 471)</span><span class="sxs-lookup"><span data-stu-id="71c90-1159">(GH #471)</span></span>
- <span data-ttu-id="71c90-1160">DNS-сервер VPN добавлен в /etc/resolv.conf (GH 416, 1350).</span><span class="sxs-lookup"><span data-stu-id="71c90-1160">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="71c90-1161">Улучшено закрытие TCP-подключений для более надежной передачи данных.</span><span class="sxs-lookup"><span data-stu-id="71c90-1161">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="71c90-1162">(GH 610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="71c90-1162">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="71c90-1163">Теперь возвращается правильный код ошибки при открытии слишком большого числа файлов (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="71c90-1163">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="71c90-1164">[GH 1126, 2090]</span><span class="sxs-lookup"><span data-stu-id="71c90-1164">(GH #1126, 2090)</span></span>
- <span data-ttu-id="71c90-1165">Журнал аудита Windows теперь отображает имя образа при аудите процесса создания.</span><span class="sxs-lookup"><span data-stu-id="71c90-1165">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="71c90-1166">Теперь запуск bash.exe из окна Bash корректно завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="71c90-1166">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="71c90-1167">Добавлено сообщение об ошибке, когда служба взаимодействия не может получить доступ к рабочему каталогу в LxFs (например, notepad.exe. bashrc).</span><span class="sxs-lookup"><span data-stu-id="71c90-1167">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="71c90-1168">Исправлена проблема, из-за которой путь Windows в WSL был усеченным.</span><span class="sxs-lookup"><span data-stu-id="71c90-1168">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="71c90-1169">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="71c90-1169">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1170">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1170">LTP Results:</span></span>
<span data-ttu-id="71c90-1171">Число пройденных тестов: 690.</span><span class="sxs-lookup"><span data-stu-id="71c90-1171">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="71c90-1172">Число непройденных тестов (неудачных, пропущенных и т. д.): 274.</span><span class="sxs-lookup"><span data-stu-id="71c90-1172">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="71c90-1173">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1173">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="71c90-1174">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="71c90-1174">Syscall Support</span></span>
<span data-ttu-id="71c90-1175">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1175">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="71c90-1176">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="71c90-1176">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="71c90-1177">Сборка 14986</span><span class="sxs-lookup"><span data-stu-id="71c90-1177">Build 14986</span></span>

<span data-ttu-id="71c90-1178">Общие сведения о сборке Windows 14986 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1178">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1179">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1179">Fixed</span></span>

- <span data-ttu-id="71c90-1180">Исправлены ошибки NETLINK и PTY IOCTL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1180">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="71c90-1181">Теперь отображается версия ядра 4.4.0-43 для обеспечения согласованности с Xenial.</span><span class="sxs-lookup"><span data-stu-id="71c90-1181">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="71c90-1182">Теперь Bash.exe запускается, когда ввод направляется в "nul:" (GH 1259).</span><span class="sxs-lookup"><span data-stu-id="71c90-1182">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="71c90-1183">Теперь идентификаторы потоков отображаются правильно в procfs (GH 967).</span><span class="sxs-lookup"><span data-stu-id="71c90-1183">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="71c90-1184">Теперь в inotify_add_watch() поддерживаются флаги IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR (GH 1280).</span><span class="sxs-lookup"><span data-stu-id="71c90-1184">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="71c90-1185">Реализован timer_create и связанные системные вызовы.</span><span class="sxs-lookup"><span data-stu-id="71c90-1185">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="71c90-1186">Это обеспечивает поддержку GHC (GH 307).</span><span class="sxs-lookup"><span data-stu-id="71c90-1186">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="71c90-1187">Исправлена проблема, из-за которой проверка связи возвращала время 0,000 мс (GH 1296).</span><span class="sxs-lookup"><span data-stu-id="71c90-1187">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="71c90-1188">Возвращается правильный код ошибки при открытии слишком большого числа файлов.</span><span class="sxs-lookup"><span data-stu-id="71c90-1188">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="71c90-1189">Исправлена проблема в WSL, из-за которой запрос NETLINK на данные сетевого интерфейса завершался ошибкой EINVAL, если аппаратный адрес интерфейса был 32-байтовым (например, интерфейс Teredo).</span><span class="sxs-lookup"><span data-stu-id="71c90-1189">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="71c90-1190">Обратите внимание на то, что служебная программа Linux "ip" содержит ошибку, из-за которой произойдет сбой, если WSL сообщит 32-байтовый адрес оборудования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1190">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="71c90-1191">Это ошибка в "ip", а не в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1191">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="71c90-1192">В служебной программе ip прописана в коде длина строкового буфера, используемого для вывода аппаратного адреса, и этот буфер слишком мал для вывода 32-байтового аппаратного адреса.</span><span class="sxs-lookup"><span data-stu-id="71c90-1192">The "ip" utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="71c90-1193">Дополнительные исправления и улучшения.</span><span class="sxs-lookup"><span data-stu-id="71c90-1193">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1194">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1194">LTP Results:</span></span>
<span data-ttu-id="71c90-1195">Число пройденных тестов: 669.</span><span class="sxs-lookup"><span data-stu-id="71c90-1195">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="71c90-1196">Число непройденных тестов (неудачных, пропущенных и т. д.): 258</span><span class="sxs-lookup"><span data-stu-id="71c90-1196">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="71c90-1197">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1197">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="71c90-1198">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="71c90-1198">Syscall Support</span></span>
<span data-ttu-id="71c90-1199">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1199">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="71c90-1200">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="71c90-1200">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="71c90-1201">Сборка 14971</span><span class="sxs-lookup"><span data-stu-id="71c90-1201">Build 14971</span></span>

<span data-ttu-id="71c90-1202">Общие сведения о сборке Windows 14971 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1202">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1203">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1203">Fixed</span></span>

 - <span data-ttu-id="71c90-1204">Из-за независящих от нас обстоятельств в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="71c90-1204">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="71c90-1205">Регулярный выпуск плановых обновлений будет возобновлен в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="71c90-1205">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1206">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1206">LTP Results:</span></span>
<span data-ttu-id="71c90-1207">без изменений с момента выпуска сборки 14965.</span><span class="sxs-lookup"><span data-stu-id="71c90-1207">Unchanged from 14965</span></span> </br>
<span data-ttu-id="71c90-1208">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="71c90-1208">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="71c90-1209">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="71c90-1209">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="71c90-1210">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1210">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="71c90-1211">Сборка 14965</span><span class="sxs-lookup"><span data-stu-id="71c90-1211">Build 14965</span></span>

<span data-ttu-id="71c90-1212">Общие сведения о сборке Windows 14965 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1212">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1213">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1213">Fixed</span></span>

- <span data-ttu-id="71c90-1214">Поддержка RTM_GETLINK и RTM_GETADDR для NETLINK_ROUTE в сокетах NETLINK (GH 468).</span><span class="sxs-lookup"><span data-stu-id="71c90-1214">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="71c90-1215">Применение команд ifconfig и ip для перечисления сетей.</span><span class="sxs-lookup"><span data-stu-id="71c90-1215">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="71c90-1216">Дополнительные сведения см. в нашей [записи блога о сетях WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1216">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="71c90-1217">Теперь /sbin добавляется в путь пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71c90-1217">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="71c90-1218">Теперь путь пользователя NT по умолчанию добавляется к пути WSL (т. е. теперь можно ввести notepad.exe, не добавляя System32 в путь Linux).</span><span class="sxs-lookup"><span data-stu-id="71c90-1218">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="71c90-1219">Добавлена поддержка /proc/sys/kernel/cap_last_cap.</span><span class="sxs-lookup"><span data-stu-id="71c90-1219">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="71c90-1220">Теперь двоичные файлы NT можно запускать из WSL, если текущий рабочий каталог содержит знаки, отличные от ANSI (GH 1254).</span><span class="sxs-lookup"><span data-stu-id="71c90-1220">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="71c90-1221">Разрешено завершение работы при отключении сокета потока UNIX.</span><span class="sxs-lookup"><span data-stu-id="71c90-1221">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="71c90-1222">Добавлена поддержка PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="71c90-1222">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="71c90-1223">Добавлена поддержка CLONE_PARENT.</span><span class="sxs-lookup"><span data-stu-id="71c90-1223">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="71c90-1224">Исправлена ошибка, из-за которой канал переставал отвечать на запросы, например bash -c "ls -alR /" | bash -c "cat" (GH 1214).</span><span class="sxs-lookup"><span data-stu-id="71c90-1224">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="71c90-1225">Обработка запросов на подключение к текущему терминалу.</span><span class="sxs-lookup"><span data-stu-id="71c90-1225">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="71c90-1226">Файл /proc/<pid>/oom_score_adj помечен как записываемый.</span><span class="sxs-lookup"><span data-stu-id="71c90-1226">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="71c90-1227">Добавлена папку /sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="71c90-1227">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="71c90-1228">Функция sched_setaffinity должна возвращать значение маски битов сходства.</span><span class="sxs-lookup"><span data-stu-id="71c90-1228">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="71c90-1229">Исправлена логика проверки ELF, которая неправильно предполагала, что пути интерпретатора должны содержать менее 64 знаков.</span><span class="sxs-lookup"><span data-stu-id="71c90-1229">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="71c90-1230">(GH 743)</span><span class="sxs-lookup"><span data-stu-id="71c90-1230">(GH #743)</span></span>
- <span data-ttu-id="71c90-1231">Открытые дескрипторы файлов могут оставаться открытыми в окне консоли (GH 1187).</span><span class="sxs-lookup"><span data-stu-id="71c90-1231">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="71c90-1232">Устранена ошибка, из-за которой происходил сбой rename(), если имя цели содержало конечную косую черту (GH 1008).</span><span class="sxs-lookup"><span data-stu-id="71c90-1232">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="71c90-1233">Реализован файл /proc/net/dev.</span><span class="sxs-lookup"><span data-stu-id="71c90-1233">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="71c90-1234">Исправлена ошибка, из-за которой при проверке связи возвращалось значение 0,000 мс из-за разрешения таймера.</span><span class="sxs-lookup"><span data-stu-id="71c90-1234">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="71c90-1235">Реализован файл /proc/self/environ (GH 730).</span><span class="sxs-lookup"><span data-stu-id="71c90-1235">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="71c90-1236">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1236">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1237">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1237">LTP Results:</span></span>
<span data-ttu-id="71c90-1238">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="71c90-1238">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="71c90-1239">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="71c90-1239">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="71c90-1240">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1240">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="71c90-1241">Сборка 14959</span><span class="sxs-lookup"><span data-stu-id="71c90-1241">Build 14959</span></span>

<span data-ttu-id="71c90-1242">Общие сведения о сборке Windows 14959 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="71c90-1242">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1243">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1243">Fixed</span></span>

- <span data-ttu-id="71c90-1244">Улучшены уведомления о процессе Pico для Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-1244">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="71c90-1245">Дополнительные сведения см. в [блоге о WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1245">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="71c90-1246">Повышена стабильность взаимодействия с Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-1246">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="71c90-1247">Устранена ошибка 0x80070057, возникавшая при запуске bash.exe при включенной защите корпоративных данных (EDP).</span><span class="sxs-lookup"><span data-stu-id="71c90-1247">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="71c90-1248">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1248">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1249">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1249">LTP Results:</span></span>
<span data-ttu-id="71c90-1250">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="71c90-1250">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="71c90-1251">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="71c90-1251">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="71c90-1252">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1252">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="71c90-1253">Сборка 14955</span><span class="sxs-lookup"><span data-stu-id="71c90-1253">Build 14955</span></span>

<span data-ttu-id="71c90-1254">Общие сведения о сборке Windows 14955 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="71c90-1254">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1255">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1255">Fixed</span></span>

 - <span data-ttu-id="71c90-1256">Из-за независящих от нас обстоятельств в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="71c90-1256">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="71c90-1257">Регулярный выпуск плановых обновлений будет возобновлен в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="71c90-1257">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1258">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1258">LTP Results:</span></span>
<span data-ttu-id="71c90-1259">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="71c90-1259">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="71c90-1260">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="71c90-1260">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="71c90-1261">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1261">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="71c90-1262">Сборка 14951</span><span class="sxs-lookup"><span data-stu-id="71c90-1262">Build 14951</span></span>

<span data-ttu-id="71c90-1263">Общие сведения о сборке Windows 14951 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1263">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="71c90-1264">Новая функция: взаимодействие Ubuntu и Windows</span><span class="sxs-lookup"><span data-stu-id="71c90-1264">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="71c90-1265">Теперь двоичные файлы Windows можно вызывать непосредственно из командной строки WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1265">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="71c90-1266">Это дает пользователям возможность взаимодействовать со средой и системой Windows способом, который ранее был невозможен.</span><span class="sxs-lookup"><span data-stu-id="71c90-1266">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="71c90-1267">Например, теперь пользователи могут выполнять следующие команды.</span><span class="sxs-lookup"><span data-stu-id="71c90-1267">As a quick example, it is now possible for users to run the following commands:</span></span>

```bash
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="71c90-1268">Дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="71c90-1268">More information can be found at:</span></span>

- [<span data-ttu-id="71c90-1269">Блог команды WSL по взаимодействию</span><span class="sxs-lookup"><span data-stu-id="71c90-1269">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="71c90-1270">Документация по взаимодействию на сайте MSDN</span><span class="sxs-lookup"><span data-stu-id="71c90-1270">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="71c90-1271">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1271">Fixed</span></span>

- <span data-ttu-id="71c90-1272">Ubuntu 16.04 (Xenial) теперь устанавливается для всех новых экземпляров WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1272">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="71c90-1273">Существующие у пользователей экземпляры Ubuntu 14.04 (Trusty) не будут обновляться автоматически.</span><span class="sxs-lookup"><span data-stu-id="71c90-1273">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="71c90-1274">Теперь отображается языковой стандарт, установленный во время установки.</span><span class="sxs-lookup"><span data-stu-id="71c90-1274">Locale set during install is now displayed</span></span>
- <span data-ttu-id="71c90-1275">Улучшения в терминале, включая устранение ошибки, из-за которой перенаправление процесса WSL в файл не всегда работало.</span><span class="sxs-lookup"><span data-stu-id="71c90-1275">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="71c90-1276">Время существования консоли должно быть связано со временем существования bash.exe.</span><span class="sxs-lookup"><span data-stu-id="71c90-1276">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="71c90-1277">Размер окна консоли должен быть основан на видимом размере, а не размере буфера.</span><span class="sxs-lookup"><span data-stu-id="71c90-1277">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="71c90-1278">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1278">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1279">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1279">LTP Results:</span></span>
<span data-ttu-id="71c90-1280">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="71c90-1280">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="71c90-1281">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="71c90-1281">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="71c90-1282">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1282">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="71c90-1283">Сборка 14946</span><span class="sxs-lookup"><span data-stu-id="71c90-1283">Build 14946</span></span>

<span data-ttu-id="71c90-1284">Общие сведения о сборке Windows 14946 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="71c90-1284">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1285">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1285">Fixed</span></span>

- <span data-ttu-id="71c90-1286">Устранена проблема, которая не позволила создавать учетные записи WSL для пользователей с именами пользователей NT, содержащими пробелы или кавычки.</span><span class="sxs-lookup"><span data-stu-id="71c90-1286">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="71c90-1287">Внесены изменения в VolFs и DrvFs, чтобы возвращалось значение 0 для количества ссылок каталога в stat.</span><span class="sxs-lookup"><span data-stu-id="71c90-1287">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="71c90-1288">Поддержка параметра сокета IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="71c90-1288">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="71c90-1289">Ограничение в один цикл ввода-вывода консоли на tty.</span><span class="sxs-lookup"><span data-stu-id="71c90-1289">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="71c90-1290">Например, можно выполнить следующую команду:</span><span class="sxs-lookup"><span data-stu-id="71c90-1290">Example: the following command is possible:</span></span>
  - <span data-ttu-id="71c90-1291">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="71c90-1291">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="71c90-1292">Пробелы в /proc/cpuinfo заменены символами табуляции (GH 1115).</span><span class="sxs-lookup"><span data-stu-id="71c90-1292">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="71c90-1293">DrvFs теперь отображается в mountinfo с именем, совпадающим с подключенным томом Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-1293">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="71c90-1294">Теперь /home и /root отображаются в mountinfo с правильными именами.</span><span class="sxs-lookup"><span data-stu-id="71c90-1294">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="71c90-1295">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1295">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1296">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1296">LTP Results:</span></span>
<span data-ttu-id="71c90-1297">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="71c90-1297">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="71c90-1298">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="71c90-1298">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="71c90-1299">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1299">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="71c90-1300">Сборка 14942</span><span class="sxs-lookup"><span data-stu-id="71c90-1300">Build 14942</span></span>

<span data-ttu-id="71c90-1301">Общие сведения о сборке Windows 14942 доступны в [блоге о Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="71c90-1301">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1302">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1302">Fixed</span></span>

- <span data-ttu-id="71c90-1303">Исправлен ряд ошибок, в том числе сбой сети ATTEMPTED EXECUTE OF NOEXECUTE MEMORY (Попытка выполнения в недоступной памяти), который блокировал SSH.</span><span class="sxs-lookup"><span data-stu-id="71c90-1303">A number of bugchecks addressed, including the "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" networking crash which was blocking SSH</span></span>
- <span data-ttu-id="71c90-1304">Добавлена поддержка inotifiy для уведомлений, созданных в приложениях для Windows в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-1304">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="71c90-1305">Реализованы параметры TCP_KEEPIDLE и TCP_KEEPINTVL для mongod.</span><span class="sxs-lookup"><span data-stu-id="71c90-1305">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="71c90-1306">(GH 695)</span><span class="sxs-lookup"><span data-stu-id="71c90-1306">(GH #695)</span></span>
- <span data-ttu-id="71c90-1307">Реализован системный вызов pivot_root.</span><span class="sxs-lookup"><span data-stu-id="71c90-1307">Implement the pivot_root system call</span></span>
- <span data-ttu-id="71c90-1308">Реализован параметр сокета для SO_DONTROUTE.</span><span class="sxs-lookup"><span data-stu-id="71c90-1308">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="71c90-1309">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1309">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="71c90-1310">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1310">LTP Results:</span></span>
<span data-ttu-id="71c90-1311">Число пройденных тестов: 665</span><span class="sxs-lookup"><span data-stu-id="71c90-1311">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="71c90-1312">Число непройденных тестов (неудачных, пропущенных и т. д.): 263.</span><span class="sxs-lookup"><span data-stu-id="71c90-1312">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="71c90-1313">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1313">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="71c90-1314">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="71c90-1314">Syscall Support</span></span>
<span data-ttu-id="71c90-1315">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1315">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="71c90-1316">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="71c90-1316">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="71c90-1317">Сборка 14936</span><span class="sxs-lookup"><span data-stu-id="71c90-1317">Build 14936</span></span>

<span data-ttu-id="71c90-1318">Общие сведения о сборке Windows 14936 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1318">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="71c90-1319">Примечание. В предстоящем выпуске WSL будет устанавливать версию Ubuntu 16.04 (Xenial) вместо Ubuntu 14.04 (Trusty).</span><span class="sxs-lookup"><span data-stu-id="71c90-1319">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="71c90-1320">Это изменение будет применено к участникам программы предварительной оценки, которые устанавливают новые экземпляры (lxrun.exe /install или первый запуск bash.exe).</span><span class="sxs-lookup"><span data-stu-id="71c90-1320">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="71c90-1321">Существующие экземпляры с версией Trusty не будут обновлены автоматически.</span><span class="sxs-lookup"><span data-stu-id="71c90-1321">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="71c90-1322">Пользователи могут обновить свой образ Trusty до версии Xenial с помощью команды do-release-upgrade.</span><span class="sxs-lookup"><span data-stu-id="71c90-1322">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="71c90-1323">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="71c90-1323">Known Issue</span></span>
<span data-ttu-id="71c90-1324">В WSL существует проблема с реализацией некоторых сокетов.</span><span class="sxs-lookup"><span data-stu-id="71c90-1324">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="71c90-1325">Ошибка проявляется как сбой с сообщением ATTEMPTED EXECUTE OF NOEXECUTE MEMORY (Попытка выполнения в недоступной памяти).</span><span class="sxs-lookup"><span data-stu-id="71c90-1325">The bugcheck manifests itself as a crash with the error "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY".</span></span>  <span data-ttu-id="71c90-1326">Чаще всего этот сбой происходит при использовании SSH.</span><span class="sxs-lookup"><span data-stu-id="71c90-1326">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="71c90-1327">Первопричина исправлена во внутренних сборках, и исправление будет добавлено в сборки для программы предварительной оценки при первой возможности.</span><span class="sxs-lookup"><span data-stu-id="71c90-1327">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="71c90-1328">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1328">Fixed</span></span>

- <span data-ttu-id="71c90-1329">Реализован системный вызов chroot.</span><span class="sxs-lookup"><span data-stu-id="71c90-1329">Implemented the chroot system call</span></span>
- <span data-ttu-id="71c90-1330">Улучшения в inotify, ~~включая поддержку уведомлений, созданных в приложениях для Windows в DrvFs~~.</span><span class="sxs-lookup"><span data-stu-id="71c90-1330">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="71c90-1331">Исправление: В настоящее время недоступна поддержка в inotify изменений, исходящих из приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-1331">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="71c90-1332">Привязка сокета к IPV6::<port n> теперь поддерживает IPV6_V6ONLY (GH 68, 157, 393, 460, 674, 740, 982, 996).</span><span class="sxs-lookup"><span data-stu-id="71c90-1332">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="71c90-1333">Реализовано поведение WNOWAIT для системного вызова waitid (GH 638).</span><span class="sxs-lookup"><span data-stu-id="71c90-1333">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="71c90-1334">Поддержка параметров IP-сокета IP_HDRINCL и IP_TTL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1334">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="71c90-1335">Результат read() нулевой длины должен возвращаться немедленно (GH 975).</span><span class="sxs-lookup"><span data-stu-id="71c90-1335">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="71c90-1336">Правильная обработка имен файлов и префиксов имен файлов, которые не содержат терминатор NULL в TAR-файле.</span><span class="sxs-lookup"><span data-stu-id="71c90-1336">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="71c90-1337">Поддержка epoll для /dev/null.</span><span class="sxs-lookup"><span data-stu-id="71c90-1337">epoll support for /dev/null</span></span>
- <span data-ttu-id="71c90-1338">Исправлен источник времени /dev/alarm.</span><span class="sxs-lookup"><span data-stu-id="71c90-1338">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="71c90-1339">Теперь команда bash -c может выполнять перенаправление в файл.</span><span class="sxs-lookup"><span data-stu-id="71c90-1339">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="71c90-1340">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1340">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1341">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1341">LTP Results:</span></span>
<span data-ttu-id="71c90-1342">Число пройденных тестов: 664</span><span class="sxs-lookup"><span data-stu-id="71c90-1342">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="71c90-1343">Число непройденных тестов (неудачных, пропущенных и т. д.): 264.</span><span class="sxs-lookup"><span data-stu-id="71c90-1343">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="71c90-1344">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1344">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="71c90-1345">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="71c90-1345">Syscall Support</span></span>
<span data-ttu-id="71c90-1346">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1346">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="71c90-1347">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="71c90-1347">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="71c90-1348">Сборка 14931</span><span class="sxs-lookup"><span data-stu-id="71c90-1348">Build 14931</span></span>

<span data-ttu-id="71c90-1349">Общие сведения о сборке Windows 14931 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1349">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1350">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1350">Fixed</span></span>

 - <span data-ttu-id="71c90-1351">Из-за независящих от нас обстоятельств в этой сборке не будет обновлений для подсистемы Windows для Linux.</span><span class="sxs-lookup"><span data-stu-id="71c90-1351">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="71c90-1352">Регулярный выпуск плановых обновлений будет возобновлен в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="71c90-1352">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="71c90-1353">Сборка 14926</span><span class="sxs-lookup"><span data-stu-id="71c90-1353">Build 14926</span></span>

<span data-ttu-id="71c90-1354">Общие сведения о сборке Windows 14926 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1354">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1355">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1355">Fixed</span></span>

- <span data-ttu-id="71c90-1356">Проверка связи теперь работает в консолях без привилегий администратора.</span><span class="sxs-lookup"><span data-stu-id="71c90-1356">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="71c90-1357">Теперь поддерживается ping6, также без привилегий администратора.</span><span class="sxs-lookup"><span data-stu-id="71c90-1357">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="71c90-1358">Поддержка в inotify файлов, измененных посредством WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1358">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="71c90-1359">(GH 216)</span><span class="sxs-lookup"><span data-stu-id="71c90-1359">(GH #216)</span></span>
  - <span data-ttu-id="71c90-1360">Поддерживаемые флаги:</span><span class="sxs-lookup"><span data-stu-id="71c90-1360">Flags supported:</span></span>
    - <span data-ttu-id="71c90-1361">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="71c90-1361">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="71c90-1362">События inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="71c90-1362">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="71c90-1363">Атрибуты inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="71c90-1363">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="71c90-1364">Выходные данные чтения: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="71c90-1364">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="71c90-1365">Известная проблема: Изменение файлов из приложений Windows не приводит к созданию событий.</span><span class="sxs-lookup"><span data-stu-id="71c90-1365">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="71c90-1366">Сокет UNIX теперь поддерживает SCM_CREDENTIALS.</span><span class="sxs-lookup"><span data-stu-id="71c90-1366">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="71c90-1367">Результаты LTP:</span><span class="sxs-lookup"><span data-stu-id="71c90-1367">LTP Results:</span></span>
<span data-ttu-id="71c90-1368">Число пройденных тестов: 651</span><span class="sxs-lookup"><span data-stu-id="71c90-1368">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="71c90-1369">Число непройденных тестов (неудачных, пропущенных и т. д.): 258</span><span class="sxs-lookup"><span data-stu-id="71c90-1369">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="71c90-1370">Журналы выполнения тестов LTP</span><span class="sxs-lookup"><span data-stu-id="71c90-1370">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="71c90-1371">Сборка 14915</span><span class="sxs-lookup"><span data-stu-id="71c90-1371">Build 14915</span></span>

<span data-ttu-id="71c90-1372">Общие сведения о сборке Windows 14915 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="71c90-1372">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1373">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1373">Fixed</span></span>
-  <span data-ttu-id="71c90-1374">Socketpair для сокетов датаграмм UNIX (GH 262).</span><span class="sxs-lookup"><span data-stu-id="71c90-1374">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="71c90-1375">Поддержка сокетов UNIX для SO_REUSEADDR.</span><span class="sxs-lookup"><span data-stu-id="71c90-1375">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="71c90-1376">Поддержка сокетов UNIX для SO_BROADCAST (GH 568).</span><span class="sxs-lookup"><span data-stu-id="71c90-1376">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="71c90-1377">Поддержка сокетов UNIX для SOCK_SEQPACKET (GH 758, 546).</span><span class="sxs-lookup"><span data-stu-id="71c90-1377">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="71c90-1378">Добавлена поддержка send, recv и shutdown для сокетов датаграмм UNIX.</span><span class="sxs-lookup"><span data-stu-id="71c90-1378">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="71c90-1379">Устранена ошибка из-за неправильной проверки параметров mmap для нефиксированных адресов.</span><span class="sxs-lookup"><span data-stu-id="71c90-1379">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="71c90-1380">(GH 847)</span><span class="sxs-lookup"><span data-stu-id="71c90-1380">(GH #847)</span></span>
- <span data-ttu-id="71c90-1381">Поддержка приостановки и возобновления состояний терминала.</span><span class="sxs-lookup"><span data-stu-id="71c90-1381">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="71c90-1382">Поддержка TIOCPKT ioctl для разблокировки служебной программы Screen (GH 774).</span><span class="sxs-lookup"><span data-stu-id="71c90-1382">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="71c90-1383">Известная проблема: Не работают функциональные клавиши.</span><span class="sxs-lookup"><span data-stu-id="71c90-1383">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="71c90-1384">Исправлено состязание в TimerFd, которое могло привести к обращению LxpTimerFdWorkerRoutine к освобожденному элементу ReaderReady (GH 814).</span><span class="sxs-lookup"><span data-stu-id="71c90-1384">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="71c90-1385">Включена поддержка перезапускаемых системных вызовов для futex, poll и clock_nanosleep.</span><span class="sxs-lookup"><span data-stu-id="71c90-1385">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="71c90-1386">Добавлена поддержка подключения привязки.</span><span class="sxs-lookup"><span data-stu-id="71c90-1386">Added bind mount support</span></span>
- <span data-ttu-id="71c90-1387">Поддержка отмены общего доступа для пространства имен подключения.</span><span class="sxs-lookup"><span data-stu-id="71c90-1387">unshare for mount namespace support</span></span>
    - <span data-ttu-id="71c90-1388">Известная проблема: При создании пространства имен подключения посредством `unshare(CLONE_NEWNS)` текущий рабочий каталог будет по-прежнему указывать на старое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="71c90-1388">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="71c90-1389">Дополнительные улучшения и исправления.</span><span class="sxs-lookup"><span data-stu-id="71c90-1389">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="71c90-1390">Сборка 14905</span><span class="sxs-lookup"><span data-stu-id="71c90-1390">Build 14905</span></span>

<span data-ttu-id="71c90-1391">Общие сведения о сборке Windows 14905 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1391">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1392">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1392">Fixed</span></span>
- <span data-ttu-id="71c90-1393">Теперь поддерживаются перезапускаемые системные вызовы (GH 349, GH 520).</span><span class="sxs-lookup"><span data-stu-id="71c90-1393">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="71c90-1394">Теперь функционируют символические ссылки на каталоги, которые заканчиваются косой чертой "/" (GH 650).</span><span class="sxs-lookup"><span data-stu-id="71c90-1394">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="71c90-1395">Реализован параметр RNDGETENTCNT ioctl для /dev/random.</span><span class="sxs-lookup"><span data-stu-id="71c90-1395">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="71c90-1396">Реализованы файлы /proc/[pid]/mounts, /proc/[pid]/mountinfo и /proc/[pid]/mountstats.</span><span class="sxs-lookup"><span data-stu-id="71c90-1396">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="71c90-1397">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1397">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="71c90-1398">Сборка 14901</span><span class="sxs-lookup"><span data-stu-id="71c90-1398">Build 14901</span></span>
<span data-ttu-id="71c90-1399">Первая сборка для программы предварительной оценки для выпуска после юбилейного обновления Windows 10.</span><span class="sxs-lookup"><span data-stu-id="71c90-1399">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="71c90-1400">Общие сведения о сборке Windows 14901 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1400">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1401">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1401">Fixed</span></span>
- <span data-ttu-id="71c90-1402">Исправлена проблема конечной косой черты.</span><span class="sxs-lookup"><span data-stu-id="71c90-1402">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="71c90-1403">Теперь работают такие команды, как `$ mv a/c/ a/b/`.</span><span class="sxs-lookup"><span data-stu-id="71c90-1403">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="71c90-1404">Теперь при установке отображается запрос, позволяющий установить языковый стандарт Ubuntu, совпадающий с языковым стандартом Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-1404">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="71c90-1405">Поддержка procfs для папки ns.</span><span class="sxs-lookup"><span data-stu-id="71c90-1405">Procfs support for ns folder</span></span>
- <span data-ttu-id="71c90-1406">Добавлены функции подключения и отключения для файловых систем tmpfs, procfs и sysfs.</span><span class="sxs-lookup"><span data-stu-id="71c90-1406">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="71c90-1407">Исправлена 32-разрядная подпись ABI для mknod[at].</span><span class="sxs-lookup"><span data-stu-id="71c90-1407">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="71c90-1408">Сокеты UNIX переведены на модель диспетчеризации.</span><span class="sxs-lookup"><span data-stu-id="71c90-1408">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="71c90-1409">Размер буфера recv сокета INET, заданный с помощью setsockopt, должен учитываться.</span><span class="sxs-lookup"><span data-stu-id="71c90-1409">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="71c90-1410">Реализован флаг получения сообщения MSG_CMSG_CLOEXEC для сокетов UNIX.</span><span class="sxs-lookup"><span data-stu-id="71c90-1410">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="71c90-1411">Перенаправление канала stdin/stdout процесса Linux (GH 2).</span><span class="sxs-lookup"><span data-stu-id="71c90-1411">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="71c90-1412">Разрешена конвейерная передача команд bash -c в командную строку.</span><span class="sxs-lookup"><span data-stu-id="71c90-1412">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="71c90-1413">Пример:  >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="71c90-1413">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="71c90-1414">Теперь Bash можно установить в системах с несколькими файлами подкачки (GH 538, 358).</span><span class="sxs-lookup"><span data-stu-id="71c90-1414">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="71c90-1415">Размер буфера сокета INET по умолчанию должен соответствовать установке Ubuntu по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71c90-1415">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="71c90-1416">Системные вызовы xattr согласованы с listxattr.</span><span class="sxs-lookup"><span data-stu-id="71c90-1416">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="71c90-1417">SIOCGIFCONF возвращает только интерфейсы с допустимым IPv4-адресом.</span><span class="sxs-lookup"><span data-stu-id="71c90-1417">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="71c90-1418">Исправлено действие по умолчанию для сигнала при внедрении с помощью ptrace.</span><span class="sxs-lookup"><span data-stu-id="71c90-1418">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="71c90-1419">Реализован файл /proc/sys/vm/min_free_kbytes.</span><span class="sxs-lookup"><span data-stu-id="71c90-1419">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="71c90-1420">Использование значений реестра для контекста компьютера при восстановлении контекста в sigreturn.</span><span class="sxs-lookup"><span data-stu-id="71c90-1420">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="71c90-1421">Это устраняет проблему, из-за которой у некоторых пользователей java и javac переставали отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="71c90-1421">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="71c90-1422">Реализован файл /proc/sys/kernel/hostname.</span><span class="sxs-lookup"><span data-stu-id="71c90-1422">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="71c90-1423">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="71c90-1423">Syscall Support</span></span>
<span data-ttu-id="71c90-1424">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1424">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="71c90-1425">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="71c90-1425">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="71c90-1426">Сборка 14388 для юбилейного обновления Windows 10</span><span class="sxs-lookup"><span data-stu-id="71c90-1426">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="71c90-1427">Общие сведения о сборке Windows 14388 доступны в [блоге о Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="71c90-1427">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="71c90-1428">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1428">Fixed</span></span>
- <span data-ttu-id="71c90-1429">Исправления для подготовки к выпуску юбилейного обновления Windows 10 2-го августа.</span><span class="sxs-lookup"><span data-stu-id="71c90-1429">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="71c90-1430">Дополнительные сведения о компоненте WSL в юбилейном обновлении можно найти на нашем [блоге](https://blogs.msdn.microsoft.com/wsl/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1430">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="71c90-1431">Сборка 14376</span><span class="sxs-lookup"><span data-stu-id="71c90-1431">Build 14376</span></span>
<span data-ttu-id="71c90-1432">Общие сведения о сборке Windows 14376 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1432">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="71c90-1433">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1433">Fixed</span></span>
- <span data-ttu-id="71c90-1434">Удалены некоторые экземпляры, в которых функция apt-get переставала отвечать на запросы (GH 493).</span><span class="sxs-lookup"><span data-stu-id="71c90-1434">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="71c90-1435">Исправлена проблема, из-за которой неправильно обрабатывались пустые подключения.</span><span class="sxs-lookup"><span data-stu-id="71c90-1435">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="71c90-1436">Исправлена проблема, из-за которой неправильно подключались диски ramdisk.</span><span class="sxs-lookup"><span data-stu-id="71c90-1436">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="71c90-1437">Изменена процедура принятия сокетов UNIX для поддержки флагов (частично GH 451).</span><span class="sxs-lookup"><span data-stu-id="71c90-1437">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="71c90-1438">Исправлена распространенная проблема с сетью, вызывавшая ошибку "синий экран".</span><span class="sxs-lookup"><span data-stu-id="71c90-1438">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="71c90-1439">Устранена ошибка "синий экран" при доступе к /proc/[pid]/task (GH 523).</span><span class="sxs-lookup"><span data-stu-id="71c90-1439">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="71c90-1440">Исправлена высокая загрузка ЦП для некоторых сценариев использования pty (GH 488, 504).</span><span class="sxs-lookup"><span data-stu-id="71c90-1440">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="71c90-1441">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1441">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="71c90-1442">Сборка 14371</span><span class="sxs-lookup"><span data-stu-id="71c90-1442">Build 14371</span></span>
<span data-ttu-id="71c90-1443">Общие сведения о сборке Windows 14371 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1443">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="71c90-1444">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1444">Fixed</span></span>
- <span data-ttu-id="71c90-1445">Исправлено состязание за синхронизацию SIGCHLD и wait() при использовании ptrace.</span><span class="sxs-lookup"><span data-stu-id="71c90-1445">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="71c90-1446">Исправлена обработка путей, которые завершаются косой чертой "/" (GH 432).</span><span class="sxs-lookup"><span data-stu-id="71c90-1446">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="71c90-1447">Устранен сбой при переименовании или отмене связи из-за открытых дескрипторов дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="71c90-1447">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="71c90-1448">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1448">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="71c90-1449">Сборка 14366</span><span class="sxs-lookup"><span data-stu-id="71c90-1449">Build 14366</span></span>
<span data-ttu-id="71c90-1450">Общие сведения о сборке Windows 14366 доступны в [блоге о Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="71c90-1450">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="71c90-1451">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1451">Fixed</span></span>
- <span data-ttu-id="71c90-1452">Исправлено создание файла с помощью символических ссылок.</span><span class="sxs-lookup"><span data-stu-id="71c90-1452">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="71c90-1453">Добавлена функция listxattr для Python (GH 385).</span><span class="sxs-lookup"><span data-stu-id="71c90-1453">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="71c90-1454">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1454">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="71c90-1455">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="71c90-1455">Syscall Support</span></span>
-   <span data-ttu-id="71c90-1456">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1456">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="71c90-1457">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="71c90-1457">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="71c90-1458">Сборка 14361</span><span class="sxs-lookup"><span data-stu-id="71c90-1458">Build 14361</span></span>
<span data-ttu-id="71c90-1459">Общие сведения о сборке Windows 14361 доступны в [блоге о Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="71c90-1459">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="71c90-1460">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1460">Fixed</span></span>
- <span data-ttu-id="71c90-1461">Теперь в DrvFs учитывается регистр при выполнении в Bash для Ubuntu в Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-1461">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="71c90-1462">Пользователи могут хранить на дисках в /mnt/c и файл case.txt, и файл CASE.TXT.</span><span class="sxs-lookup"><span data-stu-id="71c90-1462">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="71c90-1463">Учет регистра поддерживается только в Bash для Ubuntu в Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-1463">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="71c90-1464">За пределами Bash NTFS будет отображать сведения о файлах правильно, но при взаимодействии с этими файлами из Windows может наблюдаться непредвиденное поведение.</span><span class="sxs-lookup"><span data-stu-id="71c90-1464">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="71c90-1465">Корень каждого тома (т. е. /mnt/c) не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="71c90-1465">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="71c90-1466">Дополнительные сведения об обработке этих файлов в Windows можно найти [здесь](https://support.microsoft.com/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="71c90-1466">More information on handling these files in Windows can be found [here](https://support.microsoft.com/kb/100625).</span></span>
- <span data-ttu-id="71c90-1467">Значительно улучшена поддержка pty и tty.</span><span class="sxs-lookup"><span data-stu-id="71c90-1467">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="71c90-1468">Теперь поддерживаются такие приложения, как tmux (GH 40).</span><span class="sxs-lookup"><span data-stu-id="71c90-1468">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="71c90-1469">Исправлена проблема с установкой, из-за которой учетные записи пользователей создавались не всегда.</span><span class="sxs-lookup"><span data-stu-id="71c90-1469">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="71c90-1470">Оптимизирована структура аргументов командной строки, которая позволяет получить очень длинный список аргументов.</span><span class="sxs-lookup"><span data-stu-id="71c90-1470">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="71c90-1471">(GH 153)</span><span class="sxs-lookup"><span data-stu-id="71c90-1471">(GH #153)</span></span>
- <span data-ttu-id="71c90-1472">Теперь можно выполнять операции delete и chmod с файлами только для чтения в DrvFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-1472">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="71c90-1473">Исправлены некоторые экземпляры, в которых терминал при отключении переставал отвечать на запросы (GH 43).</span><span class="sxs-lookup"><span data-stu-id="71c90-1473">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="71c90-1474">Теперь на устройствах tty работает chmod и chown.</span><span class="sxs-lookup"><span data-stu-id="71c90-1474">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="71c90-1475">Разрешено подключение к 0.0.0.0 и :: как localhost (GH 388).</span><span class="sxs-lookup"><span data-stu-id="71c90-1475">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="71c90-1476">Теперь sendmsg и recvmsg обрабатывают векторы ввода-вывода длиной больше 1 (частично GH 376).</span><span class="sxs-lookup"><span data-stu-id="71c90-1476">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="71c90-1477">Теперь пользователи могут отказаться от автоматически создаваемого файла hosts (GH 398).</span><span class="sxs-lookup"><span data-stu-id="71c90-1477">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="71c90-1478">Автоматическое сопоставление языкового стандарта Linux с языковым стандартом NT во время установки (GH 11).</span><span class="sxs-lookup"><span data-stu-id="71c90-1478">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="71c90-1479">Добавлен файл /proc/sys/vm/swappiness (GH #306).</span><span class="sxs-lookup"><span data-stu-id="71c90-1479">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="71c90-1480">Теперь strace завершается правильно.</span><span class="sxs-lookup"><span data-stu-id="71c90-1480">strace now exits correctly</span></span>
- <span data-ttu-id="71c90-1481">Разрешено повторное открытие каналов через /proc/self/fd (GH 222).</span><span class="sxs-lookup"><span data-stu-id="71c90-1481">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="71c90-1482">Скрытие каталогов в %LOCALAPPDATA%\lxss из DrvFs (GH 270).</span><span class="sxs-lookup"><span data-stu-id="71c90-1482">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="71c90-1483">Улучшена обработка bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="71c90-1483">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="71c90-1484">Теперь поддерживаются такие команды, как bash ~ -c ls (GH 467).</span><span class="sxs-lookup"><span data-stu-id="71c90-1484">Commands like "bash ~ -c ls" now supported (GH #467)</span></span>
- <span data-ttu-id="71c90-1485">Сокеты теперь уведомляют epoll о доступе на чтение во время завершения (GH 271).</span><span class="sxs-lookup"><span data-stu-id="71c90-1485">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="71c90-1486">Команда lxrun /uninstall лучше удаляет файлы и папки.</span><span class="sxs-lookup"><span data-stu-id="71c90-1486">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="71c90-1487">Исправлена команда ps -f (GH 246).</span><span class="sxs-lookup"><span data-stu-id="71c90-1487">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="71c90-1488">Улучшена поддержка приложений x11, таких как xEmacs (GH 481).</span><span class="sxs-lookup"><span data-stu-id="71c90-1488">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="71c90-1489">Обновлен начальный размер стека потока в соответствии с параметром Ubuntu по умолчанию. Теперь при системном вызове get_rlimit размер отображается правильно (GH 172, 258).</span><span class="sxs-lookup"><span data-stu-id="71c90-1489">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="71c90-1490">Улучшено отображение имен образов процессов Pico (например, для аудита).</span><span class="sxs-lookup"><span data-stu-id="71c90-1490">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="71c90-1491">Реализован файл /proc/mountinfo для команды df.</span><span class="sxs-lookup"><span data-stu-id="71c90-1491">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="71c90-1492">Исправлен код ошибки символической ссылки для дочернего имени.</span><span class="sxs-lookup"><span data-stu-id="71c90-1492">Fixed symlink error code for child name .</span></span> <span data-ttu-id="71c90-1493">И еще:</span><span class="sxs-lookup"><span data-stu-id="71c90-1493">and ..</span></span>
- <span data-ttu-id="71c90-1494">Дополнительные улучшения исправлений ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1494">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="71c90-1495">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="71c90-1495">Syscall Support</span></span>
<span data-ttu-id="71c90-1496">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1496">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="71c90-1497">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="71c90-1497">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="71c90-1498">Сборка 14352</span><span class="sxs-lookup"><span data-stu-id="71c90-1498">Build 14352</span></span>
<span data-ttu-id="71c90-1499">Общие сведения о сборке Windows 14352 доступны в [блоге о Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="71c90-1499">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1500">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1500">Fixed</span></span>
- <span data-ttu-id="71c90-1501">Исправлена проблема, из-за которой большие файлы скачивались и создавались неправильно.</span><span class="sxs-lookup"><span data-stu-id="71c90-1501">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="71c90-1502">Это должно позволить использовать npm и реализовать другие сценарии (GH 3, GH 313).</span><span class="sxs-lookup"><span data-stu-id="71c90-1502">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="71c90-1503">Удалены некоторые экземпляры, в которых сокеты переставали отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="71c90-1503">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="71c90-1504">Исправлены некоторые ошибки ptrace.</span><span class="sxs-lookup"><span data-stu-id="71c90-1504">Corrected some ptrace errors</span></span>
- <span data-ttu-id="71c90-1505">Исправлена проблема с WSL, и теперь можно использовать имена файлов длиннее 255 знаков.</span><span class="sxs-lookup"><span data-stu-id="71c90-1505">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="71c90-1506">Улучшена поддержка знаков языков, отличных от английского.</span><span class="sxs-lookup"><span data-stu-id="71c90-1506">Improved support for non-English characters</span></span>
- <span data-ttu-id="71c90-1507">Добавление данных о текущем часовом поясе Windows и назначение его используемым по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71c90-1507">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="71c90-1508">Уникальный идентификатор устройства для каждой точки подключения (исправление JRE — GH 49).</span><span class="sxs-lookup"><span data-stu-id="71c90-1508">Unique device id's for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="71c90-1509">Устранена ошибка с путями, содержащими . и .. (одну и две точки).</span><span class="sxs-lookup"><span data-stu-id="71c90-1509">Correct issue with paths containing "." and ".."</span></span>
- <span data-ttu-id="71c90-1510">Добавлена поддержка FIFO (GH 71).</span><span class="sxs-lookup"><span data-stu-id="71c90-1510">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="71c90-1511">Обновлен формат resolv.conf в соответствии с собственным форматом Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="71c90-1511">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="71c90-1512">Некоторая очистка procfs.</span><span class="sxs-lookup"><span data-stu-id="71c90-1512">Some procfs cleanup</span></span>
- <span data-ttu-id="71c90-1513">Включена проверка связи для консолей администратора (GH 18).</span><span class="sxs-lookup"><span data-stu-id="71c90-1513">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="71c90-1514">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="71c90-1514">Syscall Support</span></span>
<span data-ttu-id="71c90-1515">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1515">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="71c90-1516">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="71c90-1516">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="71c90-1517">Сборка 14342</span><span class="sxs-lookup"><span data-stu-id="71c90-1517">Build 14342</span></span>
<span data-ttu-id="71c90-1518">Общие сведения о сборке Windows 14342 доступны в [блоге о Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="71c90-1518">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="71c90-1519">Сведения о VolFs и DriveFs можно найти в [блоге о WSL](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="71c90-1519">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="71c90-1520">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1520">Fixed</span></span>
- <span data-ttu-id="71c90-1521">Исправлена проблема с установкой, возникавшая, когда в имени пользователя Windows присутствовали знаки Юникода.</span><span class="sxs-lookup"><span data-stu-id="71c90-1521">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="71c90-1522">Теперь обходное решение для обновления apt-get с помощью udev, приведенное в разделе часто задаваемых вопросов, предоставляется по умолчанию при первом запуске.</span><span class="sxs-lookup"><span data-stu-id="71c90-1522">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="71c90-1523">Включены символические ссылки в каталогах DriveFs (/mnt/<drive>).</span><span class="sxs-lookup"><span data-stu-id="71c90-1523">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="71c90-1524">Теперь работают символические ссылки между DriveFs и VolFs.</span><span class="sxs-lookup"><span data-stu-id="71c90-1524">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="71c90-1525">Устранена проблема с анализом путей верхнего уровня. Теперь ls .// будет работать должным образом.</span><span class="sxs-lookup"><span data-stu-id="71c90-1525">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="71c90-1526">Теперь работает установка npm в DriveFs и параметры -g.</span><span class="sxs-lookup"><span data-stu-id="71c90-1526">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="71c90-1527">Исправлена проблема, препятствующая запуску сервера PHP.</span><span class="sxs-lookup"><span data-stu-id="71c90-1527">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="71c90-1528">Обновлены значения среды по умолчанию, такие как $PATH, чтобы они больше соответствовали собственным переменным Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="71c90-1528">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="71c90-1529">Добавлена еженедельная задача обслуживания в Windows для обновления кэша пакетов apt.</span><span class="sxs-lookup"><span data-stu-id="71c90-1529">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="71c90-1530">Исправлена проблема с проверкой заголовков ELF. Теперь WSL поддерживает все параметры Melkor.</span><span class="sxs-lookup"><span data-stu-id="71c90-1530">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="71c90-1531">Оболочка Zsh работает.</span><span class="sxs-lookup"><span data-stu-id="71c90-1531">Zsh shell is functional</span></span>
- <span data-ttu-id="71c90-1532">Теперь поддерживаются предварительно скомпилированные двоичные файлы Go.</span><span class="sxs-lookup"><span data-stu-id="71c90-1532">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="71c90-1533">Теперь запросы при первом запуске bash.exe локализованы правильно.</span><span class="sxs-lookup"><span data-stu-id="71c90-1533">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="71c90-1534">Теперь /proc/meminfo возвращает правильные сведения.</span><span class="sxs-lookup"><span data-stu-id="71c90-1534">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="71c90-1535">Сокеты теперь поддерживаются в VFS.</span><span class="sxs-lookup"><span data-stu-id="71c90-1535">Sockets now supported in VFS</span></span>
- <span data-ttu-id="71c90-1536">Теперь /dev подключен как tempfs.</span><span class="sxs-lookup"><span data-stu-id="71c90-1536">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="71c90-1537">FIFO теперь поддерживается.</span><span class="sxs-lookup"><span data-stu-id="71c90-1537">Fifo now supported</span></span>
- <span data-ttu-id="71c90-1538">Многоядерные системы теперь правильно отображаются в /proc/cpuinfo.</span><span class="sxs-lookup"><span data-stu-id="71c90-1538">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="71c90-1539">Дополнительные улучшения и сообщения об ошибках при скачивании во время первого запуска.</span><span class="sxs-lookup"><span data-stu-id="71c90-1539">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="71c90-1540">Усовершенствования и исправления системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="71c90-1540">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="71c90-1541">Список поддерживаемых системных вызовов приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="71c90-1541">Supported syscall list below.</span></span>
- <span data-ttu-id="71c90-1542">Дополнительные исправления ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1542">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="71c90-1543">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="71c90-1543">Known Issues</span></span>
- <span data-ttu-id="71c90-1544">Неправильное разрешение .. (две точки).</span><span class="sxs-lookup"><span data-stu-id="71c90-1544">Not resolving '..'</span></span> <span data-ttu-id="71c90-1545">в DriveFs в некоторых случаях.</span><span class="sxs-lookup"><span data-stu-id="71c90-1545">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="71c90-1546">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="71c90-1546">Syscall Support</span></span>
<span data-ttu-id="71c90-1547">Ниже приведен список новых или улучшенных системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1547">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="71c90-1548">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="71c90-1548">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a><span data-ttu-id="71c90-1549">Сборка 14332</span><span class="sxs-lookup"><span data-stu-id="71c90-1549">Build 14332</span></span>

<span data-ttu-id="71c90-1550">Общие сведения о сборке Windows 14332 доступны в [блоге о Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="71c90-1550">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="71c90-1551">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1551">Fixed</span></span>
- <span data-ttu-id="71c90-1552">Улучшенное создание resolv.conf, включая определение приоритета записей DNS.</span><span class="sxs-lookup"><span data-stu-id="71c90-1552">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="71c90-1553">Проблема с перемещением файлов и каталогов между дисками в /mnt и прочими дисками.</span><span class="sxs-lookup"><span data-stu-id="71c90-1553">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="71c90-1554">Теперь можно создавать TAR-файлы с помощью символических ссылок.</span><span class="sxs-lookup"><span data-stu-id="71c90-1554">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="71c90-1555">Добавлен каталог /run/lock по умолчанию, создаваемый при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="71c90-1555">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="71c90-1556">Обновлен файл /dev/null для возврата правильных сведений stat.</span><span class="sxs-lookup"><span data-stu-id="71c90-1556">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="71c90-1557">Дополнительные ошибки при скачивании во время первого запуска.</span><span class="sxs-lookup"><span data-stu-id="71c90-1557">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="71c90-1558">Усовершенствования и исправления системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="71c90-1558">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="71c90-1559">Список поддерживаемых системных вызовов приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="71c90-1559">Supported syscall list below.</span></span>
- <span data-ttu-id="71c90-1560">Дополнительные улучшения исправлений ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1560">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="71c90-1561">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="71c90-1561">Syscall Support</span></span>
<span data-ttu-id="71c90-1562">Ниже приведен новый системный вызов, реализованный в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1562">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="71c90-1563">Системный вызов в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут поддерживаться не все параметры.</span><span class="sxs-lookup"><span data-stu-id="71c90-1563">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="71c90-1564">Сборка 14328</span><span class="sxs-lookup"><span data-stu-id="71c90-1564">Build 14328</span></span>

<span data-ttu-id="71c90-1565">Общие сведения о сборке Windows 14332 доступны в [блоге о Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="71c90-1565">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="71c90-1566">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="71c90-1566">New Features</span></span>
* <span data-ttu-id="71c90-1567">Теперь поддерживаются пользователи Linux.</span><span class="sxs-lookup"><span data-stu-id="71c90-1567">Now support Linux users.</span></span>  <span data-ttu-id="71c90-1568">При установке Bash для Ubuntu в Windows будет предложено создать пользователя Linux.</span><span class="sxs-lookup"><span data-stu-id="71c90-1568">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="71c90-1569">Дополнительные сведения: https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="71c90-1569">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="71c90-1570">В качестве имени узла теперь указывается имя компьютера Windows, а не @localhost.</span><span class="sxs-lookup"><span data-stu-id="71c90-1570">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="71c90-1571">Дополнительные сведения о сборке 14328: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="71c90-1571">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="71c90-1572">Фиксированный</span><span class="sxs-lookup"><span data-stu-id="71c90-1572">Fixed</span></span>
* <span data-ttu-id="71c90-1573">Улучшения символьных ссылок для файлов вне каталога /mnt/<drive>.</span><span class="sxs-lookup"><span data-stu-id="71c90-1573">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="71c90-1574">Теперь установка npm работает.</span><span class="sxs-lookup"><span data-stu-id="71c90-1574">npm install now works</span></span>
    * <span data-ttu-id="71c90-1575">Теперь можно установить JDK или JRE с помощью [этих инструкций](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="71c90-1575">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="71c90-1576">Известная ошибка: символические ссылки не работали для подключений Windows.</span><span class="sxs-lookup"><span data-stu-id="71c90-1576">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="71c90-1577">Эта функция будет доступна в последующей сборке.</span><span class="sxs-lookup"><span data-stu-id="71c90-1577">Functionality will be available in a later build</span></span>
* <span data-ttu-id="71c90-1578">Теперь отображаются top и htop.</span><span class="sxs-lookup"><span data-stu-id="71c90-1578">top and htop now display</span></span>
* <span data-ttu-id="71c90-1579">Дополнительные сообщения об ошибке для некоторых сбоев при установке.</span><span class="sxs-lookup"><span data-stu-id="71c90-1579">Additional error messages for some install failures</span></span>
* <span data-ttu-id="71c90-1580">Усовершенствования и исправления системных вызовов.</span><span class="sxs-lookup"><span data-stu-id="71c90-1580">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="71c90-1581">Список поддерживаемых системных вызовов приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="71c90-1581">Supported syscall list below.</span></span>
* <span data-ttu-id="71c90-1582">Дополнительные улучшения исправлений ошибок и усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="71c90-1582">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="71c90-1583">Поддержка системных вызовов</span><span class="sxs-lookup"><span data-stu-id="71c90-1583">Syscall Support</span></span>
<span data-ttu-id="71c90-1584">Ниже приведен список системных вызовов, которые реализованы в WSL.</span><span class="sxs-lookup"><span data-stu-id="71c90-1584">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="71c90-1585">Системные вызовы в этом списке поддерживается по крайней мере в одном сценарии, но в настоящее время могут не поддерживаться все параметры.</span><span class="sxs-lookup"><span data-stu-id="71c90-1585">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>
