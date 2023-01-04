local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Baller HUB", "Synapse")
local Tab = Window:NewTab("Main")
local Section = Tab:NewSection("NEED EQUIP BALLER GLOVE")
local Section = Tab:NewSection("Spawn ballers")
Section:NewButton("Spawn baller once", "", function()
    game:GetService("ReplicatedStorage").GeneralAbility:FireServer()
end)
Section:NewToggle("Loop spawn baller", "", function(state)
    if state then
        getgenv().baller = true;

while wait() do
    if getgenv().baller == true then
        game:GetService("ReplicatedStorage").GeneralAbility:FireServer()
    end
end

    else
        getgenv().baller = false;

while wait() do
    if getgenv().baller == true then
        game:GetService("ReplicatedStorage").GeneralAbility:FireServer()
    end
end

    end
end)
local Tab = Window:NewTab("#Credits")
local Section = Tab:NewSection("Mady by:")
Section:NewButton("Anha#4156", "discord", function()
    setclipboard("Anha#4156")
end)
Section:NewButton("Discord channel", "discord", function()
    setclipboard("https://discord.gg/58rKZ7z4RV")
end)
