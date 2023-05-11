# Popis projektu

Tento projekt je zameraný na vytvorenie modelu, ktorý bude schopný generovať mapy pre hru Beat Saber. Beat Saber je hra, ktorá kombinuje hudbu a šport. Hráči musia reagovať na rôzne objekty, ktoré sa im zobrazujú v rytme hudby. Hra je dostupná na platformách VR (Virtual Reality) a PC.

# Hlavný kód projektu

https://github.com/xmasny/beatsaber-map-generator (je potrebne požiadať o prístup)

## Predbežný plán

- [x] vytvoriť repozitár na github-e pre kód
- [x] vytvoriť repozitár na github-e pre diplomovú prácu
- [x] vytvoriť script na stiahnutie a rozbalenie datasetu
- [x] vypočítať tempo estimation a overiť či je správne
- [ ] overiť či je dostupný server na trénovanie s vysokým uložiskom cca 1-2TB
- [ ] [pytorch tutorial](https://youtu.be/V_xro1bcAuA)
- [ ] server setup pre trénovanie a uloženie datasetu
- [ ] špecificka analýza chartov
- [ ] presna analyza suborov levelov a info suboru (potrebne na implementovanie do hry)
- [ ] vytvorenie JSON struktury pre overovanie vyslednych suborov
- [ ] trenoovanie modelu
  - [ ] trenovanie zakladnej mapy (bez ziadnych specifickych vlastnosti)
  - [ ] trenovanie mapy s dodatocnymi objektami (bombovymi blokmi, stenami, ...)
  - [ ] trenovanie mapy s svetelnymi efektami
- [ ] verejne testovanie modelu
- [ ] analýza výsledkov testovania

## Používané knižnice

- [librosa](https://librosa.github.io/librosa/)
- [numpy](https://numpy.org/)
- [matplotlib](https://matplotlib.org/)
- [seaborn](https://seaborn.pydata.org/)
- [pandas](https://pandas.pydata.org/)
- [pytorch](https://pytorch.org/)
- [wandb](https://wandb.ai/site)
- [time](https://docs.python.org/3/library/time.html)
