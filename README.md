_G.PointStats = 9999
_G.PointsType = "Demon Fruit"  Demon Fruit, Sword, Gun

spawn(function()
    while wait() do
        pcall(function()
                if game:GetService("Players")["LocalPlayer"].Data.Points.Value <= 2449 and game:GetService("Players")["LocalPlayer"].Data.Points.Value >= 2 then
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
function addSwordPoint()
    spawn(function() -- sword
        while wait() do
            pcall(function()
                if game:GetService("Players")["LocalPlayer"].Data.Points.Value <= 2449 and game:GetService("Players")["LocalPlayer"].Data.Points.Value >= 2 then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Sword",_G.PointStats)
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","1")
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")
                    end
            end)
        end
    end)
end
function addGunPoint()
    spawn(function() -- Gun
        while wait() do
            pcall(function()
                if game:GetService("Players")["LocalPlayer"].Data.Points.Value <= 2449 and game:GetService("Players")["LocalPlayer"].Data.Points.Value >= 2 then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Gun",_G.PointStats)
                    end
            end)
        end
    end)
end
function addDemonFruitPoint()
    spawn(function() -- Demon Fruit
        while wait() do
            pcall(function()
                if game:GetService("Players")["LocalPlayer"].Data.Points.Value <= 2449 and game:GetService("Players")["LocalPlayer"].Data.Points.Value >= 2 then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Demon Fruit",_G.PointStats)    
                    end
            end)
        end
    end)
end

elseif _G.PointsType == "Sword" then
    addSwordPoint()
elseif _G.PointsType == "Gun" then
    addGunPoint()
elseif _G.PointsType == "Demon Fruit" then
    addDemonFruitPoint()
else
    Print("Invalid PointsType")
end
