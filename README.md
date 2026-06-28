# 📱 ArbiCore Mobile Client (Public Edition)

[![Platform](https://img.shields.io/badge/platform-Android-3DDC84?logo=android)](https://www.android.com/)
[![License](https://img.shields.io/badge/license-Proprietary-red.svg)](#license)

Aplikacja mobilna platformy **Arbitrażysta** ułatwiająca licytację retro-konsol i elektroniki w Japonii (Yahoo Auctions, Buyee, Zenmarket). Pozwala na szybką selekcję ofert i wyliczanie całkowitych kosztów importu (TLC) bezpośrednio z telefonu.

---

## Co potrafi aplikacja?

### 1. Panel główny (Dashboard)
- Podgląd aktualnie analizowanych ofert importowych.
- Prezentacja cen w JPY oraz wyliczonego kosztu pod drzwi (TLC) w PLN na bazie aktualnych taryf i kursów walut.
- Wizualny wskaźnik stanu analizy.

### 2. Szybka selekcja (Swipe UI)
- Szybka selekcja ofert licytacji z japońskich serwisów.
- Przeciągnięcie karty w prawo zatwierdza ofertę, a w lewo ją odrzuca.
- Pełnoekranowy tryb pracy ułatwiający skupienie na ofertach.

### 3. Integracja z modelami AI
- **Audyt wizualny:** Wykrywanie wad ekranów (IPS vs TN), zużycia obudowy i modyfikacji sprzętu bezpośrednio na zdjęciach z aukcji.
- **Audyt opisu:** Dekodowanie japońskiego żargonu sprzedawców w celu wykrycia ukrytych usterek.

### 4. Wyliczanie TLC
- Automatyczne wyliczanie prowizji pośredników, kosztów wysyłki międzynarodowej, cła (0% dla konsol), podatku VAT (23%) oraz opłat pocztowych.
- Lokalny fallback w przypadku problemów z połączeniem sieciowym.

---

## 🔌 Architektura Dual-APK: Wtyczka Swarm

Dla dbałości o wydajność baterii telefonu, moduł współdzielenia pasma w tle (**Swarm Network**) został wydzielony do osobnej aplikacji systemowej (`ArbiCore-Swarm.apk`).

Aplikacja kliencka automatycznie wykrywa obecność wtyczki w systemie:
- **Wtyczka zainstalowana:** Odblokowuje panel statusu węzła na Dashboardzie i w profilu.
- **Wtyczka brakująca:** Ukrywa panel sterowania i wyświetla informacje o korzyściach płynących z instalacji wtyczki w celu zdobywania dodatkowych punktów AI.

---

## 📦 Pobieranie i Instalacja

Gotowe pliki instalacyjne APK znajdują się w zakładce **Releases** po prawej stronie tego repozytorium GitHub.

1. Pobierz najnowszy plik `ArbiCore-Mobile-Debug.apk`.
2. W ustawieniach telefonu zezwól na instalowanie aplikacji z nieznanych źródeł.
3. Zainstaluj plik APK i zaloguj się za pomocą swojego tokena z platformy Arbitrażysta.

---

## 🔒 Bezpieczeństwo

Aplikacja chroni dane użytkownika i połączenia z serwerem za pomocą podpisu cyfrowego zapytań oraz bezpiecznego szyfrowania danych sesyjnych na urządzeniu.

Luki bezpieczeństwa należy zgłaszać bezpośrednio do administratora platformy zgodnie z procedurą w pliku [SECURITY.md](SECURITY.md).

---

## 📄 Licencja

Oprogramowanie objęte licencją własnościową. Kopiowanie, dekompilacja, inżynieria wsteczna lub dystrybucja kodu źródłowego i plików binarnych bez pisemnej zgody autora są zabronione. Szczegóły znajdują się w pliku [LICENSE](LICENSE).

Copyright (c) 2026 Arbitrazysta. All rights reserved.
