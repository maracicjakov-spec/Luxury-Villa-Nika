# Villa Nika — demo web

Jednostranična stranica (`index.html`, inline CSS/JS), jezici **EN / HR / DE / IT** (EN u markupu, `HR`/`DE`/`IT` rječnici — 204 ključa, paritet provjeren skriptom).

## Struktura
- `index.html` — sve; `CONFIG` na vrhu skripte
- `images/<ime>-{640,1280,1920}.webp` — 29 fotografija (isti set kao na Contessa / Airbnb oglasu); `og-image.jpg` 1200×630
- `fonts/` — Fraunces (roman + italic) i Hanken Grotesk, self-hosted (latin + latin-ext → č ć ž š đ rade)
- `_src/` — originalne JPG fotke (ne deploya se, vidi `.vercelignore`)
- `favicon.svg`, `vercel.json` (cache za slike/fontove)

## Prije objave
1. **`CONFIG.inquiryEmail`** — prazno = demo (forma validira, ali pokaže "demo verzija — upiti se još ne šalju"). Upisati e-mail → upiti idu preko FormSubmit (prvi upit traži potvrdu na tom mailu). Mail stiže na hrvatskom, s jezikom gosta.
2. Domena `villa-nika-krk.vercel.app` je placeholder (canonical, og:image, JSON-LD).
3. Dopuštenje vlasnika / agencije za fotografije i tekst.

## Izvori (listopad 2026.)
- contessa-villas.com — Luxury Villa Nika (HR / EN / DE stranica); IT preveden ručno
- Airbnb oglas 32174938 (isti oglas, Contessa d.o.o.) — fotografije u većoj rezoluciji (Contessa daje samo 5 fotki u 1200 px, ostale 600 px)

**Korišteno (provjereno u izvorima):** Kras, otok Krk (općina Dobrinj), najviše naselje na Krku · 5* · 160 m² · 6+2 osobe (do 8) · 3 spavaće sobe na 1. katu: 2 s bračnim krevetom + dječja s 2 kreveta na kat (4 os.), sve s vlastitom kupaonicom · prizemlje: kuhinja s blagovaonicom, dnevni boravak, dodatna kupaonica (ukupno 4) · konoba → sauna i mini teretana · bazen s ležaljkama, vanjski roštilj, natkrivena terasa, vrt, dječje igralište · klima, Wi-Fi, SAT TV, perilica posuđa/rublja, pećnica, mikrovalna, hladnjak, zamrzivač, aparat za kavu, kuhalo, toster, glačalo, posteljina i ručnici, alarm · parking za 2 auta ispred vile · 1 ljubimac 15 €/dan · polog 500 € gotovina · prijava od 16 h, odjava do 10 h · noćni mir 22–08 · bez zabava · režije uključene · more 7 km (~10 min autom), znamenitosti ~15 min, trgovina/centar < 200 m, restorani < 5 km, aerodrom Rijeka 10 km+ · Vrbnik i žlahtina.
Koordinate: 45.10928, 14.59574.

**Namjerno izostavljeno:**
- Cijene (Contessa je imala samo rujan 2026., 1.764–2.471 €/tj.) — upit ih traži.
- Airbnb ocjena 4,8 (samo 5 recenzija) i recenzije.
- Kamin — vidi se na fotki, ali nije naveden u opisu.
- Kontakt agencije Contessa (stranica je za vlastiti upit).
- "Dan u Villi Nika" opisuje korištenje stvarnih sadržaja; sati su ilustrativni.

## Dizajn
Krčki vapnenac `#F4EEE3`, maslinasta `#2F3A24`, zelena škura `#5E8A63`, cigla `#A04F36`, konoba `#1B1712` + jantar `#E2A764`.
Potpis: sekcija **"Dan u Villi Nika"** — na desktopu se zakači (sticky) i scrollom vodi vodoravno od 08:00 do 22:00; sunce putuje po liniji, pozadina prelazi iz jutra u sumrak i noć. Na mobitelu je swipe karusel. Konoba kao tamna sekcija "Nekad / Danas".

## QA (15. 10. 2026.)
Lighthouse mobile: Accessibility / Best Practices / SEO 100 · LCP 1,0 s (4× CPU, Fast 4G) · CLS 0 · bez horizontalnog overflowa 320–1280 px u sva 4 jezika · bez grešaka u konzoli · forma (validacija + demo poruka), lightbox, izbornik i promjena jezika testirani u pregledniku.
