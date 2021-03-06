### CATERR: (beta)
'For all your event-staffing needs.'

-Make option for admin to compile list of staff who: are approved to work for particular caterer, are available, have certain pieces of attire, have certifications, etc.
-enable admin to compile list of emails for people who do/not have completed paperwork
-add training feature.
-work more

### BACKEND:
Setting up the database and backend server.

	1. Install postgreSQL using homebrew:
			$ brew install postgresql

	2. Install postgreSQL node-module using NPM:
			$ npm install --save pg

	3. Launch postgreSQL using homebrew:
			$ brew services start postgresql

	4. In project directory, create new db:
			$ createdb *INSERT_DB_NAME*

	5. Connect model tables (schema.sql) db:
			$ psql -d *INSERT_DB_NAME* < *INSERT_SCHEMA.SQL_PATH*

	6. Access database:
			$ psql -d *INSERT_DB_NAME*

For example, once postgreSQL is installed and launched, type:
```
	* `createdb chat`
	* `psql -d chat < backend/database/schema.sql`
	* `psql -d chat`
	* `insert into users (user_name) values ('Alex');`
	* `insert into questions (user_id, question_text, when_asked, is_answered) values (1, 'this is the questions text', '1999-01-08 04:05:06', false);`
```

Queries for accessing the SQL database directly.

	Query examples:
		CREATE:
			$ insert into *INSERT_TABLE* (*INSERT_COLUMN_1*, *INSERT_COLUMN_2*) values ('*INSERT_VALUE_1*', '*INSERT_VALUE_2*');
			'1999-01-08 04:05:06' (format timestamp like this)
		READ:
			$ select * from *INSERT_TABLE*;
			$ select *INSERT_VALUE from *INSERT_TABLE*;
			$ select *INSERT_COLUMN_1*, *INSERT_COLUMN_2* from *INSERT_TABLE* where *INSERT_COLUMN_1*='*INSERT_VALUE_1*';
		UPDATE:
			$ update *INSERT_TABLE* set *INSERT_COLUMN_1*='*INSERT_VALUE_1*' where *INSERT_VALUE_2*='*INSERT_COLUMN_2*';
		DELETE:
			$ delete from *INSERT_TABLE* where *INSERT_COLUMN_1*='*INSERT_VALUE_1*';