local Players = game:GetService("Players")
local StarterGui = game:GetService("StarterGui")
local RunService = game:GetService("RunService")
local UserInputService = game:GetService("UserInputService")

local player = Players.LocalPlayer
local mouse = player:GetMouse()local function estilizar(guiObject, radius)
    if guiObject:IsA("TextButton") or guiObject:IsA("TextBox") or guiObject:IsA("TextLabel") then
        guiObject.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
        guiObject.TextColor3 = Color3.fromRGB(255, 255, 255)
        guiObject.Font = Enum.Font.SourceSansBold
        guiObject.TextScaled = true
        guiObject.AutoButtonColor = false
        local uicorner = Instance.new("UICorner", guiObject)
        uicorner.CornerRadius = UDim.new(0, radius or 6)
    end
end

local function aplicarClique(button)
    local clickSound = Instance.new("Sound")
    clickSound.SoundId = "rbxassetid://9118824985"
    clickSound.Volume = 0.3
    clickSound.Parent = button
    button.MouseButton1Click:Connect(function()
        clickSound:Play()
    end)
endlocal screenGui = Instance.new("ScreenGui", player:WaitForChild("PlayerGui"))
screenGui.Name = "HeitorzaoHub"

local frame = Instance.new("Frame", screenGui)
frame.Size = UDim2.new(0, 320, 0, 650)
frame.Position = UDim2.new(0.5, -160, 0.5, -325)
frame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
frame.Active = true
frame.Draggable = true
local frameCorner = Instance.new("UICorner", frame)
frameCorner.CornerRadius = UDim.new(0, 12)

local title = Instance.new("TextLabel", frame)
title.Size = UDim2.new(1, 0, 0, 40)
title.Position = UDim2.new(0, 0, 0, 0)
title.BackgroundTransparency = 1
title.Text = "HEITORZÃO HUB"
title.TextColor3 = Color3.fromRGB(255, 0, 0)
title.Font = Enum.Font.SourceSansBold
title.TextScaled = truespawn(function()
    local step = 5
    while true do
        for i = 0, 255, step do
            title.TextColor3 = Color3.fromRGB(255, i, 0)
            wait(0.02)
        end
        for i = 255, 0, -step do
            title.TextColor3 = Color3.fromRGB(i, 255, 0)
            wait(0.02)
        end
        for i = 0, 255, step do
            title.TextColor3 = Color3.fromRGB(0, 255, i)
            wait(0.02)
        end
        for i = 255, 0, -step do
            title.TextColor3 = Color3.fromRGB(0, i, 255)
            wait(0.02)
        end
        for i = 0, 255, step do
            title.TextColor3 = Color3.fromRGB(i, 0, 255)
            wait(0.02)
        end
        for i = 255, 0, -step do
            title.TextColor3 = Color3.fromRGB(255, 0, i)
            wait(0.02)
        end
    end
end)local closeBtn = Instance.new("TextButton", frame)
closeBtn.Size = UDim2.new(0, 30, 0, 30)
closeBtn.Position = UDim2.new(1, -35, 0, 5)
closeBtn.Text = "X"
estilizar(closeBtn, 12)
aplicarClique(closeBtn)
closeBtn.BackgroundColor3 = Color3.fromRGB(180, 50, 50)
closeBtn.MouseButton1Click:Connect(function()
    screenGui:Destroy()
end)

local minimizeBtn = Instance.new("TextButton", frame)
minimizeBtn.Size = UDim2.new(0, 30, 0, 30)
minimizeBtn.Position = UDim2.new(1, -70, 0, 5)
minimizeBtn.Text = "_"
estilizar(minimizeBtn, 12)
aplicarClique(minimizeBtn)
minimizeBtn.BackgroundColor3 = Color3.fromRGB(100, 100, 100)
local minimized = false
minimizeBtn.MouseButton1Click:Connect(function()
    if minimized then
        frame.Size = UDim2.new(0, 320, 0, 650)
        minimized = false
    else
        frame.Size = UDim2.new(0, 320, 0, 40)
        minimized = true
    end
end)local defaultSpeed = 16
local currentSpeed = defaultSpeed

local speedInput = Instance.new("TextBox", frame)
speedInput.Size = UDim2.new(0, 100, 0, 30)
speedInput.Position = UDim2.new(0, 40, 0, 50)
speedInput.PlaceholderText = "Digite a velocidade"
speedInput.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
speedInput.TextColor3 = Color3.new(1, 1, 1)
estilizar(speedInput, 6)

local applySpeedBtn = Instance.new("TextButton", frame)
applySpeedBtn.Size = UDim2.new(0, 60, 0, 30)
applySpeedBtn.Position = UDim2.new(0, 150, 0, 50)
applySpeedBtn.Text = "Aplicar"
applySpeedBtn.BackgroundColor3 = Color3.fromRGB(50, 100, 200)
applySpeedBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(applySpeedBtn, 6)
aplicarClique(applySpeedBtn)

