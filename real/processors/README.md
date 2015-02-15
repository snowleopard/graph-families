# Processor benchmarks

This directory contains benchmarks for the following processors: [ARM Cortex M0+](https://en.wikipedia.org/wiki/ARM_Cortex-M#Cortex-M0.2B), [Intel 8051](https://en.wikipedia.org/wiki/Intel_MCS-51), and [Texas Instruments MSP430](https://en.wikipedia.org/wiki/TI_MSP430).

## Comparison of algorithms for findning compact graph families
The following table compares several algorithms for deriving compact representations of graph families applied to these benchmarks. If you add a new benchmark, please modify the table accordingly.

Model _size_ is the number of graphs in a graph family, _area_ of hardware instruction decoder is given in μm^2 (with corresponding opcode length in brackets), _runtimes_ are given in seconds. Best area results are highlighted in bold.

<table>
  <tr>
    <th colspan="2">Algorithm →</th>
    <th colspan="2">Exhaustive encoding</th>
    <th colspan="2">Single-literal encoding</th>
    <th colspan="2">Heuristic encoding</th>
    <th colspan="2">SAT-based encoding</th>
  </tr>
  <tr>
    <td>Benchmark</td>
    <td>Size</td>
    <td>Area</td>
    <td>Runtime</td>
    <td>Area</td>
    <td>Runtime</td>
    <td>Area</td>
    <td>Runtime</td>
    <td>Area</td>
    <td>Runtime</td>
  </tr>
  <tr>
    <td rowspan="2">ARM Cortex M0+</td>
    <td>8</td>
    <td>133 (3)</td>
    <td>1292</td>
    <td><strong>126 (5)</strong></td>
    <td>1</td>
    <td>144 (3)</td>
    <td>14</td>
    <td>166 (3)</td>
    <td>2</td>
  </tr>
  <tr>
    <td>11</td>
    <td>-</td>
    <td>-</td>
    <td><strong>167 (5)</strong></td>
    <td>1</td>
    <td>191 (4)</td>
    <td>16</td>
    <td>205 (4)</td>
    <td>2</td>
  </tr>
  <tr>
    <td rowspan="3">Intel 8051</td>
    <td>7</td>
    <td><strong>130 (3)</strong></td>
    <td>2092</td>
    <td>140 (6)</td>
    <td>1</td>
    <td>140 (3)</td>
    <td>15</td>
    <td>144 (3)</td>
    <td>1</td>
  </tr>
  <tr>
    <td>8</td>
    <td><strong>160 (3)</strong></td>
    <td>2075</td>
    <td>161 (7)</td>
    <td>1</td>
    <td>166 (3)</td>
    <td>15</td>
    <td>196 (3)</td>
    <td>3</td>
  </tr>
  <tr>
    <td>9</td>
    <td>-</td>
    <td>-</td>
    <td>185 (8)</td>
    <td>1</td>
    <td><strong>185 (3)</strong></td>
    <td>16</td>
    <td>196 (4)</td>
    <td>3</td>
  </tr>
  <tr>
    <td rowspan="2">TI MSP430</td>
    <td>7</td>
    <td><strong>171 (4)</strong></td>
    <td>1754</td>
    <td>177 (9)</td>
    <td>1</td>
    <td>186 (4)</td>
    <td>16</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>8</td>
    <td><strong>219 (4)</strong></td>
    <td>1982</td>
    <td>256 (9)</td>
    <td>1</td>
    <td>244 (4)</td>
    <td>16</td>
    <td>-</td>
    <td>-</td>
  </tr>
</table>

## Reproducing results
Follow these steps to reproduce the above results:
* Download the Workcraft framework: http://www.workcraft.org/.
* Open the models from this repository in Workcraft: `File` → `Open work`.
* Run the SCENCO graph encoding plugin: `Tools` → `Encoding` → `SCENCO`, selecting appropriate encoding algorithm in the plugin settings window.

If you cannot reproduce the results, please raise an issue: https://github.com/snowleopard/graph-families/issues/new.
