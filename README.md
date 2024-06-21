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
This script will configure the following
- [ ] Entra Groups
    - [ ] Assigned
        - [ ] License Assignment
        - [ ] Intune configuration targeting
        - [ ] Windows 365 targeting
        - [ ] Azure Virtual Desktop targeting
    - [ ] Dynamic
        - [ ] Windows 365 devices
- [ ] Intune policies
    - [ ] 
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

# Final Thoughts
If you find this helpful, please star the project.

If you have something to contribute, please submit a pull request.