# hse22_project

[colab](https://colab.research.google.com/drive/1PpAogbwOd69RhA8lv2XTInbBlvVAOV-9?usp=sharing)

## Выбранные геномы

| Organism | GC% |
| ----------- | ----------- |
| Leishmania braziliensis | 57,7282 |
| Leishmania major strain Friedlin | 59,7114 |
| Leishmania sp. Ghana 2012 | 59,6694 |
| Leishmania mexicana | 59,7793 |
| Leishmania tarentolae | 57,4 |

## Анализ аннотированных генов, предсказание Z-DNA
| Организм           |   Число генов |   Длина генома |   Длина покрытия экзонами |   Доля покрытия экзонами |   Количество участков zh-score > 500 |   Общая длина участков |   Количество предсказанных Z-DNA |
|:-------------|--------------:|---------------:|--------------------------:|-------------------------:|-------------------------------------:|-----------------------:|---------------------------------:|
| braziliensis |          8463 |       32068771 |                  15607007 |                       49 |                                 5110 |                  55226 |                           231164 |
| Friedlin     |          9388 |       32855089 |                  15739440 |                       48 |                                 8659 |                  94344 |                           268986 |
| Ghana        |          8119 |       35953538 |                  14915813 |                       41 |                                 8503 |                  91738 |                           295535 |
| mexicana     |          8249 |       32108741 |                  15408420 |                       48 |                                 8416 |                  91030 |                           273291 |
| tarentolae   |          8703 |       35416496 |                  15837259 |                       45 |                                 9224 |                 101250 |                           296165 |

## Гисторграммы распределения в логарифмической шкале

| Организм | Гистограмма |
| -------- | ----------- |
| braziliensis | ![alt text](https://github.com/messlav/hse22_project/blob/main/imgs/gist2_braziliensis.png) |
| Friedlin | ![alt text](https://github.com/messlav/hse22_project/blob/main/imgs/gist2_friedlin.png) |
| Ghana | ![alt text](https://github.com/messlav/hse22_project/blob/main/imgs/gist2_ghana.png) | 
| mexicana | ![alt text](https://github.com/messlav/hse22_project/blob/main/imgs/gist2_mexicana.png) | 
| tarentolae | ![alt text](https://github.com/messlav/hse22_project/blob/main/imgs/gist2_tarentolae.png) |

## Предсказания участков Z-DNA

| Организм | Визуализация |
| -------- | ----------- |
| braziliensis | ![alt text](https://github.com/messlav/hse22_project/blob/main/imgs/inter_braz.png) |
| Friedlin | ![alt text](https://github.com/messlav/hse22_project/blob/main/imgs/inter_fried.png) |
| Ghana | ![alt text](https://github.com/messlav/hse22_project/blob/main/imgs/inter_ghana.png) | 
| mexicana | ![alt text](https://github.com/messlav/hse22_project/blob/main/imgs/inter_mexicana.png) | 
| tarentolae | ![alt text](https://github.com/messlav/hse22_project/blob/main/imgs/inter_taren.png) |

## Гомологичные кластеры
Предисловие: на данном ключевом этапе произошли какие-то жуткие проблемы. Во-первых, proteinortho5 за 12 часов колаба выполнилась на 80%, думаю из-за больших размеров файлов с белками. К сожалению, не на убунте (на маке или другом линуксе), установить proteinortho5 это нерешаемая задача, т.к. авторы при переходе на новую версию, полностью стерли старую. proteinortho обновленной версии работает буквально минут 10, однако выдавало очень сомнительные результаты, из-за которых и возникло множество проблем. Что в итоге вышло:

Всего кластеров: 30919.

В кластере 2 оказалось всего пару геномов. Гистограмма: https://github.com/messlav/hse22_project/blob/main/imgs/clusters.png

Таблица с информацией по выбранным кластерам (не более 10 шт):

| cluster | organism | product accession | name                                 | fucntion                      |
| ------- | ---------| ------------------| ------------------------------------ | ----------------------------- |
| 0       | Friedlin | XP_001563956.1    | conserved hypothetical protein       | not been functionally characterized | 
| 1       | Friedlin | XP_003723036.1	   | putative kinesin heavy chain         | controls neuronal activity |
| 2       | Friedlin | XP_001564844.1    | conserved hypothetical protein       | not been functionally characterized |
| 3       | Friedlin | XP_001567415.1	   | putative profilin                    | not been functionally characterized |
| 4       | Friedlin | XP_001568591.1.   | inositol phosphorylceramide synthase | catalyses the transfer of phosphorylinositol from the phosphoglycerolipid phosphatidylinositol to the C-1 hydroxyl group of (phyto)ceramide |
| 5       | Ghana    | GET87615.1        | P-type ATPase, putative              | drive the uptake and/or efflux of cations against tremendous concentration gradients |
| 6       | Ghana    | GET87733.1        | hypothetical protein, conserved      | have not been functionally characterized |
| 7       | Ghana    | GET90982.1        | hypothetical protein, conserved      | have not been functionally characterized |
| 8       | Ghana    | GET91974.1        | hypothetical protein                 | have not been functionally characterized |
| 9       | Ghana    | GET93398.1        | hypothetical protein, conserved      | have not been functionally characterized |

## Множественное белковое выравнивание для каждого выбранного кластера

Для каждого кластера был создан необходимый файл с информацией о нем, после было произведено выравнивание ClustalW. Полученный файлы находятся в папке data, под названием cluster_aligned.txt

## Визуализация расположения участков Z-DNA для каждого выбранного кластера

Подписи на картинках означают не название гена, а название генома, в котором этот ген

Cluster 1

[!alt text](https://github.com/messlav/hse22_project/blob/main/imgs/clust_zdna1.png)
[!alt text](https://github.com/messlav/hse22_project/blob/main/imgs/clust_zdna2.png)

Cluster 2

[!alt text](https://github.com/messlav/hse22_project/blob/main/imgs/clust_zdna3.png)
[!alt text](https://github.com/messlav/hse22_project/blob/main/imgs/clust_zdna4.png)
