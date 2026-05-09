# Zadanie: Projekt końcowy

| Termin oddania | Punkty     |
|----------------|:-----------|
| 11.06.2026  23:00   |    20      |

---
Przekroczenie terminu o **n** zajęć wiąże się z karą:
- punkty uzyskane za realizację zadania są dzielone przez **2<sup>n</sup>**.

---

### Opis zadania

Napisz program, który:
* zawiera obiekty o kilku cechach ilościowych (cechy posiadają definiowalne natężenie/wartość),
* umożliwia agregację obiektów, tworząc nowe obiekty o skumulowanych cechach,
* implementuje reguły powstawania nowych cech agregatu po osiągnięciu odpowiednich poziomów cech skumulowanych,
* definiuje zadania wymagające posiadania odpowiednich cech w odpowiednim natężeniu,
* odpowiada na pytanie, czy posiadając:
  * dany zbiór obiektów o danych cechach,
  * zbiór reguł dotyczących powstawania nowych cech,
  * zbiór zadań do wykonania,

  można tak przeprowadzić agregację obiektów, by zrealizować zadania.

> Dopuszczalne są również projekty autorskie, które nie muszą realizować powyższego schematu, lecz w nietrywialny sposób wykorzystują wymagane wzorce projektowe.

---

### Przykłady

**Przykład 1 – Mrowisko**
* Mrówka ma pola: `siła`, `pamięć`, `zdrowie`, itp.
* Mrówki można agregować, tworząc roje o nowych właściwościach opisanych regułami tworzenia roju.
* Zadaniami dla mrowiska mogą być: znalezienie i przeniesienie przedmiotu, pokonanie przeszkody, pokonanie przeciwnika.

**Przykład 2 – Drużyna bohaterów (RPG)**
* Bohater ma cechy: `atak`, `obrona`, `zdrowie`, `magia`.
* Bohaterów można łączyć w drużyny, które zyskują premie zbiorowe (np. bonus do ataku, gdy łączny atak drużyny przekroczy próg).
* Misje wymagają określonego łącznego poziomu cech drużyny.

**Przykład 3 – Flota robotów**
* Robot ma cechy: `moc obliczeniowa`, `zasięg`, `wytrzymałość`.
* Roboty można łączyć w jednostki bojowe rządzące się własnymi regułami synergii.
* Zadaniami są misje wymagające określonej konfiguracji cech floty.

---

### Techniczny cel zadania

W projekcie należy w **nietrywialny sposób** wykorzystać **co najmniej 2 wzorce projektowe** z każdej z poniższych grup (łącznie **co najmniej 6 wzorców**):

| Kategoria        | Przykłady wzorców                                                                              |
|------------------|-----------------------------------------------------------------------------------------------|
| **Kreacyjne**    | Singleton, Factory Method, Abstract Factory, Builder, Prototype                               |
| **Strukturalne** | Adapter, Bridge, Composite, Decorator, Facade, Flyweight, Proxy                               |
| **Behawioralne** | Chain of Responsibility, Command, Iterator, Mediator, Observer, State, Strategy, Template Method, Visitor |

> Wzorce muszą **współpracować** w ramach jednego spójnego projektu — nie mogą być dodane sztucznie ani niezależnie od siebie.

---

### Wymagania dotyczące dostarczenia

1. **Kod źródłowy** – projekt skompilowany i uruchamialny.
2. **Diagram UML** – diagram klas oraz diagram sekwencji pokazujący zastosowane wzorce i ich wzajemne powiązania.
3. **Dokumentacja techniczna** (README lub komentarze w kodzie) zawierająca:
   * nazwy i kategorie zastosowanych wzorców,
   * uzasadnienie wyboru każdego wzorca (dlaczego pasuje do problemu),
   * opis współpracy wzorców ze sobą.
4. **Testy jednostkowe** – testy pokrywające kluczowe scenariusze. Obecność testów jest uwzględniana w kryterium *Jakość implementacji*.

---

### Kryteria oceny (20 pkt)

| Kryterium                                                  | Punkty |
|------------------------------------------------------------|--------|
| Trafność doboru wzorców (zgodność wzorców z problemem)     | 6 pkt  |
| Jakość implementacji (poprawność, czytelność kodu)         | 6 pkt  |
| Nietrywialność informatyczna wybranego problemu            | 5 pkt  |
| Dokumentacja, diagram klas i diagram sekwencji             | 3 pkt  |

---

### Wskazówki

* Wzorzec jest **trywialny**, gdy jest użyty wyłącznie jako opakowanie bez wpływu na logikę systemu (np. Singleton wyłącznie po to, by był Singleton).
* Wzorzec jest **nietrywialny**, gdy jego zastosowanie upraszcza, rozszerza lub organizuje logikę domenową projektu.
* Wzorzec **Composite** naturalnie modeluje agregację obiektów opisaną w zadaniu — warto rozważyć jego zastosowanie.
* Wzorzec **Strategy** lub **Template Method** elegancko wyraża wymienne reguły tworzenia nowych cech agregatu.
* Wzorzec **Observer** pozwala reagować na zmiany poziomów cech (np. powiadamiać o osiągnięciu progu wymagań zadania).
* Wzorzec **Builder** ułatwia konstrukcję złożonych obiektów-agregatów krok po kroku.
