repeat task.wait(5) until game:IsLoaded(3)
repeat task.wait() until game.Players
repeat task.wait() until game.Players.LocalPlayer
repeat task.wait() until game.Players.LocalPlayer:FindFirstChild("PlayerGui")
repeat task.wait() until game.Players.LocalPlayer.PlayerGui:FindFirstChild("Main");
UserSettings():GetService('UserGameSettings').MasterVolume = 0;
settings().Rendering.QualityLevel = 1;
game:GetService("StarterGui"):SetCoreGuiEnabled(Enum.CoreGuiType.Chat,false)
game:GetService("Lighting").GlobalShadows = false
for key, object in pairs(workspace:GetDescendants()) do
    if object:IsA("Part") or object:IsA("UnionOperation") or object:IsA("MeshPart") then
        object.Material = Enum.Material.SmoothPlastic
    elseif  (object:IsA("Texture") or object:IsA("Explosion") or object:IsA("ColorCorrectionEffect") or 
                object:IsA("Atmosphere") or object:IsA("SunRaysEffect") or object:IsA("BlurEffect") or 
                object:IsA("RainyStone") or object:IsA("Weather")  or object:IsA("BloomEffect")
                or object:IsA("Lighting") or object:IsA("FogEnd") or object:IsA("DepthOfFieldEffect")) then
        object:Destroy()
    end
end
getgenv().ForceTeam = "Pirates"
getgenv().DitBF = {
    ["Performance"] = {
        ["Hide Map"] = false,
        ["Black Screen"] = true,
        ["Lock FPS"] = 10,
    },
    ["Fast Attack Duration/Cooldown"] = {5, 3},
    ["Raid if Maxed Blox Fruit"] = false,
    ["Farm boss drops while not maxed"] = true,
    ["Farm Blox Fruit Mastery if maxed"] = true,
    ["Farm method after maxed"] = "Raid Boss Farm - Cake Prince Farm",
    ["Extra time Farm until unlock skills"] = true,
    ["Hop Server"] = {
        ["Type"] = {
            ["[Main] Server Hop"] = true,
            ["[Farm] Server Hop if Player nearby"] = false,
            ["[Sea 3 Quest] Server Hop for 1M+ Blox Fruit"] = true,
        },
        ["Delay"] = 100,
    },
    ["Do Action"] = {
        ["Get Godhuman"] = true,
        ["Get Rengoku"] = false,
        ["Get True Triple Katana"] = false,
        ["Get Hallow Scythe"] = false,
        ["Get Cursed Dual Katana"] = true,
        ["Get Soul Guitar"] = false,
        ["Awake Current Blox Fruit"] = true,
        ["Get Mirror Fractal"] = true,
    },
    ["Buy Haki"] = {
        ["Enhancement"] = false,
        ["Skyjump"] = false,
        ["Flash Step"] = false,
        ["Observation"] = true,
        ["Legendary Enhancement"] = false,
    },
    ["Auto Race"] = "none",
    ["Blox Fruit Sniper"] = {
    "Magma-Magma",
    },
    ["Main Blox Fruit"] = {
    "Magma-Magma",
},
    ["Eat Sniper Blox Fruits"] = true,
    ["Account Panel"] = {
        ["Enable"] = true,
        ["Delay"] = 300,
        ["Note"] = " god magma v2 ",
    },
}
getgenv().Key = "k78aebd486146558ac9d406e"
repeat wait()spawn(function()loadstring(game:HttpGet("https://ditbloxfruit.cc/devbuild.lua"))()end)wait(60)until S_Timer
