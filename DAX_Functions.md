1. Evaluate - zwraca tablicę wynikową
   EVALUATE
SUMMARIZECOLUMNS (
    DimDate[CalendarYear],
    "CurrentYearSales", DimProduct[CurrentYearSales],
    "PreviousYearSales", DimProduct[PreviousYearSales]
2. SELECTCOLUMNS w języku DAX pozwala na wybór określonych kolumn z tabeli oraz tworzenie nowych kolumn na podstawie wyrażeń DAX. Oto przykład:
SELECTCOLUMNS(
    Customer,
    "Country, State",
    [Country] & ", " & [State]
)
3. ALL w języku DAX zwraca wszystkie wiersze w tabeli lub wszystkie wartości w kolumnie, ignorując wszelkie filtry, które mogły zostać zastosowane. Jest to przydatne, gdy chcesz wyczyścić filtry i wykonać obliczenia na wszystkich wierszach w tabeli1. Oto kilka przykładów użycia:
   ALL('Sales')
4. RemoveFilters - podobnie jak ALL tylko nie zwraca tabeli


