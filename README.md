# 🔐 Password Generator

Een moderne, veilige wachtwoordgenerator voor Windows met systemtray integratie, meerdere wachtwoordtypes, entropy-gebaseerde sterkte-indicatie en volledig aanpasbare themes.

![.NET 10](https://img.shields.io/badge/.NET-10-purple)
![WPF](https://img.shields.io/badge/WPF-Windows-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Belangrijkste Features

### 🎯 Wachtwoord Generatie
- **6 Verschillende Types**:
  - 🌟 Licht Password - Alleen letters en cijfers
  - 💪 Sterk Password - Letters, cijfers en basis speciale tekens
  - 🔥 Zeer Sterk Password - Letters, cijfers en uitgebreide speciale tekens
  - 🔐 Ultra Secure (Max Entropy) - Maximum entropie met alle mogelijke tekens
  - 📝 Passphrase - Leesbare woordcombinaties met nummers
  - 📚 Woorden Password - Gemengde woorden met cijfers en tekens

- **Instelbare Lengte**: 8-32 tekens met real-time slider

### 🎨 Moderne UI
- **5 Professionele Themes**:
  - 🌌 Dark Purple (standaard)
  - 💙 Dark Blue
  - 🌃 Cyberpunk
  - 🌲 Forest
  - 🌊 Ocean

- **Visuele Feedback**:
  - Entropy-gebaseerde wachtwoordsterkte indicator
  - Real-time kleurcodering (optioneel)
  - Smooth animaties en shadow effecten
  - Toast notificaties voor acties

### 🔒 Beveiliging
- **Automatische Beveiliging**:
  - ⏱️ Auto-clear clipboard na X seconden
  - 🔐 Auto-mask wachtwoord na X seconden
  - Gemaskeerde wachtwoorden kunnen **niet** gekopieerd worden
  - Gemaskeerde wachtwoorden kunnen **niet** geselecteerd worden

- **Wachtwoord Masking**:
  - Wachtwoord wordt vervangen door ●●●●●●●● na timeout
  - Voorkomt shoulder surfing
  - Unmask automatisch bij nieuwe generatie

### 🚀 Systemtray Integratie
- **Quick Password Popup**:
  - Linker-klik op tray icon voor snelle wachtwoord generatie
  - Minimalistische interface met alleen het noodzakelijke
  - Real-time wachtwoord generatie tijdens slider gebruik
  - Optionele entropy-kleuren weergave

- **Altijd Beschikbaar**:
  - App blijft actief in systemtray
  - Sluit knop verbergt venster (sluit niet af)
  - Start bij Windows opstarten (optioneel)

### 📊 Wachtwoord Sterkte Analyse
- **Entropy Berekening**:
  - Real-time berekening van wachtwoord sterkte
  - Kleur-gecodeerde indicator
  - Bits entropy weergave
  - Waarschuwingen bij zwakke wachtwoorden (optioneel)

**Sterkte Niveaus**:
- 😟 Zeer Zwak (< 28 bits) - Rood
- 😐 Zwak (28-36 bits) - Oranje  
- 🙂 Redelijk (36-60 bits) - Geel
- 😊 Sterk (60-80 bits) - Paars
- 💪 Zeer Sterk (80-128 bits) - Licht groen
- 🔒 Onbreekbaar (>128 bits) - Groen

## 🖥️ Systeemvereisten

- **OS**: Windows 10/11
- **.NET**: .NET 10 Runtime
- **RAM**: 50 MB
- **Schijfruimte**: 10 MB

## 📦 Installatie

1. Download de laatste release
2. Pak het archief uit naar een map naar keuze
3. Voer PasswordGenerator.exe uit
4. (Optioneel) Schakel "Start bij opstarten" in via instellingen

## 🎮 Gebruik

### Basis Gebruik

1. **Wachtwoord Genereren**:
   - Selecteer een wachtwoord type
   - Pas de lengte aan met de slider (8-32 tekens)
   - Klik op "✨ Genereer Password"

2. **Kopiëren**:
   - Klik op "📋 Kopieer" om naar clipboard te kopiëren
   - Notificatie toont hoeveel seconden tot clipboard wordt gewist

3. **Quick Popup**:
   - **Linker-klik** op tray icon voor snelle generatie
   - Pas lengte aan, wachtwoord regenereert automatisch
   - Kopieer en gebruik direct

### Instellingen

Open instellingen via het ⚙️ icoon of rechter-klik tray menu.

#### 🔐 Beveiliging Opties

**Auto-clear Clipboard**
- Automatisch clipboard wissen na kopiëren
- Instelbaar tussen 5-60 seconden
- Voorkomt dat wachtwoorden blijven plakken

**Auto-mask Wachtwoord**
- Automatisch wachtwoord maskeren na generatie
- Instelbaar tussen 10-300 seconden
- Twee modi:
  - "Na kopiëren" - Direct na kopieer actie
  - "Na tijd" - Na ingestelde tijd

**Waarschuwingen**
- Optionele waarschuwing bij zwakke wachtwoorden
- Toon/verberg sterkte indicator
- Notificaties in/uitschakelen

#### ⚡ Quick Popup Instellingen

**Standaard Type**
- Kies welk wachtwoordtype standaard wordt gebruikt in quick popup
- Snellere workflow

**Standaard Lengte**
- Vooringestelde slider waarde (8-32)
- Quick popup opent met deze lengte

**Wachtwoord Kleuren**
- Toon entropy-gebaseerde kleuren in quick popup
- Real-time kleurverandering tijdens generatie

#### 🎨 Thema's

Kies uit 5 professionele themes:
- 🌌 Dark Purple
- 💙 Dark Blue  
- 🌃 Cyberpunk
- 🌲 Forest
- 🌊 Ocean

**Let op**: App herstart automatisch bij theme wijziging voor volledige toepassing.

#### 🚀 Opstarten

**Start bij opstarten**
- Automatisch starten met Windows
- App start geminimaliseerd in systemtray
- Altijd beschikbaar voor wachtwoord generatie

## 🔑 Keyboard Shortcuts

- Esc - Sluit venster (verbergt naar tray)

## 📁 Bestandslocaties

### Instellingen
%AppData%\PasswordGenerator\settings.json

Bevat:
- Beveiligingsinstellingen
- Quick popup voorkeuren
- Gekozen theme
- Opstarten configuratie

## 🛠️ Technische Details

### Architectuur
- **Framework**: WPF (.NET 10)
- **Pattern**: MVVM-achtig met code-behind
- **Resources**: Runtime theme loading via ResourceDictionary
- **Persistentie**: JSON-based settings in AppData
- **Tray**: Windows Forms NotifyIcon integratie

### Wachtwoord Generatie
- **RNG**: System.Security.Cryptography.RandomNumberGenerator
- **Entropy**: Shannon entropy berekening
- **Character Sets**: Meerdere pools afhankelijk van type

### Beveiliging Principes
- Geen wachtwoord opslag in geheugen langer dan nodig
- Automatic clipboard clearing
- Visual masking na timeout
- Geen logging van gegenereerde wachtwoorden

## 🎯 Veelgestelde Vragen

**Q: Waarom herstart de app bij theme wijziging?**  
A: Voor volledige toepassing van theme resources op alle vensters en styles is een herstart nodig.

**Q: Zijn mijn wachtwoorden veilig?**  
A: Ja! Wachtwoorden worden nergens opgeslagen en gebruiken cryptografisch veilige random generatie.

**Q: Kan ik gemaskeerde wachtwoorden kopiëren?**  
A: Nee, dit is bewust om te voorkomen dat oude/gemaskeerde wachtwoorden per ongeluk worden gebruikt.

**Q: Hoe verwijder ik de app?**  
A: 
1. Sluit de app via tray menu → "Afsluiten"
2. Verwijder de applicatie map
3. Verwijder %AppData%\PasswordGenerator voor instellingen

**Q: Werkt dit op andere besturingssystemen?**  
A: Momenteel alleen Windows. WPF is Windows-specifiek.

## 📝 Changelog

### v1.0.0 (Huidig)
- ✅ Meerdere wachtwoord types
- ✅ 5 Themes
- ✅ Quick popup tray integratie
- ✅ Entropy-gebaseerde sterkte analyse
- ✅ Auto-clear clipboard & password masking
- ✅ Configureerbare instellingen
- ✅ Windows startup integratie
- ✅ Real-time wachtwoord generatie

## 🤝 Bijdragen

Dit is een personal project, maar suggesties zijn welkom!

## 📄 Licentie

MIT License - Vrij te gebruiken voor persoonlijke en commerciële doeleinden.

## 👨‍💻 Ontwikkelaar

Ontwikkeld met ❤️ en veel ☕

---

**⚠️ Veiligheidswaarschuwing**: Gebruik altijd unieke wachtwoorden voor verschillende accounts en overweeg het gebruik van een password manager voor opslag.

**💡 Tip**: Voor maximale veiligheid, gebruik "🔐 Ultra Secure (Max Entropy)" met lengte 24+ tekens.
