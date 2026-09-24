# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB-T1-M4-ODD

# AIM

To code and generate the mean and variance for the values in x.

# EQUIPMENTS NEEDED

* Computer with i3 Processor
* SCI LAB

# ALGORITHM

1. **Input Signal:**
   * Define vector $x = [10, 15, 20, 25, 30]$ with $n = 5$ samples.

2. **Compute Mean:**
   * Calculate $\text{Mean } (\bar{x}) = \frac{\sum x}{n}$.

3. **Compute Variance:**
   * Calculate $\text{Variance} = \frac{\sum (x - \bar{x})^2}{n}$.

4. **Compute Cross-Correlation:**
   * Compute $R_{xy} = \text{xcorr}(x, x)$.

5. **Plot Waveform:**
   * Plot $R_{xy}$ against lag, and label axes with title, grid, and labels.

# PROCEDURE

* Refer Algorithms and write code for the experiment.
* Open SCILAB in System.
* Type your code in New Editor.
* Save the file.
* Execute the code.
* If any Error, correct it in code and execute again.
* Verify the generated results, waveforms, and calculations.

---

## AIM / CODE

```scilab
clc;
clear;

x = [10 15 20 25 30];
n = 5;
sum_x = sum(x);
mean_x = sum(x)/n;
disp("Mean = ");
disp(mean_x);

variance = sum((x - mean_x).^2)/n;
disp("variance = ");
disp(variance);

Rxy = xcorr(x, x);
figure();
plot(Rxy);
xlabel("Lag");
ylabel("Cross correlation");
xgrid();
```

![Aim and Scilab Code](images/page_2.png)

---

## MODEL GRAPH / SCILAB OUTPUT

**Cross Correlation Waveform:**

![Cross Correlation Waveform](images/page_1.png)

---

## TABULATION & CALCULATIONS

$$\text{Mean } (\bar{x}) = \frac{\sum x}{n} = \frac{10 + 15 + 20 + 25 + 30}{5} = \frac{100}{5} = 20$$

$$\text{Variance} = \frac{\sum (x - \bar{x})^2}{n} = \frac{250}{5} = 50$$

| $x$ | $\bar{x}$ | $x - \bar{x}$ | $(x - \bar{x})^2$ |
| :---: | :---: | :---: | :---: |
| 10 | 20 | -10 | 100 |
| 15 | 20 | -5 | 25 |
| 20 | 20 | 0 | 0 |
| 25 | 20 | 5 | 25 |
| 30 | 20 | 10 | 100 |
| **Sum** | | | **250** |

![Calculations and Result](images/page_4.png)

---

## RECORD EVALUATION

![Record Evaluation](images/page_3.png)

---

## RESULT

The mean and variance are generated and verified in Scilab.

* **Mean**: 20
* **Variance**: 50
