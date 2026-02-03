# Software Interface and Stack

The **"Login Recovery and Foreign Login Attempt Protection"** feature will integrate with the existing Cloudeka Service Portal's authentication and user management systems. Key components and the underlying software stack involved are:

- **Cloudeka Service Portal Frontend:** The existing web application where users log in and interact with their services. This will be modified to present the confirmation page and handle user input.
- **Cloudeka Service Portal Backend/API:** The server-side application responsible for user authentication, session management, and data handling. This component will be extended to:
  - Detect new devices based on browser fingerprint and device ID.
  - Trigger email notifications.
  - Process user confirmations (marking devices as trusted).
  - Initiate password reset flows.
  - Modify user account permissions (for temporary blocks).
  - Manage and store trusted device information for each user.
- **Email Service Provider:** An external or internal service responsible for sending transactional emails to users.
- **Database/User Store:** The existing database storing user profiles, login history, device information, and account permissions. This will need updates to store new device fingerprints/IDs and trusted device flags.
- **Geolocation Service (optional/internal):** A mechanism to resolve IP addresses to approximate geographical locations for email notifications.

