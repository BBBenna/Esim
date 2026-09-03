# Using Hotlink eSIM on a Non-eSIM Phone

## Introduction

After losing physical SIM cards several times from constantly swapping them between devices, I finally decided to look into eSIM.

Since I still don't want to replace my phone (definitely not because I'm broke 😄), I experimented with **HookEuicc**, created by **Unicorn369**, and successfully obtained the Hotlink eSIM activation information on a device that does not officially support eSIM.

This method does **not** retrieve a QR code. Instead, it obtains the eSIM-related activation information that can later be used with a compatible eSIM-writing solution.

## How It Works

### 1. Preparation

Before starting, make sure that:

- The **Hotlink app** is installed and you are logged in.
- The option to convert/switch to eSIM is available in the Hotlink app.
- Your Hotlink balance is more than **RM 5**, as the eSIM conversion requires a fee.
- Your Android device has **root access**.
- **LSPosed** is installed and working.
- The **HookEuicc** module is installed.

### 2. LSPosed Configuration

In LSPosed:

1. Enable **HookEuicc** for the Hotlink app.
2. Enable the additional components required by the original HookEuicc instructions.

> [!NOTE]
> Make sure `com.android.se` is selected, then reboot the phone.
>
> Alternatively, you can restart the process manually:
>
> ```bash
> su -c killall com.android.se
> ```

### 3. Converting the Hotlink SIM to eSIM

In my case, LSPosed showed that **HookEuicc was not working**, but it actually worked during testing.

After enabling the module:

1. Open the **Hotlink app**.
2. Start the SIM-to-eSIM conversion process.
3. The previous "device not eligible" warning should no longer appear.
4. Complete the required **KYC verification**.
5. After the process finishes, Hotlink may report that the conversion has failed.
6. However, the eSIM-related information should be copied to the clipboard, with a notification indicating this.
7. I then pasted the information into the eSIM-writing interface and was able to activate the eSIM successfully.

## Result

Both in theory and in my actual test, the method worked successfully.

Many thanks to **Unicorn369** for developing and sharing **HookEuicc**.

There seems to be relatively little information about converting Hotlink SIMs to eSIMs this way, especially compared with services such as Giffgaff, where the process is generally more straightforward. This may partly be due to Hotlink's KYC requirements.

Overall, the process went much more smoothly than I expected, and I was able to complete the conversion and activate the eSIM successfully.

Again, special thanks to **Unicorn369** and the **HookEuicc** project.

## Disclaimer

This README documents my own experiment and is provided for research and reference purposes only.

The procedure involves root access, LSPosed, and modifications to system behavior. Results may vary depending on the device, Android version, Hotlink app version, and network configuration.

Proceed at your own risk.
