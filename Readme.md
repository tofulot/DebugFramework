# DebugFramework
[DebugFramework](https://www.roblox.com/library/9840069360/DebugFramework) is a plugin based off the [Yucon Framework](https://www.roblox.com/library/5196221650/Yucon-Coding-Framework)
with a premade modularized system to make near perfect debug onscreen ui for simple and fast usage so you can focus more on scripting and now debugging

### Usage


## Subjects
[DebugFramework](#DebugFramework) Info about this plugin
[Install](#install) How to install [DebugFramework](https://www.roblox.com/library/9840069360/DebugFramework)

## Install

in order to install [DebugFramework](#DebugFramework)

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
