<div align="center">

# ESX Documents

## Requirements
* ESX framework

This is a modified esx_documents that allows you to create an item using ox_inventory metadata.

## Installation
Add esx_documents to server.cfg

Add this to @ox_inventory/data/items.lua

["documents"] = {
		label = "Documents",
		weight = 50,
		stack = false,
		close = true,
		client = {
			anim = { dict = 'missheistdockssetup1clipboard@base', clip = 'base' },
			prop = { model = `p_amb_clipboard_01`, pos = vec3(0.01, 0.01, 0.06), rot = vec3(5.0, 5.0, -180.5) },
			event = "mydocuments:show",
		},
	},

### Official esx_documents
```
https://github.com/apoiat/ESX_Documents
```