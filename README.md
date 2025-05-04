local Window = WindUI:CreateWindow({
    Title = "WindUI Library",
    Icon = "door-open",
    Author = "Example UI",
    Folder = "CloudHub",
    Size = UDim2.fromOffset(580, 460),
    Transparent = true,
    Theme = "Dark",
    UserEnabled = false,
    SideBarWidth = 200,
    --Background = "rbxassetid://13511292247", -- rbxassetid only
    HasOutline = true,
    -- remove it below if you don't want to use the key system in your script.

})


--Window:SetBackgroundImage("rbxassetid://13511292247")


Window:EditOpenButton({
    Title = "Open Example UI",
    Icon = "monitor",
    CornerRadius = UDim.new(0,16),
    StrokeThickness = 2,
    Color = ColorSequence.new( -- gradient
        Color3.fromHex("FF0F7B"), 
        Color3.fromHex("F89B29")
    ),
    --Enabled = false,
    Draggable = true,
})


local Tabs = {
    ParagraphTab = Window:Tab({ Title = "Paragraph", Icon = "type" }),
    ButtonTab = Window:Tab({ Title = "Button", Icon = "mouse-pointer-2", Desc = "Contains interactive buttons for various actions." }),
    CodeTab = Window:Tab({ Title = "Code", Icon = "code", Desc = "Displays and manages code snippets." }),
    ColorPickerTab = Window:Tab({ Title = "ColorPicker", Icon = "paintbrush", Desc = "Choose and customize colors easily." }),
    NotificationTab = Window:Tab({ Title = "Notification", Icon = "bell", Desc = "Configure and view notifications." }),
    ToggleTab = Window:Tab({ Title = "Toggle", Icon = "toggle-left", Desc = "Switch settings on and off." }),
    SliderTab = Window:Tab({ Title = "Slider", Icon = "sliders-horizontal", Desc = "Adjust values smoothly with sliders." }),
    InputTab = Window:Tab({ Title = "Input", Icon = "keyboard", Desc = "Accept text and numerical input." }),
    DropdownTab = Window:Tab({ Title = "Dropdown", Icon = "chevrons-up-down", Desc = "Select from multiple options." }),
    b = Window:Divider(),
    WindowTab = Window:Tab({ Title = "Window and File Configuration", Icon = "settings", Desc = "Manage window settings and file configurations." }),
    CreateThemeTab = Window:Tab({ Title = "Create Theme", Icon = "palette", Desc = "Design and apply custom themes." }),
    be = Window:Divider(),
    LongTab = Window:Tab({ Title = "Long and empty tab. Looong and empty.. tab.", Icon = "frown", Desc = "Long Description" }),
    LockedTab = Window:Tab({ Title = "Locked Tab", Icon = "lock", Desc = "This tab is locked", Locked = true }),
}

Window:SelectTab(1)


Tabs.ParagraphTab:Paragraph({
    Title = "Default",
    Desc = "Normal Paragraph",
    Image = "bird",
    --Color = "Red"
    Buttons = {
        {
            Title = "Ok!",
        },
        {
            Title = "Ok!",
        }
    }
})