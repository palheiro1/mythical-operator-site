# IFRIT beta14 tester guide

Install **0.2.0-beta.14**, complete the checks below and try one routine available to you, or the routine in your
invitation. Send every result, question or concern through the
[feedback form](/feedback). Keep your tester reference for follow-ups.

## Install or update

Download the installer for your system and `SHA256SUMS` from the
[beta14 download folder](/downloads). Use files from that one delivery.

| System                                     | Installer                                   |
| ------------------------------------------ | ------------------------------------------- |
| Windows 11 x64                             | `IFRIT-0.2.0-beta.14-win-x64.exe`           |
| Ubuntu 24.04 x64                           | `IFRIT-0.2.0-beta.14-linux-amd64.deb`       |
| Linux Mint or another compatible x64 Linux | `IFRIT-0.2.0-beta.14-linux-x86_64.AppImage` |

On Windows, check the downloaded file in PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 '.\IFRIT-0.2.0-beta.14-win-x64.exe'
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
sudo apt install './IFRIT-0.2.0-beta.14-linux-amd64.deb'
```

For AppImage, grant execution permission and open it as your ordinary user:

```sh
chmod +x './IFRIT-0.2.0-beta.14-linux-x86_64.AppImage'
'./IFRIT-0.2.0-beta.14-linux-x86_64.AppImage'
```

If FUSE is missing, try the AppImage with `--appimage-extract-and-run`. If
Ubuntu blocks its sandbox, use the DEB or request installation help through the
form. Keep the Electron sandbox enabled.

For an update, stop the active session, create and verify an encrypted backup,
exit the app and install over the previous version. Keep the existing profile.
Run one version at a time. A profile renewed with beta12 localfix.3, beta13 or beta14
must not be downgraded to the original beta12. Do not downgrade a profile after a beta14 migration.

## First session

1. Choose your language and open or create your profile. Keep wallet secrets in
   the app's local vault window. Use a dedicated test wallet for any live test.
2. Open **Routines**. Check the compact app status, your current routines and
   the templates you can create. Expand details only when you need the limits
   or an explanation. Opening a template must never submit an operation.
3. Create or edit one routine, review its purpose, assets and limits, then cancel
   once to check the flow. No live operation is needed to test the interface.
4. If you choose a live test, confirm the routine and the app's authorization,
   then enable automation explicitly. Follow **Activity** through the result;
   submission alone does not mean completion. Compare actual spending and fees
   with the limits you approved.
5. Pause the routine and check that its paused state persists. Exit and reopen
   the app; verify your profile, history and limits before resuming. After an
   update, follow any explicit migration or renewal instructions in the app.

Locking the interface hides private details and is separate from pausing
work. Closing to the tray may leave automation running. Use **Pause automation**
to stop new work or **Exit** to stop the app. A pause does not reverse a submitted
operation. Automatic resumption is available only when explicitly authorized for
that computer; check the displayed status after reopening.

## Send the result

Use the form even when everything worked. Report version **0.2.0-beta.14**; if it is not listed, choose **A different version** and include it in your report. Record review and final execution
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

Beta14 focuses on routines and a compact overview. Historical live-operation results from earlier betas do not validate every routine in this version. A full 48-hour live continuity exercise and complete Windows 11 manual acceptance are separate checks. Bounty remains informational. Report a delayed game result as pending until it arrives.

This invited beta still has unresolved dependency security alerts, including high-severity findings. The download includes `VALIDATION.md` with the test results and outstanding checks. It is not a security-cleared production release.

## Feedback privacy {#privacy}

Send all questions and feedback through the [same form](/feedback). Use a non-identifying tester reference. Your real name is not required; an optional Google account address is used only when you request private download access. Responses are stored in Google Forms and a private Google Sheet for the project maintainers. [Google's privacy policy](https://policies.google.com/privacy) applies to those services.

File uploads and public response summaries are disabled. Never send wallet credentials or complete personal exports. Share only brief redacted text; public addresses and transaction references can link activity to you, so omit them unless essential.

Reports and access requests are reviewed manually during the invited round. This form is not monitored continuously and no fixed response time is promised. Check [round updates](/#updates) before another test. This website uses Vercel Web Analytics without tracking cookies.
