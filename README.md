local cpos = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame

local stuff = workspace:getDescendants()
for i=1,#stuff do
if stuff[i].Name == "Block" and stuff[i].Parent.Name == "Ores" then
repeat
wait()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = stuff[i].CFrame
game.Players.LocalPlayer.Character.Axe.RemoteEvent:FireServer(stuff[i])
until stuff[i].Name ~= "Block" or not game.Players.LocalPlayer.Character:findFirstChild("Axe")
end
end

game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = cpos
