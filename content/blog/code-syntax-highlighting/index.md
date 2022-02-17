---
title: Code Syntax Highlighting Test
date: "2022-02-15T10:46:00.000Z"
description: A blog post showing what code looks like when rendering in Prism.js and Gatsby.
category: How-To
tags: ["PowerShell", "Bicep", "HTML", "JavaScript", "JSON", "SQL"]
---

## PowerShell
```powershell {numberLines}
Get-CimInstance -ClassName Win32_Processor | `
Select-Object -ExcludeProperty "CIM*"
```
## Terraform
```terraform {numberLines}
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 3.27"
    }
  }

  required_version = ">= 0.14.9"
}

provider "aws" {
  profile = "default"
  region  = "us-west-2"
}

resource "aws_instance" "app_server" {
  ami           = "ami-830c94e3"
  instance_type = "t2.micro"

  tags = {
    Name = "ExampleAppServerInstance"
  }
}
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