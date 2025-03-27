### **Welche Hauptversionen von Windows Server gibt es?**

- **Windows Server Standard**  
  - Für physische oder minimal virtualisierte Umgebungen  
  - Lizenz deckt **2 VOSEs** bei vollständiger Core-Lizenzierung

- **Windows Server Datacenter**  
  - Für **hochgradig virtualisierte** Umgebungen (z. B. Rechenzentren)  
  - **Unbegrenzte VOSEs** erlaubt

- **Windows Server Essentials**  
  - Für **kleine Unternehmen** mit bis zu 25 Benutzern / 50 Geräten  
  - Keine CALs erforderlich

- **Windows Server Azure Edition**  
  - Nur in **Azure Cloud** verfügbar  
  - Für Cloud-native Szenarien optimiert  

---

### **Was versteht Microsoft unter OSE, POSE und VOSE?**

- **OSE (Operating System Environment):**  
  - Allgemeiner Begriff für ein Betriebssystem-Umfeld – physisch oder virtuell  
- **POSE (Physical OSE):**  
  - Das physische Betriebssystem auf dem **echten Server (Host)**  
- **VOSE (Virtual OSE):**  
  - Eine **virtuelle Instanz** eines Betriebssystems (z. B. eine VM)

---

### **Wie werden Windows Server lizenziert?**

- **Pro physischem Server auf Basis von CPU-Kernen**  
  - Mindestlizenzierung: **16 Kerne pro Server**  
  - Mindestens **8 Kerne pro Prozessor**  
- Lizenzierung unterscheidet sich je nach Edition:
  - **Standard**: 2 VOSEs pro 16-Core-Lizenz  
  - **Datacenter**: unbegrenzte VOSEs bei vollständiger Core-Lizenzierung  
- Zusätzlich erforderlich: **CALs (Client Access Licenses)** für Benutzer oder Geräte

---

### **Wozu wird eine CAL benötigt?**

- **CAL = Client Access License**  
- Berechtigt einen **Benutzer oder ein Gerät**, auf Windows Server-Dienste zuzugreifen  
- Zwei Typen:  
  - **User CAL** – für **einen Benutzer**, egal mit welchem Gerät  
  - **Device CAL** – für **ein Gerät**, egal wie viele Benutzer  
- Wird **zusätzlich zur Server-Lizenz** benötigt  
- Ohne CAL kein legaler Zugriff auf Serverdienste wie Dateifreigaben, AD, etc.

---

### **Welchen Lizenztyp benötigen Sie für einen virtuellen Windows 11 Desktop?**

- **Windows 11 Enterprise** mit **Microsoft 365** Lizenz (z. B. E3/E5)  
  - Enthält **VDA-Rechte** (Virtual Desktop Access)  
- Alternativ:  
  - **Windows VDA Lizenz** (separat), wenn kein M365 vorhanden  
- Einsatz z. B. für **Windows Virtual Desktop / AVD (Azure Virtual Desktop)**  
- Wichtig bei VDI (Virtual Desktop Infrastructure):  
  - **Geeignete VDA- oder M365-Lizenz erforderlich**  
  - CALs gelten hier **nicht für Desktopbetriebssysteme**!