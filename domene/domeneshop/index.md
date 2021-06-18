# Domeneshop: Hvordan koble opp domene mot din nettbutikk


Før du logger inn på domeneshop så finner du ditt midlertidige domenenavn du har fått fra oss.
Dette er adressen du bruker for å se din demobutikk i dag: f.eks: https://`s1234.srv7.snartonline.no`

Uthevet del, altså `sc1234.srv7.snartonline.no` er ditt midlertidige domenenavn.

1. Logg deg inn på domene.shop/login
2. Trykk på **Mine domener** og deretter på ønsket domene.
3. Trykk på fanen **DNS-pekere**, og deretter på **Vis avanserte innstillinger**
4. Du skal opprette 3 pekere og du må trykke på lagre (grønn hake til høyre) for hver linje i skjemaet. (Du må lagre en og en peker - det går ikke an å fylle inn mange på en gang og lagre.)
5. Send en epost til [vår utvikler](mailto:mads@komplettnettbutikk.no?subject=Nettbutikkens+nye+domene) for å gi beskjed om hvilket domene du skal benytte.

Når du er ferdig med å sette opp pekerne så tar det litt tid før det er oppdatert i DNS-systemet. 

### Peker 1
- **Vertsnavn:** skal være blank 
- **TTL:** `5 min`
- **RR-type:** `ANAME`, 
- **Data:** ditt midlertidige domene, f.eks. `sc1234.srv7.snartonline.no`


### Peker 2
- **Vertsnavn:** _www_
- **TTL:** _5 min_ 
- **RR-type:** _CNAME_	        
- **Data:** ditt midlertidige domene, f.eks. `sc1234.srv7.snartonline.no`

### Peker 3
- **Vertsnavn:** skal være blank
- **TTL:** `5 min`
- **RR-type:** `TXT`
- **Data:** "v=spf1 a mx include:\_spf.domeneshop.no include:\_spf.snartonline.no ~all"

_PS: Hermetegnene må være med._



[Trykk her for å se et eksempel på ferdig oppsett](/domene/domeneshop/eksempel.png)


**PS:** Dersom du synes dette er vanskelig, eller allerede har domeneoppsett mot en annen nettside, epost eller liknende kan du ta kontakt med oss for hjelp til riktig oppsett. Dette er kostnadsfritt for førstegangsoppsett. Send i såfall din innloggingsinformasjon og ønsket domenenavn til  [vår utvikler](mailto:mads@komplettnettbutikk.no?subject=Domeneoppsett)
