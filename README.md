-- ScreenGui Settings
local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "LifeHub"
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- Main Frame
local MainFrame = Instance.new("Frame")
MainFrame.Name = "MainFrame"
MainFrame.Size = UDim2.new(0, 400, 0, 300)
MainFrame.Position = UDim2.new(0.5, -200, 0.5, -150)
MainFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
MainFrame.BorderSizePixel = 0
MainFrame.Parent = ScreenGui

-- Title
local Title = Instance.new("TextLabel")
Title.Name = "Title"
Title.Size = UDim2.new(1, 0, 0, 50)
Title.BackgroundTransparency = 1
Title.Text = "Life Hub"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.Font = Enum.Font.GothamBold
Title.TextSize = 24
Title.Parent = MainFrame

-- Tab Buttons
local Tab1Button = Instance.new("TextButton")
Tab1Button.Name = "Tab1Button"
Tab1Button.Size = UDim2.new(0, 100, 0, 30)
Tab1Button.Position = UDim2.new(0, 0, 0, 50)
Tab1Button.Text = "AuToFarm"
Tab1Button.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
Tab1Button.TextColor3 = Color3.fromRGB(255, 255, 255)
Tab1Button.Parent = MainFrame

local Tab2Button = Instance.new("TextButton")
Tab2Button.Name = "Tab2Button"
Tab2Button.Size = UDim2.new(0, 100, 0, 30)
Tab2Button.Position = UDim2.new(0, 100, 0, 50)
Tab2Button.Text = "TeLePort"
Tab2Button.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
Tab2Button.TextColor3 = Color3.fromRGB(255, 255, 255)
Tab2Button.Parent = MainFrame

-- Tab 1 (AuToFarm)
local Tab1Frame = Instance.new("Frame")
Tab1Frame.Name = "Tab1Frame"
Tab1Frame.Size = UDim2.new(1, 0, 1, -80)
Tab1Frame.Position = UDim2.new(0, 0, 0, 80)
Tab1Frame.BackgroundTransparency = 1
Tab1Frame.Visible = true
Tab1Frame.Parent = MainFrame

-- Button
local Button = Instance.new("TextButton")
Button.Name = "Button"
Button.Size = UDim2.new(0, 150, 0, 30)
Button.Position = UDim2.new(0, 20, 0, 10)
Button.Text = "Button"
Button.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
Button.TextColor3 = Color3.fromRGB(255, 255, 255)
Button.Parent = Tab1Frame

-- Toggle
local Toggle = Instance.new("TextButton")
Toggle.Name = "Toggle"
Toggle.Size = UDim2.new(0, 150, 0, 30)
Toggle.Position = UDim2.new(0, 20, 0, 50)
Toggle.Text = "Toggle: Off"
Toggle.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
Toggle.TextColor3 = Color3.fromRGB(255, 255, 255)
Toggle.Parent = Tab1Frame

-- Dropdown
local Dropdown = Instance.new("TextButton")
Dropdown.Name = "Dropdown"
Dropdown.Size = UDim2.new(0, 150, 0, 30)
Dropdown.Position = UDim2.new(0, 20, 0, 90)
Dropdown.Text = "Dropdown"
Dropdown.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
Dropdown.TextColor3 = Color3.fromRGB(255, 255, 255)
Dropdown.Parent = Tab1Frame

-- Toggle 2
local Toggle2 = Instance.new("TextButton")
Toggle2.Name = "Toggle2"
Toggle2.Size = UDim2.new(0, 150, 0, 30)
Toggle2.Position = UDim2.new(0, 20, 0, 130)
Toggle2.Text = "Toggle2: Off"
Toggle2.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
Toggle2.TextColor3 = Color3.fromRGB(255, 255, 255)
Toggle2.Parent = Tab1Frame

-- Tab 2 (TeLePort)
local Tab2Frame = Instance.new("Frame")
Tab2Frame.Name = "Tab2Frame"
Tab2Frame.Size = UDim2.new(1, 0, 1, -80)
Tab2Frame.Position = UDim2.new(0, 0, 0, 80)
Tab2Frame.BackgroundTransparency = 1
Tab2Frame.Visible = false
Tab2Frame.Parent = MainFrame

-- Dropdown (Tab 2)
local Dropdown2 = Instance.new("TextButton")
Dropdown2.Name = "Dropdown2"
Dropdown2.Size = UDim2.new(0, 150, 0, 30)
Dropdown2.Position = UDim2.new(0, 20, 0, 10)
Dropdown2.Text = "Dropdown2"
Dropdown2.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
Dropdown2.TextColor3 = Color3.fromRGB(255, 255, 255)
Dropdown2.Parent = Tab2Frame

-- Toggle (Tab 2)
local Toggle3 = Instance.new("TextButton")
Toggle3.Name = "Toggle3"
Toggle3.Size = UDim2.new(0, 150, 0, 30)
Toggle3.Position = UDim2.new(0, 20, 0, 50)
Toggle3.Text = "Toggle3: Off"
Toggle3.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
Toggle3.TextColor3 = Color3.fromRGB(255, 255, 255)
Toggle3.Parent = Tab2Frame

-- Tab Switching
Tab1Button.MouseButton1Click:Connect(function()
    Tab1Frame.Visible = true
    Tab2Frame.Visible = false
end)

Tab2Button.MouseButton1Click:Connect(function()
    Tab1Frame.Visible = false
    Tab2Frame.Visible = true
end)

-- Toggle Functions
local toggleState = false
Toggle.MouseButton1Click:Connect(function()
    toggleState = not toggleState
    Toggle.Text = toggleState and "Toggle: On" or "Toggle: Off"
end)

local toggle2State = false
Toggle2.MouseButton1Click:Connect(function()
    toggle2State = not toggle2State
    Toggle2.Text = toggle2State and "Toggle2: On" or "Toggle2: Off"
end)

local toggle3State = false
Toggle3.MouseButton1Click:Connect(function()
    toggle3State = not toggle3State
    Toggle3.Text = toggle3State and "Toggle3: On" or "Toggle3: Off"
end)
