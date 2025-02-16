local lib = loadstring(game:HttpGet"https://raw.githubusercontent.com/dawid-scripts/UI-Libs/main/Vape.txt")()

local win = lib:Window("PREVIEW",Color3.fromRGB(44, 120, 224), Enum.KeyCode.RightControl)

local tab1 = win:Tab("General")
local tab2 = win:Tab("Teleport")
local tab3 = win:Tab("items")
local tab4 = win:Tab("Visc")
local tab5 = win:Tab("Change UI Color")

tab1:Button("ReDeemCodeX", function(a)

end)

tab1:Toggle("AuToFarm",false, function(b)
print(b)
end)

tab1:Dropdown("upstats",{"Melee","Defense","Sword","Gun","Fruit"}, function(d)
_G.upstats = d
end)

tab1:Textbox("Value of stats",true, function(c)
_G.ws = c
end)

tab1:Toggle("start",false, function(z)
if _G.upstats == "Melee" then

local args = {
    [1] = "AddPoint",
    [2] = "Melee",
    [3] = 1
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

elseif _G.upstats == "Defense" then

local args = {
    [1] = "AddPoint",
    [2] = "Defense",
    [3] = 1
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

elseif _G.upstats == "Sword" then

 local args = {
    [1] = "AddPoint",
    [2] = "Sword",
    [3] = 1
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

elseif _G.upstats == "Gun" then

local args = {
    [1] = "AddPoint",
    [2] = "Gun",
    [3] = 1
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

elseif _G.upstats == "Fruit" then

local args = {
    [1] = "AddPoint",
    [2] = "Demon Fruit",
    [3] = 1
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    
end
end)

tab1:Colorpicker("Colorpicker",Color3.fromRGB(255,0,0), function(e)
print(e)
end)

tab1:Textbox("White Screen",true, function(f)
_G.ws = f
end)

tab1:Bind("Bind",Enum.KeyCode.RightShift, function(g)
print(g)
end)

tab1:Label("Label")

tab5:Colorpicker("Change UI Color",Color3.fromRGB(44, 120, 224), function(t)
lib:ChangePresetColor(Color3.fromRGB(t.R * 255, t.G * 255, t.B * 255))
end)