local removeSpeedBtn = Instance.new("TextButton", frame)
removeSpeedBtn.Size = UDim2.new(0, 60, 0, 30)
removeSpeedBtn.Position = UDim2.new(0, 220, 0, 50)
removeSpeedBtn.Text = "Retirar"
removeSpeedBtn.BackgroundColor3 = Color3.fromRGB(200, 50, 50)
removeSpeedBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(removeSpeedBtn, 6)
aplicarClique(removeSpeedBtn)local plusSpeedBtn = Instance.new("TextButton", frame)
plusSpeedBtn.Size = UDim2.new(0, 30, 0, 30)
plusSpeedBtn.Position = UDim2.new(0, 10, 0, 50)
plusSpeedBtn.Text = "+"
plusSpeedBtn.BackgroundColor3 = Color3.fromRGB(50, 200, 50)
plusSpeedBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(plusSpeedBtn, 6)
aplicarClique(plusSpeedBtn)

local minusSpeedBtn = Instance.new("TextButton", frame)
minusSpeedBtn.Size = UDim2.new(0, 30, 0, 30)
minusSpeedBtn.Position = UDim2.new(0, 280, 0, 50)
minusSpeedBtn.Text = "-"
minusSpeedBtn.BackgroundColor3 = Color3.fromRGB(200, 50, 50)
minusSpeedBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(minusSpeedBtn, 6)
aplicarClique(minusSpeedBtn)local function getHumanoid()
    if player.Character then
        return player.Character:FindFirstChildOfClass("Humanoid")
    end
    return nil
end

local function updateSpeed(newSpeed)
    local humanoid = getHumanoid()
    if humanoid then
        humanoid.WalkSpeed = newSpeed
        StarterGui:SetCore("SendNotification", {
            Title = "Velocidade Atualizada",
            Text = "Velocidade ajustada para " .. tostring(newSpeed),
            Duration = 2
        })
    end
end

applySpeedBtn.MouseButton1Click:Connect(function()
    local val = tonumber(speedInput.Text)
    if val and val > 0 and val <= 500 then
        currentSpeed = val
        updateSpeed(currentSpeed)
    else
        StarterGui:SetCore("SendNotification", {
            Title = "Erro",
            Text = "Digite um número válido (1-500)",
            Duration = 2
        })
    end
end)

removeSpeedBtn.MouseButton1Click:Connect(function()
    currentSpeed = defaultSpeed
    updateSpeed(currentSpeed)
    speedInput.Text = ""
    StarterGui:SetCore("SendNotification", {
        Title = "Velocidade Resetada",
        Text = "Velocidade voltou ao padrão (" .. tostring(defaultSpeed) .. ")",
        Duration = 2
    })
end)

plusSpeedBtn.MouseButton1Click:Connect(function()
    currentSpeed = currentSpeed + 1
    updateSpeed(currentSpeed)
end)

minusSpeedBtn.MouseButton1Click:Connect(function()
    currentSpeed = math.max(1, currentSpeed - 1)
    updateSpeed(currentSpeed)
end)local invisBtn = Instance.new("TextButton", frame)
invisBtn.Size = UDim2.new(0, 100, 0, 30)
invisBtn.Position = UDim2.new(0, 40, 0, 90)
invisBtn.Text = "Invisível"
invisBtn.BackgroundColor3 = Color3.fromRGB(100, 100, 100)
invisBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(invisBtn, 6)
aplicarClique(invisBtn)

local invisOffBtn = Instance.new("TextButton", frame)
invisOffBtn.Size = UDim2.new(0, 100, 0, 30)
invisOffBtn.Position = UDim2.new(0, 150, 0, 90)
invisOffBtn.Text = "Visível"
invisOffBtn.BackgroundColor3 = Color3.fromRGB(100, 100, 100)
invisOffBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(invisOffBtn, 6)
aplicarClique(invisOffBtn)local function setInvisible(on)
    if player.Character then
        for _, part in pairs(player.Character:GetChildren()) do
            if part:IsA("BasePart") then
                part.Transparency = on and 1 or 0
                if part:FindFirstChildOfClass("Decal") then
                    part:FindFirstChildOfClass("Decal").Transparency = on and 1 or 0
                end
            elseif part:IsA("Accessory") and part:FindFirstChild("Handle") then
                part.Handle.Transparency = on and 1 or 0
            end
        end
    end
end

invisBtn.MouseButton1Click:Connect(function()
    setInvisible(true)
    StarterGui:SetCore("SendNotification", {
        Title = "Modo Invisível",
        Text = "Você está invisível",
        Duration = 2
    })
end)

