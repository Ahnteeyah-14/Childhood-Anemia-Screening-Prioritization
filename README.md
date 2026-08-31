# Childhood-Anemia-Screening-Prioritization
A data analytics case study using Demographic and Health Survey (DHS) data to explore childhood anemia patterns and identify socioeconomic and maternal health indicators that can help prioritize pediatric anemia screening in resource-limited settings.  

## 1. Background / Context
Childhood anemia remains a massive public health crisis in developing countries, severely impacting physical growth, cognitive development, and immunity. Although early diagnosis yields the best intervention outcomes, resource-limited healthcare systems are constrained by budget, laboratory logistics, and staffing, preventing universal testing. Concurrently, national tools like the Demographic and Health Survey (DHS) gather extensive, routine data on mothers and households. This project demonstrates how leveraging existing socioeconomic profiles can reliably guide and prioritise clinical screening interventions without escalating field collection costs.
## 2. Business / Research Problem
•	Research Question:
How can routinely collected maternal and household health indicators be modelled to prioritise pediatric anemia screening in resource-constrained regions?
•	Strategic Shift
: Moving from static descriptive reporting to a clinical decision-support framework that identifies the most accurate socio-environmental indicators of child vulnerability.
## 3. Data Collection & Dataset Description
The study used data from the Demographic and Health Survey (DHS):
•	Outcome Metric: Child Anemia Status (Classified into Not Anemic, Mild, Moderate, Severe).
•	Predictor Metrics: Maternal Anemia Status, Maternal Education level, Household Wealth Index, and Place of Residence.
•	Sample Volume: Original data consisted of 33,924 records; filtered down to a highly reliable 10,062 complete observations for analytical validity.
## 4. Data Cleaning & Preparation
•	Full-Scope Profiling: Configured Power Query column profiling over the entire dataset instead of the default 1,000-row preview to capture comprehensive data quality flaws.
•	Record Elimination: Removed 25,742 records lacking mandatory hemoglobin values (`Child_Hb` and `Child_Anemia`), ensuring clinical integrity. An additional 120 rows with missing maternal anemia inputs were also filtered out to prevent variable distortion.
•	Validation: Verified the remaining 10,062 records for strict data type matching (text, whole numbers, decimals) and categorical alignment.
## 5. Analytical & Dashboard Approach
Using Microsoft Power BI, Power Query, and advanced DAX modelling, an interactive decision-support tool was built. The engine computes real-time population rates and slices childhood anemia distributions against maternal profiles, providing non-technical stakeholders with immediate visual answers to critical strategic questions.
## 6. Analysis Tasks
The visualization architecture was designed to answer these fundamental questions for stakeholders:
•	What is our baseline childhood anemia prevalence, and how severe is it? 
•	Does a child's geographic location (rural vs. urban) shift their risk? 
•	How strongly do household wealth and maternal education shield a child from anemia? 
•	Can a mother's own anemia status be used as a direct indicator to prioritize her child's screening?
## 7. Insights & Visual Findings
## Visual 1: Distribution of Childhood Anemia Status

<img width="590" height="286" alt="image" src="https://github.com/user-attachments/assets/8ba11a66-3a6b-45e6-a13a-85f0cd739964" />
 
 Healthy clinical observations account for 3.1K children, while mild anemia tracks at 2.7K cases.
The bulk of the crisis is concentrated in the Moderate Anemia band, capturing 3.9K children (roughly 39% of the entire population).
Interventions cannot wait for severe symptoms to appear. The 3.9K moderate cases represent the primary window for preventative treatment before severe clinical deterioration occurs.

## Visual 2: Childhood Anemia by Place of Residence

<img width="276" height="269" alt="image" src="https://github.com/user-attachments/assets/4843c668-c2e3-4176-af98-36cc4baec4f9" />

 
Our data is compiled from a blend of 3.93K urban families and 6.14K rural families.
 A massive 60.98% of the high-prevalence cohort is entirely isolated within rural areas where access to laboratory equipment and diagnostic services is highly constrained.
 Centralized urban hospital screening programs will structurally fail to reach the demographic core. Healthcare resources must be redistributed to rural clinics and mobile screening vans.

