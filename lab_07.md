# SKWAREK 

### zadanie 1.1

```
select round(avg(waga), 2) as srednia_waga from kreatura where rodzaj = 'wiking';
```

### zadanie 1.2

```
select round(avg(waga), 2) as srednia_waga from kreatura where rodzaj = 'wiking';
```

### zadanie 1.3

```
select round(avg(year(dataUr)), 2) as sredni_wiek, rodzaj from kreatura group by rodzaj;
```


# DYMEK

### zadanie 2.1

```
select round(avg(waga), 2) as suma_wag, rodzaj from zasob where rodzaj is not null group by rodzaj;
```

### zadanie 2.2

```
select nazwa, round(avg(waga), 2) as srednia_waga from zasob where ilosc >= 4 group by nazwa having srednia_waga > 10;
```

### zadanie 2.3

```
select rodzaj, count(distinctrow(nazwa)) as nazwa from zasob;
```


# PIEPRZ 

### zadanie 3.1

```
select k.nazwa, sum(e.ilosc) as niesione_rzeczy from kreatura k, ekwipunek e where k.idKreatury=e.idKreatury group by k.nazwa;
```


### zadanie 3.2

```
select k.nazwa, z.nazwa from kreatura k inner join 
ekwipunek e on k.idKreatury=e.idKreatury inner join 
zasob z on e.idZasobu=z.idZasobu;
```

### zadanie 3.3

```
select * from kreatura k left join 
ekwipunek e on k.idKreatury=e.idKreatury where 
e.idKreatury is null;

select * from kreatura where idKreatury not in 
(select distinct idKreatury from ekwipunek where 
idKreatury is not null);
```


# DZIADEK 

### zadanie 4.1

```
select k.nazwa, z.nazwa, k.dataUr from kreatura k inner join 
ekwipunek e on k.idKreatury=e.idKreatury inner join 
zasob z on e.idZasobu=z.idZasobu where dataUr like '%7%' and 
k.rodzaj = 'wiking';
```

### zadanie 4.2

```
select k.nazwa, k.dataUr as data_urodzenia, z.nazwa from kreatura k inner join 
ekwipunek e on k.idKreatury=e.idKreatury inner join 
zasob z on e.idZasobu=z.idZasobu where 
k.rodzaj = 'wiking' and z.rodzaj = 'jedzenie' order by 
data_urodzenia desc limit 5;
```


### zadanie 4.3

```
select concat(k.nazwa, ' - ', kr.nazwa) as 
nazwy_kreatur, k.idKreatury, kr.idKreatury from kreatura k cross join 
kreatura kr on k.idKreatury=kr.idKreatury + 5;
```


# ZŁA NOWINA

### zadanie 5.1

```
select k.rodzaj, avg(z.waga) as srednia_waga from kreatura k inner join 
ekwipunek e on k.idKreatury=e.idKreatury inner join 
zasob z on e.idZasobu=z.idZasobu group by k.rodzaj having avg(z.waga);
```
