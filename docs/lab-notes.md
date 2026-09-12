# Configure Conditional Access Policy for Admin Device Compliance

## Overview

For this task, I created a Conditional Access policy that requires administrative users to sign in from compliant devices. This helps ensure that privileged accounts can only access administrative resources from devices that meet organizational security requirements.

## Objective

- Create a Conditional Access policy for administrators.
- Require device compliance before access is granted.
- Enable and verify the policy configuration.

## Step 1: Open Conditional Access

I signed in to the Microsoft Entra Admin Center and navigated to **Conditional Access** and created a CA policy for administrator.

![](../Conditional-access-policy-for-administrators.png)

Step 4: Select administrative users and target resources
I selected All Resources (formerly 'All cloud apps') Under Target Resources to ensure admin users satisfy the device compliance requirement whenever they access protected resources. 

![](../select-target-resources.png)


## Step 5: Configure Device Compliance Requirement

Under **Access Controls → Grant**, I configured:

- Grant access
- Require device to be marked as compliant

![](../configure-device-compliance-requirements.png)


## Step 6: Verify Policy Deployment

I confirmed that the policy appeared in the Conditional Access policy list with an enabled status.

![](../verify-policy-deployment.png)


Step 7: Test Policy Enforcement

I tested the policy using Arjun Patel, who was assigned the Cloud Application Administrator role. When attempting to access an administrative resource from a non-compliant device, 
Microsoft Entra blocked access and displayed a compliance requirement message.

![](../test-policy-enforcement.png)

### Conclusion

I successfully configured a Conditional Access policy requiring administrative users to access protected resources from compliant devices. Testing confirmed that access was denied when the device did not meet compliance requirements.

