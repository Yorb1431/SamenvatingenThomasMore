# **Network Protocols**

## **Wat is een netwerkprotocol?**
Een netwerkprotocol is een set regels die bepaalt hoe gegevens worden gecommuniceerd tussen apparaten binnen een netwerk. Het reguleert:
- **Wat** er wordt gecommuniceerd (inhoud van de data).
- **Hoe** het wordt gecommuniceerd (format en transportmechanisme).
- **Wanneer** het wordt gecommuniceerd (synchronisatie en timing).

Netwerkprotocollen zorgen ervoor dat apparaten met verschillende interne structuren, besturingssystemen en ontwerpen effectief kunnen communiceren. Dit geldt zowel voor lokale netwerken (LAN) als voor wereldwijde netwerken zoals het internet.

---

## **Hoe werken netwerkprotocollen?**
Netwerkprotocollen worden georganiseerd door modellen zoals het **OSI-model** en het **TCP/IP-model**. Deze modellen zorgen ervoor dat elk aspect van netwerkcommunicatie in lagen wordt verdeeld, zodat het proces modulair en begrijpelijk blijft.

### **Het OSI-model:**
Het OSI-model bestaat uit zeven lagen, waarbij elke laag een specifieke functie heeft:
1. **Fysieke laag:** Verantwoordelijk voor het verzenden van ruwe bits over een fysiek medium.
2. **Datalinklaag:** Verzorgt framing, foutcorrectie en MAC-adressering.
3. **Netwerklaag:** Regelt routing en adressering (bijv. IP).
4. **Transportlaag:** Zorgt voor betrouwbare gegevensoverdracht (bijv. TCP).
5. **Sessielaag:** Beheert sessies tussen toepassingen.
6. **Presentatielaag:** Regelt dataconversie en encryptie.
7. **Applicatielaag:** Geeft toepassingen toegang tot netwerkdiensten (bijv. HTTP).

### **Het TCP/IP-model:**
Dit model, gericht op internetcommunicatie, heeft vier of vijf lagen:
1. **Netwerktoegang:** Verantwoordelijk voor fysieke en datalinkfuncties.
2. **Netwerklaag:** Zorgt voor IP-routing.
3. **Transportlaag:** Biedt protocollen zoals TCP en UDP.
4. **Applicatielaag:** Verzorgt toepassingen zoals HTTP, SMTP, en FTP.

---

## **Soorten netwerkprotocollen**
Netwerkprotocollen kunnen worden ingedeeld op basis van hun primaire functies:

### **1. Communicatieprotocollen**
Deze protocollen regelen gegevensoverdracht tussen apparaten. Ze zorgen ervoor dat berichten correct worden verzonden, ontvangen en opnieuw geassembleerd.

#### **Belangrijke protocollen:**
- **TCP/IP (Transmission Control Protocol / Internet Protocol):**
  - Splits gegevens op in pakketten.
  - Controleert op fouten en verzendt pakketten opnieuw indien nodig.
  - **Voordeel:** Zeer betrouwbaar.
  - **Nadeel:** Kwetsbaar voor aanvallen zoals SYN floods.
- **UDP (User Datagram Protocol):**
  - Sneller dan TCP, zonder foutcontrole.
  - Geschikt voor tijdgevoelige toepassingen zoals streaming.
  - **Nadeel:** Geen garantie dat gegevens correct aankomen.
- **FTP (File Transfer Protocol):**
  - Wordt gebruikt voor bestandsoverdracht tussen client en server.
  - **FTPS (Secure FTP):** Beveiligde versie met encryptie.
- **SIP (Session Initiation Protocol):**
  - Beheert multimedia zoals VoIP en videoconferenties.

### **2. Netwerkbeveiligingsprotocollen**
Deze protocollen beveiligen gegevensoverdracht tegen bedreigingen zoals afluisteren, manipulatie en ongeautoriseerde toegang.

