sqlcmd -S localhost -E -d Aliart -Q "DROP TABLE v8users"
sqlcmd -S localhost -E -d Aliart -Q "EXEC sp_rename 'v8users', 'v8users_old'"

/////////////////// IF ITS WORKING


sqlcmd -S localhost -E -d Aliart -Q "DROP TABLE v8users; EXEC sp_rename 'v8users_old', 'v8users'"
