sqlcmd -S localhost -E -d Aliart -Q "EXEC sp_rename 'v8users', 'v8users_old'"