#### **Belangrijke protocollen:**
- **SSH (Secure Shell):**
  - Biedt beveiligde toegang tot apparaten zoals servers.
  - Beschermt inloggegevens en sessies met encryptie.
- **SSL/TLS (Secure Sockets Layer / Transport Layer Security):**
  - Versleutelt webverkeer, zoals HTTPS.
  - Beschermt tegen afluisteren en manipulatie.
- **IPsec (Internet Protocol Security):**
  - Biedt encryptie en authenticatie op netwerklaag.
  - Wordt vaak gebruikt in VPN's.

### **3. Netwerkbeheerprotocollen**
Deze protocollen helpen bij het monitoren, beheren en configureren van netwerkapparaten.

#### **Belangrijke protocollen:**
- **SNMP (Simple Network Management Protocol):**
  - Monitoren van apparaatstatus, prestaties en fouten.
  - **SNMPv3:** Veiliger door encryptie.
- **ICMP (Internet Control Message Protocol):**
  - Voor diagnostiek zoals “ping”.
  - **Risico:** Kan worden misbruikt voor DDoS-aanvallen.
- **DNS (Domain Name System):**
  - Vertaalt domeinnamen naar IP-adressen.
  - **Risico:** DNS-spoofing kan verkeer omleiden.
- **DHCP (Dynamic Host Configuration Protocol):**
  - Automatiseert het toewijzen van IP-adressen.
  - **Risico:** Kwaadaardige DHCP-servers kunnen verstoring veroorzaken.
- **NetFlow en sFlow:**
  - Monitoren verkeersstromen binnen het netwerk.

---

## **Gedetailleerde uitleg van protocollen**

### **E-mailprotocollen**
- **SMTP (Simple Mail Transfer Protocol):**
  - Zorgt voor het verzenden van e-mails.
- **POP3 (Post Office Protocol 3):**
  - Downloadt e-mails van een server naar een apparaat.
- **IMAP (Internet Message Access Protocol):**
  - Laat e-mails op de server staan voor meerdere apparaten.

### **Bestandsbeheerprotocollen**
- **FTP (File Transfer Protocol):**
  - Voor bestandsoverdrachten. Onbeveiligd zonder encryptie.
- **FTPS (Secure FTP):**
  - Verbetert FTP met encryptie via SSL/TLS.

### **Diagnostische protocollen**
- **ICMP (Internet Control Message Protocol):**
  - Helpt bij netwerkdiagnostiek en foutopsporing.
  - **Ping:** Test connectiviteit en vertraging.
- **ARP (Address Resolution Protocol):**
  - Verbindt IP-adressen met MAC-adressen.

---

## **Belangrijke poorten**
- **HTTP:** Poort 80.
- **HTTPS:** Poort 443.
- **FTP:** Poorten 20 en 21.
- **SMTP:** Poort 25.
- **DNS:** Poort 53.
- **DHCP:** Poorten 67 en 68.

---

## **Best practices voor netwerkprotocollen**
1. **Regelmatige updates:**
   - Zorg dat software up-to-date is om kwetsbaarheden te voorkomen.
2. **Encryptie gebruiken:**
   - Bescherm gegevens met protocollen zoals TLS/SSL.
3. **Sterke authenticatie:**
   - Gebruik MFA (Multi-Factor Authentication).
4. **Monitoring en logging:**
   - Gebruik SNMP en NetFlow om netwerkactiviteiten te volgen.
5. **Alternatieven voor verouderde protocollen:**
   - Vervang Telnet door SSH voor betere beveiliging.

---

## **Samenvatting**
Netwerkprotocollen zijn cruciaal voor de communicatie, beveiliging en het beheer van netwerken. Ze zorgen ervoor dat apparaten efficiënt en veilig met elkaar kunnen communiceren. Door best practices te volgen en protocollen zoals TCP/IP, SSH, en SNMP te gebruiken, kan een netwerk betrouwbaar blijven functioneren.
