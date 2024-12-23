# Examen Januarie Computer Networking
# Network Models and Devices

## **Netwerkmodellen**

Netwerkmodellen beschrijven hoe gegevens worden uitgewisseld tussen apparaten in een netwerk. Ze maken gebruik van gelaagde structuren waarin elke laag specifieke functies heeft. Deze lagen bieden abstractie en modulariteit, zodat hogere lagen zich niet hoeven bezig te houden met hoe gegevens worden doorgestuurd.

### **Belangrijke modellen:**
1. **OSI/ISO 7-layer model**:
   - Ontwikkeld door de International Standards Organization (ISO).
   - Generiek model met zeven lagen:
     1. **Fysiek (Physical)**: Hardware, elektrische signalen, fysieke verbindingen.
     2. **Datakoppeling (Datalink)**: Foutdetectie, framing, MAC-adressen.
     3. **Netwerk (Network)**: Routering, adressering (bijvoorbeeld IP).
     4. **Transport**: End-to-end communicatie tussen applicaties, betrouwbaarheid.
     5. **Sessie (Session)**: Beheer van sessies en verbindingen.
     6. **Presentatie (Presentation)**: Vertaling van gegevens naar leesbare formaten.
     7. **Applicatie (Application)**: Toegang tot netwerkdiensten, zoals web of e-mail.

   - De lagen zijn genummerd van 1 (laagste) tot 7 (hoogste).

2. **TCP/IP 5-layer model**:
   - Simpeler en specifiek gericht op het internetprotocol.
   - Heeft vijf lagen: **Physical**, **Data Link**, **Network**, **Transport**, **Application**.

---

## **Netwerkapparatuur**

Netwerkapparatuur speelt een cruciale rol bij communicatie tussen apparaten. Hieronder een overzicht van de belangrijkste apparaten:

1. **Repeater**:
   - Werkt op de fysieke laag (laag 1).
   - Versterkt verzwakte signalen om bereik te vergroten.
   - Kopieert signalen bit voor bit.

2. **Hub**:
   - Een multi-poort repeater, werkt op laag 1.
   - Verstuurt data naar alle aangesloten apparaten zonder filtering.
   - Inefficiënt: creëert één grote collision domain.

3. **Bridge**:
   - Werkt op de datalinklaag (laag 2).
   - Filtert data door MAC-adressen te lezen.
   - Verbindt LAN's die hetzelfde protocol gebruiken.
   - Vermindert verkeer door gerichte transmissie.

4. **Switch**:
   - Een geavanceerde multi-poort bridge.
   - Werkt op laag 2.
   - Voert foutcontrole uit en stuurt alleen correcte data naar de juiste poort.
   - Verkleint collision domains maar behoudt hetzelfde broadcast domain.

   **Types switches:**
   - **Onbeheerd (Unmanaged)**: Eenvoudig, plug-and-play.
   - **Beheerd (Managed)**: Ondersteunt VLAN's, QoS en geavanceerd beheer.
   - **Smart switches**: Tussen onbeheerd en beheerd, eenvoudigere configuratie.
   - **Layer 2 switches**: Werken op de datalinklaag.
   - **Layer 3 switches**: Werken op de netwerklaag, ondersteunen routering.
   - **PoE switches**: Leveren stroom via ethernetkabels.
   - **Gigabit switches**: Ondersteunen hogere snelheden.
   - **Rack-mounted switches**: Geschikt voor serverracks in datacenters.
   - **Desktop switches**: Compact, voor kleine kantoren.
   - **Modulaire switches**: Uitbreidbaar voor grotere netwerken.

5. **Router**:
   - Werkt op de netwerklaag (laag 3).
   - Routeert data tussen verschillende netwerken (bijvoorbeeld LAN naar WAN).
   - Maakt gebruik van dynamische routingtabellen.
   - Verdeelt broadcast domains.

6. **Gateway**:
   - Verbindt netwerken met verschillende protocollen.
   - Werkt op meerdere lagen.
   - Fungeert als protocolconverter en vertaalt gegevens tussen systemen.

7. **Brouter (Bridging Router)**:
   - Combineert functies van bridge en router.
   - Werkt op laag 2 (bridging) en laag 3 (routering).

