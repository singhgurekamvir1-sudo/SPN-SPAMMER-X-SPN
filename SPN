--[[
    SPN SPAMMER (Cleaned & Updated) - Full Complete Version
    RolePlayName + Bio (Brookhaven) + RGB + Custom Loading + Spams
]]

local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local TextChatService = game:GetService("TextChatService")
local RunService = game:GetService("RunService")
local TweenService = game:GetService("TweenService")

local player = Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")

-- ==================== CONFIG ====================
local RP_NAME = "👑⚔️SPN SPAMMER V1👑⚔️"
local RP_BIO  = "ACCESSING BY  " .. player.Name

local defaultDelay = 0.25

-- ==================== SPN MESSAGES ====================
local head = "__________________________________________________________________________________________________ "
local words = {
	"TMKX МЕН VOID SPELL FUN CUT  VOID FRAUD GODZILLA HYPER GODLY BLANK",
	"TMKX MEH NOVA MASTI FRAUD FUN FACT GODZILLA MAGGI GODZILLA FRAUD DARK POWER",
	"TMKX MEH POWER VOID SPELL HYPER GODLY BEAM JANDU BEAM POWER POWER POWER",
	"TMKX MEH POWER BANK  WAVE OC3 GODZILLA  ML FUN FACT DARK POWER",
	"TMKX MEH PARALLEL MAGIC GODLY BEAM FRAUD DIMENSION WAVE HYPER SPELL SPELL",
	"TMKX MEH PARALLEL POWER WAVE VOID WORM VOID DARK POWER SPELL HYPER",
	"TMKX MEH POWER NOVA VOID WORM OC3 GODLY BEAM GODZILLA GODZILLA VOID WORM GODLY BEAM",
	"TMKX MEH DIMENSION POWER SPELL DIMENSION WAVE WAVE WAVE HYPER POWER",
	"TMKX MEH FUN FACT VOID GODZILLA FUN FACT DIMENSION VOID WORM GODLY BEAM PARALLEL NOVA",
	"SPN SPAMMER AURA",
	"SPN SPAMMER GOD",
	"SPN  NEVER LIES",
	"SPN KINGDOM"
}

local emojis = {
	"🔥", "💀", "⚡", "💎", "😈", "😆", "😔🙏", "😑", "☠️", "🚀"
}

local running = false
local startIndex = 1

-- ==================== ROLEPLAY NAME + BIO (Brookhaven) ====================
task.spawn(function()
	local RE = ReplicatedStorage:WaitForChild("RE", 10)
	if not RE then return end

	local NameRemote = RE:FindFirstChild("1RPNam1eTex1t")
	local ColorRemote = RE:FindFirstChild("1RPNam1eColo1r")

	if NameRemote then
		for i = 1, 8 do
			pcall(function()
				NameRemote:FireServer("RolePlayName", RP_NAME)
				NameRemote:FireServer("RolePlayBio", RP_BIO)
			end)
			task.wait(0.3)
		end
	end

	if ColorRemote then
		while true do
			local c = Color3.fromHSV((tick() % 5) / 5, 1, 1)
			pcall(function()
				ColorRemote:FireServer("PickingRPNameColor", c)
				ColorRemote:FireServer("PickingRPBioColor", c)
			end)
			task.wait(0.08)
		end
	end
end)

-- ==================== INTRO SCREEN ====================
local introGui = Instance.new("ScreenGui")
introGui.Name = "SG_Intro"
introGui.ResetOnSpawn = false
introGui.IgnoreGuiInset = true
introGui.Parent = playerGui

local blackBg = Instance.new("Frame")
blackBg.Size = UDim2.new(1, 0, 1, 0)
blackBg.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
blackBg.BorderSizePixel = 0
blackBg.Parent = introGui

local introText = Instance.new("TextLabel")
introText.Size = UDim2.new(1, 0, 0, 60)
introText.Position = UDim2.new(0, 0, 0.45, 0)
introText.BackgroundTransparency = 1
introText.Text = "SPN SPAMMER ⚡"
introText.TextColor3 = Color3.fromRGB(0, 150, 255)
introText.TextSize = 36
introText.Font = Enum.Font.GothamBold
introText.Parent = blackBg

-- Fade out intro
task.spawn(function()
	task.wait(2.5)
	local tweenInfo = TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
	TweenService:Create(introText, tweenInfo, {TextTransparency = 1}):Play()
	local fadeBg = TweenService:Create(blackBg, tweenInfo, {BackgroundTransparency = 1})
	fadeBg:Play()
	fadeBg.Completed:Connect(function()
		introGui:Destroy()
	end)
end)

-- ==================== MAIN GUI ====================
local gui = Instance.new("ScreenGui")
gui.Name = "SPN_SpammerGui"
gui.ResetOnSpawn = false
gui.Parent = playerGui