invisOffBtn.MouseButton1Click:Connect(function()
    setInvisible(false)
    StarterGui:SetCore("SendNotification", {
        Title = "Modo Invisível",
        Text = "Você está visível",
        Duration = 2
    })
end)local noclipOnBtn = Instance.new("TextButton", frame)
noclipOnBtn.Size = UDim2.new(0, 100, 0, 30)
noclipOnBtn.Position = UDim2.new(0, 40, 0, 130)
noclipOnBtn.Text = "Noclip ON"
noclipOnBtn.BackgroundColor3 = Color3.fromRGB(100, 100, 100)
noclipOnBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(noclipOnBtn, 6)
aplicarClique(noclipOnBtn)

local noclipOffBtn = Instance.new("TextButton", frame)
noclipOffBtn.Size = UDim2.new(0, 100, 0, 30)
noclipOffBtn.Position = UDim2.new(0, 150, 0, 130)
noclipOffBtn.Text = "Noclip OFF"
noclipOffBtn.BackgroundColor3 = Color3.fromRGB(100, 100, 100)
noclipOffBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(noclipOffBtn, 6)
aplicarClique(noclipOffBtn)local noclipEnabled = false

local function noclipLoop()
    while noclipEnabled do
        RunService.Stepped:Wait()
        if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
            player.Character.HumanoidRootPart.CanCollide = false
        end
    end
end

noclipOnBtn.MouseButton1Click:Connect(function()
    noclipEnabled = true
    StarterGui:SetCore("SendNotification", {
        Title = "Noclip",
        Text = "Noclip ativado",
        Duration = 2
    })
    coroutine.wrap(noclipLoop)()
end)

noclipOffBtn.MouseButton1Click:Connect(function()
    noclipEnabled = false
    if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
        player.Character.HumanoidRootPart.CanCollide = true
    end
    StarterGui:SetCore("SendNotification", {
        Title = "Noclip",
        Text = "Noclip desativado",
        Duration = 2
    })
end)local flying = false
local flySpeed = 50
local flyVelocity

local flyBtn = Instance.new("TextButton", frame)
flyBtn.Size = UDim2.new(0, 100, 0, 30)
flyBtn.Position = UDim2.new(0, 40, 0, 170)
flyBtn.Text = "Voar ON"
flyBtn.BackgroundColor3 = Color3.fromRGB(50, 150, 255)
flyBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(flyBtn, 6)
aplicarClique(flyBtn)

local flyOffBtn = Instance.new("TextButton", frame)
flyOffBtn.Size = UDim2.new(0, 100, 0, 30)
flyOffBtn.Position = UDim2.new(0, 150, 0, 170)
flyOffBtn.Text = "Voar OFF"
flyOffBtn.BackgroundColor3 = Color3.fromRGB(200, 100, 100)
flyOffBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(flyOffBtn, 6)
aplicarClique(flyOffBtn)local flyAnimTrack
local flyAnimPlaying = false

local function startFly()
    local char = player.Character
    if not char then return end
    local hrp = char:FindFirstChild("HumanoidRootPart")
    local humanoid = char:FindFirstChildOfClass("Humanoid")
    if not hrp or not humanoid then return end

    flying = true
    flyVelocity = Instance.new("BodyVelocity")
    flyVelocity.Velocity = Vector3.new(0,0,0)
    flyVelocity.MaxForce = Vector3.new(1e5, 1e5, 1e5)
    flyVelocity.Parent = hrp

    local animator = humanoid:FindFirstChildOfClass("Animator") or humanoid:WaitForChild("Animator")
    local animation = Instance.new("Animation")
    animation.AnimationId = "rbxassetid://7502259917"
    flyAnimTrack = animator:LoadAnimation(animation)
    flyAnimTrack:Play()
    flyAnimTrack.Looped = true
    flyAnimPlaying = true

    local connection
    connection = RunService.Heartbeat:Connect(function()
        if flying then
            local move = Vector3.new()
            if UserInputService:IsKeyDown(Enum.KeyCode.W) then
                move = move + workspace.CurrentCamera.CFrame.LookVector
            end
            if UserInputService:IsKeyDown(Enum.KeyCode.S) then
                move = move - workspace.CurrentCamera.CFrame.LookVector
            end
            if UserInputService:IsKeyDown(Enum.KeyCode.A) then
                move = move - workspace.CurrentCamera.CFrame.RightVector
            end
            if UserInputService:IsKeyDown(Enum.KeyCode.D) then
                move = move + workspace.CurrentCamera.CFrame.RightVector
            end
            flyVelocity.Velocity = move.Unit * flySpeed
        else
            flyVelocity:Destroy()
            connection:Disconnect()
            if flyAnimPlaying then
                flyAnimTrack:Stop()
                flyAnimPlaying = false
            end
        end
    end)
