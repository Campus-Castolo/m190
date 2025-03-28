### **Was versteht man unter V2V?**

- **V2V = Virtual to Virtual**  
- Migration einer **virtuellen Maschine von einem Virtualisierungssystem auf ein anderes**
- Beispiel: **VM von VMware ESXi nach Proxmox (KVM/QEMU)**  
- Ziel: Plattformwechsel oder Konsolidierung

---

### **Welchen Hypervisor verwendet Proxmox?**

- **Proxmox VE (Virtual Environment)** verwendet:
  - **KVM/QEMU** für vollständige Virtualisierung  
  - **LXC (Linux Containers)** für containerbasierte Virtualisierung  
- Verwaltung über ein zentrales Webinterface oder CLI

---

### **Welche Schritte sind notwendig, um eine ESXi VM auf Proxmox zu migrieren?**

#### **1. Vorbereitung auf ESXi:**
- **Snapshot löschen**
- **VM herunterfahren**
- **VM auf “thick provisioned” umwandeln** (optional, aber stabiler)
- Exportieren als **OVF/OVA** oder einfach die **.vmdk-Dateien sichern**

#### **2. Auf Proxmox vorbereiten:**
- Proxmox-Host mit ausreichend Speicherplatz
- ggf. passende VM-Konfiguration vorbereiten

#### **3. Konvertieren des VMDK zu QCOW2 oder RAW:**
```bash
# Beispiel mit qemu-img
qemu-img convert -f vmdk -O qcow2 vm-disk.vmdk vm-disk.qcow2
```

#### **4. Disk auf Proxmox übertragen:**
- Per SCP, SFTP oder USB-Stick auf den Server in ein Storage-Verzeichnis (z. B. `/var/lib/vz/images/VMID/`)

#### **5. Neue VM in Proxmox erstellen:**
- Leere VM anlegen mit passender Hardware (z. B. BIOS/UEFI, CPU, RAM)
- Originale Disk durch importierte ersetzen oder einhängen:
```bash
qm importdisk <VMID> vm-disk.qcow2 <storage>
```

#### **6. VM-Konfiguration anpassen:**
- Boot-Reihenfolge
- Netzwerk neu konfigurieren (Treiber ggf. auf virtio setzen)
- Optional: VMware Tools entfernen und qemu-guest-agent installieren

#### **7. Starten und testen**

---

### **Migrieren Sie Ihre VMs, die Sie auf Ihrer ESXi Umgebung erstellt haben.**

➡️ **Manuell durchzuführen**, wie oben beschrieben.

💡 Wenn du möchtest, kann ich dir ein automatisiertes Skript oder eine Checkliste für die Migration geben.

---

### **Testen Sie, ob Ihre VMs unter Proxmox fehlerfrei gestartet werden können.**

**Nach dem Start in Proxmox prüfen:**
- Bootet das Betriebssystem?
- Funktioniert das Netzwerk (ggf. IP neu vergeben)?
- Dienste laufen wie erwartet?
- Keine Fehlermeldungen im Bootprozess oder im Proxmox-Webinterface?

**Hilfsmittel:**
- **Proxmox-Konsole (noVNC)**
- **`dmesg`, `journalctl`, `ip a`, `ping` etc.** innerhalb der VM
