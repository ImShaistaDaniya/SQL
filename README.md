DROP table team;

CREATE TABLE TEAM
(
    SI_NO INT AUTO_INCREMENT,
    Name VARCHAR(30) NOT NULL,
    Sub_Group VARCHAR(30) NOT NULL,
    Position VARCHAR(30) NOT NULL,
    PRIMARY KEY(SI_NO)
);
DESCRIBE TEAM;

DROP table details;
 
 CREATE TABLE DETAILS
 (
   SI_NO INT ,
   Name VARCHAR(30) PRIMARY key,
   Projects VARCHAR(30),
   Skills VARCHAR(30)
 );

DESCRIBE DETAILS;

ALTER TABLE TEAM 
 ADD FOREIGN KEY(Name)
 REFERENCES DETAILS(Name)
 ON DELETE SET NULL;
 
  DROP table attendence;

  CREATE TABLE ATTENDENCE(
      Name VARCHAR(30),
      Today DATE   
  );
  DESCRIBE ATTENDENCE;
  
  DROP TABLE TOTAL_ATTENDANCE ;

  CREATE TABLE TOTAL_ATTENDANCE(
   Name VARCHAR(30),
   Attendence INT
  );
  DESCRIBE TOTAL_ATTENDANCE;
  SELECT * FROM `tsig`.`team` LIMIT 1000;
