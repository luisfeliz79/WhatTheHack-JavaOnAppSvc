# Challenge 3:  Keep your secrets safe

[< Previous Challenge](./solution-02.md) - **[Home](./README.md)** - [Next Challenge >](./solution-04.md)

## Notes & Guidance

- There's a number of different methods to deploy a Key Vault instance, but for the purpose of this hack you can create it from the Azure portal.

- In case that things go catastrophically wrong and you need to recreate the Key Vault, you might  run into errors, as by default Key Vaults are soft-deleted. You'd need to purge it first.

    ```shell
    az keyvault purge -n $KEYVAULT
    ```

- It's possible to verify the settings from the Configuration section of the portal, but you could also verify it through the CLI, all MYSQL settings should have the `@Microsoft.KeyVault(SecretUri=...)` structure

    ```shell
    az webapp config appsettings list -g $RG -n $WEBAPP 
    ```
