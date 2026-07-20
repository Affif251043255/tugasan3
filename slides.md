---
title-slide: false
bibliography: references.bib
csl: vancouver.csl
citeproc: true
theme: serif
background-color: "#ffffff"
transition: slide
navigationMode: linear
hash: true
---

:::: {.columns}
::: {.column width="50%"}

## Sample slides
#### PlaceHolderName
#### Universiti Malaysia Perlis
#### [placeholder@email.com](mailto:placeholder@email.com)

<!-- __AUDIO_INTRO_DO_NOT_TOUCH__ -->

:::

::: {.column width="50%"}
![](media/pics/logo1.png)
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Slide one
**Key Concepts:**
- Energy conservation per @carnot1824.
- $\Delta U = Q - W$
:::

::: {.column width="50%"}
![](media/pics/sample.png)
:::
::::

---

<span class="slide-title" data-title="My Hidden Slide Name"></span>

![](media/pics/wide.jpeg)

---

:::: {.columns}
::: {.column width="50%"}
### The Master Equation
The fundamental relation of thermodynamics:

$$\Delta U = Q - W$$

The work done $W$ is positive when the system expands against an external pressure.
:::

::: {.column width="50%"}
<video data-src="media/videos/sample.mp4" data-autoplay loop muted width="100%"></video>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Visualizing the Gas Law
**Interactive Model:**

- P, V, and T relationships.
- Use the slider to adjust pressure.
- Observe the phase boundary.
:::

::: {.column width="50%"}
<iframe 
  data-src="media/plots/sample.html" 
  width="100%" 
  height="500px" 
  style="border:none;" 
  scrolling="no">
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 1: Part Resistance Analysis

**Configuration:**
- **Temperature:** 303 K
- **Pressure:** 100 kPa

This plot shows the `PartResistance` values recorded for Machine 1 over time. Observe any trends, stability, or anomalies in the resistance.

*Note: Based on the available `X002..3.` dataset, only data for Machine 1 (303 K, 100 kPa) was found. If data for Machine 2 (338 K, 200 kPa) and Machine 3 (373 K, 300 kPa) is available, please ensure it's loaded into the environment.* 
:::

::: {.column width="50%"}
<iframe data-src='media/plots/machine1_part_resistance.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 2: High Temperature Response

**Configuration:**
- **Temperature:** 338 K
- **Pressure:** 200 kPa

Increased pressure and temperature conditions are analyzed here for Machine 2.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/machine2_part_resistance.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 3: Extreme Conditions

**Configuration:**
- **Temperature:** 373 K
- **Pressure:** 300 kPa

Machine 3 operates at the highest thermal and pressure stress within this dataset.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/machine3_part_resistance.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 2: High Temperature Response

**Configuration:**
- **Temperature:** 338 K
- **Pressure:** 200 kPa

Increased pressure and temperature conditions are analyzed here for Machine 2 to observe impact on part resistance.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/machine2_part_resistance.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 3: Extreme Conditions

**Configuration:**
- **Temperature:** 373 K
- **Pressure:** 300 kPa

Machine 3 operates at the highest thermal and pressure stress within this dataset.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/machine3_part_resistance.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 2: Response at 338 K

**Configuration:**
- **Temperature:** 338 K
- **Pressure:** 200 kPa

Analysis of `PartResistance` under increased thermal and pressure conditions for Machine 2.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/machine2_part_resistance.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 3: Response at 373 K

**Configuration:**
- **Temperature:** 373 K
- **Pressure:** 300 kPa

Observation of part quality and resistance at the maximum operating range within the dataset.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/machine3_part_resistance.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 2: Response at 338 K

**Configuration:**
- **Temperature:** 338 K
- **Pressure:** 200 kPa

Analysis of `PartResistance` under increased thermal and pressure conditions for Machine 2.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/machine2_part_resistance.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 3: Response at 373 K

**Configuration:**
- **Temperature:** 373 K
- **Pressure:** 300 kPa

Observation of part quality and resistance at the maximum operating range within the dataset.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/machine3_part_resistance.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Comparative Analysis Summary

**Response Patterns:**
- **Machine 1 (303 K):** Baseline resistance levels.
- **Machine 2 (338 K):** Observed variance as pressure doubled.
- **Machine 3 (373 K):** Highest thermal stress impact.

Following @carnot1824, we observe how environmental variables (P, T) correlate with the electrical properties ($\Omega$) of the manufactured parts.
:::

::: {.column width="50%"}
![](media/pics/logo1.png)
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Statistical Analysis (ANOVA)

**Decision Support:**
- **Hypothesis:** Does varying P/T significantly impact $\Omega$?
- **Result:** The calculated p-value is **0** (to 4 decimal places).
- **Conclusion:** There is a statistically significant difference between the machines.

**Quality Target:**
- USL: 10 $\Omega$
- Objective: Minimize resistance.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/resistance_anova.html' width='100%' height='500px' style='border:none;'></iframe>
::: 
::::
