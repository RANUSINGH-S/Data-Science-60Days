# Day 2 — Statistics Notes (Mean, Median, Mode, Variance, Std Dev)

**Date:** 21 Nov 2025  
**Topic:** Mean, Median, Mode, Variance & Standard Deviation

## Mean, Median, Mode (Summary)
- **Mean** = arithmetic average = sum(x)/n. Sensitive to outliers. Use when data is roughly symmetric/normal.
- **Median** = middle value after sorting. Robust to outliers and better for skewed data.
- **Mode** = most frequent value. Useful for categorical data. Can be multimodal.

**When to use**
- Skewed distribution or outliers → **median**.
- Normal distribution → **mean**.
- Categorical / most common value → **mode**.

## Variance & Standard Deviation
- **Variance (population)**: σ² = Σ(xᵢ − μ)² / N  
- **Variance (sample)**: s² = Σ(xᵢ − x̄)² / (n − 1)
- **Standard deviation**: σ = sqrt(variance). Returns to original units.

**Key ideas**
- Variance measures average squared distance from mean; squaring penalizes large deviations.
- Std dev is intuitive (same units as data).
- High std → data widely spread; low std → data concentrated near mean.
- Use std for feature scaling (StandardScaler), outlier detection, and understanding distribution spread.

## Normal distribution (Empirical rule)
- ~68% of data within ±1σ
- ~95% within ±2σ
- ~99.7% within ±3σ

## Quick examples
- Data: [10, 12, 14, 100] → mean pulled up by 100; median remains robust.
- Use median for income data, house prices, etc.

## Confidence (today): 5/10 — need practice via code
