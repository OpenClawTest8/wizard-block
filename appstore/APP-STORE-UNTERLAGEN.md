# Stichblock: Unterlagen für den App Store

Stand: 10. November 2026 · App-Version 1.0 (Build 1) · interne Version 1.3.0

Alle Texte sind fertig formuliert und auf die Zeichenlimits von Apple geprüft. Du kopierst sie in App Store Connect. Platzhalter in eckigen Klammern musst du selbst ausfüllen.

---

## 1. Was du selbst erledigen musst (in dieser Reihenfolge)

| Nr. | Schritt | Wo | Dauer |
|---|---|---|---|
| 1 | Apple Developer Program als Einzelperson buchen (99 USD pro Jahr) | developer.apple.com/programs | 1 bis 2 Tage Prüfung |
| 2 | Name, Anschrift und E-Mail in `datenschutz.html`, `nutzungsbedingungen.html`, `impressum.html` und `support.html` eintragen (gelb markierte Platzhalter) und auf GitHub hochladen | Repository `wizard-block` | 10 Min. |
| 3 | In App Store Connect bei „Vereinbarungen, Steuern und Bankdaten“ die Vereinbarung für kostenpflichtige Apps annehmen, Bankkonto und Steuerformulare ausfüllen. **Ohne das lässt sich kein Abo verkaufen.** | App Store Connect | 30 Min. |
| 4 | Händlerstatus nach dem Digital Services Act angeben. Wer Geld verdient, ist „Händler“. Name, Anschrift, Telefon und E-Mail werden dann im EU-App-Store öffentlich angezeigt. | App Store Connect, Geschäft | 5 Min. |
| 5 | App anlegen (Abschnitt 2), Abo anlegen (Abschnitt 6) | App Store Connect | 30 Min. |
| 6 | AdMob einrichten und IDs eintragen, RevenueCat einrichten und Schlüssel eintragen (Anleitung in `app/ANLEITUNG.md`) | admob.google.com, revenuecat.com | 1 Std. |
| 7 | Auf dem Mac: `npm install`, `npx cap sync ios`, Projekt in Xcode öffnen, Team wählen, auf eigenem iPhone testen, Testkauf mit Sandbox-Konto | Xcode | 1 Std. |
| 8 | Product, Archive, Distribute App, App Store Connect, Upload | Xcode | 20 Min. |
| 9 | Build der Version zuordnen, Screenshots hochladen, zur Prüfung einreichen | App Store Connect | 20 Min. |

Prüfdauer bei Apple: meist 1 bis 3 Tage.

---

## 2. App anlegen

| Feld | Eintrag |
|---|---|
| Plattform | iOS |
| Name | **Stichblock** |
| Primäre Sprache | Deutsch |
| Bundle-ID | `de.moritz.wizardblock` (vorher in developer.apple.com unter Identifiers anlegen; ist für Nutzer unsichtbar) |
| SKU | `stichblock-ios-001` |
| Benutzerzugriff | Uneingeschränkt |

Ich habe im App Store keine App mit dem Namen „Stichblock“ gefunden. Ob der Name frei ist, zeigt dir App Store Connect sofort beim Anlegen.

---

## 3. App-Informationen

| Feld | Eintrag |
|---|---|
| Name (max. 30) | Stichblock |
| Untertitel (max. 30) | Punktezähler für Stichspiele |
| Kategorie primär | Dienstprogramme |
| Kategorie sekundär | Unterhaltung |
| Inhaltsrechte | „Nein, sie enthält, zeigt oder greift nicht auf Inhalte Dritter zu“ |
| Altersfreigabe | siehe Abschnitt 5 |
| Datenschutzrichtlinie (URL) | https://openclawtest8.github.io/wizard-block/datenschutz.html |
| Nutzungsbedingungen | Apple-Standard-EULA (Feld leer lassen) |

---

## 4. Texte für Version 1.0

**Werbetext** (max. 170, jederzeit ohne neue Prüfung änderbar)

