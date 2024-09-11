## Vorbereitung

### 1. Anpassung der Hosts-Datei

Damit das CRM unter der URL crm.local erreichbar ist, musst du die Hosts-Datei deines Computers anpassen.

1. Öffne den **Editor** oder ein anderes Textbearbeitungsprogramm deiner Wahl als **Administrator** (Rechtsklick auf das Programmsymbol und „Als Administrator ausführen“ wählen).
2. Öffne die Datei unter folgendem Pfad:

   `C:\Windows\System32\drivers\etc\hosts`
   
3. Füge am Ende der Datei folgende Zeile hinzu:

Hier ist die überarbeitete Version deiner Anleitung im Markdown-Format:

```
192.168.168.115 crm.local
```


Diese Anpassung leitet die Domain `crm.local` auf die interne IP-Adresse `192.168.168.115` um.

4. Speichere die Datei. Sollte das Speichern nicht möglich sein, überprüfe, ob das Programm als Administrator läuft.

Das CRM ist nun unter der URL [https://crm.local](https://crm.local) erreichbar.

---

### 2. Zulassen eines selbstsignierten Zertifikats

Beim erstmaligen Öffnen des CRM unter der URL [https://crm.local](https://crm.local) wirst du eine Sicherheitswarnung erhalten, da das Zertifikat selbstsigniert ist.

1. Es erscheint die folgende Warnung:

![[ss_error.png.png]]

2. Klicke auf **Erweitert** und dann auf „Weiter zu crm.local (unsicher)“, um fortzufahren.

![[ss_error2.png.png]]

**Hinweis**: Die Warnung erscheint, weil das Zertifikat nicht von einer vertrauenswürdigen Zertifizierungsstelle stammt, was in internen Testumgebungen üblich ist.

---

### 3. Anmeldung am CRM

Nachdem die Sicherheitswarnung umgangen wurde, solltest du den folgenden Login-Bildschirm sehen:

![[login.png.png]]

1. Gib die Login-Daten ein, die du per E-Mail erhalten hast.
2. (Der „Remember me“-Haken hat aktuell noch keine Funktion.)
