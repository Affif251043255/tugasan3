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

<audio id="bg-music" src="media/audio/sb.m4a" loop></audio>

<div id="audio-credit"
     style="position: absolute; bottom: 40px; right: 20px; font-size: 0.6em; opacity: 0.6;">
  Music: “Adrift” by Scott Buckley (CC BY 4.0)
</div>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const audio = document.getElementById('bg-music');
    const credit = document.getElementById('audio-credit');

    // hide credit by default
    credit.style.display = 'none';

    const test = new Audio('media/audio/bgm.mp3');

    test.addEventListener('canplaythrough', () => {
      // bgm.mp3 exists → use it, keep credit hidden
      audio.src = 'media/audio/bgm.mp3';
    }, { once: true });

    test.addEventListener('error', () => {
      // bgm.mp3 missing → sb.m4a will play → show credit
      credit.style.display = 'block';
    }, { once: true });

    document.addEventListener('click', () => {
      if (Reveal.getIndices().h === 0) {
        audio.volume = 0.5;
        audio.play();
      }
    }, { once: true });

    Reveal.on('slidechanged', (event) => {
      if (event.indexh > 0) { audio.pause(); }
      else { audio.play(); }
    });
  });
</script>

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

---

:::: {.columns}
::: {.column width="50%"}
### Dimensional Correlation

**Key Observations:**
- Evaluation of how PartLength relates to $\Omega$.
- Differentiation by machine processing units.
- Data points clustered by Temperature/Pressure settings.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/length_vs_resistance.html' width='100%' height='500px' style='border:none;'></iframe>
::: 
::::

---

:::: {.columns}
::: {.column width="50%"}
### Statistical Analysis (ANOVA)

**Decision Support:**
- **Hypothesis:** Does varying P/T significantly impact $\Omega$?
- **Result:** The calculated p-value is **0**.
- **Conclusion:** There is a statistically significant difference between the machines (assuming p-value < 0.05).

**Quality Target:**
- USL: 10 $\Omega$
- Objective: Minimize resistance.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/resistance_anova_boxplot.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Statistical Analysis (ANOVA)

**Decision Support:**
- **Hypothesis:** Does varying P/T significantly impact $\Omega$?
- **Result:** The calculated p-value is **0**.
- **Conclusion:** There is a statistically significant difference between the machines (assuming p-value < 0.05).

**Quality Target:**
- USL: 10 $\Omega$
- Objective: Minimize resistance.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/resistance_anova_boxplot.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Part Length vs Part Resistance

**Key Observations:**
- This scatter plot visualizes the relationship between `PartLength` and `PartResistance`.
- Each point represents a measurement, colored by the `Machine` it originated from.
- Observe if there are any correlations, clusters, or trends specific to each machine's operating conditions.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/length_vs_resistance.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Comparative Machine Performance

**Machine 1 (303 K, 100 kPa):**
- Exhibits the lowest `PartResistance` on average.
- Represents the baseline performance under moderate conditions.

**Machine 2 (338 K, 200 kPa):**
- Shows a noticeable increase in `PartResistance` compared to Machine 1.
- Performance indicates impact of increased temperature and pressure.

**Machine 3 (373 K, 300 kPa):**
- Operates under the most extreme conditions, resulting in the highest `PartResistance`.
- Suggests a direct correlation between operating stress and part quality.

**Overall:**
- There is a statistically significant difference in `PartResistance` between the machines, confirming the impact of varying temperature and pressure settings.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/resistance_anova_boxplot.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Impact of Pressure and Temperature on Part Resistance

**Overview:**
This slide visualizes the distribution of `PartResistance` across different machine operating conditions, highlighting the impact of varying pressure and temperature. The goal is to understand how these factors influence product quality, specifically part resistance.

**Machine Operating Conditions:**
*   **Machine 1:**
    *   Temperature: 303 K
    *   Pressure: 100 kPa
    *   Output: `PartLength` (mm), `PartResistance` (Ohms)
*   **Machine 2:**
    *   Temperature: 338 K
    *   Pressure: 200 kPa
    *   Output: `PartLength` (mm), `PartResistance` (Ohms)
*   **Machine 3:**
    *   Temperature: 373 K
    *   Pressure: 300 kPa
    *   Output: `PartLength` (mm), `PartResistance` (Ohms)

**Quality Target:**
- **Upper Specification Limit (USL):** 10 $\Omega$
- **Objective:** Lower resistance is better.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/machine_conditions_boxplot.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine Performance Analysis

**Operational Parameters:**
- **Machine 1:** 303 K | 100 kPa
- **Machine 2:** 338 K | 200 kPa
- **Machine 3:** 373 K | 300 kPa

**Quality Benchmarks:**
- **USL:** 10 $\Omega$
- **Objective:** Minimize $\Omega$ (Lower is better).

**Observations:**
As P and T increase across machines, we evaluate the stability of the output PartResistance relative to the Upper Specification Limit.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/resistance_boxplots.html' width='100%' height='500px' style='border:none;'></iframe>
::: 
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine Performance Analysis

**Operational Parameters:**
- **Machine 1:** 303 K | 100 kPa
- **Machine 2:** 338 K | 200 kPa
- **Machine 3:** 373 K | 300 kPa

**Quality Benchmarks:**
- **USL:** 10 $\Omega$
- **Objective:** Minimize $\Omega$ (Lower is better).

**Analysis:**
As shown in the chart, we evaluate the distribution of `PartResistance` against environmental stressors. The dashed line indicates the Upper Specification Limit.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/resistance_live_box.html' width='100%' height='500px' style='border:none;'></iframe>
::: 
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine Performance Analysis

**Operational Parameters:**
- **Machine 1:** 303 K | 100 kPa
- **Machine 2:** 338 K | 200 kPa
- **Machine 3:** 373 K | 300 kPa

**Quality Benchmarks:**
- **USL:** 10 $\Omega$
- **Objective:** Minimize $\Omega$ (Lower is better).

**Analysis:**
As shown in the chart, we evaluate the distribution of `PartResistance` against environmental stressors. The dashed line indicates the Upper Specification Limit.
:::

::: {.column width="50%"}
<iframe data-src='media/plots/resistance_live_box.html' width='100%' height='500px' style='border:none;'></iframe>
::: 
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine Performance Analysis

**Operational Parameters:**
- **Machine 1:** 303 K | 100 kPa
- **Machine 2:** 338 K | 200 kPa
- **Machine 3:** 373 K | 300 kPa

**Quality Benchmarks:**
- **USL:** 10 $\Omega$
- **Objective:** Minimize $\Omega$ (Lower is better).

**Analysis:**
As shown in the chart, we evaluate the distribution of `PartResistance` against environmental stressors. The dashed line indicates the Upper Specification Limit.
::: 

::: {.column width="50%"}
<iframe data-src='media/plots/resistance_live_box.html' width='100%' height='500px' style='border:none;'></iframe>
::: 
::::

---
# Bibliography
<div id="refs"></div>
