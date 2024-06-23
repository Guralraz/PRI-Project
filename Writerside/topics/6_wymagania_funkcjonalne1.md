# 6. Wymagania funkcjonalne

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#ffcc00', 'edgeLabelBackground':'#ffffff', 'tertiaryColor': '#ffffff'}}}%%
graph TD
    A[Użytkownik] -->|Rejestracja| B[System Biblioteki]
    A -->|Logowanie| B
    A -->|Wyszukiwanie książek| B
    A -->|Rezerwowanie książek| B
    A -->|Przeglądanie historii wypożyczeń| B

    C[Bibliotekarz] -->|Dodawanie książek| B
    C -->|Aktualizowanie książek| B
    C -->|Zarządzanie wypożyczeniami i zwrotami| B
    C -->|Generowanie raportów| B

    D[Administrator] -->|Zarządzanie użytkownikami| B
