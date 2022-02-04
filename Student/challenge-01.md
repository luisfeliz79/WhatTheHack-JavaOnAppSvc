# Challenge 1: Head in the cloud, feet on the ground

[< Previous Challenge](./challenge-00.md) - **[Home](../README.md)** - [Next Challenge >](./challenge-02.md)

## Introduction

The Spring Boot application uses JPA and supports in memory databases, MySQL, and Azure SQL. In this challenge we'll put our database on Azure while the code is running locally. Taking baby steps :)

## Description

Create an AzureSQL Database and make sure that the application (which is still running locally) can connect to it without changing any code.

## Success Criteria

1. Verify the application is working by creating a new owner, a new pet and a new visit
1. Connect to the database through a SQL client (If you do not have a client installed, you can also use the "Query Editor" available from your Azure SQL DB page on the Azure Portal)
1. Verify that the tables include the newly created entities (owner/pet/visit)
1. No files should be modified for this challenge

## Tips

In order to find resources in Azure (existing or to be created) you can use the _Search bar_ in the portal, look for the text bar at the top which you can activate by pressing the keys `G` and `/` at the same time.

[Azure Cloud Shell](https://docs.microsoft.com/en-us/azure/cloud-shell/overview) includes a bunch of various tools.

And note that you can also pass configuration information to Spring Boot through [environment variables](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-external-config).

## Learning Resources

- [Azure SQL Database](https://docs.microsoft.com/en-us/azure/azure-sql/database/sql-database-paas-overview)
- [Azure Cloud Shell](https://docs.microsoft.com/en-us/azure/cloud-shell/overview)
- [Spring Boot and environment variables](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-external-config)

[Next Challenge - Azure App Services &#10084;&#65039; Spring Boot >](./challenge-02.md)
