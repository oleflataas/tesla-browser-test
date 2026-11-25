# Tesla-nettlesertest

En statisk side som måler hva Tesla-nettleseren støtter. Den er etappe 0 i `TESLA_CARPLAY_RESEARCH.md`:

- WebCodecs H.264 og H.265
- sikker kontekst (HTTPS)
- viewport og skjermstørrelse
- bildefrekvens
- berøring og multitouch
- Web Audio

Siden må serveres over **HTTPS**. Ellers mangler WebCodecs, og resultatet blir misvisende.

## Publisere på GitHub Pages

Gratis Pages krever et offentlig repo. Siden inneholder ingen personopplysninger.

```powershell
cd C:\Claude\prosjekter\Teslacarplay\tesla-browser-test
gh repo create tesla-browser-test --public --source . --push
gh api -X POST repos/{owner}/tesla-browser-test/pages -f "source[branch]=main" -f "source[path]=/"
```

Etter et minutt eller to er siden på `https://<github-bruker>.github.io/tesla-browser-test/`.

## Bruk i bilen (parkert)

1. Åpne adressen i Tesla-nettleseren.
2. Berør feltet til høyre: alle fire hjørner, midten, draing og to fingre.
3. Trykk «Spill testtone» og noter om du hører den.
4. Ta bilde av skjermen, eller bruk «Kopier resultat».
5. Noter MCU (Intel/AMD) og programvareversjon fra Kontroller → Programvare.
6. Gjenta etter hver Tesla-programvareoppdatering.
