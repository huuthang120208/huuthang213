game:GetService("RunService"):Set3dRenderingEnabled(false)
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
if script_key then
return
end
--Put Your Key Between ""
script_key="JZYWIdulfKnSxNCTfRtiwyQfFqcXDvkz";
DelayTime = 300
getgenv().FpsBoost = true
getgenv().Setting = {
    ["Team"] = "Pirates", --Marines
    ["Webhook"] = {
        ["Url"] = "https://discord.com/api/webhooks/1084193047669133392/RKxiRBvaMuGDp8ahQjPgLmyL31m7URoZYBG5b0FrQtt8kc0ypKcjM1sO7JFVnGSvPss9",
        ["Enabled"] = true,
        ["Embed"] = true,
        ["StoredFruit"] = true,
        ["ImageEmbed"] = true,
        ["CustomImage"] = false,
        ["CustomImageUrl"] = "", --Your Url
        ["OnServerHop"] = true,
        ["BountyChanged"] = true,
    }, 
    ["Panel"] = true,
    ["FpsBoost"] = {
        Enable = false,
        Mode = "Full",--Lite: Just Lower Graphics, Full: Completely Make All Objects Transparent
    },
    ["Hide Theme"] = true,
    ["3D Render Disable"] = false,
    ["Theme"] = {
        ["Name"] = "Raiden",--"Old", "Raiden","Ayaka","Hutao","Yelan","Miko","Nahida","Ganyu","Keqing","Nilou","Barbara","Zhongli","Layla"
        ["Custom"] = {
            ["Enable"] = true,
            ['char_size'] = UDim2.new(0.668, 0, 1.158, 0),
            ['char_pos'] = UDim2.new(0.463, 0, -0.105, 0),
            ['title_color'] = Color3.fromRGB(255, 221, 252),
            ['titleback_color'] = Color3.fromRGB(169, 20, 255),
            ['list_color'] = Color3.fromRGB(255, 221, 252),
            ['liststroke_color'] = Color3.fromRGB(151, 123, 207),
            ['button_color'] = Color3.fromRGB(255, 221, 252)
        },
    },
    ["In Combat Reset"] = true, -- Shouldn't Cause Much False Resets, Enable This Make Farming Much Faster
    ["BypassTP"] = {
        ["Enable"] = true,
        ["Attempt"] = 5, -- Tween If Failed After x Attempts
    },
    ["DodgeSkill"] = true,
    ["SpectatePlayer"] = false,
    ["Config"] = {
        ["nameaccount1"] = "nameconfig.txt",
        ["nameaccount2"] = "nameconfig.txt",
    },
    ["Auto Use Race V3"] = {
        Enable = true,
        UseBelowHealth = false, -- Below Specific Health It Will use Race V3
        Health = 4500,
        NearPlayer = true, -- Only use If Near Player
    },
    ["Auto Use Race V4"] = true, -- No Way you are turning this off
    ["Auto Dash If Mink V4"] = false,
    ["Auto Dash If Ghoul V4"] = false,
    ["Spam All Skill On Race Transform V4"] = false,
    ["Failed To Load Data"] = {
        Rejoin = true,
        TimeToCheck = 30,
    },
    ["Detect KeyWords"] = { -- If There Is A Person Says A Key Word In Chat, It Will Stop Auto Bounty And  Server Hop
        Enable = false,
        Words = { "Hacker", "Exploiter", "Scripter", "Script", "Hack"}
    },
    AutoConfigMelee = false,
    AutoConfigSword = false,
    AutoConfigFruit = false,
    SwitchPlayerKeybind = "G", -- Except Y Keybind
    ["LimitServerHopTime"] ={ -- Only Hop After "Time" Seconds
        Enable = false,
        Time = 600, --Second
    },
    ["Position Config"] = {
        Mode = "Default",-- You Can Create Your Own Mode By Making An Index In The Table Like Custom
        Tween = true, -- If false then it will teleport when near target
        SkyTween = false, -- Tweening In The Sky Till You Are Near The Player, Recommended For Using Gun Method
        Spin = true,
        ["Default"] = {
            DistanceFromPlayer = {
                x = 3, y = 3, z = 3,
            }
        },
        ["Custom"] = {
            DistanceFromPlayer = {
                x = 0, y = 3, z = 0
            }
        }
    },
    ["ChatKill"] = {
        Enable = false,
        Chat = {
            "Go Buy W-azure Now","I Got A Gaming Chair","I'm Just Too Good"
        },
    },
    ["Mention"] = {
        ["Enable"] = false,
        ["Id"] = "everyone", -- You Can Replace With Your Id (not your discord Name)
        ["EveryBounty"] = 16000,
    },
    ["FpsLock"] = {
        ["Enable"] = false,
        ["Cap"] = 30,
    },
    ["LockBounty"] = {
        ["Enable"] = false,
        ["Cap"] = 30000000,
        ["Action"] = "Kick", -- Kick, Shutdown
        ["SendMessage"] = false,
        ["Message"] = "Congratulation You Have Reached The Bounty Cap MyBounty 🔥 🔥 :fireworks: :fireworks: :fireworks:" -- It Will Replace MyBounty With Your Current Bounty, Add Ping Everyone If You Want
    },
    ["Click"] = {
        ["Enable"] = true,
        ["FastClick"] = true,
        ["OnLowHealthDisable"] = true,
        ["LowHealth"] = 5000,
    },
    ["Misc"] = {
        ["AutoBuyRandomandStoreFruit"] = true,
        ["AutoBuySurprise"] = true,
    },
    ["Invisible"] = true, -- Self Explain
    ["IgnoreFriends"] = false, --Server Hop When Your friends in your server
    ["GunMethod"] = false, --Use Melee,Gun Will automaticly disable invisible for things
    ["GunMethodSetting"] = {
        LessSusKillTest=true,
        StartHealth = 2000, -- Below Is Setting For Decrease Sus Kill From Gun Method
        waittime=10,
        EndHealth = 4000,
    },
    ["Notify"] = {
        Enable = false,
        CustomIcon = false,
        Image = "sticker.png", -- The Path Is: W-azure/AutoBounty/Notify
    },
    ["SpamSkill"] = false, -- Will use all skills as fast as possbile ignore holding skills
    ["Weapons"] = { -- Select Weapon, Self Explain
        ["Melee"] = {
            ["Enable"] = true,
            ["Delay"] = 3,
            ["Skills"] = {
                ["Z"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0,
                    ["TimeToNextSkill"] = 0,
                },
            [ "X"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0,
                    ["TimeToNextSkill"] = 0,
                },

                ["C"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0,
                    ["TimeToNextSkill"] = 0,
                },
            },
        },
        ["Blox Fruit"] = {
            ["Enable"] = true,
            ["Delay"] = 2.5,
            ["Skills"] = {
                ["Z"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 1.5,
                    ["TimeToNextSkill"] = 0,
                },
                ["X"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0,
                    ["TimeToNextSkill"] = 0,
                },

                ["C"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0,
                    ["TimeToNextSkill"] = 0,
                },
                ["V"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0,
                    ["TimeToNextSkill"] = 0,
                },
                ["F"] = {
                    ["Enable"] = false,
                    ["HoldTime"] = 0,
                    ["TimeToNextSkill"] = 0,
                },
            },
        },
        ["Sword"] = {
            ["Enable"] = false,
            ["Delay"] = 0.5,
            ["Skills"] = {
                ["Z"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0.1,
                    ["TimeToNextSkill"] = 0,
                },
                ["X"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0.2,
                    ["TimeToNextSkill"] = 0,
                },
            },
        },
        ["Gun"] = {
            ["Enable"] = false,
            ["Delay"] = 0.5,
            ["Skills"] = {
                ["Z"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0.1,
                    ["TimeToNextSkill"] = 0,
                },
                ["X"] = {
                    ["Enable"] = true,
                    ["HoldTime"] = 0.1,
                    ["TimeToNextSkill"] = 0,
                },
            },
        },

    }
}
repeat wait()
until game:IsLoaded()
delay(DelayTime or 300,function()
    local CG = game:GetService("CoreGui")
    if not CG:FindFirstChild("W-azureHubAutoBounty") then
       game:GetService("TeleportService"):Teleport(game.PlaceId, game.Players.LocalPlayer)
    end
end)
wait(2)
loadstring(game:HttpGet("https://api.luarmor.net/files/v3/loaders/1e7c7be9c64d317c9642fbd179359e72.lua"))()
