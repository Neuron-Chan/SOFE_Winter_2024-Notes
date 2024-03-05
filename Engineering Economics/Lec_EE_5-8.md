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
|Tire Life (warranty)|Price/Tire|
|--|--|
|12 Months|$30.95|
|24 Months|$44.95|
|36 Months|$53.95|
|48 Months|$59.95|

- If she figures that money is worth 12%, which tires should she choose?




## Other Problems to Watch For
- Centralized accounting systems have often been accused by project managers of being too slow or “untimely”
- If an organization establishes numerous files and systems so that stakeholders have the timely data they need, the level of accuracy in one or all systems may be low
  - Analysts making cost estimates will have to consider other internal data sources.
- Inventory or land valued too low because its based on acquisition cost
- Capital equipment being valued too high or too low depending on the depreciation methods and company policy

</details>

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 8 | Rate of Return Analysis</summary>

# Computing Cash Flows
- We describe the benefits and costs as receipts (cash flowing in) and disbursements (cash flowing out) at different points in time
- The foundation of engineering economic analysis are techniques for comparing the value of money at different dates

## Time Value of Money
- When monetary consequences of an alternative occur in a considerable period, we cannot simply add up the various sums of money
- Money
  - It has value over time
  - It is a valuable asset that people are willing to pay to have it available to use
  - It can be rented in roughly the same way that an apartment is rented
    - The charge is called interest instead of rent
    - Our preference for having money now rather than money in the future differs from person to person
      - The preference for having money now rather than later has nothing to do with inflation
    - The bank expresses the time value it puts on money by publishing its interest rate

### Simple Interest
- Interest that is computed only on the original sum and not on accrued interest
  - **Total interest earned = P × i × n = Pin**
    - Where: P = present sum, i = interest rate/period, and n = # of time periods (e.g. years)
  - **Total money after n periods (F) = P + Pin or F = P(1+in)**
    - Where: F = future sum
     
![simple interest ex](../static/EE_4.1.png)

### Compound Interest
- In practice, interest is determined using the compound interest method.
- Simple interest is normally not used unless specifically stated otherwise
- Interest is calculated on the accumulated amount and not simply on the original amount
  - Interest on top of interest

Below, consider a $25,000 loan at 10%/year

| Year "n" | Total in Year "n" | Interest accumulated at end of year "n" | Amount accumulated at end of year "n" |
|-|-|-|-|
| 1 | $25,000 | $2,500 | $27,500 |
| 2 | $27,500 | $2,750 | $30,250 |
| 3 | $30,250 | $3,025 | $33,275 |
| 4 | $33,275 | $3,327.50 | $36,602.50 |

## Repaying a Debt
- There are many ways in which debts are repaid, including the following three plans:
1. Constant principal
2. Interest only
3. Constant payments

# Equivalence
- Equivalence with respect to the “time value of money” implies that a sum of money in one time period may have the same “value” to a different sum in another time period with respect to an interest rate.
  - Example:
    - $1000 now is equivalent to:
      - $1100 one year from now at 10% per year
      - $1050 one year from now at 5% per year
      - $1210 two years from now at 10% per year
      - $1102 two years from now at 5% per year

- Equivalence is dependent on interest rate.
- Equivalence is useful when:
  - There are cash flows (positive and/or negative) over “n” time periods that need to be compared
  - There are alternative comparisons of multiple cash flows
    - Alternative projects with cash flows over “n” time periods


## Single-Payment Compound Interest

### Formulas
- Notation:
- i = interest rate per interest period
- n = number of interest periods
- P = a present sum of money
- F = a future sum of money at the end of the nth interest period, which is equivalent to P at the interest rate i

Assuming interest rate (n) is in years,

  After one year, the future amount at the end of year one would be
  **F = P(1 + i)**

  After two years, the future amount at the end of year two, including the additional interest from year one, would be
  **F = P(1 + i) + iP(1 + i)**

  Equivalent to:
  **F = P(1 + i)(1 + i)** or **P(1 + i)<sup>2</sup>**

  Generalizing:
  **F = P(1 + i)<sup>n</sup>**

### Simple and Compound Interest: Problem

How much more would you owe at the end of 4 years using:
- simple interest at 9% per year or
- compound interest at 9% per year

