# Anomaly Detection
Team members: **Jeremy Lagunas**, **Meredith Wang**, **Luis Arce**

August 2022

<a href="#"><img alt="Python" src="https://img.shields.io/badge/Python-013243.svg?logo=python&logoColor=white"></a>
<a href="#"><img alt="Pandas" src="https://img.shields.io/badge/Pandas-150458.svg?logo=pandas&logoColor=white"></a>
<a href="#"><img alt="NumPy" src="https://img.shields.io/badge/Numpy-2a4d69.svg?logo=numpy&logoColor=white"></a>
<a href="#"><img alt="Matplotlib" src="https://img.shields.io/badge/Matplotlib-8DF9C1.svg?logo=matplotlib&logoColor=white"></a>
<a href="#"><img alt="seaborn" src="https://img.shields.io/badge/seaborn-65A9A8.svg?logo=pandas&logoColor=white"></a>
<a href="#"><img alt="plotly" src="https://img.shields.io/badge/plotly-adcbe3.svg?logo=plotly&logoColor=white"></a>
<a href="#"><img alt="sklearn" src="https://img.shields.io/badge/sklearn-4b86b4.svg?logo=scikitlearn&logoColor=white"></a>
<a href="#"><img alt="SciPy" src="https://img.shields.io/badge/SciPy-1560bd.svg?logo=scipy&logoColor=white"></a>

<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>

## :chart:   Project Goals
Email to analyst:


    Hello,


    I have some questions for you that I need answered before the board meeting Thursday afternoon. My questions are listed below; however, if you discover anything else important that I didn’t think to ask, please include that as well.

    (Questions are listed in EDA)
- Send your email before the due date and time (5:00 PM CST, Thursday 8/23/22) to staff-kalpana@codeup.com (Only one team member should do this on behalf of the whole team).

- In Google Classroom, submit a link to a final notebook on GitHub that asks and answers questions in detail. Be sure to document the work you do to justify findings. Remember, your stakeholder may need to show your notebook during the board meeting. Try and make it as clear and professional as possible for them.

<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>

## Questions
1. **Which lesson appears to attract the most traffic consistently across cohorts (per program), which lessons are least accessed??**(Luis)

2. **Is there a cohort that referred to a lesson significantly more than other cohorts seemed to gloss over?** (Jeremy)

3. **Are there students who, when active, hardly access the curriculum? If so, what information do you have about these students?** (Luis)

4. **Is there any suspicious activity, such as users/machines/etc accessing the curriculum who shouldn’t be? Does it appear that any web-scraping is happening? Are there any suspicious IP addresses?**(Meredith)

5. **At some point in 2019, the ability for students and alumni to access both curriculums (web dev to ds, ds to web dev) should have been shut off. Do you see any evidence of that happening? Did it happen before?**(Jeremy)

6. **What topics are grads continuing to reference after graduation and into their jobs (for each program)?**(Merdith)

<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>

## :placard:    Project Plan
#### :one:   Data Acquisition

<details>
<summary> Gather data from mySQL database</summary>

- Create env.py file to establish connection to mySQL server

- Use **curriculum_log** database in the mySQL server

- Write query to join useful tables to gather all data about the customers:  <u>customers, contract_types, payment_types, internet_service_types </u>
     ```sh
     SELECT * FROM logs LEFT JOIN cohorts ON logs.user_id = cohorts.id
     ```
</details>

<details>
<summary> acqure.py</summary>

- Create acquire.py and user-defined function `get_data()` to gather data from mySQL
     ```sh
     def get_data():
        if os.path.isfile('curriculum.csv'):
    
            df = pd.read_csv('curriculum.csv', index_col=0)
        
        else:

            df = new_data()

            df.to_csv('curriculum.csv')
        
        return df
    ```
- Import [acquire.py](acquire.py)

- Test acquire function

- Calling the function, and store the table in the form of dataframe
    ```sh
    df = acquire.get_data()
    ```
</details>

#### :two:   Data Preparation

<details>
<summary> Data Cleaning</summary>

- **Missing values: 
    
- **Data types:
    
- Create function `prep_data` to clean and prepare data with steps above

- Import [prepare.py](prepare.py)

- Test prepare function

- Call the function, and store the cleaned data in the form of dataframe
</details>

#### :three:   Exploratory Analysis
- Address 6 questions raised in email

- Create visualizations for each question

- Address questions raised in email.
    
## Team Timeline
By Aug 23
- [x] Sketch out plan and each team member task
- [x] EDA questions assigned
- [x] Data Acquisition: acquire data from database 
- [x] README initial structure

By Aug 24 12 PM
- [ ] EDA complete

By Aug 24 end of day
- [ ] Final report complete
- [ ] Gmail response
- [ ] Fianl tweeks

By Aug 25 10:30 AM
- [ ] README complete

<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>

## :open_file_folder:   Data Dictionary
**Variable** |    **Value**    | **Meaning**
---|---|---
*date* | datetime | editing...
*time* | datetime | editing... 
*path* | string | The path the user is on
*user id* | float | The primary key of log table, indicating each user
*ip* | string | The user's ip address
*name* | string | The name of user's cohort
*slack* | string | The name of the slack chanel that user belongs to
*start date*| datetime | The start date of the cohort
*end date* | datetime | The end date of the cohort
*created at* | datetime | editing...
*updated at* | datetime | editing...
*program id* | datetime | This indicates which program is the user in

<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>

## :key:    Key Findings
▪️
    
▪️ 
 
▪️ 

<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>

## :high_brightness:    Recommendations
▪️ 

▪️ 

▪️ 

<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>
## 🔜  Next Steps
▪️

▪️ 

▪️ 
