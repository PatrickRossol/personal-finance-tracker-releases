# Budżet domowy

Osobisty budżet domowy — Windows i Linux.

## Windows

**[Pobierz](../../releases/latest)** plik `budzet-domowy-setup-*.exe` i uruchom go.

Program nie jest podpisany certyfikatem, więc Windows pokaże ostrzeżenie
„Windows chronił Twój komputer”:

1. Kliknij **Więcej informacji**
2. Kliknij **Uruchom mimo to**

Instalacja nie wymaga uprawnień administratora i trwa kilka sekund.

## Linux

**[Pobierz](../../releases/latest)** plik `budzet-domowy-*.AppImage`, a potem kliknij
go prawym przyciskiem → **Właściwości** → **Uprawnienia** → zaznacz **Pozwól na
wykonywanie pliku jako programu**. Od tej pory uruchamiasz go dwuklikiem.

To samo z terminala:

```bash
chmod +x budzet-domowy-*.AppImage
./budzet-domowy-*.AppImage
```

Jeśli pojawi się błąd o `libfuse.so.2`, brakuje jednej biblioteki systemowej:

```bash
sudo apt install libfuse2
```

Jest też plik `.deb`, jeśli wolisz zwykłą instalację z wpisem w menu
(`sudo apt install ./budzet-domowy_*.deb`) — ale **wersja .deb nie aktualizuje się
sama**. AppImage tak.

## Aktualizacje

Program sam sprawdza, czy jest nowsza wersja, pobiera ją w tle i instaluje przy
następnym uruchomieniu. Nie trzeba nic robić.

Na stronie wydania są też pliki `latest.yml`, `latest-linux.yml` i `.blockmap` —
**nie pobieraj ich**. Program korzysta z nich sam przez internet.

## Twoje dane

Wszystko zostaje na Twoim komputerze, w jednym pliku:

- Windows: `%APPDATA%` → `Budżet domowy` → `budget.db`
- Linux: `~/.config/Budżet domowy/budget.db`

Nic nie jest nigdzie wysyłane. Kopia zapasowa to po prostu skopiowanie tego pliku.

---

To repozytorium zawiera wyłącznie gotowe instalatory. Kod źródłowy jest prywatny.
