# verou-3-sql-introduction-derylan

* Solution per step

* Get all data from the groups
SELECT * from `groups`;

* Get the name and email of the first learner, and alias the name to learner_name
SELECT name AS learner_name, email from `learner` WHERE id=1;

* Update the start date of the first_group (make it two months later)
UPDATE `groups` SET start_date = '2022-05-15' WHERE id=1;

* Introduce a new field status which can contain a long text indicating the reason for postponing (bonus points if it's a creative one)
ALTER TABLE `groups` ADD COLUMN status text AFTER start_date; 
UPDATE `groups` SET status = 'Class postponed as BeCode decided to give Verou-3 group a free trip to the Maldives' WHERE id=1;

* Delete someone from the learners table
DELETE FROM learner WHERE name = 'Sara';