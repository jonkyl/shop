#Asortyment 
by nyga&mistrz_mlyna

**Dokumentacja przydzielonej usługi.**
 
Sprawozdanie zawiera opis usługi​asortyment​dla sklepu (firma 1). Asortyment jest to zestaw dóbr (usług/towarów) dostępnych i oferowanych w sklepie. 

###Operacje usługi:
| Operacja           | Wejście                                          | Wyjście   | Error |
| ---------------- | ------------------------------------------------ | -------   | :---: |
| Dodaj produkt | kod produktu(long int), nazwa(string), opis(string), cena(BigDecimal) | oneWay     |       |
| Usuń  produkt | kod produktu(long int) | OneWay    | |
| Pobierz listę  | opcjonalnie można podać jedno z pól: kod produktu(long int), nazwa(string), opis(string), cena(BigDecimal) do filtra | lista produktów (tabela)    |       |

**Powiązania usługi "Asortyment" z innymi usługami**

| Operacja           | Opis powiązań |
| ---------------- | ------------------------------------------------ |
| Magazyn | Usługa “Asortyment” jest powiązana z usługą “Magazyn”. Produkty dodane do asortymentu powinny zostać uzupełnione w magazynie, tak aby następnie były dostępne w sprzedaży. Podobnie, gdy z asortymentu zostanie usunięte jakieś dobro, powinno to spowodować brak możliwości zamówienia tego towaru do magazynu. Dodatkowo warto wspomnieć o przydatnym ograniczeniu: dopóki w magazynie znajduje się określony produkt, nie można go usunąć z asortymentu sklepu produkt musi zostać wcześniej sprzedany lub zutylizowany.  |
| Sprzedaż | Usługa “Sprzedaż” może czerpać informacje na temat produktów z listy asortymentu,która zawiera kody produktów, ich nazwy, opisy oraz ceny. |
| Klienci | Usługa “Klienci” – klient powinien mieć możliwość przejrzenia listy dostępnych produktów i zapoznania się z ich opisem oraz ceną. |
|Pracownicy| Pracownik powinien mieć możliwość dodawać/usuwać/wyświetlać pozycje w asortymencie.  |

```Changelog: 2015-10-20
Opis usługi SOA```

