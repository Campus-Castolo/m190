### **Wie unterscheiden sich Hypervisor Typ 1 und Typ 2?**

**Hypervisor Typ 1 (Bare Metal):**  
- Läuft **direkt auf der Hardware**  
- Keine darunterliegende Host-OS-Schicht  
- Beispiel: VMware ESXi, Microsoft Hyper-V (als Core), Xen  
- **Höhere Performance & Stabilität**  
- Wird oft in Rechenzentren eingesetzt

**Hypervisor Typ 2 (Hosted):**  
- Läuft **auf einem bestehenden Betriebssystem**  
- Beispiel: VirtualBox, VMware Workstation  
- **Einfachere Installation**, aber weniger effizient  
- Eher für Test- und Entwicklungsumgebungen  

---

### **Was versteht man unter Applikationsvirtualisierung?**

- Anwendung wird vom **Betriebssystem getrennt ausgeführt**  
- Anwendung läuft in einer isolierten Umgebung  
- Keine lokale Installation notwendig  
- Beispiele: **Microsoft App-V**, **Citrix Virtual Apps**  
- Vorteil: **Einfaches Deployment**, keine Konflikte zwischen Programmen  

---

### **Was versteht man unter Desktop-Virtualisierung (VDI)?**

- **Virtueller Desktop läuft im Rechenzentrum**  
- Benutzer greifen über Remote-Verbindung darauf zu  
- Betriebssystem, Anwendungen und Daten sind zentral gespeichert  
- Vorteile:  
  - Einfaches Management  
  - Erhöhte Sicherheit  
  - Zugriff von überall möglich  
- Beispiel: **Citrix VDI**, **VMware Horizon**, **Microsoft AVD**  

---

### **Wie unterscheiden sich Container von virtuellen Maschinen?**

| **Virtuelle Maschinen** | **Container** |
|-------------------------|---------------|
| Enthalten komplettes OS | Teilen sich den Kernel |
| Mehr Ressourcenverbrauch | Leichtgewichtig, schneller Start |
| Isolierter, höhere Sicherheit | Weniger isoliert |
| Beispiel: VMware, Hyper-V | Beispiel: Docker, LXC |

---

### **Wie unterscheiden sich Emulation und Virtualisierung?**

**Emulation:**  
- **Vollständige Nachbildung** einer anderen Hardwareplattform  
- Ermöglicht Ausführung von Software, die nicht nativ unterstützt wird  
- **Langsamer**, da jede Instruktion übersetzt wird  
- Beispiel: Emulator für Gameboy auf PC

**Virtualisierung:**  
- Nutzt vorhandene Hardware **direkt und effizient**  
- Läuft fast nativ, mit geringem Overhead  
- Beispiel: Virtuelle Windows-Maschine auf Hyper-V

---

### **Welche physischen IT-Ressourcen neben Servern können virtualisiert werden?**

- **Netzwerke** → Netzwerkvirtualisierung, z. B. VLANs, SDN  
- **Speicher** → z. B. virtuelle SANs, Storage Pools  
- **Desktops** → über VDI (virtuelle Desktop-Infrastruktur)  
- **Firewalls / Router** → als virtuelle Appliances  
- **Load Balancer** → in Form von Softwarelösungen  
- **Switches** → z. B. virtuelle Switches in Hypervisoren  
