---
title: Tech:Mattermost
---

The [WikiTide Foundation](https://meta.miraheze.org/wiki/Special:MyLanguage/WikiTide_Foundation) uses a self-hosted Mattermost instance on [mattermost1](https://meta.miraheze.org/wiki/Tech:mattermost1) for all internal (NDA-bound or confidential/sensitive) conversations. This is a guide for how to use Mattermost.

## Mattermost Access and Usage 

**Note**: *You can access the web version of Mattermost at **[mattermost.wikitide.net](https://mattermost.wikitide.net)**.*

---

If it isn't a **sensitive**, **confidential**, or **highly internal** matter, public venues (such as [Discord](https://meta.miraheze.org/wiki/Special:MyLanguage/Discord) or [IRC](https://meta.miraheze.org/wiki/Special:MyLanguage/IRC)) are most appropriate.

For example, discussions during maintenance should primarily be done on Mattermost, so that you can actively communicate during maintenance without other distractions or causing confusion within the community.

The end result should be made public if possible (non sensitive/confidential), however all information should be ensured to be accurate before making it public to prevent the spread of any misinformation that causes members within the community to worry unnecessarily.

---

**All members of the following groups should be given access to Mattermost**:
* [Board Directors](https://meta.miraheze.org/wiki/Special:MyLanguage/Board_of_Directors)
* [Technology team volunteers](https://meta.miraheze.org/wiki/Special:MyLanguage/Tech:Volunteers)
* [Trust and Safety members](https://meta.miraheze.org/wiki/Special:MyLanguage/Trust_and_Safety)

**Channel Information**:
* TSPortal will send webhook notifications to the **ts-reports** channel on Mattermost. Only Trust and Safety and members of the Board of Directors have access to this channel.
* Members of the Board of Directors should have access to every channel, while members of the Technology team and Trust and Safety should only have access to the **Tech** and **Trust and Safety** categories respectively. All members should have access to the **General** category.

## Setting Up the Mattermost Mobile App 

1. **Download the App**

   *You can download the Mattermost mobile app from the following platforms:*

   * **iOS**: [App Store](https://apps.apple.com/us/app/mattermost/id1257222717)
   * **Android**: [Google Play Store](https://play.google.com/store/apps/details?id=com.mattermost.rn)

2. **Login to the Server**
* Once installed, open the app and enter the URL of the Mattermost server (you may need to click **Sign in** first):
      `https://mattermost.wikitide.net`
* Enter a display name for the server. This can be anything you want (i.e. **WikiTide Foundation**).
* Click **Connect** and then log in with your credentials (email or username and password).
* Click **Log In**.

3. **Allow Push Notifications**
* After (or sometimes before) logging in, you may be prompted to enable push notifications.
* Follow the instructions to set up notifications so you don't miss important messages.

## Changing Push Notification Settings 

Push notifications on the Mattermost mobile app can be customized to ensure you receive alerts for important events. Sometimes, the default settings can be unreliable, so you may want to tweak them to your preference.

1. **Access Notification Settings**
* Open the Mattermost app and go to the main settings menu by tapping your profile icon in the bottom corner.
* Select **Settings** > **Notifications** > **Push Notifications**.

2. **Configure Push Notifications**

*There are two key sections to adjust within the **Push Notifications** settings:*

**Notify me about...**

*This setting controls what types of messages trigger notifications:*

* **All new messages**: Notifies you of every message in the channels you are a member of.
* **Only for mentions, direct messages, and replies**: Notifies you only when you are directly mentioned, receive a direct message, or someone replies to your post.
* **Nothing**: Disables all push notifications.

**Trigger push notifications when...**

*This setting controls when notifications are sent based on your status:*

* **Online, away, or offline**: Receive push notifications regardless of whether you are online, away, or offline.
* **Away or offline**: Receive push notifications only when you are not actively using the app (i.e., when your status is set to Away or Offline). However, this setting can sometimes be unreliable, as your status may stay as **Online** even after closing the app, leading to missed notifications.
* **Offline**: Only receive notifications when your status is set to Offline.

## Setting the Theme 

Mattermost has both preset themes and custom themes.

1. **Preset Themes**
* Go to the profile menu (mobile) or settings icon (desktop) and select **Settings** > **Display** > **Theme**.
* Choose from preset themes like **Denim**, **Sapphire**, **Quartz**, **Indigo**, or **Onyx**.

2. **Custom Themes**

*To create a custom theme, follow these steps:*

* From **Settings** > **Display** > **Theme**, scroll down to **Custom Theme**.
* Click **Edit**, and you’ll see the option to change the colors for different elements such as header, sidebar, and text.
* You can enter specific hex color codes to get the exact colors you want.
* When finished, tap **Save**.

**Note**: *Custom themes are only available from the web version or desktop app of Mattermost. However, when a custom theme is selected, it will also apply to the mobile app.*

## Setting Up Multi-Factor Authentication (MFA) 

**Note**: *Multi-factor authentication (MFA) can only be set up via the web version or desktop app of Mattermost.*

Enabling MFA adds an extra layer of security to your account by requiring a second form of authentication, such as a code from an authentication app, in addition to your password.

*Steps to enable Multi-Factor Authentication:*

* Click on your profile icon in the top-right corner of the screen.
* Select **Security** in the sidebar.
* Navigate to **Multi-factor Authentication** and click **Edit**.
* Follow the on-screen instructions to complete the setup.

## Setting Display Name 

Your display name in Mattermost is how other users will see you in the app. By default, the display name is set as follows:

* If you have a nickname set, that will be used as your display name.
* If no nickname is set, Mattermost will use your first and last name.
   * If only the first name or only the last name is set, it will use whichever is available.
* If none of these are set, your username will be displayed.
   * Usernames are always lowercase, so you may want to set a display name using the above fields if you prefer capitalization or specific formatting.

To manually set or change your display name, follow these steps:

**On Desktop:**

* Click your profile icon in the top-right corner.
* Select **Profile** from the dropdown menu.
* Click **Edit** next to **Full Name** to change your first and last name, or click **Edit** next to **Nickname** to set or update your nickname.
* Save your changes.

**On Mobile:**

* Tap your profile icon in the bottom corner.
* Select **Your Profile** from the menu.
* Enter or update your **First Name**, **Last Name**, or **Nickname** in the respective fields.
* Save your changes.

This will update how your name appears to others in Mattermost.

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Mattermost](https://meta.miraheze.org/wiki/Tech:Mattermost)