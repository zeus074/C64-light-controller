# C64-light-controller
PCB to control lights/loads via the Commodore 64 user port. (From '90s)

Revised schematic of the 1990s version that I used as a controller for the lights.
This version does not directly control 220v loads but you can do so by adding relays or triac boards after the outputs.

![alt text](https://github.com/zeus074/C64-light-controller/blob/main/IMG/lightscanner.jpg)

**Components:**

R1-R8	Resistors 390R
R9-R16	Resistors 1K
R17-R24	Resistors 10K (*)
R25		Resistor 100K
RN1		Resistor pack 100K (SIP9)
T1-T8	Transistors	BC547 or equivalents (*)
OK1-OK8	Optocouplers 4N35
IC1-IC2	CD4030N (Quad EXCLUSIVE-OR Gate)
LED1-8	Leds diode (3mm or 5mm whatever color you like)
SW1		Dip swirch (1 way, but are more likely to be found at two)
P1		C64 userport (24 Pin Card Edge Connector 3.96mm)
J1		Barrel power input (max 12v)
J2		Header 9pin (optional)
J3		Header 9pin (optional)

(*) R17-R24 and T1-T8 are optiona if you not need a open collector output.

**PCB**

:coffee: if you want the PCB, please support me and follow this link : <a href="https://www.pcbway.com/project/shareproject/C64_Light_controller_6453b34b.html" target="_NEW">PCBWAY!</a>

**Directory**

Schematic : Schematic file in PDF
IMG : Some pictures

**How it works**

A very simple interface in its schematic, the outputs of the C64 (user port) handle the photocouplers that provide electrical isolation of the computer from any problems on the power and control side.
The photocouplers drive transistors through an exor port to have an open collector output.
The exor chips are used exclusively to be able to reverse the signal coming from the computer via a dip switch (one is enough, but they are more easily found with two switches).
The Commodore64 to handle the outputs must first set the CIA registers to indicate whether the ports will be input/output and their value.

Example:

POKE 56579,255 Sets all 8 ports as output.
POKE 56577,1 Sets the bit0 of the user port (turns on the first LED)
POKE 56577,255 Sets all BITs of the user port (turns on all LEDs).
*Use external power max 12V!*

Video: https://youtu.be/YFYZ48ZZcqM

*Please consider subscribing to the channel*

**ITALIAN VERSION**

PCB per controllare luci o carichi tramite la porta utente del Commodore 64. (direttamente dagli anni '90)

Schema revisionato di quello fatto nel 1990 che usavo per controllare le luci.
Questa versione non controlla direttamente carichi a 220 volt ma puoi farlo aggiungendo una scheda relè o con triac.

**Componenti:**

R1-R8	Resistenze 390R
R9-R16	Resistenze 1K
R17-R24	Resistenze 10K (*)
R25		Resistenza 100K
RN1		Rete resistiva 100K (SIP9)
T1-T8	Transistors	BC547 o equvalenti (*)
OK1-OK8	Fotoaccoppiiatori 4N35
IC1-IC2	CD4030N (Quad EXCLUSIVE-OR Gate)
LED1-8	Diodi led (3mm or 5mm qualsiasi colore ti piaccia)
SW1		Dip swirch (1 via, ma si trovano più facilmente a due)
P1		C64 userport (24 Pin Card Edge Connector 3.96mm)
J1		Barrel power input (max 12v)
J2		Header 9pin (opzionale)
J3		Header 9pin (opzionale)

(*) R17-R24 e T1-T8 sono opzionali se non utilizzi l'uscita open collector.

**PCB**

:coffee: Se ti occorre il PCB, supporta questo lavoro prendendolo a questo link : <a href="https://www.pcbway.com/project/shareproject/C64_Light_controller_6453b34b.html" target="_NEW">PCBWAY!</a>

**Directory**

Schematic : File dello schema in PDF
IMG : Alcune foto

**Come funziona**

Il funzionamento dell'interfaccia è sempliice, le uscite del C64 (porta utente) comandano dei fotoaccoppiatori che provvedono ad isolare elettricamente il computer da qulsiasi problema sulla linea di potenza e controllo.
I fotoaccoppiatori comandano tramite delle porte exor i transistor per avere un'uscita open collector.
Le porte exor csono usate per invertire il segnale del computer (in alcuni programmi si utilizzavano uscite negate) tramite il dip switch (basta un solo contatto, ma è più facile trovarli con 2 o più).
Il Commodore64 per controllare le uscite deve settare prima i registri del CIA e specificare quale porta sarà un ingresso o uscita e lo stato.

Esempio:

POKE 56579,255 	Imposta tutte le 8 porte come uscite.
POKE 56577,1 	Imposta il bit0 della porta utente (accende il primo LED)
POKE 56577,255 	Imposta tutti i bit della porta utente (accende tutti i LEDs).
*Utilizza un'alimentazione esterna per alimentare la scheda, massimo 12V!*

Video: https://youtu.be/YFYZ48ZZcqM

*Se ti piacciono questi lavori, supportaci iscrivendoti al canale*
