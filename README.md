# Projekt analiza skutecznego rozmieszczenia farm energi na świecie

## O projekcie
Projekt wykorzystuje **Analitykę Preskryptywną** oraz **Programowanie Liniowe** do optymalizacji portfela inwestycyjnego w odnawialne źródła energii (OZE). 

Celem symulacji jest alokacja budżetu inwestycyjnego $5,000,000 w farmy fotowoltaiczne na całym świecie, aby zmaksymalizować całkowity zwrot z inwestycji (ROI), uwzględniając lokalne uwarunkowania ekonomiczne (ceny energii, koszty pracy) oraz nasłonecznienie.

## Kluczowe Wyniki
Algorytm zidentyfikował optymalny portfel inwestycyjny o średnim **ROI 19.8%**, generujący **$970,000 rocznego zysku**.

Najbardziej rentowne lokalizacje:
1.  **Dubaj (UAE)** - ROI 23.6% (Wysoka wydajność energetyczna).
2.  **Ateny (Grecja)** - ROI 22.1% (Wysokie ceny energii w UE).
3.  **Brisbane (Australia)** - ROI 21.4% (Synergia nasłonecznienia i taryf energetycznych).
<img width="1475" height="590" alt="dashboarde" src="https://github.com/user-attachments/assets/bdee77b3-9d30-437c-a232-4ca03f438c53" />

   ## Metodologia
W przeciwieństwie do prostych analiz statystycznych, projekt wykorzystuje bibliotekę **PuLP** do rozwiązania problemu optymalizacyjnego.

### 1. Inżynieria Danych
Surowe dane klimatyczne zostały wzbogacone o symulację czynników ekonomicznych:
* Korekta cen energii dla Europy - wysokie podatki/taryfy i Azji.
* Korekta kosztów instalacji zależna od regionu.

  ### 2. Model Matematyczny programowanie liniowe
* **Funkcja celu:** Maksymalizacja $\sum (Liczba\_Farm_i \times Zysk\_Roczny_i)$
 **Ograniczenia:**

* Zasada 1 (Budżet): Łączny koszt inwestycji nie może przekroczyć 5,000,000 USD. Algorytm musi "zmieścić się" w kwocie, szukając okazji tam, gdzie jest tanio i efektywnie.

* Zasada 2 (Bezpieczeństwo): Nie stawiamy wszystkiego na jedną kartę. Wprowadzono limit maksymalnie 20 farm na jedno miasto, aby wymusić dywersyfikację geograficzną (rozproszone ryzyko).

* Zasada 3 (Realizm): Algorytm operuje na liczbach całkowitych – nie można zainwestować w "pół farmy".


## Technologie
* Python 3.9+
* PuLP** - Solver optymalizacyjny.
* Pandas - Transformacja danych.
* Seaborn/Matplotlib - Wizualizacja portfela.

Źródło danych: https://www.kaggle.com/datasets/shaistashahid/urban-solar-roi-and-sustainability
