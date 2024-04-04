# Software Project Management (SOFE3490)

| Category                     | Mark   |
|------------------------------|--------|
| 5 Lab Assignments            | 15%    |
| Tutorials                    | 10%    |
| In-Class Activities/Quizzes  | 10%    |
| Midterm (Feb. 26th)          | 30%    |
| Final                        | 35%    |

Office Hours: Mondays 7-8 PM, SIRC 3386


**Quizzes:**
- Lockdown browser will be used in quizzes and must be done in class. 
- Expect a quiz bi-weekly. *(Lowest quiz mark dropped)*

**Midterm:**
- The exam will be on Feb. 26th during the class time. (**yes that means it's at 8pm**)
- No midterm deferral, marks will be added to the final exam

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 9 | Monitoring & Control</summary>
  
    
  # Outline:
  - Avoid the dangers of unrealistic estimates.
  - Understand the range of estimating methods that can be used
  - Estimate projects using a bottom-up approach
  - Count the function points and object points for a system
  - Estimate the effort needed to implement software using a procedural programming language
  - Understand the COCOMO approach
  
  
![control cycle](../static/SPM_9_1.png)

# Responsibilities
- The details relating to project progress have to originate with the people actually doing the work and have then to be fed up through the management structure.

![responsibilities](../static/SPM_9_2.png)

## Information overload
- At each management level there is going to be some summarising and commentary before information is passed up to the next level.
- This means that there is always a danger of "information overload" as information passes from the many to the few.

# Assessing progress
Checkpoints – predetermined times when progress is checked 
- Event driven: check takes place when a particular event has been achieved
- Time driven: date of the check is pre-determined

Frequency of reporting
- The higher the management level then generally the longer the gaps between checkpoints

## Categories of reporting

|Report type|Examples|Comment|
|-----------|--------|-------|
|Oral formal regular|weekly or monthly progress meetings|while reports may be oral formal written minutes should be kept|
|Oral formal ad hoc|end-of-stage review meetings|while largely oral, likely to receive and generate written reports.|
|Written formal regular|job sheets, progress reports|normally weekly using forms|
|Written formal ad hoc|exception reports, change reports||
|Oral informal ad hoc|canteen discussion, social interaction|often provides early warning; must be backed up by formal reporting|

# Collecting progress details
Need to collect data about:
- Achievements
- Costs
A big problem: how to deal with partial completions (99% completion syndrome)

Possible solutions:
- Control of products, not activities
- Subdivide into lots of sub-activities

## Red/Amber/Green Reporting
- Identify key tasks
- Break down into sub-tasks
- Assess subtasks as:
  - Green – ‘on target’
  - Amber – ‘not on target but recoverable’
  - Red – ‘not on target and recoverable only with difficulty’
Status of ‘critical tasks’ is particularly important
- ‘Critical tasks’ would be those on the critical path and/or reliant on critical resources

![activity assessment sheet](../static/SPM_9_3_1.png)


![visualizing progress via gantt charts](../static/SPM_9_3_2.png)

![visualizing progress via gantt charts](../static/SPM_9_3_3.png)

### Visualizing Progress Using Slip Charts

![Visualizing Progress Using Slip charts](../static/SPM_9_3_4.png)

- The more jagged the line, the more it means that there are some activities that are lagging to various degrees and some that are ahead of themselves.
- A very jagged line means that there is scope for re-planning to move resources from those activities that are ahead to those that are behind.

![Visualizing Progress Using timeline](../static/SPM_9_3_5.png)

### Cost monitoring
![cost monitoring](../static/SPM_9_3_5.png)

- A project could be late because the staff originally committed have not been deployed
- In this case the project will be behind time but under budget
- A project could be on time but only because additional resources have been added and so be over budget
- Need to monitor both achievements and costs

# Earned Value Analysis
- Planned Value (PV) :The authorized budget assigned to scheduled work.
- Earned Value (EV) :The measure of work performed expressed in terms of the budget authorized for that work
- Actual cost (AC) : The realized cost incurred for the work performed on an activity during a specific time period

## Accounting Conventions
- Earned Values for works started but not completed are as assigned by:
  - 50/50: half allocated at start, the other half on completion. These proportions can vary e.g. 0/100, 75/25 etc
  - Milestone: current value depends on the milestones achieved
  - Units processed
- Can use money values, or staff effort as a surrogate

## Earned Value – an example
- Tasks
  - Specify module 5 days
  - Code module 8 days
  - Test module 6 days
- At the beginning of day 20, PV = 19 days
- If everything but testing completed EV = 13 days
- Schedule variance = EV-PV i.e. 13-19 = -6
- Schedule performance indicator (SPI) = EV/PV = 13/19 = 0.68
- SV<0 or SPI <1.00  project behind the schedule

## Earned value analysis – actual cost
- Actual cost (AC) is also known as Actual Cost of Work Performed (ACWP)
- In previous example, if:
  - ‘Specify module’ actually took 3 days
  - ‘Code module’ actually took 4 days
- Actual cost = 7 days
- Cost Variance (CV) = EV-AC i.e. 13-7 = 6 days
- Cost Performance Indicator (CPI) = EV/AC= 13/7 = 1.86
- CV>0 or CPI > 1.00  project within budget

- CPI can be used to produce new cost estimate
- Budget At Completion (BAC) or current budget allocated to total costs of project
- Estimate At Completion (EAC) or updated estimate = BAC/CPI
- e.g. say BAC is $19,000 and CPI is 1.86
- EAC = BAC/CPI = $10,215 (projected costs reduced because work being completed in less time)

# Time variance
- Time variance (TV): difference between time when specified EV should have been reached and time it actually was
- For example say an EV of $19000 was supposed to have been reached on 1st April and it was actually reached on 1st July then TV = - 3 months

## Calculating Variance and Index Values

If the following equations are positive, it's good.

SV = EV - PV

CV = EV - AC

If the following equations are greater than 1, it's good.

SV = EV / PV

CV = EV / AC

# Prioritizing monitoring
We might focus more on monitoring certain types of activity e.g.
- Critical path activities
  - by definition if these are late then the project as a whole will be delayed
- Activities with no free float – if delayed later dependent activities are delayed
  - A project with no free float will delay following dependent activities, although the project end date may not be directly threatened.
- Activities with less than a specified float
  - projects when being executed can be very dynamic: some activities will take longer than estimated others less; this could lead to the critical shifting. Activities with small floats are the most likely to find themselves turned into activities on the critical path if their floats get eroded.
- High risk activities
  - If the standard deviation for an activity is large, this indicates that there is a lot of uncertainty about how long it will actually take.
- Activities using critical resources
  - some resources may only be available for a limited period and if the activities that need the resource are delayed the resource could become unavailable.

  ## Getting back on track: options
- Renegotiate the deadline
  - One way of doing this is to divide the deliverables into ‘tranches’ (see Lecture/Chapter 3), delivering the ones most valuable to the client on or before the deadline, but delaying less valuable ones.

**If not possible then**:
- Try to shorten critical path
- The idea is to try to get things done more quickly by adding more staff. Some activities lend themselves to this more readily than others – it is often quite difficult to do this with software development. It also increases costs.
- For example:
  - Work overtime
  - Re-allocate staff from less pressing work
  - Buy in more staff










</details>

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 10 | TBD</summary>

 Coming soon!
 
</details>

