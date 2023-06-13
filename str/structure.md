# Table: Patient
Description: Stores information about patients.

| Column Name | Type | Description |
| --- | --- | --- |
| patient_id | INT | Unique identifier for the patient. |
| hosp_stay_id | INT | Unique identifier for the hospital stay associated with the patient. |
| icu_stay_id | INT | Unique identifier for the ICU stay associated with the patient. |
| dob | TIMESTAMP | Date of birth of the patient. |
| sex | VARCHAR | Gender of the patient. |

# Table: Diagnosis
Description: Stores diagnosis information associated with patients.

| Column Name | Type | Description |
| --- | --- | --- |
| patient_id | INT | Unique identifier for the patient. |
| hosp_stay_id | INT | Unique identifier for the hospital stay associated with the diagnosis. |
| icu_stay_id | INT | Unique identifier for the ICU stay associated with the diagnosis. |
| diagnosis_timestamp | TIMESTAMP | Date-time of the diagnosis. |
| icd_code | VARCHAR | ICD code associated with the diagnosis. |
| priority_of_diagnosis | NUMERIC | Priority assigned to the diagnosis. |
| diagnosis_type | VARCHAR | Indicates if the diagnosis is current or past. |


# Table: ICD Dictionary

| Column Name | Type | Description |
| --- | --- | --- |
| icd_code | VARCHAR | ICD code. |
| icd_label | VARCHAR | Label or description of the ICD code. |

# Table: Laboratory
Description: Stores laboratory test results associated with ICU stays.

| Column Name | Type | Description |
| --- | --- | --- |
| icu_stay_id | INT | Unique identifier for the ICU stay associated with the laboratory test. |
| test_timestamp | TIMESTAMP | Date-time of the laboratory test. |
| lab_code | NUMERIC | Code of the laboratory test. |
| test_result | TEXT | Result of the laboratory test. |

# Table: Laboratory Dictionary

| Column Name | Type | Description |
| --- | --- | --- |
| lab_code | NUMERIC | Lab code. |
| lab_label | VARCHAR | Label or description of the lab code. |

# Table: Microbiology
Description: Stores microbiology results associated with ICU stays.

| Column Name | Type | Description |
| --- | --- | --- |
| icu_stay_id | INT | Unique identifier for the ICU stay associated with the microbiology test. |
| test_timestamp | TIMESTAMP | Date-time of the microbiology test. |
| microb_code | NUMERIC |  Code of the microbiology test. |
| test_result | TEXT | Result of the microbiology test. |

# Table: Microbiology Dictionary

| Column Name | Type | Description |
| --- | --- | --- |
| microb_code | NUMERIC | Microbiology code. |
| microb_label | VARCHAR | Label or description of the microbiology code. |

# Table: Medication
Description: Stores information about prescribed or administered medications during ICU stays.

| Column Name | Type | Description |
| --- | --- | --- |
| icu_stay_id | INT | Unique identifier for the ICU stay associated with the medication. |
| commercial_name_code | NUMERIC | Code of the prescribed/administered medication's comercial name. |
| medication_dose | NUMERIC | Dose of the medication. |
| medication_units | CHAR | Units of the medication dose. |
| prescription_timestamp | TIMESTAMP | Date-time of the medication prescription. |
| treatment_start_date | DATE | Start date of the medication treatment. |
| treatment_end_date | DATE | End date of the medication treatment. |
| treatment_dosage_frequency | TEXT | Dosage/frequency of the medication treatment. |

# Table: Medication Dictionary

| Column Name | Type | Description |
| --- | --- | --- |
| commercial_name_code | NUMERIC | Code of the prescribed/administered medication's comercial name. |
| commercial_name_label | VARCHAR | Label or description of the microbiology code. |
| active_ingredient_label | VARCHAR | Label of the prescribed/administered medication's active ingredient. |

# Table: Vital Sign
Description: Stores vital sign measurements during ICU stays.

| Column Name | Type | Description |
| --- | --- | --- |
| icu_stay_id | INT | Unique identifier for the ICU stay associated with the vital sign measurement. |
| vital_sign_code | NUMERIC | Code of the vital sign measurement. |
| vital_sign_value | NUMERIC | Value of the vital sign measurement. |
| vital_sign_units | CHAR | Units of the vital sign measurement. |
| measurement_timestamp | TIMESTAMP | Date-time of the vital sign measurement. |

# Table: Vital Sign Dictionary

| Column Name | Type | Description |
| --- | --- | --- |
| vital_sign_code | NUMERIC | Code of the vital sign measurement. |
| vital_sign_label | VARCHAR | Label or description of the vital sign code. |

# Table: Hospital
Description: Stores information about hospitals.

| Column Name | Type | Description |
| --- | --- | --- |
| hospital_id | INT | Unique identifier for the hospital. |
| hospital_name | TEXT | Name of the hospital. |
| hospital_location | TEXT | Location of the hospital. |
| hospital_type | VARCHAR | Type or category of the hospital. |

# Table: Hospital Stay
Description: Stores information about hospital stays.

| Column Name | Type | Description |
| --- | --- | --- |
| patient_id | INT | Unique identifier for the patient associated with the hospital stay. |
| hosp_stay_id | INT | Unique identifier for the hospital stay. |
| admission_timestamp | TIMESTAMP | Date-time of hospital admission. |
| discharge_timestamp | TIMESTAMP | Date-time of hospital discharge. |
| admission_reason | TEXT | Reason for hospital admission. |

# Table: ICU Stay
Description: Stores information about ICU stays.

| Column Name | Type | Description |
| --- | --- | --- |
| patient_id | INT | Unique identifier for the patient associated with the ICU stay. |
| icu_stay_id | INT | Unique identifier for the ICU stay. |
| admission_timestamp | TIMESTAMP | Date-time of ICU admission. |
| discharge_timestamp | TIMESTAMP | Date-time of ICU discharge. |
| admission_reason | TEXT | Reason for ICU admission. |

# Table: Procedures
Description: Stores information about procedures performed during ICU stays.

| Column Name | Type | Description |
| --- | --- | --- |
| icu_stay_id | INT | Unique identifier for the ICU stay associated with the procedure. |
| performed_procedure | TEXT | Description of the performed procedure. |
| procedure_timestamp | TIMESTAMP | Date-time of the procedure. |

# Table: Clinical Progress Notes
Description: Stores clinical progress notes during ICU stays.

| Column Name | Type | Description |
| --- | --- | --- |
| icu_stay_code | INT | Unique identifier for the ICU stay associated with the clinical progress note. |
| note_type | VARCHAR | Type or category of the clinical progress note. |
| note_timestamp | TIMESTAMP | Date-time of the clinical progress note. |
| clinical_summaries | TEXT | Summary of the clinical progress note. |
