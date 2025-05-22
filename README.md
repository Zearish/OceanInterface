# OceanInterface
A OceanSplash documentary where you can use OceanSplash for your scripts
## Using the UI
This is how you can use OceanSplash, and you have to add this on top of all your code.
```lua
local OceanSplashLib = {}
OceanSplashLib.__index = OceanSplashLib
function OceanSplashLib.new(title)
    local self = setmetatable({}, OceanSplashLib)
    self.gui = Instance.new("ScreenGui")
    self.gui.Name = "OceanSplash"
    self.gui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling 
    if syn and syn.protect_gui then
        syn.protect_gui(self.gui)
        self.gui.Parent = game:GetService("CoreGui")
    elseif gethui then
        self.gui.Parent = gethui()
    else
        self.gui.Parent = game:GetService("CoreGui")
    end
    self.mainFrame = Instance.new("Frame")
    self.mainFrame.Name = "MainFrame"
    self.mainFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    self.mainFrame.BackgroundTransparency = 1.000
    self.mainFrame.BorderColor3 = Color3.fromRGB(0, 0, 0)
    self.mainFrame.BorderSizePixel = 0
    self.mainFrame.Position = UDim2.new(0.329271823, 0, 0.219054237, 0)
    self.mainFrame.Size = UDim2.new(0, 462, 0, 49)
    self.mainFrame.Parent = self.gui
    self.topbarUpper = Instance.new("Frame")
    self.topbarUpper.Name = "TopbarUpper"
    self.topbarUpper.BackgroundColor3 = Color3.fromRGB(95, 115, 145)
    self.topbarUpper.BorderColor3 = Color3.fromRGB(0, 0, 0)
    self.topbarUpper.BorderSizePixel = 0
    self.topbarUpper.Position = UDim2.new(-0.0167065896, 0, -0.012017386, 0)
    self.topbarUpper.Size = UDim2.new(0, 471, 0, 33)
    self.topbarUpper.Parent = self.mainFrame
    self.topBarBottom = Instance.new("Frame")
    self.topBarBottom.Name = "TopBarBottom"
    self.topBarBottom.BackgroundColor3 = Color3.fromRGB(95, 115, 145)
    self.topBarBottom.BorderColor3 = Color3.fromRGB(0, 0, 0)
    self.topBarBottom.BorderSizePixel = 0
    self.topBarBottom.Position = UDim2.new(-0.000479728566, 0, 0.617966652, 0)
    self.topBarBottom.Size = UDim2.new(0, 471, 0, 33)
    self.topBarBottom.Parent = self.topbarUpper
    local uiCorner = Instance.new("UICorner")
    uiCorner.CornerRadius = UDim.new(0, 15)
    uiCorner.Parent = self.topbarUpper
    self.bodyUpper = Instance.new("Frame")
    self.bodyUpper.Name = "BodyUpper"
    self.bodyUpper.BackgroundColor3 = Color3.fromRGB(69, 84, 106)
    self.bodyUpper.BorderColor3 = Color3.fromRGB(0, 0, 0)
    self.bodyUpper.BorderSizePixel = 0
    self.bodyUpper.Position = UDim2.new(-0.0167065617, 0, 1.07763362, 0)
    self.bodyUpper.Size = UDim2.new(0, 471, 0, 253)
    self.bodyUpper.Parent = self.mainFrame
    self.bodyBottom = Instance.new("Frame")
    self.bodyBottom.Name = "BodyBottom"
    self.bodyBottom.BackgroundColor3 = Color3.fromRGB(69, 84, 106)
    self.bodyBottom.BorderColor3 = Color3.fromRGB(0, 0, 0)
    self.bodyBottom.BorderSizePixel = 0
    self.bodyBottom.Position = UDim2.new(-0.000479728566, 0, 0.922314644, 0)
    self.bodyBottom.Size = UDim2.new(0, 471, 0, 34)
    self.bodyBottom.Parent = self.bodyUpper
    local uiCorner2 = Instance.new("UICorner")
    uiCorner2.CornerRadius = UDim.new(0, 15)
    uiCorner2.Parent = self.bodyBottom
    self.home = Instance.new("Frame")
    self.home.Name = "Home"
    self.home.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    self.home.BackgroundTransparency = 1.000
    self.home.BorderColor3 = Color3.fromRGB(0, 0, 0)
    self.home.BorderSizePixel = 0
    self.home.Position = UDim2.new(0.0445859879, 0, 0.0632411093, 0)
    self.home.Size = UDim2.new(0, 430, 0, 237)
    self.home.Parent = self.bodyUpper
    self.scrollFrame = Instance.new("ScrollingFrame")
    self.scrollFrame.Name = "InsideHomeTab"
    self.scrollFrame.Active = true
    self.scrollFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    self.scrollFrame.BackgroundTransparency = 1.000
    self.scrollFrame.BorderColor3 = Color3.fromRGB(0, 0, 0)
    self.scrollFrame.BorderSizePixel = 0
    self.scrollFrame.Size = UDim2.new(0, 430, 0, 236)
    self.scrollFrame.ScrollBarThickness = 5
    self.scrollFrame.Parent = self.home
    local uiListLayout = Instance.new("UIListLayout")
    uiListLayout.Parent = self.scrollFrame
    uiListLayout.SortOrder = Enum.SortOrder.LayoutOrder
    uiListLayout.Padding = UDim.new(0, 10)
    local uiPadding = Instance.new("UIPadding")
    uiPadding.Parent = self.scrollFrame
    uiPadding.PaddingBottom = UDim.new(0, 10)
    uiPadding.PaddingLeft = UDim.new(0, 10)
    uiPadding.PaddingRight = UDim.new(0, 10)
    uiPadding.PaddingTop = UDim.new(0, 10)
    self.oceanSplashIcon = Instance.new("ImageLabel")
    self.oceanSplashIcon.Name = "OceanSplashIcon"
    self.oceanSplashIcon.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    self.oceanSplashIcon.BackgroundTransparency = 1.000
    self.oceanSplashIcon.BorderColor3 = Color3.fromRGB(0, 0, 0)
    self.oceanSplashIcon.BorderSizePixel = 0
    self.oceanSplashIcon.Position = UDim2.new(0.00216450216, 0, 0.122448981, 0)
    self.oceanSplashIcon.Size = UDim2.new(0, 39, 0, 37)
    self.oceanSplashIcon.Image = "rbxassetid://89403502749754"
    self.oceanSplashIcon.Parent = self.mainFrame
    self.titleLabel = Instance.new("TextLabel")
    self.titleLabel.Name = "OceanSplash"
    self.titleLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    self.titleLabel.BackgroundTransparency = 1.000
    self.titleLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
    self.titleLabel.BorderSizePixel = 0
    self.titleLabel.Position = UDim2.new(0.0995671004, 0, 0.261307061, 0)
    self.titleLabel.Size = UDim2.new(0, 305, 0, 23)
    self.titleLabel.Font = Enum.Font.GothamBold
    self.titleLabel.Text = title or "OceanSplash"
    self.titleLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
    self.titleLabel.TextScaled = true
    self.titleLabel.TextSize = 14.000
    self.titleLabel.TextWrapped = true
    self.titleLabel.TextXAlignment = Enum.TextXAlignment.Left
    self.titleLabel.Parent = self.mainFrame
    self.closeButton = Instance.new("TextButton")
    self.closeButton.Name = "Close"
    self.closeButton.BackgroundColor3 = Color3.fromRGB(255, 170, 170)
    self.closeButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
    self.closeButton.BorderSizePixel = 0
    self.closeButton.Position = UDim2.new(0.919913471, 0, 0.302123398, 0)
    self.closeButton.Size = UDim2.new(0, 19, 0, 19)
    self.closeButton.AutoButtonColor = false
    self.closeButton.Font = Enum.Font.SourceSans
    self.closeButton.Text = ""
    self.closeButton.TextColor3 = Color3.fromRGB(255, 120, 120)
    self.closeButton.TextSize = 14.000
    self.closeButton.Parent = self.mainFrame
    local uiCorner7 = Instance.new("UICorner")
    uiCorner7.CornerRadius = UDim.new(0, 3434234)
    uiCorner7.Parent = self.closeButton
    self.closeButton.MouseButton1Down:Connect(function()
        self.gui:Destroy()
    end)
    self.minifyButton = Instance.new("TextButton")
    self.minifyButton.Name = "Minify"
    self.minifyButton.BackgroundColor3 = Color3.fromRGB(255, 214, 149)
    self.minifyButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
    self.minifyButton.BorderSizePixel = 0
    self.minifyButton.Position = UDim2.new(0.854978383, 0, 0.302123398, 0)
    self.minifyButton.Size = UDim2.new(0, 19, 0, 19)
    self.minifyButton.AutoButtonColor = false
    self.minifyButton.Font = Enum.Font.SourceSans
    self.minifyButton.Text = ""
    self.minifyButton.TextColor3 = Color3.fromRGB(255, 120, 120)
    self.minifyButton.TextSize = 14.000
    self.minifyButton.Parent = self.mainFrame
    local uiCorner8 = Instance.new("UICorner")
    uiCorner8.CornerRadius = UDim.new(0, 3434234)
    uiCorner8.Parent = self.minifyButton
    self.minifyButton.MouseButton1Down:Connect(function()
        self.bodyUpper.Visible = not self.bodyUpper.Visible
    end)
    self.mobileCloseButton = Instance.new("TextButton")
    self.mobileCloseButton.Name = "MobileClose"
    self.mobileCloseButton.BackgroundColor3 = Color3.fromRGB(192, 250, 255)
    self.mobileCloseButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
    self.mobileCloseButton.BorderSizePixel = 0
    self.mobileCloseButton.Position = UDim2.new(0.792207778, 0, 0.302123398, 0)
    self.mobileCloseButton.Size = UDim2.new(0, 19, 0, 19)
    self.mobileCloseButton.Visible = false
    self.mobileCloseButton.AutoButtonColor = false
    self.mobileCloseButton.Font = Enum.Font.SourceSans
    self.mobileCloseButton.Text = ""
    self.mobileCloseButton.TextColor3 = Color3.fromRGB(255, 120, 120)
    self.mobileCloseButton.TextSize = 14.000
    self.mobileCloseButton.Parent = self.mainFrame
    local uiCorner9 = Instance.new("UICorner")
    uiCorner9.CornerRadius = UDim.new(0, 3434234)
    uiCorner9.Parent = self.mobileCloseButton
    self.mobileToggleButton = Instance.new("ImageButton")
    self.mobileToggleButton.Name = "MobileToggle"
    self.mobileToggleButton.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
    self.mobileToggleButton.BackgroundTransparency = 0.600
    self.mobileToggleButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
    self.mobileToggleButton.BorderSizePixel = 0
    self.mobileToggleButton.Position = UDim2.new(0.867395401, 0, 0.135605007, 0)
    self.mobileToggleButton.Size = UDim2.new(0, 63, 0, 63)
    self.mobileToggleButton.Visible = false
    self.mobileToggleButton.AutoButtonColor = false
    self.mobileToggleButton.Image = "rbxassetid://89403502749754"
    self.mobileToggleButton.ImageColor3 = Color3.fromRGB(165, 211, 255)
    self.mobileToggleButton.Parent = self.gui
    local uiCorner10 = Instance.new("UICorner")
    uiCorner10.CornerRadius = UDim.new(0, 123213)
    uiCorner10.Parent = self.mobileToggleButton
    self.mobileCloseButton.MouseButton1Down:Connect(function()
        self.mobileToggleButton.Visible = not self.gui.Enabled
        self.gui.Enabled = not self.gui.Enabled
    end)
    local dragScript = Instance.new("LocalScript", self.mainFrame)
    dragScript.Source = "script.Parent.Draggable = true; script.Parent.Active = true"
    local keybindScript = Instance.new("LocalScript", self.mainFrame)
    keybindScript.Source = [[
        game:GetService("UserInputService").InputBegan:Connect(function(input, gameProcessed)
            if not gameProcessed and input.KeyCode == Enum.KeyCode.Y then
                script.Parent.Visible = not script.Parent.Visible
            end
        end)
    ]]
    return self
end
function OceanSplashLib:CreateToggle(name, callback)
    local toggle = Instance.new("TextButton")
    toggle.Name = "Toggle_" .. name
    toggle.BackgroundColor3 = Color3.fromRGB(169, 218, 255)
    toggle.BorderColor3 = Color3.fromRGB(0, 0, 0)
    toggle.BorderSizePixel = 0
    toggle.Size = UDim2.new(0, 26, 0, 26)
    toggle.AutoButtonColor = false
    toggle.Font = Enum.Font.SourceSans
    toggle.Text = ""
    toggle.TextColor3 = Color3.fromRGB(0, 0, 0)
    toggle.TextSize = 14.000
    toggle.Parent = self.scrollFrame
    local uiCorner = Instance.new("UICorner")
    uiCorner.CornerRadius = UDim.new(0, 453454)
    uiCorner.Parent = toggle
    local nameLabel = Instance.new("TextLabel")
    nameLabel.Name = "ToggleNameHere"
    nameLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    nameLabel.BackgroundTransparency = 1.000
    nameLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
    nameLabel.BorderSizePixel = 0
    nameLabel.Position = UDim2.new(1.25840175, 0, 0.115384616, 0)
    nameLabel.Size = UDim2.new(0, 367, 0, 20)
    nameLabel.Font = Enum.Font.GothamBold
    nameLabel.Text = name or "Toggle Name"
    nameLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
    nameLabel.TextScaled = true
    nameLabel.TextSize = 14.000
    nameLabel.TextWrapped = true
    nameLabel.TextXAlignment = Enum.TextXAlignment.Left
    nameLabel.Parent = toggle
    local toggleEnabled = false
    toggle.MouseButton1Down:Connect(function()
        toggleEnabled = not toggleEnabled
        toggle.BackgroundColor3 = toggleEnabled and Color3.fromRGB(255, 255, 255) or Color3.fromRGB(169, 218, 255)
        if callback then
            callback(toggleEnabled)
        end
    end)
    return toggle
end
function OceanSplashLib:CreateButton(name, callback)
    local button = Instance.new("TextButton")
    button.Name = "Button_" .. name
    button.BackgroundColor3 = Color3.fromRGB(149, 209, 255)
    button.BorderColor3 = Color3.fromRGB(0, 0, 0)
    button.BorderSizePixel = 0
    button.Size = UDim2.new(0, 400, 0, 30)
    button.AutoButtonColor = false
    button.Font = Enum.Font.GothamBold
    button.Text = name or "Button Name"
    button.TextColor3 = Color3.fromRGB(255, 255, 255)
    button.TextSize = 20.000
    button.TextWrapped = true
    button.TextXAlignment = Enum.TextXAlignment.Left
    button.Parent = self.scrollFrame
    local uiCorner = Instance.new("UICorner")
    uiCorner.CornerRadius = UDim.new(0, 15)
    uiCorner.Parent = button
    local uiPadding = Instance.new("UIPadding")
    uiPadding.Parent = button
    uiPadding.PaddingLeft = UDim.new(0, 15)
    button.MouseButton1Down:Connect(function()
        if callback then
            callback()
        end
    end)
    return button
end
function OceanSplashLib:CreateTextBox(placeholder, buttonText, callback)
    local textbox = Instance.new("TextBox")
    textbox.Name = "TextBox_" .. placeholder
    textbox.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
    textbox.BackgroundTransparency = 0.600
    textbox.BorderColor3 = Color3.fromRGB(0, 0, 0)
    textbox.BorderSizePixel = 0
    textbox.Size = UDim2.new(0, 260, 0, 28)
    textbox.ClearTextOnFocus = false
    textbox.Font = Enum.Font.GothamBold
    textbox.PlaceholderText = placeholder or "Textbox Placeholder Name Goes Here"
    textbox.Text = ""
    textbox.TextColor3 = Color3.fromRGB(190, 238, 255)
    textbox.TextScaled = true
    textbox.TextSize = 17.000
    textbox.TextWrapped = true
    textbox.Parent = self.scrollFrame
    local uiCorner = Instance.new("UICorner")
    uiCorner.CornerRadius = UDim.new(0, 2423434)
    uiCorner.Parent = textbox
    local button = Instance.new("TextButton")
    button.Name = "TextboxButton"
    button.BackgroundColor3 = Color3.fromRGB(149, 209, 255)
    button.BorderColor3 = Color3.fromRGB(0, 0, 0)
    button.BorderSizePixel = 0
    button.Position = UDim2.new(1.04240954, 0, -0.0714285746, 0)
    button.Size = UDim2.new(0, 130, 0, 31)
    button.AutoButtonColor = false
    button.Font = Enum.Font.GothamBold
    button.Text = buttonText or "Textbox Set Button Name"
    button.TextColor3 = Color3.fromRGB(255, 255, 255)
    button.TextScaled = true
    button.TextSize = 20.000
    button.TextWrapped = true
    button.Parent = textbox
    local uiCorner2 = Instance.new("UICorner")
    uiCorner2.CornerRadius = UDim.new(0, 15)
    uiCorner2.Parent = button
    button.MouseButton1Down:Connect(function()
        if callback then
            callback(textbox.Text)
        end
    end)
    return textbox
end
function OceanSplashLib:SetTitle(title)
    self.titleLabel.Text = title
end
function OceanSplashLib:SetIcon(iconId)
    self.oceanSplashIcon.Image = iconId
    if self.mobileToggleButton then
        self.mobileToggleButton.Image = iconId
    end
end
function OceanSplashLib:Destroy()
    self.gui:Destroy()
end
function OceanSplashLib:Toggle(visible)
    self.mainFrame.Visible = visible
end
```
## Adding Modules
Once you're done with that, you can now add toggles, buttons, and inputs (or just textboxes)
### Creating Toggles
To create toggles, you can by doing this, callback can either be true or false, you can add code that plays if callback is either true or false.
```lua
OceanUI:CreateToggle("Toggle", function(callback)
    if callback then
        -- code that plays if toggle is true
    else
        -- code that plays if toggle is false
    end
end)
```
### Creating buttons
Buttons are like toggles, exept, they run code ONCE when you click them. Heres how you can add a button
```lua
OceanUI:CreateButton("Button", function()
    -- code that plays if button is pressed
end)
```
### Creating Textboxes
Textboxes can change a value of something. Heres how you can use them.

I also forgot to say, for textboxes to run, you have to click a button beside them :)
```lua
OceanUI:CreateTextBox("Textbox", "Set textbox", function(value)
    -- idk
end)
```
