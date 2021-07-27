# Movies-DBMS
Movies and Shows Database Management System
Design a database consisting of information about Movies and TV Shows. Database should have information about actors, directors, songs, release date, production, genre, etc. It should also have information about where to watch specific movies.
  
## ERD
To view the ER Diagram open the DBMS_ERD.pdf file


## Relational Schema
To view the Relational Schema, open the Relational_Schema.pdf file

## Key Assumptions while designing the DBMS
• Movies and TV shows have a ISA relationship with “show”. Here, the generalisation is disjoint and complete, meaning each show is either a movie or a tv show. Each show has an ID which is unique and that’s why acts as a primary key.

• Each show can have many genres and each genre contain many shows. Hence, there is a many-to-many relationship here.

• A show can be available on multiple platforms and each platform contain multiple shows. Hence many-to-many relationship. Similarly, An actor can act in many movies and each show can have many actors.

• A show is produced by a company or a group of companies and a company can produce mutliple shows. Hence, many-to-many relationship.

• Here, we are assuming that award is not a weak entity and have a
primary key award_id and it follows many-to-many relationship with
show

• Show can have reviews by multiple users and an user can review
multiple shows.

• Here, song is made to be a weak entity set because it depends on
movies. Assumption is no two movies have same songs and songs entity
set contain only those songs which are in movies.

• TV shows can have multiple episodes and episodes depend on tv show,
so the has_ep is an identifying relationship and episode is a weak entity
set.

• A director can direct a movie as well an episode. Also, no movie or tv
show has more than 1 director so it’s a one-to-many relationship in both
cases.

• actor_id and director_id is the person ID (some id to uniquely identify
every person like social id). Phone attribute of company is a multivalued
attribute and actor_name is a composite attribute. In case of actor and
director entity set, age is a derived attribute and can be derived from
DOB.
SELECT trunc((sysdate – DOB)/365.25) as AGE FROM
ACTOR/DIRECTOR;

• Company’s primary key is c_name (Company name) which is a registered
trademark. Hence, it is unique.

• Height is in metres, salary and prize in dollars and box_office_collection
in million dollars.

• Rating is an integer 1-10 inclusive.


### To view the full report view the DBMS_PROJECT.pdf file
