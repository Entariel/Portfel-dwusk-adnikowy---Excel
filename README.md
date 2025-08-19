# Two-Asset Portfolio Analysis

## English Version

### Overview

This repository contains an Excel-based analysis of a two-asset portfolio, focusing on portfolio optimization using historical stock price data. The project initially considers three Polish gaming companies: CDR (CD Projekt), Bloober Team (BLO), and 11 bit studios (11B). After analyzing correlations, the pair with the lowest correlation (CDR and BLO) was selected to construct an efficient portfolio, demonstrating portfolio theory concepts such as diversification and risk-return tradeoff.

### Project Description

The goal of this project is to practice financial data analysis and portfolio optimization. The Excel file includes:
- Weekly closing prices for CDR, BLO, and 11B.
- Calculation of weekly returns, mean returns, variance, standard deviation, and correlation matrix.
- Selection of CDR and BLO as the two-asset portfolio due to their lower correlation (0.138), which enhances diversification.
- Portfolio optimization to find the efficient portfolio with weights that minimize risk or maximize the Sharpe ratio.
- Results include expected return, portfolio risk, and Sharpe ratio for various weight combinations.

### File Structure

- **Portfel_dwuskładnikowy.xlsx**: The main Excel file with the following sheets:
  - **cdr_w**: Weekly closing prices for CDR.
  - **blo_w**: Weekly closing prices for BLO.
  - **11b_w**: Weekly closing prices for 11B (used for initial correlation analysis).
  - **Portfel**: Main analysis sheet containing:
    - Weekly returns for all three assets.
    - Summary statistics (mean, variance, standard deviation).
    - Correlation matrix to identify the least correlated pair (CDR and BLO).
    - Portfolio metrics (expected return, risk, Sharpe ratio) for various CDR-BLO weight combinations.
    - Solver setup for optimizing portfolio weights.

### Methodology

1. **Data Collection**: Weekly closing prices for CDR, BLO, and 11B, spanning August 23, 2015 to August 17, 2025 (10 years).
2. **Correlation Analysis**: Calculated Pearson correlations to select the pair with the lowest correlation (CDR and BLO at 0.138).
3. **Portfolio Construction**:
   - Weekly returns: `(Current Price - Previous Price) / Previous Price`.
   - Portfolio expected return: Weighted average of individual asset returns.
   - Portfolio variance: `w1² * var1 + w2² * var2 + 2 * w1 * w2 * cov12`.
   - Risk: Standard deviation (square root of portfolio variance).
   - Sharpe ratio: `(Portfolio Return - Risk-Free Rate) / Portfolio Std Dev` (risk-free rate assumed 0 for simplicity).
4. **Optimization**: Used Excel Solver to find optimal weights for CDR and BLO, resulting in ~59.2% CDR and ~40.8% BLO.

### Key Results

- **Correlation Matrix**:
  |       | CDR   | BLO   | 11B   |
  |-------|-------|-------|-------|
  | CDR   | 1     | 0.138 | 0.281 |
  | BLO   | 0.138 | 1     | 0.213 |
  | 11B   | 0.281 | 0.213 | 1     |

- **Asset Statistics**:
  | Asset | Mean Weekly Return | Std Dev | Variance |
  |-------|--------------------|---------|----------|
  | CDR   | 0.00618            | 0.05974 | 0.00357  |
  | BLO   | 0.00710            | 0.07592 | 0.00576  |
  | 11B   | 0.00358            | 0.05835 | 0.00340  |

- **Optimal Portfolio (CDR + BLO)**:
  - Weights: ~59.2% CDR, ~40.8% BLO.
  - Expected Weekly Return: ~0.655%.
  - Risk (Std Dev): ~5.01%.
  - Sharpe Ratio: ~0.131.

