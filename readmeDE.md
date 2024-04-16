# Offizielle IO-Net-Binärdateien

Dieses Repository enthält offizielle Binärdateien für das io.net - Folgen Sie den folgenden Anweisungen, um die Binärdateien auf Ihrem jeweiligen Betriebssystem einzurichten und auszuführen.

## Vorraussetzungen

### Für Linux
- Docker
- Nvidia-Treiber (im Falle von GPU Worker) (durch Ausführen von io-setup wird dies automatisch installiert, falls erforderlich)
- Nvidia Container Toolkit (im Falle von GPU Worker) (io-setup installiert dies automatisch, falls erforderlich)

### Für Mac
- Docker-Desktop
 - [Download Docker Desktop für Mac](https://www.docker.com/products/docker-desktop/) - wählen Sie die Mac - Apple Chip Version zum Download

## Installation

### Linux

1. **IO-Setup durchführen (einmalig für Hardware)** (überspringen, wenn Docker und Nvidia-Treiber bereits installiert und konfiguriert sind)
 - Laden Sie das Setup-Skript herunter: 
```
 curl -L https://github.com/ionet-official/io-net-official-setup-script/raw/main/ionet-setup.sh -o ionet-setup.sh
 ```
 - Führen Sie das Skript aus:
 ```
 chmod +x ionet-setup.sh && ./ionet-setup.sh
 ```
 ##### Hinweis - falls der Befehl curl fehlschlägt: 
- Installieren Sie `curl`: 
```
 sudo apt install curl
 ```

2. **Für Systeme mit GPUs**
 - Warten Sie auf einen Neustart.
 - Nach dem Neustart führen Sie das Setup erneut mit dem obigen Befehl aus.

### Starten Sie die Container mit binary

3. **Binärdatei herunterladen und starten**:
 ```
 curl -L https://github.com/ionet-official/io_launch_binaries/raw/main/launch_binary_linux -o launch_binary_linux
 chmod +x launch_binary_linux
 ```

- Starten Sie im interaktiven Modus oder kopieren Sie den generierten Befehl von der Website.
 ```
 ./launch_binary_linux
 ```


### Mac

- **Binärdatei herunterladen und starten**:
 ```
 curl -L https://github.com/ionet-official/io_launch_binaries/raw/main/launch_binary_mac -o launch_binary_mac
 chmod +x launch_binary_mac
 ```

- Starten Sie im interaktiven Modus oder kopieren Sie den generierten Befehl von der Website.
 ```
 ./launch_binary_mac
 ```

- Fehlerbehebung (optional)

 - Wenn Sie eine Fehlermeldung wie "schlechter CPU-Typ in der ausführbaren Datei" erhalten, bedeutet dies wahrscheinlich, dass Sie Software, die für einen Intel-Prozessor entwickelt wurde, auf einem Apple-Silicon-Gerät ausführen. Um dieses Problem zu beheben, müssen Sie Rosetta 2 installieren, das die Unterstützung für Intel-Prozessoren in Docker auf Apple Silicon-Geräten ermöglicht.
 
```
 softwareupdate --install-rosetta
 ```

 - Nachdem die Rosetta-Installation abgeschlossen ist, führen Sie den Befehl excute erneut aus.
 
```
 ./launch_binary_mac
 ```

<!-- ### Windows

1. **Download binary**:
- Gehen Sie zu Ihrem Browser und fügen Sie ein:
 ```
 wget https://github.com/ionet-official/io_launch_binaries/raw/main/launch_binary_windows
 ```
- Doppelklicken Sie auf die heruntergeladene Datei und geben Sie die Details im interaktiven Modus ein. -->


## Unterstützung

Wenn Sie Unterstützung benötigen, öffnen Sie bitte ein Problem oder kontaktieren Sie unser Support-Team auf [discord](https://discord.gg/kqFzFK7fg2)
