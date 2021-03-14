# aspnetcore5-with-postgres-identity-serilog-elasticsearch

A base ASP .Net 5 MVC project (to use as a basic template/boilerplate) set up with PostgreSql, a registration and login system using Identity and full logging using ILogger with Serilog and Elasticsearch

The purpose of this project is to provide a quick and easy starting point for new ASP .Net 5 MVC projects that already has the following features:

- Uses PostgreSql instead of MS SQL Server
- A working registration and login system with gmail to send emails
- Logging to daily rolling text documents (cleared weekly) using ILogger
- Logging to Elasticsearch using ILogger

There is no real commit history, as I put the work in to make this for another project, then dumped the files here in one commit as I realised it could be useful to save other people time setting up the same stuff.
