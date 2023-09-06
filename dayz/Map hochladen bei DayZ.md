# Map hochladen bei DayZ
**Tipp**: Wir empfehlen die Verwendung eines FTP Programms wie zum Beispiel [FileZilla](https://filezilla-project.org/download.php?show_all=1).

Meistens möchtest Du eine eigene Map hochladen wenn du eine entsprechende Mod installiert hast, welche ein neue Map dem Spiel hinzufügt. Für dieses Tutorial wird die Modkarte [DeerIsle](https://steamcommunity.com/sharedfiles/filedetails/?id=1602372402) verwendet.

1. Stoppe den Server und warte bis dieser vollständig gestoppt ist.

2. Lade den Mod wie in unserem Guide [Wie installiere ich Mods in DayZ](https://www.4netplayers.com/de/wiki/dayz/wie-installiere-ich-mods/) hoch.

3. Danach benötigen wir den Map Ordner, dieser wird von den Moddern unterschiedlich bereitgestellt. Bei DeerIsle geschieht dies über [GitHub](https://github.com/johnmclane666/DayZ-Deerisle-Stable) Der Ordner den Du hier benötigst heist:
`empty.deerisle`

4. Nun verbindest Du dich, mit dem Upload-FTP unter verwendung eines FTP-Programmes und lädst den Ordner unter folgenden Pfad hoch:

`/KonfigID/mpmissions/`

**Hinweis**: Die KonfigID oder KonfigurationsID für deinen Server findest du auf unserer Seite unter Gameserver.
Wäre deine KonfigID z.B. 123456 sähe das Ganze also so aus: `/123456/mpmissions/`

5. Nachdem Du den Ordner komplett hochgeladen hast, trägst du die Map nur noch in unserem Webinterface ein, beachte dabei die Groß und Kleinschreibung.
    - **Basic Mode** Hier klickst du links auf **Map Cycle**. Auf der rechten Seite findest Du dann ein Eingabefeld. Trage hier den Namen des Ordners ein und klicke anschliesend auf das Plus (+)
    - **Advanced Mode** Wähle hier auf der linken Seite die `serverDZ.cfg` aus und scrolle dann im Texteditor runter bis Du `class Missions` siehst. Trage dort dann den ordner unter `template="empty.deerisle"` ein.

6. Klicke nun auf Speichern und starte deinen Server wieder.