# Krumpir&Co — redizajn web stranice

Moderna, responzivna stranica za **Krumpir&Co** (domaći punjeni krumpiri, Zagreb),
u dvije povezane stranice:

- **`index.html`** — početna (marketing): hero, priča, sastojci, koraci „kako naručiti", kontakt.
- **`menu.html`** — cijeli meni (Spuds + pića) s košaricom; narudžba se šalje na **WhatsApp**, **e-mail** ili **telefon**.

Bez frameworka i buildanja — radi odmah u pregledniku i na GitHub Pages.

## Sadržaj mape

```
index.html          # početna stranica
menu.html           # meni + košarica + slanje narudžbe
images/
  logo.png, cover.jpg, krumpir-1..3.jpg   # početna
  menu/beans.avif, chilli.avif, beef.avif,
       pork.avif, chicken.avif, tzatziki.png   # jela na meniju
```

## Objava na GitHub Pages

1. Prenesi sve iz ove mape (`index.html`, `menu.html`, mapa `images/`) u novi repozitorij.
2. **Settings → Pages → Source:** grana `main`, mapa `/ (root)`, spremi.
3. Stranica je na `https://<korisnicko-ime>.github.io/<repo>/`.

## Kako radi narudžba

1. Svi gumbi **„Naruči odmah / Pogledaj meni"** vode na `menu.html`.
2. Na meniju kod svakog artikla je **„Dodaj +"** → ide u košaricu (gumb dolje desno).
3. U košarici se mijenja količina i vidi zbroj → **Nastavi na narudžbu**.
4. Unesu se dostava/preuzimanje, adresa, kontakt i način plaćanja.
5. **Pošalji narudžbu** → ponudi tri kanala: **WhatsApp**, **e-mail** ili **poziv**.

> ⚠️ **Plaćanje:** pravo online naplaćivanje kartice (novac odmah) nije moguće na čistoj
> GitHub stranici bez servera i platnog procesora (npr. Stripe/Monri). Zato je plaćanje
> **karticom ili gotovinom pri dostavi/preuzimanju**, a narudžba stiže na WhatsApp/e-mail.

## Što uređivati (na vrhu `<script>` u `menu.html`)

- **Meni i cijene** — polja `SPUDS` i `PICA` (cijene u eurima).
- **Trošak dostave** — `DELIVERY_FEE` (0 = besplatno) i `FREE_OVER` (besplatno iznad iznosa).
- **WhatsApp broj** — `WHATSAPP` (bez „+", npr. `385955368390`); **e-mail** — `EMAIL`.
- Tekst, adresa, radno vrijeme i kontakt su obični tekst u `index.html` / `menu.html`.

## Boje i fontovi

- Boje: krem `#F7F1E3`, tamna `#1C1815`, terakota `#C4502E`, jantar `#E0982E`.
- Fontovi: Bricolage Grotesque (naslovi) + Instrument Sans (tekst), Google Fonts.
