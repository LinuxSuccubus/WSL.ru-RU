---
title: Устранение неполадок подсистемы Windows для Linux
description: Содержит подробные сведения о распространенных ошибках и проблемах, с которыми сталкиваются пользователи при выполнении Linux в подсистеме Windows для Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
ms.date: 01/20/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 84aecf4f6111cca47ece3c2421be659fb5a27771
ms.sourcegitcommit: a5534257c236cefeebe86e6b3fc4be0be8fac24e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "88714852"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a><span data-ttu-id="ca4dd-104">Устранение неполадок подсистемы Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="ca4dd-104">Troubleshooting Windows Subsystem for Linux</span></span>

<span data-ttu-id="ca4dd-105">Для получения поддержки по вопросам, связанным с WSL, см. наш репозиторий GitHub:</span><span class="sxs-lookup"><span data-stu-id="ca4dd-105">For support with issues related to WSL, please see our GitHub repo:</span></span>

## <a name="search-for-any-existing-issues-related-to-your-problem"></a><span data-ttu-id="ca4dd-106">Поиск описанных проблем, связанных с вашей проблемой</span><span class="sxs-lookup"><span data-stu-id="ca4dd-106">Search for any existing issues related to your problem</span></span>

<span data-ttu-id="ca4dd-107">При возникновении технических проблем используйте репозиторий продуктов: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="ca4dd-107">For technical issues, use the product repo: https://github.com/Microsoft/wsl/issues</span></span>

<span data-ttu-id="ca4dd-108">При возникновении проблем, связанных с содержимым этой документации, используйте репозиторий документов: https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="ca4dd-108">For issues related to the contents of this documentation, use the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="submit-a-bug-report"></a><span data-ttu-id="ca4dd-109">Отправка отчета об ошибке</span><span class="sxs-lookup"><span data-stu-id="ca4dd-109">Submit a bug report</span></span>

<span data-ttu-id="ca4dd-110">При возникновении ошибок, связанных с функциями или компонентами WSL, отправьте сообщение о проблеме в репозитории продуктов: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="ca4dd-110">For bugs related to WSL functions or features, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="submit-a-feature-request"></a><span data-ttu-id="ca4dd-111">Отправка запроса на добавление возможностей</span><span class="sxs-lookup"><span data-stu-id="ca4dd-111">Submit a feature request</span></span>

<span data-ttu-id="ca4dd-112">Чтобы запросить новую возможность, связанную с функциональностью или совместимостью WSL, отправьте запрос в репозитории продуктов: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="ca4dd-112">To request a new feature related to WSL functionality or compatibility, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="contribute-to-the-docs"></a><span data-ttu-id="ca4dd-113">Участие в разработке документации</span><span class="sxs-lookup"><span data-stu-id="ca4dd-113">Contribute to the docs</span></span>

<span data-ttu-id="ca4dd-114">Чтобы внести изменения в документацию по WSL, отправьте запрос на вытягивание в репозитории документов: https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="ca4dd-114">To contribute to the WSL documentation, submit a pull request in the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="terminal-or-command-line"></a><span data-ttu-id="ca4dd-115">Терминал или командная строка</span><span class="sxs-lookup"><span data-stu-id="ca4dd-115">Terminal or Command Line</span></span>

<span data-ttu-id="ca4dd-116">Наконец, если ваша проблема связана с терминалом Windows, консолью Windows или интерфейсом командной строки, используйте репозиторий терминалов Windows: https://github.com/microsoft/terminal</span><span class="sxs-lookup"><span data-stu-id="ca4dd-116">Lastly, if your issue is related to the Windows Terminal, Windows Console, or the command-line UI, use the Windows terminal repo: https://github.com/microsoft/terminal</span></span>

## <a name="common-issues"></a><span data-ttu-id="ca4dd-117">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="ca4dd-117">Common issues</span></span>

### <a name="error-0x1bc-when-wsl---set-default-version-2"></a><span data-ttu-id="ca4dd-118">Ошибка. 0x1bc, когда `wsl --set-default-version 2`</span><span class="sxs-lookup"><span data-stu-id="ca4dd-118">Error: 0x1bc when `wsl --set-default-version 2`</span></span>
<span data-ttu-id="ca4dd-119">Это может произойти, если язык интерфейса или язык системы не является английским.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-119">This may happen when 'Display Language' or 'System Locale' setting is not English.</span></span>
```
wsl --set-default-version 2
Error: 0x1bc
For information on key differences with WSL 2 please visit https://aka.ms/wsl2
```

