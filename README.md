# hse_hw3_chromhmm

## Отчет

### Содержание файлов и папок
- cellmarkfiletable.txt 
- data.zip - архив с данными, полученные с помощью ChromHMM
- HW3.ipynb - ноутбук, содержащий все запущенные команды
- HW3_bonus.ipynb - ноутук с кодом бонуса
- new_bed.zip - архив с *dense.bed файлом, у которого эпигенетические типы переименованы (результат бонуса)
- pics - папка с картинками ChromHMM
- genome_browser_pics - картинка с участками генома из GenomeBrowser

### Список гистоновых меток

В HW2 использовались данные по HL-60, но тут оказалось мало данных по модификациям, поэтому в HW3 использовалась **клеточная линия HMEC**.

**Файл контроля - Control.bam**, ссылка - http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHmecControlStdAlnRep1.bam

Гистоновая метка | Имя файла в проекте | Ссылка на файл для скачивания
---              | ---                 | ---
H3k27ac          | H3k27ac.bam         | http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHmecH3k27acStdAlnRep1.bam
H3k27me3         | H3k27me3.bam        | http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHmecH3k27me3StdAlnRep1.bam
H3k36me3         | H3k36me3.bam        | http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHmecH3k36me3StdAlnRep1.bam
H3k4me1          | H3k4me1.bam         | http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHmecH3k4me1StdAlnRep1.bam
H3k4me2          | H3k4me2.bam         | http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHmecH3k4me2StdAlnRep1.bam
H3k4me3          | H3k4me3.bam         | http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHmecH3k4me3StdAlnRep1.bam
H3k9ac           | H3k9ac.bam          | http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHmecH3k9acStdAlnRep1.bam
H3k09me3         | H3k9me3.bam         | http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHmecH3k09me3AlnRep1.bam
H4k20me1         | H4k20me1.bam        | http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHmecH4k20me1StdAlnRep1.bam
Ctcf             | Ctcf.bam            | http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneHmecCtcfStdAlnRep1.bam


### Картинки ChromHMM

![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/pics/HMEC_15_RefSeqTES_neighborhood.png)

![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/pics/HMEC_15_RefSeqTSS_neighborhood.png)

![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/pics/HMEC_15_overlap.png)

![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/pics/emissions_15.png)

![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/pics/transitions_15.png)

### Эпигенетические типы

Номер | Название                  | Описание | Картинка 
---   | ---                       | ---      | ---
1     | Active promoter           | Выражен в H3k9me3. Чаще всего находится на ядерной ламине. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/1.png)
2     | Weak promoter             | Чаще всего находится на ядерной ламине. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/2.png)
3     | Inactive/poised Promoter  | Выражен в H3k27me3. Чаще всего находится на ядерной ламине, RefSeqTES, RefSeqGene. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/3.png)
4     | Strong enhancer           | Выражен в H3k27me3, H3k4me1, H3k4me2. Чаще всего находится на CpG-островках, RefSeqExon, RefSeqTSS, RefSeqTES, RefSeqGene. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/4.png)
5     | Strong enhancer           | Выражен в H3k4me1, H3k4me2. Чаще всего находится на ядерной ламине, RefSeqGene. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/5.png)
6     | Weak/poised enhancer      | Выражен в H3k4me1, H3k4me2. Чаще всего находится на RefSeqTSS2kb, RefSeqTES. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/6.png)
7     | Weak/poised enhancer      | Выражен в H3k4me1, H3k4me2, H3k4me3. Чаще всего находится на CpG-островках, RefSeqExon, RefSeqTSS. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/7.png)
8     | Insulator                 | Выражен в H3k4me2, H3k4me3, H3k9ac, H3k27ac. Чаще всего находится на RefSeqExon, RefSeqTSS, RefSeqTSS2kb, CpG-островках. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/8.png)
9     | Transcriptional transition| Выражен в H3k4me1, H3k4me2, H3k27ac. Чаще всего находится на ядерной ламине, RefSeqGene. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/9.png)
10    | Transcriptional elongation| Выражен в H3k4me1, H3k4me2, H3k27ac. Чаще всего находится на ядерной ламине, RefSeqGene. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/10.png)
11    | Weak transcribed          | Выражен в H3k4me1, H3k27ac. Чаще всего находится на ядерной ламине, RefSeqGene. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/11.png)
12    | Polycomb-repressed        | Выражен в H3k4me1. Чаще всего находится на ядерной ламине, RefSeqGene. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/12.png)
13    | Heterochromatin; low signal| Выражен в H3k4me1, H3k36me3, H4k20me1. Чаще всего находится на RefSeqTES, RefSeqGene, RefSeqExon. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/13.png)
14    | Repetitive/Copy Number Variation| Выражен в H3k36me3. Чаще всего находится наRefSeqTES, RefSeqGene, RefSeqExon. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/14.png)
15    | Repetitive/Copy Number Variation| Выражен в Ctcf. Чаще всего находится на ядерной ламине. | ![](https://github.com/LanaShhh/hse_hw3_chromhmm/blob/main/genome_browser_pics/15.png)

### Все запущенные команды находятся в файле HW3.ipynb. Код бонуса находится в файле HW3_bonus.ipynb



