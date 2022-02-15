---
title: Some PowerShell
date: "2022-02-15T10:46:00.000Z"
description: A blog post showing what PowerShell looks like when rendering in Prism.js and Gatsby.
---

Here is an example of how to write Powershell in Markdown and have the proper syntax highlighting using Prism.js!

```powershell
Get-CimInstance -ClassName Win32_Processor | Select-Object -ExcludeProperty "CIM*"
```