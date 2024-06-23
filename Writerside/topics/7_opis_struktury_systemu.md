# 7. Opis struktury systemu (schemat pojęciowy)

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#ffcc00', 'edgeLabelBackground':'#ffffff', 'tertiaryColor': '#ffffff'}}}%%
classDiagram
    class Ksiazka {
        -String tytul
        -String autor
        -String ISBN
        -int liczbaEgzemplarzy
        -String kategoria
    }

    class Uzytkownik {
        -String imie
        -String nazwisko
        -String ID
        -String email
        +zarejestruj()
        +zaloguj()
        +wyszukajKsiazke()
        +zarezerwujKsiazke()
        +przegladajHistorie()
    }

    class Bibliotekarz {
        +dodajKsiazke()
        +aktualizujKsiazke()
        +zarzadzajWypozyczeniami()
        +generujRaporty()
    }

    class Administrator {
        +zarzadzajUzytkownikami()
    }

    class Wypozyczenie {
        -String IDUzytkownika
        -String IDKsiazki
        -Date dataWypozyczenia
        -Date dataZwrotu
    }

    class Rezerwacja {
        -String IDUzytkownika
        -String IDKsiazki
        -Date dataRezerwacji
    }

    Uzytkownik <|-- Bibliotekarz
    Uzytkownik <|-- Administrator
    Uzytkownik "1" --> "0..*" Wypozyczenie : posiada
    Uzytkownik "1" --> "0..*" Rezerwacja : rezerwuje
    Ksiazka "1" --> "0..*" Wypozyczenie : jest wypożyczana
    Ksiazka "1" --> "0..*" Rezerwacja : jest rezerwowana
