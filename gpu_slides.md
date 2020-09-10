## Moore's Law

![By Max Roser - <a rel="nofollow" class="external free" href="https://ourworldindata.org/uploads/2019/05/Transistor-Count-over-time-to-2018.png">https://ourworldindata.org/uploads/2019/05/Transistor-Count-over-time-to-2018.png</a>, <a href="https://creativecommons.org/licenses/by-sa/4.0" title="Creative Commons Attribution-Share Alike 4.0">CC BY-SA 4.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=79751151">Link</a>](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8b/Moore%27s_Law_Transistor_Count_1971-2018.png/1920px-Moore%27s_Law_Transistor_Count_1971-2018.png){width=60%}

## Dennard scaling

::: {.columns}
:::::: {.column width=50%}

<br> <br>

- voltage drain, capacitance, inductance $∝$ transistor size
- clock frequency $∝ 1 /$ transistor size
- total power is the same!

::::::
:::::: {.column width=50%}

![[Soham Chatterjee](https://medium.com/@csoham358/beginners-guide-to-moore-s-law-3e00dd8b5057)](https://miro.medium.com/max/3200/0*g3vKfFpancLiFP_l.){width=100%}

::::::
:::



## The end of scaling

![C. Moore, “Data Processing in Exascale-class Computing Systems,” presented at the Salishan Conference on High-Speed Computing, 2011.](https://www.researchgate.net/profile/Luke_Shulenburger/publication/301650491/figure/fig24/AS:355250444750853@1461709714584/The-end-of-Dennard-Scaling-44.png){width=60%}

##

::: {.columns}
:::::: {.column width=50%}

### CPUs: Latency Oriented

- *latency* is lag a computer instruction and its completion

![](cpu.png){.fragment data-fragment-index="0"}

:::{.fragment .current-visible data-fragment-index="1"}
- **CPU**s use all kind of complicated tricks to minimize latency
:::


::::::
:::::: {.column width=50%}

### GPUs: Throughput Oriented

- *throughput* is number of operations per unit time

![](gpu.png){.fragment data-fragment-index="0"}

:::{.fragment .current-visible data-fragment-index="1"}
- **GPUs** maximize throughput at the cost of latency
:::

::::::
:::

:::{.fragment .current-visible data-fragment-index="2"}
Throughput $×$ Latency = Queue Size
:::

##

::: {.columns}
:::::: {.column width=50%}

### tasks can be sensitive to latency...

- serial tasks
    - sequential or iterative calculations


::::::
:::::: {.column width=50%}

### or throughput

- pleasingly/embarrassingly parallel tasks
    - calculations are independent of one another

::::::
:::

![](parallel_grayscale.png){.fragment .current-visible width=70%}

## GPU anatomy

::: {.columns}
:::::: {.column width=60%}

<br><br>

### three levels of organization:

- GPUs contain many small "threads" capable of performing calculations
     - each thread has a little bit of memory and a `threadIdx` (1, 2, or 3D)

- threads are grouped into "blocks"
    - each block has some shared memory and a  `blockIdx` (1, 2, or 3D)

 - blocks live on grids

::::::
:::::: {.column width=25%}
![](gpu_anatomy.png){width=100%}
![](gpu_anatomy_credit.png){width=100%}
::::::
:::

## Example: Image Blurring

::: {.columns}
:::::: {.column width=30%}
<br><br><br><br><br><br >
![](image_blurring.png)
::::::
:::::: {.column width=70%}
 ![](image_blurring_diagram.png)
::::::
:::
##

![](memory.png)

##

![](memory_example.png)

## Shared memory matrix multiply

::: {.columns}
:::::: {.column width=50%}

<br>
<br>

![](shared_memory.png){width=100%}

::::::
:::::: {.column width=50%}

![](matmul.png){.fragment}

::::::
:::




## Thanks!
