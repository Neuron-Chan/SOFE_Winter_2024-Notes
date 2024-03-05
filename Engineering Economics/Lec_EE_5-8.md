Note: Covers modules 5 through 8.

# Preamble:

"Open door" policy and "1% policy" in grading.

| Category                     | Mark   |
|------------------------------|--------|
| Term Group Project           | 20%    |
| Drop Quiz (TBA)              | 5%     |
| Midterm 1 (Feb. 8th)         | 15%    |
| Midterm 2 (Mar. 14th)        | 25%    |
| Final                        | 35%    |

Office hours: Mon

Missed midterms are deferred to Final exam.

Final is comprehensive

Project stuff:

- Project will look at estimating economics connected to different possible industrial applications. Five people. Deliverables are a written report and recorded video presentation.
  - Multiple Hybrid electric energy systems
  - These are some of the alternatives that will be proposed. However the group in the proposal can put something it retains interesting forward.
 
3 PARTS
A) Initial Investigation Feb. 19 2024
B) COST Estimation Mar. 22 2024
C) Final Report w/ Presentation Apr. 1 2024

Energy project will primarily look at estimating the economics connected to different electrical power plants alternatives (example:)
a) Nuclear SMR Reactor (Nuscale)
b) a PV solar power plant
c) a Wind Farm w/ Battery Storage
d) a Turbogas
e) Geothermal P.P

Each group will be composed by 5 people each of whom responsible for 1 part. [S.A.M. Software will be used](https://sam.nrel.gov/)

<ins>Costs will have to include:</ins>

a) Installation

b) operations & maintenance

c) Fuel

d) Personnel

e) Land

f) Final disposal

Each group will be expected to conduct proper literature review. A proposal of Hybrid A vs Hybrid B is expected (later on *compared for Economics* Considerations). A final Presentation w/ pre-recorded video will be uploaded as part of the deliverables.

All work & conclusions presented / written in reports / quizzes must be fully justified and explained.

All exams are closed books, closed notes, unless stated differently. Exams might be on Canvas or on Paper. All quizzes are considered pop quizzes unless previously announced / or stated.

Always have

a) your Calculator
b) Eng. Economics Formula Sheet

Assignments, Mini Quizzes need to have the following characteristics:

a) be legible
b) have a cover page
c) sent via elec
d) might be scanned in Microsoft Word

Subjects to be covered:

- Introduction to Engineering Economics: Macro & Micro Economics
- Supply and Demand / Estimating models
- Role of the Bank of Canada
- Balance Sheet Accounting
- Financial Ratios
- Time value of money
- Interest rates / Cash flow diagrams / C.F. Analysis
- Compounding & Series
- MARR & IRR / ERR & Comparisons
- Benefit Analysis A.W. / Payback Period
- Uncertainty & Risk
- Probability Analysis & Decision Trees
- Depreciation
- Taxes & Cash Flow
- Replacement Analysis & Decisions
- Inflation & Price CHange
- Public Decision Making
- Market Failures & Remedies
- FINAL EXAM

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 5 | Equivalence for Repeated Cash Flows</summary>

# Learning Objectives
- Convert uniform series of cash flows to their equivalent present or future values
- Use arithmetic and geometric gradients to solve correctly modelled problems
- Use continuously compounded interest with uniform payment series

# Uniform Series Compound Interest Formulas
- Uniform series (A) is defined as:
- An end-of-period cash receipt or disbursement in a uniform series, continuing for n periods
- The entire series equivalent to P or F at an interest rate i

![compound interest factors (slide 4)](../static/EE_5_1.png)

- In the general case:

F = A(1+i)<sup>n–1</sup> + . . . + A(1+i)<sup>2</sup> +A(1+i) + A                         **[1]**

- Multiplying by (1+i):

(1+i)F = A(1+i)<sup>n</sup> + . . . + A(1+i)<sup>3</sup> + A(1+i)<sup>2</sup> + A(1+i)    **[2]**

- Factoring out A and subtracting (1) from (2):

iF = A[(1+i)<sup>n</sup> – 1]

Rearranging the previous equation
𝐹 = 𝐴 [((1 + 𝑖)<sup>𝑛</sup> − 1) / 𝑖]

