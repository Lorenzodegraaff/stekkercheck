# Stekkercheck: welke stekkerbatterij past bij jouw huis?

**Gratis, open source rekenhulp voor stekkerbatterijen en thuisbatterijen in Nederland.** Beantwoord vier vragen (zonnepanelen, avondverbruik, energiecontract, woning) en zie welke capaciteit bij jouw situatie past.

👉 **Gebruik de officiële tool met volledig stekkerplan op [stekkergids.nl/stekkercheck](https://stekkergids.nl/stekkercheck/?utm_source=github&utm_medium=referral&utm_campaign=stekkercheck-oss)**

👉 **Live demo van deze open source versie: [lorenzodegraaff.github.io/stekkercheck](https://lorenzodegraaff.github.io/stekkercheck/)**

---

## Hoe werkt het?

De Stekkercheck kijkt naar twee dingen:

1. **Hoeveel zonnestroom je overdag overhoudt** (opbrengst van je panelen min je eigen verbruik overdag)
2. **Hoeveel stroom je na zonsondergang gebruikt**

De kleinste van die twee bepaalt grofweg hoe groot je batterij hoeft te zijn. Groter kopen levert weinig extra op, omdat de batterij dan zelden vol of leeg raakt.

| Aanname | Waarde |
|---|---|
| Vermogen per paneel | ≈ 400 Wp |
| Opbrengst per kWp | ≈ 2,7 kWh per dag (jaargemiddelde) |
| Avondverbruik laag / gemiddeld / hoog | 2,5 / 4,5 / 7 kWh |
| Dagverbruik laag / gemiddeld / hoog | 1,5 / 2,5 / 4 kWh |

Alle aannames staan in het object `AANNAMES` in [`index.html`](index.html). Pas ze aan en je ziet direct het effect.

### Mogelijke uitkomsten

- Een batterij loont waarschijnlijk niet (geen panelen, geen dynamisch contract)
- Stekkerbatterij van 2 tot 3 kWh
- Stekkerbatterij van ongeveer 5 kWh
- Stekkerbatterij van 5 kWh, uitbreidbaar
- Vaste thuisbatterij overwegen (warmtepomp, elektrische auto of hoog avondverbruik)

Daarbovenop krijg je tips over je energiecontract (dynamisch, vast of variabel, einde salderingsregeling op 1 januari 2027) en je woning (koop, huur of appartement).

## Gebruiken of inbouwen

Het is één HTML-bestand zonder dependencies en zonder tracking. Je antwoorden verlaten je browser niet.

```bash
git clone https://github.com/Lorenzodegraaff/stekkercheck.git
open stekkercheck/index.html
```

De rekenlogica (`berekenAdvies`) is een pure functie en ook in Node te gebruiken.

## Belangrijk

Dit is een **indicatie op basis van vuistregels**, geen persoonlijk advies. Wil je weten welk model precies past, wat hij oplevert bij jouw energieleverancier en wat de terugverdientijd is? Vraag dan een **gratis stekkerplan** aan op [Stekkergids.nl](https://stekkergids.nl/stekkercheck/?utm_source=github&utm_medium=referral&utm_campaign=stekkercheck-oss).

Stekkergids vergelijkt stekkerbatterijen op basis van fabrikantgegevens, publieke tests en eigen berekeningen. Geen installateur: twijfel je over je aansluiting, laat dan een erkende installateur meekijken.

## Over de maker

Gemaakt door **[Lorenzo de Graaff](https://lorenzodegraaff.nl)**, freelance SEO en GEO specialist uit Naaldwijk en maker van [Stekkergids.nl](https://stekkergids.nl), de onafhankelijke gids voor stekkerbatterijen en slim sturen.

- Website: [lorenzodegraaff.nl](https://lorenzodegraaff.nl)
- Stekkergids: [stekkergids.nl](https://stekkergids.nl)
- Hoe Stekkergids vergelijkt: [stekkergids.nl/zo-vergelijken-we](https://stekkergids.nl/zo-vergelijken-we/)

Verbeteringen of andere aannames? Open een issue of pull request.

## Licentie

[MIT](LICENSE) © 2026 Lorenzo de Graaff
