<p align="center">
  <img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Enabling and Unlocking Accounts using Active Directory Deployed in the Cloud (Azure)</h1>
In this home lab, I simulate a locked-out user account after multiple failed login attempts and demonstrate how to unlock it within Active Directory as an admin. I also configure the Account Lockout Threshold in Group Policy and observe logs for troubleshooting.

<h2>Environments and Technologies Used</h2>
<ul>
  <li>Microsoft Azure (Virtual Machines/Compute)</li>
  <li>Remote Desktop</li>
  <li>Active Directory Domain Services</li>
  <li>PowerShell</li>
</ul>

<h2>Operating Systems Used</h2>
<ul>
  <li>Windows Server 2022</li>
  <li>Windows 10 (21H2)</li>
</ul>

<h2>High-Level Deployment and Configuration Steps</h2>

<h3>Dealing with Account Lockouts</h3>
<ol>
  <li>Log in to DC-1 and pick a user account you created previously.</li>

  <li>Configure Group Policy to lock out an account after 5 failed login attempts:</li>
  <p align="center">
    <img src="https://github.com/user-attachments/assets/ad975169-aae8-49eb-ba33-ddb9c8d7c914" alt="Group Policy Configuration"/>
  </p>

  <li>Attempt to log in 6 times with an incorrect password. The account will be locked out.</li>

  <li>Unlock the account and reset the password. Attempt to log in again.</li>
  <p align="center">
    <img src="https://github.com/user-attachments/assets/00dcce29-8743-4a3a-a97a-cd20eb85253d" alt="Unlock Account Screenshot"/>
  </p>
</ol>

<h3>Enabling and Disabling Accounts</h3>
<ol>
  <li>Disable the same account in Active Directory.</li>
  <li>Attempt to log in with the disabled account, observe the error message.</li>
  <li>Re-enable the account and attempt to log in again.</li>
  <p align="center">
    <img src="https://github.com/user-attachments/assets/4d0a7f90-21c4-44a1-adf9-9a59e4bc4831" alt="Disable and Re-enable Account"/>
  </p>
</ol>

<h3>Observing Logs</h3>
<ol>
  <li>Observe the logs in the Domain Controller.</li>
  <li>Observe the logs on the client machine.</li>
  <p align="center">
    <img src="https://github.com/user-attachments/assets/9ced78f2-7c3a-4b43-964d-411005c87462" alt="Log Observation Screenshot"/>
  </p>
</ol>

<h2>Takeaways and Key Skills Developed</h2>
<ul>
  <li>Hands-on experience with managing user accounts in Active Directory in a cloud-based Azure environment.</li>
  <li>Configured Account Lockout Thresholds using Group Policy to simulate account lockouts after failed login attempts.</li>
  <li>Unlocked user accounts and reset passwords as an admin, ensuring proper troubleshooting of access issues.</li>
  <li>Disabled and re-enabled accounts, further understanding user account management in Active Directory.</li>
  <li>Observed and analyzed logs from both the Domain Controller and client machine to diagnose and resolve login problems.</li>
  <li>Gained practical experience with Azure Virtual Machines and Remote Desktop for cloud-based administration and remote troubleshooting.</li>
  <li>Developed essential skills in cloud support engineering, including security management, account recovery, and log analysis.</li>
</ul>
