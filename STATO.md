# STATO dronisoftair (Skyfire) - aggiornato 12/11/2026 sera

Sito online: https://cialdecompatibili-netizen.github.io/dronisoftair/
Cartella locale: Desktop\repository\dronisoftair

## Cosa c'e'
- Sito softair con droni: negozio, categorie, sottocategorie (VTOL, carico, lavoro, ecc.), home e guide.
- Brand provvisorio "Skyfire": esiste gia', va sostituito appena decidi il nome.
- `listino-softair.md`: listino softair ispirato ai droni reali (fibra ottica, intercettori, difesa, sciami ESP32+LoRa, guida AI, VTOL, jet EDF, benzina).
  - Sezione nuova **Scheda tecnica Turbo T1**: turbina RC vera a kerosene, pezzi commerciali, 3 versioni (Race 80 N, Pro 100 N, Max 150 N).
  - Prezzi turbine JetCat dai siti ufficiali (P80-SE 1.899 EUR, P100-RX 2.449 EUR). Il resto (cellula, prezzo di vendita 5.500-8.500 EUR) sono stime nostre.
- `listino-concorrenza.md`: DJI, Autel, Potensic, Parrot, VTOL e carico/agricoltura (sezioni 7 e 11).

## Foto
- Online: 23 foto prodotti. Mancano **26 prodotti senza foto** (turbo-t1, vtol-v5/v6/v7, kit-sciame-vtol, fibra-long-f3, bobina-fibra, valigia, eliche, batteria-ala, jet-j1-target, piston-p1, cruiser-l2-piston, catapulta, gancio-doppio, aliante-a2-color, gilet, occhiali, reti, lock-on, intercept-ai, nodo-arbitro, swarm-node, batterie-caricatore, tuta-bianca-squadra).
- Script lanciato alle 23:36: `Desktop\claudetemp\foto3.py`. Aspetta il reset dell'account 3 (23:56), genera i 26 prodotti, copia le foto in `assets/images/prodotti`, aggiorna `immagine` in `_data/catalogo.json` e fa il push.
- Log: `Desktop\claudetemp\foto3.log` (alla fine scrive quali foto sono mancate). Da controllare domani: non so se e' finito.
- Crediti Gemini alle 23:36: account 1 = 0 (reset 00:31), account 2 = 25 (reset 00:54), account 3 = 0 (reset 23:56). Circa 22 crediti a foto, 600 a finestra.

## Da fare domani
1. Leggere `foto3.log` e vedere quali foto sono uscite e quali mancano.
2. Guardare le foto a occhio: imbuto sulla fibra (non il filo da pesca), ugello visibile sul Turbo T1, struttura VTOL con 4 rotori verticali + 1 spingente. Rigenerare quelle sbagliate.
3. Rigenerare le mancanti dopo i reset (account 1 dalle 00:31, account 2 dalle 00:54).
4. Scegliere il nome del brand al posto di Skyfire e fare il rename.
5. Fornitori e prezzi reali: oggi sono tutti target indicativi.
6. Regole da verificare prima di vendere: ENAC (droni con carico, ala fissa, turbine), regole softair, lanciatore pallini sul drone, colorante dei pallini, assicurazione.

## Cose che funzionano
- Generare un lotto di foto con un account fisso: `GEMINI_ACCOUNT=3 GEMINI_FISSO=1`, poi `python gemini_auto\img.py --lista <file.json> --out <cartella>` (voci con id, soggetto, profilo "prodotto").
- Prima di lanciare: `img.py --crediti` per ogni account. Sotto circa 22 crediti non partire.
- Nei prompt di foto descrivere l'oggetto reale (fibra: bobina cilindrica con ugello a imbuto; VTOL: due travi con 4 rotori verticali + spingente posteriore; turbina: ugello posteriore, nessuna elica).
- La cronologia della chat e' in `Desktop\claudetemp\data\chat_precedente.txt`.