endflyBtn.MouseButton1Click:Connect(function()
    if not flying then
        startFly()
        StarterGui:SetCore("SendNotification", {
            Title = "Voo",
            Text = "Voo ativado",
            Duration = 2
        })
    end
end)

flyOffBtn.MouseButton1Click:Connect(function()
    flying = false
    StarterGui:SetCore("SendNotification", {
        Title = "Voo",
        Text = "Voo desativado",
        Duration = 2
    })
end)local jumpInfiniteBtn = Instance.new("TextButton", frame)
jumpInfiniteBtn.Size = UDim2.new(0, 100, 0, 30)
jumpInfiniteBtn.Position = UDim2.new(0, 40, 0, 210)
jumpInfiniteBtn.Text = "Pulo Infinito"
jumpInfiniteBtn.BackgroundColor3 = Color3.fromRGB(100, 150, 100)
jumpInfiniteBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(jumpInfiniteBtn, 6)
aplicarClique(jumpInfiniteBtn)

local jumpEnabled = false
jumpInfiniteBtn.MouseButton1Click:Connect(function()
    jumpEnabled = not jumpEnabled
    if jumpEnabled then
        StarterGui:SetCore("SendNotification", {
            Title = "Pulo Infinito",
            Text = "Ativado",
            Duration = 2
        })
    else
        StarterGui:SetCore("SendNotification", {
            Title = "Pulo Infinito",
            Text = "Desativado",
            Duration = 2
        })
    end
end)RunService.Stepped:Connect(function()
    if jumpEnabled then
        local humanoid = getHumanoid()
        if humanoid and humanoid:GetState() ~= Enum.HumanoidStateType.Jumping and humanoid:GetState() ~= Enum.HumanoidStateType.Freefall then
            humanoid:ChangeState(Enum.HumanoidStateType.Jumping)
        end
    end
end)local espBtn = Instance.new("TextButton", frame)
espBtn.Size = UDim2.new(0, 100, 0, 30)
espBtn.Position = UDim2.new(0, 40, 0, 250)
espBtn.Text = "Ativar ESP"
espBtn.BackgroundColor3 = Color3.fromRGB(150, 100, 200)
espBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(espBtn, 6)
aplicarClique(espBtn)

local espEnabled = false
local espFolder = Instance.new("Folder", screenGui)
espFolder.Name = "ESPFolder"

espBtn.MouseButton1Click:Connect(function()
    espEnabled = not espEnabled
    espFolder:ClearAllChildren()
    if espEnabled then
        for _, plr in pairs(Players:GetPlayers()) do
            if plr ~= player and plr.Character and plr.Character:FindFirstChild("Head") then
                local billboard = Instance.new("BillboardGui", espFolder)
                billboard.Adornee = plr.Character.Head
                billboard.Size = UDim2.new(0, 100, 0, 40)
                billboard.StudsOffset = Vector3.new(0, 2, 0)
                billboard.AlwaysOnTop = true

                local nameLabel = Instance.new("TextLabel", billboard)
                nameLabel.Size = UDim2.new(1, 0, 1, 0)
                nameLabel.BackgroundTransparency = 1
                nameLabel.TextColor3 = Color3.new(1, 0, 0)
                nameLabel.TextScaled = true
                nameLabel.Text = plr.Name
                nameLabel.Font = Enum.Font.SourceSansBold
            end
        end
        StarterGui:SetCore("SendNotification", {
            Title = "ESP",
            Text = "ESP Ativado",
            Duration = 2
        })
    else
        espFolder:ClearAllChildren()
        StarterGui:SetCore("SendNotification", {
            Title = "ESP",
            Text = "ESP Desativado",
            Duration = 2
        })
    end
end)local clockLabel = Instance.new("TextLabel", frame)
clockLabel.Size = UDim2.new(0, 280, 0, 20)
clockLabel.Position = UDim2.new(0, 20, 0, 610)
clockLabel.BackgroundTransparency = 1
clockLabel.TextColor3 = Color3.new(1, 1, 1)
clockLabel.Font = Enum.Font.SourceSans
clockLabel.TextScaled = true

spawn(function()
    while true do
        local hora = os.date("!*t")
        hora.hour = (hora.hour - 3) % 24
        local texto = string.format("%02d:%02d:%02d", hora.hour, hora.min, hora.sec)
        clockLabel.Text = "Horário de Brasília: " .. texto
        wait(1)
    end
end)StarterGui:SetCore("SendNotification", {
    Title = "HEITORZÃO HUB",
    Text = "VOCÊ ESTÁ USANDO HEITORZÃO HUB",
    Duration = 4
})local tempo = 0
local rodando = false

