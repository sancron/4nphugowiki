# Wie setze ich ein Passwort bei Enshrouded
Seit dem Update 2 wurde die Art und Weise wie man ein Passwort bei Enshourded setzt geändert. Im nachfolgenden Beitrag möchte ich auf die Besonderheiten eingehen.

# Benutzergruppen
Mit dem Update 2 wurde bei Enshrouded, Benutzergruppen eingefügt. Die Gruppen bestimmen die Zugriffsrechte und haben jeweils ein eigenes Passwort. Jenachdem welches Passwort beim Verbinden verwendet wird, wird der Spieler der bestimmten Gruppe zugeordnet.

Standardmässig gibt es 3 Benutzergruppen die vordefiniert sind mit folgenden Rechten:
* Admin
    * Änderungen an den Spieler-Basen sind erlaubt.
    * Die Verwendung von Truhen und anderen Behältern ist erlaubt.
    * Das Kicken und Bannen anderer Spieler ist erlaubt.
* Friend (Freund)
    * Änderungen an den Spieler-Basen sind erlaubt.
    * Die Verwendung von Truhen und anderen Behältern ist erlaub.
* Guest (Gast)
    * Änderungen an den Spieler-Basen sind nicht erlaubt.
    * Die Verwendung von Truhen und anderen Behältern ist nicht erlaubt.

Eine Einstellung die dazugekommen ist mit den Gruppen, sind reservierte Slot, die man für jede Nutzergruppe individuell konfiguriert kann.

**WICHTIG** Alle Nutzergruppen haben vollständigen Zugang zur Spielwelt außerhalb der Spieler-Basen und können sich an Kämpfen beteiligen, Ressourcen sammeln, Quests lösen, usw.

# Passwörter setzen (Basic Modus)
In unserem Webinterface unter Server Einstellungen können Sie einfach für alle drei Gruppen ein Passwort setzen. Dabei gibt es folgendes zu beachten:
* Die Passwörter für die einzelnen Gruppen, dürfen nicht gleich sein.
* Mindestens die Admin und Freunde Gruppe benötigt ein Passwort.
* Die Gastgruppe braucht als einziges kein Passwort.

# Passwörter setzen (Advanced Modus)
Im Advanced Modus könnt ihr einfach die Passwörter in den dafür vorgesehen Configeinträgen individualisieren und anpassen. Bei bedarf könnt ihr hier sogar mehr Gruppen hinzufügen.

```json
{
    "name": "Enshrouded Server",
    "password": "",
    "saveDirectory": "./savegame",
    "logDirectory": "./logs",
    "ip": "0.0.0.0",
    "queryPort": 15637,
    "slotCount": 16,
    "userGroups": [
        {
            "name": "Admin",
            "password": "Randomized password 01",
            "canKickBan": true,
            "canAccessInventories": true,
            "canEditBase": true,
            "canExtendBase": true,
            "reservedSlots": 1
        },
        {
            "name": "Friend",
            "password": "Randomized password 02",
            "canKickBan": false,
            "canAccessInventories": true,
            "canEditBase": true,
            "canExtendBase": true,
            "reservedSlots": 3
        },
        {
            "name": "Guest",
            "password": "Randomized password 03",
            "canKickBan": false,
            "canAccessInventories": false,
            "canEditBase": false,
            "canExtendBase": false,
            "reservedSlots": 0
        }
    ]
}
```