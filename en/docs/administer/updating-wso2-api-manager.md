# Updating WSO2 API Manager

WSO2 introduces [WSO2 Updates](https://updates.docs.wso2.com/en/latest/) , which is a command-line utility that allows you to get the latest updates that are available for a particular product release. These updates include the latest bug fixes and security fixes that are released by WSO2 after a particular product version is released. Therefore, you do not need to wait and upgrade to the next product release to get these bug fixes.

##WSO2 Updates 2.0
The WSO2 updates 2.0 tool allows you to update your currently used product by fetching updates from the server. While you should manually merge the updated configuration files or use a tool like Puppet, you can store backups with the custom configurations in your system, in case you have to restore later.

For more information, see [Using WSO2 Updates 2.0](https://updates.docs.wso2.com/en/latest/updates/update-tool/)

!!! warning
    
    !!! tip
        Before you discard the old API Manager instance,
        
        You must take a backup of the `<API-M_HOME>/repository/data` directory and copy it to the API Manager binary pack in the `<API-M_HOME>/repository/data` directory that is updated.
        
    
    **Persisting WSO2CarbonDB**
    
    To avoid conflicts that can be occurred in the update process, it is recommended to persist the local H2 databases as well.
    
    !!! tip
        Before you discard the old API Manager instance,
        
        Take a backup of `<API-M_HOME>/repository/database/WSO2CARBON_DB.h2.db` and replace it to the API Manager binary pack in the `<API-M_HOME>/repository/database` directory that is updated.
        
        If you are using the existing local H2 database for WSO2MetricsDB as well,
        
        Take a backup of `<API-M_HOME>/repository/database/WSO2METRICS_DB.h2.db` and replace it to the API Manager binary pack in the `<API-M_HOME>/repository/database` directory that is updated.
        
    
    For more information on run time and configuration artifact directories of API Manager refer [Common Runtime and Configuration Artifacts]({{base_path}}/administer/product-configurations/common-runtime-and-configuration-artifacts/) .
