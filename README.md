# Notification-plus v1:

# preview:

<div align="center">
    <img src="images/Screenshot_20240129-103132.png" alt="Rojo" height="130" />
</div>

# obs: essa notificação fica no meio da tela

# exemplo de notificação com um contador:

```lua
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local notification = Instance.new("ScreenGui")
notification.Name = "notification"
notification.Parent = playerGui

local Background = Instance.new("Frame")
Background.Size = UDim2.new(0, 300, 0, 50)  
Background.Position = UDim2.new(0.5, -150, 0.5, -25) 
Background.BackgroundColor3 = Color3.new(0, 0, 0)
Background.Parent = notification

local countdownText = Instance.new("TextLabel")
countdownText.Text = "Bem vindo! (5)"
countdownText.TextColor3 = Color3.new(1, 1, 1)
countdownText.BackgroundColor3 = Color3.new(0, 0, 0)
countdownText.TextSize = 19
countdownText.Size = UDim2.new(1, 0, 1, 0)
countdownText.Parent = Background

local countdown = 5
local countdownInterval = 1

local function updateCountdown()
    countdown = countdown - 1
    countdownText.Text = "Bem vindo! (" .. countdown .. ")"

    if countdown <= 0 then
        -- código para executar quando atingir (0)
        notification:Destroy()
    else

        wait(countdownInterval)
        updateCountdown()
    end
end

updateCountdown()
```

# n quer o contador na notificação? tente isso:

```lua
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local notification = Instance.new("ScreenGui")
notification.Name = "notification"
notification.Parent = playerGui

local Background = Instance.new("Frame")
Background.Size = UDim2.new(0, 300, 0, 50)  
Background.Position = UDim2.new(0.5, -150, 0.5, -25) 
Background.BackgroundColor3 = Color3.new(0, 0, 0)
Background.Parent = notification

local Text = Instance.new("TextLabel")
Text.Text = "Bem vindo!"
Text.TextColor3 = Color3.new(1, 1, 1)
Text.BackgroundColor3 = Color3.new(0, 0, 0)
Text.TextSize = 19
Text.Size = UDim2.new(1, 0, 1, 0)
Text.Parent = Background
```

# Notification-plus v1.1:

# Novidades:
1- agora vc pode mover a gui para outros lugares da tela

# obs: essa notificação fica no meio da tela

# exemplo de notificação com um contador:

```lua
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local notification = Instance.new("ScreenGui")
notification.Name = "notification"
notification.Parent = playerGui

local Background = Instance.new("Frame")
Background.Size = UDim2.new(0, 300, 0, 50)  
Background.Position = UDim2.new(0.5, -150, 0.5, -25) 
Background.BackgroundColor3 = Color3.new(0, 0, 0)
Background.Active = true
Background.Draggable = true
Background.Parent = notification

local countdownText = Instance.new("TextLabel")
countdownText.Text = "Bem vindo! (5)"
countdownText.TextColor3 = Color3.new(1, 1, 1)
countdownText.BackgroundColor3 = Color3.new(0, 0, 0)
countdownText.TextSize = 19
countdownText.Size = UDim2.new(1, 0, 1, 0)
countdownText.Parent = Background

local countdown = 5
local countdownInterval = 1

local function updateCountdown()
    countdown = countdown - 1
    countdownText.Text = "Bem vindo! (" .. countdown .. ")"

    if countdown <= 0 then
        -- código para executar quando atingir (0)
        notification:Destroy()
    else

        wait(countdownInterval)
        updateCountdown()
    end
end

updateCountdown()
```

# n quer o contador na notificação? tente isso:

```lua
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local notification = Instance.new("ScreenGui")
notification.Name = "notification"
notification.Parent = playerGui

local Background = Instance.new("Frame")
Background.Size = UDim2.new(0, 300, 0, 50)  
Background.Position = UDim2.new(0.5, -150, 0.5, -25) 
Background.BackgroundColor3 = Color3.new(0, 0, 0)
Background.Active = true
Background.Draggable = true
Background.Parent = notification

local Text = Instance.new("TextLabel")
Text.Text = "Bem vindo!"
Text.TextColor3 = Color3.new(1, 1, 1)
Text.BackgroundColor3 = Color3.new(0, 0, 0)
Text.TextSize = 19
Text.Size = UDim2.new(1, 0, 1, 0)
Text.Parent = Background
```

# Notification-plus v1.2:

# Novidades:
1- agora e com imagem a notificação

```lua
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local notification = Instance.new("ScreenGui")
notification.Name = "notification"
notification.Parent = playerGui

local Background = Instance.new("Frame")
Background.Size = UDim2.new(0, 200, 0, 200)  
Background.Position = UDim2.new(0.5, -100, 0.5, -100) 
Background.BackgroundColor3 = Color3.new(0, 0, 0)
Background.Active = true
Background.Draggable = true
BackgroundTransparency = 1 
Background.Parent = notification

local imagem = Instance.new("ImageLabel")
imagem.Parent = frame
imagem.Size = UDim2.new(1, 0, 1, 0) 
imagem.Position = UDim2.new(0, 0, 0, 0) 
imagem.BackgroundTransparency = 1 
imagem.Image = "rbxassetid://" Id image
imagem.Parent = Background
```

# para acontecer algo depois e segundos sem usar um contador, só colocar isso em baixo:
```lua
wait(5) -- em segundos
notification:Destroy()
```

# para ocultar a notificação:
```lua
notification:Destroy()
```

# precisa de ajuda? me chame pv no discord
meu nick: weszin3

## mais atualizações em breve!

