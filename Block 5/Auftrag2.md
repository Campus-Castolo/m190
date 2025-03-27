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

---

Alles klar. Ich recherchiere die aktuellen Lizenzkosten für 2025 in der Schweiz für die folgenden Microsoft-Produkte:

- Windows Server (56 Cores, 28x 2er-Pakete, Datacenter Edition empfohlen)
- 25x Windows User CALs
- 25x Exchange User CALs
- 25x SQL User CALs oder Core-basierte Lizenzierung (je nach Szenario)
- 3x M365 E3/E5 oder 3x VDA User-Lizenzen für virtuelle Desktops

Ich prüfe dabei bevorzugt offizielle und vertrauenswürdige Schweizer Quellen (z. B. Microsoft Schweiz, große IT-Reseller wie Bechtle, Also, SoftwareONE etc.). Ich melde mich, sobald ich dir die vollständige Preisliste und Infos zusammengetragen habe.

**Lizenzkosten 2025 (Schweiz, CHF) – Übersicht** 

Die folgende Tabelle zeigt die aktuellen geschätzten Preise in Schweizer Franken (exkl. MwSt) für die gewünschten Microsoft-Lizenzen, inklusive Angabe des Lizenztyps und ob es sich um Kauf- oder Mietlizenzen handelt. Alle Angaben beziehen sich auf die Schweiz (CHF) und basieren auf verfügbaren Preisen von Microsoft-Partnern (z.B. Bechtle, Lizenzhändler) im Jahr 2025.

