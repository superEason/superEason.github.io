---
title: Transducer Plan
mathjax: true
date: 2019-08-05 20:02:55
tags:
categories: 计划书
description: 
password:
notshow: 
---

<!-- more -->

# 设计指标

- 尺寸：$10mm^3 \to 1mm^3$
- 提供功率：$>10uW$
- 生物相容性：无铅……
- CMOS工艺相容性



# 方案调研

## 换能器类型

### 电磁与声比较：

- 人体能承受更大的超声波功率：
  - 人体能承受电磁波最大照射强度：$<100\mu W/mm^2$
  - 人体能承受超声波最大照射强度：$7200\mu W/mm^2$
- 高频电磁波在体内衰减更大：
  - 超声波在脑组织内衰减：$1dB/(MHz*cm)$
  - 超声波在颅骨内衰减：$10dB/(MHz*cm)$
  - 电磁波在脑组织内衰减：$>2dB/(GHz*cm)$
- 超声波不受电磁环境干扰

### 参考文献：

- Amin Arbabian, *Sound Technologies, Sound Bodies





### 可供选择的超声波换能器方案：

- PZT
- PMUT
- CMUT

### 比较

- PZT无法与CMOS工艺兼容
  - CMUT可以直接兼容
  - PMUT可以兼容，但需要采用一些材料和方法

- CMUT 有更高的带宽：
  - CMUT：>100%
  - PMUT：>50%
- CMUT 有更高的机电耦合系数
  - CMUT：>70%
  - PMUT：约5%，最高可到45%
- PMUT消耗功率更小，CMUT需要大电压直流偏置(在无源植入性设备中不可能实现)

### 参考文献：

Hongsoo Choi *Review of piezoelectric micromachined ultrasonic transducers and their applications*



## 工作频率

- 波长、频率与波速的关系：$\lambda=c/f$，由于器件尺寸约为$1mm^2$，所以波长也应该在毫米量级，组织中声速约为$1500m/s$，因此，频率约为$1.5MHz$
- 参考文献指出：建议工作频率范围为200 kHz-1.2 MHz。如果一个换能器尺寸(小于1毫米)比功率传输效率更重要，那么工作频率的选择可能包括高于1.2 MHz的频率。
- 参考文献指出：因此，设计功率传递系统，使其工作在1-2 MHz左右，在聚焦和传播损耗之间保持一个合理的平衡
- 理论计算与仿真结果均显示，会过高频率（$>5MHz$）导致巨大的能量衰减

### 参考文献

- Amin Arbabian, *Sound Technologies, Sound Bodies*
- Shaul Ozeri, Doron Shmilovitz, *Ultrasonic transcutaneous energy transfer for powering implanted devices*

**综上，结合PMUT器件的特性，考虑到未来更小型化的需求，选择$1-3MHz$频率较为合适**



## 压电材料

| Materials                   | Coefficient($pC/N$) | Typical performances |
| --------------------------- | ----------- | -------------------- |
| $ZnO$ 纳米线                | 10 | $58V$   $134uA$ |
| $MoS_2$纳米片               |  |  |
| $WSe_2$纳米片               |             |                      |
| PMN-PZT/PT薄膜              | 2000 | $17.18mW/cm^3$ |
| PZT薄膜                     | 700 | $200V$  $35uA$ |
| 铌酸碱性(KNLN)薄膜 | 310 |                      |
| $BaTiO_3$ | 190 | $1V_{pp}$    $7 mW/cm^3$ |
| AlN薄膜                     | 5 |                      |
| PVDF薄膜                    | 3000 |                      |
| 多孔聚丙烯薄膜              | 600 |                      |
| 聚二甲基硅氧烷压电驻极体薄膜  |             |                      |
| PET/EVA/PET压电驻极体薄膜           | 6300 |                      |
| 氟化乙烯丙烯压电驻极体薄膜     |             |                      |
| M13 噬菌体薄膜                |             |                      |
| 鱼鳔薄膜                      | 22 |                      |



### 无机压电材料

#### 压电晶体

#### ZnO

采用水热法可方便地制备纤锌型ZnO纳米线，

#### 压电陶瓷



### 压电聚合物

#### PVDF



### 生物压电材料





## 制造工艺



# 设计方案

材料：PZT-5A或者PMN-PZT

结构：Si/SiO2/Pt/PZT5A/Pt

尺寸：直径1mm，厚度1微米

## 实验步骤

- 批量制作PMUT(不同尺寸)，在探针台上，用超声探头施加超声波，选取用足够输出电压的的PMUT器件
- 

