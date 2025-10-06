# Informe tècnic i web: TecnoGestió S.L.  

**Autor:** Oscar Fernandez  
**Departament:** SMX2  

---

## 1. Selecció d'un SAI

### Inventari d'equips

| Dispositiu              | Quantitat | Consum (W) | Comentaris                             |
|-------------------------|-----------|------------|----------------------------------------|
| Ordinador de sobretaula | 4         | 250 W      | Inclou monitor de 22” (~50 W)          |
| Impressora multifunció  | 1         | 30 W       | Només si cal guardar treballs crítics  |
| Router Wi-Fi            | 1         | 15 W       | Ha de romandre actiu                    |

**Potència total estimada:** 1045 W → amb reserva 20%: 1254 W → ≈ 1568 VA  
**Conclusió:** SAI mínim **1600 VA / 1250 W**  

**Autonomia requerida:** 10 minuts, suficient per desar treballs i apagar equips.

### Models considerats

| Model                         | Potència (W) | Autonomia (min) | Sortides | Preu (€) |
|-------------------------------|--------------|----------------|----------|-----------|
| APC Back-UPS Pro 1500VA       | 865          | 10             | 10       | 250       |
| Eaton 5P 1550VA               | 1100         | 12–15          | 8        | 400       |
| CyberPower CP1500EPFCLCD      | 900          | 8–10           | 12       | 220       |

**Selecció final:** **Eaton 5P 1550VA**  
**Justificació:** Combina potència suficient, autonomia adequada i fiabilitat professional.  

---

## 2. Hosting i web

**Cas:** Blog informatiu / revista digital amb articles, podcasts i vídeos  
**Tràfic inicial:** 1.000–5.000 visites/mes, creixement moderat  
**Ubicació lectors:** majoritàriament Amèrica Llatina (Espanya 20%)  
**Altres requeriments:** amplada de banda per streaming, còpies de seguretat freqüents, panell fàcil, domini .com, cost moderat, suport en espanyol, escalabilitat  

### Taula comparativa hosting

| Criteri           | Webempresa         | Raiola Networks      | SiteGround             | Aruba.it             |
|------------------|-----------------|-------------------|---------------------|------------------|
| Preu 1r any/renov.| 79 €/149 €       | 7,95 €/mes (~95 €/any) | 3,99–17,99 €/mes (~215 €/any) | 29–79 €/any |
| Espai de disc     | 11 GB NVMe       | 10 GB SSD          | 10 GB SSD           | 20 GB SSD          |
| Visites           | fins 30.000/mes  | no especificat     | fins 10.000/mes     | sense límit       |
| CPU/RAM           | 1 vCPU / 1,5 GB  | 100% quota / 1 GB  | compartit optimitzat WP | no publiquen     |
| Ubicació          | Espanya/UE       | Madrid (ES)        | Madrid (ES)         | Europa             |
| Seguretat/backups | SSL, backups cada 4 h, CDN | SSL, Imunify360, backups | SSL, backups diaris, CDN | SSL, backups diaris |
| Escalabilitat     | WordPress + Cloud| VPS, Elàstic       | GrowBig/GoGeek, Cloud| upgrade fàcil      |
| Suport            | 24/7 ES          | 24/7 telèfon ES    | 24/7 ES             | 24/7 IT/EN         |

**Recomanació:** **Webempresa (WordPress Inicio)**  
- Backups cada 4 h, CDN, fàcil d’usar  
- Escalable i amb suport en espanyol  
- Espai limitat (11 GB) → es pot ampliar amb emmagatzematge extern per podcasts/vídeos  

---

## 3. Naming i validació

**Proposta:** Revista digital sobre l’art de col·leccionar taps de suro  
**Propostes de nom:** CorkMag, TapArt, RevistaDelSuro  

### Validació del ChatGPT


### Checklist resumida

| Nom             | Puntuació | Comentari                        |
|-----------------|-----------|----------------------------------|
| CorkMag         | 88/100    | Internacional i modern           |
| TapArt          | 78/100    | Curt però ambigu                 |
| RevistaDelSuro  | 72/100    | Clar però local                  |

**Elecció final:** **CorkMag** → creixement i atractiu global
