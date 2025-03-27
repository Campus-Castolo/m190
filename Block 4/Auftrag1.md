### **1. Not Attached (Nicht verbunden)**

**Erklärung:**  
- Die VM ist **mit keinem Netzwerk verbunden**  
- Wie ein PC ohne Netzwerkkabel  

**Einsatz:**  
- Für **isolierte Tests** ohne Internet oder Netzwerkzugriff  
- Zum Testen von Offline-Konfigurationen oder Sicherheitsverhalten  

---

### **2. NAT (Network Address Translation)**

**Erklärung:**  
- VM teilt sich die **IP-Adresse des Hosts**  
- Der Host leitet Anfragen aus der VM ins externe Netzwerk weiter  
- **VM kann ins Internet**, ist aber von außen **nicht erreichbar**

**Einsatz:**  
- Für VMs mit **Internet-Zugriff**, aber ohne direkte Kommunikation mit dem LAN  
- Sicherer, da VM vom Netzwerk isoliert ist  

---

### **3. Bridged Networking (Netzwerkbrücke)**

**Erklärung:**  
- VM wird wie ein **vollwertiges Gerät im LAN behandelt**  
- Erhält eigene IP-Adresse vom Router oder DHCP-Server  
- **Volle Kommunikation** mit anderen Geräten im Netzwerk möglich

**Einsatz:**  
- Für VMs, die **wie physische Rechner** im Netz funktionieren sollen  
- **Serverdienste**, die vom LAN aus erreichbar sein sollen  
- Netzwerktests mit echten Geräten  

---

### **4. Internal Networking (Internes Netzwerk)**

**Erklärung:**  
- Nur **VMs auf demselben Host** im selben internen Netzwerk können miteinander kommunizieren  
- Kein Zugriff auf Host oder Internet

**Einsatz:**  
- **Isolierte Netzwerke** für mehrere VMs (z. B. Test eines eigenen Netzwerks mit DHCP, DNS usw.)  
- **Netzwerksimulationen**, z. B. Client-Server-Tests  

---

### **5. Host-Only Networking**

**Erklärung:**  
- VM kann **nur mit dem Host kommunizieren**  
- Kein Internetzugriff, kein Zugriff auf das restliche LAN  
- Getrenntes virtuelles Netzwerk zwischen Host ↔ VM  

**Einsatz:**  
- Wenn VM und Host Daten austauschen sollen, aber kein Internetzugang nötig ist  
- Für Entwickler- und Testumgebungen mit eingeschränktem Zugriff  

---

### **Zusammenfassung als Tabelle:**

| **Modus**             | **Zugriff auf Internet** | **Zugriff auf Host** | **Zugriff auf LAN** | **Isoliert** | **Typischer Einsatz**                         |
|------------------------|---------------------------|------------------------|------------------------|----------------|-----------------------------------------------|
| Not Attached           | ❌                        | ❌                     | ❌                     | ✅             | Sicherheits- und Offline-Tests                 |
| NAT                    | ✅                        | Eingeschränkt          | ❌                     | Teilweise      | Internet für VM, keine LAN-Verbindung         |
| Bridged                | ✅                        | ✅                     | ✅                     | ❌             | Volle Integration ins Netzwerk                |
| Internal Networking    | ❌                        | ❌                     | ❌                     | ✅             | Simuliertes privates Netzwerk unter VMs       |
| Host-Only Networking   | ❌                        | ✅                     | ❌                     | Teilweise      | Austausch zwischen Host und VM, kein Internet |