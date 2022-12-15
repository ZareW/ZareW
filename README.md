
if game.PlaceId == 9183932460 then
local UILib = loadstring(game:HttpGet('https://raw.githubusercontent.com/inceldom/kinx/main/ui'))()

local win = UILib:Window("NTime",Color3.fromRGB(255, 255, 255), Enum.KeyCode.V)


local A4 = win:Tab("AntiAiming")
local A1 = win:Tab("Movement")
local A6 = win:Tab("Toggles")
local A2 = win:Tab("Target")
local A3 = win:Tab("Aiming")
local A7 = win:Tab("Visual")
local A5 = win:Tab("Other")
local A8 = win:Tab("Settings")
------------------------------------------------------------------------------------------
A1:Button("Flight(X)", function()
loadstring(game:HttpGet("https://pastebin.com/raw/gg0LV6a1",true))()
end)

A1:Button("CFrame(L)", function()
loadstring(game:HttpGet("https://pastebin.com/raw/HSTMXhrb",true))()
end)

A1:Button("SpeedTool", function()
getgenv().Suicide = false
getgenv().Speed = true
getgenv().FakeMacro = false
getgenv().ClickTp = false
loadstring(game:HttpGet("https://raw.githubusercontent.com/Allvideo/nukermode/main/Kit%20tools.txt",true))()
end)
------------------------------------------------------------------------------------------
A2:Textbox("Victim : Can Be Shortened",true, function(t)
_G.Victim = t
end)

A2:Toggle("Strafe",false, function(t)
local player = game.Players.LocalPlayer
for i,v in pairs(game.Players:GetChildren()) do
if (string.sub(string.lower(v.Name),1,string.len(_G.Victim))) == string.lower(_G.Victim) then
_G.Victim = v.Name
end
end
getgenv().u = t

local target = _G.Victim

while getgenv().u == true do
    task.wait()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[target].Character.HumanoidRootPart.CFrame * CFrame.new(0, 14, 0)
end 
end)


A2:Button("Teleport To", function()
local player = game.Players.LocalPlayer
for i,v in pairs(game.Players:GetChildren()) do
if (string.sub(string.lower(v.Name),1,string.len(_G.Victim))) == string.lower(_G.Victim) then
_G.Victim = v.Name
end
end
local p1 = game.Players.LocalPlayer.Character.HumanoidRootPart
local p2 = _G.Victim

p1.CFrame = game.Players[p2].Character.HumanoidRootPart.CFrame
end)

A2:Button("Save", function()
local player = game.Players.LocalPlayer
for i,v in pairs(game.Players:GetChildren()) do
if (string.sub(string.lower(v.Name),1,string.len(_G.Victim))) == string.lower(_G.Victim) then
_G.Victim = v.Name
end
end
local p1 = game.Players.LocalPlayer.Character.HumanoidRootPart
local p2 = _G.Victim
local pos = p1.CFrame

p1.CFrame = game.Players[p2].Character.HumanoidRootPart.CFrame

wait(0.50)

local args = {
    [1] = "Grabbing",
    [2] = true
}

game:GetService("ReplicatedStorage"):FindFirstChild(".gg/untitledhood"):FireServer(unpack(args))

wait(0.1)

p1.CFrame = pos

end)

------------------------------------------------------------------------------------------
A3:Button("Aim", function()
loadstring(game:HttpGet("https://pastebin.com/raw/u7gyhrMf",true))()
end)

A3:Textbox("Key",true, function(t)
_G.Key = t
end)

A3:Textbox("Prediction",true, function(t)
_G.Prediction = t
end)

A3:Dropdown("AimPart",{"Head", "UpperTorso", "HumanoidRootPart", "LowerTorso", "LeftHand", "RightHand", "LeftLowerArm", "RightLowerArm", "LeftUpperArm", "RightUpperArm", "LeftFoot", "LeftLowerLeg",  "LeftUpperLeg", "RightLowerLeg", "RightFoot",  "RightUpperLeg"}, function(t)
_G.Part = t
end)

------------------------------------------------------------------------------------------
A4:Button("Oblivity Desync[T]", function()
loadstring(game:HttpGet("https://pastebin.com/raw/QbasXrpg",true))()
end)

A4:Button("UnderAntiLock[Y]", function()
loadstring(game:HttpGet("https://pastebin.com/raw/pKFm66Ev",true))()
end)

A4:Button("KavoAA[N]", function()
loadstring(game:HttpGet("https://pastebin.com/raw/Wk5mk1RW",true))()
end)

A4:Toggle("AntiAim",false, function(t)
getgenv().SemiRageAA = t
getgenv().BlatantAA = t

loadstring(game:HttpGet("https://pastebin.com/raw/GNQB8iPa",true))()
end)

