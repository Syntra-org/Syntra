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

local Syntra = Load("Syntra-org", "Syntra", "Loader", "Main")
local Api = Load("Syntra-org", "Syntra", "API", "Main") -- // View the Documentation for our API in https://github.com/Syntra-org/Syntra
```

## Api Documentation
> API.Key("YourKeyHere")

Replace "YourKeyHere" with the key you got from our website, this allows you to directly execute the script without having to boot up the loader.
