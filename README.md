# Experiment-
AIM :- Create Author and books using the DDL Commands insert sample records into the authors and the books table, Retrieve books title along the author information using the inner join


following is the main code of the AIM above and also find the main code on a saperate file 



create table Authors( author_id INT Primary Key, name VARCHAR(50), country VARCHAR(50));
create table Books(book_id INT Primary Key, title VARCHAR(100), author_id INT, Foreign key (author_id) references Authors(author_id));

insert into Authors(author_id, name, country) values (1, 'George Orwell', 'UK'), (2, 'Haruki Murakami', 'Japan'), (3, 'Jane Austen', 'UK');

insert into Books(book_id, title, author_id) Values(101, '1984', 1), (102, 'Animal Farm', 1), (103, 'Norwegian Wood', 2), (104, 'Pride and Prejudice', 3), (105, 'Emma', 3);

select B.title AS Book_Title, A.name AS Author_Name, A.country AS Author_Country FROM Books B INNER JOIN Authors A ON B.author_id = A.author_id;


