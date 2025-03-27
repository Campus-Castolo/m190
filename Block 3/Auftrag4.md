### **Welche Möglichkeiten gibt es, eine virtuelle Maschine zu sichern?**

- **Snapshot-Erstellung** (nur kurzfristig empfohlen)  
- **Backup auf Hypervisor-Ebene** (z. B. Veeam, Altaro, Nakivo)  
- **Backup der virtuellen Festplatten (.vmdk, .vhdx etc.)**  
- **Agentenbasierte Backups in der VM selbst** (z. B. Windows-Backup, Datenbank-Agenten)  
- **Image-Backup der gesamten VM**  
- **Replikation auf anderen Host** (z. B. für Failover-Zwecke)

---

### **Welche Probleme gibt es bei der Sicherung von Datenbankservern?**

- **Offene Datenbankverbindungen** → Daten könnten sich während des Backups ändern  
- **Inkonsistente Daten ohne VSS oder Datenbankagenten**  
- **Hoher I/O während Backup-Zeitfenster** → kann Performance beeinträchtigen  
- **Sperren oder Locks** können auftreten  
- **Transaktionsverluste** bei nicht abgestimmten Backups  
- **Backup-Wiederherstellung ohne passende Logs schwierig**

---

### **Welche Gemeinsamkeiten haben Backups von Datenbankservern und VM-Disks?**

- Beide benötigen **Konsistenzsicherung**:
  - Z. B. durch **VSS (Volume Shadow Copy Service)** bei Windows  
  - Oder **Datenbank-spezifische Tools** (z. B. mysqldump, RMAN bei Oracle)  
- Beide können **schnell groß werden** → effiziente Speicherung wichtig (z. B. mit Deduplizierung)  
- **Snapshot-basierte Backups** möglich  
- Wiederherstellung kann **vollständig oder granular** erfolgen (ganze VM oder einzelne DB-Datei)

---

### **Welche Vorteile bietet ein Shared Storage für die Sicherung der virtuellen Maschinen?**

- **Zentraler Speicherort** → Backup-Software hat einfachen Zugriff auf alle VM-Daten  
- **Snapshots direkt auf Storage-Ebene möglich** (z. B. bei SANs oder Storage-Systemen mit Snapshot-Funktion)  
- **Schnellere Sicherung und Wiederherstellung** durch hohe Durchsatzraten  
- **Konsolidierte Backup-Strategie** für viele Hosts gleichzeitig  
- **VM-Migration (vMotion) ohne Backup-Unterbrechung**  
- **Replikation oder Spiegelung des Storage** für zusätzliche Ausfallsicherheit  