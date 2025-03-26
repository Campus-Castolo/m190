### **Zu welcher Virtualisierungslösung gehören folgende Disk-Image-Dateien?**

| **Dateiendung** | **Virtualisierungslösung** |
|------------------|-----------------------------|
| **.vhdx**        | Microsoft Hyper-V           |
| **.vdi**         | Oracle VirtualBox           |
| **.vmdk**        | VMware (z. B. ESXi, Workstation, Fusion) |
| **.qcow2**       | QEMU / KVM (Linux-basierte Virtualisierung) |

---

### **Wie kann man ein virtuelles Disk Image von einem Format in ein anderes konvertieren?**

#### ✅ **Mit dem Tool `qemu-img` (plattformübergreifend, sehr flexibel):**

**Syntax:**
```bash
qemu-img convert -f [Quellformat] -O [Zielformat] [quelle.img] [ziel.img]
```

**Beispiele:**

- **Von VDI nach QCOW2:**
```bash
qemu-img convert -f vdi -O qcow2 disk.vdi disk.qcow2
```

- **Von VMDK nach VHDX:**
```bash
qemu-img convert -f vmdk -O vhdx disk.vmdk disk.vhdx
```

- **Von QCOW2 nach RAW:**
```bash
qemu-img convert -f qcow2 -O raw disk.qcow2 disk.img
```

---

📌 **Hinweise:**
- Vorher ein Backup machen – Konvertierung kann fehlschlagen.
- Manche Formate unterstützen Snapshots, Kompression o. ä. – diese Eigenschaften können beim Konvertieren verloren gehen.
- Unter Windows lässt sich `qemu-img` z. B. mit **qemu for Windows** oder **WSL** nutzen.
