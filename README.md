# Autoprognosis for Multiple Sclerosis

The previously developed autoML tool, AutoPrognosis 2.0 (https://github.com/vanderschaarlab/AutoPrognosis), was used to develop a modelling pipeline for multiple sclerosis (MS) treatment prediction. 

The model was developed using data from MSBase (https://www.msbase.org/), and externally validated on The Italian MS and Related Disorders Register (RISM; Trojano et al., 2019).

This code outlines the process of taking appropriately formatted data and running AutoPrognosis 2.0 on it to identify the best modelling pipeline. 

# Background

Timely initiation of disease-modifying therapy (DMT) is critical to preventing disability accrual in multiple sclerosis (MS), yet treatment response varies substantially between individuals. Validated tools for predicting individualized treatment response, particularly at treatment initiation, remain lacking (Hegen et al., 2016; Ontaneda et al., 2019).

Few such tools are available for use before treatment initiation. The Rio Score, modified Rio Score, and MAGNIMS score all require on-treatment clinical or radiological data, rendering them uninformative at the point of treatment selection (Kunchok et al., 2021; Rio, Castillo, et al., 2009; Sormani et al., 2021; Sormani et al., 2016; Sormani et al., 2013; Tutuncu et al., 2021). The framework for personalized treatment proposed by (Stuhler et al., 2020) similarly requires post-treatment data, restricting utility to decisions around switching therapies. 

Models which are designed for use at treatment initiation struggle to maintain predictive performance over medium- to long-term follow-up (Kalincik et al., 2017). 

# Models 
Separate time-to-event models were developed for two common outcomes in MS: relapse and confirmed disability worsening (CDW). Treatment efficacy group was included as a model feature, such that treatment group was modelled alongside other patient-level predictors (Kunzel et al., 2019). 

The primary analysis estimated the prognostic risk associated with starting a treatment within each efficacy category without censoring at subsequent treatment changes. This approach was intended to reflect clinical use at the time of first treatment choice, when subsequent treatment trajectories are not yet known.
