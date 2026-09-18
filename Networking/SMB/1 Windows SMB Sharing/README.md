# 1 Windows SMB Sharing

## Oversikt
Lære om SMB protokollen ved å dele en mappe over nettverket ved bruk av SMB. Dette skal jeg gjøre med å dele en mappe fra windows PCen og åpne mappen med en annen PC.

## Utstyr, Oppsett og ressurser
Stasjonær PC med Fedora KDE
Laptop med Fedora KDE
Laptop med Windows 11
Alle er på samme hjemmenettverk.

## Relevant informasjon
Fedora KDE kommer preinstallert med SSH programvare som bare må bli "enabled".

## Fremgangsmåte
### Steg 1: Dele mappe
1. PC1: Lagde en mappe kaldt "Share" på windows maskinen med en .txt fil i.
2. Åpne for deling av mappen: Properties - Sharing - Advanced Sharing

### Steg 2: Åpne mappen fra annen maskin
1. PC2: I filexplorer put inn \\"PC1 IP-Adresse"\Share
2. Logg inn med outlook konto fra PC1
3. Endre på .txt fil, og se på PC1 at endring har skjedd.

### Steg 3: Verifiser port connection
1. PC1: Åpne cmd og skriv: "netstat -ano"
2. Får opp liste over forskjellige aktive connections. Finn connection for port 445 (SMB port).
3. Ser at det er PC1 sin IP-adresse som er tilkoblet, og under "State" står det "ESTABLISHED".
4. Det betyr at en connection er etablert mellom PC1 og PC2 på SMB-port 445.


## Nyttige kommandoer
- netstat -ano
