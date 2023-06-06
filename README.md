Third Party Risk Management (TPRM) is the process of analyzing and controlling risks presented to your company, your data, your operations and your finances by parties OTHER than your own company. Due Diligence is the investigative process by which a company or other third party is reviewed to determine its suitability for a given task. Due diligence is an ongoing activity, including review, monitoring, and management communication over the entire vendor lifecycle. No universally-accepted framework like CObIT or COSO.
![image](https://github.com/Lokavardhan/Monitoring-Websites-using-Python-/assets/127578172/86e9f693-7614-4b30-881d-1ee4595f89fd)


Monitoring Websites using Python 

Input and output:

import requests 
import pandas as pd
df = pd.read_excel(r"C:\Users\LOKAVARDHAN\Downloads\sites.xlsx")
for index, websites in df.iterrows():
   
    try:
        response = requests.get(websites["Name"])
    
        df.at[index,"status_code"]="Site is ok {}".format(response.status_code)

    except:
         df.at[index,"status_code"]= "site is not available"
print(df) 
![image](https://github.com/Lokavardhan/Monitoring-Websites-using-Python-/assets/127578172/9ef47b77-7912-41d9-8599-b5017a52f3cd)