local cronometroLabel = Instance.new("TextLabel", frame)
cronometroLabel.Size = UDim2.new(0, 280, 0, 20)
cronometroLabel.Position = UDim2.new(0, 20, 0, 580)
cronometroLabel.BackgroundTransparency = 1
cronometroLabel.TextColor3 = Color3.new(1, 1, 1)
cronometroLabel.Font = Enum.Font.SourceSans
cronometroLabel.TextScaled = true
cronometroLabel.Text = "Cronômetro: 00:00"

local function atualizarCronometro()
    local minutos = math.floor(tempo / 60)
    local segundos = tempo % 60
    cronometroLabel.Text = string.format("Cronômetro: %02d:%02d", minutos, segundos)
end

spawn(function()
    while true do
        wait(1)
        if rodando then
            tempo = tempo + 1
            atualizarCronometro()
        end
    end
end)

local iniciarBtn = Instance.new("TextButton", frame)
iniciarBtn.Size = UDim2.new(0, 80, 0, 30)
iniciarBtn.Position = UDim2.new(0, 20, 0, 540)
iniciarBtn.Text = "Iniciar"
iniciarBtn.BackgroundColor3 = Color3.fromRGB(0, 170, 0)
estilizar(iniciarBtn, 6)
aplicarClique(iniciarBtn)
iniciarBtn.MouseButton1Click:Connect(function()
    rodando = true
end)

local pausarBtn = Instance.new("TextButton", frame)
pausarBtn.Size = UDim2.new(0, 80, 0, 30)
pausarBtn.Position = UDim2.new(0, 110, 0, 540)
pausarBtn.Text = "Pausar"
pausarBtn.BackgroundColor3 = Color3.fromRGB(200, 170, 0)
estilizar(pausarBtn, 6)
aplicarClique(pausarBtn)
pausarBtn.MouseButton1Click:Connect(function()
    rodando = false
end)

local resetarBtn = Instance.new("TextButton", frame)
resetarBtn.Size = UDim2.new(0, 80, 0, 30)
resetarBtn.Position = UDim2.new(0, 200, 0, 540)
resetarBtn.Text = "Resetar"
resetarBtn.BackgroundColor3 = Color3.fromRGB(170, 0, 0)
estilizar(resetarBtn, 6)
aplicarClique(resetarBtn)
resetarBtn.MouseButton1Click:Connect(function()
    rodando = false
    tempo = 0
    atualizarCronometro()
end)local nomeInput = Instance.new("TextBox", frame)
nomeInput.Size = UDim2.new(0, 260, 0, 30)
nomeInput.Position = UDim2.new(0, 30, 0, 300)
nomeInput.PlaceholderText = "Digite o nome do jogador"
estilizar(nomeInput, 6)local animarOutroBtn = Instance.new("TextButton", frame)
animarOutroBtn.Size = UDim2.new(0, 260, 0, 30)
animarOutroBtn.Position = UDim2.new(0, 30, 0, 340)
animarOutroBtn.Text = "Animar jogador com Invencível"
animarOutroBtn.BackgroundColor3 = Color3.fromRGB(50, 50, 200)
estilizar(animarOutroBtn, 6)
aplicarClique(animarOutroBtn)

animarOutroBtn.MouseButton1Click:Connect(function()
    local nome = nomeInput.Text
    local target = Players:FindFirstChild(nome)
    if target and target.Character and target.Character:FindFirstChildOfClass("Humanoid") then
        local humanoid = target.Character:FindFirstChildOfClass("Humanoid")
        local animator = humanoid:FindFirstChildOfClass("Animator") or humanoid:WaitForChild("Animator")
        local anim = Instance.new("Animation")
        anim.AnimationId = "rbxassetid://7502259917"
        local track = animator:LoadAnimation(anim)
        track:Play()
        StarterGui:SetCore("SendNotification", {
            Title = "Animação",
            Text = "Invencível ativado no jogador!",
            Duration = 2
        })
    else
        StarterGui:SetCore("SendNotification", {
            Title = "Erro",
            Text = "Jogador não encontrado!",
            Duration = 2
        })
    end
end)local animarEuBtn = Instance.new("TextButton", frame)
animarEuBtn.Size = UDim2.new(0, 260, 0, 30)
animarEuBtn.Position = UDim2.new(0, 30, 0, 380)
animarEuBtn.Text = "Usar Animação Invencível"
animarEuBtn.BackgroundColor3 = Color3.fromRGB(50, 150, 255)
estilizar(animarEuBtn, 6)
aplicarClique(animarEuBtn)

