# **Virtualization and Cloud Computing & Storage**

## **Deel 1: Virtualization**

### **Wat is Virtualisatie?**
Virtualisatie is het proces waarbij een fysieke server wordt opgedeeld in meerdere virtuele servers (Virtual Machines, VM’s) via een **hypervisor**. Hierdoor kunnen meerdere besturingssystemen en toepassingen parallel draaien op dezelfde hardware.

---

### **Voordelen van Virtualisatie**
1. **Efficiënt gebruik van hardware:**
   - Hardwarebronnen zoals CPU, RAM en opslag worden optimaal benut.
2. **Flexibiliteit:**
   - Meerdere besturingssystemen en applicaties kunnen tegelijkertijd draaien zonder conflicten.
3. **Schaalbaarheid:**
   - Bronnen kunnen eenvoudig worden opgeschaald of afgeschaald op basis van behoefte.
4. **Kostenbesparing:**
   - Minder fysieke servers nodig, waardoor operationele kosten dalen.

---

### **Typen Hypervisors**
1. **Type 1 Hypervisor (Bare Metal):**
   - Draait direct op de hardware zonder een onderliggend OS.
   - **Voorbeelden:** VMware ESXi, Microsoft Hyper-V, Boot Camp.

2. **Type 2 Hypervisor:**
   - Draait bovenop een bestaand besturingssysteem als applicatie.
   - **Voorbeelden:** VirtualBox, VMware Workstation, Parallels.

---

### **Virtuele Containers**
Containers zijn een lichtere vorm van virtualisatie waarbij alleen de applicatie en bijbehorende afhankelijkheden worden gevirtualiseerd, in plaats van een volledig besturingssysteem.

#### **Voordelen van Containers**
1. **Snelle opstarttijd:** Binnen enkele seconden operationeel.
2. **Efficiënt gebruik van bronnen:** Minder overhead dan volledige VM’s.
3. **Flexibiliteit:** Containers zijn ideaal voor het ontwikkelen en implementeren van microservices.

#### **Bekende Tools voor Containers:**
- Docker
- Kubernetes
- Podman
- Swarm

---

### **Virtuele Netwerken**
1. **vSwitches:**
   - Virtuele switches beheren netwerkverkeer binnen een virtualisatieserver.
   - vSwitches maken interne communicatie mogelijk tussen VMs.

2. **vNICs:**
   - Virtuele netwerkkaarten maken verbinding met externe netwerken mogelijk.

---

### **Toepassingen van Virtualisatie**
1. **Ontwikkeling en testen:**
   - Nieuwe besturingssystemen of applicaties kunnen veilig worden getest.
2. **Penetratietests:**
   - Tools zoals Kali Linux kunnen in een gesimuleerde omgeving worden gebruikt.
3. **Back-ups en Snapshots:**
   - Gemakkelijk terugkeren naar een eerdere staat.
4. **Server Consolidatie:**
   - Meerdere VM’s kunnen draaien op één fysieke server om ruimte en energie te besparen.

---

## **Deel 2: Cloud Computing & Storage**

### **Wat is Cloud Computing?**
Cloud computing biedt schaalbare en elastische toegang tot gedeelde fysieke en virtuele bronnen via het internet. Gebruikers kunnen opslag, rekenkracht en netwerkdiensten on-demand gebruiken zonder eigen hardware te beheren.

---

### **Belangrijkste Eigenschappen van Cloud Computing** (volgens NIST):
1. **On-demand self-service:**
   - Gebruikers kunnen zelf bronnen provisioneren zonder menselijke interactie met de provider.

2. **Brede netwerktoegang:**
   - Toegang via standaardprotocollen op apparaten zoals laptops, tablets en mobiele telefoons.

3. **Resource Pooling:**
   - Bronnen worden gedeeld over meerdere gebruikers via een multi-tenant model.

4. **Snelle Elasticiteit:**
   - Bronnen kunnen automatisch worden opgeschaald of afgeschaald op basis van de vraag.

5. **Gemeten Service:**
   - Verbruik wordt gemonitord en gefactureerd op basis van daadwerkelijk gebruik.

---

### **Service Modellen in Cloud Computing**
1. **IaaS (Infrastructure as a Service):**
   - Biedt basisinfrastructuur zoals servers, opslag en netwerken.
   - **Voorbeelden:** Amazon EC2, Google Compute Engine.

2. **PaaS (Platform as a Service):**
   - Ontwikkelplatforms voor het bouwen en implementeren van applicaties.
   - **Voorbeelden:** Google App Engine, Microsoft Azure App Services.

3. **SaaS (Software as a Service):**
   - Gebruikers hebben toegang tot kant-en-klare applicaties.
   - **Voorbeelden:** Google Workspace, Dropbox, Salesforce.

---

### **Cloud Opslag**
Cloudopslag verwijst naar gegevens die extern worden opgeslagen in logische pools. De fysieke opslag wordt beheerd door cloudproviders zoals AWS, Google Drive en Microsoft Azure.

#### **Voordelen van Cloudopslag:**
1. **Schaalbaarheid:**
   - Bronnen kunnen on-demand worden uitgebreid.
2. **Beschikbaarheid:**
   - Data is overal toegankelijk via internet.
3. **Kostenbesparing:**
   - Geen investering in lokale hardware nodig.

#### **Soorten Opslag:**
1. **Primaire Opslag:** RAM, direct toegankelijk door de CPU.
2. **Secundaire Opslag:** SSD’s en HDD’s, langzamere toegang maar persistent.
3. **Tertiaire Opslag:** Automatisering zoals tapes voor archivering.
4. **Offline Opslag:** Niet direct verbonden met een systeem, bijvoorbeeld USB-schijven.

---

### **Netwerkopslag**
1. **DAS (Direct Attached Storage):**
   - Direct verbonden met een computer zonder netwerk.

2. **NAS (Network Attached Storage):**
   - Bestandsopslag via een netwerk, toegankelijk voor meerdere gebruikers.

3. **SAN (Storage Area Network):**
   - Hogesnelheidsopslag op block-niveau, ideaal voor datacenters.

---

### **Waardepropositie van Cloud Computing**
1. **Kostenreductie:**
   - Kapitaalinvesteringen worden vervangen door operationele uitgaven.

2. **Flexibiliteit:**
   - Toegang vanaf elk apparaat met een internetverbinding.

3. **Hoge Beschikbaarheid:**
   - Redundantie en back-ups zorgen voor betrouwbaarheid.

4. **Verbeterde Beveiliging:**
   - Data wordt gecentraliseerd en beveiligd met encryptie.

---

### **Uitdagingen in Cloud Computing**
1. **Beveiliging en Privacy:**
   - Gegevensbeveiliging is afhankelijk van de provider.

2. **Kostenbeheer:**
   - Zonder monitoring kunnen cloudkosten oplopen.

3. **Beperkte Controle:**
   - Gebruikers hebben minder inzicht in hoe resources worden beheerd.

---

## **Samenvatting**
Virtualisatie en cloud computing zijn fundamentele technologieën voor moderne IT-infrastructuren. Virtualisatie biedt flexibiliteit en resource-optimalisatie, terwijl cloud computing schaalbare, on-demand toegang tot infrastructuur en opslag biedt. Hoewel beide technologieën uitdagingen zoals beveiliging en kostenbeheer hebben, bieden ze enorme voordelen voor efficiëntie, schaalbaarheid en kostenbesparing.
