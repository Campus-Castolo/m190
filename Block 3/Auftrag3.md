### **Was versteht man unter Write-Back Cache?**

- Schreibzugriffe landen **zuerst im Cache**, nicht direkt auf der Festplatte  
- Daten werden **zeitverzögert** auf den Datenträger geschrieben  
- **Schneller** als Write-Through  
- **Risiko**: Bei Stromausfall können ungeschriebene Daten verloren gehen  
- **Batteriegeschützter Cache** (BBU) empfohlen

---

### **Was versteht man unter Write-Through Cache?**

- Schreibzugriffe werden **direkt auf die Festplatte geschrieben**  
- Cache wird nur zur Beschleunigung von Lesevorgängen genutzt  
- **Sicherer**, aber **langsamer** als Write-Back  
- Keine Datenverluste bei Stromausfall  

---

### **Welche Vor- und Nachteile haben SSD-Festplatten beim Einsatz als VM-Storage?**

**Vorteile:**  
- **Hohe IOPS** (Input/Output-Operationen pro Sekunde)  
- **Schnelle Zugriffszeiten** → bessere VM-Performance  
- **Geringe Latenz**, ideal für viele gleichzeitige Zugriffe  
- **Kein mechanischer Verschleiß**

**Nachteile:**  
- Höherer Preis pro GB  
- Begrenzte Lebensdauer (Write-Cycles)  
- Billige SSDs (ohne DRAM-Cache) können im Dauerbetrieb instabil sein  

---

### **Welche Eigenschaft ist entscheidend für Festplatten, die Sie für einen Virtualisierungshost mit mehreren VMs verwenden wollen?**

- **Hohe IOPS** und **niedrige Latenz**  
- **Zuverlässigkeit und Dauerbetrieb-Freigabe** (z. B. Enterprise-SSDs oder Server-HDDs)  
- **RAID-Fähigkeit**  
- **Cache mit Schutz (BBU)**  
- Ggf. **Durchsatz bei parallelen Zugriffen**

---

### **Was versteht man unter Shared Storage?**

- Gemeinsamer Speicher, der **von mehreren Hosts gleichzeitig verwendet werden kann**  
- Häufig verwendet bei **Cluster-Umgebungen**, **HA (High Availability)** und **vMotion**  
- Beispiele:  
  - SAN (Storage Area Network)  
  - NAS (Network Attached Storage)  
  - iSCSI, NFS  

---

### **Vor- und Nachteile eines Shared Storage für virtuelle Disks**

**Vorteile:**  
- **Zentrale Verwaltung** der Daten  
- **Live-Migration (vMotion)** von VMs möglich  
- **Hochverfügbarkeit & Clustering** möglich  
- **Skalierbarkeit**

**Nachteile:**  
- **Komplexere Einrichtung und Verwaltung**  
- **Kostenintensiv**  
- **Performance abhängig vom Netzwerk**  
- **Single Point of Failure** ohne Redundanz  

---

### **Wie unterscheiden sich die NFS I/O Modes `sync` und `async`?**

| **Modus** | **Verhalten** | **Vorteile** | **Nachteile** |
|-----------|----------------|--------------|----------------|
| **sync**  | Daten werden **sofort** geschrieben und bestätigt | **Datensicherheit**, konsistentes Dateisystem | **Langsamer**, höhere Latenz |
| **async** | Daten werden **gepuffert** und später geschrieben | **Schneller**, bessere Performance | **Risiko** bei Stromausfall – Datenverlust möglich |
