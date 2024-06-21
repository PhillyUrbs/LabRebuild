# LabRebuild
This project is designed to provide those in the Cloud Endpoint Technology Specialist (CETS) role at Microsoft an easy way to rebuild their lab/demo environment. Aside from initial tenant creation and license acquisition, this set of configuration scripts is designed to be completely self sustaining. CETS are responsible for the technologies below. As such, each will be configured in a basic capacity.

*Technologies*
- Azure Virtual Desktop
- Entra ID P1
- Intune P1
- Intune Suite
- Windows 365

# Requirements
## License Requirements
At least one of each of the following licenses are required 
- Intune Suite
- Microsoft 365 E5
- Microsoft Teams Enterprise
- Windows 365 Enterprise (any configuration)
- Windows 365 Frontline (any configuration)

# Final Configuration
In the default config, this script will configure the following
- [ ] Entra Groups
    - [ ] Assigned
        - [ ] License Assignment
        - [ ] Intune configuration targeting
        - [ ] Windows 365 targeting
        - [ ] Azure Virtual Desktop targeting
    - [ ] Dynamic
        - [ ] Windows 365 devices
- [ ] Intune
    - [ ] Applications
        - [ ] Enterprise App Catalog Apps
            - [ ] 7-Zip
            - [ ] Citrix Receiver
            - [ ] Google Chrome for Business
            - [ ] IrfanView
            - [ ] Microsoft PowerTowys
            - [ ] Microsoft Visual C++ 2008 Redistributable
            - [ ] Microsoft Visual C++ 2015-2022 Redistributable
            - [ ] Microsoft Visual Studio Code
            - [ ] Mozilla Firefox
            - [ ] Remote Help
        - [ ] Microsoft Store apps (new) (as both system and user)
            - [ ] Company Portal
            - [ ] Windows App
    - [ ] Policies
        - [ ] Cert - Device (from Cloud PKI)
        - [ ] Cert - User (from Cloud PKI)
    - [ ] Cloud PKI
        - [ ] Root CA
        - [ ] Issuing CA
    - [ ] Remote Help
    - [ ] Windows Autopatch
- [ ] Windows 365 policies
    - [ ] Enterprise Provisioning Policy
    - [ ] Frontline Provisioning Policy
    - [ ] User Policies

# Recommended Manual Steps
Assuming you have created your tenant from the Compliance template in CDX, you'll want to do the following before running any of the configuration scripts.
- Unassign the following licenses from all users except your admin@[yourtenantname].onmicrosoft.com account.
    - Intune Suite
    - Microsoft 365 E5 (no Teams)
    - Microsoft Teams Enterprise
    - Office 365 E3

# Some Thoughts
Part of the goal of this project is to help me learn how to use the Microsoft Graph. Ideally all interaction with tenants and subscriptions will be done with graph calls.

If you find this helpful, please star the project.

If you have something to contribute, please submit a pull request.

# References
- https://github.com/microsoftgraph/powershell-intune-samples

also a test