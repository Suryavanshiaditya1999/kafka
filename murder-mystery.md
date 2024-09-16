Based on the given information first let's see crime report of `SQL CITY`

```
SELECT * FROM crime_scene_report 
WHERE type = 'murder' 
AND city = 'SQL City';
```
![image](https://github.com/user-attachments/assets/5f568eb1-beed-40c4-97cc-49fedec6bb29)



Now based on the date and time of murder we have concluded that one witness lives in at the last house on "Northwestern Dr". The second witness, named Annabel, lives somewhere on "Franklin Ave".

- TO know more about witnesses
  ```
  SElECT * from person
  WHERE address_street_name="Northwestern Dr"
  ORDER BY address_number DESC LIMIT 1
  ```

  ```
  SElECT * from person
  WHERE address_street_name="Franklin Ave"
  AND name LIKE "Annabel%"
  ```

![image](https://github.com/user-attachments/assets/425f5256-2e26-4cf3-a21b-af130f1ddc0c)



to find their interviews

```
SELECT person.name, interview.transcript
FROM person JOIN interview
ON person.id = interview.person_id
WHERE person.id = 14887 OR person.id = 16371;
```


- Now based on the witness record
  ```
  SELECT * from get_fit_now_member
  WHERE membership_status="gold"
  AND id LIKE "48Z%"
  ```

 ![image](https://github.com/user-attachments/assets/9765649f-b0a4-4eac-bd0a-598488a32296)


 - Furthermore to identigy real culprit

    ```
    SELECT person.name, interview.transcript
    FROM person JOIN interview
    ON person.id = interview.person_id
    WHERE person.id = 67318 
    ```

   ![image](https://github.com/user-attachments/assets/190ddff0-595b-4dcb-a754-2725a6b23154)


-
    ```
    SELECT * FROM drivers_license
    WHERE car_make = 'Tesla'
    AND car_model = 'Model S'
    AND hair_color = 'red'
    AND height <= 67;
    ```
- ![image](https://github.com/user-attachments/assets/9aa4582e-a5a4-42ce-b138-9969e0e9419a)

  


