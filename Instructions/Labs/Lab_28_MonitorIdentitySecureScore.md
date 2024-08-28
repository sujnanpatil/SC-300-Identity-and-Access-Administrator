# Lab 28 - Monitor and manage security posture with Identity Secure Score

## Lab scenario

Microsoft Entra Identity Protection provides automated detection and remediation to identity-based risks, and provides data in the portal to investigate potential risks. Microsoft Entra Identity Protection also provides an Identity Secure Score to monitor and improve your identity security posture. In the same manner as Microsoft Defender XDR and Microsoft Defender for Cloud, Identity Secure Score provides improvement actions and recommendations that can improve your overall security posture for identity in Microsoft Entra ID. This lab will explore this capability.

## Lab objectives
In this lab, you will complete the following tasks:

+ Task 1 - Review Identity Secure Score and improvement actions
+ Task 2 - Execute an improvement action

## Architecture Diagram

![Screen image displaying the New Group page with Group type, Group name, Owners, and Members highlighted](./media/arch28.png)

## Estimated time: 15 minutes

## Architecture diagram

### Exercise 1 - Using Identity Secure Score to monitor and manage identity security posture

#### Task 1 - Review Identity Secure Score and improvement actions

1. Open a new tab, and sign in to the [https://entra.microsoft.com/](https://entra.microsoft.com/).

2. From the left-hand navigation pane, select **Protection > Identity Secure Score** to view the dashboard.

3. Select **Identity Secure Score**. This will take you to the Identity Secure Score dashboard.

4. Scroll down to view the **Improvement actions**.

5. In contrast to the improvement actions in Microsoft Defender for Cloud and Microsoft Defender XDR, these improvement actions are specific to identity. This provides a more focused list of potential actions to your security posture management. Any improvement actions initiated from this list will also provide an impact to your overall tenant security posture.

#### Task 2 - Execute an improvement action

1. To improve one area of the identity security posture, select **Conditional Access**. A new tab will open for **Conditional Access**.

   **Note** - By default the Get Started button will open in Azure Portal. You can use the portal or return to the Entra admin center. Either will work.

2. Select **+ Create new policy** from **Conditional Access | Overview** page.

3. Give your policy a name as **Accesspolicy-<inject key="DeploymentID"></inject>**. We recommend that organizations create a meaningful standard for the names of their policies.

4. Under Assignments, select **0 users and groups selected**. Under Include, select **All users**.

5. Under Exclude, select **Users and groups** and choose any accounts that must maintain the ability to use legacy authentication. Microsoft recommends you exclude at least one account to prevent yourself from being locked out. For now select **Spektra Systems** and **ODL_User <inject key="DeploymentID"></inject>**.

6. Under Target resources, select **No target resources selected** > **Cloud apps** > under **Include**, select **All cloud apps**.

7. Under Conditions select **0 conditions selected** > under **Client apps** select **Not configured**, set **Configure** to **Yes**. Check only the boxes **Exchange ActiveSync clients** and **Other clients**. Select Done.

8. Under Access controls|Grant select **0 controls selected**, select Block access. Choose Select.

9. Confirm your settings and set Enable policy to **Report-only**.

10. Select **Create** to create to enable your policy.

### Review
In this lab, you have completed:
- Review Identity Secure Score and improvement actions
- Execute an improvement action

### You have successfully completed the lab
