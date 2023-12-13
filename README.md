    script_key = "JZYWIdulfKnSxNCTfRtiwyQfFqcXDvkz
    repeat wait() until game:IsLoaded()

    delay(DelayTime or 300, function()
        local CG = game:GetService("CoreGui")
        if not CG:FindFirstChild("W-azure") then
            game:GetService("TeleportService"):Teleport(game.PlaceId, game.Players.LocalPlayer)
        end
    end)

    wait(0)
    loadstring(game:HttpGet("https://api.luarmor.net/files/v3/loaders/607f2cd3aa6f0808c9226aacb9bbceb0.lua"))()
