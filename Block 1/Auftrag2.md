### **1. CPU (Prozessor)**
- **Viele Kerne / Threads** → Für gleichzeitige Ausführung mehrerer VMs  
- **Virtualisierungstechnologie unterstützen**  
  - Intel VT-x / VT-d  
  - AMD-V / AMD-Vi  
- **Hohe Taktfrequenz** für bessere Performance bei Single-Thread-Anwendungen  
- **Hyperthreading** aktivieren (wenn unterstützt)  
- **Mehrere Sockel (Dual-/Quad-Socket Systeme)** bei großen Umgebungen  

---

### **2. Memory (Arbeitsspeicher)**
- **Große RAM-Kapazität** → Jede VM braucht eigenen RAM  
- **ECC-RAM** (Error Correcting Code) für höhere Stabilität  
- **Hohe Bandbreite & niedrige Latenz**  
- **Genug RAM-Reserven einplanen** für zukünftige Erweiterung  
- **Memory Overcommit möglich**, aber mit Vorsicht nutzen  

---

### **3. Festplattencontroller und Disks**
- **RAID-Controller mit Cache** für bessere Performance und Redundanz  
- **Schnelle SSDs oder NVMe-Disks** → Besonders für VM-Storage und Swap wichtig  
- **Datensicherheit durch RAID (z. B. RAID 10)**  
- **Separate Disks für OS, Daten und Logs** zur Lastverteilung  
- **Unterstützung für Trim/Discard** bei SSDs  

---

### **4. Netzwerkkarten**
- **Mindestens 2–4 physische NICs**, ggf. mehr bei Bedarf  
- **Support für SR-IOV (Single Root I/O Virtualization)** → Direkter Zugriff auf NIC für VMs  
- **Hohe Bandbreite (10 Gbit/s oder mehr)**  
- **Unterstützung für VLAN-Tagging**  
- **Redundante Netzwerkanbindung (z. B. Teaming/Bonding)**  