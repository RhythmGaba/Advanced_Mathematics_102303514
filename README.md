# Learning Probability Density Function using Roll-Number-Parameterized Non-Linear Model

## Dataset Used
- **Name:** India Air Quality Data
- **Source:** https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data
- **Feature Used:** no2

## Objectives
- Apply roll-number-based non-linear transformation on the feature.
- Learn the parameters of the given probability density function.
- Estimate parameters using Method of Moments (MoM).

## Methodology
- Data Transformation : Each NO2 value (x) was transformed into a new variable (z) using the transformation:
z = x + a_r sin(b_r x)
Where: a_r = 0.05 × (r mod 7), b_r = 0.3 × ((r mod 5) + 1), r = Roll Number
- Probability Density Function
The given density function is: p(z) = c * exp( -λ (z − μ)² )
This function resembles a Gaussian distribution. Therefore, statistical estimation techniques were applied to estimate the parameters μ, λ and c.
- Parameter Estimation Method Used: Method of Moments (MoM)
  - μ estimated as the sample mean of z.
  - Variance estimated from sample data.
  - Using Gaussian comparison:
     - λ = 1 / (2σ²)
     - c = 1 / √(2πσ²)

## Visualization
<img width="708" height="517" alt="image" src="https://github.com/user-attachments/assets/bd2780a8-a412-4c55-84c8-4896af969f75" />
