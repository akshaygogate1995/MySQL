# MySQL

create database akshay;   #Creates database

drop database akshay;   #drops database

/*     */     - To comment multiple lines

windows it is in case_sensitive

# MySQL create table without constraints

use akshaydb;

create table books(
   BookId int,
   Title varchar(25),
   Author varchar(25),
   Genre varchar(25),
   PublicationYear int
);

select * from books;


# Insert data into table

insert into books(BookId,Title,Author,Genre,PublicationYear)
values
(1,"Twilight","AG","Action",2021),
(2,"Harry Potter","Max","Sci-Fi",2019);

select * from books;

drop table books;

drop database akshay;