> Schluss mit Zettel und Kopfrechnen: Ansagen eintippen, Stiche eintragen, fertig. Alle Versionen, alle Varianten, klar und schnell am Spieltisch.

**Beschreibung** (max. 4000)

> Stichblock ersetzt den Block der Wahrheit für dein Lieblings-Stichspiel. Du tippst die Ansagen und die gewonnenen Stiche ein, den Rest erledigt die App: Punkte, Gesamtstand, Geber und Rangliste.
>
> SCHNELL AM TISCH
> • Ansagen mit Plus und Minus, der Geber sagt zuletzt an
> • Plus/Minus Eins: Die verbotene Ansage des Gebers wird angezeigt und gesperrt
> • Die App prüft, ob die Stiche zur Kartenzahl passen, und meldet Fehler sofort
> • Verdeckter Tipp und Geheime Vorhersage: Das Handy geht reihum, jeder tippt geheim
> • Bildschirm bleibt während des Spiels an
>
> ALLE VERSIONEN
> • Wizard Klassik, Deluxe und Das Schwarze Auge
> • Jubiläumsausgaben mit Bombe und Wolke
> • Wizard Junior mit eigener Wertung
> • Wizard Extreme mit Siegeln, Schwarzmagier und Strafpunkten
> • Varianten Hellsehen, Einfarbig und Wizard Maximus
> • 3 bis 10 Spieler
>
> KEIN ÄRGER BEI TIPPFEHLERN
> • Jede gewertete Runde lässt sich korrigieren, alle Folgerunden rechnen sich neu
> • Unterbrochene Spiele bleiben gespeichert und lassen sich später fortsetzen
> • Sicherung und Wiederherstellung, zum Beispiel für ein neues Handy
>
> PREMIUM
> Für 0,99 € im Jahr entfernst du die Werbung und schaltest die volle Auswertung frei:
> • Block der Wahrheit mit allen Runden
> • Punkteverlauf als Diagramm und Punkte je Runde
> • Trefferquote, Serien, zu hoch oder zu niedrig angesagt für jeden Spieler
>
> Das Abo verlängert sich automatisch um ein Jahr, wenn es nicht mindestens 24 Stunden vor Ablauf gekündigt wird. Verwalten und kündigen kannst du es in den Einstellungen deines Apple-Kontos.
>
> DEINE DATEN BLEIBEN BEI DIR
> Kein Konto, keine Anmeldung. Spielstände werden nur auf deinem Gerät gespeichert.
>
> Stichblock ist eine inoffizielle Fan-App. Wizard ist eine Marke ihres jeweiligen Inhabers. Stichblock steht in keiner Verbindung zu AMIGO oder anderen Spieleverlagen.
>
> Nutzungsbedingungen: https://www.apple.com/legal/internet-services/itunes/dev/stdeula/
> Datenschutz: https://openclawtest8.github.io/wizard-block/datenschutz.html

**Keywords** (max. 100, ohne Leerzeichen, 95 Zeichen)

```
punkteblock,stichspiel,kartenspiel,punktezähler,spieleabend,ansage,stiche,wertung,zählen,trumpf
```

„Wizard“ steht bewusst nicht in den Keywords. Apple verbietet fremde Marken dort (Richtlinie 2.3.7).

| Feld | Eintrag |
|---|---|
| Support-URL | https://openclawtest8.github.io/wizard-block/support.html |
| Marketing-URL | https://openclawtest8.github.io/wizard-block/ |
| Copyright | 2026 [Vor- und Nachname] |
| Version | 1.0 |

**Screenshots:** Die sechs Dateien aus `screenshots/` (1320 × 2868, iPhone 6,9 Zoll) in dieser Reihenfolge hochladen. Apple skaliert sie für alle kleineren iPhones. Die App ist auf iPhone beschränkt, iPad-Screenshots sind deshalb nicht nötig.

---

## 5. Altersfreigabe

