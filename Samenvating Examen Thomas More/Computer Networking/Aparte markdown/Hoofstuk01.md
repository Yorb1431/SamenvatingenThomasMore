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
