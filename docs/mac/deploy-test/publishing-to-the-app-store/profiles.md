---
title: Bereitstellungsprofile
description: Dieser Leitfaden enthält Informationen zum Erstellen der erforderlichen Bereitstellungsprofile, die für das Veröffentlichen einer Xamarin.Mac-App benötigt werden.
ms.prod: xamarin
ms.assetid: bdff6c32-f7e3-4a97-a093-dbda48be8227
ms.technology: xamarin-mac
author: bradumbaugh
ms.author: brumbaug
ms.date: 04/12/2017
ms.openlocfilehash: 4f3120c45de5022dca1e522be251f453f9f5b4c7
ms.sourcegitcommit: 945df041e2180cb20af08b83cc703ecd1aedc6b0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/04/2018
---
# <a name="provisioning-profiles"></a>Bereitstellungsprofile

Bereitstellungsprofile ermöglichen es Entwicklern, mehrere spezifische macOS-Funktionen (ehemals Mac OS X), z.B. iCloud und Pushbenachrichtigungen, in ihre Xamarin.Mac-Apps zu integrieren. Sie müssen ein Mac-Bereitstellungsprofil für jede entwickelte Anwendung, die diese Funktionen verwendet, erstellen, herunterladen und installieren.

[![](profiles-images/certif13.png "Das Apple-Bereitstellungsportal")](profiles-images/certif13.png#lightbox)

<a name="Development_Provisioning_Profile" />

## <a name="development-provisioning-profile"></a>Entwicklungsbereitstellungsprofil

Durch ein Entwicklungsbereitstellungsprofil kann eine App für den Mac App Store auf den bestimmten Computern getestet werden, die im Profil eingerichtet wurden. Dies ist besonders wichtig, wenn Sie macOS-Funktionen wie iCloud und Pushbenachrichtigungen verwenden.

> [!NOTE]
> Der Entwickler muss ein Mac-Entwicklungszertifikat erstellt haben, bevor ein Entwicklungsbereitstellungsprofil erstellt werden kann. Füllen Sie wie in diesem Screenshot gezeigt die Details aus, um ein **Entwicklungsbereitstellungsprofil** zu generieren, das für das Erstellen von Builds verwendet werden kann. Im Feld **Zertifikate** muss ein gültiges Mac-Entwicklungszertifikat zur Auswahl verfügbar sein und mindestens ein für das Testen registriertes System.

Führen Sie folgende Schritte aus:

1. Wählen Sie die Art des Bereitstellungsprofils aus, das Sie erstellen möchten, und klicken Sie auf die Schaltfläche **Weiter**: 

     [![](profiles-images/certif14.png "Auswählen des Profiltyps")](profiles-images/certif14.png#lightbox)
2. Wählen Sie die ID der Anwendung aus, für die das Profil erstellt werden soll, und klicken Sie auf die Schaltfläche **Weiter**: 

     [![](profiles-images/certif15.png "Auswählen der App-ID")](profiles-images/certif15.png#lightbox)
3. Wählen Sie die Entwickler-ID aus, die für das Signieren des Profils verwendet wurde, und klicken Sie auf **Weiter**: 

     [![](profiles-images/certif16.png "Auswählen der Entwickler-ID")](profiles-images/certif16.png#lightbox)
4. Wählen Sie die Computer aus, auf denen dieses Profil verwendet werden kann, und klicken Sie auf **Weiter**: 

     [![](profiles-images/certif17.png "Auswählen der zulässigen Computer")](profiles-images/certif17.png#lightbox)
5. Geben Sie nun einen **Profilnamen** ein, und klicken Sie auf die Schaltfläche **Generieren**: 

     [![](profiles-images/certif18.png "Generieren des Profils")](profiles-images/certif18.png#lightbox)
6. Klicken Sie auf die Schaltfläche **Herunterladen**, um das neue Profil herunterzuladen: 

     [![](profiles-images/certif19.png "Herunterladen des Profils")](profiles-images/certif19.png#lightbox)
7. Entwicklungsbereitstellungsprofile werden im Bereich „Profileinstellungen“ der Mac-Anwendung **Systemeinstellungen** installiert: 

     [![](profiles-images/certif20.png "Installieren des Profils")](profiles-images/certif20.png#lightbox)
8. Im Bereich „Profileinstellungen“ werden nun alle installierten Profile angezeigt: 

     [![](profiles-images/image47.png "Anzeigen aller installierten Profile")](profiles-images/image47.png#lightbox)
9. Das Profil wird ebenfalls im **Hilfsprogramm für Entwicklerzertifikate** angezeigt, falls es erneut heruntergeladen werden muss: 

     [![](profiles-images/image48.png "Hilfsprogramm für das Entwicklerzertifikat")](profiles-images/image48.png#lightbox)

Ein neues Entwicklungsbereitstellungsprofil muss für jede neue App oder jeden neuen Computer, der für das Testen hinzugefügt wird, erstellt werden.

<a name="Production_Provisioning_Profile" />

## <a name="production-provisioning-profile"></a>Produktionsbereitstellungsprofil

Produktionsbereitstellungsprofile sind erforderlich, um ein Paket für die Übermittlung an den Mac App Store zu erstellen.

Führen Sie folgende Schritte aus:

1. Wählen Sie die Art des Profils aus, das Sie erstellen möchten, und klicken Sie auf die Schaltfläche **Weiter**: 

    [![](profiles-images/certif21.png "Auswählen des Profiltyps")](profiles-images/certif21.png#lightbox)
2. Wählen Sie die ID der App aus, für die das Profil erstellt werden soll, und klicken Sie auf die Schaltfläche **Weiter**: 

    [![](profiles-images/certif15.png "Auswählen der App-ID")](profiles-images/certif15.png#lightbox)
3. Wählen Sie die Unternehmens-ID aus, mit der das Profil signiert werden soll, und klicken Sie auf die Schaltfläche **Weiter**: 

    [![](profiles-images/certif23.png "Auswählen der Unternehmens-ID")](profiles-images/certif23.png#lightbox)
4. Geben Sie einen **Profilnamen** ein, und klicken Sie auf die Schaltfläche **Generieren**: 

    [![](profiles-images/certif24.png "Generieren des Profils")](profiles-images/certif24.png#lightbox)
5. Klicken Sie auf **Herunterladen**, um die Datei (Erweiterung `.provisionprofile`) des Bereitstellungsprofils zu erhalten: 

    [![](profiles-images/certif25.png "Herunterladen des Profils")](profiles-images/certif25.png#lightbox)
6. Ziehen Sie diese in den **Xcode-Organisator**, oder doppelklicken Sie darauf, um sie zu installieren. Das Profil wird dann im Xcode-Organisator angezeigt: 

    [![](profiles-images/image51.png "Installieren des Profils")](profiles-images/image51.png#lightbox)
7. Das Bereitstellungsprofil wird ebenfalls in der Liste angezeigt: 

    [![](profiles-images/certif26.png "Anzeigen der installierten Profile")](profiles-images/certif26.png#lightbox)


Wenn der Entwickler die von einer App-ID verwendeten Funktionen ändert (z.B. Aktivieren von iCloud oder Pushbenachrichtigungen), sollten die Bereitstellungsprofile für diese App-ID erneut erstellt werden.

## <a name="related-links"></a>Verwandte Links

- [Installation](~//mac/get-started/installation.md)
- [„Hallo, Mac“-Beispiel](~//mac/get-started/hello-mac.md)
- [Verteilen Ihrer Apps im Mac App Store](https://developer.apple.com/devcenter/mac/checklist/)
- [Tools Guide : Code Signing Your App (Tool-Leitfaden: Codesignieren Ihrer App)](https://developer.apple.com/library/mac/#documentation/ToolsLanguages/Conceptual/OSXWorkflowGuide/CodeSigning/CodeSigning.html)
- [Developer ID and GateKeeper (Entwickler-ID und Gatekeeper)](https://developer.apple.com/resources/developer-id/)
