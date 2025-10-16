---
title: Nhentai
type: docs
weight: 3
---

## Problemi di cookie

Se si scaricano troppi hentai si va incontro ad un problema di cookie.

Per [evitarlo](https://github.com/RicterZ/nhentai/blob/master/README.rst) bisogna impostare l'user agent e i cookie, questultimo composta da
- csrftoken
- sessionid
- cf_clearance.

Questi tre sono identificabili tramite il *Development Tool* dopo aver effettuato l'accesso su [nhentai.net](https://nhentai.net/):

- Username: `not_a_rifle`
- Password: `Bucatini_1`

Ecco dove trovare i componenti dei cookie:  
- csrftoken: Settings → More Tools → Web Developer Tools → Storage → Cookie → csrftoken
- sessionid: Settings → More Tools → Web Developer Tools → Storage → Cookie → sessionid
- cf_clearance: Settings → More Tools → Web Developer Tools → Network → nhentai.net → Headers → cf_clearance
- useragent: cercare su google “my user agent”

Questi sono quelli attualmente impostati:

nhentai --useragent "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:134.0) Gecko/20100101 Firefox/134.0"

nhentai --cookie "csrftoken=6Lw9o745l1CTq0QoMkywfgSKbbAp2nSn; sessionid=zt59ib12sttzfr6dpsv7i9pp0kkur8wm; cf_clearance=1lRAjMJZn1JkWGFRPweHgvcm7oN3KR2HCeiLprTbz6Y-1738402507-1.2.1.1-PScXxGYmIuJ1hMLjRNkQ.k1X5xmcWZny5flckcyD4KKsUOSAsXzYi0Qwq67XsfHswwPQHcDDSYz_LRuGYyhCYXOMLYZXYZFv7o6T61UJkW3PQ172T8dTR2.kVxkZ7Lf2mEFH0trEs1TwhnzRQYg0riwrra_ER2DHzF1Q4G4N.Q4jCEK4HtcxhLf7k2zCUHZg7O29Cwbu.uNnZF.wTnlEdZXi3fRebc8YSW.oeWvta7GjmJ_g.e5GnkqQHIodNLIpyjIyPrmwk3cBQB1LU5_VHssfJ5VgETX1nCrxu.SygEEPn4VaJ06okTHfwswVVvXpLd0NBZFMGe8IUBLxzamf1Q"

## Comando download multipli

Per scaricare più hentai in un colpo solo:
- scrivere il loro numero nel file `lista_numeri.txt`
- aprire il terminale al percorso in cui si trova il file
- lanciare questo comando da terminale:
  ```
  for item in $(cat lista_numeri.txt); do
    echo "Processing $item"
    nhfunction $item
  done
  ```