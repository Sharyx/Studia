.. _zmienne:

Zmienne w programowaniu obiektowym w Pythonie
=============================================

W programowaniu obiektowym zmienne są powiązane z obiektami i umożliwiają przechowywanie danych. W Pythonie zmienne w klasach są deklarowane w metodzie konstruktora `__init__()`.

Deklaracja zmiennych w klasie
------------------------------

Aby zadeklarować zmienną w klasie, używamy metody konstruktora `__init__()`:

.. code-block:: python

   class Samochod:
       def __init__(self, marka, model):
           self.marka = marka
           self.model = model

W tym przykładzie `marka` i `model` są zmiennymi przypisanymi do obiektu klasy `Samochod`.

Dostęp do zmiennych obiektu
---------------------------

Aby uzyskać dostęp do zmiennych obiektu, odwołujemy się do nich za pomocą składni `obiekt.zmienna`:

.. code-block:: python

   moj_samochod = Samochod("Toyota", "Corolla")
   print(moj_samochod.marka)  # Wyświetli: Toyota
   print(moj_samochod.model)  # Wyświetli: Corolla

Modyfikacja zmiennych obiektu
------------------------------

Zmienne obiektu mogą być modyfikowane po ich utworzeniu:

.. code-block:: python

   moj_samochod.marka = "Honda"
   print(moj_samochod.marka)  # Wyświetli: Honda

Teraz `marka` samochodu została zmieniona na "Honda".

Zmienne klasowe i zmienne instancyjne
--------------------------------------

W Pythonie możemy mieć zmienne, które są wspólne dla wszystkich instancji danej klasy (zmienne klasowe) oraz zmienne, które są specyficzne dla każdej instancji (zmienne instancyjne):

.. code-block:: python

   class Licznik:
       licznik_klasowy = 0

       def __init__(self):
           Licznik.licznik_klasowy += 1
           self.licznik_instancyjny = 0

       def zwieksz_licznik(self):
           self.licznik_instancyjny += 1

Teraz `licznik_klasowy` jest zmienną klasową, a `licznik_instancyjny` jest zmienną instancyjną.

Zmienne w programowaniu obiektowym w Pythonie pozwalają na przechowywanie danych w obiektach i manipulację nimi. Czy potrzebujesz dodatkowych informacji?

