# Mods installieren bei Arma Reforger
Für die Installation einer Modifikation benötigst du die ModID, Name und Version der Modifikation. All diese Informationen findest im [Workshop](https://reforger.armaplatform.com/workshop/) auf der Seite für die Modifikation von Arma Reforger.

Die Mods werden bei Arma Reforger wenn Sie in der Serverkonfiguration eingetragen sind, automatisch vom Server heruntergeladen, ein separates Hochladen der Mods ist nicht nötig.

**Wichtig**: Das Hinzufügen von Mods funktioniert nur im Advanced Modus. Nach dem Wechsel in den Advanced Modus, muust du in dem Modus blkeiben.

## Mods in der config.json hinzufügen
Nach dem wechsel in den Advanced Modus, suche in der config.json den Eintrag

```json
"mods": []
```

Um jetzt einen Mod hinzuzufügen trage diesen wie folgt ein. Alle Informationen die du benötigst sind auf der Workshopseite der Modifikation vermerkt.

```json
"mods": [
    {
        "modId": "591AF5BDA9F7CE8B",
        "name": "Capture & Hold",
        "version": "1.0.3"
    }
]
```

Möchtest du mehr als einen Mod hinzufügen, dann füge einfach einen weiteren Abschnitt hinzu wie hier:

```json
"mods": [
    {
        "modId": "591AF5BDA9F7CE8B",
        "name": "Capture & Hold",
        "version": "1.0.3"
    },
    {
        "modId": "5614E481506D2979",
        "name": "Sample Mod - New Weapon",
        "version": "1.0.4"
    },
    {
        "modId": "5614E482BF83E310",
        "name": "Sample Mod - New Car",
        "version": "1.0.5"
    }
]
```

Wichtig ist dass hier der Syntax eingehalten wird, damit der Server erfolgreich starten kann. Um sicherzustellen dass du keinen Fehler gemacht hast, kannst du dazu auch einen Online JSON Validator verwenden wie diesen hier: [JSONLint](https://jsonlint.com/) und die Konfiguration einfach über Kopieren und Einfügen dort testen.