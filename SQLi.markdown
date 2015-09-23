#Tactical Fuzzing - SQLi

##SQL Injection
Core Idea: Does the page look like it might need to call on stored data?

There exist some SQLi polyglots, i.e (Mathias Karlsson);

``
SLEEP(1) /*‘ or SLEEP(1) or ‘“ or SLEEP(1) or “*/
``

Works in single quote context, works in double quote context, works in “straight into query” context!

You can also leverage the large database of fuzzlists from Seclists (https://github.com/danielmiessler/SecLists)

##￼￼SQL Injection Observations
Blind is predominant, Error based is highly unlikely.

``
‘%2Bbenchmark(3200,SHA1(1))%2B’
``


``
‘+BENCHMARK(40000000,SHA1(1337))+’
``

SQLMap is king!
- Use -l to parse a Burp log file.
- Use Tamper Scripts for blacklists.
- SQLiPy Burp plugin works well to instrument SQLmap quickly.
Lots of injection in web services!

##￼Best SQL injection resources

- MySQL:
  - [PentestMonkey's mySQL injection cheat sheet] (http://pentestmonkey.net/cheat-sheet/sql-injection/mysql-sql-injection-cheat-sheet)
  - [Reiners mySQL injection Filter Evasion Cheatsheet] (https://websec.wordpress.com/2010/12/04/sqli-filter-evasion-cheat-sheet-mysql/)
- MSQQL:
  - [EvilSQL's Error/Union/Blind MSSQL Cheatsheet] (http://evilsql.com/main/page2.php)
  - [PentestMonkey's MSSQL SQLi injection Cheat Sheet] (http://pentestmonkey.net/cheat-sheet/sql-injection/mssql-sql-injection-cheat-sheet)
- ORACLE:
  - [PentestMonkey's Oracle SQLi Cheatsheet] (http://pentestmonkey.net/cheat-sheet/sql-injection/oracle-sql-injection-cheat-sheet)
- POSTGRESQL:
  - [PentestMonkey's Postgres SQLi Cheatsheet] (http://pentestmonkey.net/cheat-sheet/sql-injection/postgres-sql-injection-cheat-sheet)
- Others
  - [Access SQLi Cheatsheet] (http://nibblesec.org/files/MSAccessSQLi/MSAccessSQLi.html)
  - [PentestMonkey's Ingres SQL Injection Cheat Sheet] (http://pentestmonkey.net/cheat-sheet/sql-injection/ingres-sql-injection-cheat-sheet)
  - [Pentestmonkey's DB2 SQL Injection Cheat Sheet] (http://pentestmonkey.net/cheat-sheet/sql-injection/db2-sql-injection-cheat-sheet)
  - [Pentestmonkey's Informix SQL Injection Cheat Sheet] (http://pentestmonkey.net/cheat-sheet/sql-injection/informix-sql-injection-cheat-sheet)
  - [SQLite3 Injection Cheat sheet] (https://sites.google.com/site/0x7674/home/sqlite3injectioncheatsheet)
  - [Ruby on Rails (Active Record) SQL Injection Guide] (http://rails-sqli.org/)
