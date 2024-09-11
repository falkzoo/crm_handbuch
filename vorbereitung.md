# Vorbereitung

## 1. Anpassung der Hosts-Datei

Damit das CRM unter der URL crm.local erreichbar ist, musst du die Hosts-Datei deines Computers anpassen.

1. Öffne den **Editor** oder ein anderes Textbearbeitungsprogramm deiner Wahl als **Administrator** (Rechtsklick auf das Programmsymbol und „Als Administrator ausführen“ wählen).
2. Öffne die Datei unter folgendem Pfad:

   `C:\Windows\System32\drivers\etc\hosts`
   
3. Füge am Ende der Datei folgende Zeile hinzu:

```
192.168.168.115 crm.local
```

Diese Anpassung leitet die Domain `crm.local` auf die interne IP-Adresse `192.168.168.115` um.

4. Speichere die Datei. Sollte das Speichern nicht möglich sein, überprüfe, ob das Programm als Administrator läuft.

Das CRM ist nun unter der URL [https://crm.local](https://crm.local) erreichbar.

---

## 2. Zulassen eines selbstsignierten Zertifikats

Beim erstmaligen Öffnen des CRM unter der URL [https://crm.local](https://crm.local) wirst du eine Sicherheitswarnung erhalten, da das Zertifikat selbstsigniert ist.

1. Es erscheint die folgende Warnung:

![Warnung](https://raw.githubusercontent.com/falkzoo/crm_handbuch/main/images/selfsigned.png)

2. Klicke auf **Erweitert** und dann auf „Weiter zu crm.local (unsicher)“, um fortzufahren.

![Warnung2](https://raw.githubusercontent.com/falkzoo/crm_handbuch/main/images/selfsigned2.png)

**Hinweis**: Die Warnung erscheint, weil das Zertifikat nicht von einer vertrauenswürdigen Zertifizierungsstelle stammt, was in internen Testumgebungen üblich ist.
