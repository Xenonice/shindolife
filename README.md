repeat wait() until game:IsLoaded()
--old-antitp bypass
if workspace:FindFirstChild("CCoff") then
    game:GetService("Workspace").CCoff:Destroy()
end
--antiafk
local VirtualUser=game:service'VirtualUser'
	game:service'Players'.LocalPlayer.Idled:connect(function()
	warn("anti-afk")
	VirtualUser:CaptureController()
	VirtualUser:ClickButton2(Vector2.new())
end)
-------------------------------------------------------------------------------------

local player = game.Players.LocalPlayer
local mission = player.PlayerGui:WaitForChild("Main"):WaitForChild("ingame"):WaitForChild("Missionstory")
local menuplace = 4616652839
local forestplace = 5447073001
local rainplace = 5084678830
local trainingplace = 5431071837
local akatsukiplace = 5431069982
local worldxplace = 5943874201
local villageplace = game:GetService("Workspace"):FindFirstChild("rank")
local warplace = game:GetService("Workspace"):FindFirstChild("warmode")
function toTarget(pos, targetPos, targetCFrame)
    local tween_s = game:service"TweenService"
    local info = TweenInfo.new((targetPos - pos).Magnitude/getgenv().speed, Enum.EasingStyle.Linear)
    local tween, err = pcall(function()
        local tween = tween_s:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"], info, {CFrame = targetCFrame * CFrame.fromAxisAngle(Vector3.new(1,0,0), math.rad(90))})
        tween:Play()
    end)
    if not tween then return err end
end

--UI Lib Loading

_G.Color = Color3.fromRGB(220,20,60)
_G.Color2 = Color3.fromRGB(255, 255, 255)
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/naypramx/Ui__Project/Script/XeNonUi", true))()
    local CenterHubNo1 = library:CreateWindow("kamua HUB | shindo life", Enum.KeyCode.RightControl)
    local Tab = CenterHubNo1:CreateTab("Main", 8607359113)
    
    local Sector1 = Tab:CreateSector("Main","left")
    Sector1:AddSeperator("Inf Mode")
    
    
    Sector1:AddButton("Open", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/6Wumpus6/SpyHub/main/InfmodeOpen", true))()
    end)

    Sector1:AddButton("Close", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/6Wumpus6/SpyHub/main/Infmodeclose", true))()
    end)

    Sector1:AddSeperator("Doge")
    
    Sector1:AddButton("Open", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/6Wumpus6/SpyHub/main/Autoopen", true))()
    end)

    Sector1:AddButton("Close", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/6Wumpus6/SpyHub/main/Autoclose", true))()
    end)
    
    
