lägg denna rad för att skapa "startnyckeln".


usb-storage.quirks=0204:3639:u console=serial0,115200 console=tty1 root=PARTUUID=df6d3ab6-02 rootfstype=ext4 fsck.repair=yes rootwait quiet splash plymouth.ignore-serial-consoles


ID på SSD som ska ta över nät booten är klar: root=PARTUUID=df6d3ab6-02



2. Vad gör man om SD-kortet går sönder?
Det fina med din setup är att all din viktiga data ligger på SSD:n. Om SD-kortet brinner upp imorgon har du inte förlorat en enda fil från ditt projekt!

Om kortet går sönder har du bara tappat bort "nyckeln". Så här gör du en ny:

Köp ett nytt SD-kort (vilket som helst, storlek spelar ingen roll).

Sätt det i datorn och kör Raspberry Pi Imager (installera Raspberry Pi OS, precis som vi gjorde nyss).

Öppna cmdline.txt på det nya kortet.

Klistra in "den magiska raden" som pekar på din SSD.

Klart! Stoppa i och starta.

⚠️ VIKTIGT: Gör detta NU
För att kunna göra en ny nyckel i framtiden måste du komma ihåg vad din SSD heter (ID-numret) och din Quirk-fix. Om SD-kortet dör kommer du inte kunna läsa den gamla filen.

Gör så här: Kopiera textraden du precis skapade (den med df6d3ab6-02) och spara den någonstans säkert: