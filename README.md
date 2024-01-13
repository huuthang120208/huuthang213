_G.PointStats = 9999
_G.Point = "Demon Fruit"  -- Demon Fruit, Sword, Gun ,

spawn(function()
    while wait() do
        pcall(function()
                if game:GetService("Players")["LocalPlayer"].Data.Points.Value ~= 2550 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Melee",_G.PointStats)
                end
        end)
    end
end)

spawn(function()
    while wait() do
        pcall(function()
                if game:GetService("Players")["LocalPlayer"].Data.Points.Value <= 2449 and game:GetService("Players")["LocalPlayer"].Data.Points.Value >= 2 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense",_G.PointStats)
                end
        end)
    end
end)

spawn(function() -- sword
    while wait() do
        pcall(function()
            if game:GetService("Players")["LocalPlayer"].Data.Points.Value <= 2449 and game:GetService("Players")["LocalPlayer"].Data.Points.Value >= 2 and _G.Point == "Sword" then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","1")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Sword",_G.PointStats)
                end
        end)
    end
end)

spawn(function() -- Gun
    while wait() do
        pcall(function()
            if game:GetService("Players")["LocalPlayer"].Data.Points.Value <= 2449 and game:GetService("Players")["LocalPlayer"].Data.Points.Value >= 2 and _G.Point == "Gun" then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","1")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Gun",_G.PointStats)
                end
        end)
    end
end)

spawn(function() -- Demon Fruit
    while wait() do
        pcall(function()
            if game:GetService("Players")["LocalPlayer"].Data.Points.Value <= 2449 and game:GetService("Players")["LocalPlayer"].Data.Points.Value >= 2 and _G.Point == "Demon Fruit" then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","1")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Demon Fruit",_G.PointStats)
                end
        end)
    end
end)
