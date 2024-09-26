# learn_linux_by_doing
## command lines

### 0. Removing file test-1
rm test-1 -r

### 1. Moving the `top-5-lowest-temparatures.csv` file:
mv top-5-lowest-temparatures.csv analyzed/

### 2. Removing duplicate rows from top-5-lowest-temparatures.csv
sort top-5-lowest-temparatures.csv | uniq > temp.csv && mv temp.csv top-5-lowest-temparatures.csv

### 3. Extracting the top 5 highest recorded temperatures
sort -t, -k2 -nr satelite_temperature_data.csv | head -n 5 > ../analyzed/top-5-highest-temparatures.csv

### 4. Extracting the top 5 lowest recorded temperatures
sort -t, -k2 -n satelite_temperature_data.csv | head -n 5 > ../analyzed/top-5-lowest-temparatures.csv

### 5. Extracting heat data for my country
grep Rwanda satelite_temperature_data.csv > ../analyzed/country-heat_data.csv

