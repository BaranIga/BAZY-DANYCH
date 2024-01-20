# ROZBITEK

### zadanie 1.1

```SQL
create table kreatura as select * from wikingowie.kreatura;
```

```SQL
create table zasob as select * from wikingowie.zasob;
```

```SQL
create table ekwipunek as select * from wikingowie.ekwipunek;
```


### zadanie 1.2

```SQL
select * from zasob;
```


### zadanie 1.3 

```SQL
select * from zasob where rodzaj = 'jedzenie';
```


### zadanie 1.4 

```SQL
select idZasobu, ilosc from zasob where idZasobu in (1,3,5);
```



# KOKOS?

### zadanie 2.1

```SQL
select * from kreatura where rodzaj != "wiedzma" and udzwig >= 50;
```


### zadanie 2.2

```SQL
select * from zasob where waga between 2 and 5;
```


### zadanie 2.3

```SQL
select * from kreatura where nazwa like "%or%" and udzwig between 30 and 70;
```



# HAMAK

### zadanie 3.1

```SQL
select * from zasob where month(dataPozyskania) = 7 or month(dataPozyskania) = 8;
```


### zadanie 3.2

```SQL
select * from zasob where rodzaj is not null order by waga asc;
```


### zadanie 3.3

```SQLselect * from kreatura order by dataUr desc limit 5;
```




# ZŁOTA RYBKA 

### zadanie 4.1

```SQL
select distinct rodzaj from zasob;
```



### zadanie 4.2

```SQL
select concat(nazwa, 'to id=', idKreatury) from kreatura;
```


### zadanie 4.3

```SQL
select nazwa, (ilosc*waga) as waga_calkowita from zasob where year(dataPozyskania) between 2000 and 2007;
```



# TWARDY SEN

### zadanie 5.1

```SQL
select nazwa, waga*0.7 as masa_netto, waga*0.3 as waga_odpadkow from zasob where rodzaj='jedzenie';
```


### zadanie 5.2

```SQL
select * from zasob where rodzaj is null;
```


### zadanie 5.3

```SQL
select distinct * from zasob where nazwa like 'Ba%' or nazwa like '%os' order by rodzaj asc;
```
