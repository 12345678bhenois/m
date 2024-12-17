-- Script Universal para execução de comandos

local Players = game:GetService("Players")

local function executeCommand(player, command)
    local character = player.Character
    if not character then return end
    
    if command == ":fly me" then
        character.HumanoidRootPart.Anchored = true
    elseif command == ":unfly me" then
        character.HumanoidRootPart.Anchored = false
    elseif command == ":fire me" then
        Instance.new("Fire", character.HumanoidRootPart)
    elseif command == ":unfire me" then
        local fire = character.HumanoidRootPart:FindFirstChildOfClass("Fire")
        if fire then fire:Destroy() end
    elseif command == ":smoke me" then
        Instance.new("Smoke", character.HumanoidRootPart)
    elseif command == ":unsmoke me" then
        local smoke = character.HumanoidRootPart:FindFirstChildOfClass("Smoke")
        if smoke then smoke:Destroy() end
    elseif command == ":sparkles me" then
        Instance.new("Sparkles", character.HumanoidRootPart)
    elseif command == ":unsparkles me" then
        local sparkles = character.HumanoidRootPart:FindFirstChildOfClass("Sparkles")
        if sparkles then sparkles:Destroy() end
    elseif command == ":forcefield me" then
        Instance.new("ForceField", character)
    elseif command == ":unff me" then
        local forceField = character:FindFirstChildOfClass("ForceField")
        if forceField then forceField:Destroy() end
    elseif command == ":sit me" then
        character.Humanoid.Sit = true
    elseif command == ":invisible me" then
        for _, part in pairs(character:GetChildren()) do
            if part:IsA("BasePart") then
                part.Transparency = 1
            elseif part:IsA("Decal") then
                part.Transparency = 1
            end
        end
    elseif command == ":visible me
