# Wie werde ich Admin bei ATS
Um Admin zu werden musst Du in den Advanced Modus, denn nur so kannst Du die server_config.sii bearbeiten, was notwendig ist um Admins hinzuzufügen.

**Wichtig**: Der Server muss sich im Advanced-Modus befinden. Nach dem Wechsel in den Advanced-Modus musst du in diesem bleiben.

# Admins in der server_config.sii hinzufügen
Suchen Sie in der server_config.sii folgende Zeile:

```json
moderator_list: 0
```

Nun geben Sie die anzahl der Admins ein die Sie eintragen möchten. Als Beispiel nehmen wir mal 3 admins. Dabei muss für jeden Eintrag eine neue Zeile erstellt werden die wie folgt aufgebaut ist.

```json
moderator_list[0]: 123456789
```

Wichtig ist, dass die Zahl zwischen den eckigen Klammern bei 0 beginnt und für jeden Eintrag hoch gezählt wird. Die Zahl 123456789 ersetzen Sie durch die SteamID64 der Benutzer die Sie zum Admin machen wollen.

```json
moderator_list: 3
moderator_list[0]: 123456789
moderator_list[1]: 123456789
moderator_list[2]: 123456789
```

Wie Du die SteamID herausfindest kannst du hier nachlesen: [Wie kann ich meine SteamIDs herausfinden](https://www.4netplayers.com/de/wiki/allgemein/steamid-finden/)