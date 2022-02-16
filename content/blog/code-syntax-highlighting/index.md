---
title: Code Syntax Highlighting Test
date: "2022-02-15T10:46:00.000Z"
description: A blog post showing what code looks like when rendering in Prism.js and Gatsby.
categories: ["PowerShell"]
image: ./pwsh-girl.png
---

## PowerShell
```powershell {numberLines}
Get-CimInstance -ClassName Win32_Processor | `
Select-Object -ExcludeProperty "CIM*"
```

## HTML
```html {numberLines}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>

<p>My first paragraph.</p>

</body>
</html>
```

## JavaScript
```javascript {numberLines}
function storeNames() { return arguments; }
```

## JSON 
```json {numberLines}
{
    "glossary": {
        "title": "example glossary",
		"GlossDiv": {
            "title": "S",
			"GlossList": {
                "GlossEntry": {
                    "ID": "SGML",
					"SortAs": "SGML",
					"GlossTerm": "Standard Generalized Markup Language",
					"Acronym": "SGML",
					"Abbrev": "ISO 8879:1986",
					"GlossDef": {
                        "para": "A meta-markup language, used to create markup languages such as DocBook.",
						"GlossSeeAlso": ["GML", "XML"]
                    },
					"GlossSee": "markup"
                }
            }
        }
    }
}
```

## Bicep
```bicep {numberLines}
param location string = resourceGroup().location
param storageAccountName string = 'toylaunch${uniqueString(resourceGroup().id)}'

resource storageAccount 'Microsoft.Storage/storageAccounts@2021-06-01' = {
  name: storageAccountName
  location: location
  sku: {
    name: 'Standard_LRS'
  }
  kind: 'StorageV2'
  properties: {
    accessTier: 'Hot'
  }
}
```

## SQL
```sql {numberLines}
SELECT * FROM Customers
WHERE Country='Mexico';
```