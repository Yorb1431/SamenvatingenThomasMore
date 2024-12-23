# **Command-line Interfaces (CLI)**

## **Wat is een Command-line Interface (CLI)?**
Een CLI is een manier om te communiceren met een computerprogramma door tekstcommando’s in te voeren. Het werd ontwikkeld in de jaren 60 als alternatief voor het werken met ponskaarten.

### **Kenmerken van een CLI:**
1. **Directe tekstinteractie:** Gebruikers voeren tekstcommando’s in via een terminal of console.
2. **Breed toepasbaar:** Wordt gebruikt voor zowel besturingssystemen als specifieke applicaties.
3. **Automatisering:** CLI’s zijn ideaal voor scripting, omdat commandolijnen eenvoudig in code kunnen worden gespecificeerd.

---

## **Belangrijke aspecten van een CLI**
1. **Command-line Interpreter:**  
   Een programma dat tekstcommando's leest en uitvoert, zoals Bash, Command Prompt of PowerShell.
2. **Parameters en Argumenten:**  
   CLI’s ondersteunen parameters om extra informatie door te geven bij het uitvoeren van een programma.
3. **Interactiviteit:**  
   Sommige CLI’s ondersteunen interactieve sessies waarin gebruikers meerdere opdrachten kunnen uitvoeren zonder de toepassing opnieuw te starten.
4. **Interprocess Communication (IPC):**  
   Gebruikers kunnen commandolijnen van andere processen omleiden naar een CLI-programma via standaardstreams of named pipes.

---

## **Soorten CLI’s**
1. **OS Command-line Interfaces:**  
   Worden geleverd door het besturingssysteem. Voorbeelden zijn Bash (Linux), PowerShell (Windows) en Zsh (macOS).
2. **Applicatie CLI’s:**  
   Specifieke programma’s met een eigen CLI voor configuratie en gebruik. Voorbeelden zijn Git CLI en de Python-interpreter.

---

## **CLI in Netwerk Operating Systems (NOS)**
Netwerkapparaten zoals routers en switches gebruiken vaak een CLI als primaire interface voor configuratie en beheer.

### **Voorbeelden van NOS CLI’s:**
- Cisco IOS XE
- Meraki CLI
- Ruckus CLI

### **Belangrijkste functies van een NOS CLI:**
1. **Configuratie:** Beheren van instellingen zoals interfaces, routes en firewalls.
2. **Monitoring:** Controleren van netwerkprestaties en logbestanden.
3. **Probleemoplossing:** Uitvoeren van diagnostische opdrachten zoals `ping` en `traceroute`.
4. **Remote Access:** Beheer via SSH of andere externe toegangsmethoden.

---

## **CLI-taken en functies in Cisco IOS XE**

### **1. Context-Sensitive Help:**
Gebruik `?` om beschikbare commando’s en syntaxopties te bekijken.
- Voorbeeld:
  ```
  Router# show ?
  Router# show ip ?
  ```

### **2. Command History:**
Navigeer snel door eerder ingevoerde commando’s:
- **Pijltjestoetsen:** Om door eerdere opdrachten te bladeren.
- **Ctrl + P:** Snel toegang tot het vorige commando.

### **3. Editing Shortcuts:**
- **Cursor bewegen:**  
  - Links/Rechts: `Ctrl + B` / `Ctrl + F`.  
  - Woorden overslaan: `Esc + B` / `Esc + F`.  
- **Begin/Einde van lijn:**  
  - `Ctrl + A` (begin), `Ctrl + E` (einde).

### **4. Filtering van Output:**
Filter uitvoer van commando’s om relevante informatie te vinden.
- Voorbeeld:
  ```
  Router# show running-config | include interface
  ```

### **5. Verwijderen van Tekst:**
- **Delete:** Verwijdert het vorige teken.
- **Ctrl + K:** Verwijdert van de cursor tot het einde van de lijn.
- **Ctrl + U:** Verwijdert van de cursor tot het begin van de lijn.
- **Ctrl + W:** Verwijdert het woord links van de cursor.

---

## **Praktische Voorbeelden van CLI-gebruik**

### **Netwerkconfiguratie:**
```bash
Router(config)# interface GigabitEthernet0/1
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown
```

### **Foutopsporing:**
```bash
Router# show ip route
Router# ping 192.168.1.1
```

### **Filtering van Output:**
```bash
Router# show running-config | include interface
```

---

## **Voordelen van een CLI**
1. **Efficiëntie:** Directe toegang tot functies zonder de GUI te openen.
2. **Automatisering:** Ideaal voor scripting en herhaalbare taken.
3. **Flexibiliteit:** Compatibel met meerdere besturingssystemen en applicaties.

---

## **Nadelen van een CLI**
1. **Steile leercurve:** Vereist kennis van commando’s en syntax.
2. **Fouten:** Typfouten kunnen leiden tot onverwachte resultaten.
3. **Geen GUI:** Minder toegankelijk voor visueel ingestelde gebruikers.

---

## **Samenvatting**
Een command-line interface is een krachtig hulpmiddel voor het beheren van systemen en netwerken. Het biedt flexibiliteit, efficiëntie en automatiseringsmogelijkheden, maar vereist een goed begrip van commando’s en syntax. Het gebruik van CLI’s, vooral in netwerkbeheertools zoals Cisco IOS XE, is essentieel voor IT-professionals die verantwoordelijk zijn voor complexe netwerkinfrastructuren.
