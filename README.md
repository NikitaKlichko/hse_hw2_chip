# Домашнее задание №2.Chip-seq.

###### Кличко Никита

## Анализ FastQC

В результате анализа было получено, что на всех 3-х образцах программа выдает Warning на "Per sequence GC content". После подрезаний Warning остаются,а качество чтений немного увеличивается. В целом улучшения незначительны, поэтому, думаю, можно было бы работать с исходными fastq файлами. Далее идет работа уже с подрезанными чтениями.
Рассмотрим основные элементы FastQC до и после подрезаний. 

**ENCFF000AQW**

| До| После | 
--- | ---  
![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/Aqw_stat.PNG) | ![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/Aqw_trim_stat.PNG) |
![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqw_seq.PNG) | ![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqw_trim_seq.PNG) | 
![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqw_tile.PNG) | ![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqw_trim_tile.PNG) | 
![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqw_gc.PNG) | ![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqw_trim_gc.PNG) | 

**ENCFF000AQX** 

| До| После | 
--- | ---  
![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqx_stat.PNG) | ![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqx_trim_stat.PNG) |
![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqx_seq.PNG) | ![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqx_trim_seq.PNG) | 
![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqx_tile.PNG) | ![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqx_trim_tile.PNG) | 
![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqx_gc.PNG) | ![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aqx_trim_gc.PNG) | 

**ENCFF000AOF** 

| До| После | 
--- | ---  
![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aof_stat.PNG) | ![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aof_trim_stat.PNG) |
![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aof_seq.PNG) | ![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aof_trim_seq.PNG) | 
![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aof_tile.PNG) | ![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aof_trim_tile.PNG) | 
![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aof_gc.PNG) | ![](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/aof_trim_gc.PNG) | 
 
 ## Статистика по чтениям
 
 | Chip-seq| Total reads | Aligned exactly 1 time| Aligned >1 times | aligned 0 times |
--- | --- | --- | --- | --- 
ENCFF000AQW | 37839216 | 1739301 (4.60%) | 6131221 (16.20%) | 29968694 (79.20%) | 
ENCFF000AQX | 22712939 | 1028452 (4.53%) | 3696690 (16.28%)	 | 17987797 (79.20%) |  
ENCFF000AOF(control) | 	39460514 | 1799863 (4.56%) | 5619839 (14.24%)	 | 32040812 (81.20%) | 

## Сравнение результатов 
Диаграммы Венна:
![alt-text-1](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/venn1.PNG) ![alt-text-2](https://github.com/NikitaKlichko/hse_hw2_chip/blob/main/imgs/venn2.PNG)