if you borrowed $150,000 now?

### Solution

_Simple Interest_

F = P + Pin = 150,000 + 150,000(0.09)(4)

F = $204,000

_Compound Interest_

F = P(1 + i)<sup>n</sup>

F = 150,000(1.09)<sup>4</sup>

F = $211,737.24

211,737.24 – 204,000 = $7737.24

You would owe **$7737.24** more with a compound interest arrangement.

![simple interest ex](../static/EE_4.2.png)

![simple interest ex](../static/EE_4.3.png)

![simple interest ex](../static/EE_4.4.png)

![simple interest ex](../static/EE_4.5.png)

# Nominal and Effective Interest
- When specifying an interest rate, we implicitly mention two time periods
- We pay an interest rate of i per time_period1, compounded every time_period2
- Effective interest rate: when these time periods are both the same
- Nominal interest rate: when the two time periods don’t match

## Interest Rate Statements
The terms ‘nominal’ and ‘effective’ enter into consideration when the interest period is less than one year.

**New time-based definitions to understand and remember:**

- Interest period (t) – period of time over which interest is expressed.
  - For example, 1% per month.
- Compounding period (CP) – Shortest time unit over which interest is charged or earned.
  - For example,10% per year compounded monthly.
- Compounding frequency (m) – Number of times compounding occurs within the interest period t

## Understanding Interest Rate Terminology
- A nominal interest rate (r) is obtained by multiplying an interest rate that is expressed over a short time period by the number of compounding periods in a longer time period: That is:
  - r = interest rate per period x number of compounding periods
    - Example: If i = 1% per month, nominal rate per year is
    - r = (1)(12) = 12% per year)
      
- Effective interest rates (i) take compounding into account (effective rates can be obtained from nominal rates via a formula to be discussed later).

IMPORTANT: **Nominal interest rates** are essentially **simple interest rates**. Therefore, they **can never be used in interest formulas**. **Effective rates** must **always be used hereafter in all interest formulas**.

![More About Interest Rate Technology](../static/EE_4.6.png)

## Effective Annual Interest Rates

Nominal rates are converted into effective annual rates via the equation:
𝒊<sub>𝒂</sub> = (𝟏 + 𝒓/𝒎)<sup>𝒎</sup> − 𝟏

𝒊<sub>𝒂</sub> = (𝟏 + 𝒊)<sup>𝒎</sup> − 𝟏

where 
- i<sub>a</sub> = effective annual interest rate
- i = effective rate for one compounding period
- m = number of times that interest is compounded per year
  - Example: For a nominal interest rate of 12% per year, determine the nominal and effective rates per year for (a) quarterly, and (b) monthly compounding
  - Solution:

(a)

Nominal r / year = 12% per year

Nominal r / quarter = 12/4 = 3.0% per quarter

Effective i / year = (1 + 0.03)<sup>4</sup> − 1 = 12.55% per year



    
(b) 

Nominal r /month = 12/12 = 1.0% per month

Effective i / year = (1 + 0.01)<sup>12</sup> − 1 = 12.68% per year


# Continuous Compounding
- The number of compounding periods depends on the number of subdivisions.
- A nominal interest rate of 12%/year compounded:
  - m = 1: yearly (equals 12% effective yearly)
  - m = 2: semi-annually (equals 12.360% effective yearly)
  - m = 4: quarterly (equals 12.551% effective yearly)
  - m = 52: weekly (equals 12.734% effective yearly)
  - m = 365: daily (equals 12.747% effective yearly)
  - m = 525600: hourly (equals 12.749% effective yearly)
- Note: we are approaching a limit!
- For infinite compounding periods (continuously compounded):
  - 𝑖<sub>-𝑎</sub>=(𝑒<sup>𝑟</sup>) − 1
  
- To find compound amount and present worth for continuous compounding and a single payment, we write:
- Compound amount F = P(ern) = P[F/P, r, n]
- Present worth P = F(e−rn) = F[P/F, r, n]
- Square brackets around the factors denote continuous compounding.

## Equivalence and Sustainability
- The formulas and methods we use give reasonable results when applied to time spans of less than a century, but can be misleading when applied to longer time periods
- Many of the problems humanity currently faces require us to plan on a time scale of centuries or longer

</details>

---
