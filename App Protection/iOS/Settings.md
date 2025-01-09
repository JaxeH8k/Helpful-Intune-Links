https://github.com/MicrosoftDocs/memdocs/blob/main/memdocs/intune/apps/app-protection-policy-settings-ios.md

Use CFBundleUrl for Exemptions from Transferring to Managed Apps
GROK:
To exempt a third-party app in an Intune iOS App Protection Policy using the "Select apps to exempt" setting, you need to use the app's URL protocol or URL scheme. Here's how you can proceed:

Identify the URL Scheme: The URL scheme is a unique identifier for the app on iOS. This can usually be found in the app's Info.plist file under the key CFBundleURLSchemes. If you don't have direct access to the app's source code or the .ipa file, you might need to contact the app's developer to get this information.
Format for Exemption: Once you have the URL scheme, you should enter this into the exemption field in the Intune admin center. For example, if the URL scheme for an app like "MyApp" was "myapp", you would enter myapp into the "Select apps to exempt" field.
Example: If you're exempting the Webex app for iOS, and its URL scheme is wbx, you would simply enter wbx in the exemption list.

Here's a summary based on the information from the web results:

iOS URL Protocol: You need to use the URL protocol of the app to exempt it. This means adding the URL scheme string to the exemption list in the policy settings.




Remember, this exemption allows managed apps to transfer data to the specified unmanaged app using the iOS operating system's "Share" functionality or open links directly in the app. However, this does not affect restrictions like copy/paste unless explicitly configured otherwise.