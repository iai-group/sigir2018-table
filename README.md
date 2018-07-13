# On-the-fly Table Generation

This repository contains resources developed within the following paper:

> S. Zhang and K. Balog. On-the-fly Table Generation. In: *Proceedings of SIGIR 2018*, July 2018.


## Test collection

The table corpus is [WikiTables](http://websail-fe.cs.northwestern.edu/TabEL/), which comprises 1.6M tables extracted from Wikipedia. We proproceeed it and make it public downloadable [here](http://iai.group/downloads/smart_table/WP_tables.zip).



## Methods and results


The `runfile/` folder contains the table rankings generated by the various methods (in TREC runfile format).


(I) Core Column Entity Retrieval (The `runfile/CCER/` folder)

|  |  | QS-1 || QS-2||
| -- | -- | -- | -- | -- | -- |
| **Method** | **Runfile**  | NDCG@5 | NDCG@10 | NDCG@5 | NDCG@10|
| Query-based Entity Ranking (Round \#0)|
| LM | `QS1_lm.txt` | 0.2419 | 0.2591 | 0.0708 | 0.0823 |
| DRRM_TKS (e_d) | `QS1/2_ed.txt` | 0.2015 | 0.2028 | 0.0501 | 0.0540 |
| DRRM_TKS (e_q) | `QS1/2_ep.txt` | 0.1780 | 0.1808 | 0.1089 | 0.1083 |
| Combined | `QS1/2_combined.txt` | 0.2821 | 0.2834 | 0.0852 | 0.0920 |
|Schema-assisted Entity Ranking|
|Round \#1|`QS1/2_R1.txt`|0.3012 | 0.2892 | 0.1232 | 0.1201|
|Round \#2|`QS1/2_R2.txt`|0.3369| 0.3221 |0.1307 | 0.1264 |
|Round \#3|`QS1/2_R3.txt`|0.3445|0.3250|0.1345| 0.1270|
|Oracle |`QS1/2_Oracle.txt`|0.3518|0.3355|0.1587|0.1555|

(II) Schema Deternimation (The `runfile/SD/` folder)

|  |  | QS-1 || QS-2||
| -- | -- | -- | -- | -- | -- |
| **Method** | **Runfile**  | NDCG@5 | NDCG@10 | NDCG@5 | NDCG@10|
| Query-based Entity Ranking (Round \#0)|
| CP | `QS1/2_CP.txt` | 0.0561 | 0.0675 | 0.1770 | 0.2092|
| DRRM\_TKS | `QS1/2_DRRM.txt` | 0.0380 | 0.0427 | 0.0920 | 0.1415 |
| Combined | `QS1/2_combined.txt` | 0.0786 | 0.0878 | 0.2310 | 0.2695 |
|Schema-assisted Entity Ranking|
|Round \#1|`QS1/2_R1.txt`|0.1676 | 0.1869 | 0.3342 | 0.3845|
|Round \#2|`QS1/2_R2.txt`|0.1775 | 0.2046 |0.3614 | 0.4143 |
|Round \#3|`QS1/2_R3.txt`|0.1910|0.2136|0.3683| 0.4350|
|Oracle |`QS1/2_Oracle.txt`|0.2002|0.2434|0.4239|0.4825|

(III) Vavlue Lookup (The `runfile/VL/` folder)

|  |  | QS-1 || QS-2||
| -- | -- | -- | -- | -- | -- |
| **Method** | **Runfile**  | MAP | MRR | MAP | MRR|
| KB | `QS1/2_kb.txt` | 0.7759 | 0.7990 | 0.0745 | 0.0745 |
| TC | `QS1_TC.txt` | 0.1614 | 0.1746 | 0.9564 | 0.9564 |
| KB+TC | `QS1/2_all.txt` | 0.9270 | 0.9427 | 0.9564 | 0.9564 |

The evaluation scores are reported using [trec_eval](https://github.com/usnistgov/trec_eval).


## Citation
```
@inproceedings{Zhang:2018:OTG,
 author = {Zhang, Shuo and Balog, Krisztian},
 title = {On-the-fly Table Generation},
 booktitle = {The 41st International ACM SIGIR Conference on Research \&\#38; Development in Information Retrieval},
 series = {SIGIR '18},
 year = {2018},
 isbn = {978-1-4503-5657-2},
 location = {Ann Arbor, MI, USA},
 pages = {595--604},
 numpages = {10},
 url = {http://doi.acm.org/10.1145/3209978.3209988},
 doi = {10.1145/3209978.3209988},
 acmid = {3209988},
 publisher = {ACM},
 address = {New York, NY, USA},
 keywords = {entity-oriented search, structured data search, table generation},
}
```

## Contact
If you have any questions, please contact Shuo Zhang at shuo.zhang@uis.no.
