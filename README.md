1. Show all the criteria id along with the country code CD.
![image](https://github.com/KasturiGhosh12/SQLBigQuery-Assignment/assets/154314536/8bda633d-d21b-40c0-bcae-bba91d773c70)
![image](https://github.com/KasturiGhosh12/SQLBigQuery-Assignment/assets/154314536/d2c3a035-70f8-49ed-81c7-8c592067535f)
2. What is the total fare of each taxi company?
  
   ![image](https://github.com/KasturiGhosh12/SQLBigQuery-Assignment/assets/154314536/11ad34be-0ca7-49c5-83f0-e1656e24c3a6)
![image](https://github.com/KasturiGhosh12/SQLBigQuery-Assignment/assets/154314536/d791cf3b-e064-452c-8382-497ace1664b2)
   3. Show location of the various covid vaccination facilities.
      ![image](https://github.com/KasturiGhosh12/SQLBigQuery-Assignment/assets/154314536/08e9421e-8385-4f3c-bb19-9fcc01d86b36)
      ![image](https://github.com/KasturiGhosh12/SQLBigQuery-Assignment/assets/154314536/59b4659d-6b44-4a45-8793-fdc40772139b)
 4. What is the average pressure of the hurricane in each season?
    ![image](https://github.com/KasturiGhosh12/SQLBigQuery-Assignment/assets/154314536/ca43e6c8-7b7c-4489-abbf-366312650e40)
![image](https://github.com/KasturiGhosh12/SQLBigQuery-Assignment/assets/154314536/c0dab51e-4454-4db7-b485-95601908aa34)

5. What are the bed types and and stffing levels for each country?
   
   {SELECT
  b.county_name,
  b.total_hospital_beds,
  b.gen_medical_surgical_adult_beds,
  s.total_personnel_ft,
  s.registered_nurses_ft,
  s.physicians_and_dentists_ft
FROM `bigquery-public-data.covid19_aha.hospital_beds` b
LEFT JOIN `bigquery-public-data.covid19_aha.staffing` s
  ON b.county_fips_code = s.county_fips_code;}

![image](https://github.com/KasturiGhosh12/SQLBigQuery-Assignment/assets/154314536/af9c8f71-fab3-4537-9f9d-a4ad38fe7006)
6. State the drug names with recalls and detiled label information.

   { SELECT
  de.recall_number,
  de.product_description,
  de.reason_for_recall,
  dl.openfda_brand_name,
  dl.openfda_generic_name,
FROM `bigquery-public-data.fda_drug.drug_enforcement` de
LEFT JOIN `bigquery-public-data.fda_drug.drug_label` dl
  ON de.openfda_unii = dl.openfda_unii;}
 
  
 ![image](https://github.com/KasturiGhosh12/SQLBigQuery-Assignment/assets/154314536/b652bae4-3c72-4f7d-94f4-df4207b99239)

