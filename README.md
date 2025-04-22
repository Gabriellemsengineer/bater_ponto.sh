# bater_ponto.sh
#!/bin/bash
DATA=$(date +"%Y-%m-%d")
HORA=$(date +"%H:%M:%S")
TIPO="entrada"  # Mude para "saida" quando necessário

echo "$DATA,$HORA,$TIPO" >> registros/$DATA.csv

git add registros/$DATA.csv
git commit -m "Registro de ponto $TIPO em $DATA $HORA"
git push origin main
