# SoloCopy Privacy Policy

> Draft.

Last updated: 23 October 2026
Applies to SoloCopy 0.9.0 (public beta) and later
Online version: https://bhimahelavar.github.io/solocopy/privacy

SoloCopy – Duplicate File Cleaner ("the app") is published by Bhimashankar ("we", "the publisher"). This policy explains what the app stores and what it does not send.

## Summary

- There is no account and no sign-in.
- There is no telemetry, no analytics and no tracking.
- The app does not check for updates by itself.
- The app itself makes no network calls. It works fully offline.
- Your files, file names and delete history stay on your PC.
- We, the publisher, receive nothing from the app.

## What the app stores and where

Everything is stored per Windows user in `%LOCALAPPDATA%\FoundDuplicate` (the folder kept its old name, from when the app was called Found Duplicate).

| What | Where | What it contains | How long |
|---|---|---|---|
| Delete history | `audit\audit-YYYY-MM.jsonl` | For each file you asked to delete: date and time, Windows user name, computer name, file path, file size, result (for example "Moved to the Recycle Bin"), a SHA-256 fingerprint of the file's content, and the path of the copy that was kept. Restores are recorded too. | Until you delete it. New lines are only added. |
| Logs | `logs\app-YYYYMMDD.log` | Technical messages, such as app version, Windows version, errors, folder paths and counts. Never file contents. | 14 days, then deleted by the app. |
| Settings | `settings.json` | Your choices: last folder searched, search options, keep rule and language. | Until you delete it. |
| Browser engine data | `WebView2\` | Data that the Microsoft Edge WebView2 engine needs to draw the app window. | Until you delete it. |

**File contents.** The app reads a file's contents only to calculate a fingerprint (a hash), to find exact copies. The contents are never stored and never sent anywhere.

**Deleted files.** The app moves files to the Windows Recycle Bin. It never deletes files permanently. It refuses to delete on drives without a Recycle Bin (such as network and USB drives). You can put files back with **Restore** in History, or from the Recycle Bin.

**PDF reports.** To make a PDF, the app writes a temporary page to your Windows temporary folder and deletes it right after the PDF is made.

## What never leaves your PC

- your files and their contents
- file names and folder paths
- the delete history, logs and settings (except in the IT administrator case below)
- information about you, your PC or how you use the app

The app has no code that sends data over the internet. It draws its window from files installed with the app, under a made-up local address (`app.founddup.local`). This address does not use the network.

**Links.** Some links point to outside websites, for example the Microsoft download page for WebView2, if WebView2 is missing. These open in your normal web browser, and only when you click them. That website's own privacy policy then applies.

## When your IT administrator sets a history folder

In an office, an IT administrator can use Group Policy (setting `AuditLogFolder`) to save the delete history in another folder, for example a folder on a network server. Then:

- the delete history is stored where IT chooses, and your organisation controls it;
- your organisation's own rules apply to it, not this policy;
- if that folder cannot be reached, the app saves the history on your PC instead.

The publisher does not receive this history either. Ask your IT department how they use it.

## Microsoft Edge WebView2

The app window uses the Microsoft Edge WebView2 Runtime. This is a part of Windows made by Microsoft. It has its own Microsoft privacy terms. WebView2 may contact Microsoft for its own updates, and may send diagnostic data to Microsoft according to your Windows settings. The publisher does not control this and receives none of this data. See Microsoft's privacy statement for details.

## Copy diagnostics

The **Copy diagnostics** button copies some technical details to your clipboard: app and Windows versions, WebView2 version, the app's folders and the most recent log lines. This happens only when you click the button. Nothing is sent. You decide whether to paste it somewhere, for example into an email to support. Check the text before you share it, because log lines can contain folder and file paths.

## Exports

When you export the history to CSV or PDF, the file is saved only in the place you choose. The app does not send it anywhere.

## Your choices

- **Remove your history, logs and settings:** close the app and delete the folder `%LOCALAPPDATA%\FoundDuplicate`. (Type `%LOCALAPPDATA%` in the File Explorer address bar to find it.)
- **Uninstalling keeps this folder on purpose.** The delete history may be needed later. Delete the folder by hand if you want it gone.
- **Microsoft Store version:** Windows may keep these files in the app's own private folder instead, under `%LOCALAPPDATA%\Packages\`. Windows removes that folder when you uninstall the Store version.
- **Language:** you can choose English or Hindi in the app.

## Children

The app is a general tool for managing files. It is not aimed at children, and it does not collect personal data from anyone, including children.

## India's Digital Personal Data Protection Act, 2023

The app does not collect any personal data for the publisher. The publisher does not process your personal data through the app.

The delete history on your PC contains a Windows user name, a computer name and file paths. When an organisation uses the app, that organisation decides how this history is kept, used and deleted. The organisation is responsible for its own records, including the delete history, under the Digital Personal Data Protection Act, 2023 and other laws.

## Changes to this policy

If we change this policy, we will update the "Last updated" date and publish the new version at https://bhimahelavar.github.io/solocopy/privacy. Important changes will also be listed in the release notes.

## Contact

Questions about privacy: bhimarh2020@gmail.com
Publisher: Bhimashankar, India
