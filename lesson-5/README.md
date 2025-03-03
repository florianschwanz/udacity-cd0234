### Convert csv file

Tableau appears to have problems reading the csv file due to its formatting. The file is encoded in ISO-8859-1 and uses commas as separators and dots as decimal points. 
The following commands convert the file to UTF-8 encoding, use semicolons as separators, and commas as decimal points.

```shell
iconv -f ISO-8859-1 -t UTF-8 ./phoneswatersanitation.csv > ./phoneswatersanitation-converted.csv
sed -i '' 's/,/;/g' phoneswatersanitation-converted.csv 
sed -i '' 's/\./,/g' phoneswatersanitation-converted.csv
```