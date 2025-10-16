---
title: Twitch senza pubblicità
type: docs
weight: 5
---

Per eliminare la pubblicità da twitch, seguire questi passaggi descritti su questa [pagina](https://github.com/pixeltris/TwitchAdSolutions)

1. Andare sull'estensione **uBlock Origin**
2. Andare su **Preferences**
3. Spostarsi sulla scheda **My Filters** e aggiungere `twitch.tv##+js(twitch-videoad)`
4. Spostarsi sulla scheda **Settings**, attivare **I am an advanced user** e cliccare sull'icona dell'**ingranaggio** che compare.
5. Modificare il valore di **userResourcesLocation** da *unset* all'url completo della soluzione che si vuole usare (se è già presente un url, aggiungere uno spazio dopo quello esistente).  
Nel nostro caso:  
`userResourcesLocation https://raw.githubusercontent.com/pixeltris/TwitchAdSolutions/master/video-swap-new/video-swap-new-ublock-origin.js`
6. Attivare e Disattivare l'estensione o **riavviare** il browser.