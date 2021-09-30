# Aplikace neuronových sítí 2021

## Instalace

Úlohy jsou připravené ve formě jupyter notebooků jazyka Python 3.x především s využitím knihoven numpy, matplotlib a PyTorch.

### Vlastní stroj

Pokud máte k dispozici vlastní PC či notebook, nejlépe s NVIDIA GPU, nejspolehlivější cesta, jak vše zprovoznit kompatibilně s materiály předmětu, je následující postup.

0. [Instalace toolkitu NVIDIA CUDA 11.x](https://developer.nvidia.com/cuda-downloads).
  - Tento krok je sice nepovinný, avšak doporučený, jelikož výrazně urychlí práci především s konvolučními sítěmi.
1. [Instalace 64-bitové 3.x verze distribuce Anaconda (Individual)](https://www.anaconda.com/products/individual).
  - Pokud Anacondu s nikým nesdílíte, jednodušší je instalace na úrovni uživatele.
  - Jestliže nezvolíte přidání spustitelných skriptů Anacondy do standardních cest, je potřeba po instalaci spustit Anaconda Prompt a zadat příkaz `conda init`, aby bylo možné ji používat i z běžného příkazového řádku (`cmd.exe`). V opačném případě bude pro práci vždy nutné spouštět Anaconda Prompt, která všechny potřebné cesty již obsahuje.
2. Instalace potřebných balíků do virtuálního prostředí Anacondy.
- Spusťte příkazový řádek z adresáře obsahujícího soubor `environment.yml` a zadejte `conda env create -f environment.yml`. Příkaz vytvoří  virtuální prostředí Anacondy s názvem `ans21zs`.
- Aktivujte virutální prostředí `ans21zs` příkazem `conda activate ans21zs`. Tento příkaz bude nutné zadat po každém otevření nového příkazového řádku a vždy, kdy budeme chtít pracovat v tomto prostředí.
3. Přidání kernelu `ans21zs` do jupyterlabu.
  - V aktivovaném prostředí zadejte `python -m ipykernel install --user --name ans21zs`.
  - Po spuštění notebooku se vždy přes tlačítko "Python 3" vpravo nahoře ujistěte, zda opravdu běží nad kernelem `ans21zs`.

### Google Collaboratory

Využít lze rovněž službu Google Collaboratory, která na omezenou dobu (až 12 hod.) umožňuje spuštět jupyter notebooky i s grafickou akcelerací. Kromě HW zdarma služba navíc obsahuje předinstalované všechny balíky, které jsou pro předmět potřeba. **Avšak pozor: po vyčerpání času se notebook odpojí a neuložená práce je ztracena.**

## Úlohy

- Za vypracování každé úlohy je možné získat 10 bodů. Bodování jednotlivých dílčích částí je uvedeno v popisu.
- Je možné získat i další plusové body za nadstandardně vypracovanou úlohu.
- Úlohy se dělí na povinné a bonusové. Povinné úlohy musejí být splněny alespoň za 5 bodů (tj. 50 %). 
- **Odevzdání úlohy po termínu je penalizováno odečtením 5 bodů!**
- Kopírování kódu bude penalizováno odečtením 1 bodu oběma odevzdávajícím, tedy i originálu, a to i opakovaně. Pokud např. budou odevzdány 3 stejné kopie jednoho kódu, každé z nich budou odečteny 2 body! Rozmyslete si tedy pořádně, zdali vypustíte svoje řešení úlohy "do světa".
- Zcela či z podstatné části zkopírovaná úloha nebude uznána vůbec.

### 1. Lineární klasifikace
- Notebook: [linear-classification.ipynb](linear-classification.ipynb)
- Bodování:
  - Softmax s validačním skóre > 20 %: 5 bodů
    - Validační skóre > 30 %: +1 bod
  - SVM: 3 body
    - Validační skóre > 30 %: +1 bod
- **deadline: 20.10.2021 7:59**