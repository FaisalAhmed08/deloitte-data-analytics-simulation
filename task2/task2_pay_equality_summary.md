# Task 2: Gender Pay Equality Classification

## Objective
Daikibo Industrials raised concerns about gender-based pay inequality. We were provided with an Excel sheet containing:
- `Factory`
- `Job Role`
- `Equality Score` (range: -100 to +100; 0 is ideal)

Our task was to classify each record based on the **level of pay fairness**.

---

## Methodology

### Classification Logic (New Column: *Equality Class*)
- **Fair**: Score between -10 and +10 (inclusive)
- **Unfair**: Score between -20 and -11 OR between 11 and 20
- **Highly Discriminative**: Score < -20 OR > 20

### Sample Formula (in Excel):
```excel
=IF(AND([@[Equality Score]]>=-10,[@[Equality Score]]<=10),"Fair",
IF(AND([@[Equality Score]]>-20,[@[Equality Score]]<-10), "Unfair",
IF(AND([@[Equality Score]]>10,[@[Equality Score]]<20), "Unfair","Highly Discriminative")))