local frame = Instance.new("Frame")
frame.Size = UDim2.fromOffset(420, 320)
frame.Position = UDim2.new(0.5, -210, 0.5, -160)
frame.BackgroundColor3 = Color3.fromRGB(15, 20, 35)
frame.BorderSizePixel = 0
frame.Parent = gui

Instance.new("UICorner", frame).CornerRadius = UDim.new(0, 10)

local frameStroke = Instance.new("UIStroke")
frameStroke.Thickness = 2.2
frameStroke.Parent = frame

-- Title
local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, -50, 0, 45)
title.Position = UDim2.fromOffset(15, 0)
title.BackgroundTransparency = 1
title.Text = "👑⚔️ SPN SPAMMER V1 👑⚔️"
title.TextSize = 15
title.Font = Enum.Font.GothamBold
title.TextXAlignment = Enum.TextXAlignment.Left
title.Parent = frame

-- Minimize Button (-)
local minimizeButton = Instance.new("TextButton")
minimizeButton.Size = UDim2.fromOffset(35, 30)
minimizeButton.Position = UDim2.new(1, -40, 0, 8)
minimizeButton.Text = "-"
minimizeButton.TextColor3 = Color3.fromRGB(240, 240, 240)
minimizeButton.TextSize = 22
minimizeButton.Font = Enum.Font.GothamBold
minimizeButton.BackgroundColor3 = Color3.fromRGB(25, 35, 55)
minimizeButton.Parent = frame
Instance.new("UICorner", minimizeButton).CornerRadius = UDim.new(0, 6)

-- Minimized Floating Button
local miniButton = Instance.new("TextButton")
miniButton.Size = UDim2.new(0, 110, 0, 36)
miniButton.Position = UDim2.new(0, 15, 0.5, -18)
miniButton.Text = "SPN PANEL"
miniButton.TextSize = 13
miniButton.Font = Enum.Font.GothamBold
miniButton.BackgroundColor3 = Color3.fromRGB(15, 20, 35)
miniButton.TextColor3 = Color3.fromRGB(255, 255, 255)
miniButton.Visible = false
miniButton.Parent = gui
Instance.new("UICorner", miniButton).CornerRadius = UDim.new(0, 8)

local miniStroke = Instance.new("UIStroke")
miniStroke.Thickness = 2
miniStroke.Parent = miniButton

-- Target Clan / Name
local targetLabel = Instance.new("TextLabel")
targetLabel.Size = UDim2.new(0, 120, 0, 35)
targetLabel.Position = UDim2.fromOffset(25, 60)
targetLabel.BackgroundTransparency = 1
targetLabel.Text = "Target Name:"
targetLabel.TextColor3 = Color3.fromRGB(200, 200, 200)
targetLabel.TextSize = 14
targetLabel.Font = Enum.Font.GothamMedium
targetLabel.TextXAlignment = Enum.TextXAlignment.Left
targetLabel.Parent = frame

local nameBox = Instance.new("TextBox")
nameBox.Size = UDim2.new(0, 220, 0, 38)
nameBox.Position = UDim2.fromOffset(165, 60)
nameBox.PlaceholderText = "Target..."
nameBox.Text = ""
nameBox.TextColor3 = Color3.fromRGB(100, 200, 255)
nameBox.TextSize = 15
nameBox.Font = Enum.Font.GothamBold
nameBox.BackgroundColor3 = Color3.fromRGB(25, 35, 55)
nameBox.ClearTextOnFocus = false
nameBox.Parent = frame
Instance.new("UICorner", nameBox).CornerRadius = UDim.new(0, 8)

-- Delay
local delayLabel = Instance.new("TextLabel")
delayLabel.Size = UDim2.new(0, 120, 0, 35)
delayLabel.Position = UDim2.fromOffset(25, 115)
delayLabel.BackgroundTransparency = 1
delayLabel.Text = "Delay (sec):"
delayLabel.TextColor3 = Color3.fromRGB(200, 200, 200)
delayLabel.TextSize = 14
delayLabel.Font = Enum.Font.GothamMedium
delayLabel.TextXAlignment = Enum.TextXAlignment.Left
delayLabel.Parent = frame

local delayBox = Instance.new("TextBox")
delayBox.Size = UDim2.new(0, 220, 0, 38)
delayBox.Position = UDim2.fromOffset(165, 115)
delayBox.PlaceholderText = "0.25"
delayBox.Text = tostring(defaultDelay)
delayBox.TextColor3 = Color3.fromRGB(100, 200, 255)
delayBox.TextSize = 15
delayBox.Font = Enum.Font.GothamBold
delayBox.BackgroundColor3 = Color3.fromRGB(25, 35, 55)
delayBox.ClearTextOnFocus = false
delayBox.Parent = frame
Instance.new("UICorner", delayBox).CornerRadius = UDim.new(0, 8)

