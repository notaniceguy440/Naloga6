# ImplicitIntents

Android aplikacija za prikaz uporabe **implicitnih namenov**. Omogoča odpiranje spletne strani, prikaz lokacije na zemljevidu in deljenje besedila z drugimi aplikacijami.

## Funkcionalnosti

| Gumb | Akcija | Opis |
|---|---|---|
| **Open Website** | `Intent.ACTION_VIEW` | Odpre vneseni spletni naslov v brskalniku |
| **Open Location** | `Intent.ACTION_VIEW` | Prikaže lokacijo na zemljevidu (`geo:0,0?q=lokacija`) |
| **Share This Text** | `ShareCompat.IntentBuilder` | Deli besedilo z MIME tipom `text/plain` |

## Delovanje

Uporabniški vmesnik je zgrajen z navpičnim **LinearLayout**, ki vsebuje tri vnosna polja in tri gumbe. Pred zagonom namena aplikacija z metodo **resolveActivity()** preveri, ali je na napravi nameščena aplikacija, ki lahko namen obdela. Tako se aplikacija ne sesuje, če take aplikacije ni.

Za sprejemanje povezav mora sprejemna aplikacija v datoteki **AndroidManifest.xml** definirati `intent-filter` z akcijo VIEW, kategorijama DEFAULT in BROWSABLE ter podatkovnim filtrom za shemo in gostitelja.

## Tehnologije

**Java**, **Android SDK**, **AndroidX**, **Android Studio**
