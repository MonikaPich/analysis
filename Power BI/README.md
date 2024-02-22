# My Power BI training

### Raport no 1 - my first power BI report

* [my first power BI report](https://drive.google.com/file/d/1I7d-ujXMYfU0fnv8lx43YrdTAZb3Z9J8/view?usp=sharing)

I present my first report created using Power BI.
I started compiling the data by pre-filtering and downloading it from a database (Database source: https://github.com/datacharmer/test_db).  I performed the following queries:
* I combined the employee data (titles) with the position they cover
SQL request: 
```sql
SELECT titles.emp_no, titles.title, titles.from_date, titles.to_date, CONCAT(employees.first_name, " ", employees.last_name) AS employee, employees.birth_date, employees.gender FROM `titles` LEFT JOIN employees ON titles.emp_no = employees.emp_no;
```
* I retrieved the data from the salaries, dept_emp and dept_menager tables.
Once the data had been imported from the CSV files into power BI, I transformed the data by creating a new sum salary table merging the salaries, titles and dept_emp tables.
I also used measures with aggregating functions to produce the report and built a hierarchy of departments - title employees.