animarEuBtn.MouseButton1Click:Connect(function()
    if player.Character and player.Character:FindFirstChildOfClass("Humanoid") then
        local humanoid = player.Character:FindFirstChildOfClass("Humanoid")
        local animator = humanoid:FindFirstChildOfClass("Animator") or humanoid:WaitForChild("Animator")
        local anim = Instance.new("Animation")
        anim.AnimationId = "rbxassetid://7502259917"
        local track = animator:LoadAnimation(anim)
        track:Play()
        StarterGui:SetCore("SendNotification", {
            Title = "Animação",
            Text = "Animação Invencível ativada!",
            Duration = 2
        })
    end
end)local horarioLabel = Instance.new("TextLabel", frame)
horarioLabel.Size = UDim2.new(0, 260, 0, 25)
horarioLabel.Position = UDim2.new(0, 30, 0, 620)
horarioLabel.BackgroundTransparency = 1
horarioLabel.TextColor3 = Color3.new(1, 1, 1)
horarioLabel.Font = Enum.Font.SourceSans
horarioLabel.TextScaled = true
horarioLabel.Text = "Horário de Brasília: --:--:--"

spawn(function()
    while true do
        local horaAtual = os.date("!*t")
        local horaBrasilia = {
            hour = (horaAtual.hour - 3) % 24,
            min = horaAtual.min,
            sec = horaAtual.sec
        }
        horarioLabel.Text = string.format("Horário de Brasília: %02d:%02d:%02d", horaBrasilia.hour, horaBrasilia.min, horaBrasilia.sec)
        wait(1)
    end
end)StarterGui:SetCore("SendNotification", {
    Title = "HEITORZÃO HUB",
    Text = "VOCÊ ESTÁ USANDO HEITORZÃO HUB",
    Duration = 4
})local musica = Instance.new("Sound", workspace)
musica.SoundId = "rbxassetid://9121286626" -- Arctic Monkeys - 505
musica.Looped = true
musica.Volume = 1
musica:Play()local neon = Instance.new("UIStroke", frame)
neon.Thickness = 3
neon.Color = Color3.fromRGB(255, 0, 255)

spawn(function()
    local cores = {
        Color3.fromRGB(255, 0, 0),
        Color3.fromRGB(255, 127, 0),
        Color3.fromRGB(255, 255, 0),
        Color3.fromRGB(0, 255, 0),
        Color3.fromRGB(0, 255, 255),
        Color3.fromRGB(0, 0, 255),
        Color3.fromRGB(139, 0, 255)
    }
    while true do
        for _, cor in ipairs(cores) do
            neon.Color = cor
            wait(0.2)
        end
    end
end)local tempo = 0
local rodando = false
local cronometroLabel = Instance.new("TextLabel", frame)
cronometroLabel.Size = UDim2.new(0, 200, 0, 25)
cronometroLabel.Position = UDim2.new(0, 60, 0, 580)
cronometroLabel.BackgroundTransparency = 1
cronometroLabel.TextColor3 = Color3.new(1,1,1)
cronometroLabel.Font = Enum.Font.SourceSans
cronometroLabel.TextScaled = true
cronometroLabel.Text = "00:00:00"

local function formatarTempo(segundos)
    local h = math.floor(segundos / 3600)
    local m = math.floor((segundos % 3600) / 60)
    local s = segundos % 60
    return string.format("%02d:%02d:%02d", h, m, s)
end

spawn(function()
    while true do
        if rodando then
            tempo = tempo + 1
            cronometroLabel.Text = formatarTempo(tempo)
        end
        wait(1)
    end
end)local iniciarBtn = Instance.new("TextButton", frame)
iniciarBtn.Size = UDim2.new(0, 70, 0, 25)
iniciarBtn.Position = UDim2.new(0, 30, 0, 550)
iniciarBtn.Text = "Iniciar"
estilizar(iniciarBtn, 6)
aplicarClique(iniciarBtn)
iniciarBtn.MouseButton1Click:Connect(function()
    rodando = true
end)

local pausarBtn = Instance.new("TextButton", frame)
pausarBtn.Size = UDim2.new(0, 70, 0, 25)
pausarBtn.Position = UDim2.new(0, 125, 0, 550)
pausarBtn.Text = "Pausar"
estilizar(pausarBtn, 6)
aplicarClique(pausarBtn)
pausarBtn.MouseButton1Click:Connect(function()
    rodando = false
end)

