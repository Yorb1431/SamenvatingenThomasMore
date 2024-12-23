# Internet Protocol Suite

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

## **Samenvatting**
De TCP/IP-suite is de ruggengraat van moderne netwerken. Subnetten en IP-adressering zijn essentieel voor netwerkbeheer. IPv6 biedt een oplossing voor de uitputting van IPv4-adressen en zorgt voor toekomstbestendigheid.
