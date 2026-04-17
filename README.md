
DOS
net stop "1C:Enterprise 8.3 Server Agent"
net stop MSSQLSERVER


DOS
net start MSSQLSERVER /m"SQLCMD"

DOS
sqlcmd -S localhost -E -d Aliart -Q "DROP TABLE v8users"

DOS
sqlcmd -S localhost -E -d Aliart -Q "EXEC sp_rename 'v8users_old', 'v8users'"


DOS
sqlcmd -S localhost -E -d Aliart -Q "DELETE FROM v8users"
