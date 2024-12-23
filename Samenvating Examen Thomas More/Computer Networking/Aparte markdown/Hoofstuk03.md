# Network Segmentation

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
