# USA-hospital
A large volumes of patient, admission, condition, and billing data across multiple facilities and locations across Hospitals in USA.
# US Hospital Operations Dashboard
*Power BI* 
_Report structure: Overview · Demographic · Insights pages_    

# Hospital Problem

US hospitals generate large volumes of patient, admission, condition, and billing data across multiple facilities and locations, but this data is scattered and hard to interpret in raw form. Without a consolidated view, hospital administrators struggle to answer basic operational questions: which hospitals are overloaded, what conditions are most costly, whether patients are satisfied, and whether length of stay is trending up or down.
# Objective
_Build a single interactive Power BI dashboard that lets hospital management_ 

•	Monitor patient volume, admissions, and length of stay in real time

•	Understand patient demographics (gender, age, location)

•	Track billing performance by condition and month

•	Measure patient satisfaction

•	Drill down by hospital, condition, and time period using slicers

# Skills Applied

•	Data modeling: fact/dimension design (Hospital fact table + Date table + lookup dataset)

•	DAX measures: total patients, average length of stay, average satisfaction, YoY billing comparison, total billing

•	Data visualization: cards, donut/bar/column/line charts, gauge, treemap, chart, pivot table

•	Filtering: Year / Month / Hospital slicers for interactive drill-down

# Key Metrics Overview

| Metric	     |Value	   | Trend              |
|-----------   | ------| ---------------------|
|Total Patients |	5,000 |	vs Last Month +0.1% |
| Total Billing Amount |	$1.247B | YoY +2%   |
| Average Length of Stay |	23.30 days |	YoY +0% |
| Most Common Condition |	Sepsis | 	—  |
| Patient Satisfaction |	3 / 6	| gauge score |

With 5,000 total patients and $1.247B in total billing, the average billed amount works out to roughly $249,000 per patient. Average length of stay sits at 23.3 days, flat year-over-year, and overall patient satisfaction registers a modest 3 out of 6+.

# Key Metrics Summary 

### _Patients by Gender_

There was an even split between male (49.6%) and female (48.5%) patients, with 1.9% recorded as other.

### _Admitted Patients by Month_

Admissions range from as low as 376 in February to a high of 468 in January, averaging ~417 per month.

### _Admitted Patients by Hospital (Top 9)_

NYU Langone Health leads with 267 admitted patients, follow by massachuetts with 265, Univ. of washington 264, Vanderbilt Univ 262, Cedars-Sinai Med. 258, Barne-jewish Hospital 255, Northwestern 255, Houston Meth. 253, Univ. of Pitt. 253. the volumes are tightly clustered across the top 9 hospitals (253–267).

### _Patients by Age Band_

Other leads with 801, While 71–80 leads with 595 which is the largest age bands, and 5–10 is smallest at 335.

### _Patients by Location (Top 5)_

New York, NY leads with  (517), Los Angeles, CA (504),Boston, MA (265), Seattle, WA (264) and Nashville, TN (262). Which  far outpace all other cities, which cluster between 216–255 patients.

### *_Total Billing by Condition_*
 
Cancer generates the highest billing at $68M, followed by Kidney Failure and Liver Disease $67M each. While  Fracture and Obesity are lowest at $54M.

### _Billing by Month_
May is the peak billing month at $121M(highest), Billing dips to $96M in June, September, and December( which are deepest months).

### _Patients by Hospital and Condition (excerpt)_
| Hospital |	Anemia |	Appendicitis |	Arthritis |	Asthma |	Cancer |	Cardiac Arrest |	COPD |
|----------|--------|---------------|-------------|-------|----------|---------------|--------|
| Barnes-Jewish Hospital	| 16 |	17 |	15 |	10 |	9	| 17 |	12 |
| Cedars-Sinai Medical Center  |	15 |	11 |	13 |	13 |	17 |	14 |	15 |
| Cleveland Clinic |	6 |	14 |	9	 | 18 	 |	13 	 |	10 	 |	11 	 |
| Duke University |	11 |	10 |	20 |	13 |	11 |	13 |	7  |




# Key Insights

•	 *_Revenue concentration by condition is shallow, not steep:_* billing ranges narrowly from $54M to $68M across all 20 conditions no single condition dominates spend, meaning cost-control efforts need to span the full condition list rather than target one or two outliers.

•	*_Seasonality in billing doesn't track admission volume:_* May shows the highest billing ($121M) despite average admission counts (452), while January has the highest admissions (468) but only mid-tier billing ($112M) suggesting higher-cost cases cluster in specific months rather than following raw patient volume.

•	*_Two cities drive disproportionate demand:_* New York (517) and Los Angeles (504) each host roughly double the patient volume of the next-tier cities (250–265), signaling these two markets need dedicated capacity planning.

•	*_Hospital admissions are evenly distributed:_* the top 9 hospitals sit within a tight 253–267 patient band, indicating good load-balancing across the network rather than one overloaded flagship facility.

•	Satisfaction (3/6) alongside a flat 23.3-day average length of stay suggests stay duration isn't improving even as satisfaction sits at the midpoint worth a deeper root cause look (staffing, discharge process, communication) rather than assuming volume alone is the driver.

•	Age band “other” (801) and 71–80 (595) are the two largest patient groups, together making up close to 28% of all patients relevant for staffing geriatric and specialty care capacity.

# Strategic Recommendations

•	Build a May billing deep-dive: identify which conditions or procedures spiked that month to understand whether it's seasonal (e.g., flu/allergy season complications) or a one-off billing anomaly.

•	Since billing is spread evenly across conditions, pursue network-wide cost initiatives (standardized care pathways, bulk procurement) rather than single-condition programs.

•	Add dedicated capacity planning for New York and Los Angeles given their outsized patient volumes relative to every other market.

•	Investigate the flat length-of-stay trend paired with mid-range satisfaction run a discharge-process and staffing review to identify whether LOS can be safely reduced without harming outcomes.

•	Expand geriatric and specialty resources for the 71–80 and “other” age bands, which together represent the largest share of patients.

•	Add year-over-year and target/benchmark lines to the billing and admissions visuals so future readings are judged against goals, not just historical values.

