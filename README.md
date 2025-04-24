# Syntra
> A scripting utility for roblox 

# Booting the Script
```lua
local function Load(user, repo, name, file)
    local url = ("https://raw.githubusercontent.com/%s/%s/main/%s/%s"):format(user, repo, name, file)
    local s,o = pcall(function() return loadstring(assert(game:HttpGet(url), "HttpGet failed"))() end) 
    if not s then game.Players.LocalPlayer:Kick("Failed to load " .. file .. "\n\nYour executor is most likely not supported.") end
    return o
end

local Syntra = Load("Syntra-org", "Syntra", "Loader", "Main") -- // Loads the Syntra loader
-- // View the Documentation for our API in https://github.com/Syntra-org/Syntra
```

## API Documentation
Directly execute the script `without having to boot up the loader.`
```lua
Syntra.Key("YourKeyHere")
```
Replace `YourKeyHere` with the key you recieved from the website, add this part of code under `local Syntra = Load("Syntra-org", "Syntra", "Loader", "Main")`. 

## Tutorial
Syntra requires a good executor and device to run it; PC Executors such as AWP, Wave, Swift are recommended.
Upon executing the script, you will be greeted with a key input and submit key button, press "Get Key" and paste it in your browser to get started. If you have issues with the key system or anything else, check our discord: https://discord.gg/vTYMjtDA5V