A4:Toggle("BlatantAA",false, function(t)
getgenv().BlatantAA = t

local Position = game.Players.LocalPlayer.Character.HumanoidRootPart.Position
while getgenv().BlatantAA == true  do
    task.wait()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = (CFrame.new(Position) + Vector3.new(math.random(-15, 15), math.random(-15, 15), math.random(-15, 15))) * CFrame.Angles(math.rad(math.random(-180, 180)), math.rad(math.random(-180, 180)), math.rad(math.random(-180, 180)))
end
end)
------------------------------------------------------------------------------------------
A5:Button("Loot AirDrop", function()
local p1 = game.Players.LocalPlayer.Character.HumanoidRootPart
local pos = p1.CFrame

wait(0.000001)

game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(game:GetService("Workspace").Ignored.Airdrops.Airdrop.Crate.position)

wait(0.000001)

if fireproximityprompt then
		for i,v in pairs(workspace:GetDescendants()) do
			if v:IsA("ProximityPrompt") then
				fireproximityprompt(v)
			end
		end
  end

wait(0.0000001)

p1.CFrame = pos

end)
------------------------------------------------------------------------------------------
A6:Toggle("Auto Stomp",false, function(t)
AutoStomp = t
while AutoStomp do
wait(0.0001)
-- Script generated by SimpleSpy - credits to exx#9394

local args = {
    [1] = "Stomp"
}

game:GetService("ReplicatedStorage"):FindFirstChild(".gg/untitledhood"):FireServer(unpack(args))
end
end)
------------------------------------------------------------------------------------------
A7:Textbox("Fov",true, function(t)
Workspace.CurrentCamera.FieldOfView = t
end)
------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------
A8:Button("Rejoin", function()
local ts = game:GetService("TeleportService")
local p = game:GetService("Players").LocalPlayer
ts:Teleport(game.PlaceId, p)
end)

A8:Button("ServerHop", function()
loadstring(game:HttpGet("https://pastebin.com/raw/x0QqWgDx",true))()
end)

A8:Button("Exit The Game", function()
game:Shutdown()
end)
------------------------------------------------------------------------------------------

wait(0.01)

UILib:Notification("Notification", "Keybind Is V", "Okay")    

wait(0.01)

if game.PlaceId == 2636441885 then
local UILib = loadstring(game:HttpGet('https://raw.githubusercontent.com/inceldom/kinx/main/ui'))()

local win = UILib:Window("NTime",Color3.fromRGB(255, 255, 255), Enum.KeyCode.V)

local A1 = win:Tab("Farm")
local A2 = win:Tab("Crate")
local A3 = win:Tab("Trade")

A1:Toggle("Trillionaire City Farm",false, function(t)
TF = t
while TF do
wait(0.1)
if game:GetService("Workspace").TrillionaireCity.TrillionaireOrbs:FindFirstChild("Trillionaire") then 
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(game:GetService("Workspace").TrillionaireCity.TrillionaireOrbs.Trillionaire.Outside.Position)
end
end
end)

A1:Toggle("Ghost City White Orb Farm",false, function(t)
GWF = t
while GWF do
wait(0.1)
   if game:GetService("Workspace").GhostCity.GhostOrbsMega:FindFirstChild("GhostMega") then 
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(game:GetService("Workspace").GhostCity.GhostOrbsMega.GhostMega.Outside.Position)
end
end
end)

A1:Toggle("Ghost City Black Orb Farm",false, function(t)
GBF = t
while GBF do
wait(0.1)
if game:GetService("Workspace").GhostCity.GhostOrbsMega:FindFirstChild("GhostMega2") then 
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(game:GetService("Workspace").GhostCity.GhostOrbsMega.GhostMega2.Outside.Position)
end
end
end)

A2:Toggle("Happy Ghost Crate",false, function(t)
HGC = t
while HGC do
wait(0.1)
if game:GetService("Workspace").GhostCity.GhostOrbsMega:FindFirstChild("Happy") then 
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(game:GetService("Workspace").GhostCity.GhostOrbsMega.Happy.Crate.Position)
end
end
end)

A2:Toggle("Zombie Ghost Crate", function(t)
ZGC = t
while ZGC do
wait(0.1)
if game:GetService("Workspace").GhostCity.GhostOrbsMega:FindFirstChild("Zombie Ghost") then 
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(game:GetService("Workspace").GhostCity.GhostOrbsMega["Zombie Ghost"].Crate.Position)
end
end
end)

A2:Toggle("King Ghost Crate",false, function(t)
KGC = t
while KGC do
wait(0.1)
if game:GetService("Workspace").GhostCity.GhostOrbsMega:FindFirstChild("King Ghost") then 
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(game:GetService("Workspace").GhostCity.GhostOrbsMega["King Ghost"].Crate.Position)
end
end
end)

A3:Textbox("Trail Name",true, function(t)
_G.TN = t
end)

A3:Button("Add Trail", function()
-- Script generated by SimpleSpy - credits to exx#9394

local args = {
    [1] = _G.TN
}

game:GetService("ReplicatedStorage").TradeTrailAdd:FireServer(unpack(args))
end)

A3:Button("PutBack Trail", function()
-- Script generated by SimpleSpy - credits to exx#9394

local args = {
    [1] = _G.TN
}

game:GetService("ReplicatedStorage").TradeTrailPutBack:FireServer(unpack(args))
end)

A3:Button("Accept Trade", function()
-- Script generated by SimpleSpy - credits to exx#9394

game:GetService("ReplicatedStorage").TradeMenuAccept:FireServer()
end)

A3:Button("Cancel Trade", function()
-- Script generated by SimpleSpy - credits to exx#9394

game:GetService("ReplicatedStorage").TradeMenuCancel:FireServer()
end)
------------------------------------------------------------------------------------------

wait(0.1)

for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.Idled)) do
    v:Disable()
end

wait(0.1)

local vu = game:GetService("VirtualUser")
	game:GetService("Players").LocalPlayer.Idled:connect(function()
		vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
		wait(1)
		vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
	end)
	
	wait(4)
	
	UILib:Notification("Notification", "Keybind Is V", "Okay")    
