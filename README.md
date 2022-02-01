# SIMPLE CODE TO INSERT DATA TO TABLE
### Use of `csv_to_db` :
- This reads the data from `data.csv` file in the root folder.
- The first row is the column names to be used.
- Make sure the table and database exists.
### Config in `csv_to_db`:
```
{
    "table":"<table>",
    "host":"<host>",
    "user":"<user>",
    "password":"<password>",
    "database":"<db name>",
}
```

### Use of `db_to_db` :
- This reads the data from the first database (db_one).
- Then combines the extra rows (if needed) to be inserted in second database (db_two)
- Finally, inserts the data into second database (db_two).
- The `extra_from_csv` key in config is `True` then it will read extra data from csv whose file name will be stored in key `csv_file_name`.
- The first row is the column names to be used.
- Make sure the table and database exists.
### Config in `db_to_db`:
```
{
    "db_one_host":"<host>",
    "db_one_user":"<user>",
    "db_one_pass":"<password>",
    "db_one_name":"<db name>",
    "db_one_tble":"<table name>",
    "db_one_cols":["col1","col2",....],
    "db_two_host":"<host>",
    "db_two_user":"<user>",
    "db_two_pass":"<password>",
    "db_two_name":"<db name>",
    "db_two_tble":"<table>",
    "db_two_cols":["col1","col2","col3",....],
    "extra_from_csv":"<Boolean>",
    "csv_file_name":"<file_name>.csv"
}
```
