### **Was versteht man unter Proxmox Container?**

- **Container = leichtgewichtige Virtualisierungseinheiten**  
- In Proxmox basieren sie auf **LXC (Linux Containers)**  
- Teilen sich den **Kernel mit dem Host**, daher ressourcenschonender als VMs  
- Ideal für **Linux-basierte Dienste** wie Webserver, Datenbanken, etc.  
- Schnell startbereit, geringerer Overhead als KVM-VMs

---

### **Wozu dienen Container Templates?**

- Templates sind **vorkonfigurierte, minimierte Images** von Linux-Distributionen  
- Dienen als **Basis zur schnellen Erstellung** neuer Container  
- Enthalten meist:
  - Grundsystem (z. B. Debian, Ubuntu, Alpine)
  - Minimale Paketausstattung  
- Neue Container basieren auf dem Template, was Zeit und Ressourcen spart

---

### **Unter welchem Menüpunkt im Proxmox Webinterface können Sie Container Templates herunterladen?**

1. Im Webinterface **einen Storage auswählen**, z. B. `local` oder `local-lvm`
2. In der linken Navigation:  
   **→ "Inhalt" auswählen**  
3. Oben im Menü:  
   **→ Button "Templates" klicken**  
4. Dort erscheinen alle verfügbaren **Container Templates**, die Proxmox-typisch über das Internet geladen werden können  
5. Gewünschtes Template auswählen und **auf "Herunterladen" klicken**
