# Datenschutzerklärung — PersonenDB

**Stand: Mai 2026**

Der Schutz Ihrer Daten und der Daten Ihrer Klienten hat für uns oberste Priorität. PersonenDB ist als **lokal-first** Anwendung konzipiert. Dies bedeutet, dass die Verarbeitung sensibler Daten ausschließlich auf Ihrem Endgerät stattfindet.

## 1. Verantwortliche Stelle
Die Verarbeitung der Daten erfolgt direkt durch den Nutzer der App (Endanwender) in seiner Funktion als datenschutzrechtlich Verantwortlicher (z. B. Therapeut, Coach, Berater). Es werden keine Daten an den Entwickler der App übermittelt.

## 2. Grundsatz: Keine Datenübertragung (Offline-Integrität)
* **Keine Cloud-Speicherung:** PersonenDB verfügt über keine eigenen Server-Infrastrukturen. Alle von Ihnen eingegebenen Personenstammdaten, Verbindungen, Notizen und Sprachnotizen verbleiben lokal auf Ihrem Gerät.
* **Kein Tracking, keine Analyse:** Die App verwendet keine Tracker, Werbe-IDs oder Analysetools (wie Google Analytics oder Firebase). Ihr Nutzungsverhalten wird nicht aufgezeichnet.

## 3. Lokale Verschlüsselung & Gerätesicherheit
* **Field-Encryption:** Sensible Datenkategorien (wie psychologische Notizen oder Gesundheitsdaten) werden vor dem Ablegen in der lokalen SQLite-Datenbank verschlüsselt.
* **Schlüsselverwaltung:** Die kryptografischen Schlüssel werden sicher im nativen Keystore/SecureStore Ihres Betriebssystems verwaltet. Der Zugriff ist an die biometrische Entsperrung (Face ID / Touch ID / Geräte-Passcode) Ihres Geräts gekoppelt.
* **Kaskadierendes Löschen:** Wenn Sie einen Datensatz oder eine Sprachnotiz in der App löschen, werden die dazugehörigen Fragmente und Mediendateien restlos vom physischen Speicher des Geräts entfernt.

## 4. Erforderliche Geräteberechtigungen
Die App fordert Zugriff auf folgende Systemfunktionen an, die ausschließlich lokal genutzt werden:
* **Mikrofon (`RECORD_AUDIO`):** Erforderlich für das Aufnehmen von lokalen Sprachnotizen innerhalb der Klientenprofile.
* **Standort (`ACCESS_FINE_LOCATION`):** Wird ausschließlich genutzt, um die geografische Übersicht Ihrer Kontakte auf der lokalen Netzwerkkarte darzustellen. Es findet keine Standortübermittlung statt.
* **Kontakte (`READ_CONTACTS`):** Ermöglicht den optionalen Import bestehender Kontakte zur manuellen Deduplizierung.

## 5. Rechte der Betroffenen
Da alle Daten ausschließlich auf Ihrem Gerät gespeichert sind, können Sie Auskunfts-, Berichtigungs- oder Löschungsanfragen Ihrer Klienten jederzeit selbstständig und direkt in der App durchführen, indem Sie die entsprechenden Profile bearbeiten oder löschen.
