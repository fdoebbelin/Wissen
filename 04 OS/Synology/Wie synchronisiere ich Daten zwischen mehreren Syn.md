Einige Artikel wurden maschinell aus dem Englischen übersetzt. Sie können Ungenauigkeiten oder Grammatikfehler enthalten. Wir möchten, dass Sie den größtmöglichen Nutzen aus unseren Artikeln ziehen können. Unter diesem Artikel können Sie uns mitteilen, ob diese Informationen für Sie hilfreich sind. Sie können unten rechts auch zur englischen Originalversion wechseln.

## <a id="x_anchor_id1"></a>Zweck

Mit Synology Drive ShareSync können Sie Daten nahtlos zwischen mehreren Synology NAS-Geräten synchronisieren.

## <a id="x_anchor_id10"></a>Umgebung

Sie betreiben Synology Drive ShareSync auf dem lokalen Synology NAS. Der zentrale Synology NAS, mit dem Sie Daten synchronisieren, wird als Remote-Host-NAS bezeichnet.

Bevor Sie beginnen, sollten Sie Folgendes sicherstellen:

- **[Synology Drive Server](https://www.synology.com/support/download)** wurde auf allen Synology NAS-Geräten installiert, die Sie synchronisieren möchten.
- Sie haben einen freigegebenen Ordner auf jedem Synology NAS-Gerät. Weitere Informationen zur Erstellung eines freigegebenen Ordners finden Sie in [diesem Artikel](https://kb.synology.com/DSM/help/DSM/AdminCenter/file_share_create).
- Sie haben die freigegebenen Ordner, die Sie synchronisieren möchten, als Team-Ordner unter **Synology Drive Admin-Konsole** \> **Team-Ordner** aktiviert.

## <a id="x_anchor_id2"></a>Lösung

Um Dateien zwischen dem Remote-NAS und dem lokalen NAS zu synchronisieren, müssen Sie zunächst eine Verbindung herstellen.

### <a id="x_anchor_id3"></a>Verbindung zwischen lokalem NAS und Remote-NAS herstellen:

1.  Öffnen Sie auf Ihrem lokalen NAS **Synology Drive ShareSync** und geben Sie die IP-Adresse (oder die QuickConnect ID), den Benutzernamen und das Kennwort Ihres Host-Synology NAS ein. Domainbenutzer verwenden Ihren Domainnamen / Benutzernamen für die Anmeldung. LDAP-Benutzer verwenden „Benutzername @ Base_DN“ für die Anmeldung. Sie können sich auch mit IPv6 anmelden.
    

Wenn Sie keine Verbindung zu Ihrem Remote-NAS herstellen können, gehen Sie zu DSM **Systemsteuerung** \> **Netzwerk** \> **Allgemein**, um den Proxy zu aktivieren. Geben Sie Ihre Proxy-Einstellungen ein, um sich mit Ihrem Remote-NAS zu verbinden. Weitere Informationen finden Sie in [diesem Artikel](https://www.synology.com/knowledgebase/DSM/help/DSM/AdminCenter/connection_network_general).

- Wenn sich Ihr Remote-NAS und die lokalen NAS-Geräte an verschiedenen Standorten befinden und Sie eine externe IP-Adresse zum Herstellen der Verbindung verwenden möchten, ist Portweiterleitung erforderlich. Da Synology Drive Server an der Verbindung beteiligt ist, muss Port 6690 auf Ihrem Router weitergeleitet werden. Weitere Informationen finden Sie in [diesem Artikel](https://www.synology.com/knowledgebase/DSM/help/DSM/AdminCenter/connection_routerconf).
- Wenn Synology Drive ShareSync das SSL-Zertifikat nicht verifizieren kann, hat es wahrscheinlich ein nicht vertrauenswürdiges, selbst signiertes Zertifikat oder jemand versucht, Ihre Verbindung abzufangen. Gehen Sie für weitere Informationen **zu DSM Systemsteuerung** \> **Sicherheit** \> **Zertifikat**. Synology Drive ShareSync verwendet 128-Bit RC4 und MD5 für die SSL-Verschlüsselung. Weitere Informationen finden Sie in [diesem Artikel](https://www.synology.com/knowledgebase/DSM/help/DSM/AdminCenter/connection_certificate).

4.  Wählen Sie die Remote- und lokalen freigegebenen Ordner aus, die Sie synchronisieren möchten, markieren Sie das Kontrollkästchen **Aktivieren** und klicken Sie auf **Übernehmen**. Weitere Informationen zu den Einstellungsoptionen finden Sie in [diesem Artikel](https://www.synology.com/knowledgebase/DSM/help/SynologyDrive/drive_sharesync).
    
5.  Nachdem die Einrichtung abgeschlossen wurde, wird eine neue Verbindung auf der linken Seite angezeigt.
    
6.  Sie können entweder weitere Synchronisierungsaufgaben mit dem angeschlossenen Synology NAS erstellen oder einen neuen Synology NAS hinzufügen, indem Sie auf klicken <img width="19" height="18" src="../../_resources/6_e754040651ab40a895923298bcc101cb.png"/> und wiederholen Sie die obigen Schritte.