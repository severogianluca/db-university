1. Selezionare tutti gli studenti nati nel 1990 (160)

SELECT * 
FROM `db-university`.students
WHERE YEAR(date_of_birth) = 1990;


2. Selezionare tutti i corsi che valgono più di 10 crediti (479)

SELECT * FROM `db-university`.courses
where cfu > 10;

3. Selezionare tutti gli studenti che hanno più di 30 anni

SELECT *
FROM `db-university`.students
WHERE TIMESTAMPDIFF(YEAR, date_of_birth, CURDATE()) > 30;


4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
laurea (286)

SELECT * FROM `db-university`.courses
where period = 'I semestre'
and year = 1;

5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020 (21)

SELECT * FROM `db-university`.exams
where date = '2020-06-20'
and hour > '14:00:00';

6. Selezionare tutti i corsi di laurea magistrale (38)

SELECT * FROM `db-university`.degrees
where level = 'magistrale';

7. Da quanti dipartimenti è composta l'università? (12)

SELECT * FROM `db-university`.departments;


8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)

SELECT * FROM `db-university`.teachers
where phone is null;