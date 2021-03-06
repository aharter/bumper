# Using Bumper with the official Android/iOS App 

Bumper *can* be used with the official "Ecovacs" or "Ecovacs Home" app, but with limitations. Your phone needs to use your DNS server with custom settings, and you ***must*** import Bumper's CA cert and trust it before the app will work.

**Steps**

1. Configure your DNS server as described above in the [DNS](DNS_Setup.md) doc
2. [Import the Bumper CA Cert](#import-the-bumper-ca-cert)
3. [Use the app](#use-the-app)

## Import the Bumper CA Cert

- E-mail yourself the Bumper CA cert (located at `./certs/CA/cacert.crt`)

**Note:** Make sure you select the `cacert.crt` file, which is a DER encoded version that will work on either Android or iOS.

![Example of emailing CA cert](images/emailcert.png)

- Import the cert as a CA, and trust it
	- Instructions for [iOS](#importing-the-ca-cert-on-ios)
	- Instruction for [Android](#importing-the-ca-cert-on-android)

----

### Importing the CA Cert on iOS

1. Open the e-mail on your iOS device, and click the attached cert

![Example of email on iOS device](images/ios_email_cert.png)

2. Install the profile by clicking "Install", and entering your pass code if prompted

![Example of install profile on iOS device](images/ios_install_profile.png)

3. Accept the certificate warning by clicking "Install" again

![Example of cert warning on iOS device](images/ios_cert_warning_install.png)

4. Click "Done" to exit the profile installation
5. Go to Settings > General > About
6. Scroll to the bottom and click "Certificate Trust Settings"
7. Enable Full Trust for the Bumper CA Cert, by moving the slider to the right

![Example of enable trust cert on iOS device](images/ios_cert_trust.png)

![Example of enable trust cert on iOS device 2](images/ios_cert_trust_continue.png)

8. Click continue when prompted
9. That's it, you can now [Use the app](#use-the-app)

----

### Importing the CA Cert on Android

1. Open the e-mail on your Android device

**Quick Method**

2. Click the cert, and if prompted provide a name
3. Under "Used for", select "VPN and apps"

**Long Method**

2. Save the attached cert file
3. Go to Settings > Lock screen and security > Other security settings
4. Under "Credential storage", click "Install from device storage"
5. Browse to the downloaded cert, select it, then click "Done"
6. Click the cert, and if prompted provide a name
7. Under "Used for", select "VPN and apps"

Now, start [using the app](#use-the-app).

----

### Use the app
 
 - Open the app
 - At this time there is no authentication layer, you can enter any e-mail address and password (as long as it is 6 characters) and you will be authenticated
 - If your robot has already checked into Bumper, then it will be available in the list of robots  
- The app now does a ping to the robot to make sure it is online, and if it is you can now control the robot