8. **NIC (Network Interface Card)**:
   - Een netwerkadapter die een computer verbindt met het netwerk.
   - Werkt op de fysieke en datalinklaag.
   - Bevat een unieke identificatie (MAC-adres).




### Voorbeelden lagen
- Fysieke laag(1) => Kabels
- Datalinklaag(2) => MAC
- Netwerklaag (3) => IP
- Transportlaag (4) => Pakketen
- Sessielaag (5) => Videocall
- Presentatielaag (6) => IMG
- Applicatielaag (7) => HTTP
---


# Hoofdstuk 2 - Internet Protocol Suite

## **TCP/IP-Modellen**

### **Originele 4-lagenmodel**
1. **Applicatielaag (Application):**
   - Verantwoordelijk voor netwerkdiensten direct voor eindgebruikers (bijv. HTTP, SMTP, FTP).
2. **Transportlaag (Transport):**
   - Zorgt voor betrouwbare dataoverdracht via TCP of minder betrouwbare overdracht via UDP.
3. **Internetlaag (Internet):**
   - Adressering en routering van datapakketten via IP.
4. **Netwerkinterface-laag (Link/Network Access):**
   - Regelt de fysieke transmissie van data via de netwerkinterface.

### **Bijgewerkt 5-lagenmodel**
1. **Applicatielaag (Application):**
   - Diensten voor eindgebruikers.
2. **Transportlaag (Transport):**
   - Betrouwbare overdracht (TCP, UDP).
3. **Netwerklaag (Network):**
   - Adressering en routering.
4. **Datalinklaag (Data Link):**
   - Foutdetectie en framing.
5. **Fysieke laag (Physical):**
   - Fysieke transmissie van data.

## **Voordelen van TCP/IP**
1. **Universele adoptie:** Wereldwijde standaard voor internetcommunicatie.
2. **Schaalbaarheid en flexibiliteit:** Geschikt voor nieuwe protocollen en technologieën.
3. **Interoperabiliteit:** Zorgt voor compatibiliteit tussen verschillende apparaten en systemen.
4. **Standaardisatie:** Biedt een uniform raamwerk voor protocollen.

---

## **IP-Adressen**

### **Wat is een IP-adres?**
- Uniek identificatienummer voor apparaten in een netwerk.
- Bestaat uit een **Netwerk-ID** (gebied) en een **Host-ID** (specifiek apparaat).

### **IPv4**
- **Formaat:** 32-bits (4 octets).
- **Notatie:** `xxx.xxx.xxx.xxx` (bijv. `192.168.0.1`).
- **Beperkingen:** Biedt ~4 miljard unieke adressen.
- **Subnetmasker:** Voorbeeld: `255.255.255.0` (CIDR `/24`).

### **IPv6**
- **Formaat:** 128-bits (8 groepen van 16-bits in hexadecimaal).
- **Notatie:** `xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx:xxxx`.
- **Voordelen:** 340 undeciljoen adressen, ontworpen om IPv4-beperkingen op te lossen.

---

## **Subnetten en CIDR**

### **Wat is subnetting?**
Subnetting verdeelt een netwerk in kleinere subnetwerken. Dit helpt bij beter gebruik van IP-adressen en verhoogt de veiligheid.

### **Subnetmaskers en CIDR-notatie**
- **Subnetmasker:** Duidt aan welk deel van een IP-adres het netwerk-ID en host-ID definieert.
  - Voorbeeld: `255.255.255.0` betekent dat de eerste 24 bits het netwerk-ID vormen.
- **CIDR-notatie:** Compacte representatie van subnetmaskers (bijv. `/24` voor `255.255.255.0`).

### **Subnetberekening**
- **Formule voor aantal hosts:** 2^(aantal hostbits) - 2.
  - Voorbeeld: Bij `/24` blijven 8 bits over voor hosts → 2^8 - 2 = 254 hosts.
- **Formule voor subnetten:** 2^(aantal subnetbits).
  - Voorbeeld: Als je 4 bits gebruikt voor subnetten → 2^4 = 16 subnetten.

---

## **IP-Klassen**

