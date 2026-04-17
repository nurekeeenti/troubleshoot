taskkill /F /IM 1cv8.exe
taskkill /F /IM 1cv8s.exe
net stop "1C:Enterprise 8.3 Server Agent"

sqlcmd -S localhost -E -d Aliart -Q "DELETE FROM v8users"


net start MSSQLSERVER
