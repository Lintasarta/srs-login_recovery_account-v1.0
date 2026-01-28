# Scope

**In-Scope:**

- **New Device Login Detection:** The system will identify and flag successful user logins that originate from a browser or device not previously associated with the user's account.
- **Email-Based User Notification:** An automated email notification will be sent to the user upon a successful login from a new device, containing details of the login event.
- **User-Driven Login Verification:** A secure, one-time-use link will be provided in the notification email, allowing the user to confirm the login's legitimacy ("Yes, that's me") or deny it ("No, that's not me").
- **Account Securing Actions:** If a user denies a login attempt, the system will provide immediate options to secure the account, specifically by initiating a password change or placing the account into a temporary, view-only mode.
- **Trusted Device Management:** The system will maintain a list of trusted devices for each user to prevent repeated notifications for legitimate, recognized devices.
- **Inactive Account Deactivation:** The system will include an automated process to deactivate user accounts that have shown no login activity for more than 60 consecutive days.

**Out-of-Scope:**

- **Implementation of Multi-Factor Authentication (MFA):** This feature operates after a successful login and MFA challenge. It does not include the development or modification of the MFA system itself.
- **Alternative Notification Channels:** Notifications will be sent via email only. SMS, push notifications, or other messaging platforms are not included in this version.
- **Social Media Login:** Authentication using third-party providers like Google or Facebook is not part of this feature.
- **Forced Logout of Active Sessions:** While an account can be temporarily blocked, this feature will not automatically terminate all other active sessions for the user.
- **Admin-Facing Security Dashboard:** A centralized dashboard for administrators to review all foreign login attempts across the entire user base is not included. The feature is focused on user self-service security.
- **Deactivation of Organization and Projects:** While this SRS will add cleanup of unused accounts, the business flow for organization and projects (in which the accounts are attached to) will be different and require attention in itself, hence it will not be mentioned in this document.

