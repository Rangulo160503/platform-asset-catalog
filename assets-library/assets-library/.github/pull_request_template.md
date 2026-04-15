# Documentation
- [ ] Reviewed documentation in [README.md](README.md) and [wiki](https://idtjira.atlassian.net/wiki/spaces/DSD/pages/549093913/Assets+Inventory)

# CODEOWNERS
- [ ] [CODEOWNERS](CODEOWNERS) file includes entry for `<asset_name>.yaml`

# New Asset

### Naming
- [ ] Best Practice: Keep new Asset name max of 9 characters. Asset name is used for resource naming 
and AWS has max char limits for various resources

### Template
- [ ] Best Practice: Use example in [README.md](README.md) as a template for new `<asset_name>.yaml`

# Environments

### Dev
- [ ] IDT Sandbox account 312226949769 is for 1.x only. Use IDT Dev 833915412828 for 2.x

### Prod/UAT
Best Practices:
- [ ] set `protected: true`
- [ ] set `allowApplyInParallelWithOtherEnvironments: false` 

### Vault Support
- [ ] Set `vaultSupport: true` if support for Hashicorp Vault is needed in environemnt

# Ticket link
- [ ] https://idtjira.atlassian.net/browse/DEVOPS-XXX

# [Jira-ID] in the commit message
- [ ] Update description and commit message