- The notation is F = A(F/A, i%, n)
- This is called the **uniform series compound amount factor**


Solving for A:
𝐴 = 𝐹 * [𝑖 / ((1 + 𝑖)<sup>𝑛</sup> − 1)]

- The notation is A = F(A/F, i%, n)
- This is called the **uniform series sinking fund factor**

Taking the sinking fund formula and substituting the single payment compound formula for F yields:

𝐴 = 𝐹 * [𝑖 / ((1 + 𝑖)<sup>𝑛</sup> − 1)] = 𝑃(1 + 𝑖)<sup>𝑛</sup> * [𝑖 / ((1 + 𝑖)<sup>𝑛</sup> − 1)]

- Therefore:

𝐴 = 𝑃[𝑖(1 + 𝑖)<sup>𝑛</sup> / ((1 + 𝑖)<sup>𝑛</sup> − 1)]

- Notation: A = P(A/P, i%, n)
- This is called the **uniform series capital recovery factor**

Solving the capital recovery formula for P:
𝑃 = 𝐴 * [((1 + 𝑖)<sup>𝑛</sup> − 1) / 𝑖(1 + 𝑖)<sup>𝑛</sup>]

- Notation: P = A(P/A, i%, n)
- This is called the **uniform series present worth** formula

## Uniform Series Formulas: Problem 1
Joe wants to be able to **purchase a dream car for about $19,000** on **1 January 2004**, just after he graduates from college. Joe has had a part time job and started making deposits of **$275 each month** into an account that pays **9% compounded monthly** beginning with the **first deposit on 1 February 1999.** The **last deposit is to be made on 1 January 2004**. Determine how much money he would have saved to buy the car.

## Solution
_Monthly deposits_, 

A = $275

n = 2/1999 to 1/2004 = 60 periods. (5 years = 12 * 5 = 60 months)

F = $275 (F/A, 0.75%, 60) = $275 (69.770) = $19,168.75

Joe will have **$19,168.75** available for his purchase.

Therefore, Joe will have enough to purchase a dream car.

## Uniform Series Formulas: Problem 2
You are repaying a debt of $10,000 with equal payments made at the end of four equal periods. If the interest rate is 10% per period, how much of the original $10,000 principal will be paid in the second payment?

## Solution
Principal = $10,000

Number of equal payments (n) = 4. i = 10% per period.

A = P(A/P, i, n) = 10,000(A/P, 10%, 4) = 10,000 × 0.3155 = $3155

First payment interest on unpaid balance = 10,000 × 0.10 = $1000.

Principal repaid = A – 1,000 = $2155.00

Second payment Principal due = 10,000 – 2155 = $7845

Interest on unpaid balance = 7,845 × 0.10 = $784.50.

Principal paid in the second payment = 3,155 – 784.50 = $2370.50.

## Relationships Between Compound Interest Factors
- Single Payment
  - Compound amount factor = 1/Present Worth Factor
  - (F/P, i, n) = 1/(P/F, i, n)
- Uniform Series
  - Capital recovery factor = 1/Present Worth Factor
  - (A/P, i, n) = 1/(P/A, i, n)
    
  - Compound amount factor = 1/Sinking Fund Factor
  - (F/A, i, n) = 1/(A/F, i, n)
    
  - Capital recovery factor = Sinking Fund Factor plus i
  - (A/P, i, n) = (A/F, i, n) + i
    
# Uniform Series Involving P/A and A/P
The uniform series factors that involve P and A are derived as follows:

(1) Cash flow occurs in consecutive interest periods

(2) Cash flow amount is same in each interest period

The cash flow diagrams are:

![cash flow diagrams](../static/EE_5_2_1.png)

# Uniform Series Involving F/A and A/F
The uniform series factors that involve F and A are derived as follows:

(1) Cash flow occurs in consecutive interest periods

(2) Last cash flow occurs in same period as F

Cash flow diagrams are:

![cash flow diagrams](../static/EE_5_2_2.png)

![spreadsheet functions](../static/EE_5_2_3.png)

# Arithmetic Gradient
- A uniformly increasing series consists of two components:
  - Series component (A)
  - Gradient component (G)
 
![arithmetic gradient](../static/EE_5_3.png)

