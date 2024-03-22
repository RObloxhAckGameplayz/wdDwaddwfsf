local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "⭐️Early Acesss Version⭐️ WOND3RFOL SCRIPT HUB", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})

--[[
Name = <string> - The name of the UI.
HidePremium = <bool> - Whether or not the user details shows Premium status or not.
SaveConfig = <bool> - Toggles the config saving in the UI.
ConfigFolder = <string> - The name of the folder where the configs are saved.
IntroEnabled = <bool> - Whether or not to show the intro animation.
IntroText = <string> - Text to show in the intro animation.
IntroIcon = <string> - URL to the image you want to use in the intro animation.
Icon = <string> - URL to the image you want displayed on the window.
CloseCallback = <function> - Function to execute when the window is closed.
]]
local Tab = Window:MakeTab({
	Name = "Settings & Information",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddParagraph("nothing changed made this ye","Yeah hi.")
local Tab = Window:MakeTab({
	Name = "da hood.",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Fps Gui ",
	Callback = function()
        pcall(function()
            local espcolor = Color3.fromRGB(140, 69, 102)
            local wallhack_esp_transparency = .4
            local gui_hide_button = {Enum.KeyCode.LeftControl, "h"}
            local plrs = game:GetService("Players")
            local lplr = game:GetService("Players").LocalPlayer
            local TeamBased = false ; local teambasedswitch = "c"
            local presskeytoaim = true; local aimkey = "q"
            aimbothider = false; aimbothiderspeed = .5
            local Aim_Assist = false ; Aim_Assist_Key = {Enum.KeyCode.LeftControl, "z"}
            local espupdatetime = 5; autoesp = false; local charmsesp = true
            local movementcounting = true
            
            
            
            
            local mouselock = false
            local canaimat = true
            local lockaim = true; local lockangle = 5
            local ver = "2.4"
            local cam = game.Workspace.CurrentCamera
            local BetterDeathCount = true
            local ballisticsboost = 0
            
            local mouse = lplr:GetMouse()
            local switch = false
            local key = "k"
            local aimatpart = nil
            local lightesp = false
            
            local abs = math.abs
            
            local Gui = Instance.new("ScreenGui")
            local Move = Instance.new("Frame")
            local Main = Instance.new("Frame")
            local EspStatus = Instance.new("TextLabel")
            local st1 = Instance.new("TextLabel")
            local st1_2 = Instance.new("TextLabel")
            local st1_3 = Instance.new("TextBox")
            local Name = Instance.new("TextLabel")
            --Properties:
            
            Gui.Parent = plrs.LocalPlayer:WaitForChild("PlayerGui")
            
            
            local aimbotstatus = {"qc", "qr", "qe", "qd", "qi", "qt", "qs", "dd", "sp", "ql", "qa", "qd", "qs"}
            local gotstring = 0
            local function getrandomstring()
                gotstring = gotstring+666
                local str = ""
                local randomstring = {"a", "b", "c", "d", "e", "f", "g", "h", "i", "g", "k", "l", "m", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z",
                     "а","б","в","г","д","е","ё","ж","з","и","й","к","л","м","о","п","р","с","т","у","ф","х","ч","щ","ъ","ы","ъ","э","ю","я", "`", "$", 
                    "0","1","2","3","4","5","6","7","8","9", }
                local counting123 = 0
                for i, v in ipairs(randomstring) do
                    counting123 = i
                end
                do
                    math.randomseed(tick()+gotstring)
                    for i = 3, math.random(1,100) do
                            math.randomseed(i+tick()+gotstring)
                            
                            local oneortwo = math.random(1,2)
                            if oneortwo == 2 then
                                math.randomseed(i+tick()+gotstring)
                                str = str..""..randomstring[math.random(1, counting123)]
                            else
                                math.randomseed(i+tick()+gotstring)
                                str = str..""..string.upper(randomstring[math.random(1, counting123)])
                            end
                        
                    end
                end
                return str
            end
            local mousedown = false
            local isonmovething = false
            local mouseoffset = Vector2.new()
            local mousedown = false
            local bspeed = 3584
            local aimbotoffset = {dd = ":", sp = " ", qa = "a", qb = "b",qc = "c", qd = "d", qe = "e", qf = "f", qg = "g" , qh = "h" , qi = "i", qj = "j", qk = "k", ql = "l", qm = "m", qn = "n", qo = "o", qp = "p", qq = "q", qr = "r", qs = "s", qt = "t", qu = "u", qv = "w", qx = "x", qy = "y", qz = "z"}
            
            
            
            Gui.Name = getrandomstring()
            
            Move.Name = getrandomstring()
            Move.Draggable = true
            Move.Parent = Gui
            Move.BackgroundColor3 = Color3.new(0.0431373, 1, 0.0745098)
            Move.BackgroundTransparency = 0.40000000596046
            Move.BorderSizePixel = 0
            Move.Position = UDim2.new(0.5, 0,0.018, 0)
            Move.Size = UDim2.new(0, 320, 0, 30)
            
            Move.MouseEnter:Connect(function()
                
                isonmovething = true
                
            end)
            Move.MouseLeave:Connect(function()
                
                isonmovething = mousedown and true or false
            end)
            mouse.Button1Down:connect(function()
                mousedown = true
                mouseoffset = Move.AbsolutePosition - Vector2.new(mouse.X, mouse.Y)
            end)
            mouse.Button1Up:connect(function()
                mousedown = false
            end)
            
            mouse.Move:Connect(function()
                if isonmovething == true and mousedown then
                    Move.Position = UDim2.new(0, mouseoffset.X + mouse.X, 0, mouseoffset.Y + mouse.Y)
                end
            end)
            local function uc (st)
                local ast = ""
                for i, v in ipairs(st) do
                    local let = aimbotoffset[v]
                    ast = ast..let
                end
                return ast
            end
            
            Main.Name = getrandomstring()
            Main.Parent = Move
            Main.BackgroundColor3 = Color3.new(0.176471, 0.176471, 0.176471)
            Main.BackgroundTransparency = 0.69999998807907
            Main.Position = UDim2.new(0, 0, 0.995670795, 0)
            Main.Size = UDim2.new(1.0000006, 0, 11.2, 0)
            
            st1.Name = getrandomstring()
            st1.Parent = Main
            st1.BackgroundColor3 = Color3.new(1, 1, 1)
            st1.BackgroundTransparency = 1
            st1.Position = UDim2.new(0, 0, 0, 0)
            st1.Size = UDim2.new(1, 0, 0.161862016, 0)
            st1.Font = Enum.Font.ArialBold
            st1.Text = uc(aimbotstatus)
            st1.TextColor3 = Color3.new(0.0431373, 1, 0.0745098)
            st1.TextScaled = true
            st1.TextSize = 14
            st1.TextWrapped = true
            
            st1_2.Name = getrandomstring()
            st1_2.Parent = Main
            st1_2.BackgroundColor3 = Color3.new(1, 1, 1)
            st1_2.BackgroundTransparency = 1
            st1_2.Position = UDim2.new(0, 0, 0.375590861, 0)
            st1_2.Size = UDim2.new(0.999999881, 0, 0.161862016, 0)
            st1_2.Font = Enum.Font.ArialBold
            st1_2.TextXAlignment = Enum.TextXAlignment.Left
            st1_2.Text = "Current ballistics: 0"
            st1_2.TextColor3 = Color3.new(0.0431373, 1, 0.0745098)
            st1_2.TextScaled = true
            st1_2.TextSize = 14
            st1_2.TextWrapped = true
            
            local aimbothiderbox = Instance.new("TextBox")
            aimbothiderbox.Name = getrandomstring()
            aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." off"
            aimbothiderbox.Size = UDim2.new(1, 0,0.162, 0)
            aimbothiderbox.TextScaled = true
            aimbothiderbox.TextColor3 =Color3.fromRGB(255, 0, 0)
            aimbothiderbox.Position = UDim2.new(0, 0,0.853, 0)
            aimbothiderbox.BackgroundTransparency = 1
            aimbothiderbox.Parent = Main
            
            st1_3.Name = getrandomstring()
            st1_3.Parent = Main
            st1_3.BackgroundColor3 = Color3.new(1, 1, 1)
            st1_3.BackgroundTransparency = 1
            st1_3.Position = UDim2.new(0, 0, 0.18558608, 0)
            st1_3.Size = UDim2.new(0.999999881, 0, 0.161862016, 0)
            st1_3.Font = Enum.Font.ArialBold
            st1_3.Text = "Bullet speed = 3584"
            st1_3.TextColor3 = Color3.new(0.0431373, 1, 0.0745098)
            st1_3.TextScaled = true
            st1_3.TextSize = 14
            st1_3.TextWrapped = true
            local teambasedstatus = st1_3:Clone()
            teambasedstatus.Parent = Main
            teambasedstatus.TextScaled = true
            teambasedstatus.Position = UDim2.new(0, 0,.7, 0)
            teambasedstatus.Size = UDim2.new(1, 0,.1, 0)
            teambasedstatus.Name = getrandomstring()
            teambasedstatus.Text = "Team Based: "..tostring(TeamBased)
            local espstatustext = teambasedstatus:Clone()
            espstatustext.Name = getrandomstring()
            espstatustext.Position = UDim2.new(0, 0,0.58, 0)
            espstatustext.Text = "Esp loop :"..tostring(autoesp)
            espstatustext.Parent = Main
            local hide = Instance.new("TextButton")
            hide.Text = "_"
            hide.BackgroundTransparency = 1
            hide.TextScaled = true
            hide.TextWrapped = true
            hide.Size = UDim2.new(0.1, 0,1, 0)
            hide.Position = UDim2.new(0.9, 0,-0.15, 0)
            hide.Name = getrandomstring()
            hide.Parent = Move
            Name.Name = getrandomstring()
            Name.Parent = Move
            Name.BackgroundColor3 = Color3.new(1, 1, 1)
            Name.BackgroundTransparency = 1
            Name.Size = UDim2.new(0.838, 0, 1, 0)
            Name.Font = Enum.Font.Arial
            Name.Text = "FPS gui v"..ver
            Name.TextColor3 = Color3.new(0, 0, 0)
            Name.TextScaled = true
            Name.TextSize = 14
            Name.TextWrapped = true
            Name.TextXAlignment = Enum.TextXAlignment.Left
            local scr = Instance.new("ScrollingFrame")
            scr.Size = Main.Size
            scr.Position = Main.Position
            scr.ScrollBarThickness = 0
            scr.BackgroundTransparency = 1
            scr.Name = getrandomstring()
            Main.Size = UDim2.new(1, 0, 1, 0)
            Main.Position = UDim2.new(0,0,0,0)
            Main.Parent = scr
            scr.Parent = Move
            startpos = Main.Position
            Move.Active = true
            
            -- Scripts:
            hided = false
            hide.MouseButton1Click:Connect(function()
                if hided == false then
                    hided = true
                    Main:TweenPosition(UDim2.new(0, 0, -1.5, 0))
                else
                    hided = false
                    Main:TweenPosition(startpos)
                end
            end)
            
            
            aimbothiderbox.FocusLost:Connect(function()
                local numb = tonumber(aimbothiderbox.Text)
                if aimbothider == true then
                    aimbothiderbox.TextColor3 =Color3.fromRGB(11, 255, 19)
                else
                    aimbothiderbox.TextColor3 =Color3.fromRGB(255, 0, 0)
                end
                if numb ~= nil then
                    aimbothiderspeed = numb
                    if aimbothider == true then
                        aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." on"
                    else
                        aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." off"
                    end
                else
                    if aimbothider == true then
                        aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." on"
                    else
                        aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." off"
                    end
                end
            end)
            
            
            local plrsforaim = {}
            
            
            Move.Draggable = true
            Gui.ResetOnSpawn = false
            --Gui.Name = "Chat"
            Gui.DisplayOrder = 999
            pcall(function()
            if not game:GetService("CoreGui") then
                Gui.Parent = plrs.LocalPlayer.PlayerGui
            else
                Gui.Parent = game:GetService("CoreGui")
            end
            end)
            local espheadthing
            do
            local BillboardGui = Instance.new("BillboardGui")
            local PName = Instance.new("TextLabel")
            local Pdist = Instance.new("TextLabel")
            local ImageLabel = Instance.new("ImageLabel")
            local ImageLabel_2 = Instance.new("ImageLabel")
            --Properties:
            --BillboardGui.Parent = game.Workspace.Part
            BillboardGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
            BillboardGui.AlwaysOnTop = true
            BillboardGui.LightInfluence = 0
            BillboardGui.Size = UDim2.new(0, 100, 0, 46)
            BillboardGui.Name = "headoverthing"
            PName.Name = "PName"
            PName.Parent = BillboardGui
            PName.BackgroundColor3 = espcolor
            PName.BackgroundTransparency = 0.55000001192093
            PName.BorderSizePixel = 0
            PName.Size = UDim2.new(0, 100, 0, 23)
            PName.Font = Enum.Font.SourceSans
            PName.Text = "urmom"
            PName.TextColor3 = Color3.new(0, 0, 0)
            PName.TextScaled = true
            PName.TextSize = 14
            PName.TextWrapped = true
            st1.Text = uc(aimbotstatus)
            Pdist.Name = "Pdist"
            Pdist.Parent = BillboardGui
            Pdist.AnchorPoint = Vector2.new(0.5, 0)
            Pdist.BackgroundColor3 = espcolor
            Pdist.BackgroundTransparency = 0.55000001192093
            Pdist.BorderSizePixel = 0
            Pdist.Position = UDim2.new(0.5, 0, 0.5, 0)
            Pdist.Size = UDim2.new(0, 70, 0, 23)
            Pdist.Font = Enum.Font.SourceSans
            Pdist.Text = "666"
            Pdist.TextColor3 = Color3.new(0, 0, 0)
            Pdist.TextScaled = true
            Pdist.TextSize = 14
            Pdist.TextWrapped = true
            
            ImageLabel.Parent = BillboardGui
            ImageLabel.BackgroundColor3 = Color3.new(0.298039, 1, 0)
            ImageLabel.BackgroundTransparency = 1
            ImageLabel.BorderColor3 = espcolor
            ImageLabel.Position = UDim2.new(1, -15, 0.5, 0)
            ImageLabel.Rotation = 180
            ImageLabel.Size = UDim2.new(0, 15, 0, 23)
            ImageLabel.Image = "rbxassetid://2832171824"
            ImageLabel.ImageColor3 = espcolor
            ImageLabel.ImageTransparency = 0.55000001192093
            
            ImageLabel_2.Parent = BillboardGui
            ImageLabel_2.BackgroundColor3 = espcolor
            ImageLabel_2.BackgroundTransparency = 1
            ImageLabel_2.BorderColor3 = Color3.new(0.298039, 1, 0)
            ImageLabel_2.Position = UDim2.new(0, 0, 0.5, 0)
            ImageLabel_2.Rotation = 180
            ImageLabel_2.Size = UDim2.new(0, 15, 0, 23)
            ImageLabel_2.Image = "rbxassetid://2832177613"
            ImageLabel_2.ImageColor3 = espcolor
            ImageLabel_2.ImageTransparency = 0.55000001192093
            espheadthing = BillboardGui
            end
            
            
            
            f = {}
            f.UpdateHeadUI = function(v)
                
                    
                        if v.Adornee and v.Adornee ~= nil then
                            local destr = false
                            if TeamBased then
                                destr = true
                                local plr = plrs:GetPlayerFromCharacter(v.Adornee.Parent)
                                if plr and plr.Team and plr.Team.Name ~= lplr.Team.Name then
                                    destr = false
                                end
                            end
                            if lightesp == true then
                                v.Pdist.TextColor3 = Color3.new(1,1,1)
                                v.PName.TextColor3 = Color3.new(1,1,1)
                            else
                                v.Pdist.TextColor3 = Color3.new(0,0,0)
                                v.PName.TextColor3 = Color3.new(0,0,0)
                            end
                            local d = math.floor((cam.CFrame.p - v.Adornee.CFrame.p).magnitude)
                            v.Pdist.Text = tostring(d)
                            if d < 14 then
                                v.Enabled = false
                            else
                                v.Enabled = true
                            end
                            v.StudsOffset = Vector3.new(0,.6+d/14,0)
                            if destr then
                                v:Destroy()
                            end
                        else
                            v:Destroy()
                        end
                    
                
            end
            st1.Text = uc(aimbotstatus)
            local espforlder
            local partconverter = Instance.new("Part")
            --local headsupdatelist = {}
            st1_3.FocusLost:connect(function()
                if tonumber(st1_3.Text) then
                    bspeed = tonumber(st1_3.Text)
                else
                    
                end
            end)
            f.addesp = function()
                pcall(function()
                --print("ESP ran")
                if espforlder then
                    espforlder:Destroy()
                    espforlder = Instance.new("Folder")
                    espforlder.Parent = game.Workspace.CurrentCamera
                else
                    espforlder = Instance.new("Folder")
                    espforlder.Parent = game.Workspace.CurrentCamera
                end
                for i, v in pairs(espforlder:GetChildren()) do
                    v:Destroy()
                end
                for _, plr in pairs(plrs:GetChildren()) do
                    if plr.Character and plr.Character.Humanoid.Health > 0 and plr.Name ~= lplr.Name then
                        if TeamBased == true then
                            
                            if plr.Team.Name ~= plrs.LocalPlayer.Team.Name  then
                                pcall(function()
                                local e = espforlder:FindFirstChild(plr.Name)
                                if not e then
                                    local fold = Instance.new("Folder", espforlder)
                                    fold.Name = plr.Name
                                    
                                    --partconverter.BrickColor = plr.Team.Color
                                    --local teamc = partconverter.Color
                                    for i, p in pairs(plr.Character:GetChildren()) do
                                        if p:IsA("BasePart") and p.Name ~= "HumanoidRootPart" then
                                            if charmsesp then
                                            local urmom = Instance.new("BoxHandleAdornment")
                                            urmom.ZIndex = 10
                                            urmom.AlwaysOnTop = true
                                            urmom.Color3 = espcolor
                                            urmom.Size = p.Size
                                            urmom.Adornee = p
                                            urmom.Name = tick().." Ur mom has big gay"
                                            urmom.Transparency = wallhack_esp_transparency
                                            urmom.Parent = fold
                                            if p.Name == "Head" then
                                                local th = p:FindFirstChild("headoverthing")
                                                if not th then
                                                    local ht = espheadthing:Clone()
                                                    ht.PName.Text = p.Parent.Name
                                                    ht.Adornee = p
                                                    --table.insert(headsupdatelist, ht)
                                                    delay(0, function()
                                                        while wait(0.08) and plr and p do
                                                            f.UpdateHeadUI(ht)
                                                        end
                                                    end)
                                                    ht.Parent = p
                                                end
                                            end
                                            end
                                        end
                                    end
                                    plr.Character.Humanoid.Died:Connect(function()
                                        fold:Destroy()
                                    end)
                                    
                                end
                                end)
                            end
                        else
                            local e = espforlder:FindFirstChild(plr.Name)
                            if not e then
                                local fold = Instance.new("Folder", espforlder)
                                    fold.Name = plr.Name
                                    
                                    --partconverter.BrickColor = plr.Team.Color
                                    --local teamc = Move.BackgroundColor3
                                    for i, p in pairs(plr.Character:GetChildren()) do
                                        if p:IsA("BasePart") and p.Name ~= "HumanoidRootPart" then
                                            pcall(function()
                                            if charmsesp then
                                            local urmom = Instance.new("BoxHandleAdornment")
                                            urmom.ZIndex = 10
                                            urmom.AlwaysOnTop = true
                                            urmom.Color3 = espcolor
                                            urmom.Size = p.Size
                                            urmom.Adornee = p
                                            urmom.Name = tick().." Ur mom has big gay"
                                            urmom.Transparency = wallhack_esp_transparency
                                            urmom.Parent = fold
                                            end
                                            if p.Name == "Head" then
                                                local th = p:FindFirstChild("headoverthing")
                                                if not th then
                                                    local ht = espheadthing:Clone()
                                                    ht.PName.Text = p.Parent.Name
                                                    ht.Adornee = p
                                                    delay(0, function()
                                                        while wait(0.08) and plr and p do
                                                            f.UpdateHeadUI(ht)
                                                        end
                                                    end)
                                                    --table.insert(headsupdatelist, ht)
                                                    ht.Parent = p
                                                end
                                            end
                                            end)
                                        end
                                    end
                                    plr.Character.Humanoid.Died:Connect(function()
                                        fold:Destroy()
                                    end)
                            end
                        end
                        
                        
                    end
                end
                end)
            end
            
            local uis = game:GetService("UserInputService")
            local bringall = false
            local hided2 = false
            local upping = false
            local downing = false
            mouse.KeyDown:Connect(function(a)
                
                if a == "t" then
                    --print("worked1")
                    f.addesp()
                elseif a == gui_hide_button[2] and uis:IsKeyDown(gui_hide_button[1]) then
                    if hided2 == false then
                        hided2 = true
                        autoesp =false
                        if espforlder then
                            espforlder:Destroy()
                        end
                        Gui.Enabled = false
                    else
                        Gui.Enabled = true
                        hided2 = false
                    end
                        
                elseif a == "y" then
                    if aimbothider == false then
                        aimbothider = true
                        if aimbothider == true then
                        aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." on"
                    else
                        aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." off"
                    end
                    else
                        
                        aimbothider = false
                        if aimbothider == true then
                        aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." on"
                    else
                        aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." off"
                    end
                    end
                    if aimbothider == true then
                        aimbothiderbox.TextColor3 =Color3.fromRGB(11, 255, 19)
                    else
                        aimbothiderbox.TextColor3 =Color3.fromRGB(255, 0, 0)
                    end
                elseif a == "l" then
                    if not uis:IsKeyDown(Enum.KeyCode.LeftControl) then
                        if autoesp == false then
                            autoesp = true
                        else
                            autoesp = false
                        end
                    else
                        if lightesp == true then
                            lightesp = false
                        else
                            lightesp = true
                        end
                    end
                elseif a == "]" then
                    upping = true
                    downing = false
                elseif a== "[" then
                    downing = true
                    upping = false
                elseif a == Aim_Assist_Key[2] and uis:IsKeyDown(Aim_Assist_Key[1]) then
                    if Aim_Assist == true then
                        Aim_Assist = false
                        --print("disabled")
                    else
                        Aim_Assist = true
                    end
                end
                if a == "j" then
                    if mouse.Target then
                        mouse.Target:Destroy()
                    end
                end
                if a == key then
                    if switch == false then
                        switch = true
                    else
                        switch = false
                        if aimatpart ~= nil then
                            aimatpart = nil
                        end
                    end
                elseif a == "b" and uis:IsKeyDown(Enum.KeyCode.LeftControl) and not uis:IsKeyDown(Enum.KeyCode.R) then
                    if movementcounting then
                        movementcounting = false
                    else
                        movementcounting = true
                    end
                elseif a == teambasedswitch then
                    if TeamBased == true then
                        TeamBased = false
                        teambasedstatus.Text = "Team Based: "..tostring(TeamBased)
                    else
                        TeamBased = true
                        teambasedstatus.Text = "Team Based: "..tostring(TeamBased)
                    end
                elseif a == "b" and uis:IsKeyDown(Enum.KeyCode.LeftControl) and uis:IsKeyDown(Enum.KeyCode.R) then
                    ballisticsboost = 0
                elseif a == aimkey then
                    if not aimatpart then
                        local maxangle = math.rad(20)
                        for i, plr in pairs(plrs:GetChildren()) do
                            if plr.Name ~= lplr.Name and plr.Character and plr.Character.Head and plr.Character.Humanoid and plr.Character.Humanoid.Health > 1 then
                                if TeamBased == true then
                                    if plr.Team.Name ~= lplr.Team.Name then
                                        local an = checkfov(plr.Character.HumanoidRootPart)
                                        if an < maxangle then
                                            maxangle = an
                                            aimatpart = plr.Character.HumanoidRootPart
                                        end
                                    end
                                else
                                    local an = checkfov(plr.Character.HumanoidRootPart)
                                        if an < maxangle then
                                            maxangle = an
                                            aimatpart = plr.Character.HumanoidRootPart
                                        end
                                        --print(plr)
                                end
                                local old = aimatpart
                                plr.Character.Humanoid.Died:Connect(function()
                                    --print("died")
                                    if aimatpart and aimatpart == old then
                                        aimatpart = nil
                                    end
                                end)
                                
                            end
                        end
                    else
                        aimatpart = nil
                        canaimat = false
                        delay(1.1, function()
                            canaimat = true
                        end)
                    end
                end
            end)
            
            function getfovxyz (p0, p1, deg)
                local x1, y1, z1 = p0:ToOrientation()
                local cf = CFrame.new(p0.p, p1.p)
                local x2, y2, z2 = cf:ToOrientation()
                local d = math.deg
                if deg then
                    return Vector3.new(d(x1-x2), d(y1-y2), d(z1-z2))
                else
                    return Vector3.new((x1-x2), (y1-y2), (z1-z2))
                end
            end
            
            
            function aimat(part)
                if part then
                    --print(part)
                    local d = (cam.CFrame.p - part.CFrame.p).magnitude
                    local calculatedrop
                    local timetoaim = 0
                    local pos2 = Vector3.new()
                    if movementcounting == true then
                        timetoaim = d/bspeed
                        pos2 = part.Velocity * timetoaim
                    end
                    local minuseddrop = (ballisticsboost+50)/50
                    if ballisticsboost ~= 0 then
                        calculatedrop = d - (d/minuseddrop)
                        
                    else
                        calculatedrop = 0
                    end
                    --print(calculatedrop)
                    local addative = Vector3.new()
                    if movementcounting then
                        addative = pos2
                    end
                    local cf = CFrame.new(cam.CFrame.p, (addative + part.CFrame.p+ Vector3.new(0, calculatedrop, 0)))
                    if aimbothider == true or Aim_Assist == true then
                        cam.CFrame = cam.CFrame:Lerp(cf, aimbothiderspeed)
                    else
                        
                        cam.CFrame = cf
                    end
                    --print(cf)
                end
            end
            function checkfov (part)
                local fov = getfovxyz(game.Workspace.CurrentCamera.CFrame, part.CFrame)
                local angle = math.abs(fov.X) + math.abs(fov.Y)
                return angle
            end
            pcall(function()
                delay(0, function()
                    while wait(.32) do
                        if Aim_Assist and not aimatpart and canaimat and lplr.Character and lplr.Character.Humanoid and lplr.Character.Humanoid.Health > 0 then
                            for i, plr in pairs(plrs:GetChildren()) do
                                
                                
                                    local minangle = math.rad(5.5)
                                    local lastpart = nil
                                    local function gg(plr)
                                        pcall(function()
                                        if plr.Name ~= lplr.Name and plr.Character and plr.Character.Humanoid and plr.Character.Humanoid.Health > 0 and plr.Character.Head then
                                            local raycasted = false
                                            local cf1 = CFrame.new(cam.CFrame.p, plr.Character.Head.CFrame.p) * CFrame.new(0, 0, -4)
                                            local r1 = Ray.new(cf1.p, cf1.LookVector * 9000)
                                            local obj, pos = game.Workspace:FindPartOnRayWithIgnoreList(r1,  {lplr.Character.Head})
                                            local dist = (plr.Character.Head.CFrame.p- pos).magnitude
                                            if dist < 4 then
                                                raycasted = true
                                            end
                                            if raycasted == true then
                                                local an1 = getfovxyz(cam.CFrame, plr.Character.Head.CFrame)
                                                local an = abs(an1.X) + abs(an1.Y)
                                                if an < minangle then
                                                    minangle = an
                                                    lastpart = plr.Character.Head
                                                end
                                            end
                                        end
                                        end)
                                    end
                                    if TeamBased then
                                        if plr.Team.Name ~= lplr.Team.Name then
                                            gg(plr)
                                        end
                                    else
                                        gg(plr)
                                    end
                                    --print(math.deg(minangle))
                                    if lastpart then
                                        aimatpart = lastpart
                                        aimatpart.Parent.Humanoid.Died:Connect(function()
                                            if aimatpart == lastpart then
                                                aimatpart = nil
                                            end
                                        end)
                                    
                                end
                            end
                        end
                    end
                end)
            end)
            local oldheadpos
            local lastaimapart
            game:GetService("RunService").RenderStepped:Connect(function(dt)
                if uis:IsKeyDown(Enum.KeyCode.RightBracket) or uis:IsKeyDown(Enum.KeyCode.LeftBracket) then
                    if upping then
                        ballisticsboost = ballisticsboost + dt/1.9
                    elseif downing then
                        ballisticsboost = ballisticsboost - dt/1.9
                    end
                end
                if movementcounting then
                    st1_2.TextColor3 = Color3.new(0.0431373, 1, 0.0745098)
                    st1_2.Text = "Current ballistics: "..tostring(math.floor(ballisticsboost*10)/10)
                else
                    st1_2.TextColor3 = Color3.new(1,0,0)
                end
                espstatustext.Text = "Esp loop :"..tostring(autoesp)
                if aimatpart and lplr.Character and lplr.Character.Head then
                    if BetterDeathCount and lastaimapart and lastaimapart == aimatpart then
                        local dist = (oldheadpos - aimatpart.CFrame.p).magnitude
                        if dist > 40 then
                            aimatpart = nil
                        end
                    end
                    lastaimapart = aimatpart
                    oldheadpos = lastaimapart.CFrame.p
                    do 
                        if aimatpart.Parent == plrs.LocalPlayer.Character then
                            aimatpart = nil
                        end
                        aimat(aimatpart)
                        pcall(function()
                            if Aim_Assist == true then
                                local cf1 = CFrame.new(cam.CFrame.p, aimatpart.CFrame.p) * CFrame.new(0, 0, -4)
                                local r1 = Ray.new(cf1.p, cf1.LookVector * 1000)
                                local obj, pos = game.Workspace:FindPartOnRayWithIgnoreList(r1,  {lplr.Character.Head})
                                local dist = (aimatpart.CFrame.p- pos).magnitude
                                if obj then
                                    --print(obj:GetFullName())
                                end
                                if not obj or dist > 6 then
                                    aimatpart = nil
                                    --print("ooof")
                                end
                                canaimat = false
                                delay(.5, function()
                                    canaimat = true
                                end)
                            end
                        end)
                    end
                    
                    
                    
                end
            end)
            
            
            delay(0, function()
                while wait(espupdatetime) do
                    if autoesp == true then
                        pcall(function()
                        f.addesp()
                        end)
                    end
                end
            end)
            --warn("loaded")
            end)
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Faded Script",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/NighterEpic/Faded/main/YesEpic", true))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Nyula",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/nyulachan/nyula/main/nyuladhm", true))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Oblivion",
	Callback = function()
        Loadstring(game:HttpGet("https://raw.githubusercontent.com/CorruptOblivion/Oblivion/main/loader.lua"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Beamed Ware",
	Callback = function()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "crimskid",
	Callback = function()
        loadstring(game:HttpGet("https://github.com/finobe7650/goodbyedahoodmodded/blob/main/crackthisidgaffinobeontop"))()
      		print("button pressed")
  	end    
})
Tab:AddButton({
	Name = "Orisis PC ONLY",
	Callback = function()
        -- source provided by chips https://www.youtube.com/channel/UCUaVppa2GUFi4_fvXw4Ayng 


if not LPH_OBFUSCATED then --  set these if not obfuscated so your script can run without obfuscation for when you are testing
    LPH_JIT_ULTRA = function(...)
        return (...)
    end
    LPH_JIT_MAX = function(...)
        return (...)
    end
end
-- dne exclusive
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/cat"))()
local LinoriaNotifs = loadstring(game:HttpGet("https://pastebin.com/raw/T8K6dsf3"))()
getgenv().WatermarkColor = Color3.fromRGB(255, 0, 125)
local DLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/dnelol/3d-drawing/main/code.lua"))()
local StrafeVisualss = DLib:New3DCircle()

local AnimationModule = {
    Astronaut = {
        "rbxassetid://891621366",
        "rbxassetid://891633237",
        "rbxassetid://891667138",
        "rbxassetid://891636393",
        "rbxassetid://891627522",
        "rbxassetid://891609353",
        "rbxassetid://891617961"
    },
    Bubbly = {
        "rbxassetid://910004836",
        "rbxassetid://910009958",
        "rbxassetid://910034870",
        "rbxassetid://910025107",
        "rbxassetid://910016857",
        "rbxassetid://910001910",
        "rbxassetid://910030921",
        "rbxassetid://910028158"
    },
    Cartoony = {
        "rbxassetid://742637544",
        "rbxassetid://742638445",
        "rbxassetid://742640026",
        "rbxassetid://742638842",
        "rbxassetid://742637942",
        "rbxassetid://742636889",
        "rbxassetid://742637151"
    },
    Confindent = {
        "rbxassetid://1069977950",
        "rbxassetid://1069987858",
        "rbxassetid://1070017263",
        "rbxassetid://1070001516",
        "rbxassetid://1069984524",
        "rbxassetid://1069946257",
        "rbxassetid://1069973677"
    },
    Cowboy = {
        "rbxassetid://1014390418",
        "rbxassetid://1014398616",
        "rbxassetid://1014421541",
        "rbxassetid://1014401683",
        "rbxassetid://1014394726",
        "rbxassetid://1014380606",
        "rbxassetid://1014384571"
    },
    Default = {
        "http://www.roblox.com/asset/?id=507766666",
        "http://www.roblox.com/asset/?id=507766951",
        "http://www.roblox.com/asset/?id=507777826",
        "http://www.roblox.com/asset/?id=507767714",
        "http://www.roblox.com/asset/?id=507765000",
        "http://www.roblox.com/asset/?id=507765644",
        "http://www.roblox.com/asset/?id=507767968"
    },
    Elder = {
        "rbxassetid://845397899",
        "rbxassetid://845400520",
        "rbxassetid://845403856",
        "rbxassetid://845386501",
        "rbxassetid://845398858",
        "rbxassetid://845392038",
        "rbxassetid://845396048"
    },
    Ghost = {
        "rbxassetid://616006778",
        "rbxassetid://616008087",
        "rbxassetid://616013216",
        "rbxassetid://616013216",
        "rbxassetid://616008936",
        "rbxassetid://616005863",
        "rbxassetid://616012453",
        "rbxassetid://616011509"
    },
    Knight = {
        "rbxassetid://657595757",
        "rbxassetid://657568135",
        "rbxassetid://657552124",
        "rbxassetid://657564596",
        "rbxassetid://658409194",
        "rbxassetid://658360781",
        "rbxassetid://657600338"
    },
    Levitation = {
        "rbxassetid://616006778",
        "rbxassetid://616008087",
        "rbxassetid://616013216",
        "rbxassetid://616010382",
        "rbxassetid://616008936",
        "rbxassetid://616003713",
        "rbxassetid://616005863"
    },
    Mage = {
        "rbxassetid://707742142",
        "rbxassetid://707855907",
        "rbxassetid://707897309",
        "rbxassetid://707861613",
        "rbxassetid://707853694",
        "rbxassetid://707826056",
        "rbxassetid://707829716"
    },
    Ninja = {
        "rbxassetid://656117400",
        "rbxassetid://656118341",
        "rbxassetid://656121766",
        "rbxassetid://656118852",
        "rbxassetid://656117878",
        "rbxassetid://656114359",
        "rbxassetid://656115606"
    },
    OldSchool = {
        "rbxassetid://5319828216",
        "rbxassetid://5319831086",
        "rbxassetid://5319847204",
        "rbxassetid://5319844329",
        "rbxassetid://5319841935",
        "rbxassetid://5319839762",
        "rbxassetid://5319852613",
        "rbxassetid://5319850266"
    },
    Patrol = {
        "rbxassetid://1149612882",
        "rbxassetid://1150842221",
        "rbxassetid://1151231493",
        "rbxassetid://1150967949",
        "rbxassetid://1148811837",
        "rbxassetid://1148811837",
        "rbxassetid://1148863382"
    },
    Pirtate = {
        "rbxassetid://750781874",
        "rbxassetid://750782770",
        "rbxassetid://750785693",
        "rbxassetid://750783738",
        "rbxassetid://750782230",
        "rbxassetid://750779899",
        "rbxassetid://750780242"
    },
    Popstar = {
        "rbxassetid://1212900985",
        "rbxassetid://1150842221",
        "rbxassetid://1212980338",
        "rbxassetid://1212980348",
        "rbxassetid://1212954642",
        "rbxassetid://1213044953",
        "rbxassetid://1212900995"
    },
    Princess = {
        "rbxassetid://941003647",
        "rbxassetid://941013098",
        "rbxassetid://941028902",
        "rbxassetid://941015281",
        "rbxassetid://941008832",
        "rbxassetid://940996062",
        "rbxassetid://941000007"
    },
    Robot = {
        "rbxassetid://616088211",
        "rbxassetid://616089559",
        "rbxassetid://616095330",
        "rbxassetid://616091570",
        "rbxassetid://616090535",
        "rbxassetid://616086039",
        "rbxassetid://616087089"
    },
    Rthro = {
        "rbxassetid://2510196951",
        "rbxassetid://2510197257",
        "rbxassetid://2510202577",
        "rbxassetid://2510198475",
        "rbxassetid://2510197830",
        "rbxassetid://2510195892",
        "rbxassetid://02510201162",
        "rbxassetid://2510199791",
        "rbxassetid://2510192778"
    },
    Sneaky = {
        "rbxassetid://1132473842",
        "rbxassetid://1132477671",
        "rbxassetid://1132510133",
        "rbxassetid://1132494274",
        "rbxassetid://1132489853",
        "rbxassetid://1132461372",
        "rbxassetid://1132469004"
    },
    Stylish = {
        "rbxassetid://616136790",
        "rbxassetid://616138447",
        "rbxassetid://616146177",
        "rbxassetid://616140816",
        "rbxassetid://616139451",
        "rbxassetid://616133594",
        "rbxassetid://616134815"
    },
    Superhero = {
        "rbxassetid://782841498",
        "rbxassetid://782845736",
        "rbxassetid://782843345",
        "rbxassetid://782842708",
        "rbxassetid://782847020",
        "rbxassetid://782843869",
        "rbxassetid://782846423"
    },
    Toy = {
        "rbxassetid://782841498",
        "rbxassetid://782845736",
        "rbxassetid://782843345",
        "rbxassetid://782842708",
        "rbxassetid://782847020",
        "rbxassetid://782843869",
        "rbxassetid://782846423"
    },
    Vampire = {
        "rbxassetid://1083445855",
        "rbxassetid://1083450166",
        "rbxassetid://1083473930",
        "rbxassetid://1083462077",
        "rbxassetid://1083455352",
        "rbxassetid://1083439238",
        "rbxassetid://1083443587"
    },
    Werewolf = {
        "rbxassetid://1083195517",
        "rbxassetid://1083214717",
        "rbxassetid://1083178339",
        "rbxassetid://1083216690",
        "rbxassetid://1083218792",
        "rbxassetid://1083182000",
        "rbxassetid://1083189019"
    },
    Zombie = {
        "rbxassetid://616158929",
        "rbxassetid://616160636",
        "rbxassetid://616168032",
        "rbxassetid://616163682",
        "rbxassetid://616161997",
        "rbxassetid://616156119",
        "rbxassetid://616157476"
    }
}

StrafeVisualss.Visible = false
StrafeVisualss.ZIndex = 1
StrafeVisualss.Transparency = 1
StrafeVisualss.Color = Color3.fromRGB(255, 255, 255)
StrafeVisualss.Thickness = 1

--// Lua guard has variables Ill change the 100th and user when released

local BodyParts = {
    "Head",
    "HumanoidRootPart",
    "Torso",
    "UpperTorso",
    "LowerTorso",
    "RightHand",
    "LeftLowerArm",
    "RightLowerArm",
    "RightUpperArm",
    "LeftLowerLeg",
    "LeftUpperLeg",
    "LeftFoot",
    "RightFoot",
    "RightUpperLeg",
    "RightLowerLeg"
}

Library.theme.topheight = 50
Library.theme.accentcolor = Color3.fromRGB(203, 9, 61)
Library.theme.accentcolor2 = Color3.fromRGB(203, 9, 61)
Library.theme.fontsize = 15
Library.theme.titlesize = 17

local CursorPath = Instance.new("ScreenGui")
local Swastika = Instance.new("TextLabel")

CursorPath.Name = "CursorPath"
CursorPath.Parent = game.CoreGui
CursorPath.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Swastika.Name = "Swastika"
Swastika.Parent = CursorPath
Swastika.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Swastika.BackgroundTransparency = 1.000
Swastika.BorderSizePixel = 2
Swastika.Position = UDim2.new(0, 0, 0, 0)
Swastika.Size = UDim2.new(0, 93, 0, 84)
Swastika.Font = Enum.Font.SourceSans
Swastika.Text = "卍"
Swastika.TextColor3 = Color3.fromRGB(0, 0, 0)
Swastika.TextSize = 46.000
Swastika.TextTransparency = 0
Swastika.Rotation = 45
Swastika.Visible = false

--[[
local Animations = game.ReplicatedStorage.ClientAnimations

local LeanAnimation = Instance.new("Animation", Animations)
LeanAnimation.Name = "Lean"
LeanAnimation.AnimationId = "rbxassetid://3152375249"

local LayAnimation = Instance.new("Animation", Animations)
LayAnimation.Name = "Lay"
LayAnimation.AnimationId = "rbxassetid://3152378852"

local Dance1Animation = Instance.new("Animation", Animations)
Dance1Animation.Name = "Dance1"
Dance1Animation.AnimationId = "rbxassetid://3189773368"

local Dance2Animation = Instance.new("Animation", Animations)
Dance2Animation.Name = "Dance2"
Dance2Animation.AnimationId = "rbxassetid://3189776546"

local GreetAnimation = Instance.new("Animation", Animations)
GreetAnimation.Name = "Greet"
GreetAnimation.AnimationId = "rbxassetid://3189777795"

local ChestPumpAnimation = Instance.new("Animation", Animations)
ChestPumpAnimation.Name = "Chest Pump"
ChestPumpAnimation.AnimationId = "rbxassetid://3189779152"

local PrayingAnimation = Instance.new("Animation", Animations)
PrayingAnimation.Name = "Praying"
PrayingAnimation.AnimationId = "rbxassetid://3487719500"
]]
local LocalPlayer = game.Players.LocalPlayer
local CC = game.Workspace.CurrentCamera
local LocalMouse = LocalPlayer:GetMouse()

--// Main Table

local Script = {
    Main = {
        Speed = false,
        SpeedPower = 2.5,
        SpeedType = "CFrame",
        InfiniteJump = false,
        FakeMacro = false
    },
    SilentAim = {
        Resolver = false,
        Part = "Head",
        Enabled = false,
        RandomBodyPart = false,
        Prediction = 0.1413
    },
    WorldViusals = {
        Ambient = nil,
        Ambient2 = nil
    },
    AntiAims = {
        JitterBot = false,
        SpinBot = false,
        SpinBotSpeed = 7
    },
    Desync = {
        Velocity = {
            Desync = false,
            Unhittable = false,
            Visualize = false,
            VisualizeColor = Color3.fromRGB(255, 0, 125),
            X = 0,
            Y = 0,
            Z = 0,
            DesyncSpinPower = 0.001,
            DesyncPower = 16
        },
        CFrame = {
            Desync = false,
            RandomMode = false,
            RandomRange = 15,
            AngleX = 0,
            AngleY = 0,
            AngleZ = 0,
            X = 0,
            Y = 0,
            Z = 0
        }
    },
    ShitTalk = {
        Enabled = false,
        Delay = 2,
        Type = "Main"
        --[[
        Emoji
        Chinese
        Main
        ]]
    },
    TargetAim = {
        Enabled = false,
        AirShotFunction = true,
        Notifications = false,
        HitNotifs = false,
        AutoPrediction = false,
        Prediction = 0.1413,
        Part = "HumanoidRootPart",
        SelectedPart = "HumanoidRootPart",
        Resolver = false,
        KnockCheck = false,
        BackWardsBang = false,
        ViewTarget = false,
        LookAt = false,
        RandomBodyPart = false
    },
    CamLock = {
        Enabled = false,
        Prediction = 0.1413,
        AutoPrediction = false,
        Resolver = false,
        Smoothness = 0,
        Part = "Head"
    },
    PartSettings = {
        PartVisible = false,
        PartRainbow = false,
        PartColor = Color3.fromRGB(255, 255, 255),
        PartSize = Vector3.new(10, 10, 10),
        PartTransparency = 0,
        PartMaterial = Enum.Material.Neon,
        PartType = Enum.PartType.Ball
    },
    Tracer = {
        Enabled = true,
        Thickness = 1,
        Color = Color3.fromRGB(255, 255, 255),
        Origin = "Mouse"
    },
    Cursor = {
        Spinning = false,
        Rainbow = false,
        SpinSpeed = 1
    },
    Strafe = {
        Enabled = false,
        DesyncStrafe = false,
        Distance = 10,
        Speed = 5,
        Height = 0,
        Visual = false,
        VisualColor = Color3.fromRGB(255, 0, 0)
    },
    RageBot = {
        Enabled = false,
        Distance = 50,
        LookAt = false,
        Resolver = false
    },
    Ratio = {
        Enabled = false,
        Amount = 80
    },
    Misc = {
        AntiBag = false,
        AutoReload = false,
        Reach = false,
        PickUpMoney = false,
        AntiStomp = false,
        NJCD = false,
        CustomGunSFX = false,
        ID = "rbxassetid://1053296915",
        Volume = 10
    },
    Settings = {
        Watermark = true,
        fpscap = 144,
        Type = "Main",
        CheatName = "midnight.cc on top "
        --game:GetService("CoreGui").osiris.main.top.title
    }
}

--[[
    },
    Tracer = {
        Enabled = true,
        Thickness = 1 ,
        Color = Color3.fromRGB(255,255,255),
    },
]]
local TargetPart = Instance.new("Part")
TargetPart.Color = Color3.fromRGB(255, 255, 255)
TargetPart.CanCollide = false
TargetPart.Size = Vector3.new(10, 10, 10)
TargetPart.Transparency = 0.8
TargetPart.Material = Enum.Material.Neon
TargetPart.Shape = Enum.PartType.Ball
TargetPart.Parent = game.Workspace
TargetPart.Anchored = true

local FOV = Drawing.new("Circle")
FOV.Filled = false
FOV.Color = Color3.fromRGB(255, 255, 255)
FOV.Visible = false
FOV.Radius = 100000

local Tracer = Drawing.new("Line")
Tracer.Visible = false
Tracer.Thickness = 1
Tracer.Color = Color3.fromRGB(255, 0, 0)

local RandomShitTalk = {
    [1] = {
        "but doctor prognosis: OWNED but doctor prognosis: OWNED but doctor prognosis: OWNED but doctor prognosis: OWNED but doctor prognosis: OWNED but doctor prognosis: OWNED ",
        "but doctor results: 🔥 but doctor results: 🔥 but doctor results: 🔥 but doctor results: 🔥 but doctor results: 🔥 but doctor results: 🔥 but doctor results: 🔥 ",
        "looks like you need to talk to your doctor looks like you need to talk to your doctor looks like you need to talk to your doctor looks like you need to talk to your doctor ",
        "speak to your doctor about this one speak to your doctor about this one speak to your doctor about this one speak to your doctor about this one speak to your doctor about this one ",
        "but analysis: PWNED but analysis: PWNED but analysis: PWNED but analysis: PWNED but analysis: PWNED but analysis: PWNED but analysis: PWNED but analysis: PWNED but analysis: PWNED ",
        "but diagnosis: OWND but diagnosis: OWND but diagnosis: OWND but diagnosis: OWND but diagnosis: OWND but diagnosis: OWND but diagnosis: OWND but diagnosis: OWND but diagnosis: OWND "
    },
    ["Chinese"] = {
        "音频少年公民记忆欲求无尽 heywe 僵尸强迫身体哑集中排水",
        "持有毁灭性的神经重景气游行脸红青铜色类别创意案",
        "诶比西迪伊艾弗吉艾尺艾杰开艾勒艾马艾娜哦屁吉吾",
        "完成与草屋两个苏巴完成与草屋两个苏巴完成与草屋",
        "庆崇你好我讨厌你愚蠢的母愚蠢的母庆崇",
        "坐下，一直保持着安静的状态。 谁把他拥有的东西给了他，所以他不那么爱欠债务，却拒  参加锻炼，这让他爱得更少了",
        ", yīzhí bǎochízhe ānjìng de zhuàngtài. Shéi bǎ tā yǒngyǒu de dōngxī gěile tā, suǒyǐ tā bù nàme ài qiàn zhàiwù, què jùjué cānjiā duànliàn, z",
        "他，所以他不那r给了他东西给了他爱欠s，却拒绝参加锻炼，这让他爱得更UGT少了",
        "有的东西给了他，所以他不那rblx trader captain么有的东西给了他爱欠绝参加锻squidward炼，务，却拒绝参加锻炼，这让他爱得更UGT少了",
        "wocky slush他爱欠债了他他squilliam拥有的东西给爱欠绝参加锻squidward炼",
        "坐下，一直保持着安静的状态 谁把他拥有的东西给了他，所以他不那rblx trader captain么有的东西给了他爱欠债了他他squilliam拥有的东西给爱欠绝参加锻squidward炼，务，却拒绝参加锻炼，这让他爱得更UGT少了",
        "免费手榴弹 hack绕过作弊工作DA HOOD roblox aimbot瞄准无声目标绕过2020工作真正免费下载和使用",
        "zal發明了roblox汽車貿易商的船長ro blocks，並將其洩漏到整個宇宙，還修補了虛假的角神模式和虛假的身體，還發明了基於速度的AUTOWALL和無限制的自動壁紙遊戲 ",
        "彼が誤って禁止されたためにファントムからautowallgamingを禁止解除する請願とそれはでたらめですそれはまったく意味がありませんなぜあなたは合法的なプレーヤーを禁止するのですか ",
        "ジェイソンは私が神に誓う女性的な男の子ではありません ",
        "傑森不是我向上帝發誓女性男孩 "
    },
    ["Emoji"] = {
        "🔥🔥🔥🔥🔥🔥🔥🔥",
        "😅😅😅😅😅😅😅😅",
        "😂😂😂😂😂😂😂😂",
        "😹😹😹😹😹😹😹😹",
        "😛😛😛😛😛😛😛😛",
        "🤩🤩🤩🤩🤩🤩🤩🤩",
        "🌈🌈🌈🌈🌈🌈🌈🌈",
        "😎😎😎😎😎😎😎😎",
        "🤠🤠🤠🤠🤠🤠🤠🤠",
        "😔😔😔😔😔😔😔😔"
    },
    ["Main"] = {
        "brb taking a nap 💤💤💤 ",
        "gonna go take a walk 🚶‍♂️🚶‍♀️🚶‍♂️🚶‍♀️ ",
        "#osiris better XD .gg/dhmscript",
        "osiris user VV 😳😳😳",
        "just a skill issue that you dont have osiris",
        "mad cause no osiris LOL .gg/dhmscript"
    }
}

function CheckWall(head)
    if v == LocalPlayer then
        return false
    end

    local castPoints = {LocalPlayer.Character.Head.Position, head.Position}
    local ignoreList = {LocalPlayer.Character, head.Parent}
    a = workspace.CurrentCamera:GetPartsObscuringTarget(castPoints, ignoreList)
    if #a == 0 then
        return false
    end

    return true
end

function IsAlive()
    if
        LocalPlayer.Character.Humanoid.Health > 0 and LocalPlayer.Character:FindFirstChild("Humanoid") and
            LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
     then
        return true
    else
        return false
    end
end

function getClosestPlayerToCursor()
    local closestPlayer

    local shortestDistance = FOV.Radius

    for i, v in pairs(game.Players:GetPlayers()) do
        if
            v ~= LocalPlayer and v.Character and v.Character:FindFirstChild("Humanoid") and
                v.Character.Humanoid.Health ~= 0 and
                v.Character:FindFirstChild("LowerTorso")
         then
            if not CheckWall(v.Character.Head) then
                local pos = CC:WorldToViewportPoint(v.Character.PrimaryPart.Position)
                local magnitude = (Vector2.new(pos.X, pos.Y) - Vector2.new(LocalMouse.X, LocalMouse.Y)).magnitude
                if magnitude < shortestDistance then
                    closestPlayer = v
                    shortestDistance = magnitude
                end
            end
        end
    end
    return closestPlayer
end

local UIS = game:GetService("UserInputService")
local RunService = game:GetService("RunService")

local VisualizerFolder = Instance.new("Folder")
VisualizerFolder.Parent = game.Workspace.Terrain

function createvisualizer()
    local Visualizer = Instance.new("Part")
    Visualizer.Anchored = true
    Visualizer.CanCollide = false
    Visualizer.Size = Vector3.new(2, 2, 2)
    Visualizer.Parent = VisualizerFolder
    Visualizer.Color = Color3.fromRGB(0, 0, 0)
    Visualizer.Shape = Enum.PartType.Ball
    if Script.Desync.Velocity.Desync and not Script.Desync.CFrame.Desync and getgenv().VisualizerVelocity ~= nil then
        Visualizer.Position = LocalPlayer.Character.HumanoidRootPart.Position + getgenv().VisualizerVelocity * 0.1413
    else
        Visualizer.CFrame = LocalPlayer.Character.HumanoidRootPart.CFrame
    end
    Visualizer.Transparency = 1
    BoxVar = Instance.new("BoxHandleAdornment", Visualizer)
    BoxVar.Name = "Box"
    BoxVar.AlwaysOnTop = true
    BoxVar.ZIndex = 4
    BoxVar.Adornee = Visualizer
    BoxVar.Color3 = Script.Desync.Velocity.VisualizeColor
    BoxVar.Transparency = 0.5
    BoxVar.Size = Visualizer.Size
    game:GetService("RunService").RenderStepped:Wait()
    Visualizer:Destroy()
end

local Window = Library:CreateWindow("osiris", Vector2.new(492, 598), Enum.KeyCode.RightShift)

--// Tabs
local Main = Window:CreateTab("Main")
local Rage = Window:CreateTab("Rage")
local Misc = Window:CreateTab("Misc")
local Visuals = Window:CreateTab("Visuals")
local Settings = Window:CreateTab("Settings")

--// Sectors
local a = Main:CreateSector("Movement", "left")
local b = Main:CreateSector("Anti Aim", "right")
local c = Misc:CreateSector("Misc", "left")
local d = Misc:CreateSector("Shit Talk", "right")
local e = Misc:CreateSector("Cursor", "right")
local f = Rage:CreateSector("Target Aim", "left")
local g = Rage:CreateSector("Part", "right")
local i = Rage:CreateSector("Tracer", "right")
local h = Visuals:CreateSector("Self Visuals", "right")
local j = Main:CreateSector("Target Strafe", "left")
local k = Rage:CreateSector("Ragebot", "left")
local l = Visuals:CreateSector("World Visuals", "right")
local n = Rage:CreateSector("Aimlock", "left")
local o = Rage:CreateSector("FOV", "right")
local p = Misc:CreateSector("Auto Buys", "left")
local q = Misc:CreateSector("Animations", "left")

local LibrarySettings = Settings:CreateSector("Settings", "left")

local Speed =
    a:AddToggle(
    "Speed",
    false,
    function(Boolean)
        Script.Main.Speed = Boolean
    end
):AddKeybind()

a:AddDropdown(
    "Method",
    {"CFrame", "BHop"},
    "CFrame",
    false,
    function(Option)
        Script.Main.SpeedType = Option

        if Option ~= "BHop" then
            LocalPlayer.Character.Humanoid.UseJumpPower = true
        end
    end
)

a:AddSlider(
    "Speed",
    0,
    1,
    100,
    1,
    function(Value)
        Script.Main.SpeedPower = Value / 40
    end
)

a:AddToggle(
    "Infinite Jump",
    false,
    function(Boolean)
        Script.Main.InfiniteJump = Boolean

        if Script.Main.InfiniteJump then
            LocalPlayer.Character.Humanoid.UseJumpPower = false
            local InfiniteJump =
                UIS.InputBegan:Connect(
                function(key)
                    if key.KeyCode == Enum.KeyCode.Space and Script.Main.InfiniteJump then
                        LocalPlayer.Character.Humanoid:ChangeState("Jumping")
                    elseif not Script.Main.InfiniteJump then
                        LocalPlayer.Character.Humanoid.UseJumpPower = true
                    end
                end
            )
        end
    end
)

a:AddToggle(
    "Fake Macro",
    false,
    function(Boolean)
        Script.Main.FakeMacro = Boolean

        if Script.Main.FakeMacro then
            local Dance = game:GetService("ReplicatedStorage").ClientAnimations.Crouching
            LoadedAnim = LocalPlayer.Character.Humanoid:LoadAnimation(Dance)
            LoadedAnim:Play()
        else
            pcall(
                function()
                    LoadedAnim:Stop()
                end
            )
        end

        while Script.Main.FakeMacro == true do
            task.wait()
            LocalPlayer.Character.HumanoidRootPart.Velocity =
                LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector * 190
        end
    end
):AddKeybind()
--[[Toggle:AddColorpicker(Color3.fromRGB(255,0,0), function(Color)
    print(Color)
end)]]
a:AddLabel("Label")

b:AddSeperator("Animations")

b:AddToggle(
    "Bicycle",
    false,
    function(Boolean)
        if Boolean then
            local Dance = game:GetService("ReplicatedStorage").ClientAnimations.Bicycling
            LoadedAnim = LocalPlayer.Character.Humanoid:LoadAnimation(Dance)
            LoadedAnim:Play()
        else
            pcall(
                function()
                    LoadedAnim:Stop()
                end
            )
        end
    end
):AddKeybind()

b:AddToggle(
    "Block",
    false,
    function(Boolean)
        if Boolean then
            local Dance = game:GetService("ReplicatedStorage").ClientAnimations.Block
            LoadedAnim = LocalPlayer.Character.Humanoid:LoadAnimation(Dance)
            LoadedAnim:Play()
        else
            pcall(
                function()
                    LoadedAnim:Stop()
                end
            )
        end
    end
):AddKeybind()

b:AddToggle(
    "Lay",
    false,
    function(Boolean)
        if Boolean then
            local Dance = LayAnimation
            LoadedAnim = LocalPlayer.Character.Humanoid:LoadAnimation(Dance)
            LoadedAnim:Play()
        else
            pcall(
                function()
                    LoadedAnim:Stop()
                end
            )
        end
    end
):AddKeybind()

b:AddToggle(
    "Lean",
    false,
    function(Boolean)
        if Boolean then
            local Dance = LeanAnimation
            LoadedAnim = LocalPlayer.Character.Humanoid:LoadAnimation(Dance)
            LoadedAnim:Play()
        else
            pcall(
                function()
                    LoadedAnim:Stop()
                end
            )
        end
    end
):AddKeybind()
--

b:AddToggle(
    "Dance1Animation",
    false,
    function(Boolean)
        if Boolean then
            local Dance = Dance1Animation
            LoadedAnim = LocalPlayer.Character.Humanoid:LoadAnimation(Dance)
            LoadedAnim:Play()
        else
            pcall(
                function()
                    LoadedAnim:Stop()
                end
            )
        end
    end
):AddKeybind()

b:AddToggle(
    "Dance2Animation",
    false,
    function(Boolean)
        if Boolean then
            local Dance = Dance2Animation
            LoadedAnim = LocalPlayer.Character.Humanoid:LoadAnimation(Dance)
            LoadedAnim:Play()
        else
            pcall(
                function()
                    LoadedAnim:Stop()
                end
            )
        end
    end
):AddKeybind()

b:AddSeperator("Visuals")

b:AddToggle(
    "Jitter",
    false,
    function(Boolean)
        Script.AntiAims.JitterBot = Boolean

        if Boolean then
            LocalPlayer.Character.Humanoid.AutoRotate = false
        else
            LocalPlayer.Character.Humanoid.AutoRotate = true
        end
    end
):AddKeybind()

b:AddToggle(
    "SpinBot",
    false,
    function(Boolean)
        Script.AntiAims.SpinBot = Boolean

        if Boolean then
            LocalPlayer.Character.Humanoid.AutoRotate = false
        else
            LocalPlayer.Character.Humanoid.AutoRotate = true
        end
    end
):AddKeybind()

b:AddSlider(
    "Spinbot Speed",
    1,
    100,
    100,
    1,
    function(Value)
        Script.AntiAims.SpinBotSpeed = Value
    end
)

b:AddSeperator("Desync")

b:AddToggle(
    "Velocity Desync",
    false,
    function(Boolean)
        Script.Desync.Velocity.Desync = Boolean
    end
):AddKeybind()

b:AddToggle(
    "Visualize",
    false,
    function(Boolean)
        Script.Desync.Velocity.Visualize = Boolean
    end
):AddColorpicker(
    Color3.fromRGB(203, 9, 61),
    function(Color)
        Script.Desync.Velocity.VisualizeColor = Color
    end
)

b:AddSlider(
    "Position X",
    -50,
    0,
    50,
    1,
    function(Value)
        Script.Desync.Velocity.X = Value / 2500
    end
)

b:AddSlider(
    "Position X",
    -50,
    0,
    50,
    1,
    function(Value)
        Script.Desync.Velocity.Y = Value / 2500
    end
)

b:AddSlider(
    "Position X",
    -50,
    0,
    50,
    1,
    function(Value)
        Script.Desync.Velocity.Z = Value / 2500
    end
)

b:AddToggle(
    "Unhittable",
    false,
    function(Boolean)
        Script.Desync.Velocity.Unhittable = Boolean
    end
)

b:AddSeperator("-")

b:AddToggle(
    "CFrame Desync",
    false,
    function(Boolean)
        Script.Desync.CFrame.Desync = Boolean
    end
):AddKeybind()

b:AddToggle(
    "Random Mode",
    false,
    function(Boolean)
        Script.Desync.CFrame.RandomMode = Boolean
    end
)

b:AddSlider(
    "Power",
    0,
    0,
    50,
    1,
    function(Value)
        Script.Desync.CFrame.RandomModePower = Value
    end
)

b:AddToggle(
    "Roll",
    false,
    function(Boolean)
        Script.Desync.CFrame.Roll = Boolean
    end
)

b:AddToggle(
    "Manual",
    false,
    function(Boolean)
        Script.Desync.CFrame.Manual = Boolean
    end
)

b:AddSlider(
    "X",
    -50,
    0,
    50,
    1,
    function(Value)
        Script.Desync.CFrame.X = Value
    end
)

b:AddSlider(
    "Y",
    -50,
    0,
    50,
    1,
    function(Value)
        Script.Desync.CFrame.Y = Value
    end
)

b:AddSlider(
    "Z",
    -50,
    0,
    50,
    1,
    function(Value)
        Script.Desync.CFrame.Z = Value
    end
)

b:AddSlider(
    "Rotation X",
    -360,
    0,
    360,
    1,
    function(Value)
        Script.Desync.CFrame.RotationX = Value
    end
)

b:AddSlider(
    "Rotation Y",
    -360,
    0,
    360,
    1,
    function(Value)
        Script.Desync.CFrame.RotationY = Value
    end
)

b:AddSlider(
    "Rotation Z",
    -360,
    0,
    360,
    1,
    function(Value)
        Script.Desync.CFrame.RotationZ = Value
    end
)

--fin0

j:AddToggle(
    "Target Strafe",
    false,
    function(Boolean)
        Script.Strafe.Enabled = Boolean
    end
)

j:AddToggle(
    "Desync Strafe",
    false,
    function(Boolean)
        Script.Strafe.DesyncStrafe = Boolean

        if Script.Desync.CFrame.Desync == false and Script.Strafe.DesyncStrafe then
            LinoriaNotifs:Notify("CFrame Desync must be enabled for this to work.", 5)
        end
    end
)

j:AddToggle(
    "Strafe Visualize",
    false,
    function(Boolean)
        Script.Strafe.Visual = Boolean
    end
):AddColorpicker(
    Color3.fromRGB(255, 255, 255),
    function(color)
        Script.Strafe.VisualColor = color
    end
)

j:AddSlider(
    "Strafe Speed",
    0,
    5,
    100,
    1,
    function(Value)
        Script.Strafe.Speed = Value
    end
)

j:AddSlider(
    "Radius",
    0,
    5,
    100,
    1,
    function(Value)
        Script.Strafe.Distance = Value
    end
)

j:AddSlider(
    "Height",
    0,
    5,
    100,
    1,
    function(Value)
        Script.Strafe.Height = Value
    end
)

d:AddDropdown(
    "Shit Talk Type",
    {"Emoji", "Main", "Chinese"},
    "Main",
    false,
    function(Option)
        Script.ShitTalk.Type = Option
    end
)

d:AddSlider(
    "Delay",
    0,
    30,
    30,
    1,
    function(Value)
        Script.ShitTalk.Delay = Value
    end
)

d:AddToggle(
    "Shit talk",
    false,
    function(Boolean)
        Script.ShitTalk.Enabled = Boolean
    end
)

local TopCursorToggle =
    e:AddToggle(
    "Top",
    true,
    function(Boolean)
        game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.Aim.Top.Visible = Boolean
    end
)

local TopCursorColor =
    TopCursorToggle:AddColorpicker(
    Color3.fromRGB(255, 255, 255),
    function(color)
        game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.Aim.Top.BackgroundColor3 = color
    end
)

local MiddleCursorToggle =
    e:AddToggle(
    "Middle",
    true,
    function(Boolean)
        game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.Aim.Visible = Boolean
    end
)

local MiddleCursorColor =
    MiddleCursorToggle:AddColorpicker(
    Color3.fromRGB(255, 255, 255),
    function(color)
        game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.Aim.BackgroundColor3 = color
    end
)

local BottomCursorToggle =
    e:AddToggle(
    "Bottom",
    true,
    function(Boolean)
        game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.Aim.Bottom.Visible = Boolean
    end
)

local BottomCursorColor =
    BottomCursorToggle:AddColorpicker(
    Color3.fromRGB(255, 255, 255),
    function(color)
        game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.Aim.Bottom.BackgroundColor3 = color
    end
)

local LeftCursorToggle =
    e:AddToggle(
    "Left",
    true,
    function(Boolean)
        game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.Aim.Left.Visible = Boolean
    end
)

local LeftCursorColor =
    LeftCursorToggle:AddColorpicker(
    Color3.fromRGB(255, 255, 255),
    function(color)
        game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.Aim.Left.BackgroundColor3 = color
    end
)

local RightCursorToggle =
    e:AddToggle(
    "Right",
    true,
    function(Boolean)
        game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.Aim.Right.Visible = Boolean
    end
)

local RightCursorColor =
    RightCursorToggle:AddColorpicker(
    Color3.fromRGB(255, 255, 255),
    function(color)
        game:GetService("Players").LocalPlayer.PlayerGui.MainScreenGui.Aim.Right.BackgroundColor3 = color
    end
)

local Spin =
    e:AddToggle(
    "Spin",
    false,
    function(Boolean)
        getgenv().SpinningCursor = Boolean
    end
)

e:AddSlider(
    "Spinning Cursor Speed",
    0,
    1,
    50,
    1,
    function(Value)
        getgenv().SpinPower = Value
    end
)

e:AddToggle(
    "Swastika",
    false,
    function(Boolean)
        Swastika.Visible = Boolean
    end
):AddColorpicker(
    Color3.fromRGB(255, 255, 255),
    function(Color)
        Swastika.TextColor3 = Color
    end
)

e:AddToggle(
    "Rainbow",
    false,
    function(Boolean)
        Script.Cursor.Rainbow = Boolean
    end
)

e:AddToggle(
    "Spinning Swastika",
    false,
    function(Boolean)
        Script.Cursor.Spin = Boolean
    end
)

e:AddSlider(
    "Swastika Spin Speed",
    0,
    1,
    5,
    1,
    function(Value)
        Script.Cursor.SpinSpeed = Value
    end
)
--// Target Aim

local Enabled =
    f:AddToggle(
    "Target Aim",
    false,
    function(Boolean)
        Script.TargetAim.Enabled = Boolean
    end
)

f:AddToggle(
    "Lock Keybind",
    false,
    function(Boolean)
        getgenv().Locking = Boolean

        if getgenv().Locking == true and Script.TargetAim.Enabled then
            getgenv().Plr = getClosestPlayerToCursor()

            local Health = getgenv().Plr.Character.Humanoid.Health

            if Script.TargetAim.LookAt then
                LocalPlayer.Character.Humanoid.AutoRotate = false
            else
                LocalPlayer.Character.Humanoid.AutoRotate = true
            end

            if Script.TargetAim.Notifications then
                LinoriaNotifs:Notify("Locked Onto: " .. getgenv().Plr.Name .. "!", 3)
            end

            if Script.Tracer.Enabled then
                Tracer.Visible = true
            end

            if Script.TargetAim.ViewTarget then
                game.Workspace.Camera.CameraSubject = getgenv().Plr.Character.Humanoid
            end

            if Script.Strafe.Enabled and not Script.Strafe.DesyncStrafe then
                if Script.Strafe.Visual then
                    StrafeVisualss.Visible = true
                    StrafeVisualss.Color = Script.Strafe.VisualColor
                    StrafeVisualss.Radius = Script.Strafe.Distance
                end

                for i = 0, 10000000, Script.Strafe.Speed do
                    task.wait()
                    if getgenv().Locking and Script.Strafe.Enabled then
                        LocalPlayer.Character.HumanoidRootPart.CFrame =
                            CFrame.new(getgenv().Plr.Character.HumanoidRootPart.Position) *
                            CFrame.Angles(0, math.rad(i), 0) *
                            CFrame.new(Script.Strafe.Distance, Script.Strafe.Height, 0)
                    end
                end
            end
        else
            game.Workspace.Camera.CameraSubject = LocalPlayer.Character.Humanoid
            LocalPlayer.Character.Humanoid.AutoRotate = true
            Tracer.Visible = false
            if getgenv().HealthNotifs then
                getgenv().HealthNotifs:Disconnect()
            end
            StrafeVisualss.Visible = false
            StrafeVisualss.Position = Vector3.new(9999, 9999, 9999)
        end
    end
):AddKeybind()

f:AddToggle(
    "Notifications",
    false,
    function(Boolean)
        Script.TargetAim.Notifications = Boolean
    end
)

f:AddToggle(
    "Knock Notifs",
    false,
    function(Boolean)
        Script.TargetAim.HitNotifs = Boolean
    end
)

f:AddTextbox(
    "Target Aim Prediction",
    nil,
    function(Text)
        Script.TargetAim.Prediction = Text
    end
)

f:AddToggle(
    "Auto Prediction",
    false,
    function(Boolean)
        Script.TargetAim.AutoPrediction = Boolean
    end
)

f:AddDropdown(
    "BodyPart",
    {
        "Head",
        "HumanoidRootPart",
        "Torso",
        "UpperTorso",
        "LowerTorso",
        "RightHand",
        "LeftLowerArm",
        "RightLowerArm",
        "RightUpperArm",
        "LeftLowerLeg",
        "LeftUpperLeg",
        "LeftFoot",
        "RightFoot",
        "RightUpperLeg",
        "RightLowerLeg"
    },
    "HumanoidRootPart",
    false,
    function(Option)
        Script.TargetAim.Part = Option
        Script.TargetAim.SelectedPart = Option
    end
)

f:AddToggle(
    "Random Body HitPart",
    false,
    function(Boolean)
        Script.TargetAim.RandomBodyPart = Boolean
    end
)

f:AddToggle(
    "Resolver",
    false,
    function(Boolean)
        Script.TargetAim.Resolver = Boolean
    end
)

f:AddToggle(
    "View Target",
    false,
    function(Boolean)
        Script.TargetAim.ViewTarget = Boolean
    end
)

f:AddToggle(
    "Look At",
    false,
    function(Boolean)
        Script.TargetAim.LookAt = Boolean
    end
)

k:AddToggle(
    "RageBot",
    false,
    function(Boolean)
        Script.RageBot.Enabled = Boolean
    end
):AddKeybind()

k:AddToggle(
    "LookAt",
    false,
    function(Boolean)
        Script.RageBot.LookAt = Boolean
    end
)

k:AddToggle(
    "Resolver",
    false,
    function(Boolean)
        Script.RageBot.Resolver = Boolean
    end
)

k:AddSlider(
    "Distance",
    0,
    50,
    200,
    1,
    function(Value)
        Script.RageBot.Distance = Value
    end
)

g:AddToggle(
    "Part Enabled",
    false,
    function(Boolean)
        Script.PartSettings.PartVisible = Boolean
    end
):AddColorpicker(
    Color3.fromRGB(255, 0, 0),
    function(Color)
        Script.PartSettings.PartColor = Color
    end
)

g:AddToggle(
    "Rainbow Part",
    false,
    function(Boolean)
        Script.PartSettings.PartRainbow = Boolean
    end
)

g:AddSlider(
    "Size",
    0,
    6,
    100,
    1,
    function(Value)
        Script.PartSettings.PartSize = Vector3.new(Value, Value, Value)
    end
)

g:AddSlider(
    "Transparency",
    0,
    1,
    10,
    1,
    function(Value)
        Script.PartSettings.PartTransparency = Value / 10
    end
)

g:AddDropdown(
    "Material",
    {"Neon", "Plastic", "ForceField"},
    "ForceField",
    false,
    function(Option)
        Script.PartSettings.PartMaterial = Enum.Material[Option]
    end
)

g:AddDropdown(
    "Shape",
    {"Cylinder", "Block", "Ball"},
    "Block",
    false,
    function(Option)
        Script.PartSettings.PartType = Enum.PartType[Option]
    end
)

l:AddToggle(
    "Bullet Tracers",
    false,
    function(Boolean)
        BulletTracers = Boolean
    end
):AddColorpicker(
    Color3.fromRGB(255, 0, 0),
    function(Color)
        BulletTracerColor = Color
    end
)

l:AddSlider(
    "Bullet Thickness",
    0,
    5,
    10,
    1,
    function(Value)
        BulletWidth = Value
    end
)

l:AddToggle(
    "Custom Gun SFX",
    false,
    function(Boolean)
        Script.Misc.CustomGunSFX = Boolean
    end
)

l:AddTextbox(
    "ID",
    nil,
    function(Text)
        Script.Misc.ID = "rbxassetid://" .. Text .. ""
    end
)

l:AddSlider(
    "Volume",
    0,
    5,
    10,
    1,
    function(Value)
        Script.Misc.Volume = Value
    end
)

local Ambient =
    l:AddToggle(
    "Ambient",
    false,
    function(Boolean)
        Ambient = Boolean

        if not Ambient then
            game:GetService("Lighting").OutdoorAmbient = Color3.fromRGB(152, 152, 146)
            game:GetService("Lighting").Ambient = Color3.fromRGB(0, 0, 0)
        end
    end
)

game:GetService("Lighting").Ambient = Color3.fromRGB(0, 0, 0)
game:GetService("Lighting").OutdoorAmbient = Color3.fromRGB(152, 152, 146)

Ambient:AddColorpicker(
    Color3.fromRGB(255, 255, 255),
    function(Color)
        if Ambient then
            game:GetService("Lighting").Ambient = Color
        end
    end
)

game:GetService("Lighting").Ambient = Color3.fromRGB(0, 0, 0)
game:GetService("Lighting").OutdoorAmbient = Color3.fromRGB(152, 152, 146)

Ambient:AddColorpicker(
    Color3.fromRGB(255, 255, 255),
    function(Color)
        if Ambient then
            game:GetService("Lighting").OutdoorAmbient = Color
        end
    end
)

game:GetService("Lighting").Ambient = Color3.fromRGB(0, 0, 0)
game:GetService("Lighting").OutdoorAmbient = Color3.fromRGB(152, 152, 146)

local highlight =
    h:AddToggle(
    "Shadow",
    false,
    function(state)
        FFBody = state

        if not FFBody then
            if LocalPlayer.Character then
                for i, v in pairs(LocalPlayer.Character:GetChildren()) do
                    if v:IsA("BasePart") then
                        v.Material = Enum.Material.Plastic
                    end
                end
            end
        end
    end
)

function Weld(x, y)
    local W = Instance.new("Weld")
    W.Part0 = x
    W.Part1 = y
    local CJ = CFrame.new(x.Position)
    local C0 = x.CFrame:inverse() * CJ
    local C1 = y.CFrame:inverse() * CJ
    W.C0 = C0
    W.C1 = C1
    W.Parent = x
end

h:AddToggle(
    "Custom Character",
    false,
    function(state)
        if state then
            for i, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                if v:IsA("BasePart") or v:IsA("Decal") then
                    v.Transparency = 1
                end
            end

            getgenv().Custom =
                LocalPlayer.Character:WaitForChild("Humanoid").Died:Connect(
                function()
                    fuc:Destroy()
                    wait(5)
                    fuc = Instance.new("Part", workspace)
                    fuc.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
                    fuc.CanCollide = false
                    fuck = Instance.new("SpecialMesh")
                    fuck.Parent = fuc
                    fuck.MeshType = "FileMesh"
                    if getgenv().CharacterType == "AmongUs" then
                        fuck.Scale = Vector3.new(0.2, 0.2, 0.2)
                        fuck.TextureId = "http://www.roblox.com/asset/?id=6686375937"
                        fuck.MeshId = "http://www.roblox.com/asset/?id=6686375902"
                    elseif getgenv().CharacterType == "Stewie" then
                        fuck.Scale = Vector3.new(0.1, 0.1, 0.1)
                        fuck.TextureId = "http://www.roblox.com/asset/?id=3692134820"
                        fuck.MeshId = "http://www.roblox.com/asset/?id=3692134742"
                    elseif getgenv().CharacterType == "Sonic" then
                        fuck.Scale = Vector3.new(0.1, 0.1, 0.1)
                        fuck.TextureId = "http://www.roblox.com/asset/?id=6901422268"
                        fuck.MeshId = "http://www.roblox.com/asset/?id=6901422170"
                    elseif getgenv().CharacterType == "Chicken" then
                        fuck.Scale = Vector3.new(3, 3, 3)
                        fuck.TextureId = "http://www.roblox.com/asset/?id=2114220248"
                        fuck.MeshId = "http://www.roblox.com/asset/?id=2114220154"
                    end

                    Weld(game.Players.LocalPlayer.Character.HumanoidRootPart, fuc)

                    for i, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                        if v:IsA("BasePart") or v:IsA("Decal") then
                            v.Transparency = 1
                        end
                    end
                end
            )

            fuc = Instance.new("Part", workspace)
            fuc.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            fuc.CanCollide = false
            fuck = Instance.new("SpecialMesh")
            fuck.Parent = fuc
            fuck.MeshType = "FileMesh"

            if getgenv().CharacterType == "AmongUs" then
                fuck.Scale = Vector3.new(0.2, 0.2, 0.2) --sizerbxassetid://6901422268
                fuck.TextureId = "http://www.roblox.com/asset/?id=6686375937" --Texture / Skin
                fuck.MeshId = "http://www.roblox.com/asset/?id=6686375902" -- Mesh Id
            elseif getgenv().CharacterType == "Stewie" then
                fuck.Scale = Vector3.new(0.1, 0.1, 0.1) --sizerbxassetid://6901422268
                fuck.TextureId = "http://www.roblox.com/asset/?id=3692134820" --Texture / Skin
                fuck.MeshId = "http://www.roblox.com/asset/?id=3692134742" -- Mesh Id
            elseif getgenv().CharacterType == "Sonic" then
                fuck.Scale = Vector3.new(0.1, 0.1, 0.1) --sizerbxassetid://6901422268
                fuck.TextureId = "http://www.roblox.com/asset/?id=6901422268" --Texture / Skin
                fuck.MeshId = "http://www.roblox.com/asset/?id=6901422170"
            elseif getgenv().CharacterType == "Chicken" then
                fuck.Scale = Vector3.new(3, 3, 3) --sizerbxassetid://6901422268
                fuck.TextureId = "http://www.roblox.com/asset/?id=2114220248" --Texture / Skin
                fuck.MeshId = "http://www.roblox.com/asset/?id=2114220154" -- Mesh Id
            end

            Weld(game.Players.LocalPlayer.Character.HumanoidRootPart, fuc)
        else
            fuc:Destroy()

            for i, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                if v:IsA("BasePart") or v:IsA("Decal") and v.Name ~= "CUFF" then
                    v.Transparency = 0
                end

                if v.Name == "CUFF" then
                    v:Destroy()
                end
            end

            for i, v in pairs(LocalPlayer.Character.BodyEffects.SpecialParts:GetDescendants()) do
                if v:IsA("BasePart") or v:IsA("Decal") then
                    v.Transparency = 1
                end
            end

            getgenv().Custom:Disconnect()

            LocalPlayer.Character.HumanoidRootPart.Transparency = 1
        end
    end
)

h:AddDropdown(
    "Character Type",
    {"AmongUs", "Stewie", "Sonic", "Chicken"},
    "AmongUs",
    false,
    function(Option)
        getgenv().CharacterType = Option

        if Option == "AmongUs" then
            fuck.Scale = Vector3.new(0.2, 0.2, 0.2) --sizerbxassetid://6901422268
            fuck.TextureId = "http://www.roblox.com/asset/?id=6686375937" --Texture / Skin
            fuck.MeshId = "http://www.roblox.com/asset/?id=6686375902" -- Mesh Id
        elseif Option == "Stewie" then
            fuck.Scale = Vector3.new(0.1, 0.1, 0.1) --sizerbxassetid://6901422268
            fuck.TextureId = "http://www.roblox.com/asset/?id=3692134820" --Texture / Skin
            fuck.MeshId = "http://www.roblox.com/asset/?id=3692134742" -- Mesh Id
        elseif Option == "Sonic" then
            fuck.Scale = Vector3.new(0.25, 0.25, 0.25) --sizerbxassetid://6901422268
            fuck.TextureId = "http://www.roblox.com/asset/?id=6901422268" --Texture / Skin
            fuck.MeshId = "http://www.roblox.com/asset/?id=6901422170"
        elseif Option == "Chicken" then
            fuck.Scale = Vector3.new(3, 3, 3) --sizerbxassetid://6901422268
            fuck.TextureId = "http://www.roblox.com/asset/?id=2114220248" --Texture / Skin
            fuck.MeshId = "http://www.roblox.com/asset/?id=2114220154" -- Mesh Id
        end
    end
)

highlight:AddColorpicker(
    Color3.fromRGB(255, 255, 255),
    function(Color)
        FFBodyColour = Color
    end
)

local skybox = Instance.new("Sky")
skybox.Parent = game.Lighting
skybox.SkyboxBk = "rbxassetid://600830446"
skybox.SkyboxDn = "rbxassetid://600831635"
skybox.SkyboxFt = "rbxassetid://600832720"
skybox.SkyboxLf = "rbxassetid://600886090"
skybox.SkyboxRt = "rbxassetid://600833862"
skybox.SkyboxUp = "rbxassetid://600835177"

l:AddToggle(
    "Custom Skyboxes",
    false,
    function(Boolean)
        getgenv().Skybox = Boolean

        if not getgenv().Skybox then
            skybox.SkyboxBk = "rbxassetid://600830446"
            skybox.SkyboxDn = "rbxassetid://600831635"
            skybox.SkyboxFt = "rbxassetid://600832720"
            skybox.SkyboxLf = "rbxassetid://600886090"
            skybox.SkyboxRt = "rbxassetid://600833862"
            skybox.SkyboxUp = "rbxassetid://600835177"
        end
    end
)

l:AddDropdown(
    "Skybox",
    {"Normal", "DoomSpire", "CatGirl", "Vibe", "Blue Aurora"},
    "Normal",
    false,
    function(Option)
        getgenv().SkyBoxOption = Option

        if getgenv().Skybox then
            if getgenv().SkyBoxOption == "DoomSpire" then
                skybox.SkyboxBk = "rbxassetid://6050664592"
                skybox.SkyboxDn = "rbxassetid://6050648475"
                skybox.SkyboxFt = "rbxassetid://6050644331"
                skybox.SkyboxLf = "rbxassetid://6050649245"
                skybox.SkyboxRt = "rbxassetid://6050649718"
                skybox.SkyboxUp = "rbxassetid://6050650083"
            elseif getgenv().SkyBoxOption == "Normal" then
                skybox.SkyboxBk = "rbxassetid://600830446"
                skybox.SkyboxDn = "rbxassetid://600831635"
                skybox.SkyboxFt = "rbxassetid://600832720"
                skybox.SkyboxLf = "rbxassetid://600886090"
                skybox.SkyboxRt = "rbxassetid://600833862"
                skybox.SkyboxUp = "rbxassetid://600835177"
            elseif getgenv().SkyBoxOption == "CatGirl" then
                skybox.SkyboxBk = "rbxassetid://444167615"
                skybox.SkyboxDn = "rbxassetid://444167615"
                skybox.SkyboxFt = "rbxassetid://444167615"
                skybox.SkyboxLf = "rbxassetid://444167615"
                skybox.SkyboxRt = "rbxassetid://444167615"
                skybox.SkyboxUp = "rbxassetid://444167615"
            elseif getgenv().SkyBoxOption == "Vibe" then
                skybox.SkyboxBk = "rbxassetid://1417494030"
                skybox.SkyboxDn = "rbxassetid://1417494146"
                skybox.SkyboxFt = "rbxassetid://1417494253"
                skybox.SkyboxLf = "rbxassetid://1417494402"
                skybox.SkyboxRt = "rbxassetid://1417494499"
                skybox.SkyboxUp = "rbxassetid://1417494643"
            elseif getgenv().SkyBoxOption == "Blue Aurora" then
                skybox.SkyboxBk = "rbxassetid://12064107"
                skybox.SkyboxDn = "rbxassetid://12064152"
                skybox.SkyboxFt = "rbxassetid://12064121"
                skybox.SkyboxLf = "rbxassetid://12063984"
                skybox.SkyboxRt = "rbxassetid://12064115"
                skybox.SkyboxUp = "rbxassetid://12064131"
            end
        end
    end
)

---

i:AddToggle(
    "Tracer",
    false,
    function(Boolean)
        Script.Tracer.Enabled = Boolean

        if Script.Tracer.Enabled == false then
            Tracer.Visible = false
        end
    end
):AddColorpicker(
    Color3.fromRGB(255, 0, 0),
    function(Color)
        Script.Tracer.Color = Color

        Tracer.Color = Script.Tracer.Color
    end
)

i:AddSlider(
    "Tracer Thickness",
    0,
    1,
    10,
    1,
    function(Value)
        Script.Tracer.Thickness = Value

        Tracer.Thickness = Script.Tracer.Thickness
    end
)

i:AddDropdown(
    "Origin",
    {"Mouse", "Character"},
    "Mouse",
    false,
    function(Option)
        Script.Tracer.Origin = Option
    end
)

c:AddToggle(
    "Auto Stomp",
    false,
    function(state)
        Script.Misc.AutoStomp = state
    end
)

c:AddToggle(
    "Auto Reload",
    false,
    function(state)
        Script.Misc.AutoReload = state
    end
)

c:AddToggle(
    "Pick-Up Monkey",
    false,
    function(state)
        Script.Misc.PickUpMoney = state
    end
)

c:AddToggle(
    "Anti Stomp",
    false,
    function(state)
        Script.Misc.AntiStomp = state
    end
)

c:AddToggle(
    "Anti Bag",
    false,
    function(state)
        Script.Misc.AntiBag = state
    end
)

c:AddToggle(
    "Jump Cooldown",
    true,
    function(state)
        LocalPlayer.Character.Humanoid.UseJumpPower = state
    end
)

----------------------------------------------------------------------------------
----------------------------------------------------------------------------------
--------------------------------SETTINGS BELLOW-----------------------------------
----------------------------------------------------------------------------------
----------------------------------------------------------------------------------
Settings:CreateConfigSystem("right")

LibrarySettings:AddTextbox(
    "Watermark Name",
    nil,
    function(Text)
        Script.Settings.CheatName = Text
        Library:CreateWatermark("" .. Script.Settings.CheatName .. " | {fps} | {game}")
    end
)

LibrarySettings:AddToggle(
    "Watermark",
    true,
    function(Boolean)
        game:GetService("CoreGui").Watermark.Enabled = Boolean
    end
)

LibrarySettings:AddToggle(
    "No FPS Cap",
    true,
    function(Boolean)
        if Boolean then
            setfpscap(99999)
        end
    end
)

LibrarySettings:AddTextbox(
    "FPS Cap",
    nil,
    function(Text)
        setfpscap(Text)
    end
)

--[[
        Enabled = false,
        Prediction = 0.1413,
        AutoPrediction = false,
        Resolver = false

]]
n:AddToggle(
    "CamLock",
    false,
    function(state)
        Script.CamLock.Enabled = state
    end
)

n:AddToggle(
    "KeyBind",
    false,
    function(state)
        getgenv().CamLocking = state

        if getgenv().CamLocking and Script.CamLock.Enabled == true then
            getgenv().CLT = getClosestPlayerToCursor()
        end
    end
):AddKeybind()

n:AddTextbox(
    "CamLock Prediction",
    nil,
    function(Text)
        Script.CamLock.Prediction = Text
    end
)

n:AddDropdown(
    "Camlock Part",
    {"Head", "HumanoidRootPart", "UpperTorso", "LowerTorso"},
    "Head",
    false,
    function(Option)
        Script.CamLock.Part = Option
    end
)

n:AddSlider(
    "Smoothness",
    0,
    100,
    100,
    1,
    function(Value)
        Script.CamLock.Smoothness = Value / 100
    end
)

n:AddToggle(
    "Resolver",
    false,
    function(state)
        Script.CamLock.Resolver = state
    end
)

--// FOV

local fov =
    o:AddToggle(
    "FOV",
    false,
    function(state)
        FOV.Visible = state

        if FOV.Visible == false then
            FOV.Radius = math.huge
        else
            FOV.Radius = abc
        end
    end
)

fov:AddColorpicker(
    Color3.fromRGB(255, 255, 255),
    function(Color)
        FOV.Color = Color
    end
)

fov:AddKeybind()

o:AddToggle(
    "FOV Filled",
    false,
    function(state)
        FOV.Filled = state
    end
)

o:AddSlider(
    "FOV Radius",
    0,
    200,
    1000,
    1,
    function(Value)
        FOV.Radius = Value
        abc = Value
    end
)

o:AddSlider(
    "FOV Transparency",
    0,
    10,
    10,
    1,
    function(Value)
        FOV.Transparency = Value / 10
    end
)

o:AddSlider(
    "FOV Sides",
    0,
    100,
    100,
    1,
    function(Value)
        FOV.NumSides = Value
    end
)

o:AddSlider(
    "FOV Thickness",
    0,
    5,
    10,
    1,
    function(Value)
        FOV.Thickness = Value / 3.33333
    end
)

local BuysUwu =
    p:AddDropdown(
    "Other",
    Buys,
    "Pick me",
    false,
    function(Option)
        if Option then
            local OldPosition = LocalPlayer.Character.HumanoidRootPart.CFrame
            LocalPlayer.Character.HumanoidRootPart.CFrame =
                game:GetService("Workspace").Ignored.Shop[Option].Head.CFrame
            wait(0.5)
            fireclickdetector(game:GetService("Workspace").Ignored.Shop[Option].ClickDetector)
            fireclickdetector(game:GetService("Workspace").Ignored.Shop[Option].ClickDetector)
            fireclickdetector(game:GetService("Workspace").Ignored.Shop[Option].ClickDetector)
            fireclickdetector(game:GetService("Workspace").Ignored.Shop[Option].ClickDetector)
            fireclickdetector(game:GetService("Workspace").Ignored.Shop[Option].ClickDetector)
            fireclickdetector(game:GetService("Workspace").Ignored.Shop[Option].ClickDetector)
            wait(0.5)
            LocalPlayer.Character.HumanoidRootPart.CFrame = OldPosition
        end
    end
)

local BuyOptions =
    p:AddDropdown(
    "Ammo",
    Buys,
    "Ammo",
    false,
    function(Option)
        if Option then
            local OldPosition = LocalPlayer.Character.HumanoidRootPart.CFrame
            LocalPlayer.Character.HumanoidRootPart.CFrame =
                game:GetService("Workspace").Ignored.Shop[Option].Head.CFrame
            wait(0.5)
            fireclickdetector(game:GetService("Workspace").Ignored.Shop[Option].ClickDetector)
            fireclickdetector(game:GetService("Workspace").Ignored.Shop[Option].ClickDetector)
            fireclickdetector(game:GetService("Workspace").Ignored.Shop[Option].ClickDetector)
            fireclickdetector(game:GetService("Workspace").Ignored.Shop[Option].ClickDetector)
            fireclickdetector(game:GetService("Workspace").Ignored.Shop[Option].ClickDetector)
            fireclickdetector(game:GetService("Workspace").Ignored.Shop[Option].ClickDetector)
            wait(0.5)
            LocalPlayer.Character.HumanoidRootPart.CFrame = OldPosition
        end
    end
)

local Buys = {}
--[[
for i,v in pairs(game:GetService("Workspace").Ignored.Shop:GetChildren()) do 
    if v:IsA("Model") then 
        if not string.match(v.Name, "Ammo") then
            if not string.match(v.Name, "Phone") then 
                if not string.match(v.Name, "Mask") then 
                    if not string.match(v.Name, "Weights") then 
                        BuysUwu:Add(v.Name)
                    end 
                end 
            end 
        end 
    end 
end 

for i,v in pairs(game:GetService("Workspace").Ignored.Shop:GetChildren()) do 
    if v:IsA("Model") then 
        if string.match(v.Name, "Ammo") then
            BuyOptions:Add(v.Name)
        end 
    end 
end 
]]
q:AddToggle(
    "Animation Changer",
    false,
    function(state)
        Anim = state
    end
)

q:AddDropdown(
    "Idle",
    {
        "Nothing",
        "Astronaut",
        "Bubbly",
        "Cartoony",
        "Confindent",
        "Cowboy",
        "Zombie",
        "Elder",
        "Ghost",
        "Knight",
        "Levitation",
        "Mage",
        "Astronaut",
        "Ninja",
        "OldSchool",
        "Patrol",
        "Pirate",
        "Popstar",
        "Princess",
        "Robot",
        "Rthro",
        "Stylish",
        "Superhero",
        "Toy",
        "Vampire",
        "Werewolf"
    },
    "Rthro",
    false,
    function(Option)
        local ballocks = Option

        if Anim then
            while wait(3) do
                if Anim then
                    LocalPlayer.Character.Animate.idle.Animation1.AnimationId = AnimationModule[ballocks][1]
                    LocalPlayer.Character.Animate.idle.Animation2.AnimationId = AnimationModule[ballocks][2]
                end
            end
        end
    end
)

q:AddDropdown(
    "Walk",
    {
        "Nothing",
        "Astronaut",
        "Bubbly",
        "Cartoony",
        "Confindent",
        "Cowboy",
        "Zombie",
        "Elder",
        "Ghost",
        "Knight",
        "Levitation",
        "Mage",
        "Astronaut",
        "Ninja",
        "OldSchool",
        "Patrol",
        "Pirate",
        "Popstar",
        "Princess",
        "Robot",
        "Rthro",
        "Stylish",
        "Superhero",
        "Toy",
        "Vampire",
        "Werewolf"
    },
    "Rthro",
    false,
    function(Option)
        local ballockss = Option

        if Anim then
            while wait(3) do
                if Anim then
                    LocalPlayer.Character.Animate.walk.WalkAnim.AnimationId = AnimationModule[ballockss][3]
                end
            end
        end
    end
)

q:AddDropdown(
    "Run",
    {
        "Nothing",
        "Astronaut",
        "Bubbly",
        "Cartoony",
        "Confindent",
        "Cowboy",
        "Zombie",
        "Elder",
        "Ghost",
        "Knight",
        "Levitation",
        "Mage",
        "Astronaut",
        "Ninja",
        "OldSchool",
        "Patrol",
        "Pirate",
        "Popstar",
        "Princess",
        "Robot",
        "Rthro",
        "Stylish",
        "Superhero",
        "Toy",
        "Vampire",
        "Werewolf"
    },
    "Rthro",
    false,
    function(Option)
        local Run = Option

        if Anim then
            while wait(3) do
                if Anim then
                    LocalPlayer.Character.Animate.run.RunAnim.AnimationId = AnimationModule[Run][4]
                end
            end
        end
    end
)

q:AddDropdown(
    "Fall",
    {
        "Nothing",
        "Astronaut",
        "Bubbly",
        "Cartoony",
        "Confindent",
        "Cowboy",
        "Zombie",
        "Elder",
        "Ghost",
        "Knight",
        "Levitation",
        "Mage",
        "Astronaut",
        "Ninja",
        "OldSchool",
        "Patrol",
        "Pirate",
        "Popstar",
        "Princess",
        "Robot",
        "Rthro",
        "Stylish",
        "Superhero",
        "Toy",
        "Vampire",
        "Werewolf"
    },
    "Rthro",
    false,
    function(Option)
        local fall = Option

        if Anim then
            while wait(3) do
                if Anim then
                    LocalPlayer.Character.Animate.fall.FallAnim.AnimationId = AnimationModule[fall][7]
                end
            end
        end
    end
)

q:AddDropdown(
    "Jump",
    {
        "Nothing",
        "Astronaut",
        "Bubbly",
        "Cartoony",
        "Confindent",
        "Cowboy",
        "Zombie",
        "Elder",
        "Ghost",
        "Knight",
        "Levitation",
        "Mage",
        "Astronaut",
        "Ninja",
        "OldSchool",
        "Patrol",
        "Pirate",
        "Popstar",
        "Princess",
        "Robot",
        "Rthro",
        "Stylish",
        "Superhero",
        "Toy",
        "Vampire",
        "Werewolf"
    },
    "Rthro",
    false,
    function(Option)
        local pooop = Option

        if Anim then
            while wait(3) do
                if Anim then
                    LocalPlayer.Character.Animate.jump.JumpAnim.AnimationId = AnimationModule[pooop][5]
                end
            end
        end
    end
)

LPH_JIT_ULTRA(
    function()
        RunService.heartbeat:Connect(
            function()
                for _, v in pairs(LocalPlayer.Character:GetChildren()) do
                    if v:IsA("Script") and v.Name ~= "Health" and v.Name ~= "Sound" and v:FindFirstChild("LocalScript") then
                        v:Destroy()
                    end
                end

                if FOV.Visible then
                    FOV.Position = Vector2.new(LocalMouse.X, LocalMouse.Y + 36)
                end

                if getgenv().CamLocking then
                    if getgenv().CLT ~= nil then
                        local Pos, OnScreen = CC:WorldToViewportPoint(getgenv().CLT.Character.Head.Position)
                        if OnScreen and Script.CamLock.Enabled then
                            if Script.CamLock.Resolver then
                                getgenv().Main =
                                    CFrame.new(
                                    CC.CFrame.p,
                                    getgenv().CLT.Character[Script.CamLock.Part].Position +
                                        (getgenv().CLT.Character.Humanoid.MoveDirection * 3)
                                )
                                CC.CFrame =
                                    CC.CFrame:Lerp(
                                    getgenv().Main,
                                    Script.CamLock.Smoothness,
                                    Enum.EasingStyle.Elastic,
                                    Enum.EasingDirection.InOut
                                )
                            else
                                getgenv().Main =
                                    CFrame.new(
                                    CC.CFrame.p,
                                    getgenv().CLT.Character[Script.CamLock.Part].Position +
                                        (getgenv().CLT.Character.HumanoidRootPart.Velocity * Script.CamLock.Prediction)
                                )
                                CC.CFrame =
                                    CC.CFrame:Lerp(
                                    getgenv().Main,
                                    Script.CamLock.Smoothness,
                                    Enum.EasingStyle.Elastic,
                                    Enum.EasingDirection.InOut
                                )
                            end
                        end
                    end
                end

                if Script.Misc.AutoReload then
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChildWhichIsA("Tool") ~= nil then
                        if
                            game:GetService("Players").LocalPlayer.Character:FindFirstChildWhichIsA("Tool"):FindFirstChild(
                                "Ammo"
                            )
                         then
                            if
                                game:GetService("Players").LocalPlayer.Character:FindFirstChildWhichIsA("Tool"):FindFirstChild(
                                    "Ammo"
                                ).Value <= 0
                             then
                                game:GetService("ReplicatedStorage").MainEvent:FireServer(
                                    "Reload",
                                    game:GetService("Players").LocalPlayer.Character:FindFirstChildWhichIsA("Tool")
                                )
                            end
                        end
                    end
                end

                if Script.Misc.CustomGunSFX then
                    for i, v in pairs(LocalPlayer.Character:GetDescendants()) do
                        if v:IsA("Sound") and v.Name == "ShootSound" then
                            v.SoundId = Script.Misc.ID
                            v.Volume = Script.Misc.Volume
                        end
                    end
                end

                if Script.Misc.PickUpMoney then
                    for __, v in pairs(game:GetService("Workspace").Ignored.Drop:GetChildren()) do
                        if v.Name == "MoneyDrop" then
                            if (v.Position - LocalPlayer.Character.HumanoidRootPart.Position).Magnitude < 25 then
                                fireclickdetector(v.ClickDetector)
                            end
                        end
                    end
                end

                if Script.Misc.AntiBag then
                    if LocalPlayer.Character:FindFirstChild("Christmas_Sock") then
                        LocalPlayer.Character["Christmas_Sock"]:Destroy()
                    end
                end

                if Script.Misc.AntiStomp then
                    if LocalPlayer.Character.Humanoid.Health < 50 then
                        for __, v in pairs(LocalPlayer.Character:GetDescendants()) do
                            if v:IsA("BasePart") then
                                v:Destroy()
                            end
                        end
                    end
                end

                if Script.Misc.AutoStomp then
                    game.ReplicatedStorage.MainEvent:FireServer("Stomp")
                end

                if Swastika.Visible then
                    CursorPath.Swastika.Position = UDim2.fromOffset(LocalMouse.X - 43, LocalMouse.Y - 39)

                    if Script.Cursor.Rainbow then
                        CursorPath.Swastika.TextColor3 = Color3.fromHSV(tick() % 6 / 6, 1, 1)
                    end

                    if Script.Cursor.Spin == true then
                        CursorPath.Swastika.Rotation = CursorPath.Swastika.Rotation + Script.Cursor.SpinSpeed
                    end
                end

                if BulletTracers then
                    local ColourSequence =
                        ColorSequence.new(
                        {
                            ColorSequenceKeypoint.new(0, BulletTracerColor),
                            ColorSequenceKeypoint.new(1, BulletTracerColor)
                        }
                    )

                    for _, v in pairs(game:GetService("Workspace").Ignored:GetDescendants()) do
                        if v.Name == "BULLET_RAYS" then
                            if 100 > (v.Position - LocalPlayer.Character.HumanoidRootPart.Position).Magnitude then
                                v.GunBeam.Texture = "http://www.roblox.com/asset/?id=9150561638"
                                v.GunBeam.Width0 = BulletWidth
                                v.GunBeam.Width1 = BulletWidth
                                v.GunBeam.Color = ColourSequence
                            end
                        end
                    end
                end

                if Script.Main.Speed then
                    if Script.Main.SpeedType == "CFrame" then
                        LocalPlayer.Character.HumanoidRootPart.CFrame =
                            LocalPlayer.Character.HumanoidRootPart.CFrame +
                            LocalPlayer.Character.Humanoid.MoveDirection * Script.Main.SpeedPower
                    elseif Script.Main.SpeedType == "BHop" then
                        LocalPlayer.Character.HumanoidRootPart.CFrame =
                            LocalPlayer.Character.HumanoidRootPart.CFrame +
                            LocalPlayer.Character.Humanoid.MoveDirection * Script.Main.SpeedPower
                        if
                            LocalPlayer.Character.Humanoid.MoveDirection.Magnitude > 0 and
                                LocalPlayer.Character.Humanoid:GetState() ~= Enum.HumanoidStateType.Freefall
                         then
                            LocalPlayer.Character.Humanoid.UseJumpPower = false
                            LocalPlayer.Character.Humanoid:ChangeState("Jumping")
                        end
                    end
                end

                if Script.RageBot.Enabled then
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChildWhichIsA("Tool") ~= nil then
                        if
                            game:GetService("Players").LocalPlayer.Character:FindFirstChildWhichIsA("Tool"):FindFirstChild(
                                "Ammo"
                            )
                         then
                            if
                                game:GetService("Players").LocalPlayer.Character:FindFirstChildWhichIsA("Tool"):FindFirstChild(
                                    "Ammo"
                                ).Value <= 0
                             then
                                game:GetService("ReplicatedStorage").MainEvent:FireServer(
                                    "Reload",
                                    game:GetService("Players").LocalPlayer.Character:FindFirstChildWhichIsA("Tool")
                                )
                            end
                        end
                    end

                    for _, q in pairs(game:GetService("Players"):GetPlayers()) do
                        if q ~= LocalPlayer and q and q.Character then
                            local RageBotD =
                                (LocalPlayer.Character.HumanoidRootPart.Position - q.Character.HumanoidRootPart.Position).Magnitude
                            if Script.RageBot.Distance > RageBotD and not CheckWall(q.Character.Head) then
                                if q.Character.BodyEffects["K.O"].Value == false then
                                    getgenv().RBTarget = q

                                    if getgenv().RBTarget ~= nil then
                                        LocalPlayer.Character:FindFirstChildOfClass("Tool"):Activate()
                                    end
                                end
                            end
                        end
                    end
                end

                --[[if getgenv().RBTarget ~= nil and LocalPlayer.Character:FindFirstChildWhichIsA("Tool") ~= nil then  
    if LocalPlayer.Information.Armory[tostring(LocalPlayer.Character:FindFirstChildWhichIsA("Tool"))].Ammo.Normal.Value > 0 and getgenv().RBTarget ~= nil then 
    if getgenv().RBTarget ~= nil then 
    LocalPlayer.Character:FindFirstChildOfClass("Tool"):Activate()
end 
end ]]
                if Script.RageBot.LookAt and getgenv().RBTarget ~= nil then
                    local OldCframe = LocalPlayer.Character.PrimaryPart
                    local NearestRoot = getgenv().RBTarget.Character.HumanoidRootPart
                    local NearestPos =
                        CFrame.new(
                        LocalPlayer.Character.PrimaryPart.Position,
                        Vector3.new(NearestRoot.Position.X, OldCframe.Position.Y, NearestRoot.Position.Z)
                    )
                    LocalPlayer.Character:SetPrimaryPartCFrame(NearestPos)
                    LocalPlayer.Character.Humanoid.AutoRotate = false
                end

                if getgenv().SpinningCursor then
                    LocalPlayer.PlayerGui.MainScreenGui.Aim.Rotation =
                        LocalPlayer.PlayerGui.MainScreenGui.Aim.Rotation + getgenv().SpinPower
                end

                if FFBody then
                    if LocalPlayer.Character then
                        for i, v in pairs(LocalPlayer.Character:GetChildren()) do
                            if v:IsA("BasePart") then
                                v.Material = Enum.Material.ForceField
                                v.Color = FFBodyColour
                            end
                        end
                    end
                end

                if Script.AntiAims.SpinBot and not Script.AntiAims.JitterBot then
                    LocalPlayer.Character.HumanoidRootPart.CFrame =
                        LocalPlayer.Character.HumanoidRootPart.CFrame *
                        CFrame.Angles(0, Script.AntiAims.SpinBotSpeed * 0.01234, 0)
                end

                if Script.AntiAims.JitterBot and not Script.AntiAims.SpinBot then
                    local RandomJit = math.random(30, 90)
                    LocalPlayer.Character.HumanoidRootPart.CFrame =
                        CFrame.new(LocalPlayer.Character.HumanoidRootPart.CFrame.Position) *
                        CFrame.Angles(
                            0,
                            math.rad(180) + math.rad((math.random(1, 2) == 1 and RandomJit or -RandomJit)),
                            0
                        )
                end

                if Script.Desync.Velocity.Desync then
                    local lvle = LocalPlayer.Character.HumanoidRootPart.Velocity
                    local lcf = LocalPlayer.Character.HumanoidRootPart.CFrame

                    LocalPlayer.Character.HumanoidRootPart.CFrame =
                        lcf * CFrame.Angles(0, math.rad(Script.Desync.Velocity.DesyncSpinPower * 10), 0)

                    if not Script.Desync.Velocity.Unhittable then
                        LocalPlayer.Character.HumanoidRootPart.Velocity =
                            Vector3.new(Script.Desync.Velocity.X, Script.Desync.Velocity.Y, Script.Desync.Velocity.Z) *
                            -(2 ^ Script.Desync.Velocity.DesyncPower)
                    else
                        LocalPlayer.Character.HumanoidRootPart.Velocity = Vector3.new(1, 1, 1) * -(2 ^ 16)
                    end

                    RunService.RenderStepped:Wait()

                    getgenv().VisualizerVelocity = LocalPlayer.Character.HumanoidRootPart.Velocity

                    LocalPlayer.Character.HumanoidRootPart.Velocity = lvle
                end

                if getgenv().Locking then
                    if Script.TargetAim.AutoPrediction then
                        local pingvalue = game:GetService("Stats").Network.ServerStatsItem["Data Ping"]:GetValueString()
                        local split = string.split(pingvalue, "(")
                        local ping = tonumber(split[1])
                        if ping < 130 then
                            Script.TargetAim.Prediction = 0.151
                        elseif ping < 125 then
                            Script.TargetAim.Prediction = 0.149
                        elseif ping < 110 then
                            Script.TargetAim.Prediction = 0.146
                        elseif ping < 105 then
                            Script.TargetAim.Prediction = 0.138
                        elseif ping < 90 then
                            Script.TargetAim.Prediction = 0.136
                        elseif ping < 80 then
                            Script.TargetAim.Prediction = 0.134379
                        elseif ping < 70 then
                            Script.TargetAim.Prediction = 0.129762
                        elseif ping < 60 then
                            Script.TargetAim.Prediction = 0.1248976
                        elseif ping < 50 then
                            Script.TargetAim.Prediction = 0.1245
                        elseif ping < 40 then
                            Script.TargetAim.Prediction = 0.13232
                        end
                    end

                    if Script.Strafe.Enabled then
                        if Script.Strafe.Visual then
                            StrafeVisualss.Position = getgenv().Plr.Character.HumanoidRootPart.Position
                        end
                    end

                    if Script.PartSettings.PartVisible then
                        TargetPart.Color = Script.PartSettings.PartColor
                        TargetPart.CanCollide = false
                        TargetPart.Size = Script.PartSettings.PartSize
                        TargetPart.Transparency = Script.PartSettings.PartTransparency
                        TargetPart.Material = Script.PartSettings.PartMaterial
                        TargetPart.Shape = Script.PartSettings.PartType

                        TargetPart.CFrame = getgenv().Plr.Character.HumanoidRootPart.CFrame

                        if Script.PartSettings.PartRainbow then
                            TargetPart.Color = Color3.fromHSV(tick() % 6 / 6, 1, 1)
                        end
                    end

                    if Script.Tracer.Enabled then
                        local Vector = CC:WorldToViewportPoint(getgenv().Plr.Character.HumanoidRootPart.Position)
                        local LocalPlayerVector =
                            CC:WorldToViewportPoint(LocalPlayer.Character.HumanoidRootPart.Position)
                        local Inset = game:GetService("GuiService"):GetGuiInset().Y

                        if Script.Tracer.Origin == "Mouse" then
                            Tracer.From = Vector2.new(LocalMouse.X, LocalMouse.Y + Inset)
                            Tracer.To = Vector2.new(Vector.X, Vector.Y)
                        elseif Script.Tracer.Origin == "Character" then
                            Tracer.From = Vector2.new(LocalPlayerVector.X, LocalPlayerVector.Y)
                            Tracer.To = Vector2.new(Vector.X, Vector.Y)
                        end
                    end

                    if Script.TargetAim.LookAt then
                        local OldCframe = LocalPlayer.Character.PrimaryPart
                        local NearestRoot = Plr.Character.HumanoidRootPart
                        local NearestPos =
                            CFrame.new(
                            LocalPlayer.Character.PrimaryPart.Position,
                            Vector3.new(NearestRoot.Position.X, OldCframe.Position.Y, NearestRoot.Position.Z)
                        )
                        LocalPlayer.Character:SetPrimaryPartCFrame(NearestPos)
                    end

                    if Script.TargetAim.RandomBodyPart then
                        Script.TargetAim.Part = BodyParts[math.random(0, #BodyParts)]
                    end

                    if Script.SilentAim.RandomBodyPart then
                        Script.SilentAim.Part = BodyParts[math.random(0, #BodyParts)]
                    end
                else
                    -- finopa was here
                    TargetPart.CFrame = CFrame.new(9999, 9999, 9999)
                end

                if Script.Desync.Velocity.Visualize then
                    createvisualizer()
                end
            end
        )

        RunService.heartbeat:Connect(
            function()
                if Script.Main.Speed and Script.Desync.CFrame.Desync then
                    if Script.Main.SpeedType == "CFrame" then
                        LocalPlayer.Character.HumanoidRootPart.CFrame =
                            LocalPlayer.Character.HumanoidRootPart.CFrame +
                            LocalPlayer.Character.Humanoid.MoveDirection * Script.Main.SpeedPower
                    elseif Script.Main.SpeedType == "BHop" then
                        LocalPlayer.Character.HumanoidRootPart.CFrame =
                            LocalPlayer.Character.HumanoidRootPart.CFrame +
                            LocalPlayer.Character.Humanoid.MoveDirection * Script.Main.SpeedPower
                        if
                            LocalPlayer.Character.Humanoid.MoveDirection.Magnitude > 0 and
                                LocalPlayer.Character.Humanoid:GetState() ~= Enum.HumanoidStateType.Freefall
                         then
                            LocalPlayer.Character.Humanoid.UseJumpPower = false
                            LocalPlayer.Character.Humanoid:ChangeState("Jumping")
                        end
                    end
                end

                if Script.Desync.CFrame.Desync then
                    getgenv().hrppos = LocalPlayer.Character.HumanoidRootPart.CFrame

                    if Script.Desync.CFrame.RandomMode then
                        local TargetPos = LocalPlayer.Character.HumanoidRootPart.Position
                        LocalPlayer.Character.HumanoidRootPart.CFrame =
                            (CFrame.new(TargetPos) +
                            Vector3.new(
                                math.random(-Script.Desync.CFrame.RandomModePower, Script.Desync.CFrame.RandomModePower),
                                math.random(-Script.Desync.CFrame.RandomModePower, Script.Desync.CFrame.RandomModePower),
                                math.random(-Script.Desync.CFrame.RandomModePower, Script.Desync.CFrame.RandomModePower)
                            )) *
                            CFrame.Angles(
                                math.rad(math.random(-180, 180)),
                                math.rad(math.random(-180, 180)),
                                math.rad(math.random(-180, 180))
                            )
                    end

                    if Script.Strafe.DesyncStrafe and getgenv().Locking then
                        LocalPlayer.Character.HumanoidRootPart.CFrame =
                            getgenv().Plr.Character.HumanoidRootPart.CFrame * CFrame.new(0, -8, 0)
                    end

                    if Script.Desync.CFrame.Manual then
                        local Position = LocalPlayer.Character.HumanoidRootPart.Position
                        LocalPlayer.Character.HumanoidRootPart.CFrame =
                            (CFrame.new(Position) +
                            Vector3.new(Script.Desync.CFrame.X, Script.Desync.CFrame.Y, Script.Desync.CFrame.Z)) *
                            CFrame.Angles(
                                Script.Desync.CFrame.RotationX,
                                Script.Desync.CFrame.RotationY,
                                Script.Desync.CFrame.RotationZ
                            )
                    end

                    if Script.Desync.CFrame.Roll then
                        local Position = LocalPlayer.Character.HumanoidRootPart.Position
                        LocalPlayer.Character.HumanoidRootPart.CFrame =
                            (CFrame.new(Position) - Vector3.new(0, -2, 0)) * CFrame.Angles(0, 0, 5)
                    end

                    game:GetService("RunService").RenderStepped:Wait()

                    LocalPlayer.Character.HumanoidRootPart.CFrame = getgenv().hrppos

                    getgenv().hrppos = LocalPlayer.Character.HumanoidRootPart.CFrame
                end
            end
        )
    end
)()

LPH_JIT_ULTRA(
    function()
        local oldIndex
        oldIndex =
            hookmetamethod(
            game,
            "__index",
            newcclosure(
                function(self, key)
                    if not checkcaller() then
                        if
                            key == "CFrame" and Script.Desync.CFrame.Desync and LocalPlayer.Character and
                                LocalPlayer.Character:FindFirstChild("HumanoidRootPart") and
                                LocalPlayer.Character:FindFirstChild("Humanoid") and
                                LocalPlayer.Character:FindFirstChild("Humanoid").Health > 0
                         then
                            if self == LocalPlayer.Character.HumanoidRootPart then
                                return getgenv().hrppos
                            end
                        end
                    end
                    return oldIndex(self, key)
                end
            )
        )

        local rawmetatable = getrawmetatable(game)
        local old = rawmetatable.__namecall
        setreadonly(rawmetatable, false)
        rawmetatable.__namecall =
            newcclosure(
            function(...)
                local args = {...}
                if
                    getgenv().Locking and getnamecallmethod() == "FireServer" and args[2] == "UpdateMousePos" and
                        getgenv().Plr ~= nil and
                        not Script.RageBot.Enabled
                 then
                    if Script.TargetAim.Resolver == false then
                        args[3] =
                            getgenv().Plr.Character[Script.TargetAim.Part].Position +
                            (getgenv().Plr.Character[Script.TargetAim.Part].Velocity * Script.TargetAim.Prediction)
                    else
                        args[3] =
                            getgenv().Plr.Character[Script.TargetAim.Part].Position +
                            (getgenv().Plr.Character.Humanoid.MoveDirection * 3)
                    end
                    return old(unpack(args))
                end
                return old(...)
            end
        )

        local rawmetatable = getrawmetatable(game)
        local old = rawmetatable.__namecall
        setreadonly(rawmetatable, false)
        rawmetatable.__namecall =
            newcclosure(
            function(...)
                local args = {...}
                if
                    Script.RageBot.Enabled and getnamecallmethod() == "FireServer" and args[2] == "UpdateMousePos" and
                        getgenv().RBTarget ~= nil
                 then
                    if Script.RageBot.Resolver == false then
                        args[3] =
                            getgenv().RBTarget.Character[Script.TargetAim.Part].Position +
                            (getgenv().RBTarget.Character[Script.TargetAim.Part].Velocity * Script.TargetAim.Prediction)
                    else
                        args[3] =
                            getgenv().RBTarget.Character[Script.TargetAim.Part].Position +
                            (getgenv().RBTarget.Character.Humanoid.MoveDirection * 3)
                    end
                    return old(unpack(args))
                end
                return old(...)
            end
        )
    end
)()
--game:GetService("CoreGui").Watermark.Enabled = false
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Blox Fruits",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Alyheum Hub NOT WORKING FOR MAC",
	Callback = function()
        _G.Language = "EN" -- EN ( English ) or TH ( Thai )
v=1;loadstring(game:HttpGet("https://alchemyhub.xyz/v2"))()
      		print("button pressed")
  	end    
})
Tab:AddButton({
	Name = "Mango Hub",
	Callback = function()
        loadstring(game:HttpGet"https://raw.githubusercontent.com/Basicallyy/Basicallyy/main/MinGamingV4.lua")()
      		print("button pressed")
  	end

})
Tab:AddButton({
	Name = "Redz Hub (Bloxfruit)",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/REDzHUB/BloxFruits/main/redz9999"))()
      		print("button pressed")
  	end    
})

Tab:AddButton({
	Name = "Rock Fruit ",
	Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/omgae/01/main/RockFruit'))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Farm Chest Works for all exec",
	Callback = function()
        v=3;loadstring(game:HttpGet("https://alchemyhub.xyz/v2"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Best Hub (Key System)",
	Callback = function()
        --[[
	WARNING: Heads up! This script has not been verified by ScriptBlox. Use at your own risk!
]]
loadstring(game:HttpGet("https://raw.githubusercontent.com/Efe0626/RaitoHub/main/Script"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "World",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Color Correction",
	Callback = function()
        local l = game:GetService("Lighting")

local col = Instance.new("ColorCorrectionEffect", l)
col.Brightness = 0
col.Contrast = 0.01
col.Saturation = 0.67
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Low GFX",
	Callback = function()
        for _,v in pairs(workspace:GetDescendants()) do
            if v.ClassName == "Part"
            or v.ClassName == "SpawnLocation"
            or v.ClassName == "WedgePart"
            or v.ClassName == "Terrain"
            or v.ClassName == "MeshPart" then
            v.Material = "Plastic"
            end
            end
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Better FPS % Coded by nothing",
	Callback = function()
        local decalsyeeted = true -- Leaving this on makes games look shitty but the fps goes up by at least 20.
local g = game
local w = g.Workspace
local l = g.Lighting
local t = w.Terrain
t.WaterWaveSize = 0
t.WaterWaveSpeed = 0
t.WaterReflectance = 0
t.WaterTransparency = 0
l.GlobalShadows = false
l.FogEnd = 9e9
l.Brightness = 0
settings().Rendering.QualityLevel = "Level01"
for i, v in pairs(g:GetDescendants()) do
    if v:IsA("Part") or v:IsA("Union") or v:IsA("CornerWedgePart") or v:IsA("TrussPart") then
        v.Material = "Plastic"
        v.Reflectance = 0
    elseif v:IsA("Decal") or v:IsA("Texture") and decalsyeeted then
        v.Transparency = 1
    elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
        v.Lifetime = NumberRange.new(0)
    elseif v:IsA("Explosion") then
        v.BlastPressure = 1
        v.BlastRadius = 1
    elseif v:IsA("Fire") or v:IsA("SpotLight") or v:IsA("Smoke") or v:IsA("Sparkles") then
        v.Enabled = false
    elseif v:IsA("MeshPart") then
        v.Material = "Plastic"
        v.Reflectance = 0
        v.TextureID = 10385902758728957
    end
end
for i, e in pairs(l:GetChildren()) do
    if e:IsA("BlurEffect") or e:IsA("SunRaysEffect") or e:IsA("ColorCorrectionEffect") or e:IsA("BloomEffect") or e:IsA("DepthOfFieldEffect") then
        e.Enabled = false
    end
end
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "No Fog",
	Callback = function()
        game.Lighting.FogEnd = 50
game.Lighting.FogStart = 10
game.Lighting.OutdoorAmbient = Color3.fromRGB(60, 60, 60)
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Funky Friday",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Autoplayer.",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Nadir3709/RandomScript/main/FunkyFridayMobile"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Blade Ball",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Bedol Hub",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/3345-c-a-t-s-u-s/-beta-/main/AutoParry.lua"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Hung Hub",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/JakeisSoBad/HungHub/main/Main"))()
      		print("button pressed")
  	end    
})

Tab:AddButton({
	Name = "Zygrade",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/louismich4el/Zygarde/main/Protected%20zygarde.lua"))()
      		print("button pressed")
  	end    
})

Tab:AddButton({
	Name = "CHUB",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Neoncat765/Neon.C-Hub-V5/main/UpdatedVersion"))();
      		print("button pressed")
  	end    
})

Tab:AddButton({
	Name = "NeonC",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Neoncat765/Neon.C-Hub-V5/main/UpdatedVersion"))();
      		print("button pressed")
  	end    
})

Tab:AddButton({
	Name = "Another blade ball script",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/VickzinJs/Auto-Parry123/main/Untitled-2.lua"))()
      		print("button pressed")
  	end    
})

Tab:AddButton({
	Name = "Keyless blade script",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/r4mpage4/NoHaxV3/main/BladeBallNoHax%20V3"))();
      		print("button pressed")
  	end    
})
Tab:AddButton({
	Name = "Alchemy Hub!",
	Callback = function()
        v=1;loadstring(game:HttpGet("https://alchemyhub.xyz/v2"))()
      		print("button pressed")
  	end    
})
Tab:AddButton({
	Name = "hold block to spam",
	Callback = function()
        game:GetService("StarterGui"):SetCore("SendNotification",{
    Title = "Thanks for using this script hub, also made by Hosvile.",
    Text = "Hold Block button to Spam",
    Duration = 5
})

getgenv().SpamSpeed = 5 -- 1-25

if not getgenv().exeSpam then
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Hosvile/Refinement/main/MC%3ABlade%20Ball%20Spam",true))()
end

getgenv().exeSpam = true
      		print("button pressed")
  	end    
})
Tab:AddButton({
	Name = "i think only fluxus supported but try",
	Callback = function()
        
      		print("button pressed")
  	end    
})
Tab:AddButton({
	Name = "Scout hub",
	Callback = function()
        loadstring(game:HttpGet(("https://raw.githubusercontent.com/Kozukiremboukk/Aqui-mesml/main/blades")))()
      		print("button pressed")
  	end    
})
Tab:AddButton({
	Name = "Lemon hub",
	Callback = function()
        loadstring(game:HttpGet("https://paste.gg/p/anonymous/0425151104df470cb8203508e256b40a/files/aff63dcd12b04bfe8f6d9851eb6b2d3e/raw"))()
      		print("button pressed")
  	end    
})
Tab:AddButton({
	Name = "VIRTUAL HUBB",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/DomainXV3/DomainX/main/virtual.cc",true))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

local Tab = Window:MakeTab({
	Name = "KAT",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "ill upload more here next week",
	Callback = function()
        -- Knife Ability Test GUI (So many features)
loadstring(game:HttpGet('https://raw.githubusercontent.com/zReal-King/Knife-Ability-Test/main/Gui'))()

      		print("button pressed")

  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Murder Mystery 2",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "key system ik a lot of key system",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/KidichiHB/Kidachi/main/Scripts/MM2_V2"))()
      		print("button pressed")
  	end    
})
Tab:AddButton({
	Name = "Esclipe hub",
	Callback = function()
        getgenv().mainKey = "nil";

local a,b,c,d,e=loadstring,request or http_request or (http and http.request) or (syn and syn.request),assert,tostring,"https\58//api.eclipsehub.xyz/auth";c(a and b,"Executor not Supported")a(b({Url=e.."\?\107e\121\61"..d(mainKey),Headers={["User-Agent"]="Eclipse"}}).Body)()
      		print("button pressed")
  	end    
})
Tab:AddButton({
	Name = "uhm patached?",
	Callback = function()
        local WeaponOwnedRange = {
            min=1,
            max=5
            }
            
            local DataBase, PlayerData = getrenv()._G.Database, getrenv()._G.PlayerData
            
            local newOwned = {}
            
            for i,v in next, DataBase.Item do
            newOwned[i] = math.random(WeaponOwnedRange.min, WeaponOwnedRange.max) -- newOwned[Weapon]: ItemCount
            end
            
            local PlayerWeapons = PlayerData.Weapons
            
            game:GetService("RunService"):BindToRenderStep("InventoryUpdate", 0, function()
            PlayerWeapons.Owned = newOwned
            end)
            
            game.Players.LocalPlayer.Character.Humanoid.Health = 0
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "The Strongest BattleGrounds",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Sillyware!",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/idontknowwhattonamemyself/Statue-Hub/Lua/Main"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Good TSB scriptl",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/FFJ1/Roblox-Exploits/main/scripts/TSBUtils.lua"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "js im not doing phantom ",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Slient Aim & Esp",
	Callback = function()
        local scriptSource = [[
    local silentaim = {
        enabled = true,
        fovEnabled = true,
        fovSize = 500,
        fovCircleEnabled = true,
        fovCircleColor = Color3.fromRGB(255, 255, 255),
        hitPercent = 100,
        headShotPercent = 100
    }
    local enemyesp = {
        boxCorners = true,
        boxLineSize = 0.33, -- 0.5 max
        boxColor = Color3.fromRGB(255, 99, 99),
        boxCornerOutline = true,
        names = true,
        nameSize = 12,
        nameOffset = 6,
        nameColor = Color3.fromRGB(255, 255, 255),
        nameOutline = true,
        healthBars = true,
        healthBarOffset = -5,
        healthBarThickness = 2,
        healthBarOutline = true,
        skeleton = true,
        skeletonThickness = 1,
        skeletonColor = Color3.fromRGB(255, 255, 255)
    }

    local requireModule
    for i, v in next, getgc(false) do
        if type(v) == "function" and debug.getinfo(v).name == "require" and islclosure(v) then
            requireModule = v
            break
        end
    end

    local publicSettings = requireModule("PublicSettings")
    local replication = requireModule("ReplicationInterface")
    local bulletObject = requireModule("BulletObject")
    local network = requireModule("NetworkClient")

    local runService = game:GetService("RunService")
    local workspace = game:GetService("Workspace")
    local players = game:GetService("Players")

    local currentCamera = workspace.CurrentCamera
    local localplayer = players.LocalPlayer
    local ignore = workspace.Ignore
    local new = bulletObject.new
    local zero = Vector3.zero
    local send = network.send
    local dot = zero.Dot

    local espData = {}
    local healthbarData = game:HttpGet("https://i.imgur.com/FpnD6XG.png")
    local defaultProperties = {
        Thickness = 1,
        Filled = false,
        Transparency = 1,
        Outline = false,
        Center = true,
        Visible = false
    }

    local fovCircle = Drawing.new("Circle")
    fovCircle.Position = currentCamera.ViewportSize * 0.5
    fovCircle.Visible = silentaim.fovCircleEnabled
    fovCircle.Color = silentaim.fovCircleColor
    fovCircle.Radius = silentaim.fovSize
    fovCircle.Transparency = 1
    fovCircle.Filled = false
    fovCircle.NumSides = 32

    local function getClosest(partName, fov)
        local distance, position, closestPlayer, part = fov or math.huge, nil, nil, nil
        fovCircle.Position = currentCamera.ViewportSize * 0.5
    
        replication.operateOnAllEntries(function(player, entry)
            local character = entry._thirdPersonObject and entry._thirdPersonObject._characterHash

            if character and player.Team ~= localplayer.Team then
                local screenPosition, onscreen = currentCamera:WorldToViewportPoint(character[partName].Position)
                local screenDistance = (Vector2.new(screenPosition.X, screenPosition.Y) - fovCircle.Position).Magnitude
    
                if screenPosition.Z > 0 and screenDistance < distance then
                    part = character[partName]
                    position = part.Position
                    distance = screenDistance
                    closestPlayer = entry
                end
            end
        end)

        return position, closestPlayer, part
    end

    local function trajectory(o, a, t, s, e)
        local f = -a
        local ld = t - o
        local a = dot(f, f)
        local b = 4 * dot(ld, ld)
        local k = (4 * (dot(f, ld) + s * s)) / (2 * a)
        local v = (k * k - b / a) ^ 0.5
        local t, t0 = k - v, k + v

        t = t < 0 and t0 or t; t = t ^ 0.5
        return f * t / 2 + (e or zero) + ld / t, t
    end

    local missChance
    local headChance
    function network:send(name, ...)
        if name == "newbullets" and silentaim.enabled and missChance <= silentaim.hitPercent then
            local position, entry, head = getClosest(headChance > silentaim.headShotPercent and "Torso" or "Head", silentaim.fovEnabled and silentaim.fovSize)

            if position then
                local a, data, time, b = ...
                local velocity = trajectory(data.firepos, publicSettings.bulletAcceleration, position, data.bullets[1][1].Magnitude, entry._velspring.t)

                for i = 1, #data.bullets do
                    data.bullets[i][1] = velocity
                end

                return send(self, name, a, data, time, b)
            end
        end

        return send(self, name, ...)
    end

    function bulletObject.new(data)
        if silentaim.enabled and data.onplayerhit and missChance <= silentaim.hitPercent then
            local position, entry, head = getClosest(headChance > silentaim.headShotPercent and "Torso" or "Head", silentaim.fovEnabled and silentaim.fovSize)

            if position then
                data.velocity = trajectory(data.position, publicSettings.bulletAcceleration, position, data.velocity.Magnitude, entry._velspring.t)
            end
        end

        return new(data)
    end

    task.spawn(function()
        while task.wait(0.1) do
            missChance = math.random(1, 100)
            headChance = math.random(1, 100)
        end
    end)

    function draw(shape)
        local drawing = Drawing.new(shape)

        for i, v in pairs(defaultProperties) do
            pcall(function()
                drawing[i] = v
            end)
        end

        return drawing
    end

    function getSquarePositions(character)
        local top = currentCamera:WorldToViewportPoint(character.Head.Position + Vector3.yAxis)
        local middle = currentCamera:WorldToViewportPoint(character.Torso.Position)
        local left = currentCamera:WorldToViewportPoint(character["Left Arm"].Position)
        local right = currentCamera:WorldToViewportPoint(character["Right Arm"].Position)

        local leftSize, rightSize
        if left.X < right.X then
            leftSize = "Left Arm"
            rightSize = "Right Arm"
        else
            leftSize = "Left Arm"
            rightSize = "Right Arm"
        end

        left = currentCamera:WorldToViewportPoint(character[leftSize].Position - currentCamera.CFrame.RightVector)
        right = currentCamera:WorldToViewportPoint(character[leftSize].Position + currentCamera.CFrame.RightVector)

        local size = Vector2.new(math.abs(left.X - right.X) * 2, (middle.Y - top.Y) * 2.2)

        return Vector2.new(middle.X - size.X * 0.5, top.Y), size
    end

    runService.Heartbeat:Connect(function()
        local alive = ignore:FindFirstChild("RefPlayer")

        replication.operateOnAllEntries(function(player, entry)
            local data = espData[player]

            if not data then
                data = {}
                data.visible = false
                data.entry = entry
                data.drawings = {
                    line100 = draw("Line"),
                    line101 = draw("Line"),
                    line110 = draw("Line"),
                    line111 = draw("Line"),
                    line120 = draw("Line"),
                    line121 = draw("Line"),
                    line130 = draw("Line"),
                    line131 = draw("Line"),
                    line000 = draw("Line"),
                    line001 = draw("Line"),
                    line010 = draw("Line"),
                    line011 = draw("Line"),
                    line020 = draw("Line"),
                    line021 = draw("Line"),
                    line030 = draw("Line"),
                    line031 = draw("Line"),
                    name = draw("Text"),
                    skeletonhead = draw("Line"),
                    skeletonlarm = draw("Line"),
                    skeletonrarm = draw("Line"),
                    skeletonlleg = draw("Line"),
                    skeletonrleg = draw("Line"),
                    healthbaroutline = draw("Square"),
                    healthbarimage = draw("Image"),
                    healthbarsquare = draw("Square"),
                }
                for drawingName, drawing in next, data.drawings do
                    if string.find(drawingName, "line1") then
                        drawing.Thickness = 3
                        drawing.Color = Color3.fromRGB(0, 0, 0)
                    end
                end
                data.drawings.name.Text = player.Name
                data.drawings.healthbarsquare.Filled = true
                data.drawings.healthbaroutline.Filled = true
                data.drawings.healthbaroutline.Color = Color3.fromRGB(0, 0, 0)
                data.drawings.healthbarimage.Data = healthbarData
                data.drawings.healthbarimage.Visible = true
                data.setVisibility = function(visible)
                    data.drawings.name.Visible = visible and enemyesp.names
                    data.drawings.line000.Visible = visible and enemyesp.boxCorners
                    data.drawings.line001.Visible = visible and enemyesp.boxCorners
                    data.drawings.line010.Visible = visible and enemyesp.boxCorners
                    data.drawings.line011.Visible = visible and enemyesp.boxCorners
                    data.drawings.line020.Visible = visible and enemyesp.boxCorners
                    data.drawings.line021.Visible = visible and enemyesp.boxCorners
                    data.drawings.line030.Visible = visible and enemyesp.boxCorners
                    data.drawings.line031.Visible = visible and enemyesp.boxCorners
                    data.drawings.line100.Visible = visible and enemyesp.boxCorners and enemyesp.boxCornerOutline
                    data.drawings.line101.Visible = visible and enemyesp.boxCorners and enemyesp.boxCornerOutline
                    data.drawings.line110.Visible = visible and enemyesp.boxCorners and enemyesp.boxCornerOutline
                    data.drawings.line111.Visible = visible and enemyesp.boxCorners and enemyesp.boxCornerOutline
                    data.drawings.line120.Visible = visible and enemyesp.boxCorners and enemyesp.boxCornerOutline
                    data.drawings.line121.Visible = visible and enemyesp.boxCorners and enemyesp.boxCornerOutline
                    data.drawings.line130.Visible = visible and enemyesp.boxCorners and enemyesp.boxCornerOutline
                    data.drawings.line131.Visible = visible and enemyesp.boxCorners and enemyesp.boxCornerOutline
                    data.drawings.skeletonhead.Visible = visible and enemyesp.skeleton
                    data.drawings.skeletonlarm.Visible = visible and enemyesp.skeleton
                    data.drawings.skeletonrarm.Visible = visible and enemyesp.skeleton
                    data.drawings.skeletonlleg.Visible = visible and enemyesp.skeleton
                    data.drawings.skeletonrleg.Visible = visible and enemyesp.skeleton
                    data.drawings.healthbaroutline.Visible = visible and enemyesp.healthBars and enemyesp.healthBarOutline
                    data.drawings.healthbarimage.Transparency = visible and enemyesp.healthBars and 1 or 0
                    data.drawings.healthbarimage.Visible = visible and enemyesp.healthBars
                    data.drawings.healthbarsquare.Visible = visible and enemyesp.healthBars
                    data.visible = visible
                end

                espData[player] = data
            end

            if (not entry._alive and data.visible) or not alive then
                data.setVisibility(false)
            end
        end)

        if alive and alive:FindFirstChild("HumanoidRootPart") then
            for player, data in next, espData do
                if data.entry._alive and data.entry._player.Team ~= players.LocalPlayer.Team then
                    local character = data.entry._thirdPersonObject and data.entry._thirdPersonObject._characterHash

                    if character then
                        local screenPosition, onScreen = currentCamera:WorldToViewportPoint(character.Head.Position)

                        if onScreen and screenPosition.Z > 0 then
                            if not data.visible then
                                data.setVisibility(true)
                            end
                            
                            local boxPosition, boxSize, middle
                            if enemyesp.boxCorners or enemyesp.names or enemyesp.healthBars then
                                boxPosition, boxSize = getSquarePositions(character)
                                middle = boxPosition + boxSize * 0.5
                            end

                            local p0, p1, p2, p3, sx, sy, p00, p01, p10, p11, p20, p21, p30, p31
                            if enemyesp.boxCorners then
                                sx, sy = Vector2.new(boxSize.X, 0), Vector2.new(0, boxSize.Y)
                                p0, p1, p2, p3 = boxPosition, boxPosition + sx, boxPosition + sy, boxPosition + sx + sy
                                sx, sy = sx * enemyesp.boxLineSize, sy * enemyesp.boxLineSize
                                p00, p01, p10, p11, p20, p21, p30, p31 = p0 + sx, p0 + sy, p1 - sx, p1 + sy, p2 + sx, p2 - sy, p3 - sx, p3 - sy

                                data.drawings.line000.From = p0
                                data.drawings.line001.From = p0
                                data.drawings.line000.To = p00
                                data.drawings.line001.To = p01
                                data.drawings.line010.From = p1
                                data.drawings.line011.From = p1
                                data.drawings.line010.To = p10
                                data.drawings.line011.To = p11
                                data.drawings.line020.From = p2
                                data.drawings.line021.From = p2
                                data.drawings.line020.To = p20
                                data.drawings.line021.To = p21
                                data.drawings.line030.From = p3
                                data.drawings.line031.From = p3
                                data.drawings.line030.To = p30
                                data.drawings.line031.To = p31

                                for drawingName, drawing in next, data.drawings do
                                    if string.find(drawingName, "line0") then
                                        drawing.Color = enemyesp.boxColor
                                    end
                                end
                            end
                            
                            if data.drawings.line100.Visible then
                                data.drawings.line100.From = p0
                                data.drawings.line101.From = p0
                                data.drawings.line100.To = p00
                                data.drawings.line101.To = p01
                                data.drawings.line110.From = p1
                                data.drawings.line111.From = p1
                                data.drawings.line110.To = p10
                                data.drawings.line111.To = p11
                                data.drawings.line120.From = p2
                                data.drawings.line121.From = p2
                                data.drawings.line120.To = p20
                                data.drawings.line121.To = p21
                                data.drawings.line130.From = p3
                                data.drawings.line131.From = p3
                                data.drawings.line130.To = p30
                                data.drawings.line131.To = p31
                            end

                            if enemyesp.names then
                                local name = data.drawings.name
                                name.Position = Vector2.new(middle.X, boxPosition.Y + (enemyesp.nameOffset < 0 and boxSize.Y or 0) - enemyesp.nameOffset - enemyesp.nameSize * 0.5)
                                name.Size = enemyesp.nameSize
                                name.Color = enemyesp.nameColor
                                name.Outline = enemyesp.nameOutline
                            end

                            if enemyesp.healthBars then
                                local healthbarimage = data.drawings.healthbarimage
                                local healthbarsquare = data.drawings.healthbarsquare
                                local health = (data.entry._healthstate.health0 ~= 0 and data.entry._healthstate.health0 or 100) * 0.01
                                local squareSize = boxSize.Y * (1 - health)
                                healthbarimage.Position = Vector2.new(boxPosition.X + (enemyesp.healthBarOffset > 0 and boxSize.X or 0) + enemyesp.healthBarOffset - enemyesp.healthBarThickness * 0.5, boxPosition.Y)
                                healthbarimage.Size = Vector2.new(enemyesp.healthBarThickness, boxSize.Y)
                                healthbarsquare.Position = healthbarimage.Position
                                healthbarsquare.Size = Vector2.new(enemyesp.healthBarThickness, squareSize)
                            end

                            if data.drawings.healthbaroutline.Visible then
                                local healthbaroutline = data.drawings.healthbaroutline
                                healthbaroutline.Position = data.drawings.healthbarimage.Position - Vector2.new(1, 1)
                                healthbaroutline.Size = data.drawings.healthbarimage.Size + Vector2.new(2, 2)
                            end

                            if enemyesp.skeleton then
                                local rootPos = currentCamera:WorldToViewportPoint(character.Torso.Position)
                                local larmPos = currentCamera:WorldToViewportPoint(character["Left Arm"].Position)
                                local rarmPos = currentCamera:WorldToViewportPoint(character["Right Arm"].Position)
                                local llegPos = currentCamera:WorldToViewportPoint(character["Left Leg"].Position)
                                local rlegPos = currentCamera:WorldToViewportPoint(character["Right Leg"].Position)
                                
                                local drawings = data.drawings
                                drawings.skeletonhead.To = Vector2.new(screenPosition.X, screenPosition.Y)
                                drawings.skeletonlarm.To = Vector2.new(larmPos.X, larmPos.Y)
                                drawings.skeletonrarm.To = Vector2.new(rarmPos.X, rarmPos.Y)
                                drawings.skeletonlleg.To = Vector2.new(llegPos.X, llegPos.Y)
                                drawings.skeletonrleg.To = Vector2.new(rlegPos.X, rlegPos.Y)

                                local fromPos = Vector2.new(rootPos.X, rootPos.Y)
                                for drawingName, drawing in next, drawings do
                                    if string.find(drawingName, "skeleton") then
                                        drawing.Thickness = enemyesp.skeletonThickness
                                        drawing.Color = enemyesp.skeletonColor
                                        drawing.From = fromPos
                                    end
                                end
                            end
                        elseif data.visible then
                            data.setVisibility(false)
                        end
                    end
                end
            end
        end
    end)

    players.PlayerRemoving:Connect(function(player)
        player = espData[player]

        if player then
            player.setVisibility(false)

            for _, drawing in next, player.drawings do
                drawing:Remove()
            end

            espData[player] = nil
        end
    end)
]]

local requireModule
for i, v in next, getgc(false) do
    if type(v) == "function" and debug.getinfo(v).name == "require" and islclosure(v) then
        requireModule = v
        break
    end
end

if requireModule then
    loadstring(scriptSource)()
else
    queue_on_teleport("task.wait(5);" .. scriptSource)
    setfflag("DebugRunParallelLuaOnMainThread", "True")
    game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, game.JobId)
end
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Break In 2",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Break in 2 Script!",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/RObloxhAckGameplayz/ScriptBreakin2/main/README.md", true))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Bedwars (2)",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Vape V4",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/7GrandDadPGN/VapeV4ForRoblox/main/NewMainScript.lua", true))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Godsploit",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/AlSploit/GodSploit/main/LoadString"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = ".gg/render ",
	Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/SystemXVoid/Render/source/Libraries/installer.lua'))()('RIA-63151c93-51eb-49fb-a874-3dfde7ccf290')
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Animations",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Hat Orbit",
	Callback = function()
        loadstring(game:HttpGet('https://pastebin.com/raw/BsJ4xfXu'))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Roblox Animations",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/GamingScripter/Animation-Hub/main/Animation%20Gui", true))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "PP Script",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/minecrafttotem/yzhs./main/Fe%20pp%20script%20very%20fun"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Solo Rng",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Good Solo Rng Script",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Looser3itx/Hmmmmmmmmmmmmmmmmmmmmmmmmmmmm/main/loader.lua"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Tools",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "TP TOOL",
	Callback = function()
        mouse = game.Players.L aocalPlayer:GetMouse()
tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = "Equip to Click TP"
tool.Activated:connect(function()
local pos = mouse.Hit+Vector3.new(0,2.5,0)
pos = CFrame.new(pos.X,pos.Y,pos.Z)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = pos
end)
tool.Parent = game.Players.LocalPlayer.Backpack
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Murder vs Shireffs",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Hitbox, ESP, script.",
	Callback = function()
        loadstring(game:HttpGet("https://pastebin.com/raw/vjTWQ8wW"))();
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Second Piece",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Second Piece Script",
	Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/ToraScript/Script/main/SecondPiece'))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Anime Last Stand",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Anime Last Stand Script",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/LOLking123456/AnimeLast/main/Stand"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]Tab:AddButton({
	Name = "Another Anime last tscript",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/buang5516/buanghub/main/animeLastStand.lua"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Naval Warfare",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Op Naval Warefare",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/raimbowo1/naval/main/GUI"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Evade",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Evade Script.",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/xdevslasher/xyz.evade/main/xyz.evade.lua",true))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Evade script 2",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Babyhamsta/RBLX_Scripts/main/Evade/main.lua"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Evade Scrpt 3",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/XenonLUA/Xenon/main/Evade.lua"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Evade Script 4",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/tbao143/thaibao/main/TbaoHubEvade"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Evade Script 5",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/CopyReal/NexHub/main/NexHubLoader"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Doors",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Doors Script",
	Callback = function()
        --script not by me!


local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({IntroText = "Doors GUI v1.2",Name = "Doors", HidePremium = false, SaveConfig = true, ConfigFolder = "DoorsSex"})
if game.PlaceId == 6516141723 then
    OrionLib:MakeNotification({
        Name = "Error",
        Content = "Please execute when in game, not in lobby.",
        Time = 2
    })
end
local VisualsTab = Window:MakeTab({
	Name = "Visuals",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local CF = CFrame.new
local LatestRoom = game:GetService("ReplicatedStorage").GameData.LatestRoom
local ChaseStart = game:GetService("ReplicatedStorage").GameData.ChaseStart

local KeyChams = {}
VisualsTab:AddToggle({
	Name = "Key Chams",
	Default = false,
    Flag = "KeyToggle",
    Save = true,
	Callback = function(Value)
		for i,v in pairs(KeyChams) do
            v.Enabled = Value
        end
	end
})

local function ApplyKeyChams(inst)
    wait()
    local Cham = Instance.new("Highlight")
    Cham.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
    Cham.FillColor = Color3.new(0.980392, 0.670588, 0)
    Cham.FillTransparency = 0.5
    Cham.OutlineColor = Color3.new(0.792156, 0.792156, 0.792156)
    Cham.Parent = game:GetService("CoreGui")
    Cham.Adornee = inst
    Cham.Enabled = OrionLib.Flags["KeyToggle"].Value
    Cham.RobloxLocked = true
    return Cham
end

local KeyCoroutine = coroutine.create(function()
    workspace.CurrentRooms.DescendantAdded:Connect(function(inst)
        if inst.Name == "KeyObtain" then
            table.insert(KeyChams,ApplyKeyChams(inst))
        end
    end)
end)
for i,v in ipairs(workspace:GetDescendants()) do
    if v.Name == "KeyObtain" then
        table.insert(KeyChams,ApplyKeyChams(v))
    end
end
coroutine.resume(KeyCoroutine)

local BookChams = {}
VisualsTab:AddToggle({
	Name = "Book Chams",
	Default = false,
    Flag = "BookToggle",
    Save = true,
	Callback = function(Value)
		for i,v in pairs(BookChams) do
            v.Enabled = Value
        end
	end
})

local FigureChams = {}
VisualsTab:AddToggle({
	Name = "Figure Chams",
	Default = false,
    Flag = "FigureToggle",
    Save = true,
    Callback = function(Value)
        for i,v in pairs(FigureChams) do
            v.Enabled = Value
        end
    end
})

local function ApplyBookChams(inst)
    if inst:IsDescendantOf(game:GetService("Workspace").CurrentRooms:FindFirstChild("50")) and game:GetService("ReplicatedStorage").GameData.LatestRoom.Value == 50 then
        wait()
        local Cham = Instance.new("Highlight")
        Cham.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
        Cham.FillColor = Color3.new(0, 1, 0.749019)
        Cham.FillTransparency = 0.5
        Cham.OutlineColor = Color3.new(0.792156, 0.792156, 0.792156)
        Cham.Parent = game:GetService("CoreGui")
        Cham.Enabled = OrionLib.Flags["BookToggle"].Value
        Cham.Adornee = inst
        Cham.RobloxLocked = true
        return Cham
    end
end

local function ApplyEntityChams(inst)
    wait()
    local Cham = Instance.new("Highlight")
    Cham.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
    Cham.FillColor = Color3.new(1, 0, 0)
    Cham.FillTransparency = 0.5
    Cham.OutlineColor = Color3.new(0.792156, 0.792156, 0.792156)
    Cham.Parent = game:GetService("CoreGui")
    Cham.Enabled = OrionLib.Flags["FigureToggle"].Value
    Cham.Adornee = inst
    Cham.RobloxLocked = true
    return Cham
end

local BookCoroutine = coroutine.create(function()
    task.wait(1)
    for i,v in pairs(game:GetService("Workspace").CurrentRooms["50"].Assets:GetDescendants()) do
        if v.Name == "LiveHintBook" then
            table.insert(BookChams,ApplyBookChams(v))
        end
    end
end)
local EntityCoroutine = coroutine.create(function()
    local Entity = game:GetService("Workspace").CurrentRooms["50"].FigureSetup:WaitForChild("FigureRagdoll",5)
    Entity:WaitForChild("Torso",2.5)
    table.insert(FigureChams,ApplyEntityChams(Entity))
end)


local GameTab = Window:MakeTab({
	Name = "Game",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local CharTab = Window:MakeTab({
	Name = "Character",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local TargetWalkspeed
CharTab:AddSlider({
	Name = "Speed",
	Min = 0,
	Max = 50,
	Default = 5,
	Color = Color3.fromRGB(255,255,255),
	Increment = 1,
	Callback = function(Value)
		TargetWalkspeed = Value
	end
})

local pcl = Instance.new("SpotLight")
pcl.Brightness = 1
pcl.Face = Enum.NormalId.Front
pcl.Range = 90
pcl.Parent = game.Players.LocalPlayer.Character.Head
pcl.Enabled = false


CharTab:AddToggle({
	Name = "Headlight",
	Default = false,
    Callback = function(Value)
        pcl.Enabled = Value
    end
})

GameTab:AddToggle({
	Name = "No seek arms/obstructions",
	Default = false,
    Flag = "NoSeek",
    Save = true
})

GameTab:AddToggle({
	Name = "Instant Interact",
	Default = false,
    Flag = "InstantToggle",
    Save = true
})
GameTab:AddButton({
	Name = "Skip level",
	Callback = function()
        pcall(function()
            local HasKey = false
            local CurrentDoor = workspace.CurrentRooms[tostring(game:GetService("ReplicatedStorage").GameData.LatestRoom.Value)]:WaitForChild("Door")
            for i,v in ipairs(CurrentDoor.Parent:GetDescendants()) do
                if v.Name == "KeyObtain" then
                    HasKey = v
                end
            end
            if HasKey then
                game.Players.LocalPlayer.Character:PivotTo(CF(HasKey.Hitbox.Position))
                wait(0.3)
                fireproximityprompt(HasKey.ModulePrompt,0)
                game.Players.LocalPlayer.Character:PivotTo(CF(CurrentDoor.Door.Position))
                wait(0.3)
                fireproximityprompt(CurrentDoor.Lock.UnlockPrompt,0)
            end
            if LatestRoom == 50 then
                CurrentDoor = workspace.CurrentRooms[tostring(LatestRoom+1)]:WaitForChild("Door")
            end
            game.Players.LocalPlayer.Character:PivotTo(CF(CurrentDoor.Door.Position))
            wait(0.3)
            CurrentDoor.ClientOpen:FireServer()
        end)
  	end
})

GameTab:AddToggle({
	Name = "Auto skip level",
	Default = false,
    Save = false,
    Flag = "AutoSkip"
})

local AutoSkipCoro = coroutine.create(function()
        while true do
            task.wait()
            pcall(function()
            if OrionLib.Flags["AutoSkip"].Value == true and game:GetService("ReplicatedStorage").GameData.LatestRoom.Value < 100 then
                local HasKey = false
                local LatestRoom = game:GetService("ReplicatedStorage").GameData.LatestRoom.Value
                local CurrentDoor = workspace.CurrentRooms[tostring(LatestRoom)]:WaitForChild("Door")
                for i,v in ipairs(CurrentDoor.Parent:GetDescendants()) do
                    if v.Name == "KeyObtain" then
                        HasKey = v
                    end
                end
                if HasKey then
                    game.Players.LocalPlayer.Character:PivotTo(CF(HasKey.Hitbox.Position))
                    task.wait(0.3)
                    fireproximityprompt(HasKey.ModulePrompt,0)
                    game.Players.LocalPlayer.Character:PivotTo(CF(CurrentDoor.Door.Position))
                    task.wait(0.3)
                    fireproximityprompt(CurrentDoor.Lock.UnlockPrompt,0)
                end
                if LatestRoom == 50 then
                    CurrentDoor = workspace.CurrentRooms[tostring(LatestRoom+1)]:WaitForChild("Door")
                end
                game.Players.LocalPlayer.Character:PivotTo(CF(CurrentDoor.Door.Position))
                task.wait(0.3)
                CurrentDoor.ClientOpen:FireServer()
            end
        end)
        end
end)
coroutine.resume(AutoSkipCoro)

GameTab:AddButton({
	Name = "No jumpscares",
	Callback = function()
        pcall(function()
            game:GetService("ReplicatedStorage").Bricks.Jumpscare:Destroy()
        end)
  	end
})
GameTab:AddToggle({
	Name = "Avoid Rush/Ambush",
	Default = false,
    Flag = "AvoidRushToggle",
    Save = true
})
GameTab:AddToggle({
	Name = "No Screech",
	Default = false,
    Flag = "ScreechToggle",
    Save = true
})

GameTab:AddToggle({
	Name = "Always win heartbeat",
	Default = false,
    Flag = "HeartbeatWin",
    Save = true
})

GameTab:AddToggle({
	Name = "Predict chases",
	Default = false,
    Flag = "PredictToggle" ,
    Save = true
})
GameTab:AddToggle({
	Name = "Notify when mob spawns",
	Default = false,
    Flag = "MobToggle" ,
    Save = true
})
GameTab:AddButton({
	Name = "Complete breaker box minigame",
	Callback = function()
        game:GetService("ReplicatedStorage").Bricks.EBF:FireServer()
  	end
})
GameTab:AddButton({
	Name = "Skip level 50",
	Callback = function()
        local CurrentDoor = workspace.CurrentRooms[tostring(LatestRoom+1)]:WaitForChild("Door")
        game.Players.LocalPlayer.Character:PivotTo(CF(CurrentDoor.Door.Position))
  	end
})
GameTab:AddParagraph("Warning","You may need to open/close the panel a few times for this to work, fixing soon.")

--// ok actual code starts here

game:GetService("RunService").RenderStepped:Connect(function()
    pcall(function()
        if game.Players.LocalPlayer.Character.Humanoid.MoveDirection.Magnitude > 0 then
            game.Players.LocalPlayer.Character:TranslateBy(game.Players.LocalPlayer.Character.Humanoid.MoveDirection * TargetWalkspeed/50)
        end
    end)
end)

game:GetService("Workspace").CurrentRooms.DescendantAdded:Connect(function(descendant)
    if OrionLib.Flags["NoSeek"].Value == true and descendant.Name == ("Seek_Arm" or "ChandelierObstruction") then
        task.spawn(function()
            wait()
            descendant:Destroy()
        end)
    end
end)

game:GetService("ProximityPromptService").PromptButtonHoldBegan:Connect(function(prompt)
    if OrionLib.Flags["InstantToggle"].Value == true then
        fireproximityprompt(prompt)
    end
end)

local old
old = hookmetamethod(game,"__namecall",newcclosure(function(self,...)
    local args = {...}
    local method = getnamecallmethod()

    if tostring(self) == 'Screech' and method == "FireServer" and OrionLib.Flags["ScreechToggle"].Value == true then
        args[1] = true
        return old(self,unpack(args))
    end
    if tostring(self) == 'ClutchHeartbeat' and method == "FireServer" and OrionLib.Flags["HeartbeatWin"].Value == true then
        args[2] = true
        return old(self,unpack(args))
    end

    return old(self,...)
end))

workspace.CurrentCamera.ChildAdded:Connect(function(child)
    if child.Name == "Screech" and OrionLib.Flags["ScreechToggle"].Value == true then
        child:Destroy()
    end
end)

local NotificationCoroutine = coroutine.create(function()
    LatestRoom.Changed:Connect(function()
        if OrionLib.Flags["PredictToggle"].Value == true then
            local n = ChaseStart.Value - LatestRoom.Value
            if 0 < n and n < 4 then
                OrionLib:MakeNotification({
                    Name = "Warning!",
                    Content = "Event in " .. tostring(n) .. " rooms.",
                    Time = 5
                })
            end
        end
        if OrionLib.Flags["BookToggle"].Value == true then
            if LatestRoom.Value == 50 then
                coroutine.resume(BookCoroutine)
            end
        end
        if OrionLib.Flags["FigureToggle"].Value == true then
            if LatestRoom.Value == 50 then
                coroutine.resume(EntityCoroutine)
            end
        end
    end)
    workspace.ChildAdded:Connect(function(inst)
        if inst.Name == "RushMoving" and OrionLib.Flags["MobToggle"].Value == true then
            if OrionLib.Flags["AvoidRushToggle"].Value == true then
                OrionLib:MakeNotification({
                    Name = "Warning!",
                    Content = "Avoiding Rush. Please wait.",
                    Time = 5
                })
                local OldPos = game.Players.LocalPlayer.Character.HumanoidRootPart.Position
                local con = game:GetService("RunService").Heartbeat:Connect(function()
                    game.Players.LocalPlayer.Character:MoveTo(OldPos + Vector3.new(0,20,0))
                end)

                inst.Destroying:Wait()
                con:Disconnect()

                game.Players.LocalPlayer.Character:MoveTo(OldPos)
            else
                OrionLib:MakeNotification({
                    Name = "Warning!",
                    Content = "Rush has spawned, hide!",
                    Time = 5
                })
            end
        elseif inst.Name == "AmbushMoving" and OrionLib.Flags["MobToggle"].Value == true then
            if OrionLib.Flags["AvoidRushToggle"].Value == true then
                OrionLib:MakeNotification({
                    Name = "Warning!",
                    Content = "Avoiding Ambush. Please wait.",
                    Time = 5
                })
                local OldPos = game.Players.LocalPlayer.Character.HumanoidRootPart.Position
                local con = game:GetService("RunService").Heartbeat:Connect(function()
                    game.Players.LocalPlayer.Character:MoveTo(OldPos + Vector3.new(0,20,0))
                end)

                inst.Destroying:Wait()
                con:Disconnect()

                game.Players.LocalPlayer.Character:MoveTo(OldPos)
            else
                OrionLib:MakeNotification({
                    Name = "Warning!",
                    Content = "Ambush has spawned, hide!",
                    Time = 5
                })
            end
        end
    end)
end)

--// ok actual code ends here

local CreditsTab = Window:MakeTab({
	Name = "Credits",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

CreditsTab:AddParagraph("Credits to","OminousVibes - (Got most of the ideas from their thread, check it out! - https://v3rmillion.net/showthread.php?tid=1184088)")

coroutine.resume(NotificationCoroutine)

OrionLib:Init()

task.wait(2)
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "Doors Script 2",
	Callback = function()
        loadstring(game:HttpGetAsync("https://pastebin.com/raw/R8QMbhzv"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]local Tab = Window:MakeTab({
	Name = "Basketball Legends",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Op Aimbot",
	Callback = function()
        getgenv().greenNumber = 72.34 -- keep this number around 72
getgenv().unlockfps = true -- reccomend
getgenv().keytoclick = "E" -- dont change this
getgenv().customautogreen = Enum.KeyCode.R -- press R if you dont want to hold shoot button

loadstring(game:HttpGet('https://raw.githubusercontent.com/notxkid/scriptsbecauseimbored/main/basketballlegends.lua'))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
local Tab = Window:MakeTab({
	Name = "Anime Sprit",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]
Tab:AddButton({
	Name = "Anime sprit",
	Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Omgshit/Scripts/main/MainLoader.lua"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
Tab:AddButton({
	Name = "callfunction virtual imput",
	Callback = function()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
