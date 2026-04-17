В CMD: net stop MSSQLSERVER и net stop "1C:Enterprise 8.3 Server Agent".

Потом net start MSSQLSERVER /m"SQLCMD".

И сразу команду на переименование: sqlcmd -S localhost -E -d Aliart -Q "EXEC sp_rename 'v8users', 'v8users_old'"

net start "1C:Enterprise 8.3 Server Agent"

sqlcmd -S localhost -E -d Aliart -Q "DROP TABLE v8users; EXEC sp_rename 'v8users_old', 'v8users'"


sqlcmd -S localhost -E -d Aliart -Q "EXEC sp_rename 'v8users', 'v8users_old'"
