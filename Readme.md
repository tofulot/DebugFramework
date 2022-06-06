## How to start

example
'''
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
'''
