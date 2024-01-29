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
    else

        wait(countdownInterval)
        updateCountdown()
    end
end

updateCountdown()
```

# Deseja q a ui seja destruída quando atinge (0)? tente isso:

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
## obs: se vc quiser q a notificação seja destruída só colocar isso em baixo do código:
```lua
wait(5) -- em segundos
notification:Destroy()
```

# em baixo desses códigos de notificação coloque seu script todo

# precisa de ajuda? me chame pv no discord
meu nick: weszin3

meu servidor: https://discord.gg/K82z3EujJn

## mais atualizações em breve!