local resetarBtn = Instance.new("TextButton", frame)
resetarBtn.Size = UDim2.new(0, 70, 0, 25)
resetarBtn.Position = UDim2.new(0, 220, 0, 550)
resetarBtn.Text = "Resetar"
estilizar(resetarBtn, 6)
aplicarClique(resetarBtn)
resetarBtn.MouseButton1Click:Connect(function()
    tempo = 0
    cronometroLabel.Text = "00:00:00"
end)local nomeInput = Instance.new("TextBox", frame)
nomeInput.Size = UDim2.new(0, 200, 0, 30)
nomeInput.Position = UDim2.new(0, 60, 0, 510)
nomeInput.PlaceholderText = "Nome do jogador"
nomeInput.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
nomeInput.TextColor3 = Color3.new(1, 1, 1)
estilizar(nomeInput, 6)local animarBtn = Instance.new("TextButton", frame)
animarBtn.Size = UDim2.new(0, 200, 0, 30)
animarBtn.Position = UDim2.new(0, 60, 0, 480)
animarBtn.Text = "Animar Jogador"
estilizar(animarBtn, 6)
aplicarClique(animarBtn)

animarBtn.MouseButton1Click:Connect(function()
    local nome = nomeInput.Text
    local alvo = Players:FindFirstChild(nome)
    if alvo and alvo.Character then
        local humanoid = alvo.Character:FindFirstChildOfClass("Humanoid")
        if humanoid then
            local anim = Instance.new("Animation")
            anim.AnimationId = "rbxassetid://7502259917"
            local track = humanoid:LoadAnimation(anim)
            track:Play()
        end
    else
        StarterGui:SetCore("SendNotification", {
            Title = "Erro",
            Text = "Jogador não encontrado",
            Duration = 2
        })
    end
end)local horaLabel = Instance.new("TextLabel", frame)
horaLabel.Size = UDim2.new(0, 200, 0, 25)
horaLabel.Position = UDim2.new(0, 60, 0, 620)
horaLabel.BackgroundTransparency = 1
horaLabel.TextColor3 = Color3.new(1,1,1)
horaLabel.Font = Enum.Font.SourceSans
horaLabel.TextScaled = true
horaLabel.Text = "Horário de Brasília"

spawn(function()
    while true do
        local hora = os.date("!*t")
        hora.hour = hora.hour - 3
        if hora.hour < 0 then hora.hour = hora.hour + 24 end
        local horaFormatada = string.format("%02d:%02d:%02d", hora.hour, hora.min, hora.sec)
        horaLabel.Text = "Brasília: " .. horaFormatada
        wait(1)
    end
end)local musica = Instance.new("Sound", workspace)
musica.Name = "HeitorMusic"
musica.SoundId = "rbxassetid://9013142630" -- 505
musica.Volume = 2
musica.Looped = true
musica:Play()StarterGui:SetCore("SendNotification", {
    Title = "🎧 HEITORZÃO HUB",
    Text = "VOCÊ ESTÁ USANDO HEITORZÃO HUB",
    Duration = 5
})local glow = Instance.new("UIStroke", frame)
glow.Thickness = 3
glow.Transparency = 0
glow.Color = Color3.fromRGB(255, 0, 0)

spawn(function()
    while true do
        for i = 0, 255, 5 do
            glow.Color = Color3.fromRGB(255, i, 0)
            wait(0.02)
        end
        for i = 255, 0, -5 do
            glow.Color = Color3.fromRGB(i, 255, 0)
            wait(0.02)
        end
        for i = 0, 255, 5 do
            glow.Color = Color3.fromRGB(0, 255, i)
            wait(0.02)
        end
        for i = 255, 0, -5 do
            glow.Color = Color3.fromRGB(0, i, 255)
            wait(0.02)
        end
        for i = 0, 255, 5 do
            glow.Color = Color3.fromRGB(i, 0, 255)
            wait(0.02)
        end
        for i = 255, 0, -5 do
            glow.Color = Color3.fromRGB(255, 0, i)
            wait(0.02)
        end
    end
end)local playerNameBox = Instance.new("TextBox", frame)
playerNameBox.Size = UDim2.new(0, 240, 0, 30)
playerNameBox.Position = UDim2.new(0, 40, 0, 250)
playerNameBox.PlaceholderText = "Digite o nome do jogador"
playerNameBox.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
playerNameBox.TextColor3 = Color3.new(1, 1, 1)
estilizar(playerNameBox, 6)local animarOutroBtn = Instance.new("TextButton", frame)
animarOutroBtn.Size = UDim2.new(0, 240, 0, 30)
animarOutroBtn.Position = UDim2.new(0, 40, 0, 290)
animarOutroBtn.Text = "Usar animação em jogador"
animarOutroBtn.BackgroundColor3 = Color3.fromRGB(90, 90, 180)
animarOutroBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(animarOutroBtn, 6)
aplicarClique(animarOutroBtn)

