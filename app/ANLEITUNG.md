# Wizard Block als Mobile App

Es gibt zwei Wege, die sich nicht ausschließen.

| | Weg 1: Web-App installieren | Weg 2: Store-App mit Capacitor |
|---|---|---|
| Ergebnis | Icon auf dem Homescreen, Vollbild, offline | Echte App im App Store und Play Store |
| Kosten | 0 € (kostenloses Hosting) | Apple 99 USD pro Jahr, Google einmalig 25 USD |
| Aufwand | ca. 10 Minuten | Android ca. 1 Stunde, iOS braucht einen Mac mit Xcode |
| Updates | Datei ersetzen, fertig | Neuer Build und erneute Prüfung durch den Store |

## Weg 1: Web-App (Ordner `wizard-block-pwa`)

Der Ordner enthält `index.html`, `manifest.webmanifest`, `sw.js` und `icons/`. Er muss über **https** erreichbar sein, sonst funktionieren Installation und Offline-Modus nicht.

**Hosting, am einfachsten mit Netlify Drop:**
1. app.netlify.com/drop öffnen und den Ordner `wizard-block-pwa` in das Fenster ziehen.
2. Netlify vergibt eine Adresse wie `https://irgendwas.netlify.app`. Den Namen kannst du in den Site-Einstellungen ändern.

Gleichwertig gehen Cloudflare Pages oder GitHub Pages.

**Auf dem iPhone installieren:** Adresse in Safari öffnen, Teilen antippen und „Zum Home-Bildschirm“ wählen.
**Auf Android installieren:** Adresse in Chrome öffnen. Entweder erscheint „App installieren“ direkt, oder du findest es im Menü mit den drei Punkten.

Danach startet die App im Vollbild, läuft ohne Internet und speichert Spiele auf dem Gerät.

**Update:** Datei ersetzen und in `sw.js` die Zeile `const VERSION = 'wizard-block-v1'` hochzählen. Beim nächsten Öffnen mit Internet holt sich die App die neue Version.

## Weg 2: Store-App (Ordner `wizard-block-app`)

Das Capacitor-Projekt ist fertig eingerichtet. Android und iOS sind angelegt, Icons und Startbildschirm erzeugt, und die App ist auf Hochformat festgelegt. Eingebaut sind die Plugins Statusleiste, Haptik (Vibration bei Plus und Minus) und App (Android-Zurück-Taste).

### Einmalig vorbereiten
1. Node.js 20 oder neuer installieren (nodejs.org).
2. Im Ordner `wizard-block-app` ein Terminal öffnen und `npm install` ausführen.
3. In `capacitor.config.json` die `appId` auf eine eigene Kennung ändern, zum Beispiel `de.deinname.wizardblock`. **Die Kennung lässt sich nach der ersten Veröffentlichung nicht mehr ändern.** Danach `npx cap sync` ausführen.

### Android
1. Android Studio installieren.
2. `npm run android` öffnet das Projekt in Android Studio.
3. Zum Testen das Handy per USB verbinden (Entwickleroptionen und USB-Debugging aktivieren) und auf Run klicken.
4. Für den Play Store: Build, dann Generate Signed App Bundle. Den Keystore sicher aufbewahren, ohne ihn kannst du keine Updates mehr hochladen.
5. In der Play Console die App anlegen und das `.aab` hochladen. Neue private Entwicklerkonten müssen vor der Freigabe einen geschlossenen Test mit 12 Testern über 14 Tage durchführen.

### iOS (nur auf einem Mac)
1. Xcode aus dem Mac App Store installieren.
2. `npm run ios` öffnet das Projekt in Xcode. Die Abhängigkeiten laufen über den Swift Package Manager, CocoaPods ist nicht nötig.
3. Unter Signing & Capabilities dein Team (Apple-Developer-Konto) auswählen.
4. Zum Testen das iPhone verbinden und auf Run klicken.
5. Für den App Store: Product, dann Archive und Distribute App. Über TestFlight kannst du vorher testen.

### Nach Änderungen an der App
Neue `index.html` nach `www/` kopieren und `npx cap sync` ausführen. Danach wie oben neu bauen.

### Icons neu erzeugen
Die Quellbilder liegen in `assets/`. Nach einer Änderung `npm run assets` ausführen.

## Vor der Store-Veröffentlichung klären
- **Name:** Im App Store gibt es bereits eine App namens „WizardBlock“ (0,99 USD, anderer Entwickler). „Wizard Block“ scheidet deshalb als Store-Name aus. Andere Zähl-Apps weisen außerdem darauf hin, dass „Wizard“ eine eingetragene Marke von Wizard Cards International ist. Empfehlung: eigener Name ohne „Wizard“ (zum Beispiel „Stichblock“ oder „Trickbook“), im Untertitel „Punkteblock für Wizard“ und in der Beschreibung der Hinweis „inoffizielle Fan-App“. Vor dem Einreichen den Wunschnamen bei DPMA und EUIPO sowie in beiden Stores suchen.
- **Datenschutzerklärung:** Beide Stores verlangen eine. Sie liegt fertig als `datenschutz.html` vor und ist unter dem Pages-Link erreichbar. Vor der Veröffentlichung musst du oben nur noch Name, Anschrift und E-Mail eintragen. Die App sammelt keine Daten und speichert nur lokal auf dem Gerät. Das muss auch so in den Datenschutzangaben stehen.
- **Werbung und In-App-Kauf** wie bei der Catan App sind noch nicht eingebaut.
