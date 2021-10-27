# BioinfoBash
A collection of helpful Bash commands for Bioinformatics

## FASTQ

### Read length in Mega Base Pairs
```bash
grep -v "@" [FASTQFILE] | wc | awk '{print $1}'
```

### Total number of base pairs within file in Mega base pairs
```bash
grep -v "@" [FASTQFILE] | wc | awk '{print calc ($3-$1)/1000000}'
```

### Average read length
```bash
grep -v "@" [FASTQFILE] | wc | awk '{print calc ($3-$1)/$1}'
```

## FASTA

### Read length in Mega Base Pairs
```bash
grep -v ">" [FASTQFILE] | wc | awk '{print $1}'
```

### Total number of base pairs within file in Mega base pairs
```bash
grep -v ">" [FASTQFILE] | wc | awk '{print calc ($3-$1)/1000000}'
```

### Average read length
```bash
grep -v ">" [FASTQFILE] | wc | awk '{print calc ($3-$1)/$1}'
```

## CSV/TSV file

## Check if column in CSV file
```bash
head -n1 example.csv | tr "," "\n" | grep example_keyword
```

## Check if column in TSV file
```bash
head -n1 example.tsv | tr "\t" "\n" | grep example_keyword
```
