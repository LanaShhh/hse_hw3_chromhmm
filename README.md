# hse_hw3_chromhmm

## Отчет

### Содержание файлов и папок
- cellmarkfiletable.txt 
- data.zip - архив с данными, полученные с помощью ChromHMM
- HW3.ipynb - ноутбук, содержащий все запущенные команды
- pics - папка с картинками ChromHMM

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