## Visual 3: Childhood Anemia Across Household Wealth Groups

<img width="419" height="283" alt="image" src="https://github.com/user-attachments/assets/92aae57d-e47e-42cd-b16a-b520b2b5f588" />

 
Economic standing is a significant driver of childhood outcomes, with the wealthiest families securing a high baseline health rate (46.51% of their children are not anemic).
 In the poorest families, the moderate-to-severe childhood anemia burden escalates dramatically, leaving only 20.49% of children completely healthy.
Where budgets prevent universal testing, poverty mapping acts as a natural diagnostic filter. Prioritizing 'Poorest' and 'Poorer' households directly maximizes field screening yield.

## Visual Block 4: Childhood Anemia by Maternal Anemia Status

<img width="530" height="300" alt="image" src="https://github.com/user-attachments/assets/198c1690-3c37-4f1d-861a-8a7da8dfc905" />

 
 Children belonging to healthy, non-anemic mothers show the strongest resistance patterns, with 39.85% remaining fully non-anemic.
 Mothers suffering from severe anemia have children with a combined 64.43% moderate-to-severe anemia rate, with less than 15.44% escaping the condition entirely.
Maternal anemia is our most potent clinical proxy. If a full child screening is unavailable, testing the child of any woman diagnosed with maternal anemia provides an immediate, high-probability risk capture.

## Visual 5: Childhood Anemia Across Maternal Education Levels

<img width="484" height="303" alt="image" src="https://github.com/user-attachments/assets/a74c85f5-b7be-4d03-aef4-c183c3c80be1" />

 
Higher maternal education functions as an effective protective layer, yielding a clean 50.99% non-anemic rate among their children.
For mothers with no formal education, that protective layer collapses, resulting in 45.62% of their children developing moderate anemia and only 24.02% remaining healthy.
Clinical screening must be integrated with direct educational outreach. Nutrition literacy programs deployed through community channels are required to break the cross-generational cycle.

## 8. Actionable Recommendations
•	1. Establish Proxy-Driven Screening: Mandate automatic pediatric testing for any child whose mother presents with positive anemia findings during routine clinical consultations.

•	2. Geographically Reallocate Assets: Shift diagnostic funding, mobile vans, and supply chains directly toward rural clinics to address the 60.98% vulnerable rural majority.

•	3. Deploy Wealth-Indexed Filters: Utilize existing regional economic and poverty data to bypass universal screening costs, instantly focusing testing resources on the lowest two wealth percentiles.

•	4. Unify Family Care Checkups: Co-locate maternal postnatal checkups with early childhood nutrition interventions, creating a single unified family screening window.

## 9.  Expected Impact
•	Resource Optimization: Drastically reduces the cost of universal screening by filtering focus to high-risk groups. 

•	Proactive Intervention: Catching the 3.9K "Moderate" cases before they degrade into severe, resource-heavy clinical emergencies. 

•	Data-Driven Partnerships: Equips local health departments and NGOs with visual, geographic, and socioeconomic evidence to secure targeted funding. 

## 10. Challenges & Solutions
•	Incomplete Regional Data: Originally, 25,742 records lacked essential hemoglobin results. Solution: Purged incomplete records to base findings strictly on 10,062 fully validated data points, ensuring statistical integrity.

•	Default Tool Limitations: Power Query was initially profiling only a fraction of the dataset. Solution: Switched to "Column Profiling Based on Entire Dataset" to accurately inspect and clean the full data catalog.

## 11. Conclusion
This case study proves that we do not need expensive, universal testing programs to make an impact on public health. By smartly repurposing routine demographic indicators—maternal health, education, wealth, and location—we can build an automated, data-driven prioritization framework. This ensures that in resource-limited settings, every screening dollar spent is directed precisely to the children who need it most. 


## THANK YOU