Alle Fragen zu Inhalten (Gewalt, Sexualität, Glücksspiel, Drogen, Horror, Schimpfwörter, medizinische Inhalte und so weiter) mit **Keine** beziehungsweise **Nein** beantworten.

| Frage | Antwort |
|---|---|
| Unbeschränkter Webzugriff | Nein |
| Nutzergenerierte Inhalte, Nachrichten, Chat | Nein |
| Werbung | Ja |
| Glücksspiel oder simuliertes Glücksspiel | Nein |
| Wettbewerbe | Nein |

Erwartetes Ergebnis: **4+**. Die App fordert bei Google nur allgemein geeignete Anzeigen an (Einstellung „General“).

---

## 6. Abo anlegen (In-App-Käufe, Abonnements)

**Abonnementgruppe**

| Feld | Eintrag |
|---|---|
| Referenzname | Premium |
| Anzeigename (Deutsch) | Stichblock Premium |

**Abonnement**

| Feld | Eintrag |
|---|---|
| Referenzname | Premium jährlich |
| Produkt-ID | `stichblock.premium.yearly` |
| Dauer | 1 Jahr |
| Preis | 0,99 € (Deutschland als Basisland, andere Länder automatisch) |
| Anzeigename (max. 35) | Premium für ein Jahr |
| Beschreibung (max. 45) | Werbefrei, Verlauf, Block und Trefferwerte |
| Familienfreigabe | Ein (optional, wirkt kundenfreundlich) |
| Screenshot zur Prüfung | `abo-pruefung-screenshot.png` |
| Hinweis zur Prüfung | Premium entfernt das Werbebanner und schaltet die Tabs „Block“ und „Verlauf“ sowie die Trefferwerte in der Statistik frei. Erreichbar über das Werbebanner unten oder über Einstellungen, Werbefrei und volle Auswertung. |

In RevenueCat dieselbe Produkt-ID importieren, der Berechtigung `premium` zuordnen und als Paket „Annual“ ins aktuelle Angebot legen.

---

## 7. App-Datenschutz (Datenschutzangaben in App Store Connect)

Frage „Erfassen Sie oder Drittanbieter Daten aus dieser App?“: **Ja**

| Datentyp | Zweck | Mit Identität verknüpft | Für Tracking |
|---|---|---|---|
| Kennungen: Geräte-ID | Werbung durch Dritte, Analysen | Nein | Ja |
| Nutzungsdaten: Produktinteraktion | Werbung durch Dritte, Analysen | Nein | Ja |
| Nutzungsdaten: Werbedaten | Werbung durch Dritte, Analysen | Nein | Ja |
| Standort: Grober Standort | Werbung durch Dritte | Nein | Ja |
| Diagnose: Absturzdaten | App-Funktionalität | Nein | Nein |
| Diagnose: Leistungsdaten | App-Funktionalität | Nein | Nein |
| Diagnose: Andere Diagnosedaten | App-Funktionalität | Nein | Nein |
| Käufe: Kaufverlauf | App-Funktionalität | Nein | Nein |
| Kennungen: Nutzer-ID | App-Funktionalität | Nein | Nein |

Die ersten acht Zeilen stammen vom Google Mobile Ads SDK, die letzten beiden von RevenueCat. Gleiche die Tabelle vor dem Einreichen mit den aktuellen Angaben beider Anbieter ab:
- Google: developers.google.com/admob/ios/privacy/data-disclosure
- RevenueCat: revenuecat.com/docs/platform-resources/apple-platform-resources/apple-app-privacy

Spielstände, Spielernamen und Feedback werden nicht erfasst. Sie bleiben auf dem Gerät beziehungsweise gehen nur über die Teilen-Funktion an das Ziel, das der Nutzer selbst wählt.

---

## 8. Hinweise für die App-Prüfung

| Feld | Eintrag |
|---|---|
| Anmeldung erforderlich | Nein |
| Kontakt | [Vor- und Nachname], [Telefon], [E-Mail] |

**Notizen** (Englisch, weil das Prüfteam international arbeitet):

