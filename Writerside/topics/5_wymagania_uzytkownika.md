# 5. Wymagania użytkownika

## Struktura dziedziny problemowej
System zarządza następującymi bytami:

- **Książka**: tytuł, autor, ISBN, liczba egzemplarzy, kategoria.
- **Użytkownik**: imię, nazwisko, ID, adres e-mail.
- **Wypożyczenie**: ID użytkownika, ID książki, data wypożyczenia, data zwrotu.
- **Rezerwacja**: ID użytkownika, ID książki, data rezerwacji.

### Relacje między bytami:
- Jeden użytkownik może wypożyczyć wiele książek.
- Jedna książka może być wypożyczona przez wielu użytkowników (ale tylko jeden egzemplarz na użytkownika w danym momencie).
- Użytkownik może rezerwować książki.

## Oczekiwana funkcjonalność systemu
Oczekuje się, że system będzie wspomagał użytkowników w:
- Rejestracji i logowaniu do systemu.
- Wyszukiwaniu książek po tytule, autorze, ISBN, kategorii.
- Rezerwowaniu dostępnych książek.
- Przeglądaniu historii wypożyczeń i zwrotów.

Oczekuje się, że system będzie wspomagał bibliotekarzy w:
- Dodawaniu nowych książek do księgozbioru.
- Aktualizowaniu informacji o książkach.
- Zarządzaniu wypożyczeniami i zwrotami książek.
- Generowaniu raportów o stanie biblioteki.

## Ograniczenia systemu
- System powinien działać na serwerach z systemem Linux.
- Oczekiwana dostępność systemu to minimum 99,5%.
- System powinien obsługiwać jednocześnie minimum 100 użytkowników.
