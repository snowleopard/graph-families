# Processor benchmarks

This directory contains benchmarks for the following processors: [ARM Cortex M0+](https://en.wikipedia.org/wiki/ARM_Cortex-M#Cortex-M0.2B), [Intel 8051](https://en.wikipedia.org/wiki/Intel_MCS-51), and [Texas Instruments MSP430](https://en.wikipedia.org/wiki/TI_MSP430).

## Comparison of algorithms for finding compact graph families
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
    <td width="80pt">Area (bits)</td>
    <td>Runtime</td>
    <td width="80pt">Area (bits)</td>
    <td>Runtime</td>
    <td width="80pt">Area (bits)</td>
    <td>Runtime</td>
    <td width="80pt">Area (bits)</td>
    <td>Runtime</td>
  </tr>
  <tr>
    <td rowspan="8">ARM Cortex M0+</td>
    <td>4</td>
    <td><strong>123 (2)</strong></td>
    <td>1</td>
    <td>148 (4)</td>
    <td>1</td>
    <td><strong>123 (2)</strong></td>
    <td>2</td>
    <td><strong>123 (2)</strong></td>
    <td>1</td>
  </tr>
  <tr>
    <td>5</td>
    <td><strong>124 (3)</strong></td>
    <td>181</td>
    <td>157 (5)</td>
    <td>1</td>
    <td>135 (3)</td>
    <td>3</td>
    <td>155</td>
    <td>1</td>
  </tr>
  <tr>
    <td>6</td>
    <td>161 (3)</td>
    <td>539</td>
    <td><strong>144 (5)</strong></td>
    <td>1</td>
    <td>172 (3)</td>
    <td>3</td>
    <td>182 (3)</td>
    <td>1</td>
  </tr>
  <tr>
    <td>7</td>
    <td>171 (3)</td>
    <td>1234</td>
    <td><strong>144 (5)</strong></td>
    <td>1</td>
    <td>176 (3)</td>
    <td>3</td>
    <td>172 (3)</td>
    <td>1</td>
  </tr>
  <tr>
    <td>8</td>
    <td>133 (3)</td>
    <td>1292</td>
    <td><strong>126 (5)</strong></td>
    <td>1</td>
    <td>152 (3)</td>
    <td>3</td>
    <td>166 (3)</td>
    <td>2</td>
  </tr>
  <tr>
    <td>9</td>
    <td>-</td>
    <td>-</td>
    <td><strong>160 (5)</strong></td>
    <td>1</td>
    <td>179 (4)</td>
    <td>4</td>
    <td>187 (4)</td>
    <td>1</td>
  </tr>
  <tr>
    <td>10</td>
    <td>-</td>
    <td>-</td>
    <td><strong>179 (5)</strong></td>
    <td>1</td>
    <td>192 (4)</td>
    <td>4</td>
    <td>180 (4)</td>
    <td>1</td>
  </tr>
  <tr>
    <td>11</td>
    <td>-</td>
    <td>-</td>
    <td><strong>169 (5)</strong></td>
    <td>1</td>
    <td>198 (4)</td>
    <td>4</td>
    <td>205 (4)</td>
    <td>2</td>
  </tr>
  <tr>
    <td rowspan="13">Intel 8051</td>
    <td>4</td>
    <td>93 (2)</td>
    <td>1</td>
    <td><strong>85 (3)</strong></td>
    <td>1</td>
    <td>93 (2)</td>
    <td>1</td>
    <td>93</td>
    <td>1</td>
  </tr>
  <tr>
    <td>5</td>
    <td><strong>94 (3)</strong></td>
    <td>173</td>
    <td>95 (4)</td>
    <td>1</td>
    <td><strong>94 (3)</strong></td>
    <td>2</td>
    <td>96 (3)</td>
    <td>1</td>
  </tr>
  <tr>
    <td>6</td>
    <td><strong>125 (3)</strong></td>
    <td>544</td>
    <td>136 (5)</td>
    <td>1</td>
    <td><strong>125 (3)</strong></td>
    <td>3</td>
    <td>147 (3)</td>
    <td>1</td>
  </tr>
  <tr>
    <td>7</td>
    <td><strong>130 (3)</strong></td>
    <td>2092</td>
    <td>140 (6)</td>
    <td>1</td>
    <td>140 (3)</td>
    <td>3</td>
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
    <td>3</td>
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
    <td>3</td>
    <td>196 (4)</td>
    <td>3</td>
  </tr>
  <tr>
    <td>10</td>
    <td>-</td>
    <td>-</td>
    <td><strong>333(9)</strong></td>
    <td>2</td>
    <td>335(4)</td>
    <td>3</td>
    <td>361(5)</td>
    <td>5</td>
  </tr>
  <tr>
    <td>15</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>492(4)</td>
    <td>4</td>
    <td><strong>444(9)</strong></td>
    <td>36</td>
  </tr>
  <tr>
    <td>20</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td><strong>660(5)</strong></td>
    <td>4</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>25</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td><strong>942(5)</strong></td>
    <td>4</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>30</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td><strong>1256(5)</strong></td>
    <td>4</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>35</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td><strong>1615(6)</strong></td>
    <td>5</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>37</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td><strong>1645(6)</strong></td>
    <td>5</td>
    <td>-</td>
    <td>-</td>
  </tr>
    <td rowspan="5">TI MSP430</td>
    <td>4</td>
    <td><strong>116 (2)</strong></td>
    <td>2</td>
    <td>135 (4)</td>
    <td>1</td>
    <td><strong>116 (2)</strong></td>
    <td>4</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>5</td>
    <td><strong>129 (3)</strong></td>
    <td>184</td>
    <td>150 (6)</td>
    <td>1</td>
    <td>140 (3)</td>
    <td>4</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>6</td>
    <td><strong>159 (3)</strong></td>
    <td>560</td>
    <td>165 (7)</td>
    <td>1</td>
    <td><strong>159 (3)</strong></td>
    <td>4</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>7</td>
    <td><strong>171 (4)</strong></td>
    <td>1754</td>
    <td>177 (9)</td>
    <td>1</td>
    <td>186 (4)</td>
    <td>4</td>
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
    <td>4</td>
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
