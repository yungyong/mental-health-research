# Mental Health research

This repository contains my research on the mental health issues survey dataset 
(https://www.kaggle.com/osmi/mental-health-in-tech-survey). 
In this research some correlations are found and 2 models are trained to predict,
 whether a human should seek treatment for a mental health condition or not.

The survey addresses following issues:
---

* timestamp                     
* age                           
* gender                        
* country                        
* state                          
* self_employed                  
* family_history                
* treatment                     
* work_interfere                 
* no_employees                   
* remote_work                    
* tech_company                 
* benefits                      
* care_options                   
* wellness_program               
* seek_help                    
* anonymity                      
* leave                          
* mental_health_consequence      
* phys_health_consequence        
* coworkers                      
* supervisor                     
* mental_health_interview        
* phys_health_interview         
* mental_vs_physical             
* obs_consequence              
* comments   

Data research
---

The most people taking part in this survey are from USA. Other people's countries:

![](https://habrastorage.org/webt/qv/e0/9d/qve09dgu_yojydesdsdygbzltpm.png)


The age has normal distribution with parameters:
* mean       32.019138
* std         7.375005
* min         5.000000
* 25%        27.000000
* 50%        31.000000
* 75%        36.000000
* max        72.000000

![](https://habrastorage.org/webt/9k/tu/zi/9ktuzicun9-giquwqobjzm4tdq4.png)

Women and other gender people are more tended to seek treatment, than men.

![](https://habrastorage.org/webt/hj/i1/9q/hji19q4uenijzktffakkmoomzlu.png)

Between 20 and 40 years they are women, who seek treatment more often, but after 40 years – men.


![](https://habrastorage.org/webt/cp/ms/vd/cpmsvdp1z0ohingqclmxdvugkwk.png)

Random forests' results
---

After preparing data and greed search on parameters 'n_estimators', 'criterion', 'max_depth', 'min_samples_leaf'
 for RandomForestClassifier (sklearn), obtained
 
*  0.80% accuracy

with best parameters:

* 'criterion': 'entropy',
*  'max_depth': 15,
*  'min_samples_leaf': 3,
 * 'n_estimators': 64.