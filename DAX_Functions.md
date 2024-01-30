ISFILTERED ### Zwraca wartość TRUE, gdy określona tabela lub kolumna jest filtrowana bezpośrednio.
ALL ###Zwraca wszystkie wiersze w tabeli lub wszystkie wartości w kolumnie, ignorując wszystkie filtry, które mogły zostać zastosowane. Ta funkcja jest przydatna do czyszczenia filtrów i tworzenia obliczeń we wszystkich wierszach w tabeli.
Sales % of Total =
VAR SalesALLCustomers =


### używanie Remove Filter, aby uzyskać wynik całościowy.
CALCULATE(
          [Total Sales],
          REMOVEFILTERS(dimCustomer[Customer Name])
)
VAR SalesPctTotal =
DIVIDE(
    [Total Sales],
    SalesALLCustomers
)
RETURN
SalesPctTotal



