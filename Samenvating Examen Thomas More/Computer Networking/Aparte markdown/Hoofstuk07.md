# **Scripting**

## **Wat is Scripting?**
Scripting is het proces van het schrijven van relatief korte en eenvoudige instructies (scripts) om een anders handmatig proces te automatiseren. Een script wordt meestal geschreven in een **scripttaal**, ontworpen om eenvoudige automatisering mogelijk te maken.

### **Kenmerken van Scripting:**
1. **Geïnterpreteerd:**
   - Scripts worden niet gecompileerd naar machinecode zoals traditionele programma's. Ze worden rechtstreeks uitgevoerd door een interpreter.
2. **Kort en eenvoudig:**
   - Scripts bevatten vaak enkele regels code en zijn gericht op specifieke taken.
3. **Beperkte mogelijkheden:**
   - Scripttalen missen vaak de complexiteit van algemene programmeertalen.
4. **Directe uitvoering:**  
   - Scripts starten doorgaans met de eerste regel code, zonder de noodzaak van een expliciete ingangspunten zoals `main()` in Java.

---

## **Voorbeelden van Scripttalen**
1. **Python:** Een veelzijdige taal, geschikt voor zowel scripting als applicatieontwikkeling.  
   - Voorbeeld:  
     ```python
     print("Hello World")
     ```
2. **Bash:** Veel gebruikt op Unix/Linux-systemen voor het schrijven van shellscripts.  
3. **PowerShell:** Speciaal ontworpen voor Windows-beheer en automatisering.

---

### **PowerShell vs Bash**
1. **PowerShell:**
   - Gebaseerd op .NET-objecten.
   - Syntax: **werkwoord-zelfstandig naamwoord** (bijv. `Get-Item`).
2. **Bash:**
   - Gebaseerd op tekstmanipulatie.
   - Simpel en direct, maar minder geschikt voor complexe objectmanipulaties.

---

## **Belangrijke PowerShell Commando’s**
1. **Get-Command:** Bekijk alle beschikbare commando’s.
2. **Get-Help:** Toon hulpinformatie voor een specifiek commando.
3. **Set-Location:** Navigeer naar een map (alias `cd`).
4. **Get-ChildItem:** Lijst bestanden en mappen (alias `dir`).

---

### **Veelgebruikte Werkwoorden in PowerShell**
- **Get:** Haalt gegevens op zonder wijzigingen aan te brengen.  
- **Set:** Wijzigt bestaande instellingen.  
- **New:** Maakt nieuwe items aan.  
- **Remove:** Verwijdert bestaande items.  
- **Add:** Voegt items toe.

---

### **Navigeren in PowerShell**
1. **Map veranderen:**  
   ```powershell
   Set-Location "C:\\Users\\Documents"
   ```
2. **Gebruik pijltjestoetsen:** Navigeer door recente commando’s.
3. **Tab-completie:** Gebruik `<Tab>` om commando’s automatisch aan te vullen.

---

### **Bestanden en Directories Beheren**
1. **Nieuw bestand of map aanmaken:**  
   ```powershell
   New-Item -Path "C:\\Test" -ItemType "Directory"
   ```
2. **Inhoud bekijken:**  
   ```powershell
   Get-Content "C:\\Test\\file.txt"
   ```
3. **Tekst toevoegen:**  
   ```powershell
   "Nieuwe tekst" >> "C:\\Test\\file.txt"
   ```

---

## **Pipelines in PowerShell**
De **pipeline (`|`)** in PowerShell maakt het mogelijk om de uitvoer van een commando als invoer voor een ander te gebruiken.  
- **Voorbeeld:**  
  ```powershell
  Get-ChildItem | Where-Object {$_.Length -gt 100KB}
  ```

---

### **Geavanceerde Functies**
1. **Filteren:**  
   Gebruik regex of logische operatoren om gegevens te filteren.  
   - Voorbeeld:  
     ```powershell
     Get-ChildItem | Where-Object {$_.Name -match "log"}
     ```
2. **Groeperen:**  
   Groepeer resultaten op eigenschappen.  
   - Voorbeeld:  
     ```powershell
     Get-ChildItem | Group-Object Extension
     ```
3. **Meting:**  
   Meet eigenschappen zoals bestandsgrootte.  
   - Voorbeeld:  
     ```powershell
     Get-ChildItem | Measure-Object Length -Sum
     ```

---

## **Toepassingen van Scripting**
1. **Automatisering:**  
   Het uitvoeren van routinetaken zoals back-ups of updates.
2. **Beheer:**  
   Configureren van gebruikersrechten of het installeren van software.
3. **Data-analyse:**  
   Filteren en sorteren van logbestanden.
4. **Testen:**  
   Scripts worden gebruikt om applicaties te testen in verschillende omgevingen.

---

### **Praktijkvoorbeeld: Eenvoudige Automatisering**
1. Maak een script dat mappen aanmaakt en bestanden verplaatst:  
   ```powershell
   $source = "C:\\Downloads"
   $destination = "C:\\SortedFiles"
   New-Item -Path $destination -ItemType "Directory"
   Get-ChildItem $source | Move-Item -Destination $destination
   ```

---

## **Voordelen van Scripting**
1. **Snelheid:** Automatisering van repetitieve taken bespaart tijd.  
2. **Flexibiliteit:** Scripts kunnen eenvoudig worden aangepast.  
3. **Integratie:** Werkt goed met andere tools en systemen.

---

## **Nadelen van Scripting**
1. **Beperkte complexiteit:** Niet geschikt voor grote applicaties.  
2. **Foutgevoelig:** Scripts zijn afhankelijk van correcte syntax en logica.  
3. **Performance:** Meestal minder efficiënt dan gecompileerde talen.

---

## **Samenvatting**
Scripting is een essentiële vaardigheid voor automatisering en systeembeheer. Met talen zoals PowerShell, Bash en Python kunnen gebruikers efficiënter werken en complexe taken automatiseren. Hoewel scripts beperkt zijn in functionaliteit, zijn ze ideaal voor routinematige en beheertaken.
