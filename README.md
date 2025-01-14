-- carregar biblioteca
local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()

local Window = Fluent:CreateWindow({
    Title = "CleitonScripts" .. Fluent.Version,
    TabWidth = 160, Size = UDim2.fromOffset(580, 460), Theme = "Dark"
})

-- avisos ao executar
Fluent:Notify({ Title = "executando!", Content = "executado com sucesso!" })

local Tabs = {
    Main = Window:AddTab({ Title = "Games🎮" }),
}
-- Games
Tabs.Main:AddButton({ Title = "MM2🔪", Callback = function() 
loadstring(game:HttpGet(('https://raw.githubusercontent.com/MarsQQ/ScriptHubScripts/master/MM2%20Admin%20Panel'),true))()
end })

Tabs.Main:AddButton({ Title = "🏠Brookhaven🏠", Callback = function() 
loadstring(game:HttpGet("https://raw.githubusercontent.com/REDzHUB/REDzHUB/main/REDzHUB"))()
end })

Tabs.Main:AddButton({ Title = "Blox fruit v1", Callback = function() print("Botão clicado!") 
loadstring(game:HttpGet("https://raw.githubusercontent.com/Augustzyzx/UraniumMobile/main/MobilePC.lua"))()
end })

Tabs.Main:AddButton({ Title = "build aboat🛥️", Callback = function() print("Botão clicado!") 
loadstring(game:HttpGet("https://orbitsc.net/babft"))()
end })

local Tabs = {
    Main = Window:AddTab({ Title = "Scripts" }),
    Settings = Window:AddTab({ Title = "Settings", Icon = "settings" })
}
-- parágrafos
Tabs.Main:AddParagraph({ Title = "Cleitonscript", Content = "Script abaixo" })

-- botões
Tabs.Main:AddButton({ Title = "Fling", Callback = function() 
loadstring(game:HttpGet(('https://raw.githubusercontent.com/0Ben1/fe/main/obf_5wpM7bBcOPspmX7lQ3m75SrYNWqxZ858ai3tJdEAId6jSI05IOUB224FQ0VSAswH.lua.txt'),true))()
end })

Tabs.Main:AddButton({ Title = "Fly Gui", Callback = function() 
loadstring("\108\111\97\100\115\116\114\105\110\103\40\103\97\109\101\58\72\116\116\112\71\101\116\40\40\39\104\116\116\112\115\58\47\47\103\105\115\116\46\103\105\116\104\117\98\117\115\101\114\99\111\110\116\101\110\116\46\99\111\109\47\109\101\111\122\111\110\101\89\84\47\98\102\48\51\55\100\102\102\57\102\48\97\55\48\48\49\55\51\48\52\100\100\100\54\55\102\100\99\100\51\55\48\47\114\97\119\47\101\49\52\101\55\52\102\52\50\53\98\48\54\48\100\102\53\50\51\51\52\51\99\102\51\48\98\55\56\55\48\55\52\101\98\51\99\53\100\50\47\97\114\99\101\117\115\37\50\53\50\48\120\37\50\53\50\48\102\108\121\37\50\53\50\48\50\37\50\53\50\48\111\98\102\108\117\99\97\116\111\114\39\41\44\116\114\117\101\41\41\40\41\10\10")()
end })

Tabs.Main:AddButton({ Title = "infjump", Callback = function() 
loadstring(game:HttpGet("https://raw.githubusercontent.com/HeyGyt/infjump/main/main"))()
end })

Tabs.Main:AddButton({ Title = "fates admin", Callback = function() print("Botão clicado!") 
loadstring(game:HttpGet("https://raw.githubusercontent.com/fatesc/fates-admin/main/main.lua"))()
end })

-- sliders

local Slider = Tabs.Main:AddSlider("pulo", 
{
    Title = "super pulo",
    Description = "ajustar super pulo",
    Default = 2,
    Min = 0,
    Max = 5,
    Rounding = 1,
    Callback = function(Value)
        print("pulo modificado:", Value)
    end
})

local Slider = Tabs.Main:AddSlider("velocidade", 
{
    Title = "Velocidade",
    Description = "Ajusta a velocidade do jogador",
    Default = 2,
    Min = 0,
    Max = 10,
    Rounding = 1,
    Callback = function(Value)
        local player = game.Players.LocalPlayer
        local character = player.Character or player.CharacterAdded:Wait()
        local humanoid = character:WaitForChild("Humanoid")
        
        -- Define a velocidade de caminhada
        humanoid.WalkSpeed = Value * 10  -- Multiplica o valor para aumentar o impacto
    end
})
