---
title: Инициализация нового дистрибутива Linux для WSL
description: После установки дистрибутива Linux для WSL выполните инициализацию с помощью следующих простых действий.
keywords: BashOnWindows, bash, wsl, windows, подсистема windows для linux, windowssubsystem, ubuntu, debian, suse, windows 10
ms.date: 07/24/2018
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 11dc84d3a58b51241c7c63e8ca35eba94a12508b
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413215"
---
# <a name="initializing-a-newly-installed-distribution"></a><span data-ttu-id="28c12-104">Инициализация недавно установленного дистрибутива</span><span class="sxs-lookup"><span data-stu-id="28c12-104">Initializing a newly installed distribution</span></span>

<span data-ttu-id="28c12-105">После скачивания и установки дистрибутива необходимо выполнить инициализацию нового дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="28c12-105">Once your distribution has been downloaded and installed, you'll need to complete initialization of the new distribution:</span></span>

## <a name="launch-a-distribution"></a><span data-ttu-id="28c12-106">Запуск дистрибутива</span><span class="sxs-lookup"><span data-stu-id="28c12-106">Launch a distribution</span></span>

<span data-ttu-id="28c12-107">Чтобы завершить инициализацию недавно установленного дистрибутива, запустите новый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="28c12-107">To complete the initialization of your newly installed distribution, launch a new instance.</span></span> <span data-ttu-id="28c12-108">Для этого нажмите кнопку "Запустить" в приложении Microsoft Store или запустите дистрибутив из меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="28c12-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distribution from the Start menu:</span></span>

> <span data-ttu-id="28c12-109">Совет. Возможно, потребуется закрепить часто используемые дистрибутивы в меню "Пуск" и (или) на панели задач.</span><span class="sxs-lookup"><span data-stu-id="28c12-109">Tip: You might want to pin your most frequently used distributions to your Start menu, and/or to your taskbar!</span></span>

![Запуск дистрибутива из меню "Пуск"](media/start-menu.png)

> <span data-ttu-id="28c12-111">В Windows Server можно запустить исполняемый файл средства запуска дистрибутива `<distribution>.exe` из папки установки дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="28c12-111">On Windows Server, you can launch your distribution's launcher executable `<distribution>.exe` from the distribution installation folder.</span></span>

<span data-ttu-id="28c12-112">При первом запуске недавно установленного дистрибутива откроется окно консоли с сообщением о том, что вам нужно подождать одну или две минуты до завершения установки.</span><span class="sxs-lookup"><span data-stu-id="28c12-112">The first time a newly installed distribution runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="28c12-113">На этом последнем этапе установки файлы дистрибутива будут распакованы и сохранены на компьютере полностью готовые к использованию.</span><span class="sxs-lookup"><span data-stu-id="28c12-113">During this final stage of installation, the distribution's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="28c12-114">Это может занять около минуты, в зависимости от производительности накопителей на компьютере.</span><span class="sxs-lookup"><span data-stu-id="28c12-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="28c12-115">Этот начальный этап установки требуется, только если выполняется чистая установка дистрибутива. Все последующие запуски должны занимать меньше секунды.</span><span class="sxs-lookup"><span data-stu-id="28c12-115">This initial installation phase is only required when a distribution is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="28c12-116">Настройка новой учетной записи пользователя Linux</span><span class="sxs-lookup"><span data-stu-id="28c12-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="28c12-117">После завершения установки вам будет предложено создать учетную запись пользователя (и ее пароль).</span><span class="sxs-lookup"><span data-stu-id="28c12-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span>

![Распаковка Ubuntu в консоли Windows](media/UbuntuInstall.png)

<span data-ttu-id="28c12-119">Эта учетная запись представляет обычного пользователя без прав администратора, который будет по умолчанию входить в систему при запуске дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="28c12-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distribution.</span></span>

> <span data-ttu-id="28c12-120">Вы можете выбрать любые имя пользователя и пароль, которые не связаны с именем пользователя Windows.</span><span class="sxs-lookup"><span data-stu-id="28c12-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span>

