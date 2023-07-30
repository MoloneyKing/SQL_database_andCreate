# SQL_database_andCreate
SQL – Database and Create; SQL is easy, see!

- Create the Soccer database
CREATE DATABASE Soccer;
-- Switch to the Soccer database
USE Soccer;
-- Create the Clubs table
CREATE TABLE Clubs (
club_name varchar(20),
stadium_name varchar(20),
ground_capacity int,
club_manager varchar(30),
year_founded date
);
-- Insert records into the Clubs table
INSERT INTO Clubs (club_name, stadium_name, ground_capacity, club_manager,
year_founded)
VALUES ('Manchester Utd', 'Old Trafford', 74140, 'Ole Gunnar Solskjaer', '1878-01-01'),
('Liverpool FC', 'Anfield', 53394, 'Jurgen Klopp', '1892-06-03');
-- Update the ground capacity for 'Liverpool FC'
UPDATE Clubs
SET ground_capacity = 75000
WHERE club_name = 'Liverpool FC';
-- Update the club manager for 'Manchester Utd'
UPDATE Clubs
SET club_manager = 'Mike Phelan'
WHERE club_name = 'Manchester Utd';
-- Query all records from the Clubs table
SELECT *
FROM Clubs;
-- Delete the record for 'Manchester Utd'
DELETE FROM Clubs
WHERE club_name = 'Manchester Utd'
