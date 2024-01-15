# zadanie 1.1

```create table kreatura as select * from wikingowie.kreatura;```

create table zasob as select * from wikingowie.zasob;

create table ekwipunek as select * from wikingowie.ekwipunek;


#zadanie 1.2

select * from zasob;


#zadanie 1.3 

select * from zasob where rodzaj = 'jedzenie';


# zadanie 1.4 

select idZasobu, ilosc from zasob where idZasobu in (1,3,5);


# zadanie 2.1

select * from kreatura where rodzaj != "wiedzma" and udzwig >= 50;


# zadanie 2.2

select * from zasob where waga between 2 and 5;


# zadanie 2.3

select * from kreatura where nazwa like "%or%" and udzwig between 30 and 70;


# zadanie 3.1

select * from zasob where month(dataPozyskania) = 7 or month(dataPozyskania) = 8;


# zadanie 3.2

select * from zasob where rodzaj is not null order by waga asc;


# zadanie 3.3

select * from kreatura order by dataUr desc limit 5;


# zadanie 4.1

select distinct rodzaj from zasob;


# zadanie 4.2

select concat(nazwa, 'to id=', idKreatury) from kreatura;


# zadanie 4.3

select nazwa, (ilosc*waga) as waga_calkowita from zasob where year(dataPozyskania) between 2000 and 2007;


# zadanie 5.1

select nazwa, waga*0.7 as masa_netto, waga*0.3 as waga_odpadkow from zasob where rodzaj='jedzenie';


# zadanie 5.2

select * from zasob where rodzaj is null;


# zadanie 5.3

select distinct * from zasob where nazwa like 'Ba%' or nazwa like '%os' order by rodzaj asc;
