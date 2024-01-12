SPISEK 

1) Skopiowac z bazy wikingowie tabele uczestnicy, etapy_wyprawy, sektor, wyprawa, kreatura
    CREATE TABLE uczestnicy AS SELECT * FROM wikingowie.uczestnicy;

    CREATE TABLE etapy_wyprawy AS SELECT * FROM wikingowie.etapy_wyprawy;

    CREATE TABLE sektor AS SELECT * FROM wikingowie.sektor;

    CREATE TABLE wyprawa AS SELECT * FROM wikingowie.wyprawa;

    CREATE TABLE kreatura AS SELECT * FROM wikingowie.kreatura;
