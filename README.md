local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()

local Window = Fluent:CreateWindow({
    Title = "Steam Hub [Beta]",
    SubTitle = "True V0.23",
    TabWidth = 160,
    Size = UDim2.fromOffset(480, 340),
    Acrylic = false, -- The blur may be detectable, setting this to false disables blur entirely
    Theme = "Darker",
    MinimizeKey = Enum.KeyCode.LeftControl -- Used when theres no MinimizeKeybind
})

local Tabs = {
    Main = Window:AddTab({ Title = "+Tab Combat", Icon = "" })
}


    
Tabs.Main:AddButton({
        Title = "Auto Parry ",
        Description = "Good auto parry,Click X For Spam and Z for Normal ",
        Callback = function()  
getgenv().visualizer = false
loadstring(game:HttpGet("https://raw.githubusercontent.com/1f0yt/community/main/RedCircleBlock"))()
      print("Executed")         
        end
    })

    Tabs.Main:AddButton({
        Title = "Visual Part(can make bug)",
        Description = "Visual part",
        Callback = function()  
getgenv().visualizer = true
loadstring(game:HttpGet("https://raw.githubusercontent.com/1f0yt/community/main/RedCircleBlock"))()
      print("Executed")         
        end
    })

Tabs.Main:AddButton({
        Title = "Manual Spam",
        Description = "Good spam it's recommend for mobile",
        Callback = function()  
      print("Executed")        gui, frame, button = Instance.new("ScreenGui", game.CoreGui), Instance.new("Frame"), Instance.new("TextButton")
gui.ResetOnSpawn = false
frame.Size, frame.Position, frame.BackgroundColor3, frame.BorderSizePixel, frame.Active, frame.Draggable, frame.Parent = UDim2.new(0, 150, 0, 75), UDim2.new(0, 10, 0, 10), Color3.new(0, 0, 0), 0, true, true, gui
button.Text, button.Size, button.Position, button.BackgroundColor3, button.BorderColor3, button.BorderSizePixel, button.Font, button.TextColor3, button.TextSize, button.Parent = "Manual spam", UDim2.new(1, -20, 1, -20), UDim2.new(0, 10, 0, 10), Color3.new(0, 0, 0), Color3.new(), 2, Enum.Font.SourceSans, Color3.new(1, 1, 1), 16, frame

local activated = false

local function toggle()
    activated, button.Text = not activated, activated and "Off" or "On"
    
    while activated do
        local args = {1.5, CFrame.new(-254.29, 112.14, -119.27) * CFrame.Angles(-2.03, 0.57, 2.31), {["2617721424"] = Vector3.new(-273.40, -724.80, -20.92)}, {910, 154}}
        game:GetService("ReplicatedStorage").Remotes.ParryAttempt:FireServer(unpack(args))
        game:GetService("RunService").Heartbeat:Wait()
        button.BorderColor3 = Color3.new(math.random(), math.random(), math.random())
    end
end

local function showNotification()
    game.StarterGui:SetCore("SendNotification", {Title = "Manual Spam", Text = "Manual spam", Duration = 5})
end

button.MouseButton1Click:Connect(function()
    toggle()
    showNotification()
end)     
        end
    })

