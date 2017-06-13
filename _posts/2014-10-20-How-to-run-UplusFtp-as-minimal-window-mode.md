---
layout: post
title: How to run UplusFtp as minimal window mode
---

Copy the VBScript code to a vbs file and save it into the UplusFtp directory as naming ftprun.vbs , and run it.

	Sub forceCScriptExecution
		Dim Arg, Str
		If Not LCase( Right( WScript.FullName, 12 ) ) = "\cscript.exe" Then
			For Each Arg In WScript.Arguments
				If InStr( Arg, " " ) Then Arg = """" & Arg & """"
				Str = Str & " " & Arg
			Next
			CreateObject( "WScript.Shell" ).Run _
				"cscript //nologo """ & _
				WScript.ScriptFullName & _
				""" " & Str
			WScript.Quit
		End If
	End Sub
	forceCScriptExecution

	Set WshShell = WScript.CreateObject("WScript.Shell")
	FTP = CreateObject("Scripting.FileSystemObject").GetFile(Wscript.ScriptFullName).ParentFolder.Path
	WshShell.Run FTP&"\ftpadmingui.exe", 0

