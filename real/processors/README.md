## BENCHMARKS
|Model|#POs|Exhaustive encoding||Single-literal encoding||Heuristic encoding (SA)||SAT-based encoding||
|:---------------:|:---------------:|:---------------:|:---------------:|:---------------:|:---------------:|:---------------:|:---------------:|:---------------:|:---------------:|
|||**Best area**|**Runtime**|**Best area**|**Runtime**|**Best area**|**Runtime**|**Best area**|**Runtime**|
|ARM Cortex M0+ |	11	|	-	|	-	|	**167,090 (5)**|	1	|	191,090 (4)|	16	|	204,800 (4)|	2	|
|		|	8 	|	133,090 (3)|	1292	|	**126,300 (5)**|	1	|	143,680 (3)|	14	|	166,260 (3)|	2|
|TI MSP430 	|	8	|	**219,350 (4)**|	1982	|	255,570 (9)|	1	|	244,010 (4)|	16	|	-	|	-|
|		|	7	|	**171,330 (4)**|	1754	|	176,590 (9)|	1	|	185,750 (4)|	16	|	-	|	-|
|Intel 8051	|	9	|	-	|	-	|	**184,870 (8)**|	1	|	185,310 (3)|	16	|	195,890 (4)|	3|
|		|	8	|	**160,040 (3)**|	2075	|	161,450 (7)|	1	|	165,680 (3)|	15	|	195,760 (3)|	3|
|		|	7	|	**130,140 (3)**|	2092	|	140,410 (6)|	1	|	140,150 (3)|	15	|	143,550 (3)|	1|

___
___


## DESCRIPTION
Benchmark of the encoding approaches applied to different instructions set architecture subsets.
Unit of measure: Area: [μ^2 m] (opcode length in brackets), Runtime [s].

The file "benchmarks.txt" contains the results of the encoding processes applied to the models included into real folder.
It needs to be modified by the user who wants to add a new model into the set.

___
___

## REPRODUCING RESULTS
In order to reproduce the same result obtained, the interested user should follow the steps below.
1. Download **Workcraft** at the following website: http://www.workcraft.org/, in particular in the section _Download_.
2. Donwload the models included in this repository, or create a new model. It can be done by opening Workcraft and going into _Files_ -> _Open_, or _Files_ -> _Create work_ -> Conditional Partial Order Graphs (an interesting tutorial is present at http://www.workcraft.org/help/cpog_plugin).
3. Run **SCENCO** encoder present into the tab _Tools_ -> _Encoding_ selecting the options which the user want to use for the encoding process.
