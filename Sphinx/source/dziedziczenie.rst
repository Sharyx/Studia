.. _dziedziczenie_python:

Dziedziczenie w Pythonie
========================

Dziedziczenie to kluczowy koncept w programowaniu obiektowym, który umożliwia tworzenie nowych klas na podstawie istniejących. Klasa dziedzicząca może korzystać z atrybutów i metod klasy nadrzędnej.

Tworzenie podklasy
------------------

Aby utworzyć klasę dziedziczącą, użyjemy notacji nawiasów przy tworzeniu klasy:

.. code-block:: python

   class Zwierze:
       def __init__(self, gatunek):
           self.gatunek = gatunek

       def odglos(self):
           pass

   class Pies(Zwierze):
       def odglos(self):
           return "Hau!"

W tym przykładzie `Pies` dziedziczy po klasie `Zwierze`. Klasa `Pies` może wykorzystać atrybuty i metody klasy `Zwierze`.

Wywoływanie metod z klasy nadrzędnej
--------------------------------------

Czasami w klasie dziedziczącej chcemy skorzystać z metody z klasy nadrzędnej. W Pythonie możemy to zrobić za pomocą funkcji `super()`:

.. code-block:: python

   class Kot(Zwierze):
       def odglos(self):
           dzwiek_zwierzecia = super().odglos()
           return f"Kot mówi: {dzwiek_zwierzecia}"

Teraz klasa `Kot` nadpisuje metodę `odglos()`, ale wywołuje również tę metodę z klasy nadrzędnej (`Zwierze`) i dodaje własny tekst.

Dziedziczenie wielokrotne
--------------------------
W Pythonie istnieje możliwość dziedziczenia z wielu klas:

.. code-block:: python

   class ZwierzeDomowe:
       def info(self):
           return "To zwierze domowe."

   class KotDomowy(Zwierze, ZwierzeDomowe):
       pass

Teraz klasa `KotDomowy` dziedziczy atrybuty i metody zarówno z klasy `Zwierze` jak i `ZwierzeDomowe`.

To są podstawy dziedziczenia w Pythonie, pozwalające na tworzenie hierarchii klas i wykorzystywanie istniejącego kodu w sposób efektywny.

Listy:
------

1. **Podstawowe zagadnienia:**
   - Tworzenie podklasy
   - Wywoływanie metod z klasy nadrzędnej
   - Dziedziczenie wielokrotne

Odnośniki:
-----------

1. `Przykład dziedziczenia w Pythonie <#dziedziczenie_python>`_
