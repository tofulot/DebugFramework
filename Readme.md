# DebugFramework
[DebugFrameworkPlugin](https://www.roblox.com/library/9840069360/DebugFramework) is a plugin based off the [Yucon FrameworkPlugin](https://www.roblox.com/library/5196221650/Yucon-Coding-Framework)
with a premade modularized system to make near perfect debug onscreen ui for simple and fast usage so you can focus more on scripting and now debugging

### Usage

After [DebugFramework](#debugframework) is installed open the plugin and add yourself using the "Whitelist" button then close it and press edit then add a new script and open the module and enjoy the plugin [Api Reference](#api)

## Subjects
[DebugFramework](#debugframework) Info about this plugin

[Usage](#usage) Usage for this plugin

[Install](#install) How to install [DebugFrameworkPlugin](https://www.roblox.com/library/9840069360/DebugFramework)

[API reference](#api) good presets and tips for making debug menus

## Install

in order to install [DebugFramework](#debugframework) you need to download the plugin
```
https://www.roblox.com/library/9840069360/DebugFramework
```
<br>


Example

 ```lua
local Module = {} 
local RS = game:GetService("RunService")
function Module.Run(Plr) 
	local UI = Module.Instance(Plr) 
	UI.Size = UDim2.new(0.089, 0,0.056, 0)
	UI.Name = script.Name
	UI.Position = UDim2.new(0,100,0,100)
	UI.TextScaled = true
	--Right here 
	RS.Heartbeat:Connect(function(dt)
		UI.Text = tostring(Plr.Character:WaitForChild("Humanoid").MoveDirection)
	end)
	
end 
function Module.Instance(Plr)
local UI = Instance.new("TextLabel")
UI.Parent = Plr.PlayerGui:FindFirstChild("DebugMenu(Admin)")
return UI
end
return Module 
```

## Api
