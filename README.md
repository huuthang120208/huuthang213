_G.PointStats = 9999
_G.PointStatsSmall = 2448
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
                if game:GetService("Players")["LocalPlayer"].Data.Points.Value = 0 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense",_G.PointStats)
                end
        end)
    end
end)

spawn(function() -- sword
    while wait() do
        pcall(function()
            if game:GetService("Players")["LocalPlayer"].Data.Points.Value = 0 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","1")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Sword",_G.PointStatsSmall)
                end
        end)
    end
end)
spawn(function() -- Gun
    while wait() do
        pcall(function()
            if game:GetService("Players")["LocalPlayer"].Data.Points.Value = 0 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","1")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Gun",_G.PointStatsSmall)
                end
        end)
    end
end)
spawn(function() -- Demon Fruit
    while wait() do
        pcall(function()
            if game:GetService("Players")["LocalPlayer"].Data.Points.Value = 0 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","1")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Demon Fruit",_G.PointStatsSmall)
                end
        end)
    end
end)
