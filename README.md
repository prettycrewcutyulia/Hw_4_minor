# hse_hw4_hic
 
Выбранная хромосома: chr2L 7 000 000 - 8 500 000
Colab: https://github.com/prettycrewcutyulia/Hw_4_minor/blob/main/data/colab/hw_4_nic.ipynb

## a. получить информацию и атрибуты матрицы Hi-C с помощью cooler.info

### HiC1.dm3.mapq_30.1000.mcool

```
{'bin-size': 20000,
 'bin-type': 'fixed',
 'creation-date': '2023-04-06T04:39:00.281457',
 'format': 'HDF5::Cooler',
 'format-url': 'https://github.com/open2c/cooler',
 'format-version': 3,
 'generated-by': 'cooler-0.8.11',
 'genome-assembly': 'unknown',
 'metadata': {},
 'nbins': 6024,
 'nchroms': 7,
 'nnz': 7122786,
 'storage-mode': 'symmetric-upper',
 'sum': 63912926}
```
### HiC2.dm3.mapq_30.1000.mcool
```
{'bin-size': 20000,
 'bin-type': 'fixed',
 'creation-date': '2023-04-06T04:16:47.610855',
 'format': 'HDF5::Cooler',
 'format-url': 'https://github.com/open2c/cooler',
 'format-version': 3,
 'generated-by': 'cooler-0.8.11',
 'genome-assembly': 'unknown',
 'metadata': {},
 'nbins': 6024,
 'nchroms': 7,
 'nnz': 7386462,
 'storage-mode': 'symmetric-upper',
 'sum': 61819050}
```
### HiC3.dm3.mapq_30.1000.mcool
```
{'bin-size': 20000,
 'bin-type': 'fixed',
 'creation-date': '2023-04-06T04:23:11.844138',
 'format': 'HDF5::Cooler',
 'format-url': 'https://github.com/open2c/cooler',
 'format-version': 3,
 'generated-by': 'cooler-0.8.11',
 'genome-assembly': 'unknown',
 'metadata': {},
 'nbins': 6024,
 'nchroms': 7,
 'nnz': 4852836,
 'storage-mode': 'symmetric-upper',
 'sum': 62878716}
```
### HiC4.dm3.mapq_30.1000.mcool
```
{'bin-size': 20000,
 'bin-type': 'fixed',
 'creation-date': '2023-04-06T04:53:24.060433',
 'format': 'HDF5::Cooler',
 'format-url': 'https://github.com/open2c/cooler',
 'format-version': 3,
 'generated-by': 'cooler-0.8.11',
 'genome-assembly': 'unknown',
 'metadata': {},
 'nbins': 6024,
 'nchroms': 7,
 'nnz': 5689703,
 'storage-mode': 'symmetric-upper',
 'sum': 74497702}
```

## b. открыть объект cooler как сбалансированную матрицу для внутрихромосомных контактов

### HiC1.dm3.mapq_30.1000.mcool
![](/data/screenshots/b1.png)
### HiC2.dm3.mapq_30.1000.mcool
![](/data/screenshots/b2.png)
### HiC3.dm3.mapq_30.1000.mcool
![](/data/screenshots/b3.png)
### HiC4.dm3.mapq_30.1000.mcool
![](/data/screenshots/b4.png)

## c. получить таблицу с координатами и контактами, они сбалансированные или нет?
![](/data/screenshots/c1.png)
![](/data/screenshots/c2.png)

### Вывод:
Как мы можем наблюдать по колонке count контакты не сбалансированные

## d. получить таблицу в командной строке командой cooler dump
Все файлы представлены в папке data
### HiC1.dm3.mapq_30.1000.mcool
https://github.com/prettycrewcutyulia/Hw_4_minor/blob/main/data/coolerInfo/coolerInfo1.tcv

### HiC2.dm3.mapq_30.1000.mcool
https://github.com/prettycrewcutyulia/Hw_4_minor/blob/main/data/coolerInfo/coolerInfo2.tcv

### HiC3.dm3.mapq_30.1000.mcool
https://github.com/prettycrewcutyulia/Hw_4_minor/blob/main/data/coolerInfo/coolerInfo3.tcv

### HiC4.dm3.mapq_30.1000.mcool
https://github.com/prettycrewcutyulia/Hw_4_minor/blob/main/data/coolerInfo/coolerInfo4.tcv


## e. посмотрите таблицу с бинами, какие столбцы там присутствуют?
![](/data/screenshots/e1.png)
![](/data/screenshots/e2.png)

Присутствуют столбцы:
chrom - имя хромосомы
start - позиция начала бина
end - позиция конца бина
weight - вес бина

## f. постройте кривые зависимости число контактов от расстояния для выбранной хромосомы (в логарифмических-координатах) для 4х реплик. Сравните их.

### Общий график
![](/data/screenshots/f1.png)
### HiC1.dm3.mapq_30.1000.mcool
![](/data/screenshots/f2.png)

### HiC2.dm3.mapq_30.1000.mcool
![](/data/screenshots/f3.png)

### HiC3.dm3.mapq_30.1000.mcool
![](/data/screenshots/f4.png)

### HiC4.dm3.mapq_30.1000.mcool
![](/data/screenshots/f5.png)

#### Вывод:
Можно заметить, что графики реплик крайне похоже и начинают значительно для нас отличаться только в конце, что связано с увеличением воздействия шума
