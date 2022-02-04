# Challenge 1: Head in the cloud, feet on the ground

[< Previous Challenge](./solution-00.md) - **[Home](./README.md)** - [Next Challenge >](./solution-02.md)

## Notes & Guidance

- There's a number of different methods to deploy an Azure SQL database, you can create it from the Azure Portal (Click on "Create a resource" and search for "Azure SQL"), Azure CLI, PowerShell, Terraform, bicep templates etc.

- Once the database is up and running, you can connect to it from your application by providing the configuration parameters AZSQL_USER, AZSQL_PASS, AZSQL_URL. Easiest method is to define those in the current shell as environment variables, but alternatively you could pass them to the `mvn` command as well. And don't forget to turn on the `azuresql` profile.

    ```shell
   	mvn spring-boot:run -Dspring-boot.run.jvmArguments="-Dspring.profiles.active=azuresql -DAZSQL_URL=jdbc:sqlserver://<your_dbservername>.database.windows.net:1433;database=<your_dbname> -DAZSQL_USER=<your_db_admin_user> -DAZSQL_PASS=<your_db_password>"
    ```