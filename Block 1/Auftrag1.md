## Beantworten Sie die folgenden Fragen in der Gruppe und notieren Sie Ihre Antworten stichwortartig:

### **Welche Vorteile hat Virtualisierung?**
- Bessere Auslastung der Hardware-Ressourcen  
- Reduzierte Anschaffungskosten für physische Server  
- Einfacheres Backup und Wiederherstellung  
- Schnellere Bereitstellung von Systemen  
- Hohe Flexibilität & Skalierbarkeit  
- Isolation zwischen verschiedenen Systemen (mehr Sicherheit)  
- Energie- und Platzersparnis im Rechenzentrum  

---

### **Welche Nachteile bringt Virtualisierung mit sich?**
- Höherer Ressourcenverbrauch durch Virtualisierungs-Overhead  
- Komplexere Verwaltung bei vielen VMs  
- Abhängigkeit von Hypervisor-Software  
- Performance kann geringer sein als bei nativer Installation  
- Lizenzkosten für Virtualisierungssoftware  
- Sicherheitsrisiken bei falscher Konfiguration  

---

### **Was versteht man unter TCO?**
- *TCO = Total Cost of Ownership*  
- Gesamtkosten eines IT-Systems über die gesamte Nutzungsdauer  
- Umfasst Anschaffung, Betrieb, Wartung, Support, Energieverbrauch usw.  

---

### **Weshalb sinken die TCO mit Virtualisierung?**
- Weniger physische Server nötig → geringere Hardwarekosten  
- Geringere Strom- und Kühlkosten  
- Weniger Platzbedarf  
- Weniger Aufwand für Wartung und Management  
- Schnellere Wiederherstellung bei Ausfällen  

---

### **Was bedeutet Server-Konsolidierung im Zusammenhang mit Virtualisierung?**
- Mehrere physische Server werden auf weniger, leistungsstärkeren Servern als virtuelle Maschinen betrieben  
- Ziel: Reduktion von Hardware, Kosten, Energie und Verwaltungsaufwand  

---

### **Nennen Sie 3 verschiedene Virtualisierungsprodukte**
- VMware vSphere / ESXi  
- Microsoft Hyper-V  
- Oracle VirtualBox  
- (Bonus: Proxmox, KVM, QEMU)  

---

### **Mit welchen dieser Produkte haben Sie bereits gearbeitet?**

- VirtualBox im Schulunterricht  
- Proxmox privat für Homelab  
- VMware Workstation für Testumgebungen  

---

### **Was sind LXC und OpenVZ?**
- Container-basierte Virtualisierung (anstatt vollständiger VMs)  
- **LXC (Linux Containers):** Leichtgewichtige Container-Technologie auf Linux-Basis  
- **OpenVZ:** Ähnlich wie LXC, älter, basiert auf speziell gepatchtem Linux-Kernel  
- Nutzen denselben Kernel wie das Host-System → geringerer Overhead  
- Schnell, ressourcenschonend, aber weniger Isolation als VMs  

