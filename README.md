# izGear — distribuzione

Qui si pubblicano le release di **izGear**, il motore che esegue script scritti in XML:
pacchetti del motore e dei moduli e script di installazione. I sorgenti non sono in
questo repository.

## Installazione

Non serve nulla di preinstallato: lo script scarica nella directory di installazione
un runtime Java 21 (Temurin JRE) in `jvm/` e Apache Ant in `ant/`, ne verifica
l'impronta, poi installa izGear. Non modifica PATH, registro né profilo dell'utente.

**Windows 10 o successivo, x64** (PowerShell):

```powershell
irm https://github.com/initzeromp/izgear-dist/releases/latest/download/install.ps1 | iex
```

**Linux x64, macOS (Intel e Apple Silicon)**, con `curl`, `tar` e `unzip`:

```sh
curl -fsSL https://github.com/initzeromp/izgear-dist/releases/latest/download/install.sh | sh
```

La directory predefinita è `%USERPROFILE%\izgear` o `$HOME/izgear`; se ne indica
un'altra con la variabile `IZG_HOME` o come argomento dello script.

Chi preferisce leggere lo script prima di lanciarlo lo scarica, lo legge e lo esegue:

```sh
curl -fsSLO https://github.com/initzeromp/izgear-dist/releases/latest/download/install.sh
less install.sh
sh install.sh
```

## Aggiornamento e disinstallazione

Per aggiornare si rilancia lo stesso comando, oppure `bin/update` dentro
l'installazione. Per disinstallare basta cancellare la directory di installazione:
nulla è scritto fuori.
