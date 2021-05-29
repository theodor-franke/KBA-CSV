# KBA-CSV
A CSV table of the "List of manufacturer and types of motor vehicles" registered by the german KBA.

This CSV-file is parsed from the official ["List of manufacturer and types
of motor vehicles with at least four wheels designed and built for the passenger (Category M) PDF"](https://www.kba.de/DE/Statistik/Verzeichnisse/verzeichnisse_node.html) releases by the KBA

Release-date: 15.02.2021

## Parsing

The parsing was done with the help of [tabula-java](https://github.com/tabulapdf/tabula-java) using the following command:

```
java -jar tabula.jar input.pdf -a 115,30,561,813 -c 62,90,211,335,452,506,557,611,640,670,698,721,746,776 -f CSV -p all -o output.csv
```

I removed the first and last pages of the file beforehand.
