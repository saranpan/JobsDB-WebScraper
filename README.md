# **WebsDB** : The webscraper on JobsDb

---
> using just BeautifulSoup & Requests Packages (No Selenium needed)
<img src="https://github.com/wallik2/Jobsdb_WebScraper/blob/main/picture/JobsDB_meme.jpg?raw=true" width="50%">

[![open in colab](https://camo.githubusercontent.com/52feade06f2fecbf006889a904d221e6a730c194/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667)](https://colab.research.google.com/drive/1J-7DNtrsZj8nN2YhD9g-hypexiVO4mI_?usp=sharing)

--- 
## Brief summary

Basically, the input for our web scraper is a keyword to search like 'doctor','data','chemistry' etc.

Suppose our keyword is 'doctor'. The following table is the first 5 row with that keyword. 

|index|job title                                                                                                        |more info                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |job_company                                        |job_location              |skill requirement 1                               |skill requirement 2                               |skill requirement 3                               |posted time|
|------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|--------------------------|--------------------------------------------------|--------------------------------------------------|--------------------------------------------------|-----------|
|0     |Medical Doctor                                                                                                   |https://th.jobsdb.com//th/en/job/medical-doctor-300003002466359?token=0~426b9c9f-ab6e-4fae-aaa8-168612118aa6&sectionRank=1&jobId=jobsdb-th-job-300003002466359                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |Minor Hotel Group Limited                          |Petchaburi                |Bachelor of Medicine                              |5 to 7 yrs of clinical experience                 |Doctor of Medicine                                |5d ago     |
|1     |Nurse (Telemedicine)                                                                                             |https://th.jobsdb.com//th/en/job/nurse-telemedicine-300003002461247?token=0~426b9c9f-ab6e-4fae-aaa8-168612118aa6&sectionRank=2&jobId=jobsdb-th-job-300003002461247                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |Good Doctor Technology (Singapore) Pte Ltd.        |Pathumwan                 |                                                  |                                                  |                                                  |20h ago    |
|2     |HR staff (HRD Department)(ID:60722)                                                                              |https://th.jobsdb.com//th/en/job/hr-staff-hrd-department-id%3A60722-300003002470542?token=0~426b9c9f-ab6e-4fae-aaa8-168612118aa6&sectionRank=3&jobId=jobsdb-th-job-300003002470542                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |Reeracoen Recruitment Co., Ltd.                    |Wattana                   |Bachelor degree in any fields                     |Good command in English                           |New Graduated                                     |20h ago    |
|3     |แม็คโคร สาขาบางคอแหลม (เจริญกรุง 109) เปิดรับสมัคร พนักงานส่วนซ่อมบำรุง (Staff - General Affair)                 |https://th.jobsdb.com//th/en/job/%E0%B9%81%E0%B8%A1%E0%B9%87%E0%B8%84%E0%B9%82%E0%B8%84%E0%B8%A3-%E0%B8%AA%E0%B8%B2%E0%B8%82%E0%B8%B2%E0%B8%9A%E0%B8%B2%E0%B8%87%E0%B8%84%E0%B8%AD%E0%B9%81%E0%B8%AB%E0%B8%A5%E0%B8%A1-%E0%B9%80%E0%B8%88%E0%B8%A3%E0%B8%B4%E0%B8%8D%E0%B8%81%E0%B8%A3%E0%B8%B8%E0%B8%87-109-%E0%B9%80%E0%B8%9B%E0%B8%B4%E0%B8%94%E0%B8%A3%E0%B8%B1%E0%B8%9A%E0%B8%AA%E0%B8%A1%E0%B8%B1%E0%B8%84%E0%B8%A3-%E0%B8%9E%E0%B8%99%E0%B8%B1%E0%B8%81%E0%B8%87%E0%B8%B2%E0%B8%99%E0%B8%AA%E0%B9%88%E0%B8%A7%E0%B8%99%E0%B8%8B%E0%B9%88%E0%B8%AD%E0%B8%A1%E0%B8%9A%E0%B8%B3%E0%B8%A3%E0%B8%B8%E0%B8%87-staff-general-affair-300003002459826?token=0~426b9c9f-ab6e-4fae-aaa8-168612118aa6&sectionRank=4&jobId=jobsdb-th-job-300003002459826                                                                                                                                                                                                                           |Siam Makro Public Company Limited                  |Bangkor-laem              |                                                  |                                                  |                                                  |2d ago     |
|4     |Accountant/เจ้าหน้าที่บัญชี                                                                                      |https://th.jobsdb.com//th/en/job/accountant-%E0%B9%80%E0%B8%88%E0%B9%89%E0%B8%B2%E0%B8%AB%E0%B8%99%E0%B9%89%E0%B8%B2%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%9A%E0%B8%B1%E0%B8%8D%E0%B8%8A%E0%B8%B5-300003002466185?token=0~426b9c9f-ab6e-4fae-aaa8-168612118aa6&sectionRank=5&jobId=jobsdb-th-job-300003002466185                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |GCC Services (Thailand) Co., Ltd.                  |Sathorn                   |                                                  |                                                  |                                                  |20h ago    |

scraped at 19/11/64 20:15 

---

## Data Features 
There are 8 features that we scrape.
1. **job title**
2. **more info** : URL link contains the full information of that job
3. **job_company** 	
4. **job_location**	
5. **skill requirement 1**	
6. **skill requirement 2**	
7. **skill requirement 3**	
8. **posted time** : The range of time between posted date and now

<img src="https://github.com/wallik2/Jobsdb_WebScraper/blob/main/picture/3.%20label%20feature.jpg?raw=true" width="50%">

<img src="https://github.com/wallik2/Jobsdb_WebScraper/blob/main/picture/4.%20more%20info.jpg?raw=true" width="50%">

Note that in JobsDB platform treat the *skill requirement 1-3* as optional feature, while the rest of the features are required. This mean it's possible to see the missing value that is scraped (only miss ing in Skill Requirement 1-3). 

Also note that the data in *skill requirement 1-3* are all ambigious to name the categories for it. It maybe just the data about that job 


---
## How we obtain those data features

1. We manually explore where each data feature was embbed in that webpage source code.

<img src="https://github.com/wallik2/Jobsdb_WebScraper/blob/main/picture/5.%20Compare.jpg?raw=true" width="75%">                

2. Then we use *requests* to obtain the source code of the webpage given the job keyword

3. Lastly, we use beautifulsoup to parse the imported source code (just like RegEx) using the location of each feature, then extract them out

Once we extracted them, we can write those data to the csv file..
