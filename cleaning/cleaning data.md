Mediscribes:- 
1) Dropped 'Race' column
2) Dropped all the duplicate entries in the merged csv
3) Created a new csv file with columns 'HospitalID', 'HospitalName', 'Short_HospitalName', 'HospitalTimeZone' from the merged csv and dropped all these columns except 'HospitalID'.

Pulse:-
1) Dropped all the duplicate entries in the merged csv
2) Made the following changes in the columns-
        df['PatientGender']=df['PatientGender'].str.replace('feMale','Female', regex=False)
        df['PatientGender']=df['PatientGender'].str.replace('female','Female', regex=False)

Rivercity:-
1) Dropped all the duplicate entries in the merged csv
2) Made the following changes in the columns-
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('SUR - SURGICAL', 'SURGICAL', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Surgical Services', 'SURGICAL', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('SURGICAL ', 'SURGICAL', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Surgical', 'SURGICAL', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('SURGERY', 'SURGICAL', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Surgery', 'SURGICAL', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].replace('SURGICAL Services', 'SURGICAL', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('INTENSIVE CARE UNIT', 'ICU/CCU', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('MEDICAL/I', 'MEDICAL', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('MED - MEDICAL', 'MEDICAL', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Nursery 1', 'NURSERY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Nursery 2', 'NURSERY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Cardiology', 'CARDIOLOGY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('OBD - OB DELIVERED', 'OB DELIVERED', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('OBU - OB UNDELIVERED', 'OB NOT DELIVERED', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('GYN - GYNECOLOGY', 'OB/GYN', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('GYNECOLOGY', 'OB/GYN', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Gynecology', 'OB/GYN', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('OBSTETRICS/OB/GYN', 'OB/GYN', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Obstetrics', 'OB/GYN', regex=False)  
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Nursery 3', 'NURSERY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Psychiatry', 'PSYCHIATRY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Psychiatry/Adult', 'PSYCHIATRY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Newborn', 'NEWBORN', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('NEWBORN/NURSERY', 'NEWBORN', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('LABOR AND DELIVERY OBSERVATION', 'LABOR AND DELIVERY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Radiology', 'RAD-RADIOLOGY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('OBSTETRICS/OB/GYN', 'OB/GYN', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Pediatrics', 'PEDIATRICS', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('Urology', 'URO - UROLOGY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('PSY - PSYCHIATRIC', 'PSYCHIATRY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('EMERGNECY ROOM OBSERVATION', 'ER - EMERGNECY ROOM', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].replace('23 HOUR OBSERVATION 600', '23 HOUR OBSERVATION NURSERY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('23 HOUR OBSERVATION - ICU', '23 HOUR OBSERVATION NURSERY ', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('23 HOUR OBSERVATION 250', '23 HOUR OBSERVATION NURSERY ', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('23 HOUR OBSERVATION 350', '23 HOUR OBSERVATION NURSERY ', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('23 HOUR OBSERVATION 200', '23 HOUR OBSERVATION NURSERY ', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('23 HOUR OBSERVATION 300', '23 HOUR OBSERVATION NURSERY ', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('23 HOUR OBSERVATION 500', '23 HOUR OBSERVATION NURSERY ', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('23 HOUR OBSERVATION NURSERY ', '23 HOUR OBSERVATION NURSERY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('NURSERY 3', 'NURSERY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('NURSERY 2', 'NURSERY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('NURSERY 1', 'NURSERY', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('OBSTETRICS', 'OB/GYN', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('PEDIATRICS/MEDICAL', 'PEM - PEDIATRIC/MEDICAL', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('UNKNOWN', 'OTHER', regex=False)
        df['serviceLineDesc'] = df["serviceLineDesc"].str.replace('UROLOGY', 'URO - UROLOGY', regex=False)
        df['RefinedWorktype'] = df["RefinedWorktype"].str.replace('Stress Test', 'Stress Test Report', regex=False)
        df['RefinedWorktype'] = df["RefinedWorktype"].str.replace('Clinical Summary Note', 'Clinic Note', regex=False)
        df['RefinedWorktype'] = df["RefinedWorktype"].str.replace('Physical Therapy Evaluation', 'Physical Therapy Report', regex=False)
        df['payerDescription'] = df["payerDescription"].str.replace('Medicare', 'MEDICARE', regex=False)
        df['State'] = df["State"].str.replace('nj', 'NJ', regex=False)
        df['patientclassdesc'] = df["patientclassdesc"].str.replace('outpatient', 'Outpatient', regex=False)

3) Dropped all the duplicate entries in the merged csv
4) Dropped the following columns 'Payer', 'financialClassName', 'payerDescription', 'reimbursement'
5) Renamed 'countryCode' to 'CountyCode'.