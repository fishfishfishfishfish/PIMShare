![logo](img/logo-no-background.png)
Experiment code of `PIMShare: Scheduling Inference to Multiple Neural Networks for Processing-in-memory Accelerator` for reproducubility.

## file description
- NetStructure: store netstructure file that defined by NeuroSIM. Additionally, we include a extra column to represent the padding size.
- NeuroSIMOut: simulation result obtianed from NeuroSIM simulation. For each model, include following attributes:
    - DNN: DNN name
    - V_nn: memory space for storing the DNN weights
    - C: number of crossbars for storing the DNN
    - C_tile: number of tiles for storing the DNN
    - V: memory space for storing the DNN input
    - num computation: number of addition and multiplication operation to process one input
    - read latency: read latency for processing one input from NeuroSIM simulation
    - write latency: write latency for storing the DNN model from NeuroSIM simulation
    - ADC(ns): latency cost by ADC for processing one input from NeuroSIM simulation
    - Accumulation(ns):	latency cost by on-chip accumulation units for processing one input from NeuroSIM simulation
    - Synaptic Array(ns): latency cost by crossbar MVM for processing one input from NeuroSIM simulation
    - Buffer(ns): latncy cost by buffer for processing one input from NeuroSIM simulation
    - Interconnect(ns):	latency cost by on-chip data communication for processing one input from NeuroSIM simulation
    - DRAM(ns): latency cost by off-chip memory access for processing one input from NeuroSIM simulation	
    - SubArray Write(ns): latency cost by crossbar writing for storing the DNN model from NeuroSIM simulation
- *.ipynb: experiment codes in the paper, ran by python3.7 jupyter notebook.