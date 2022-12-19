# LPAC-Bypass
i joined a gmod server with an anticheat called "LPAC" i don't know what it stands for but i found a bypass really easily. this bypass allows for basically any antiaim or aimbot to bypass the anticheat without silent flagging.

```lua
local function randomStr() 
    local RandomString = ""
    for x=0,25 do
        math.randomseed(CurTime()*math.random(1000,100000))
        RandomString = RandomString .. string.char(math.random(65,122))
    end
    return RandomString
end
hook.Add("CreateMove",randomStr(),function(cmd)
    cmd:SetViewAngles(cmd:GetViewAngles() + Angle(360,360,0))
end)
```
