e17e01=# CREATE TABLE area(
e17e01(# id SERIAL PRIMARY KEY,
e17e01(# name VARCHAR(100)
e17e01(# );
CREATE TABLE
e17e01=# CREATE TABLE workers(
e17e01(# id SERIAL PRIMARY KEY,
e17e01(# name VARCHAR(100)
e17e01(# )
e17e01-# ;
CREATE TABLE


e17e01=# create table salaries(                                                 id SERIAL primary key,                                                          month date,                                                                     worker_id integer references workers(id)                                        )                                                                               ;
CREATE TABLE

                                               ^
e17e01=# alter table workers add column area_id integer;
ALTER TABLE
e17e01=#
e17e01=# alter table workers add constraint fk_areas foreign key (area_id) references area(id);                                                                
ALTER TABLE
e17e01=# \dt
                List of relations
 Schema |   Name   | Type  |        Owner        
--------+----------+-------+---------------------
 public | area     | table | sebastianfuenzalida
 public | salaries | table | sebastianfuenzalida
 public | workers  | table | sebastianfuenzalida
(3 rows)

e17e01=# \d
                     List of relations
 Schema |      Name       |   Type   |        Owner        
--------+-----------------+----------+---------------------
 public | area            | table    | sebastianfuenzalida
 public | area_id_seq     | sequence | sebastianfuenzalida
 public | salaries        | table    | sebastianfuenzalida
 public | salaries_id_seq | sequence | sebastianfuenzalida
 public | workers         | table    | sebastianfuenzalida
 public | workers_id_seq  | sequence | sebastianfuenzalida
(6 rows)


____
