### 🔑 Wichtigste Schritte aus dem Video (stichwortartig)
- **VMware Converter herunterladen** von der offiziellen VMware-Webseite
- **Installation lokal** auf einem Windows-Rechner durchführen
- **Start der Anwendung**, Quelle (physischer Rechner) auswählen
- **Agent auf Quellmaschine installieren**, Snapshot der Volumes erstellen
- **Zielsystem auswählen** (z. B. ESXi-Host), IP-Adresse und Zugangsdaten eingeben
- **Netzwerkkonfiguration** (Proxy-Modus ein/aus)
- **Virtuelle Maschine konfigurieren**: Name, Speicherort, Hardware, Festplattentyp (thick/thin)
- **Konvertierung starten**, Daten werden übertragen und VM auf Ziel erstellt
- **Nach Abschluss optional Agent vom Quellsystem entfernen**

---

### 🧭 Was bedeutet Live Migration / vMotion?
**Live Migration**, bei VMware auch **vMotion** genannt, beschreibt den **nahtlosen Transfer einer laufenden virtuellen Maschine (VM) von einem Host zu einem anderen**, ohne dass die VM heruntergefahren werden muss.

🔍 **Kernaspekte von vMotion:**
- **Keine Downtime**: Die VM läuft während des Umzugs weiter, Dienste bleiben erreichbar.
- **Speicher und Zustand der VM** (RAM, CPU-Zustand etc.) werden im laufenden Betrieb auf das Zielsystem übertragen.
- **Netzwerkverbindungen bleiben bestehen**, was für produktive Umgebungen essenziell ist.
- **Häufig verwendet für Wartung, Lastverteilung oder Notfallmaßnahmen**

🛠️ **Hinweis zum Video:**  
Das im Video gezeigte Verfahren (mittels VMware Converter) ist **keine Live Migration**, sondern eine **P2V-Konvertierung (Physical to Virtual)**. Dabei wird ein **laufendes physisches System in eine VM umgewandelt** – im Gegensatz zu vMotion, bei dem es sich um den Umzug einer bereits vorhandenen VM handelt.
