# PostgreSQL-lesson-1
PostgreSQL Lesson 1
```sql
CREAT DATABASE testdb


CREATE TABLE publisher
(
	publisher_id integer PRIMARY KEY,
	org_name varchar(130) NOT NULL,
	address text NOT NULL,
	
);

CREATE TABLE book
(
	book_id integer PRIMARY KEY,
	title text NOT NULL,
	isbn varchar(32) NOT NULL
)

DROP TABLE publisher;
DROP TABLE book;

INSERT INTO book
VALUES
(1,'The Diary of a Young Girl','0123403430430'),
(2,'Pride and Prejudice','93232304204'),
(3,'To Kill a Mockingbird','3424254456'),
(4,'The Book of Gutsy Women','12344532');


INSERT INTO publisher
VALUES
(1,'Evereman''s Library','NY'),
(2,'Oxford University Press', 'NY'),
(3,'Grand Central Publishing','Washington'),
(4,'Simon & Schister','Chicago');


SELECT pg_terminate_backend(pg_stat_activity.pid)
FROM pg_stat_activity
WHERE pg_stat_activity.datname = 'testdb'
  AND pid <> pg_backend_pid()


DROP DATABASE testdb

"test string"
```


