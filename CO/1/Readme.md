# Computer Abstractions and Technology

## 1.1 Introduction
## 1.2 Eight Great Ideas in Computer Architecture
1. Design for Moore's Law
2. Use Abstraction to Simplify Design
3. Make the Common Case Fast
4. Performance via Parallelism
5. Performance via Pipelining
6. Performance via Prediction
7. Hierarchy of Memories
8. Dependability via Redundancy

## 1.3 Below Your Program

1. Application software
2. Systems software
    1. OS
    2. Compiler
3. Hardware

## 1.4 Under the Cover

1. **Big Picture 1: Five classic components of a computer**
    1. input
    2. output
    3. memory 
    4. datapath
    5. control

## 1.5 Technologies for Building Processors and Memory

1. Yield: the percentage of good dies

## 1.6 Performance

1. Response time (Execution time)
2. Throughput (bandwidth)
3. Clock cycles per instruction (CPI)
    - $CPU \, time = Instructions\,count \times CPI / Clock \, rate $

4. Factors
    1. Algorithm: 
        - Influence: Inst. count and maybe CPI.
        - The preference of floating/integer also influences CPI.
    2. Programming language:
        - Influence: Inst. count and CPI.
        - E.g., Java features higher data abstraction at the cost of higher CPI.
    3. Compiler
        - Influence: Inst. count and CPI.
    4. Instruction Architecture:
        - Influence: CPI, clock rate, Inst. count.

## 1.7 The Power Wall

1. $Energy \propto Capacitive \, load \times Voltage^2$
2. $Power \propto Capacitive \, load \times Voltage^2 \times Switch Frequency$
3. Even today about $40%$ of the power
consumption in server chips is due to leakage.
4. 

## 1.8 The Sea Change: The Switch from Uniprocessors to Multiprocessors

1. Chapter 2, Section 2.11: Parallelism and Instructions: Synchronization.
2. Chapter 3, Section 3.6: Parallelism and Computer Arithmetic: Subword
3. Chapter 4, Section 4.10: Parallelism via Instructions.
    1. Pipeline 
    2. Prediction
4. Chapter 5, Section 5.10: Parallelism and Memory Hierarchies: Cache Coherence.
5. Chapter 5, Section 5.11: Parallelism and Memory Hierarchy: Redundant Arrays of Inexpensive Disks.

## 1.9 Real Stuff: Benchmarking the Intel Core i7

1. System Performance Evaluation Cooperative (SPEC)
    - SPEC CPU 2006
    - SPECratio (via geometric mean, not arithmetic mean).
2. SPEC Power benchmark
    - Two kinds:
        1. 10% increments
        2. over a period of time 

## 1.10 Fallacies and Pitfalls
1. When discussing a **fallacy**, we try to give a **counterexample**.
2. Often **pitfalls** are
generalizations of principles that are true **in a limited context**.
3. Pitfall: Expecting the improvement of one aspect of a computer to increase overall performance by an amount proportional to the size of the improvement.
4. Amdahl's Law
    - The performance enhancement possible
with a given improvement is limited by the amount that the improved feature is used.
    - The Law of diminishing returns
    - $Executation \, time \, after \, improvement = 
    \frac{Executation \,time \,effected \,by \,improvement}{Amount\, of \,improvement}+Executation\, time\, unaffected$

5. Fallacy: Computers at low utilization use little power.
    - Utilization of servers in Google’s warehouse scale computer, for example, is between 10% and 50% most of the time and at 100% less than 1% of the time.
    - In 2012 still it uses 33% of the peak power at 10% of the load.

6. Fallacy: Designing for performance and designing for energy efficiency are unrelated goals.

7. Pitfall: Using a subset of the performance equation as a performance metric.
    - A common mistake is to use only two of the
three factors to compare performance (e.g., MIPS)
    - MIPS (million instructions per
second)
        1. MIPS does not take into account the capabilities of the instructions.
        2. MIPS varies between programs on the
same computer

        $MIPS = \frac{Inst. count}{\frac{Inst.count\times CPU}{clock rate}\times 10^6}=\frac{clock\,rate}{CPI\times10^6}$

## 1.11 Conclusion Remarks
1. One of the most abstraction is the instruction set architecture (ISA)

2. **Execution time** is the **only valid** and **unimpeachable measure** of performance.
