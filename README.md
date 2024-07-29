# LibraryManagementSystem-Gui-Java

**For Data Base Connection**<br>
    First Add your mysql connector jar file path

Now copy and paste these commands as it is in mysql and execute all:
```
create database LMS;
use LMS;
create table auth (
	id int auto_increment,
	username varchar(77) ,
	email varchar(88) unique,
    password varchar(111),
    phone varchar(22),
    joiningDate varchar(66),
    primary key(id)
);

create table books (
	id int auto_increment,
	title varchar(111) ,
	author varchar(111) ,
    genre varchar(111),
    status varchar(30),
    primary key(id)
);

create table members (
	id int auto_increment,
	name varchar(77) ,
	email varchar(88) unique,
    phone varchar(22),
    noOfBorrowedBooks int,
    membershipDate varchar(66),
    primary key(id)
);

create table borrowbooks (
	id int auto_increment,
    bookId int,
    bookTitle  varchar(99),
	memberId int ,
	memberName  varchar(99),
    borrowDate varchar(22),
    primary key(id)
);

INSERT INTO members (name, email, phone,noOfBorrowedBooks, membershipDate) VALUES
('Ayesha Khan', 'ayesha.khan@gmail.com', '+923001234567','0', '15-01-2024'),
('Ahmed Ali', 'ahmed.ali@gmail.com', '+923112345678','0', '20-02-2024'),
('Fatima Noor', 'fatima.noor@gmail.com', '+923223456789','0', '10-03-2024'),
('Usman Malik',  'usman.malik@gmail.com', '+923334567890','0', '05-04-2024'),
('Zara Qureshi',  'zara.qureshi@gmail.com', '+923445678901','0', '18-05-2024'),
('Hassan Javed', 'hassan.javed@gmail.com', '+923556789012','0', '22-06-2024'),
('Mariam Siddiqui' ,'mariam.siddiqui@gmail.com', '+923667890123','0', '15-07-2024'),
('Bilal Ahmed', 'bilal.ahmed@gmail.com', '+923778901234','0', '30-08-2024'),
('Nida Shaikh', 'nida.shaikh@gmail.com', '+923889012345', '0','05-09-2024'),
('Rizwan Khan', 'rizwan.khan@gmail.com', '+923990123456', '0','12-10-2024');

INSERT INTO books (title, author, genre, status) VALUES
('Clean Code', 'Robert C. Martin', 'Programming', 'Available'),
('The Pragmatic Programmer', 'Andrew Hunt and David Thomas', 'Programming', 'Available'),
('Effective Java', 'Joshua Bloch', 'Programming', 'Available'),
('Design Patterns', 'Gamma et al.', 'Programming', 'Available'),
('Theory of Computation', 'Michael Sipser', 'Computer Science', 'Available'),
('Java Complete Reference', 'Herbert Schildt', 'Programming', 'Available'),
('Python Crash Course', 'Eric Matthes', 'Programming', 'Available'),
('Art of Computer Programming', 'Donald E. Knuth', 'Computer Science', 'Available'),
('You Don\'t Know JS', 'Kyle Simpson', 'Programming', 'Available'),
('Algorithms Unlocked', 'Thomas H. Cormen', 'Algorithms', 'Available');

```
