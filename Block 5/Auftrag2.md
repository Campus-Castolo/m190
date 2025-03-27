## **1. Wie viele Cores müssen Sie für die virtuellen Server lizenzieren?**

### **Gegeben:**
- 2x CPU mit je **28 Cores** → **insgesamt 56 Cores**
- Microsoft verlangt:
  - **mindestens 8 Cores pro CPU**
  - **mindestens 16 Cores pro Server**
  - Lizenziert wird **immer in 2er-Core-Paketen**

### **Antwort:**
👉 **56 Cores** müssen lizenziert werden  
👉 **28 x 2er-Core-Pakete**

---

## **2. Welche Serverversion würden Sie lizenzieren?**

### **Optionen:**
- **Windows Server Standard**
- **Windows Server Datacenter**

### **Empfehlung:**
- **➡️ Windows Server Datacenter**, da:
  - **viele virtuelle Server** benötigt werden (mind. 7 Serverrollen)
  - ggf. zusätzliche VMs für Test, Management, Backup, Monitoring usw.
  - Datacenter erlaubt **unbegrenzte VOSEs**

### **Alternativ:**
- **Windows Server Standard**:
  - Lizenz deckt nur **2 VOSEs pro 16 lizenzierten Cores**
  - Bei 56 Cores = **7 VOSEs**
  - Nur geeignet, wenn wirklich **max. 7 VMs betrieben werden** und keine Skalierung geplant ist

---

## **3. Welche und wie viele CALs benötigen Sie?**

### **Gegeben:**
- 25 Mitarbeitende → alle benötigen Zugriff auf AD, Datei-, Print-, Exchange- und SQL-Server

### **CAL-Typen:**
- **User CALs** (empfohlen bei 1 Benutzer mit mehreren Geräten)
- Alternativ: **Device CALs**

### **Benötigt:**
- **25 Windows Server User CALs**  
- **25 Exchange CALs** (für Zugriff auf den Exchange-Server)  
- **25 SQL CALs** oder alternativ **SQL Server mit Core-Lizenzierung** (abhängig von Zugriffsmuster)

💡 Wenn SQL z. B. von Anwendungen oder externen Geräten angesprochen wird → besser **pro Core** lizenzieren.

---

## **4. Wie müssen die virtuellen Desktops lizenziert werden?**

### **Gegeben:**
- 3 Außendienstmitarbeitende sollen auf virtuelle Windows 11 Desktops zugreifen

### **Lösungsmöglichkeiten:**

#### **a) Microsoft 365 E3 oder E5**
- Beinhaltet:
  - **Windows 11 Enterprise**
  - **Virtual Desktop Access (VDA) Rechte**
  - Office, Intune, AzureAD uvm.
- **Empfohlen für Unternehmen mit M365-Infrastruktur**

#### **b) Separate VDA-Lizenz**
- Falls **kein M365 verwendet wird**
- Pro Benutzer, der auf den virtuellen Desktop zugreift

### **Benötigt:**
👉 **3x M365 E3/E5 Lizenzen** **oder** **3x VDA User-Lizenzen**

---

## **Zusammenfassung in Stichpunkten:**

| Kategorie                        | Lizenzbedarf                                      |
|----------------------------------|---------------------------------------------------|
| **Windows Server Cores**         | 56 Cores (28 x 2er-Pakete)                        |
| **Empfohlene Edition**           | **Datacenter** (wegen hoher Virtualisierungsdichte) |
| **Windows CALs**                 | 25x **User CALs**                                 |
| **Exchange CALs**                | 25x **Exchange User CALs**                        |
| **SQL-Lizenzierung**             | 25x **SQL User CALs** oder Core-basiert (je nach Einsatz) |
| **Virtuelle Desktops**           | 3x **M365 E3/E5** oder **3x VDA User-Lizenz**     |
