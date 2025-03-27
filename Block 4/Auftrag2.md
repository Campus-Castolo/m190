### **Was ist ein vSwitch?**

- **Virtueller Switch**, der Netzwerkverbindungen innerhalb eines Hypervisors bereitstellt  
- Funktioniert wie ein physischer Switch, aber **softwarebasiert**  
- Verbindet:
  - **Virtuelle Maschinen (VMs)**
  - **VMkernel-Adapter**
  - **Physische Netzwerkkarten (NICs)**  
- Leitet Netzwerkverkehr zwischen VMs oder zwischen VM und physischem Netzwerk  

---

### **Welche Eigenschaften hat vSwitch0?**

- Standardmäßig bei **ESXi automatisch vorhanden**  
- Beinhaltet meist:
  - Einen **VMkernel-Port** (z. B. für Management, vMotion, etc.)
  - Einen **Standard-Portgroup** (z. B. "VM Network")
  - Eine **physische NIC (vmnicX)**  
- Kann VLANs unterstützen  
- Konfigurierbar bzgl. Sicherheit, Load Balancing, Failover etc.

---

### **Wie können Sie weitere vSwitches erstellen?**

- Über die **vSphere Weboberfläche (vCenter oder direkt am Host)**  
- Menü:  
  `Netzwerk` → `vSwitches` → `Neuen vSwitch hinzufügen`  
- Alternativ über **CLI (esxcli)** oder **PowerCLI**

---

### **Wie können Sie einen vSwitch mit einem physischen Switch verbinden?**

- Durch **Zuordnung einer physischen Netzwerkkarte (vmnic)** zum vSwitch  
- Diese vmnic verbindet den vSwitch mit dem **physischen LAN**  
- Verbindung erfolgt über **Patchkabel** zum realen Switch-Port  
- Wichtig: Switch-Port muss korrekt konfiguriert sein (Access oder Trunk)

---

### **Was ist ein VLAN?**

- **Virtuelles LAN**, das Netzwerke logisch trennt – auch wenn Geräte physisch im selben Netzwerk sind  
- Identifiziert durch eine **VLAN-ID (z. B. 10, 20, 30...)**  
- **Segmentierung** und **Sicherheit** im Netzwerk  
- Wird in der Netzwerkhardware und Software (vSwitch) konfiguriert  

---

### **Was versteht man unter Trunk?**

- **Trunk-Ports** übertragen **mehrere VLANs gleichzeitig** über eine einzige Leitung  
- VLANs werden über **Tags (802.1Q)** unterschieden  
- Wird z. B. verwendet zwischen:
  - **Switch ↔ Switch**
  - **Switch ↔ ESXi-Host (vSwitch)**  
- Gegenspieler zu **Access-Ports** (nur ein VLAN)

---

### **Wie können Sie einen vSwitch mit einem VLAN verbinden?**

- **In der Portgruppe** (nicht direkt im vSwitch selbst) wird die VLAN-ID angegeben  
- Schritte (vSphere Weboberfläche):  
  - Netzwerk → Portgruppen → Neue Portgruppe erstellen  
  - vSwitch auswählen  
  - VLAN-ID eintragen  
  - VMs dieser Portgruppe zuweisen  
- Trunk-Port am physischen Switch erforderlich, wenn mehrere VLANs genutzt werden sollen  