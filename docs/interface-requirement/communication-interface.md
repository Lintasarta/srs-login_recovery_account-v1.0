# Communication Interface

Communication related to this feature will primarily occur between the following components:

- **User Browser to Cloudeka Service Portal Backend:**
  - During login, the browser will send device fingerprint and ID information to the backend.
  - When the user clicks the security link in the email, the browser will navigate to a specific endpoint on the Cloudeka Service Portal.
  - User selections ("Yes, that's me" / "No, that's not me") will be communicated back to the backend via secure API calls (e.g., HTTPS).

- **Cloudeka Service Portal Backend to Email Service Provider:**
  - The backend will send requests to the email service provider to trigger new device login notification emails, including all necessary dynamic content (account, device, date, location, confirmation link).
  - **Protocol:** Typically SMTP or API calls (HTTPS).

- **Cloudeka Service Portal Backend to Database/User Store:**
  - The backend will query the database to check for existing device IDs/fingerprints for a user.
  - It will update the database to mark devices as trusted, update user account permissions (for blocking), and potentially log foreign login attempts.
  - **Protocol:** Standard database connection protocols.

- **Cloudeka Service Portal Backend to Geolocation Service (if external):**
  - If an external geolocation service is used, the backend will send the user's login IP address to retrieve location details.
  - **Protocol:** Typically HTTPS API calls.
