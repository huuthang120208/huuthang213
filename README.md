_G.PointStats = 9999
_G.PointStatsSmall = 2448
if game:GetService("Players")
 ["LocalPlayer"].Data.Points.Value ~= 1 and game:GetService("Players")["LocalPlayer"].Data.Points.Value = 0 then
spawn(function()
      while wait() do
         pcall(function()
                 if game:GetService("Players")["LocalPlayer"].Data.Points.Value ~= 1 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Melee",_G.PointStats)
                 end
         end)
     end
 end)
 spawn(function()
     while wait() do
         pcall(function()
                 if game:GetService("Players")["LocalPlayer"].Data.Points.Value ~= 1 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense",_G.PointStats)
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
