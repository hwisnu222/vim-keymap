# HTTP Request


install library 

```bash
# use LuaRocks (package manager for Lua):
luarocks install luasocket

# if use Lua 5.1 (default Neovim):
luarocks --lua-version=5.1 install luasocket
```


```bash

local http = require("socket.http")
local ltn12 = require("ltn12")

local response = {}
local body = [[{ "contents": [{ "parts": [{ "text": "example text" }] }] }]]

local res, code = http.request{
  url = "https://example.com/api/v1",
  method = "POST",
  headers = {
    ["Content-Type"] = "application/json",
    ["Content-Length"] = tostring(#body)
  },
  source = ltn12.source.string(body),
  sink = ltn12.sink.table(response)
}

print(table.concat(response))
```