# Popis projektu

Tento projekt je zameraný na vytvorenie modelu, ktorý bude schopný generovať mapy pre hru Beat Saber. Beat Saber je hra, ktorá kombinuje hudbu a šport. Hráči musia reagovať na rôzne objekty, ktoré sa im zobrazujú v rytme hudby. Hra je dostupná na platformách VR (Virtual Reality) a PC.

## Ciel

Napísať prehľad z oblasti štruktúr chart súborov v rytmických hrách, nástrojov na ich výrobu a pod.
Navrhnúť a implementovať algoritmus na automatizované vytváranie chartov
Porovnať kvalitu automaticky vytvorených chartov

# Hlavný kód projektu

https://github.com/xmasny/beatsaber-map-generator (je potrebne požiadať o prístup)

## Predbežný plán

- server setup pre trénovanie a uloženie datasetu
- špecificka analýza chartov
- presna analyza suborov levelov a info suboru (potrebne na implementovanie do hry)
- Nastavenie veľkokapacitného fakultného serveru
- Stiahnutie dát chartov a songov z verejného úložiska beatsaver.com pomocou python skriptu
- Vyfiltrovanie nepouzitelnych zvukových a map súborov
- Analýza a preprocess máp, uloženie základných objektov do osobitných súborov (kocky, steny a bomby)
- Vygenerovanie mel spektrogramu (mels=128, hop length=512, sample rate=22050) (napr. song6_2dd81.npy)
- Výpočet časovej pozície objektu na základe chart súboru
  - Prepočet beatu na sekundy a určenie najbližšieho framu
- trenovanie modelu
  - trenovanie zakladnej mapy (bez ziadnych specifickych vlastnosti)
  - trenovanie mapy s dodatocnymi objektami (bombovymi blokmi, stenami, ...)
- verejne testovanie modelu
- analýza výsledkov testovania

## Informácie o datasete

- pocet songov:  145831
- Dva priečinky data (raw dáta) a dataset (generovane a preprocesovane dáta)

![velkost datasetu](<images/velkost datasetu.png>)
![pocet map](<images/dostupne mapy.png>)
![block types](<images/block types.png>)

## Používané knižnice

- [librosa](https://librosa.github.io/librosa/)
- [numpy](https://numpy.org/)
- [matplotlib](https://matplotlib.org/)
- [seaborn](https://seaborn.pydata.org/)
- [pandas](https://pandas.pydata.org/)
- [pytorch](https://pytorch.org/)
- [wandb](https://wandb.ai/site)
- [time](https://docs.python.org/3/library/time.html)

## Odkazy na použité vedecké články a iné zdroje

- [Beat Saber](https://beatsaber.com/)
- [Beat Saber Wiki](https://bsmg.wiki/)
- [Dance Dance Convolution](https://arxiv.org/pdf/1703.06891.pdf)
- [Procedural Content Generation of Rhythm Games Using Deep Learning Methods](https://inria.hal.science/hal-03652042/document)
