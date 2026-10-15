# Mythical Operator beta13 tester guide

Install **0.2.0-beta.13**, complete the checks below and try one feature available to you, or the feature in your
invitation. Send every result, question or concern through the
[feedback form](/feedback). Keep your tester reference for follow-ups.

## Install or update

Download the installer for your system and `SHA256SUMS` from the
[beta13 download folder](/downloads). Use files from that one delivery.

| System                                     | Installer                                               |
| ------------------------------------------ | ------------------------------------------------------- |
| Windows 11 x64                             | `Mythical.Operator-0.2.0-beta.13-win-x64.exe`           |
| Ubuntu 24.04 x64                           | `Mythical.Operator-0.2.0-beta.13-linux-amd64.deb`       |
| Linux Mint or another compatible x64 Linux | `Mythical.Operator-0.2.0-beta.13-linux-x86_64.AppImage` |

On Windows, check the downloaded file in PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 '.\Mythical.Operator-0.2.0-beta.13-win-x64.exe'
```

Compare its hash with the matching entry in `SHA256SUMS`. This beta has no
commercial publisher signature, so Windows may identify an unknown publisher.
If you are unsure about the file or installation, ask through the form.

On Linux, check the downloaded files from their folder:

```sh
sha256sum --ignore-missing -c SHA256SUMS
```

The installer you will use must report `OK`. For Ubuntu, install the DEB:

```sh
sudo apt install './Mythical.Operator-0.2.0-beta.13-linux-amd64.deb'
```

For AppImage, grant execution permission and open it as your ordinary user:

```sh
chmod +x './Mythical.Operator-0.2.0-beta.13-linux-x86_64.AppImage'
'./Mythical.Operator-0.2.0-beta.13-linux-x86_64.AppImage'
```

If FUSE is missing, try the AppImage with `--appimage-extract-and-run`. If
Ubuntu blocks its sandbox, use the DEB or request installation help through the
form. Keep the Electron sandbox enabled.

For an update, stop the active session, create and verify an encrypted backup,
exit the app and install over the previous version. Keep the existing profile.
Run one version at a time. A profile renewed with beta12 localfix.3 or beta13
must not be downgraded to the original beta12.

## First session

1. Choose your language, configure the vault and optional PIN, and add a public
   account for observation. Enter wallet secrets only in the app's local vault
   window. Use a dedicated test wallet for live operations.
2. Check the account, network and inventory. Open a review for your assigned
   feature, verify the assets, destination and fees, then cancel. No operation
   should be submitted by that cancellation.
3. If you choose a live test, review and confirm your limits and validity in
   Settings. Activate the session explicitly. Review the operation again and
   approve it only when its details are correct.
4. Follow Activity through the result. Compare the assets, fees and remaining
   limits with what you approved. Submission alone is not a completed result.
5. Exit normally and reopen once the submission state is known. Check that
   history persists and the app requires unlocking and manual session activation.

Changing limits or renewing an authorization requires manual session activation.
Closing the window to the tray can leave an authorized session running; use
**Exit** to stop the app. Pause stops new work; it does not reverse work already
submitted.

## Send the result

Use the form even when everything worked. Record review and final execution
separately: **Pass**, **Fail**, **Pending**, **Blocked** or **Not run**. A missing
ingredient, offer or service is a reason to explain a blocked test. Bounty is
observation-only. A delayed game result stays pending until it arrives.

For problems, describe your steps, what you expected and what happened. Never
paste seeds, keys, PINs, passwords, raw signed transactions, vaults, databases or
complete logs. File uploads are disabled for this round; brief redacted text
and optional public transaction references are enough.

If spending, recipients, repeated sends or the ability to stop new work look
wrong, pause or exit if available and choose **Important spending or security
concern** in the form. Preserve the profile and inspect Activity before retrying
an uncertain send. Check the entry page for round updates and retest requests;
all replies go through the same form.

## Current limitations {#limitations}

Updates are manual. Windows 11 x64 and Ubuntu 24.04 x64 are the primary targets; other compatible x64 Linux systems are welcome but coverage varies. Some translations and layouts are still being refined.

Craft and GIFTZ have completed-operation evidence. The reviewed Incubation report included submission, retained-card and renewal evidence; its final return was pending. Morph has earlier completed-operation evidence. Market, Battlegrounds, Polygon/bridge, potions and collection rewards need more complete testing. Bounty is observation-only.

## Feedback privacy {#privacy}

Send all questions and feedback through the [same form](/feedback). Use a non-identifying tester reference. Your real name is not required; an optional Google account address is used only when you request private download access. Responses are stored in Google Forms and a private Google Sheet for the project maintainers. [Google's privacy policy](https://policies.google.com/privacy) applies to those services.

File uploads and public response summaries are disabled. Never send wallet credentials or complete personal exports. Share only brief redacted text; public addresses and transaction references can link activity to you, so omit them unless essential.

Reports and access requests are reviewed manually during the invited round, 15–29 October 2026. This form is not monitored continuously and no fixed response time is promised. Check [round updates](/#updates) before another test. This website uses no analytics scripts or tracking cookies.
