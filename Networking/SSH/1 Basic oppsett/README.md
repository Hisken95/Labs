# 1 Basic oppsett av SSH connection

## Oversikt
- Jeg vil lære hvordan jeg bruker SSH for å koble til en annen PC på nettverket.
- Jeg skal forsøke å "enable" SSH på min stasjonære PC, og koble til den med laptopene.


## Utstyr, Oppsett og ressurser
- Videoguide: https://www.youtube.com/watch?v=_RgTs6axOV8
- Stasjonær PC med Fedora KDE
- Laptop med Fedora KDE
- Laptop med Windows 11
- Alle er på samme hjemmenettverk. 

## Relevant informasjon
- Fedora KDE kommer preinstallert med SSH programvare som bare må bli "enabled". 

## Fremgangsmåte

### Steg 1: Enable SSH på stasjonær PC
1. Åpne konsole og skriv "sudo systemctlt enable SSHD"
2. Deretter "sudo systemctl start sshd"
3. Sjekk at den er startet og aktiv med "sudo systemctl status sshd"

### Steg 2: Koble til fra annen PC
1. Fedora laptop: I konsole kjør kommando: "ssh (IP adressen til PC du kobler til)"
2. Første gang vil den spør om man virkelig vil "connect" da den ikke kjenner igjen IP adressen du kobler til. Skriv "yes".
3. Testet at jeg var koblet til den stasjonære PCen ved å sjekke ip adresse "ip a", og ved å opprette tekstdokument "touch test.txt".

### Steg 3: Koble til med windows PC
1. Last ned on installer PuTTY
2. I PuTTY legg inn ip adressen på PCen jeg skal koble til, og trykk "open". Videre trykk "accept"
3. Login inn med brukernavn og passordet til den stasjonære fedora PCen.
4. Test at er logget på rett PC med kommandoer som "ip a" og "touch test2.txt". 


---

## Nyttige kommandoer
- sudo systemctlt enable SSHD
- sudo systemctl start sshd
- sudo systemctl status sshd
- ssh (IP adressen til PC du kobler til)

