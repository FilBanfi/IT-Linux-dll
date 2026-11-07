# IT-Linux-dll

The Linux Italian keyboard layout finally ported to Windows.

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Platform: Windows](https://img.shields.io/badge/Platform-Windows%2010%2F11-blue.svg)](https://www.microsoft.com/windows)

[Italiano](#italiano)

| Base | Shift |
| :---: | :---: |
| ![Layout Base](resources/layout_base.png) | ![Layout Shift](resources/layout_shift.png) |
| **AltGr** | **Shift + AltGr** |
| ![Layout AltGr](resources/layout_altgr.png) | ![Layout Shift+AltGr](resources/layout_altgr_shift.png) |

---

## Overview

This project ports the logical and functional mapping of the standard Linux (XKB) Italian keyboard layout to Windows. 

The default Windows Italian layout limits `AltGr` usage to a few keys and relies on dead keys that slow down coding. This DLL faithfully replicates the Linux experience, providing full `AltGr` and `Shift+AltGr` support across almost all keys, allowing developers to maintain the same muscle memory across both operating systems.

## Installation

### Recommended Method (MSI)
1. Go to the [Releases](https://github.com/FilBanfi/IT-Linux-dll/releases) section.
2. Download `IT-Linux-dll-amd64.msi` (for 64-bit systems) or `IT-Linux-dll-x86.msi` (for 32-bit systems).
3. Run the `.msi` file to install the layout.
4. Go to **Settings > Time & Language > Language & Region > Italian > Options**.
5. Under "Keyboards", click **Add a keyboard** and select the newly installed layout.

### Manual DLL Installation
*Useful for custom ISO integration or environments without installation privileges.*
1. Download `IT-Linux-dll-amd64.dll` (or `x86`) from the Releases section.
2. Place the file in `C:\Windows\System32\` (for amd64) or `C:\Windows\SysWOW64\` (for x86).
3. Manually register the layout in the Windows Registry under the installed keyboards key.

## Compilation

**Prerequisites:**
- [Microsoft Keyboard Layout Creator 1.4 (MSKLC)](https://download.microsoft.com/download/6/f/5/6f5ce43a-e892-4fd1-b9a6-1a0cbb64e6e2/MSKLC.exe)
- [.NET Framework 3.5 for Windows 11](https://download.microsoft.com/download/298af580-974e-4001-a07d-bb200d7c5792/DotNet35Setup.exe)

**Procedure:**
1. Install .NET Framework 3.5, then install MSKLC. 
   *(Note: If the MSKLC installer hangs due to .NET 3.5 checks, you can extract the binaries, including `kbdutool.exe`, directly from the executable using 7-Zip and compile from the command line).*
2. Open the `FilBanfi_IT.klc` file with MSKLC.
3. Make any necessary modifications in the visual grid.
4. Select **Project > Build DLL and Setup Package**.
5. The generated files (`.dll` and `.msi`/`setup.exe`) will be located in the project folder.

## Repository Structure

- `FilBanfi_IT.klc`: Layout source file, compatible with MSKLC 1.4.
- `LICENSE`: GNU General Public License v3.0 text.
- `README.md`: Project documentation.
- `resources/`: Reference images of the keyboard mapping.

## AI Acknowledgement & Disclaimer

This project utilized AI assistance specifically to parse the raw XKB keyboard export from Fedora 44 and accurately map it to the Windows `.klc` format. If you disagree with the use of AI in this workflow, you are welcome to write the layout mapping manually.

---

## Italiano

Questo progetto porta la mappatura logica e funzionale del layout di tastiera italiano standard di Linux (XKB) su Windows.

Il layout italiano predefinito di Windows limita l'uso di `AltGr` a pochi tasti e utilizza dead keys che rallentano la scrittura di codice. Questa DLL replica fedelmente l'esperienza Linux, fornendo supporto completo per `AltGr` e `Shift+AltGr` su quasi tutti i tasti, permettendo di mantenere la stessa memoria muscolare tra i due sistemi operativi.

## Installazione

### Metodo consigliato (MSI)
1. Vai alla sezione [Releases](https://github.com/FilBanfi/IT-Linux-dll/releases).
2. Scarica `IT-Linux-dll-amd64.msi` (per sistemi a 64-bit) o `IT-Linux-dll-x86.msi` (per sistemi a 32-bit).
3. Esegui il file `.msi` per installare il layout.
4. Vai su **Impostazioni > Tempo e lingua > Lingua e area geografica > Italiano > Opzioni**.
5. In "Tastiere", clicca su **Aggiungi una tastiera** e seleziona il layout appena installato.

### Installazione manuale della DLL
*Utile per l'integrazione in ISO custom o ambienti senza privilegi di installazione.*
1. Scarica `IT-Linux-dll-amd64.dll` (o `x86`) dalla sezione Releases.
2. Posiziona il file in `C:\Windows\System32\` (per amd64) o `C:\Windows\SysWOW64\` (per x86).
3. Registra manualmente il layout nel Registro di sistema di Windows sotto la chiave delle tastiere installate.

## Compilazione

**Prerequisiti:**
- [Microsoft Keyboard Layout Creator 1.4 (MSKLC)](https://download.microsoft.com/download/6/f/5/6f5ce43a-e892-4fd1-b9a6-1a0cbb64e6e2/MSKLC.exe)
- [.NET Framework 3.5 per Windows 11](https://download.microsoft.com/download/298af580-974e-4001-a07d-bb200d7c5792/DotNet35Setup.exe)

**Procedura:**
1. Installa .NET Framework 3.5 e successivamente MSKLC.
   *(Nota: Se l'installer di MSKLC si blocca, è possibile estrarre i binari, incluso `kbdutool.exe`, direttamente dall'eseguibile usando 7-Zip e compilare da riga di comando).*
2. Apri il file `FilBanfi_IT.klc` con MSKLC.
3. Apporta le modifiche necessarie nella griglia visuale.
4. Seleziona **Project > Build DLL and Setup Package**.
5. I file generati (`.dll` e `.msi`/`setup.exe`) si troveranno nella cartella del progetto.

## Struttura del repository

- `FilBanfi_IT.klc`: File sorgente del layout, compatibile con MSKLC 1.4.
- `LICENSE`: Testo della licenza GNU General Public License v3.0.
- `README.md`: Documentazione del progetto.
- `resources/`: Immagini di riferimento della mappatura dei tasti.

## Riconoscimento e Disclaimer sull'IA

Questo progetto ha utilizzato l'assistenza dell'IA specificamente per analizzare l'export grezzo della tastiera XKB da Fedora 44 e mapparlo accuratamente nel formato `.klc` di Windows. Se non sei d'accordo con l'uso dell'IA in questo flusso di lavoro, sei liberissimo di scriverti la mappatura del layout manualmente.

## Licenza

Questo progetto è distribuito sotto i termini della **GNU General Public License v3.0**. Vedi il file [LICENSE](LICENSE) per i dettagli.
