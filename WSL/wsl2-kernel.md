---
title: Обновление ядра Linux в WSL 2
description: Инструкции по обновлению ядра Linux в WSL 2 вручную
keywords: WSL, Windows, ядро Linux, подсистема Windows для Linux, ядро
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 7bf2ef606d0bd23083f323117348aeea87c52b10
ms.sourcegitcommit: f1996541005ae126ef379d8aebfe1abfcccb9ac9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2020
ms.locfileid: "91238804"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Обновление ядра Linux в WSL 2

Чтобы вручную обновить ядро Linux в WSL 2, выполните описанные ниже действия.

> [!NOTE] 
> Если установщику не удается найти WSL 1, щелкните правой кнопкой мыши установщик обновления ядра Linux, а затем нажмите кнопку "Удалить" и запустите установщик повторно.

## <a name="download-the-linux-kernel-update-package"></a>Скачивание пакета обновления ядра Linux

[Скачайте последнюю версию пакета обновления ядра Linux в WSL 2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) для 64-разрядных компьютеров.

> [!NOTE]
> Если вы используете компьютер ARM64, вместо этого скачайте [пакет ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi).

## <a name="install-the-linux-kernel-update-package"></a>Установка пакета обновления ядра Linux

Чтобы установить пакет обновления ядра Linux:

  1. Запустите пакет обновления, скачанный на предыдущем этапе.

  2. Появится запрос на повышение уровня разрешений. Нажмите кнопку "Да", чтобы утвердить эту установку.

  3. По завершении установки можно приступить к использованию WSL 2.

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Дальнейшие планы по обновлению ядра Linux в WSL 2

Дополнительные сведения см. в статье об [изменениях процесса установки обновления ядра Linux в WSL 2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), доступной в блоге, [посвященному командной строке Windows](https://aka.ms/cliblog).

## <a name="troubleshooting"></a>Диагностика

### <a name="this-update-only-applies-to-machines-with-the-windows-subsystem-for-linux"></a>Это обновление применяется только к компьютерам с подсистемой Windows для Linux.
Чтобы установить ядро MSI, сначала нужно включить WSL. В случае сбоя отображается следующее сообщение: `This update only applies to machines with the Windows Subsystem for Linux`. 

Есть три возможные причины, по которым вы видите это сообщение:

1. Вы используете старую версию Windows, которая не поддерживает WSL 2. Проверьте [требования к WSL 2](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2) и выполните обновление, чтобы включить поддержку WSL 2. 
2. `Windows Subsystem for Linux` не включена. См. статью [Руководство по установке подсистемы Windows для Linux в Windows 10](https://docs.microsoft.com/windows/wsl/install-win10).
3. После включения `Windows Subsystem for Linux` нужно перезагрузить компьютер. Сделайте это и повторите попытку.

### `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`

Если ядро отсутствует в %SystemRoot%\system32\lxss\tools\,, может возникнуть описанная выше ошибка.

Есть несколько способов устранения этой проблемы:

1. Установите ядро Linux вручную, следуя инструкциям на этой странице.
2. Перейдите к разделу "Установка и удаление программ", а затем удалите и снова установите MSI.