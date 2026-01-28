# Product Features

The **"Login Recovery and Foreign Login Attempt Protection"** feature will offer the following key capabilities:

- **New Device Detection:** Automatically identifies when a user logs into the Cloudeka Service Portal from a device not previously recognized. This identification will be based on a combination of browser fingerprinting and device ID.
- **Email Notification for New Device Login:** Upon successful login from a new device, an email notification will be immediately sent to the user's registered email address. This notification will be sent only once per new device login.
- **Detailed Login Information:** The email notification will include crucial details of the suspicious login attempt, such as the logged-in account (email address), the device used (e.g., operating system, browser, device model if available), the date and time of login, and the approximate location (based on IP geolocation) along with the IP address.
- **Security Action Link:** The email will contain a clear call-to-action button/link, "Secure My Account," which users can click if the login was not authorized by them. This link will be valid for 7 days.
- **Interactive Confirmation Page:** Clicking the security action link will redirect the user to a dedicated page within the Cloudeka Service Portal (without requiring re-authentication). This page will present the user with details of the login and ask for confirmation: "Is this you?".
- **User Confirmation Options:**
  - **"Yes, that's me":** The user confirms the login. This action will also implicitly mark the newly used device as 'trusted' for future logins, preventing further notifications for that specific device.
  - **"No, that's not me":** The user indicates the login was unauthorized. This option will lead to immediate actions to secure the account.
- **Account Securing Actions (if "No, that's not me" selected):**
  - **Password Change:** Users will be redirected to a password reset page to immediately change their password.
  - **Temporary Account Block:** The user's account permissions will be temporarily limited to 'view mode' only. A prompt will be displayed, instructing the user to contact the administrator for full account restoration. An additional notification will be sent to the user confirming the account block/permission limitation.
- **Graceful Handling of Unconfirmed Logins:** If the email is ignored or the security action link expires, the login will be considered legitimate, and no adverse action will be taken against the user's account.
- **Post-MFA Implementation:** This feature will be triggered *after* a successful login, even if Multi-Factor Authentication (MFA) is already in place.