### **Overzicht van IP-klassen**
1. **Klasse A:**
   - Publieke IP-range: `1.0.0.0 - 127.255.255.255`.
   - Privé: `10.0.0.0 - 10.255.255.255`.
   - Maximaal aantal hosts: 2^24 - 2 = 16.777.214.

2. **Klasse B:**
   - Publieke IP-range: `128.0.0.0 - 191.255.255.255`.
   - Privé: `172.16.0.0 - 172.31.255.255`.
   - Maximaal aantal hosts: 2^16 - 2 = 65.534.

3. **Klasse C:**
   - Publieke IP-range: `192.0.0.0 - 223.255.255.255`.
   - Privé: `192.168.0.0 - 192.168.255.255`.
   - Maximaal aantal hosts: 2^8 - 2 = 254.

4. **Klasse D:** Multicast (geen hosts).
5. **Klasse E:** Gereserveerd voor onderzoek.

---

## **Voorbeelden van berekeningen**

### **Subnetmasker /24**
- **Subnetmasker:** `255.255.255.0`.
- **Aantal hosts:** 2^8 - 2 = 254.
- **Beschikbare IP-adressen:** `192.168.1.1 - 192.168.1.254`.

### **Subnetmasker /26**
- **Subnetmasker:** `255.255.255.192`.
- **Aantal hosts:** 2^6 - 2 = 62.
- **Beschikbare IP-adressen:** `192.168.1.1 - 192.168.1.62`.

### **IPv4 naar binair**
- **IP-adres:** `192.168.1.1`.
- **Binair:** `11000000.10101000.00000001.00000001`.

### **IPv6 voorbeeld**
- **Adres:** `2001:0db8:85a3:0000:0000:8a2e:0370:7334`.
- **Samengevoegd:** `2001:db8:85a3::8a2e:370:7334`.

---
![alt text](image.png)
---

## **Samenvatting**
De TCP/IP-suite is de ruggengraat van moderne netwerken. Subnetten en IP-adressering zijn essentieel voor netwerkbeheer. IPv6 biedt een oplossing voor de uitputting van IPv4-adressen en zorgt voor toekomstbestendigheid.


---

# Hoofdstuk 3 - Network Segmentation

## **Wat is netwerksegmentatie?**
Netwerksegmentatie is het proces waarbij een netwerk wordt onderverdeeld in kleinere, beter beheersbare domeinen, met beperkte communicatie tussen deze segmenten. Dit verhoogt zowel de veiligheid als het beheer binnen netwerken en cloudomgevingen. Elk segment kan specifieke beveiligingsregels en beleidsmaatregelen krijgen, afhankelijk van de behoeften van een organisatie. 

Bijvoorbeeld, een onderneming kan afzonderlijke segmenten maken voor HR, financiën, IT, marketing, en productie. Ook cloudgebaseerde omgevingen en SaaS-applicaties profiteren van segmentatie.

---

## **Voordelen van Netwerksegmentatie**
1. **Beperking van het aanvalsoppervlak:**
   - Door het netwerk te segmenteren, wordt de schade beperkt die een cyberaanvaller kan veroorzaken. Dit voorkomt laterale bewegingen van bedreigingen binnen een netwerk.
2. **Geavanceerde monitoring en detectie:**
   - Systemen kunnen waarschuwingen geven bij ongeautoriseerde toegangspogingen en verdachte activiteiten detecteren.
3. **Naleving van regelgeving:**
   - Bij audits, zoals voor de Payment Card Industry Data Security Standard (PCI DSS), kan de focus worden beperkt tot segmenten die kaartgegevens opslaan of verwerken.
4. **Beheersbaarheid:**
   - Netwerkbeheer wordt overzichtelijker doordat specifieke regels op afzonderlijke segmenten worden toegepast.

---

## **Netwerksegmentatie versus Microsegmentatie**
- **Netwerksegmentatie:** Verdeelt een netwerk in grotere secties en past algemene beveiligingsregels toe, zoals VLANs en firewalls.
- **Microsegmentatie:** Gaat verder door beveiligingsregels toe te passen op individuele workloads of virtuele machines. Het biedt meer granulariteit en is vaak gebaseerd op software-defined technologieën.

---

