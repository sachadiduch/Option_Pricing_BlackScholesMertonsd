# Option Pricer (BSMM)

This Python script implements the **Black-Scholes-Merton (BSM) model** (of course for European option pricing only). It calculates option prices for both **continuous and discrete dividend** cases, computes **Greeks**, and visualizes option payoffs at expiration.

## Features
- **Black-Scholes-Merton Pricing:** Computes call and put prices with continuous and discrete dividend adjustments.
- **Greeks Calculation:** Delta, Gamma, Vega, Theta, and Rho.
- **Discrete Dividend Adjustments:** Adjusts the stock price for discrete dividend payments.
- **Comparison Table:** Displays option values under continuous and discrete dividend adjustments.
- **Option Payoff Visualization:** Plots the payoff profiles for call and put options at expiry.

## Usage
1. Clone this repository or download `Option Pricer (BSMM).py`.
2. Ensure you have Python 3.12+ installed along with required libraries (`numpy`, `pandas`, `scipy`, `matplotlib`).
3. Run the script in your terminal or IDE:
   ```bash
   python "Option Pricer (BSMM).py"
   ```
4. Follow the prompts to enter option parameters.

## Parameters
The script will prompt you to enter:
- **S_0:** Initial stock price (e.g., `1000`).
- **K:** Strike price (e.g., `1000`).
- **T:** Time to maturity in years (e.g., `3`).
- **rf:** Risk-free rate (as a decimal, e.g., `0.06` for 6%).
- **σ (sigma):** Implied volatility (e.g., `0.15`).
- **q:** Continuous dividend yield (as a decimal, `0` if none).
- **D:** Discrete dividend amount (optional for discrete model).
- **T_div:** Time when the discrete dividend is paid (must be `< T`).

### Input Example:
```
Enter the initial stock price (S_0): 1000
Enter the strike price (S_K): 1000
Enter the time to maturity (T in years): 3
Enter the risk-free rate (rf, as a decimal): 0.06
Enter the implied volatility (σ, sigma): 0.15
Enter the continuous dividend yield (q, as a decimal, 0 if none): 0.015

--- Discrete Dividend Option Pricing ---
Enter the discrete dividend amount (D): 15
Enter the dividend payment time (T_div in years, must be less than T): 3
```

## Output
After running the script, you will receive:
- A **table comparing** option prices and Greeks for continuous vs. discrete dividend models.
- **Payoff visualization** of call and put options at expiry.
- **Adjustments for discrete dividends** in option pricing.

### Example Output:
```
       Metric  Continuous Dividend  Discrete Dividend
0  Call Price           165.065753         189.038614
1   Put Price            44.338482          36.837879
2  Delta Call             0.709349           0.780592
3   Delta Put            -0.246649          -0.219408
4       Gamma             0.001189           0.001152
5        Vega           534.956476         505.640343
6  Theta Call           -35.390660         -47.547425
7   Theta Put             0.385591           2.568788
8    Rho Call          1632.848927        1745.320803
9     Rho Put          -872.961707        -760.489831
```

## Visualization
The script generates a **payoff plot** for call and put options:

- **Long Call (blue):** Profit increases as stock price rises above strike.
- **Long Put (red):** Profit increases as stock price drops below strike.
- **Strike Price (dashed line):** Indicates the breakeven point.

## Requirements
Ensure the following Python libraries are installed:
- `numpy`
- `pandas`
- `scipy`
- `matplotlib`

Install missing libraries using:
```bash
pip install numpy pandas scipy matplotlib
```

## Contributions
Contributions are welcome! Feel free to fork this repository and suggest improvements.

## Author
**Sacha D.**

## Disclaimer
This script is for educational purposes only and should not be used for financial decisions. The author assumes no responsibility for any actions taken based on the results of this script.
