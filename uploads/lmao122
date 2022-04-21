local Test = {
    Container = {}
    Settings = {
        Enabled = true;
    }
}

local GameLogic;
for I,V in pairs(getgc(true)) do
    if type(V) == "table" then
        if rawget(V, "gammo") then
            GameLogic = V;
        end
    end
end

game:GetService('RunService').RenderStepped:Connect(function()
    if (Test.Settings.Enabled) then
        for i,v in pairs(workspace.Camera[GameLogic.currentgun.name]:GetChildren()) do
            if (v:IsA("MeshPart") or v:IsA("UnionOperation")) then
                v.Material = Enum.Material.ForceField
                v.Color = Color3.fromRGB(169, 132, 255)
            end
        end
    end
end)

return Test;
