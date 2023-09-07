# ESX Documents

## Requirements
* ESX framework

This is a modified esx_documents that allows you to create an item using ox_inventory metadata.

## Installation
Add esx_documents to server.cfg

Add this to @ox_inventory/data/items.lua
```
["documents"] = {
		label = "Documents",
		weight = 50,
		stack = false,
		close = true,
		client = {
			anim = { dict = 'missheistdockssetup1clipboard@base', clip = 'base' },
			prop = { model = `p_amb_clipboard_01`, pos = vec3(0.01, 0.01, 0.06), rot = vec3(5.0, 5.0, -180.5) },
			event = "esx_documents:viewdocuments",
		},
	},
```

Add this to your context script
```
lib.registerContext({
    id = 'police_documents_menu',
    title = '📑 Police Documents Menu',
    options = {
      {
        title = '🔫 Weapons Permit',
        description = 'Special gun permit provided by the police.',
        event = 'esx_documents:createnewdocument',
        args = 1
      },
      {
        title = '🚘 Student Driver Permit',
        description = 'Special student driver permit by the police.',
        event = 'esx_documents:createnewdocument',
        args = 2
      },
      {
        title = '👮🏻‍♂️ Police Clearance',
        description = 'Official clean, general purpose, citizen criminal record.',
        event = 'esx_documents:createnewdocument',
        args = 3
      }
    }
  })

  lib.registerContext({
    id = 'ambulance_documents_menu',
    title = '📑 Ambulance Documents Menu',
    options = {
      {
        title = '😷 Medical Report - Phatology',
        description = 'Official medical report provided by a pathologist.',
        event = 'esx_documents:createnewdocument',
        args = 1
      },
      {
        title = '😀 Medical Report - Psychology',
        description = 'Official medical report provided by a psychologist.',
        event = 'esx_documents:createnewdocument',
        args = 2
      },
      {
        title = '🤓 Medical Report - Eye Specialist',
        description = 'Official medical report provided by an eye specialist.',
        event = 'esx_documents:createnewdocument',
        args = 3
      }
    }
  })
```
### Official esx_documents
```
https://github.com/apoiat/ESX_Documents
```
