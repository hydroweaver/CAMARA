### Bank Application User Verification Workflow

1. **Scenario**: 
   - A bank application needs to verify the user's identity and in the process needs to ensure they are accessing the app from a specific location (e.g., within France).
2. **User Input**: 
   - The user enters their phone number (MSISDN) into the application.
3. **Network API Call**: 
   - The application sends a request to the network's CAMARA APIs using the provided MSISDN.
4. **Network Response**: 
   - The network responds to the app with the latest known location of the user based on network data.
5. **Location Verification** (Backend Logic, not shown in UI):
   - The bank compares the user's network-reported location (via API) with the desired location:
     - **If the device (MSISDN) is in France**: Verification succeeds, and the user is allowed access.
     - **If the device (MSISDN) is outside France**: Verification fails, and the user is denied access to the application's resources.
