local Flux = loadstring(game:HttpGet"https://raw.githubusercontent.com/dawid-scripts/UI-Libs/main/fluxlib.txt")()
local win = Flux:Window("Test", "Clicker Madness", Color3.fromRGB(25, 60, 150), Enum.KeyCode.LeftControl)
local ky = win:Tab("auto", "http://www.roblox.com/asset/?id=6023426915")
 
ky:Toggle("Auto Gems", "",false,function(x)
_G.Auto = x
while _G.Auto do wait()
for _, xd in pairs(game:GetService("Workspace").ScriptObjects:GetDescendants()) do
if xd.Name == "Decoration" then
game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = xd.CFrame
end
end
end
end)
 
ky:Toggle("Auto click", "",false,function(x)
_G.Auto = x
while _G.Auto do wait()
local A_1 = 100000
local Event = game:GetService("ReplicatedStorage").Aero.AeroRemoteServices.ClickService.Click
Event:FireServer(A_1)
 
end
end)
 
