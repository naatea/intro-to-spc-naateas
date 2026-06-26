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
### T-test Results: PartLength (Machine 1 vs Machine 2)

**Conditions:**
- Pressure = 100
- Temperature = 303

**Hypotheses:**
- Null Hypothesis ($H_0$): There is no significant difference in PartLength between Machine 1 and Machine 2.
- Alternative Hypothesis ($H_1$): There is a significant difference in PartLength between Machine 1 and Machine 2.

**P-value:** <span id="p-value-placeholder"></span>

**Interpretation:**
If the p-value is less than the significance level (e.g., 0.05), we reject the null hypothesis, suggesting a significant difference. Otherwise, we fail to reject the null hypothesis.

::: {.column width="50%"}

:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Part Resistance by Process Parameters

The boxplots visualize the distribution of `PartResistance` for `Machine == 1` across different levels of `Pressure` and `Temperature`. This helps in understanding the spread and central tendency of resistance values for each parameter setting.

From these plots, it is visually apparent how different levels of pressure and temperature affect the part resistance, which aligns with the ANOVA results showing their significant individual effects.
:::

::: {.column width="50%"}
<iframe
  data-src="media/plots/resistance_boxplots.html"
  width="100%"
  height="500px"
  style="border:none;"
  scrolling="no">
</iframe>
:::
::::
