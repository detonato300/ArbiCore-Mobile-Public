# 📱 ArbiCore Mobile Client (Public Edition)

[![Platform](https://img.shields.io/badge/platform-Android-3DDC84?logo=android)](https://www.android.com/)
[![License](https://img.shields.io/badge/license-Proprietary-red.svg)](#license)

Aplikacja mobilna platformy **Arbitrażysta** stanowiąca mobilne centrum operacyjne dla inwestorów licytujących retro-konsole i elektronikę w Japonii (Yahoo Auctions, Buyee, Zenmarket). 

To dedykowany runtime mobilny zaprojektowany z myślą o maksymalnej szybkości selekcji ofert i optymalizacji kosztów importowych (TLC) bezpośrednio z telefonu.

---

## 🚀 Kluczowe Funkcjonalności

### 1. Panel Główny (Dashboard)
- Szybki podgląd aktualnie analizowanych ofert importowych.
- Prezentacja cen w JPY oraz wyliczonego całkowitego kosztu **TLC (Total Landed Cost)** w PLN w oparciu o aktualne kursy i taryfy.
- Wizualny wskaźnik stanu analizy.

### 2. Szybka Selekcja (Swipe UI)
- Moduł ekspresowej selekcji ofert licytacji z japońskich serwisów.
- Przeciągnięcie karty w prawo oznacza zatwierdzenie/analizę oferty, przeciągnięcie w lewo odrzucenie.
- Pełnoekranowy tryb pracy dla maksymalnego skupienia uwagi inwestora.

### 3. Integracja z Gemini 3.1 Flash-Lite
- **Audyt Wizualny:** Analiza zdjęć aukcji pod kątem wykrywania wad ekranów (IPS vs TN), zużycia obudowy i modyfikacji hardware.
- **Audyt Semantyczny:** Dekodowanie japońskiego opisu sprzedawców ("Tatemae") w celu ujawnienia ukrytych usterek i rzeczywistego stanu technicznego.

### 4. Kalkulacja TLC (VPS-First)
- Obliczenia kosztowe wykonywane w czasie rzeczywistym.
- Uwzględnia koszty prowizji pośredników, wysyłki międzynarodowe, cło (0% dla konsol), podatki VAT (23%) oraz opłaty manipulacyjne.
- Bezpieczny fallback lokalny w przypadku problemów z połączeniem sieciowym.

---

## 🔌 Architektura Dual-APK: Wtyczka Swarm

Dla dbałości o zasoby systemowe Twojego telefonu, moduł współdzielenia pasma i zwiadu w tle (**Swarm Network**) został całkowicie wydzielony do osobnej aplikacji systemowej (`ArbiCore-Swarm.apk`).

Aplikacja kliencka dynamicznie wykrywa obecność wtyczki w systemie:
- **Wtyczka zainstalowana:** Odblokowuje panel statusu węzła na Dashboardzie i w profilu.
- **Wtyczka brakująca:** Ukrywa panel sterowania i wyświetla informacje o korzyściach płynących z instalacji wtyczki w celu zdobywania dodatkowych Kredytów AI (Swarm Points).

---

## 📦 Pobieranie i Instalacja

Gotowe pliki instalacyjne APK znajdują się w zakładce **Releases** po prawej stronie tego repozytorium GitHub.

1. Pobierz najnowszy plik `ArbiCore-Mobile-Debug.apk`.
2. W ustawieniach telefonu włącz zezwolenie na instalowanie aplikacji z nieznanych źródeł.
3. Zainstaluj plik APK i zaloguj się za pomocą swojego konta na platformie Arbitrażysta.

---

## 🔒 Bezpieczeństwo i Ochrona Danych

Aplikacja wdraża zaawansowane mechanizmy ochrony danych użytkownika i komunikacji z zapleczem analitycznym:
- **Podpis Cyfrowy:** Każde zapytanie do serwera jest podpisane kryptograficznie.
- **Twarde Szyfrowanie:** Tokeny sesyjne oraz konfiguracje kluczy są przechowywane w bezpiecznym, szyfrowanym kontenerze systemowym urządzenia.

Wszelkie potencjalne luki bezpieczeństwa należy zgłaszać bezpośrednio do administratora platformy zgodnie z procedurą w pliku [SECURITY.md](SECURITY.md).

---

## 📄 Licencja

Oprogramowanie objęte licencją własnościową. Kopiowanie, dekompilacja, inżynieria wsteczna lub dystrybucja kodu źródłowego i plików binarnych bez pisemnej zgody autora są surowo zabronione. Szczegóły znajdują się w pliku [LICENSE](LICENSE).

Copyright (c) 2026 Arbitrazysta. All rights reserved.