- Therefore:
- P = A(P/A, i%, n) + G(P/G, i%, n)

- Derivation of Arithmetic Gradient Factors
  - Arithmetic gradient present worth factor:

(𝑃/𝐺, 𝑖, 𝑛) = [((1 + 𝑖)<sup>𝑛</sup> − 𝑖𝑛 − 1) / 𝑖<sup>2</sup>(1 + 𝑖)<sup>𝑛</sup>

- Arithmetic gradient uniform series factor:
(𝐴/𝐺, 𝑖, 𝑛) = [(1/i) - (n/(1 + 𝑖)<sup>𝑛</sup> − 1)]

## Reality and the Assumed Uniformity of a, G, and g
- We define and start with an A (uniform annual cost), a G (uniform annual gradient), and a g (uniform annual rate of increase) for three reasons:
  1. It is easier to start with simple models
  2. These model cash flows are convenient for bounding the problems often encountered in engineering economic analysis
  3. Not enough is known about the future and so it is approximated through uniform series and gradients

# Geometric Gradient
- Period-by-period change is a uniform rate (g)
- It can be traced to population levels or other levels of activity where changes over time are best modelled as a percentage of the previous year.

![geometric gradient](../static/EE_5_4.png)

- Two possible cases:
  **- Where: i ≠ g**

𝑃 = 𝐴<sub>1</sub> [(1 − (1 + 𝑔)<sup>𝑛</sup> * (1 + 𝑖)<sup>-𝑛</sup>) /(𝑖 − 𝑔)]

- Factor Notation: (P/A, g, i, n)
- This is called the “geometric series present worth factor” where i ≠ g

  **- Where: i = g**

  𝑃 = 𝐴<sub>1</sub> * 𝑛(1 + 𝑖)<sup>–1</sup>

- Factor Notation: (P/A, g, i, n)
- This is called the “geometric series present worth factor” where i = g

# When Compounding Period and Payment Period Differ
- When compounding interest periods and payment periods differ, an adjustment is required in order to utilize the formulas.
- This is usually done by:
  1. Computing the equivalent payment amounts for each compounding period and applying the interest rate
  2. Computing an effective interest rate for the payment periods

![continuous compounding](../static/EE_5_5.png)


</details>

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 6 | Present Worth Analysis</summary>

# Learning Objectives
- Define the _present worth_ and _future worth_ criteria
- Use these criteria to choose between alternatives
- Apply the criteria in cases with equal, unequal, and infinite project lives

# Assumptions in Solving Economic Analysis Problems
- End-of-Year Convention
  - All cash flow amounts are calculated as amounts at the end of each period:
    - Now = end of period 0 (beginning of period 1)
    - Future amounts happen at the end of the period specified

![continuous compounding](../static/EE_6_1.png)

- No Sunk Costs
  - Only the current situation and the potential future is considered.

- Viewpoint of Economic Analysis Studies
  - Point of view of a firm vs. point of view of a department
  - Generally, we will want to take the point of view of a total firm when doing industrial economic analyses.
- Borrowed Money Viewpoint
  - Each problem has two monetary aspects:
    - Financing—the obtaining of money
    - Investment—the spending of money
  - Money required to finance projects is obtained at interest rate i.
- Income Taxes
  - Income taxes must be considered in order to find the real payoff of a project.
  - However, taxes will often affect alternatives in the same way, allowing us to compare our choices without considering income taxes.
- Effect of Inflation and Deflation
  - Inflation and deflation must be considered in order to find the real payoff of a project.

## Economic Criteria
- Alternatives are judged based on economic efficiency.
- To compare cash flows of alternatives, we must first move them to the same moment in time.
  - Present – present worth analysis
  - Future – future worth analysis
  - Series of equal cash flows at regular intervals – annual cash flow analysis
- Each of these methods will always yield the same recommendation for choosing the best alternative(s).

# Present Worth Techniques
- Careful consideration must be given to the time period covered by the analysis.
- Three potential analysis-period situations are possible when comparing alternatives:
  - Useful life of each alternative equals the analysis period
  - Useful lives different from the analysis period
  - There is an infinite analysis period, n = ∞

## 1. Useful Lives Equal to the Analysis Period
- When selecting between two alternatives using present worth analysis:
- Maximize:
  - Net Present Worth = Present worth benefits – Present worth of costs
  - NPW = PW of benefits – PW of costs
- The alternative with the higher NPW is selected
- This criterion is called the net present worth criterion and is written simply as NPW

![example1](../static/EE_6_2_1.png)
![example1](../static/EE_6_2_2.png)

## 2. Useful Lives Different from the Analysis Period
- It is NOT correct to analyze alternatives using NPW with different lives.
- Methods to handle this problem:
  - Examine the alternatives using a “least common multiple” (LCM) of lives.
  - Decide on an analysis period if the LCM method is too large or doesn’t make sense.
    - (e.g., 7 and 13 years gives an LCM = 91 years)

![example2](../static/EE_6_3_1.png)
![example2](../static/EE_6_3_2.png)
![example2](../static/EE_6_3_3.png)
![example2](../static/EE_6_3_4.png)

## 3. Infinite Analysis Period: Capitalized Cost
- The need for large-scale infrastructure projects (bridges, pipelines, etc.) is considered to be permanent.
- These types of projects are considered to have an infinite analysis period.
- Capitalized cost is the present sum that is required to provide the service indefinitely.
- For any initial present sum P, there can be an end-of-period withdrawal of A which is equal to P(i):
  - These withdrawals will never decrease the original principal
  - **A = Pi for n = infinity**
  - **Capitalized Cost = P = A/i**
    - The money set aside that can provide the funds for the project forever
 
![example3](../static/EE_6_4.png)

### Present Worth Analysis: Problem 1

Two outdoor facilities are being considered for an upcoming Olympic baseball event in three years. The ticket price is fixed for the event at $150/person payable in the event year. Facility A requires a non-refundable deposit of $250,000 and will hold 15,000 people for the event. Facility B does not require a deposit but holds only 13,000 people. If the event sells out in either facility, which facility should be chosen based on a present worth analysis, if the interest rate is 10%?

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">**Solution**</summary>

  - Present worth of Facility A
  - P = –250,000 + 15,000(150)(P/F, 10%, 3)
  - P = –250,000 + 15,000(150)(0.7513)
  - P = $1,440,425
    
  - Present worth of Facility B
  - P = 13,000(150)(P/F, 10%, 3)
  - P = 13,000(150)(0.7513)
  - P = $1,465,035

  Choose Facility B because the NPW of B is more profitable based on a present worth analysis.
</details>

---

### Present Worth Analysis: Problem 2
A municipal contractor has agreed to construct an electric power plant and to deposit sufficient money in a perpetual trust fund to pay a $10,000/year operating cost and to perform a major renovation to the plant every 15 years at a cost of $200,000. The plant itself will initially cost $500,000 to construct. If the trust fund earns 10% interest per year (compounded annually), what is his capitalized cost to construct the plant, to make the future periodic renovations, and to pay the annual operating costs forever?

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">**Solution**</summary>

  - A = $10,000 /year
  - Renovation cost every 15 years = $200,000

  - Initial cost = $500,000. Interest rate = 10%
  - Capitalized cost, P0 = 500,000 + (100,000/0.10) + {200,000 (A/P, 10%, 15)/0.10} = 500,000 + 1,000,000 + {200,000(0.1315)/0.10}
  
  - **= $1,763,000**
</details>

# Multiple Alternatives
- Two or more alternatives can be handled by present worth analysis.
- The NPW can be evaluated for each project.
- Selection is made based on the criteria for the project (minimizing or maximizing the present worth of the alternatives).

![example4](../static/EE_6_5_1.png)

# Bond Pricing
- When Bonds are purchased, the fixed items are:
  - Face Value (e.g., $1000)
    - Amount paid out when the bond matures
  - A nominal interest rate (e.g., 8% semi-annually)
    - Sometimes called “coupon rate”
    - The amount of interest paid out to the bond holder per compounding period
- The purchase price can vary depending on the current market interest rate as the present worth of a bond is determined from the fixed values above (the interest paid out per compounding period and the final face value paid out in the future).

![example5](../static/EE_6_6_1.png)
![example5](../static/EE_6_6_2.png)

## Spreadsheets and Present Worth
- With spreadsheets, it is easy to use 120 months instead of 10 years, and the cash flows can be estimated for each month.
  - e.g., Air-conditioning costs for summer vs. winter
- No interpolation needed for interest rates
  - Easy to calculate a repayment schedule

# Future Worth Analysis
- In present worth analysis, alternatives are compared in terms of their present equivalent value.
- We can also choose between alternatives by finding their equivalent value at some future date. This is called future worth analysis.
- Future worth analysis is a more natural way of thinking about certain types of problems.
  - E.g., if we are setting aside money to provide ourselves with a pension on retirement, we’re interested in how much money we’ll have when we retire. We don’t care what that amount of money would be worth now, since we’re not going to be spending it now.

![example6](../static/EE_6_7.png)
</details>

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 7 | Annual Cash Flow Analysis</summary>

# Learning Objectives
- Define equivalent uniform annual cost (EUAC)
- Resolve any series of cash flows into its annual cash flow equivalent
- Use annual costs to compare alternatives with equal, common multiple, or continuous lives, or over some fixed study period
 
# Annual Cash Flow Calculations
- The objective is to compare alternatives based on annual cash flows.
- This requires converting present values and one-time values on the timeline to equivalent uniform annual values.
  - Using annual worth factors: F
    - For example: A = P(A/P, i%, 4)
![diagram](../static/EE_7_1_1.png)   
![example1](../static/EE_7_1_2.png)

# Treatment of Salvage Value
- When there is a salvage value at the end of the life of an asset, it is represented as a one-time cash flow benefit at the end of the asset’s life (i.e., it lowers the equivalent uniform annual cost).
- Example: Salvage value (S) of asset with a four-year life

![diagram](../static/EE_7_2_1.png)

When there is an initial cost (P) followed by a salvage value (S) the equivalent uniform annual worth (EUAC) can be computed by:
- EUAC = P(A/P, i, n) – S(A/F, i, n)
**OR**
- EUAC = (P – S)(A/F, i, n) + Pi
**OR**
- EUAC = (P – S)(A/P, i, n) + Si

- Known as "capital recovery cost"

- Direct relationship between present worth cost and equivalent uniform cost:
  - EUAC = PWCost(A/P, i, n)
- Expenditure of money increases EUAC, whereas receipt of money decreases EUAC.
- For irregular cash disbursements over the analysis period it is convenient to convert them to a present worth cost first, rather than use the above equation.
- For arithmetic gradient the factor that can be used is: (A/G, i, n)

![example2](../static/EE_7_2_2.png)
![example2](../static/EE_7_2_3.png)


# Annual Cash Flow Analysis
- When comparing alternatives, we can always ignore any cash flows common to each alternative.
- So if two strategies both yield the same benefits, we can simply choose the one with the lower equivalent annual costs.
- Conversely, if two strategies have the same costs, we will choose the one with the greater equivalent annual benefits.

# Cash Flow Calculations: Problem
- A university student looking for new tires has located the following alternatives:

| Tire Life (warranty) | Price/Tire |
|-|-|
|12 Months|$30.95|
|24 Months|$44.95|
|36 Months|$53.95|
|48 Months|$59.95|

- If she figures that money is worth 12%, which tires should she choose?

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Solution</summary>
  
  - EUAC (12 month tire) = $30.95 (A/P, 12%, 1) = $34.66
  - EUAC (24 month tire) = $44.95 (A/P, 12%, 2) = $26.60
  - EUAC (36 month tire) = $53.95 (A/P, 12%, 3) = $22.46
  - EUAC (48 month tire) = $59.95 (A/P, 12%, 4) = $19.74

**Choose the 48 Month Tire to reduce annual costs.**

</details>

---

# Analysis Period
- Alternatives have equal lives.
  - If the lives are equal, the analysis period is based on the same lifetime.
    
- Alternatives have unequal lives.
  - If the lives are unequal, the analysis period is based on alternate lifetimes.
    - No LCM is required as in present worth analysis.
    - **Multiples of service life are equivalent to one service life with annual worth analysis—therefore, it doesn’t matter!**
   

## Infinite Analysis Period
- Since multiples of finite service lives are equivalent to one service life, an infinite analysis of finite service lives yield:
  - EUAC<sub>infinite analysis period</sub> = EUAC<sub>for limited life _n_</sub>
- However, when an alternative with an infinite life is evaluated over an infinite analysis period:
  - EUAC<sub>infinite analysis period</sub> = P(A/P, i, ∞) + Any other annual costs

- When n = ∞, A = Pi, therefore:
  - EUAC<sub>infinite analysis period</sub> = Pi + Any other annual costs

- The difference in annual cost between a long life and an infinite life is normally small, unless an unusually low interest rate is used.
  - Example: $5.5 Million cost at 6%/year
    - Infinite Life: EUAC = 5.5(0.06) = $330,000
    - Long Life (85 years): EUAC = 5.5(A/P, 6%, 85) = $332,000
  - Difference in time is large (85 compared to infinity) but the EUAC is small.

# Annual Cash Flow Analysis: Problem
- The following data are available for three different alternatives:


|  | Alternative A | Alternative B | Alternative C |
|-|-|-|-|
|Initial Cost|$1000|$1500|$2000|
|Uniform Annual Benefits|$200|$276.20|$654.80|
|Useful Life in Years|--|20|5|
|Interest Rate|15%|15%|15%|

- Alternatives B and C are replaced at the end of their useful lives with identical replacements. Using annual cash flow analysis find the most attractive alternative.

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Solution</summary>
  
**Alternative A**
- EUAB – EUAC = 200 – 1000(0.15) = $50

**Alternative B**
- EUAB – EUAC = 276.2 – 1500(A/P, 15%, 20) = 276.2 – 1500(0.1598) = $36.5

**Alternative C**
- EUAB – EUAC = 654.8 – 2000(A/P, 15%, 5) = 654.8 – 2000(0.2983) = $58.2

**Choose Alternative C.**

</details>

---

![example3](../static/EE_7_3.png)

# Some Other Analysis Period
- The analysis period in a particular problem may be something other than the ones described so far.
- It may be equal to the life of the shorter-life alternative, the longer-life alternative, or something entirely different.
- One must carefully examine **the consequences** of each alternative throughout the analysis period and, in addition, see what differences there might be in salvage values, and so forth, at the end of the analysis period.

# Mortgages in Canada
- Although technically a mortgage is a legal document, most people use the word to mean a long-term amortized loan that is used for buying real property such as a house or land.
- If the mortgage payments are not made, the lender can take the property and sell it to recover the outstanding debt.

- A mortgage document:
  - Outlines the terms and conditions for repaying the money borrowed: the amount borrowed, the interest rate, the first and last payment dates, the amortization period, and the date the balance is due (the renewal date or term).
  - Prepayment options and penalties may also be included.

- Amortization:
  - Length of time it takes to pay off the mortgage assuming:
    - Payments are made on time with no additional payments
    - Interest rate doesn’t change

- Amortization periods are typically between 5 years and 40 years (The norm is 20 or 25 years)

- Terms
  - The amortization of a mortgage is often made up of smaller periods called "terms" and a term is the period in which the interest rate "term" is fixed.
- At the end of the term, the mortgage can be renewed for a another term at the current interest rate.

## Building an Amortization Schedule

- An amortization schedule lists the following for each payment period:
  - Loan payment
  - Interest paid
  - Principal paid
  - Remaining balance
- For each period _the interest paid_ equals the interest rate times the balance remaining from the period before.
- Then, the principal payment equals the payment minus the interest paid.
- Finally, this _principal payment_ is applied to the balance remaining from the preceding period to calculate the _new remaining balance._

![example4](../static/EE_7_4.png)

# Types of Mortgages Available
- “Conventional”:
  - For 80% or less of the appraised value of the property, and as such they require the purchaser to make a down payment of at least 20%.

- “High-ratio” mortgages:
  - Higher than 80% and usually require an outside agency such as the CMHC (Central Mortgage and Housing Corporation) to insure the mortgage.
  
- Some others:
  - Open, variable rate, ARM (adjustable rate mortgage), capped rate, closed, convertible rate, second, reverse, and CHIP mortgage.

# Mortgage Interest Rate

Interest rate is expressed as:

- % compounded semi-annually, not in advance.
  - An old English term when ledgers were kept by hand
  - Nominal rate mortgage at 6% is actually 3% semi-annually
  - To determine actual effective monthly rate for this example
- (1+i)6 = 1.03
- In this case: i = 0.49%/month

# Equity
- The value remaining in a property after all mortgage and loans registered against the title are subtracted from its value.

- For example:
- Appraised value        $210,000
- minus mortgage        -$150,000
- minus second mortgage  -$25,000
- equals equity           $35,000
</details>

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 8 | Rate of Return Analysis</summary>

# Learning Objectives
- Evaluate project cash flows with the internal rate of return (IRR) measure
- Use an incremental rate of return analysis to evaluate competing alternatives
- Conduct a sensitivity analysis by plotting the present worth (PW) of a project against the interest rate
- Recognize when to calculate the modified internal rate of return (MIRR)

# Introduction
- Rate of return analysis is the most frequently used measure in industry.
- It provides a measure of a project’s desirability in terms that are easily understood.
- In rate of return analysis, we compute a rate of return (more accurately called _internal rate of return_) from the cash flow.
- The calculated rate of return is then compared with a pre-selected **Minimum Attractive Rate of Return (MARR).**

# Minimum Attractive Rate of Return
- The purpose of rate of return analysis is to allow us to decide between different possible projects.
- Once we have calculated that the rate of return on a particular project is, for example, 23%, what do we do next?
- We need some form of benchmark against which we can compare this number.
- The average rate at which we have to recompense our creditors and investors sets a lower bound on the rate of return at which a proposed project becomes attractive.
- The highest of these lower bounds is the **Minimum Attractive Rate of Return (MARR).**

# Internal Rate of Return (IRR)
- A project’s rate of return is defined by IRR.
- Internal Rate of Return (IRR) is the interest rate at which the present worth and equivalent uniform annual worth are equal to zero.
- The IRR is the interest rate at which the benefits are equivalent to the costs.

## Calculating Rate of Return
- Given a cash flow, there are five forms of equations that can be used to solve for the unknown interest rate:
  - Present worth = Net present worth = 0
  - PW of benefits – PW of costs = 0
  - PW of benefits/PW of costs = 1
  - EUAW = EUAB – EUAC = 0
  - PW of costs = PW of benefits

- These are the same concepts in five different forms.

### Rate of Return: Problem 1
- With an initial investment of $6549.32 in a new machine, you will provide your company with $4000 more incoming dollars over the next four years. However, over those four years, the maintenance of the machine will cost $800. Also, in Year 2 a refit of the machine will cost $5,100.
  
- What is the rate of return?

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Solution</summary>
  
0 = –6549.32 + 4000(P/A, i, 4) – 800(P/A, i, 4) – 5100(P/F, i, 2)

i = 6%/year

</details>

A typical plot for borrowed money:
- Viewpoint of the borrower:
![plot of NPW](../static/EE_8_1_1.png)

The **IRR** is located where the plot crosses the **NPW = 0** point.

A typical plot for invested money:
- Viewpoint of the investor:
![plot of NPW](../static/EE_8_1_2.png)

The **IRR** is located where the plot crosses the **NPW = 0** point.

# Interest Rates When There Are Fees or Discounts
- The internal rate of return is affected by fees or discounts.
- Example:
  - An electronics retailer offers a 2% interest rate on purchases. However, they charge a financing fee of $200.00 to provide the service.
    - The fee increases the true internal interest rate of the purchase.

![incremental ROR Evaluation](../static/EE_8_2.png)

Incremental Analysis
• In rate of return analysis, two or more alternatives are compared
using the incremental rate of return (IRR).
• The project increment is ordered by:
• Higher initial cost project – Lower initial cost project = Increment
• The new cash flow created from the cash flow increments is
evaluated.
• The IRR of the new cash flow is determined.
14
Incremental Analysis, cont’d
• The decision is then based on the MARR:
• If IRR >= MARR choose the higher initial cost alternative.
➢ This indicates that the additional cost is justified.
• If IRR < MARR choose the lower initial cost alternative.
➢ This indicates that the additional cost is NOT justified.
• The opposite is true if the viewpoint is from the
borrowing perspective instead of the investment
perspective.
15



</details>

---