-- Status
local status = Instance.new("TextLabel")
status.Size = UDim2.new(1, 0, 0, 30)
status.Position = UDim2.fromOffset(0, 180)
status.BackgroundTransparency = 1
status.Text = "Status: READY"
status.TextColor3 = Color3.fromRGB(170, 170, 170)
status.TextSize = 13
status.Font = Enum.Font.Gotham
status.Parent = frame

-- Start & Stop Buttons
local startButton = Instance.new("TextButton")
startButton.Size = UDim2.new(0, 175, 0, 40)
startButton.Position = UDim2.fromOffset(25, 230)
startButton.Text = "START"
startButton.TextColor3 = Color3.fromRGB(255, 255, 255)
startButton.TextSize = 15
startButton.Font = Enum.Font.GothamBold
startButton.BackgroundColor3 = Color3.fromRGB(0, 120, 220)
startButton.Parent = frame
Instance.new("UICorner", startButton).CornerRadius = UDim.new(0, 8)

local stopButton = Instance.new("TextButton")
stopButton.Size = UDim2.new(0, 175, 0, 40)
stopButton.Position = UDim2.fromOffset(210, 230)
stopButton.Text = "STOP"
stopButton.TextColor3 = Color3.fromRGB(255, 255, 255)
stopButton.TextSize = 15
stopButton.Font = Enum.Font.GothamBold
stopButton.BackgroundColor3 = Color3.fromRGB(180, 40, 60)
stopButton.Parent = frame
Instance.new("UICorner", stopButton).CornerRadius = UDim.new(0, 8)

-- RGB Animation Loop
RunService.RenderStepped:Connect(function()
	local hue = (tick() * 0.5) % 1
	local rainbow = Color3.fromHSV(hue, 1, 1)
	frameStroke.Color = rainbow
	miniStroke.Color = rainbow
	title.TextColor3 = rainbow
end)

-- Minimize Logic
minimizeButton.MouseButton1Click:Connect(function()
	frame.Visible = false
	miniButton.Visible = true
end)

miniButton.MouseButton1Click:Connect(function()
	miniButton.Visible = false
	frame.Visible = true
end)

nameBox:GetPropertyChangedSignal("Text"):Connect(function()
	local tName = nameBox.Text
	if tName == "" then
		status.Text = "Status: READY"
	else
		status.Text = "Status: READY (Target: " .. tName .. ")"
	end
end)

-- Chat Functions
local function getChannel()
	local channels = TextChatService:FindFirstChild("TextChannels")
	if channels then
		return channels:FindFirstChild("RBXGeneral")
	end
	return nil
end

local function buildMessage(targetName, offset)
	local output = {}
	table.insert(output, head)

	if targetName ~= "" then
		table.insert(output, "[" .. targetName .. "]")
	end

	local position = ((offset - 1) % #words) + 1
	table.insert(output, words[position])

	local randomEmoji = emojis[math.random(1, #emojis)]
	table.insert(output, randomEmoji)

	return table.concat(output, " ")
end

local function sendMessage(text)
	local channel = getChannel()
	if channel then
		pcall(function()
			channel:SendAsync(text)
		end)
	else
		pcall(function()
			local events = ReplicatedStorage:FindFirstChild("DefaultChatSystemChatEvents")
			if events and events:FindFirstChild("SayMessageRequest") then
				events.SayMessageRequest:FireServer(text, "All")
			end
		end)
	end
end

-- Start / Stop Triggers
startButton.MouseButton1Click:Connect(function()
	if running then return end

	local targetName = nameBox.Text
	local customDelay = tonumber(delayBox.Text) or 0.25
	if customDelay < 0.05 then customDelay = 0.25 end

	running = true
	status.Text = "Status: RUNNING" .. (targetName ~= "" and " (Target: " .. targetName .. ")" or "")
	status.TextColor3 = Color3.fromRGB(100, 200, 255)

	task.spawn(function()
		while running do
			local message = buildMessage(targetName, startIndex)
			sendMessage(message)

			startIndex = startIndex + 1
			if startIndex > #words then
				startIndex = 1
			end

			task.wait(customDelay)
		end
	end)
end)

stopButton.MouseButton1Click:Connect(function()
	running = false
	local targetName = nameBox.Text
	status.Text = "Status: STOPPED (Target: " .. (targetName ~= "" and targetName or "NONE") .. ")"
	status.TextColor3 = Color3.fromRGB(255, 100, 100)
end)

print("✅ SPN SPAMMER V1 Fully Loaded Successfully!")
