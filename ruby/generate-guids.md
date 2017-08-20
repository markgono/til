# Generating GUIDs

You can generate GUIDs for use in Ruby using the built-in SecureRandom library. These will be random and whilst not guaranteed to be unique - it is safe to assume so for most practical purposes. 

## Usage

`require 'securerandom'`

Then... 

### UUID

`SecureRandom.uuid` will result in a UUID. e.g. `"9425a5d2-db15-465a-a6bd-227e5dfaa28c"`


### Hex

`SecureRandom.hex` generates a random 16-bit hex value. e.g. `"87c71fb0fc135c9f76185e0c163775fb"`

`SecureRandom.hex(8)` generates a 8-bit hex value. e.g. `"17a65a894de02118"`

### Base64

`SecureRandom.base64` results in a URL-safe base-64 string. e.g. `"Yw7oOyE5GCRcbdsU8FbmnQ=="`


