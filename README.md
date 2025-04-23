# Syntra
> A scripting utility for roblox 

## Booting the Script
```lua
local function Load(user, repo, name, file)
    local url = ("https://raw.githubusercontent.com/%s/%s/main/%s/%s"):format(user, repo, name, file)
    local s,o = pcall(function() return loadstring(assert(game:HttpGet(url), "HttpGet failed"))() end) 
    if not s then game.Players.LocalPlayer:Kick("Failed to load " .. file .. "\n\nYour executor is most likely not supported.") end
    return o
end

local Syntra = Load("RobloxScriptHub", "Syntra", "Loader", "Main")
```
