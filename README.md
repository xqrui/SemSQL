# SemSQL: Fine-Grained Semantic Modeling for Faithful Text-to-SQL

Official implementation of the paper:

> **SemSQL: Fine-Grained Semantic Modeling for Faithful Text-to-SQL**

Yongqiang Zhang, Qirui Xiang, Yunyao Zhang, Zikai Song, and Tao Guan
Huazhong University of Science and Technology

## Overview

Text-to-SQL systems may generate SQL queries that execute successfully but fail to preserve the semantics expressed in the original question. We refer to this problem as **semantic drift**.

SemSQL explicitly models question semantics along four complementary dimensions:

* **Projection:** what information should be returned;
* **Predicate:** which conditions and values should be preserved;
* **Relational Grounding:** which tables, columns, and relation paths should be used;
* **Computation:** how the answer should be derived and at what granularity.

The resulting semantic representation guides:

* candidate generation;
* SQL repair;
* candidate selection.

<p align="center">
  <img src="assets/framework.png" width="900">
</p>

## Main Results

Execution accuracy on BIRD Dev and Spider Test:

| Backbone                      | BIRD Dev | Spider Test |
| ----------------------------- | -------: | ----------: |
| GPT-4o-mini + SemSQL          |     68.8 |        84.7 |
| Gemma 3-27B-Instruct + SemSQL | **70.4** |    **87.6** |
| DeepSeek-V4-Flash + SemSQL    |     68.7 |        86.1 |

SemSQL improves the reproduced DeepEye-SQL backbone across all evaluated model–benchmark combinations, with gains of up to:

* **+1.3 points on BIRD Dev**
* **+1.1 points on Spider Test**




