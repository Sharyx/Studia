.. _hermetyzacja:

Hermetyzacja w programowaniu
============================

Hermetyzacja jest jednym z kluczowych konceptów obiektowości w programowaniu. Polega na ukrywaniu wewnętrznych danych obiektu oraz implementacji jego metody przed innymi częściami programu, ograniczając dostęp i modyfikację tych elementów tylko za pomocą określonych interfejsów.

Główne cele hermetyzacji:
--------------------------

1. **Ochrona danych:** Hermetyzacja umożliwia kontrolowanie dostępu do danych w obiekcie. Poprzez tworzenie getterów i setterów, można zapewnić kontrolowany dostęp do pól obiektu, co zwiększa bezpieczeństwo i zapobiega niepożądanym zmianom.

2. **Abstrakcja:** Ukrywanie implementacji metod umożliwia programistom korzystanie z interfejsów obiektów, niezależnie od ich wewnętrznej logiki. Dzięki temu zmiany wewnątrz obiektów nie powinny wpływać na inne części programu.

Przykład wykorzystania hermetyzacji w języku Python:
-----------------------------------------------------

.. code-block:: python

  class KontoBankowe:
    def __init__(self, saldo):
        self._saldo = saldo

    def get_saldo(self):
        return self._saldo

    def set_saldo(self, nowe_saldo):
        self._saldo = nowe_saldo