| **Lizenz / Edition**                                     | **Einzelpreis**           | **Menge**                   | **Gesamtpreis (ca.)**    | **Lizenzmodell / Hinweise**                     |
|----------------------------------------------------------|---------------------------|-----------------------------|--------------------------|-------------------------------------------------|
| **Windows Server 2022 Datacenter** (56 Kerne = 28× 2-Core-Packs) | ~ CHF 495 pro 2-Core-Pack ([Buy HPE MS WinServer 2022 DC Add Licence (P46214-B21)](https://www.bechtle.com/ch-en/shop/hpe-ms-winserver-2022-dc-add-licence--4588170--p#:~:text=494)) | 28 × 2-Core-Packs         | ~ CHF 13’860 gesamt      | **Kauflizenz (perpetual).** Preis z.B. als OEM/ROK-Add-On ~495 CHF pro 2 Kerne ([Buy HPE MS WinServer 2022 DC Add Licence (P46214-B21)](https://www.bechtle.com/ch-en/shop/hpe-ms-winserver-2022-dc-add-licence--4588170--p#:~:text=494)) ([Buy HPE MS WinServer 2022 DC Add Licence (P46214-B21)](https://www.bechtle.com/ch-en/shop/hpe-ms-winserver-2022-dc-add-licence--4588170--p#:~:text=Microsoft%20Windows%20Server%202022%20Data,delivery%20For%20HPE%20servers%20only)). Datacenter-Edition erlaubt unbegrenzte VMs (hohe Virtualisierungsdichte). |
| **Windows Server 2022 User CAL** (Client Access License) | CHF 45.99 pro User ([Buy Microsoft Windows Server 2022 1 Client User CAL 1Pack (R18-06450)](https://www.bechtle.com/ch-en/shop/microsoft-windows-server-2022-1-client-user-cal-1pack--107394090--p#:~:text=45)) | 25 User                  | ~ CHF 1’150 gesamt       | **Kauflizenz (perpetual).** Preis pro Benutzer-CAL ca. 46 CHF ([Buy Microsoft Windows Server 2022 1 Client User CAL 1Pack (R18-06450)](https://www.bechtle.com/ch-en/shop/microsoft-windows-server-2022-1-client-user-cal-1pack--107394090--p#:~:text=45)). Erforderlich für Zugriff der Nutzer auf Windows Server (Editionunabhängig). |
| **Exchange Server 2019 Standard User CAL**              | CHF 75.00 pro User ([Exchange Server CAL | Zugriffslizenzen/CALs | Server & CAL | Lizenzguru](https://lizenzguru.ch/server-cal/zugriffslizenzencals/exchange-server-cal/#:~:text=Image%20%20Microsoft%20Exchange%20Server,2019%20Standard%201%20User%20CAL)) | 25 User                  | ~ CHF 1’875 gesamt       | **Kauflizenz (perpetual).** Preis pro Exchange CAL ca. 75 CHF ([Exchange Server CAL | Zugriffslizenzen/CALs | Server & CAL | Lizenzguru](https://lizenzguru.ch/server-cal/zugriffslizenzencals/exchange-server-cal/#:~:text=Image%20%20Microsoft%20Exchange%20Server,2019%20Standard%201%20User%20CAL)). Erlaubt einem Benutzer den Zugriff auf einen Exchange-Server (Standard Edition). |
| **SQL Server 2022 Standard** – *Server/CAL-Modell*      | CHF 749.95 Serverlizenz ([Wie Sie für den SQL Server 2022 günstig Lizenzen kaufen können | Lizenzguru](https://lizenzguru.ch/server-cal/microsoft-sql-server/sql-server-2022/#:~:text=Image%20%20SQL%20Server%202022,Standard))<br>CHF 189.99 pro User-CAL ([SQL Server 2022 Standard - 1 User CAL - Lizenzguru](https://lizenzguru.ch/sql-server-2022-standard-1-user-cal.html#:~:text=SQL%20Server%202022%20Standard%20,8%2C%209%2C%2010%2C%2011)) | 1 Server<br>25 User-CALs | ~ CHF 5’500 gesamt       | **Kauflizenz (perpetual).** Serverlizenz ~750 CHF ([Wie Sie für den SQL Server 2022 günstig Lizenzen kaufen können | Lizenzguru](https://lizenzguru.ch/server-cal/microsoft-sql-server/sql-server-2022/#:~:text=Image%20%20SQL%20Server%202022,Standard)) plus ~190 CHF pro Benutzer-CAL ([SQL Server 2022 Standard - 1 User CAL - Lizenzguru](https://lizenzguru.ch/sql-server-2022-standard-1-user-cal.html#:~:text=SQL%20Server%202022%20Standard%20,8%2C%209%2C%2010%2C%2011)). Geeignet bei begrenzter Nutzerzahl (z.B. 25 User). |
| **SQL Server 2022 Standard** – *Core-basiert*          | CHF 2’699.95 pro 2-Core-Pack ([Wie Sie für den SQL Server 2022 günstig Lizenzen kaufen können | Lizenzguru](https://lizenzguru.ch/server-cal/microsoft-sql-server/sql-server-2022/#:~:text=Image%20%20SQL%20Server%202022,Standard%202%20Core)) | *n.V.* (z.B. 2 Packs für 4 Kerne) | z.B. ~ CHF 5’400 (4 Kerne) | **Kauflizenz (perpetual).** Alternativ Core-Lizenzierung ohne CALs: ca. 2’700 CHF pro 2 Kerne ([Wie Sie für den SQL Server 2022 günstig Lizenzen kaufen können | Lizenzguru](https://lizenzguru.ch/server-cal/microsoft-sql-server/sql-server-2022/#:~:text=Image%20%20SQL%20Server%202022,Standard%202%20Core)). Bsp.: 4 Kerne ~5’400 CHF. Lohnt sich v.a. bei vielen Usern oder >25 User CALs. |
| **Microsoft 365 E3 (Enterprise)** – inkl. Windows, Office, EMS | CHF 35.60 **pro User/Monat** ([Microsoft 365 Enterprise-Pläne vergleichen | Microsoft 365](https://www.microsoft.com/de-ch/microsoft-365/enterprise/microsoft365-plans-and-pricing#:~:text=Microsoft%20365%20E3%20EWR%20,Teams)) | 3 User (jährl. Zahlung)  | ~ CHF 1’280 pro Jahr     | **Mietlizenz (CSP Abo).** Cloud-Subscription, jährliche Abrechnung. Preis ~35.60 CHF pro Benutzer/Monat ([Microsoft 365 Enterprise-Pläne vergleichen | Microsoft 365](https://www.microsoft.com/de-ch/microsoft-365/enterprise/microsoft365-plans-and-pricing#:~:text=Microsoft%20365%20E3%20EWR%20,Teams)). Beinhaltet Windows 10/11 Enterprise, Office-Apps, EMS. |
| **Microsoft 365 E5 (Enterprise)** – inkl. erweiterte Features | CHF 55.20 **pro User/Monat** ([Microsoft 365 Enterprise-Pläne vergleichen | Microsoft 365](https://www.microsoft.com/de-ch/microsoft-365/enterprise/microsoft365-plans-and-pricing#:~:text=Microsoft%20365%20E5%20EWR%20,Teams))  | 3 User (jährl. Zahlung)  | ~ CHF 1’987 pro Jahr     | **Mietlizenz (CSP Abo).** Umfangreichstes Paket mit Security/Voice-Features. Preis ~55.20 CHF pro Benutzer/Monat ([Microsoft 365 Enterprise-Pläne vergleichen | Microsoft 365](https://www.microsoft.com/de-ch/microsoft-365/enterprise/microsoft365-plans-and-pricing#:~:text=Microsoft%20365%20E5%20EWR%20,Teams)). Ebenfalls Windows Enterprise + O365 + EMS enthalten. |
| **Windows 10/11 VDA** (Virtual Desktop Access) – **nur Windows** | ca. CHF 11 **pro User/Monat** ([Lizenz-Falle Desktop-Virtualisierung: VDA Lizenzen benötigt!](https://www.loginventory.de/blog/lizenz-falle-desktop-virtualisierung/#:~:text=%2A%20VDA,700%20Euro)) | 3 User                   | ~ CHF 396 pro Jahr       | **Mietlizenz (Abo).** Nur Zugriffsrecht auf virtuellen Windows-Desktop (ohne Office). Preis ~11 € (~11 CHF) pro Gerät/User/Monat ([Lizenz-Falle Desktop-Virtualisierung: VDA Lizenzen benötigt!](https://www.loginventory.de/blog/lizenz-falle-desktop-virtualisierung/#:~:text=%2A%20VDA,700%20Euro)). Alternative zu M365, falls nur VDI-Zugriff benötigt. |

**Hinweise:** Die Windows Server und SQL Server Lizenzen sind in der Regel perpetual (unbefristete Kauflizenzen, z.B. über Volumenlizenz oder OEM). Preise können je nach Bezugsweg variieren (z.B. OEM/ROK bei Server-Hardware oft günstiger ([Buy HPE MS WinServer 2022 DC Add Licence (P46214-B21)](https://www.bechtle.com/ch-en/shop/hpe-ms-winserver-2022-dc-add-licence--4588170--p#:~:text=494))). Die Microsoft 365 und VDA-Lizenzen sind abonnementbasiert (CSP/Mietmodell) mit monatlicher oder jährlicher Abrechnung. Alle angegebenen Preise sind **ca.-Werte exkl. MwSt** und stammen aus Schweizer Quellen (z.B. Bechtle, Software-Reseller) im Jahr 2025 ([Buy HPE MS WinServer 2022 DC Add Licence (P46214-B21)](https://www.bechtle.com/ch-en/shop/hpe-ms-winserver-2022-dc-add-licence--4588170--p#:~:text=494)) ([Microsoft 365 Enterprise-Pläne vergleichen | Microsoft 365](https://www.microsoft.com/de-ch/microsoft-365/enterprise/microsoft365-plans-and-pricing#:~:text=Microsoft%20365%20E3%20EWR%20,Teams)). Bitte beachten, dass tatsächliche Konditionen je nach Anbieter und Lizenzprogramm leicht abweichen können.