## **Netwerksegmentatie als Kern van Multi-Layer Defense**
Netwerksegmentatie vormt een belangrijk onderdeel van "defense-in-depth" strategieën. Door segmentatie wordt het voor aanvallers moeilijker om door te dringen. Het voorkomt of vertraagt onder andere:
- **SQL-injecties:** Aanvallen gericht op databases.
- **Compromitteren van werkstations:** Vooral apparaten met verhoogde rechten.
- **Aanvallen op perimeter servers:** Servers die extern toegankelijk zijn.
- **Misbruik van interne diensten:** Bijvoorbeeld LDAP of DNS.

Segmentatie voorkomt niet alleen aanvallen, maar biedt ook de mogelijkheid om schade te beperken als een aanval succesvol is.

---

## **Best Practices voor Netwerksegmentatie**

1. **Beveiligingsbeleid en bronnen identificeren:**
   - Ontwikkel beveiligingsbeleid voor elk type data en bron.
   - Identificeer welke gebruikers en systemen toegang nodig hebben, en definieer het toegangsmodel (bijv. lezen, schrijven).

2. **Gebruik Allowlist Access Control Lists (ACLs):**
   - Sta uitsluitend specifiek toegestane datastromen toe.
   - Identificeer en documenteer de datastromen van elke applicatie.
   - Hoewel dit tijdrovend kan zijn, voorkomt het dure beveiligingsincidenten.

3. **Fysieke en logische scheiding:**
   - **Fysieke scheiding:** Gebruik aparte firewalls of gescheiden hardware om netwerkcomplexiteit te verminderen.
   - **Logische scheiding:** Maak gebruik van VLANs, ACLs, en Virtual Routing and Forwarding (VRF) om netwerken logisch te scheiden.

4. **Software-defined Access (SD-Access):**
   - Gebruik SD-Access om endpoints te identificeren en ze aan specifieke segmenten toe te wijzen, ongeacht hun fysieke locatie.
   - Datastromen worden getagd, waardoor beveiligingsregels consistent kunnen worden toegepast.

5. **Automatisering:**
   - Automatiseer zoveel mogelijk stappen, zoals beveiligingsaudits, om consistentie te waarborgen en menselijke fouten te verminderen.
   - Gebruik tools die gebaseerd zijn op software-defined technologieën.

---

## **Hoe werkt Netwerksegmentatie?**

1. **Volledige blokkering:**
   - Het meest restrictieve beleid blokkeert alle communicatie tussen segmenten, bijvoorbeeld om te voldoen aan PCI DSS-regels. Dit voorkomt dat bedreigingen zich kunnen verspreiden.

2. **Selectieve filtering:**
   - Beperk welke soorten verkeer tussen zones mogen plaatsvinden, zoals DNS- of NTP-verkeer toestaan, maar alle andere typen blokkeren.
   - Filters kunnen gebaseerd zijn op IP-adressen, poorten, bron-applicaties, etc.

3. **Inspectie op applicatieniveau:**
   - Moderne netwerken vereisen granulariteit op applicatieniveau. Door next-gen firewalls te gebruiken, kunnen netwerkbeheerders datastromen inspecteren en toestaan of blokkeren op basis van gebruikersidentiteit, apparaatstatus en andere contextuele factoren.

---

## **Toepassingstechnologieën**
1. **Firewalls:** Voor fysieke en logische scheiding van segmenten.
2. **VLANs:** Virtuele netwerken creëren binnen een fysieke infrastructuur.
3. **VRF (Virtual Routing and Forwarding):** Logische scheiding van routinginformatie voor verschillende segmenten.
4. **SD-Access:** Voor consistent beleid ongeacht fysieke locatie.
5. **Automatisering:** Tools zoals software-defined technologieën voor consistentie en efficiëntie.

---

## **Samenvatting**
Netwerksegmentatie is een cruciaal mechanisme in moderne netwerkbeveiliging. Het beschermt gevoelige gegevens, voorkomt verspreiding van bedreigingen en verhoogt naleving van regelgeving. Door best practices zoals ACL’s, SD-Access en automatisering te implementeren, kunnen organisaties een robuust en schaalbaar beveiligingsmodel creëren.