### How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/two-asset-portfolio.git
   ```
2. Open `Portfel_dwuskładnikowy.xlsx` in Microsoft Excel.
3. Review the **Portfel** sheet for calculations and results.
4. To replicate optimization:
   - Enable Excel's Solver add-in (File > Options > Add-ins).
   - Go to Data > Solver and maximize the Sharpe ratio or minimize risk, ensuring weights sum to 1 and are non-negative.
5. Extend the analysis by adding new price data.

### Requirements

- Microsoft Excel (with Solver add-in enabled).

---

# Analiza Portfela Dwuskładnikowego

## Wersja Polska

### Przegląd

To repozytorium zawiera analizę portfela dwuskładnikowego przeprowadzoną w pliku Excel, skupiającą się na optymalizacji portfela z wykorzystaniem historycznych danych cen akcji. Projekt początkowo uwzględnia trzy polskie spółki gamingowe: CDR (CD Projekt), Bloober Team (BLO) oraz 11 bit studios (11B). Po analizie korelacji wybrano parę o najniższej korelacji (CDR i BLO), aby zbudować portfel efektywny, demonstrując koncepcje teorii portfela, takie jak dywersyfikacja i relacja ryzyko-zwrot.

### Opis projektu

Celem projektu jest praktyczne zastosowanie analizy danych finansowych i optymalizacji portfela. Plik Excel zawiera:
- Tygodniowe ceny zamknięcia dla CDR, BLO i 11B.
- Obliczenie tygodniowych stóp zwrotu, średnich zwrotów, wariancji, odchylenia standardowego i macierzy korelacji.
- Wybór CDR i BLO jako portfela dwuskładnikowego ze względu na niską korelację (0,138), co poprawia dywersyfikację.
- Optymalizację portfela w celu znalezienia efektywnego portfela z wagami minimalizującymi ryzyko lub maksymalizującymi wskaźnik Sharpe’a.
- Wyniki obejmują oczekiwany zwrot, ryzyko portfela i wskaźnik Sharpe’a dla różnych kombinacji wag.

### Struktura pliku

- **Portfel_dwuskładnikowy.xlsx**: Główny plik Excel z następującymi arkuszami:
  - **cdr_w**: Tygodniowe ceny zamknięcia dla CDR.
  - **blo_w**: Tygodniowe ceny zamknięcia dla BLO.
  - **11b_w**: Tygodniowe ceny zamknięcia dla 11B (użyte do początkowej analizy korelacji).
  - **Portfel**: Główny arkusz analizy zawierający:
    - Tygodniowe stopy zwrotu dla wszystkich trzech aktywów.
    - Statystyki podsumowujące (średnia, wariancja, odchylenie standardowe).
    - Macierz korelacji do identyfikacji najmniej skorelowanej pary (CDR i BLO).
    - Metryki portfela (oczekiwana stopa zwrotu, ryzyko, wskaźnik Sharpe’a) dla różnych kombinacji wag CDR-BLO.
    - Ustawienia Solvera do optymalizacji wag portfela.

### Metodologia

1. **Zbieranie danych**: Tygodniowe ceny zamknięcia dla CDR, BLO i 11B, obejmujące okres od 23 sierpnia 2015 do 17 sierpnia 2025 (10 lat).
2. **Analiza korelacji**: Obliczono korelacje Pearsona, aby wybrać parę o najniższej korelacji (CDR i BLO na poziomie 0,138).
3. **Konstrukcja portfela**:
   - Tygodniowe stopy zwrotu: `(Aktualna cena - Poprzednia cena) / Poprzednia cena`.
   - Oczekiwana stopa zwrotu portfela: Średnia ważona stóp zwrotu aktywów.
   - Wariancja portfela: `w1² * var1 + w2² * var2 + 2 * w1 * w2 * cov12`.
   - Ryzyko: Odchylenie standardowe (pierwiastek kwadratowy z wariancji portfela).
   - Wskaźnik Sharpe’a: `(Stopa zwrotu portfela - Stopa wolna od ryzyka) / Odchylenie standardowe portfela` (stopa wolna od ryzyka założona jako 0).
4. **Optymalizacja**: Użyto Solvera w Excelu do znalezienia optymalnych wag dla CDR i BLO, wynikających w ~59,2% CDR i ~40,8% BLO.

### Kluczowe wyniki

- **Macierz korelacji**:
  |       | CDR   | BLO   | 11B   |
  |-------|-------|-------|-------|
  | CDR   | 1     | 0,138 | 0,281 |
  | BLO   | 0,138 | 1     | 0,213 |
  | 11B   | 0,281 | 0,213 | 1     |

- **Statystyki aktywów**:
  | Aktywo | Średnia tygodniowa stopa zwrotu | Odchylenie standardowe | Wariancja |
  |--------|--------------------------------|------------------------|-----------|
  | CDR    | 0,00618                        | 0,05974                | 0,00357   |
  | BLO    | 0,00710                        | 0,07592                | 0,00576   |
  | 11B    | 0,00358                        | 0,05835                | 0,00340   |

- **Optymalny portfel (CDR + BLO)**:
  - Udziały: ~59,2% CDR, ~40,8% BLO.
  - Oczekiwana tygodniowa stopa zwrotu: ~0,655%.
  - Ryzyko (odchylenie standardowe): ~5,01%.
  - Wskaźnik Sharpe’a: ~0,131.

### Jak używać

1. Sklonuj repozytorium:
   ```bash
   git clone https://github.com/twoja_nazwa_uzytkownika/portfel-dwuskladnikowy.git
   ```
2. Otwórz plik `Portfel_dwuskładnikowy.xlsx` w Microsoft Excel.
3. Przejrzyj arkusz **Portfel** z obliczeniami i wynikami.
4. Aby powtórzyć optymalizację:
   - Włącz dodatek Solver (Plik > Opcje > Dodatki).
   - Przejdź do Dane > Solver i zmaksymalizuj wskaźnik Sharpe’a lub zminimalizuj ryzyko, zapewniając sumę udziałów równą 1 i udziały nieujemne.
5. Rozszerz analizę, dodając nowe dane cenowe.

### Wymagania

- Microsoft Excel (z włączonym dodatkiem Solver).