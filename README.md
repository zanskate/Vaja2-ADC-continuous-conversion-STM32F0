# Vaja2-ADC-continuous-conversion-STM32F0
kontinuirana ADC pretvorba z STM32F0
------------------------------------------------------------------------------------------------------------------------------------
ODGOVORI:
a) Glede na vašo razvojno ploščico in razširitveno vezje z tipkami ter potenciometri, izberite ustrezni
analogni vhod. Kateri pin je to? PCO
b) Glede na potenciometer na vaši ploščici izberite-obkljukajte ustrezni kanal/pin. Na zaslonu se vam mora usterzno pobarvati izbrani pin v zeleno barvo. Kaj se izpiše poleg pina? ADC_IN10
c) V Clock Configuration spremenimo APB1 peripheral clock (MHz) na 16
MHz. Kaj opazite? PCLK1 (48MHz max)
d) Clock Prescaler nastavimo z deliteljem 4. Kolikšna je sedaj preskalirana frekvenca takta fpreskalirana ? 
4MHz =(16MHz/4)
e) Sampling time (čas vzorčenja tvz_ciklih ) spremenite na 239.5 cikov. Pravi čas vzorčenja se nato poveča še za 12 ciklov. Koliko znaša pravi čas vzorčenja tvz v mikro sekundah?
(enačba: tvz =tvz_ciklih /fpreskalriana )? 62.875µs
----------------------------------------------------------------------------------------------------------------------------------
KOMENTAR:
S pomočjo potenciometra in ADC pretvornika smo naredili program, ki nam izpisuje vrednost na potenciometru. S pomočjo Debug mode v μVision5 smo lahko na računalniku opazovali to vrednost. Pretvorba je 8 bitna, kar nam omogoča, da izpisuje vrednosti od 0 do 254. Pri nas nam vrne najvišjo vrednost od 0 do 252 (slabši stik na potenciometru). Delovanje je podobno Vaji 1, le da je pri Vaji 2 uporabljena Continuous Conversion Mode namesto Single Conversion Mode. Takšna pretvorba je primerna za hitro in nenehno branje vhodne vrednosti.
