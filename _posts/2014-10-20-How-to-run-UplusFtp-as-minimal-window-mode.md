---
layout: post
title: How to run UplusFtp as minimal window mode
---

Copy the VBScript code to a vbs file and save it into the UplusFtp directory as naming ftprun.vbs , and run it.

bc.. Set WshShell = WScript.CreateObject("WScript.Shell")
FTP = CreateObject("Scripting.FileSystemObject").GetFile(Wscript.ScriptFullName).ParentFolder.Path
WshShell.Run FTP&"\ftpadmingui.exe", 0