<span data-ttu-id="28c12-121">Когда вы открываете новый экземпляр дистрибутива, вам не будет предложено ввести пароль. Но **если вы повысите свои привилегии для выполнения процесса, используя `sudo`, вам нужно будет указать пароль**. Поэтому выбирайте пароль, который можно легко запомнить.</span><span class="sxs-lookup"><span data-stu-id="28c12-121">When you open a new distribution instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="28c12-122">Дополнительные сведения приведены на странице [Учетные записи пользователей и разрешения для подсистемы Windows для Linux](user-support.md).</span><span class="sxs-lookup"><span data-stu-id="28c12-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distributions-packages"></a><span data-ttu-id="28c12-123">Обновление пакетов дистрибутива</span><span class="sxs-lookup"><span data-stu-id="28c12-123">Update & upgrade your distribution's packages</span></span>

<span data-ttu-id="28c12-124">Большинство дистрибутивов поставляется с пустым или минимально наполненным каталогом пакетов.</span><span class="sxs-lookup"><span data-stu-id="28c12-124">Most distributions ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="28c12-125">Мы настоятельно рекомендуем регулярно обновлять каталог пакетов и установленные пакеты с помощью предпочитаемого диспетчера пакетов дистрибутива.</span><span class="sxs-lookup"><span data-stu-id="28c12-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distribution's preferred package manager.</span></span> <span data-ttu-id="28c12-126">В Debian или Ubuntu используется функция apt.</span><span class="sxs-lookup"><span data-stu-id="28c12-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="28c12-127">Windows не выполняет автоматическую установку новых версий или обновление дистрибутивов Linux. Это задача, выполнение которой пользователи Linux предпочитают контролировать самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="28c12-127">Windows does not automatically update or upgrade your Linux distribution(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="28c12-128">Готово!</span><span class="sxs-lookup"><span data-stu-id="28c12-128">You're done!</span></span> <span data-ttu-id="28c12-129">Приятного вам использования дистрибутивов Linux в WSL.</span><span class="sxs-lookup"><span data-stu-id="28c12-129">Enjoy using your new Linux distribution on WSL!</span></span> <span data-ttu-id="28c12-130">Чтобы узнать больше о WSL, ознакомьтесь с другой [документацией по WSL](./index.md) или перейдите на [страницу учебных материалов по WSL](https://aka.ms/learnwsl).</span><span class="sxs-lookup"><span data-stu-id="28c12-130">To learn more about WSL, review the other [WSL docs](./index.md), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![Приятного вам использования Linux в WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="28c12-132">Диагностика</span><span class="sxs-lookup"><span data-stu-id="28c12-132">Troubleshooting</span></span>

<span data-ttu-id="28c12-133">Ниже перечислены возможные ошибки и способы их устранения.</span><span class="sxs-lookup"><span data-stu-id="28c12-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="28c12-134">Другие распространенные ошибки и способы их устранения приведены в разделе [Устранение неполадок подсистемы Windows для Linux](troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="28c12-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="28c12-135">**Сбой установки с ошибкой 0x8007007e**. Эта ошибка возникает, когда система не поддерживает Linux из Store.</span><span class="sxs-lookup"><span data-stu-id="28c12-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="28c12-136">Убедитесь в следующем.</span><span class="sxs-lookup"><span data-stu-id="28c12-136">Make sure that:</span></span>
> * <span data-ttu-id="28c12-137">Вы используете сборку Windows 16215 или более позднюю версию.</span><span class="sxs-lookup"><span data-stu-id="28c12-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="28c12-138">[Проверьте используемую сборку](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="28c12-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="28c12-139">Дополнительный компонент "Подсистема Windows для Linux" включен, а компьютер был перезагружен.</span><span class="sxs-lookup"><span data-stu-id="28c12-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="28c12-140">[Убедитесь, что WSL включен](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="28c12-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>