<span data-ttu-id="ca4dd-120">Фактическая ошибка для `0x1bc`:</span><span class="sxs-lookup"><span data-stu-id="ca4dd-120">THe actual error for `0x1bc` is:</span></span>
```
WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel
```

<span data-ttu-id="ca4dd-121">См. сведения о проблеме [5749](https://github.com/microsoft/WSL/issues/5749).</span><span class="sxs-lookup"><span data-stu-id="ca4dd-121">For more information, please refer to issue [5749](https://github.com/microsoft/WSL/issues/5749)</span></span>


### <a name="cannot-access-wsl-files-from-windows"></a><span data-ttu-id="ca4dd-122">Не удается получить доступ к файлам WSL из Windows</span><span class="sxs-lookup"><span data-stu-id="ca4dd-122">Cannot access WSL files from Windows</span></span>
<span data-ttu-id="ca4dd-123">Файловый сервер протокола 9p предоставляет службу на стороне Linux, которая позволяет Windows получить доступ к файловой системе Linux.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-123">A 9p protocol file server provides the service on the Linux side to allow Windows to access the Linux file system.</span></span> <span data-ttu-id="ca4dd-124">Если вы не можете получить доступ к WSL с помощью `\\wsl$` в Windows, возможно, это вызвано неправильным запуском 9P.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-124">If you cannot access WSL using `\\wsl$` on Windows, it could be because 9P did not start correctly.</span></span>

<span data-ttu-id="ca4dd-125">Чтобы убедиться в этом, можно проверить журналы запуска с помощью команды `dmesg |grep 9p`. Если ошибки есть, отобразятся сведения о них.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-125">To check this, you can check the start up logs using: `dmesg |grep 9p`, and this will show you any errors.</span></span> <span data-ttu-id="ca4dd-126">Вывод выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ca4dd-126">A successfull output looks like the following:</span></span> 

```
[    0.363323] 9p: Installing v9fs 9p2000 file system support
[    0.363336] FS-Cache: Netfs '9p' registered for caching
[    0.398989] 9pnet: Installing 9P2000 support
```

<span data-ttu-id="ca4dd-127">Дополнительные сведения об этой ошибке см. в [этом потоке GitHub](https://github.com/microsoft/wsl/issues/5307).</span><span class="sxs-lookup"><span data-stu-id="ca4dd-127">Please see [this Github thread](https://github.com/microsoft/wsl/issues/5307) for further discussion on this issue.</span></span>

### <a name="cant-start-wsl-2-distro-and-only-see-wsl-2-in-output"></a><span data-ttu-id="ca4dd-128">Не удается запустить дистрибутив WSL 2 — отображается только WSL 2 в выходных данных</span><span class="sxs-lookup"><span data-stu-id="ca4dd-128">Can't start WSL 2 distro and only see 'WSL 2' in output</span></span>
<span data-ttu-id="ca4dd-129">Если язык интерфейса не английский, возможно, отображается усеченная версия текста ошибки.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-129">If your display language is not English, then it is possible you are seeing a truncated version of an error text.</span></span>

```powershell
C:\Users\me>wsl
WSL 2
```

<span data-ttu-id="ca4dd-130">Чтобы устранить эту проблему, перейдите по адресу `https://aka.ms/wsl2kernel` и установите ядро вручную, следуя инструкциям на этой странице документации.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-130">To resolve this issue, please visit `https://aka.ms/wsl2kernel` and install the kernel manually by following the directions on that doc page.</span></span> 

### <a name="please-enable-the-virtual-machine-platform-windows-feature-and-ensure-virtualization-is-enabled-in-the-bios"></a><span data-ttu-id="ca4dd-131">Включите компонент платформы виртуальных машин Windows и убедитесь, что в BIOS включена виртуализация.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-131">Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS.</span></span>

1. <span data-ttu-id="ca4dd-132">Проверка [требований к системе Hyper-V](https://docs.microsoft.com/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.)</span><span class="sxs-lookup"><span data-stu-id="ca4dd-132">Check the [Hyper-V system requirements](https://docs.microsoft.com/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.)</span></span>
2. <span data-ttu-id="ca4dd-133">Если компьютер является виртуальной машиной, включите [вложенную виртуализацию](https://docs.microsoft.com/windows/wsl/wsl2-faq#can-i-run-wsl-2-in-a-virtual-machine) вручную.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-133">If your machine is a VM, please enable [nested virtualization](https://docs.microsoft.com/windows/wsl/wsl2-faq#can-i-run-wsl-2-in-a-virtual-machine) manually.</span></span> <span data-ttu-id="ca4dd-134">Запустите PowerShell с правами администратора и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ca4dd-134">Launch powershell with admin, and run:</span></span> 

```powershell
Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
```

3. <span data-ttu-id="ca4dd-135">Следуйте рекомендациям производителя компьютера, чтобы включить виртуализацию.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-135">Please follow guidelines from your PC's manufacturer on how to enable virtualization.</span></span> <span data-ttu-id="ca4dd-136">Как правило, для проверки того, что эти функции включены в ЦП, может использоваться BIOS системы.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-136">In general, this can involve using the system BIOS to ensure that these features are enabled on your CPU.</span></span> 
4. <span data-ttu-id="ca4dd-137">Перезагрузите компьютер после включения дополнительного компонента `Virtual Machine Platform`.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-137">Restart your machine after enabling the `Virtual Machine Platform` optional component.</span></span> 

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a><span data-ttu-id="ca4dd-138">Bash утрачивает подключение к сети после подключения к сети VPN</span><span class="sxs-lookup"><span data-stu-id="ca4dd-138">Bash loses network connectivity once connected to a VPN</span></span>

<span data-ttu-id="ca4dd-139">Если после подключения к VPN в Windows оболочка Bash утрачивает подключение к сети, попробуйте воспользоваться этим обходным решением в Bash.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-139">If after connecting to a VPN on Windows, bash loses network connectivity, try this workaround from within bash.</span></span> <span data-ttu-id="ca4dd-140">Это решение позволит вручную переопределить разрешение DNS с помощью `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-140">This workaround will allow you to manually override the DNS resolution through `/etc/resolv.conf`.</span></span>

1. <span data-ttu-id="ca4dd-141">Запишите DNS-сервер виртуальной частной сети. Для этого выполните `ipconfig.exe /all`</span><span class="sxs-lookup"><span data-stu-id="ca4dd-141">Take a note of the DNS server of the VPN from doing `ipconfig.exe /all`</span></span>
2. <span data-ttu-id="ca4dd-142">Создайте копию существующего resolv.conf, выполнив `sudo cp /etc/resolv.conf /etc/resolv.conf.new`</span><span class="sxs-lookup"><span data-stu-id="ca4dd-142">Make a copy of the existing resolv.conf `sudo cp /etc/resolv.conf /etc/resolv.conf.new`</span></span>
3. <span data-ttu-id="ca4dd-143">Разорвите связь с текущим файлом resolv.conf, выполнив команду `sudo unlink /etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-143">Unlink the current resolv.conf `sudo unlink /etc/resolv.conf`</span></span>
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. <span data-ttu-id="ca4dd-144">Откройте `/etc/resolv.conf` и сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-144">Open `/etc/resolv.conf` and</span></span> <br/>
   <span data-ttu-id="ca4dd-145">a.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-145">a.</span></span> <span data-ttu-id="ca4dd-146">Удалите из файла первую строку с текстом "\# This file was automatically generated by WSL.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-146">Delete the first line from the file, which says "\# This file was automatically generated by WSL.</span></span> <span data-ttu-id="ca4dd-147">To stop automatic generation of this file, remove this line." (Этот файл был автоматически создан WSL. Чтобы остановить автоматическое создание этого файла, удалите данную строку).</span><span class="sxs-lookup"><span data-stu-id="ca4dd-147">To stop automatic generation of this file, remove this line.".</span></span> <br/>
   <span data-ttu-id="ca4dd-148">b.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-148">b.</span></span> <span data-ttu-id="ca4dd-149">Добавьте запись DNS из пункта 1 выше в качестве первой записи в списке DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-149">Add the DNS entry from (1) above as the very first entry in the list of DNS servers.</span></span> <br/>
   <span data-ttu-id="ca4dd-150">c.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-150">c.</span></span> <span data-ttu-id="ca4dd-151">Закройте файл.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-151">Close the file.</span></span> <br/>

<span data-ttu-id="ca4dd-152">После отключения VPN необходимо будет отменить изменения в `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-152">Once you have disconnected the VPN, you will have to revert the changes to `/etc/resolv.conf`.</span></span> <span data-ttu-id="ca4dd-153">Для этого сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-153">To do this, do:</span></span>

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a><span data-ttu-id="ca4dd-154">При запуске WSL или установке дистрибутива возвращается код ошибки</span><span class="sxs-lookup"><span data-stu-id="ca4dd-154">Starting WSL or installing a distribution returns an error code</span></span>

<span data-ttu-id="ca4dd-155">Выполните [эти инструкции](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs), чтобы получить подробные журналы и сообщить о возникшей проблеме на портале GitHub.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-155">Follow [these instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) to collect detailed logs and file an issue on our GitHub.</span></span>

### <a name="updating-bash-on-ubuntu-on-windows"></a><span data-ttu-id="ca4dd-156">Обновление Bash для Ubuntu в Windows</span><span class="sxs-lookup"><span data-stu-id="ca4dd-156">Updating Bash on Ubuntu on Windows</span></span>

<span data-ttu-id="ca4dd-157">Два компонента Bash для Ubuntu в Windows могут требовать обновления.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-157">There are two components of Bash on Ubuntu on Windows that can require updating.</span></span>

1. <span data-ttu-id="ca4dd-158">Подсистема Windows для Linux</span><span class="sxs-lookup"><span data-stu-id="ca4dd-158">The Windows Subsystem for Linux</span></span>
  
   <span data-ttu-id="ca4dd-159">Обновление этой части Bash для Ubuntu в Windows обеспечит применение всех новых исправлений, описанных в [заметках о выпуске](./release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="ca4dd-159">Upgrading this portion of Bash on Ubuntu on Windows will enable any new fixes outlines in the [release notes](./release-notes.md).</span></span> <span data-ttu-id="ca4dd-160">Убедитесь, что вы подписаны на Программу предварительной оценки Windows и что ваша сборка обновлена.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-160">Ensure that you are subscribed to the Windows Insider Program and that your build is up to date.</span></span> <span data-ttu-id="ca4dd-161">Чтобы обеспечить более точное управление, включая сброс экземпляра Ubuntu, ознакомьтесь со [страницей справочных материалов по командам](./reference.md).</span><span class="sxs-lookup"><span data-stu-id="ca4dd-161">For finer grain control including resetting your Ubuntu instance check out the [command reference page](./reference.md).</span></span>

2. <span data-ttu-id="ca4dd-162">Двоичные файлы пользователя Ubuntu</span><span class="sxs-lookup"><span data-stu-id="ca4dd-162">The Ubuntu user binaries</span></span>

   <span data-ttu-id="ca4dd-163">При обновлении этой части Bash для Ubuntu в Windows будут установлены все обновления двоичных файлов пользователя Ubuntu, включая приложения, установленные с помощью apt-get.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-163">Upgrading this portion of Bash on Ubuntu on Windows will install any updates to the Ubuntu user binaries including applications that you have installed via apt-get.</span></span> <span data-ttu-id="ca4dd-164">Чтобы выполнить обновление, выполните следующие команды в Bash.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-164">To update run the following commands in Bash:</span></span>
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a><span data-ttu-id="ca4dd-165">Ошибки apt-get upgrade</span><span class="sxs-lookup"><span data-stu-id="ca4dd-165">Apt-get upgrade errors</span></span>

<span data-ttu-id="ca4dd-166">Некоторые пакеты используют функции, которые еще не реализованы.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-166">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="ca4dd-167">Например, `udev`пока не поддерживается и вызывает несколько ошибок `apt-get upgrade`.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-167">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="ca4dd-168">Чтобы устранить проблемы, связанные с `udev`, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-168">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="ca4dd-169">Введите приведенный ниже код в `/usr/sbin/policy-rc.d` и сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-169">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>
  
   ```bash
   #!/bin/sh
   exit 101
   ```
  
2. <span data-ttu-id="ca4dd-170">Добавьте разрешения на выполнение в `/usr/sbin/policy-rc.d`:</span><span class="sxs-lookup"><span data-stu-id="ca4dd-170">Add execute permissions to `/usr/sbin/policy-rc.d`:</span></span>

   ```bash
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. <span data-ttu-id="ca4dd-171">Выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="ca4dd-171">Run the following commands:</span></span>

   ```bash
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a><span data-ttu-id="ca4dd-172">"Ошибка: 0x80040306" при установке</span><span class="sxs-lookup"><span data-stu-id="ca4dd-172">"Error: 0x80040306" on installation</span></span>

<span data-ttu-id="ca4dd-173">Это связано с тем, что мы не поддерживаем устаревшую консоль.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-173">This has to do with the fact that we do not support legacy console.</span></span>
<span data-ttu-id="ca4dd-174">Чтобы отключить устаревшую консоль, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-174">To turn off legacy console:</span></span>

1. <span data-ttu-id="ca4dd-175">Выполните файл cmd.exe.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-175">Open cmd.exe</span></span>
1. <span data-ttu-id="ca4dd-176">Щелкните правой кнопкой мыши строку заголовка и выберите "Свойства", затем снимите флажок "Использовать прежнюю версию консоли".</span><span class="sxs-lookup"><span data-stu-id="ca4dd-176">Right click title bar -> Properties -> Uncheck Use legacy console</span></span>
1. <span data-ttu-id="ca4dd-177">Нажмите кнопку "ОК".</span><span class="sxs-lookup"><span data-stu-id="ca4dd-177">Click OK</span></span>

### <a name="error-0x80040154-after-windows-update"></a><span data-ttu-id="ca4dd-178">"Ошибка: 0x80040154" после обновления Windows</span><span class="sxs-lookup"><span data-stu-id="ca4dd-178">"Error: 0x80040154" after Windows update</span></span>

<span data-ttu-id="ca4dd-179">Компонент "Подсистема Windows для Linux" может быть отключен во время обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-179">The Windows Subsystem for Linux feature may be disabled during a Windows update.</span></span> <span data-ttu-id="ca4dd-180">В этом случае данную функцию Windows необходимо включить заново.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-180">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="ca4dd-181">Инструкции по включению подсистемы Windows для Linux можно найти в [руководстве по установке](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="ca4dd-181">Instructions for enabling the Windows Subsystem for Linux can be found in the [Installation Guide](./install-win10.md).</span></span>

### <a name="changing-the-display-language"></a><span data-ttu-id="ca4dd-182">Изменение отображаемого языка</span><span class="sxs-lookup"><span data-stu-id="ca4dd-182">Changing the display language</span></span>

<span data-ttu-id="ca4dd-183">Установщик WSL попытается автоматически изменить языковой стандарт Ubuntu в соответствии с языковым стандартом установки Windows.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-183">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span>  <span data-ttu-id="ca4dd-184">Если это нежелательно, можно выполнить приведенную ниже команду, чтобы изменить языковой стандарт Ubuntu после завершения установки.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-184">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span>  <span data-ttu-id="ca4dd-185">Чтобы это изменение вступило в силу, потребуется повторно запустить bash.exe.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-185">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="ca4dd-186">В приведенном ниже примере языковой стандарт изменяется на EN-US.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-186">The below example changes to locale to en-US:</span></span>

```bash
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a><span data-ttu-id="ca4dd-187">Проблемы установки после восстановления системы Windows</span><span class="sxs-lookup"><span data-stu-id="ca4dd-187">Installation issues after Windows system restore</span></span>

1. <span data-ttu-id="ca4dd-188">Удалите папку `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-188">Delete the `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` folder.</span></span> <br/>
  <span data-ttu-id="ca4dd-189">**Примечание. Не делайте этого, если дополнительный компонент полностью установлен и работает.**</span><span class="sxs-lookup"><span data-stu-id="ca4dd-189">**Note: Do not do this if your optional feature is fully installed and working.**</span></span>
2. <span data-ttu-id="ca4dd-190">Включите дополнительный компонент WSL (если он еще не включен).</span><span class="sxs-lookup"><span data-stu-id="ca4dd-190">Enable the WSL optional feature (if not already)</span></span>
3. <span data-ttu-id="ca4dd-191">Выполните перезагрузку.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-191">Reboot</span></span>
4. <span data-ttu-id="ca4dd-192">Выполните команду lxrun /uninstall /full</span><span class="sxs-lookup"><span data-stu-id="ca4dd-192">lxrun /uninstall /full</span></span>
5. <span data-ttu-id="ca4dd-193">Установите Bash.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-193">Install bash</span></span>

### <a name="no-internet-access-in-wsl"></a><span data-ttu-id="ca4dd-194">Нет доступа к Интернету в WSL</span><span class="sxs-lookup"><span data-stu-id="ca4dd-194">No internet access in WSL</span></span>

<span data-ttu-id="ca4dd-195">Некоторые пользователи сообщили о проблемах с определенными приложениями брандмауэра, блокирующими доступ к Интернету в WSL.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-195">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span>  <span data-ttu-id="ca4dd-196">Сообщили о следующих брандмауэрах:</span><span class="sxs-lookup"><span data-stu-id="ca4dd-196">The firewalls reported are:</span></span>

1. <span data-ttu-id="ca4dd-197">Kaspersky;</span><span class="sxs-lookup"><span data-stu-id="ca4dd-197">Kaspersky</span></span>
2. <span data-ttu-id="ca4dd-198">AVG;</span><span class="sxs-lookup"><span data-stu-id="ca4dd-198">AVG</span></span>
3. <span data-ttu-id="ca4dd-199">Avast.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-199">Avast</span></span>

<span data-ttu-id="ca4dd-200">В некоторых случаях отключение брандмауэра обеспечивает доступ.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-200">In some cases turning off the firewall allows for access.</span></span>  <span data-ttu-id="ca4dd-201">В некоторых случаях доступ блокируется просто при наличии установленного брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-201">In some cases simply having the firewall installed looks to block access.</span></span>

### <a name="permission-denied-error-when-using-ping"></a><span data-ttu-id="ca4dd-202">Ошибка "Отказ в разрешении" при проверке связи</span><span class="sxs-lookup"><span data-stu-id="ca4dd-202">Permission Denied error when using ping</span></span>

<span data-ttu-id="ca4dd-203">В выпуске [Windows Anniversary Update, версия 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update) для проверки связи в WSL требуются **права администратора**.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-203">For [Windows Anniversary Update, version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), **administrator privileges** in Windows are required to run ping in WSL.</span></span>  <span data-ttu-id="ca4dd-204">Чтобы выполнить проверку связи, запустите Bash для Ubuntu в Windows от имени администратора или запустите bash.exe из командной строки или сеанса PowerShell с привилегиями администратора.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-204">To run ping, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

<span data-ttu-id="ca4dd-205">В более поздних версиях Windows ([сборка 14926+](./release-notes.md#build-14926)) права администратора не требуются.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-205">For later versions of Windows, [Build 14926+](./release-notes.md#build-14926), administrator privileges are no longer required.</span></span>

### <a name="bash-is-hung"></a><span data-ttu-id="ca4dd-206">Bash перестал отвечать на запросы</span><span class="sxs-lookup"><span data-stu-id="ca4dd-206">Bash is hung</span></span>

<span data-ttu-id="ca4dd-207">Если при работе с Bash вы обнаружите, что Bash перестал отвечать на запросы (или взаимозаблокирован), помогите нам диагностировать проблему путем сбора и передачи дампа памяти.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-207">If while working with bash, you find that bash is hung (or deadlocked) and not responding to inputs, help us diagnose the issue by collecting and reporting a memory dump.</span></span> <span data-ttu-id="ca4dd-208">Обратите внимание на то, что выполнение этих действий приведет к сбою системы.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-208">Note that these steps will crash your system.</span></span> <span data-ttu-id="ca4dd-209">Не делайте этого, если вас это не устраивает, либо предварительно сохраните результаты своей работы.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-209">Do not do this if you are not comfortable with that or save your work prior to doing this.</span></span>

<span data-ttu-id="ca4dd-210">Сбор дампа памяти</span><span class="sxs-lookup"><span data-stu-id="ca4dd-210">To collect a memory dump</span></span>

1. <span data-ttu-id="ca4dd-211">Измените тип дампа памяти на "Полный дамп памяти".</span><span class="sxs-lookup"><span data-stu-id="ca4dd-211">Change the memory dump type to "complete memory dump".</span></span> <span data-ttu-id="ca4dd-212">При изменении типа дампа запишите текущий тип.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-212">While changing the dump type, take a note of your current type.</span></span>

2. <span data-ttu-id="ca4dd-213">Выполните [эти действия](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809), чтобы настроить аварийное завершение с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-213">Use the [steps](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) to configure crash using keyboard control.</span></span>

3. <span data-ttu-id="ca4dd-214">Воспроизведите взаимоблокировку или прекращение ответа на запросы.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-214">Repro the hang or deadlock.</span></span>

4. <span data-ttu-id="ca4dd-215">Выполните аварийное завершение системы с помощью последовательности клавиш из пункта 2.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-215">Crash the system using the key sequence from (2).</span></span>

5. <span data-ttu-id="ca4dd-216">Произойдет аварийное завершение системы и будет собран дамп памяти.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-216">The system will crash and collect the memory dump.</span></span>

6. <span data-ttu-id="ca4dd-217">После перезагрузки системы отправьте memory.dmp на адрес электронной почты secure@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-217">Once the system reboots, report the memory.dmp to secure@microsoft.com.</span></span> <span data-ttu-id="ca4dd-218">По умолчанию файл дампа находится в папке %SystemRoot%\memory.dmp или C:\Windows\memory.dmp, если C: является системным диском.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-218">The default location of the dump file is %SystemRoot%\memory.dmp or C:\Windows\memory.dmp if C: is the system drive.</span></span> <span data-ttu-id="ca4dd-219">В письме укажите, что дамп предназначен для команды разработчиков WSL или Bash в Windows.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-219">In the email, note that the dump is for the WSL or Bash on Windows team.</span></span>

7. <span data-ttu-id="ca4dd-220">Восстановите исходное значение типа дампа памяти.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-220">Restore the memory dump type to the original setting.</span></span>

### <a name="check-your-build-number"></a><span data-ttu-id="ca4dd-221">Проверка номера сборки</span><span class="sxs-lookup"><span data-stu-id="ca4dd-221">Check your build number</span></span>

<span data-ttu-id="ca4dd-222">Чтобы узнать архитектуру компьютера и номер сборки Windows, выберите</span><span class="sxs-lookup"><span data-stu-id="ca4dd-222">To find your PC's architecture and Windows build number, open</span></span>  
<span data-ttu-id="ca4dd-223">**Параметры** > **Система** > **О программе**</span><span class="sxs-lookup"><span data-stu-id="ca4dd-223">**Settings** > **System** > **About**</span></span>

<span data-ttu-id="ca4dd-224">Найдите поля **Сборка ОС** и **Тип системы**.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-224">Look for the **OS Build** and **System Type** fields.</span></span>  
    <span data-ttu-id="ca4dd-225">![Снимок экрана с полями "Сборка ОС" и "Тип системы"](media/system.png)</span><span class="sxs-lookup"><span data-stu-id="ca4dd-225">![Screenshot of Build and System Type fields](media/system.png)</span></span>

<span data-ttu-id="ca4dd-226">Чтобы найти номер сборки Windows Server, выполните в PowerShell следующую команду.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-226">To find your Windows Server build number, run the following in PowerShell:</span></span>  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a><span data-ttu-id="ca4dd-227">Подтверждение включения WSL</span><span class="sxs-lookup"><span data-stu-id="ca4dd-227">Confirm WSL is enabled</span></span>

<span data-ttu-id="ca4dd-228">Вы можете убедиться, что подсистема Windows для Linux включена, выполнив в PowerShell следующую команду.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-228">You can confirm that the Windows Subsystem for Linux is enabled by running the following in PowerShell:</span></span>  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a><span data-ttu-id="ca4dd-229">Проблемы с подключением к серверу OpenSSH</span><span class="sxs-lookup"><span data-stu-id="ca4dd-229">OpenSSH-Server connection issues</span></span>

<span data-ttu-id="ca4dd-230">Попытка подключения к серверу SSH завершается следующей ошибкой: "Connection closed by 127.0.0.1 port 22" (Подключение закрыто узлом 127.0.0.1 через порт 22).</span><span class="sxs-lookup"><span data-stu-id="ca4dd-230">Trying to connect your SSH server is failed with the following error: "Connection closed by 127.0.0.1 port 22".</span></span>

1. <span data-ttu-id="ca4dd-231">Убедитесь, что сервер OpenSSH работает</span><span class="sxs-lookup"><span data-stu-id="ca4dd-231">Make sure your OpenSSH Server is running:</span></span>

   ```bash
   sudo service ssh status
   ```

   <span data-ttu-id="ca4dd-232">и вы следовали указаниям в этом руководстве: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-232">and you've followed this tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span></span>

2. <span data-ttu-id="ca4dd-233">Завершите работу службы sshd и запустите sshd в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-233">Stop the sshd service and start sshd in debug mode:</span></span>

   ```bash
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. <span data-ttu-id="ca4dd-234">Проверьте журналы запуска и убедитесь, что ключи сервера доступны и в журнале нет сообщений, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-234">Check the startup logs and make sure HostKeys are available and you don't see log messages such as:</span></span>

   ```BASH
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

<span data-ttu-id="ca4dd-235">Если вы видите такие сообщения и в разделе `/etc/ssh/` отсутствуют ключи, потребуется повторно создать ключи или просто очистить и установить сервер OpenSSH.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-235">If you do see such messages and the keys are missing under `/etc/ssh/`, you will have to regenerate the keys or just purge&install openssh-server:</span></span>

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a><span data-ttu-id="ca4dd-236">"Указанная сборка не найдена".</span><span class="sxs-lookup"><span data-stu-id="ca4dd-236">"The referenced assembly could not be found."</span></span> <span data-ttu-id="ca4dd-237">Это сообщение может появиться при включении дополнительного компонента WSL.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-237">when enabling the WSL optional feature</span></span>

<span data-ttu-id="ca4dd-238">Данная ошибка связана с неправильным состоянием установки.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-238">This error is related to being in a bad install state.</span></span> <span data-ttu-id="ca4dd-239">Чтобы устранить эту проблему, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-239">Please complete the following steps to try and fix this issue:</span></span>

- <span data-ttu-id="ca4dd-240">Если вы используете команду включения компонента WSL в PowerShell, попробуйте использовать графический пользовательский интерфейс. Для этого откройте меню "Пуск", выполните поиск фразы "Включение или отключение компонентов Windows", а затем из списка выберите "Подсистема Windows для Linux". Этот дополнительный компонент будет установлен.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-240">If you are running the enable WSL feature command from PowerShell, try using the GUI instead by opening the start menu, searching for 'Turn Windows features on or off' and then in the list select 'Windows Subsystem for Linux' which will install the optional component.</span></span>

- <span data-ttu-id="ca4dd-241">Обновите версию Windows, выбрав "Параметры" > "Обновления" и щелкнув "Проверить наличие обновлений".</span><span class="sxs-lookup"><span data-stu-id="ca4dd-241">Update your version of Windows by going to Settings, Updates, and clicking 'Check for Updates'</span></span>

- <span data-ttu-id="ca4dd-242">Если оба способа не помогли и вам нужно использовать WSL, рассмотрите возможность обновления на месте, переустановив Windows 10 с установочного носителя и выбрав параметр "Сохранить все", чтобы сохранить свои приложения и файлы.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-242">If both of those fail and you need to access WSL please consider upgrading in place by reinstalling Windows 10 using installation media and selecting 'Keep Everything' to ensure your apps and files are preserved.</span></span> <span data-ttu-id="ca4dd-243">Инструкции по такой установке можно найти на странице [Переустановка Windows 10](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span><span class="sxs-lookup"><span data-stu-id="ca4dd-243">You can find instructions on how to do so at the [Reinstall Windows 10 page](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span></span>

### <a name="correct-ssh-related-permission-errors"></a><span data-ttu-id="ca4dd-244">Правильные (связанные с SSH) ошибки разрешений</span><span class="sxs-lookup"><span data-stu-id="ca4dd-244">Correct (SSH related) permission errors</span></span>

<span data-ttu-id="ca4dd-245">Если вы видите эту ошибку:</span><span class="sxs-lookup"><span data-stu-id="ca4dd-245">If you're seeing this error:</span></span>

```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

<span data-ttu-id="ca4dd-246">Чтобы устранить эту проблему, добавьте следующий текст в файл ```/etc/wsl.conf```:</span><span class="sxs-lookup"><span data-stu-id="ca4dd-246">To fix this, append the following to the the ```/etc/wsl.conf``` file:</span></span>

```
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

<span data-ttu-id="ca4dd-247">Обратите внимание, что добавление этой команды будет включать метаданные и изменять разрешения для файлов Windows, показанных в WSL.</span><span class="sxs-lookup"><span data-stu-id="ca4dd-247">Please note that adding this command will include metadata and modify the file permissions on the Windows files seen from WSL.</span></span> <span data-ttu-id="ca4dd-248">См. сведения о [разрешениях файловой системы](./file-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="ca4dd-248">Please see the [File System Permissions](./file-permissions.md) for more information.</span></span>
