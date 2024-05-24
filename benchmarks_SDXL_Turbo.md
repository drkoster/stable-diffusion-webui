# The following are benchmark results done with the following hardware

Dual socket AMD Epyc 7453
per socket: 4 channels of 3200mhz 64gb ram modules
Host os: Windows 11 pro workstation
After initial testing both root and classic scheduler made no measurable difference and has been omitted. 
Guest os: Ubuntu 22.04 lts
The Guest vm is provided with 128Gb of ram. Generation 2. 

The total number of physical cores is 56, 28 per socket.
Maximum number of logical cores is 112. 

Each benchmark set is grouped with changes in set count and resolution.
Set 1 - x will use resolution 512x512
Set 2 - x will use resolution 768x768
Set 3 - x will use resolution 1024x124

Each set has 3 subsets to test with sampling step 6, 8 and 12.
The column "vCPU`s" shows the assigned number of virtual cpu's through hyper-v

Version information:
Stable Diffusion webui: v1.9.3
Python: v3.10.12


## Global settings used for EACH test set:

Model   =   DreamshaperXL_v21TurboDPMSDE
Seed    =	2266374543
Sampler =	DPM++ SDE Karras
cfg     =	2

**Since we are using a Turbo model, low cfg and step count chosen**

## Benchmark set 1 / 512x512 results

### Benchmark set 1 - 1
steps   =	6
res     =	w512xh512

**Results**
| vCPU's | time taken |
| ------ | ---------- |
| 96 | 40.4 sec. |
| 80 | 39.2 sec. |
| 68 | 42.4 sec. |
| 56 | 43.2 sec. |


### Benchmark set 1 - 2
steps   =	8
res     =	w512xh512

**Results**
| vCPU's | time taken |
| ------ | ---------- |
| 96 | 54.2 sec. |
| 80 | 52.2 sec. |
| 68 | 56.2 sec. |
| 56 | 57.3 sec. |

### Benchmark set 1 - 3
steps   =	12
res     =	w512xh512

**Results**
| vCPU's | time taken |
| ------ | ---------- |
| 96 | 1 min. 21.8 sec. |
| 80 | 1 min. 18.7 sec. |
| 68 | 1 min. 25.8 sec. |
| 56 | 1 min. 28.3 sec. |

## Benchmark set 2 / 768x768 results

### Benchmark set 2 - 1
steps   =	6
res     =	w768xh768

| vCPU's | time taken |
| ------ | ---------- |
| 96 | 1 min. 21.4 sec. |
| 80 | 1 min. 25.5 sec. |
| 68 | 1 min. 33.6 sec. |
| 56 | 1 min. 35.0 sec. |

### Benchmark set 2 - 2
steps   =	8
res     =	w768xh768

| vCPU's | time taken |
| ------ | ---------- |
| 96 | 1 min. 50.7 sec. |
| 80 | 1 min. 56.0 sec. |
| 68 | 2 min. 5.8 sec. |
| 56 | 2 min. 8.7 sec. |

### Benchmark set 2 - 3
steps   =	12
res     =	w768xh768

| vCPU's | time taken |
| ------ | ---------- |
| 96 | 2 min. 48.5 sec.
| 80 | 2 min. 50.1 sec. |
| 68 | 3 min. 4.3 sec. |
| 56 | 3 min. 14.5 sec. |

## Benchmark set 3 / 1024x1024 results

### Benchmark set 3 - 1
steps   =	6
res     =	w1024xh1024

| vCPU's | time taken |
| ------ | ---------- |
| 96 | 2 min. 34.3 sec. |
| 80 | 2 min. 30.6 sec. | 
| 68 | 2 min. 55.0 sec. |
| 56 | 2 min. 52.9 sec. |

### Benchmark set 3 - 2
steps   =	8
res     =	w1024xh1024

| vCPU's | time taken |
| ------ | ---------- |
| 96 | 3 min. 25.7 sec. |
| 80 | 3 min. 23.5 sec. |
| 68 | 3 min. 51.3 sec. |
| 56 | 3 min. 54.0 sec. |

### Benchmark set 3 - 3
steps   =	12
res     =	w1024xh1024

| vCPU's | time taken |
| ------ | ---------- |
| 96 | 5 min. 7.9 sec. |
| 80 | 5 min. 5.5 sec. |
| 68 | 5 min. 44.8 sec.|
| 56 | 6 min. 5.2 sec. |