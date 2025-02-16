local lib = loadstring(game:HttpGet"https://raw.githubusercontent.com/dawid-scripts/UI-Libs/main/Vape.txt")()

local win = lib:Window("POOM HUB",Color3.fromRGB(44, 120, 224), Enum.KeyCode.RightControl)

local tab1 = win:Tab("General")
local tab2 = win:Tab("Teleport")
local tab3 = win:Tab("items")
local tab4 = win:Tab("Visc")
local tab5 = win:Tab("UI")

tab1:Button("ReDeemCodeX", function(a)

end)

tab1:Toggle("AuToFarm",false, function(b)
print(b)
end)

tab1:Toggle("Fast Attack",true, function(fat)
print(fat)
end)

tab1:Dropdown("Select Up-Stats",{"Melee","Defense","Sword","Gun","Fruit"}, function(d)
_G.upstats = d
end)

tab1:Toggle("start",false, function(z)
if _G.upstats == "Melee" then

local args = {
    [1] = "AddPoint",
    [2] = "Melee",
    [3] = 9999999999
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

elseif _G.upstats == "Defense" then

local args = {
    [1] = "AddPoint",
    [2] = "Defense",
    [3] = 9999999999
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

elseif _G.upstats == "Sword" then

 local args = {
    [1] = "AddPoint",
    [2] = "Sword",
    [3] = 9999999999
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

elseif _G.upstats == "Gun" then

local args = {
    [1] = "AddPoint",
    [2] = "Gun",
    [3] = 9999999999
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

elseif _G.upstats == "Fruit" then

local args = {
    [1] = "AddPoint",
    [2] = "Demon Fruit",
    [3] = 9999999999
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    
end
end)

tab1:Toggle("White Screen",true, function(ws)

_G.whitescreen = ws

local whiteFrame = Instance.new("Frame")
whiteFrame.Size = UDim2.new(1, 0, 1, 0)
whiteFrame.Position = UDim2.new(0, 0, 0, 0)
whiteFrame.BackgroundColor3 = Color3.new(1, 1, 1)
whiteFrame.Visible = false
whiteFrame.ZIndex = 9999
whiteFrame.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
local function checkWhiteScreen()
    if _G.whitescreen == true then
        whiteFrame.Visible = true
    else
        whiteFrame.Visible = false
    end
end
while wait(0.1) do
    checkWhiteScreen()
end
end)

tab5:Colorpicker("Change UI Color",Color3.fromRGB(44, 120, 224), function(t)
lib:ChangePresetColor(Color3.fromRGB(t.R * 255, t.G * 255, t.B * 255))
end)

tab5:Button("Close Ui", function(cui)

end)
