# Process mining benchmarks

This directory contains benchmarks of some the traces extracted via some of the Process mining algorithms available.

## Comparison of algorithms for finding compact graph families
The following table compares several algorithms for deriving compact representations of graph families applied to these benchmarks. If you add a new benchmark, please modify the table accordingly.

Model _size_ is the number of graphs in a graph family, _area_ of hardware instruction decoder is given in μm^2 (with corresponding opcode length in brackets), _runtimes_ are given in seconds. Best area results are highlighted in bold. In the following benchmarks, the number of bits used for the encoding is equal to the minimum bits necessary to encode _n_ graphs.

<table>
  <tr>
    <th colspan="2">Algorithm →</th>
    <th colspan="2">Sequential encoding</th>
    <th colspan="2">Random search</th>
    <th colspan="2">Heuristic encoding</th>
  </tr>
  <tr>
    <td>Benchmark</td>
    <td>Size</td>
    <td width="80pt">Area</td>
    <td>Runtime</td>
    <td width="80pt">Area</td>
    <td>Runtime</td>
    <td width="80pt">Area</td>
    <td>Runtime</td>
  </tr>
  <tr>
    <td rowspan="1">BigLog1</td>
    <td>16</td>
    <td>893</td>
    <td>1</td>
    <td>884</td>
    <td>1</td>
    <td><strong>673</strong></td>
    <td>3</td>
  </tr>
  <tr>
    <td rowspan="1">Purchasetopay</td>
    <td>20</td>
    <td>994</td>
    <td>1</td>
    <td>1090</td>
    <td>1</td>
    <td><strong>903</strong></td>
    <td>4</td>
  </tr>
  <tr>
    <td rowspan="1">BigLog2</td>
    <td>26</td>
    <td>1312</td>
    <td>1</td>
    <td>1506</td>
    <td>1</td>
    <td><strong>1039</strong></td>
    <td>4</td>
  </tr>
  <tr>
    <td rowspan="1">Log2</td>
    <td>32</td>
    <td>1586</td>
    <td>1</td>
    <td>1681</td>
    <td>1</td>
    <td><strong>1245</strong></td>
    <td>4</td>
  </tr>
  <tr>
    <td rowspan="1">Incidenttelco</td>
    <td>77</td>
    <td>4762</td>
    <td>2</td>
    <td>4938</td>
    <td>2</td>
    <td><strong>4371</strong></td>
    <td>2</td>
  </tr>
  <tr>
    <td rowspan="1">svn_log</td>
    <td>92</td>
    <td>4080</td>
    <td>1</td>
    <td>4279</td>
    <td>1</td>
    <td><strong>3689</strong></td>
    <td>2</td>
  </tr>
  <tr>
    <td rowspan="1">telecom</td>
    <td>122</td>
    <td>6072</td>
    <td>1</td>
    <td>6430</td>
    <td>2</td>
    <td><strong>5944</strong></td>
    <td>3</td>
  </tr>
  <tr>
    <td rowspan="1">Colibrilog</td>
    <td>167</td>
    <td><strong>10783</strong></td>
    <td>4</td>
    <td>11455</td>
    <td>4</td>
    <td>11086</td>
    <td>6</td>
  </tr>
  <tr>
    <td rowspan="1">Caise2014</td>
    <td>401</td>
    <td>47857</td>
    <td>21</td>
    <td>50578</td>
    <td>21</td>
    <td><strong>47157</strong></td>
    <td>38</td>
  </tr>
  <tr>
    <td rowspan="1">Log1-filtered</td>
    <td>402</td>
    <td><strong>14902</strong></td>
    <td>3</td>
    <td>20006</td>
    <td>5</td>
    <td>18559</td>
    <td>21</td>
  </tr>
  <tr>
    <td rowspan="1">Documentflow</td>
    <td>651</td>
    <td><strong>27599</strong></td>
    <td>12</td>
    <td>31148</td>
    <td>13</td>
    <td>30223</td>
    <td>59</td>
  </tr>
</table>

## Reproducing results
Follow these steps to reproduce the above results:
* Download the Workcraft framework: http://www.workcraft.org/.
* Open the models from this repository in Workcraft: `File` → `Open work`.
* Run the SCENCO graph encoding plugin: `Tools` → `Encoding` → `SCENCO`, selecting appropriate encoding algorithm in the plugin settings window.

If you cannot reproduce the results, please raise an issue: https://github.com/snowleopard/graph-families/issues/new.

### Note
The only approaches which are able to deal with a high amount of graphs (above 12/15) are the: Heuristic encoding, Random search and Sequential encoding. This is the reason why the benchmarks within the process-mining folder are performed with these three encoding methods only.
