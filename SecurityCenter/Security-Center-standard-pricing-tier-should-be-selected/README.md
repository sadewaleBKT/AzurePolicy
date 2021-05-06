# Security Center standard pricing tier should be selected


## Try on Portal

[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#blade/Microsoft_Azure_Policy/CreatePolicyDefinitionBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2FsadewaleBKT%2FAzurePolicy%2Fmaster%2FSecurityCenter%2FSecurity%20Center%20standard%20pricing%20tier%20should%20be%20selected%2Fazurepolicy.json)
[![Deploy to Azure Gov](https://docs.microsoft.com/azure/governance/policy/media/deploy/deployGovbutton.png)](https://portal.azure.us/?#blade/Microsoft_Azure_Policy/CreatePolicyDefinitionBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2FsadewaleBKT%2FAzurePolicy%2Fmaster%2FSecurityCenter%2FSecurity%20Center%20standard%20pricing%20tier%20should%20be%20selected%2Fazurepolicy.json)

## Try with PowerShell

````powershell
# Create the Policy Definition
$definition = New-AzPolicyDefinition -Name "disallow-keyvault-access-policies" -DisplayName "Audit when a given service principal is assigned to the Key Vault data plane" -description "Audit when a specified AAD object is granted any permissions to secrets, certs, or keys stored in a Key Vault through data plane access policies." -Policy '<>' -Mode All

# Show definition
$definition

# Create the Policy Assignment
$assignment = New-AzPolicyAssignment -Name "disallow-keyvault-access-policies" -Scope <scope> -PolicyDefinition $definition -aadObjectId f8efb48a-34e8-4ee6-b31f-133a05248f9c

# Show assignment
$assignment
````

## Try with CLI

````cli
# Create the Policy Definition
az policy definition create --name 'disallow-keyvault-access-policies' --display-name 'Audit when a given service principal is assigned to the Key Vault data plane' --description 'Audit when a specified AAD object is granted any permissions to secrets, certs, or keys stored in a Key Vault through data plane access policies.' --rules '<>' --mode All

# Create the Policy Assignment
az policy assignment create --name 'disallow-keyvault-access-policies' --scope <scope> --policy 'disallow-keyvault-access-policies' --params "{'aadObjectId': {'value': 'f8efb48a-34e8-4ee6-b31f-133a05248f9c'}}"
````