> Stichblock is a score keeper for trick-taking card games such as Wizard. No account or login is required.
>
> To test: tap "Neues Spiel starten", enter three names, tap "Spiel starten". Use plus/minus to enter bids, tap "Vorhersagen fertig", enter tricks, tap "Runde werten".
>
> Premium (auto-renewable yearly subscription, 0.99 EUR) removes the banner ad and unlocks the "Block" and "Verlauf" tabs and per-player statistics under "Tabelle". The paywall opens by tapping the bottom banner, a locked tab, or Settings (gear icon on the home screen) > "Werbefrei und volle Auswertung". "Käufe wiederherstellen" is on the paywall.
>
> Ads are served by Google AdMob with max ad content rating "General". The app shows Google's consent form (UMP) and the App Tracking Transparency prompt before ads are requested.
>
> The app is an unofficial fan app and is not affiliated with the publishers of the card game. Game names are used descriptively only.

---

## 9. Exportvorschriften

Beantwortet sich automatisch: In `Info.plist` ist `ITSAppUsesNonExemptEncryption = NO` gesetzt. Die App nutzt nur die Verschlüsselung des Betriebssystems (HTTPS).

---

## 10. Was im Projekt bereits vorbereitet ist

- App-Name „Stichblock“ auf dem Homescreen, nur iPhone, nur Hochformat
- App-Icon 1024 × 1024 ohne Transparenz
- Datenschutz-Manifest `PrivacyInfo.xcprivacy` für die App selbst. Google, RevenueCat und Capacitor bringen eigene Manifeste mit, Xcode fügt alle zusammen.
- Tracking-Abfrage mit deutschem Text, Google-Einwilligungsabfrage, `SKAdNetworkItems` (50 Einträge laut Google)
- Kauf-Fenster mit Preis, Laufzeit, Hinweis zur Verlängerung, „Käufe wiederherstellen“ sowie Links zu Nutzungsbedingungen und Datenschutz
- „Abo verwalten“ in den Einstellungen bei aktivem Abo
- Rechtstexte, Impressum und Support-Seite online

---

## 11. Risiken bei der Prüfung und was dann zu tun ist

| Risiko | Einschätzung | Falls abgelehnt |
|---|---|---|
| Marke „Wizard“ in der App (Richtlinie 5.2.1) | Mittel. Andere Zähl-Apps nutzen den Namen beschreibend und sind im Store. Die App nennt ihn nur als Spielversion mit Hinweis „inoffiziell“. | Spielversion in der App umbenennen, zum Beispiel „Klassik“ statt „Wizard“, und den Namen nur noch in der Beschreibung nennen. |
| Jahresabo für eine kleine App (Richtlinie 3.1.2) | Gering bis mittel. Apple verlangt bei Abos einen fortlaufenden Wert. Werbefreiheit plus Auswertung wird meist akzeptiert. | Auf einen einmaligen Kauf („nicht verbrauchbar“) für 0,99 € umstellen. In der App ist das eine kleine Änderung. |
| Testanzeigen im Build | Hoch, wenn vergessen | Vor dem Archivieren in `MONETIZE` die eigenen AdMob-IDs eintragen und `adTesting: false` setzen. |
| Platzhalter in den Rechtstexten | Hoch, wenn vergessen | Schritt 2 aus Abschnitt 1. |
| GitHub-Name „OpenClawTest8“ in den URLs | Kein Ablehnungsgrund | Später eigene Domain, dann URLs in App Store Connect und in `WEB_BASE` in der App ändern. |

---

## 12. Dateien in diesem Paket

- `APP-STORE-UNTERLAGEN.md` (dieses Dokument)
- `screenshots/01_ansage.png` bis `06_versionen.png` (1320 × 2868)
- `abo-pruefung-screenshot.png` (Kauf-Fenster für die Abo-Prüfung)
- `app-icon-1024.png`
- Rechtstexte liegen online und im Repository: `datenschutz.html`, `nutzungsbedingungen.html`, `impressum.html`, `support.html`