animarOutroBtn.MouseButton1Click:Connect(function()
    local nome = playerNameBox.Text
    local target = Players:FindFirstChild(nome)
    if target and target.Character then
        local humanoid = target.Character:FindFirstChildOfClass("Humanoid")
        if humanoid then
            local anim = Instance.new("Animation")
            anim.AnimationId = "rbxassetid://7502259917"
            local track = humanoid:LoadAnimation(anim)
            track:Play()
        end
    else
        StarterGui:SetCore("SendNotification", {
            Title = "Erro",
            Text = "Jogador não encontrado ou nome incorreto.",
            Duration = 3
        })
    end
end)local animarBtn = Instance.new("TextButton", frame)
animarBtn.Size = UDim2.new(0, 240, 0, 30)
animarBtn.Position = UDim2.new(0, 40, 0, 330)
animarBtn.Text = "Usar animação Invencível"
animarBtn.BackgroundColor3 = Color3.fromRGB(50, 100, 200)
animarBtn.TextColor3 = Color3.new(1, 1, 1)
estilizar(animarBtn, 6)
aplicarClique(animarBtn)

animarBtn.MouseButton1Click:Connect(function()
    if player.Character then
        local humanoid = player.Character:FindFirstChildOfClass("Humanoid")
        if humanoid then
            local anim = Instance.new("Animation")
            anim.AnimationId = "rbxassetid://7502259917"
            local track = humanoid:LoadAnimation(anim)
            track:Play()
        end
    end
end)Players.PlayerChatted:Connect(function(p, msg)
    if msg:sub(1,5) == "!msg " then
        local content = msg:sub(6)
        local nome, texto = content:match("^(%S+)%s+(.+)$")
        if nome and texto then
            local alvo = Players:FindFirstChild(nome)
            if alvo and alvo ~= p then
                StarterGui:SetCore("ChatMakeSystemMessage", {
                    Text = "[Mensagem privada de " .. p.Name .. "]: " .. texto;
                    Color = Color3.fromRGB(255, 200, 255);
                })
            end
        end
    end
end)local tempo = 0
local rodando = false
local cronometroLabel = Instance.new("TextLabel", frame)
cronometroLabel.Size = UDim2.new(0, 240, 0, 25)
cronometroLabel.Position = UDim2.new(0, 40, 0, 370)
cronometroLabel.BackgroundTransparency = 1
cronometroLabel.TextColor3 = Color3.new(1,1,1)
cronometroLabel.Font = Enum.Font.SourceSansBold
cronometroLabel.TextScaled = true
cronometroLabel.Text = "00:00"

spawn(function()
    while true do
        if rodando then
            tempo = tempo + 1
            local min = math.floor(tempo / 60)
            local sec = tempo % 60
            cronometroLabel.Text = string.format("%02d:%02d", min, sec)
        end
        wait(1)
    end
end)local iniciarBtn = Instance.new("TextButton", frame)
iniciarBtn.Size = UDim2.new(0, 70, 0, 25)
iniciarBtn.Position = UDim2.new(0, 40, 0, 400)
iniciarBtn.Text = "Iniciar"
estilizar(iniciarBtn, 6)
aplicarClique(iniciarBtn)

local pausarBtn = Instance.new("TextButton", frame)
pausarBtn.Size = UDim2.new(0, 70, 0, 25)
pausarBtn.Position = UDim2.new(0, 120, 0, 400)
pausarBtn.Text = "Pausar"
estilizar(pausarBtn, 6)
aplicarClique(pausarBtn)

local resetarBtn = Instance.new("TextButton", frame)
resetarBtn.Size = UDim2.new(0, 70, 0, 25)
resetarBtn.Position = UDim2.new(0, 200, 0, 400)
resetarBtn.Text = "Resetar"
estilizar(resetarBtn, 6)
aplicarClique(resetarBtn)

iniciarBtn.MouseButton1Click:Connect(function()
    rodando = true
end)

pausarBtn.MouseButton1Click:Connect(function()
    rodando = false
end)

resetarBtn.MouseButton1Click:Connect(function()
    rodando = false
    tempo = 0
    cronometroLabel.Text = "00:00"
end)local function criarESP(player)
    if player == Players.LocalPlayer then return end
    player.CharacterAdded:Connect(function(char)
        wait(1)
        local box = Instance.new("BoxHandleAdornment")
        box.Adornee = char:FindFirstChild("HumanoidRootPart")
        box.Size = Vector3.new(2, 5, 2)
        box.Color3 = Color3.new(1, 0, 0)
        box.AlwaysOnTop = true
        box.ZIndex = 10
        box.Transparency = 0.5
        box.Parent = char:FindFirstChild("HumanoidRootPart")
    end)
end

for _, p in pairs(Players:GetPlayers()) do
    criarESP(p)
end

Players.PlayerAdded:Connect(criarESP)print("HEITORZÃO HUB carregado com sucesso!")
StarterGui:SetCore("SendNotification", {
    Title = "✔️ Sucesso",
    Text = "HEITORZÃO HUB foi totalmente carregado!",
    Duration = 4
})
