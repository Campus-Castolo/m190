### **Welche Daten werden bei einem VMware Snapshot gesichert?**

- **Zustand der VM im Moment des Snapshots**, inkl.:
  - **Virtuelle Festplatten (nur Änderungen!)**
  - **Arbeitsspeicher (optional)**  
  - **Gerätezustände (z. B. CPU, Netzwerk, angeschlossene Medien)**
- Kein vollständiges Backup – Snapshots speichern **nur Änderungen (Delta-Files)**  
- Festplatten erhalten `.vmdk`-Differenzdateien  

---

### **Wie viel Speicherplatz benötigt ein Snapshot?**

- **Abhängig von der Aktivität der VM nach dem Snapshot**
  - Kaum Änderungen → wenig Speicher
  - Viel I/O → schnell mehrere GB
- Speicherbedarf **steigt mit Laufzeit und Änderungen**  
- Optional: Speicherabbild des RAM → zusätzlich mehrere GB

---

### **Snapshot-Optionen im Überblick:**

#### **Revert (Wiederherstellen):**
- VM wird in **genauen Zustand des Snapshots zurückgesetzt**  
- Alle Änderungen **nach dem Snapshot gehen verloren**  
- Wird oft zum Testen oder vor Updates genutzt

#### **Edit (Umbenennen):**
- Snapshot kann **neu benannt oder kommentiert** werden  
- Nützlich zur besseren Nachverfolgbarkeit

#### **Delete (Löschen):**
- **Änderungen werden mit dem vorherigen Zustand zusammengeführt** (Merge)  
- Daten bleiben erhalten – Snapshot-Datei wird entfernt  
- Achtung: **Nicht wie "Rückgängig"**, sondern eher **"Zusammenführen + Aufräumen"**

---

### **Was ist die empfohlene Maximaldauer eines VMware Snapshots?**

- **Max. 72 Stunden (3 Tage)**  
  - **Je kürzer, desto besser**  
- Länger laufende Snapshots können zu:
  - **Leistungsproblemen**
  - **Instabilität**
  - **Schwieriger Konsolidierung**
  - **Speicherüberlauf** führen

---

### **Was versteht man unter Klon?**

- **Kopie einer VM** auf Basis des aktuellen Zustands oder Snapshots  
- Kann **unabhängig** von der Original-VM verwendet werden  
- Zwei Varianten: **Linked Clone** und **Full Clone**

---

### **Wie unterscheiden sich Linked und Full Clones?**

| **Typ**         | **Beschreibung**                                        | **Vorteile**                     | **Nachteile**                              |
|------------------|----------------------------------------------------------|----------------------------------|---------------------------------------------|
| **Full Clone**   | Vollständige, unabhängige Kopie der VM                  | Eigenständig, keine Abhängigkeit | Braucht viel Speicherplatz                  |
| **Linked Clone** | Verweist auf Original-Snapshot (Differenzdateien)       | Spart Speicher, schneller erstellt | Abhängig vom Original, langsamer bei I/O    |

---

### **Snapshot in ESXi erstellen (Kurzanleitung über vSphere Web Client):**

1. VM auswählen  
2. Rechtsklick → **Snapshots** → **Take Snapshot**  
3. Name und Kommentar eingeben  
4. Optional:  
   - **Speicherabbild des RAM einschließen**  
   - **Quiesce Guest File System** (für konsistente Disk-Zustände, falls Tools installiert)  
5. **Snapshot erstellen**