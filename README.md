for _,v in pairs(game.workspace.Collectibles:GetChildren()) do
	if string.find(v.Name,"") then
		v:Destroy()
	end
end 
noclip = false
game:GetService('RunService').Stepped:connect(function()
	if noclip then
		game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
	end
end)
plr = game.Players.LocalPlayer
mouse = plr:GetMouse()
mouse.KeyDown:connect(function(key)

	if key == "e" then
		noclip = not noclip
		game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
	end
end)
local wp = {
	["Snail Bug"] = CFrame.new(422.218964, 122.764984, -177.787811, -0.0653970614, 5.28176187e-08, -0.997859657, 8.36690006e-08, 1, 4.74474788e-08, 0.997859657, -8.03868971e-08, -0.0653970614),
	["King Bettle Bug"] = CFrame.new(180.669632, 25.9235001, 254.876663, 0.418621242, -3.62905757e-06, -0.908159912, 5.87855766e-07, 1, -3.72507543e-06, 0.908159912, 1.0255269e-06, 0.418621242),
	["Mushroom Field"] = CFrame.new(-89.7000122, 1.95073581, 111.725006, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Strawberry Field"] = CFrame.new(-178.174973, 18.1322384, -9.8549881, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Pumpkin Patch"] = CFrame.new(-188.5, 65.5000153, -183.845093, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Sunflower Field"] = CFrame.new(-208.951294, 1.5, 176.579224, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Blue Flower Field"] = CFrame.new(146.865021, 2.13494039, 100.725006, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Mountain Top Field"] = CFrame.new(77.6849823, 173.500015, -165.431, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Bamboo Field"] = CFrame.new(132.963409, 18.1719551, -25.6000061, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Spider Field"] = CFrame.new(-43.4654312, 18.1220875, -13.5899963, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Pine Tree Forest"] = CFrame.new(-328.670013, 65.5, -187.348999, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Rose Field"] = CFrame.new(-327.459839, 17.5552464, 129.496735, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Cactus Field"] = CFrame.new(-188.5, 65.5000153, -101.595818, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Stump Field"] = CFrame.new(425.05658, 94.4255676, -176.612457, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Clover Field"] = CFrame.new(161.389954, 31.608448, 196.350006, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Coconut Field"] = CFrame.new(-254.478104, 68.9707947, 469.459045, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Pepper Patch"] = CFrame.new(-480.850342, 120.701508, 521.680298, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Pineapple Patch"] = CFrame.new(260.256622, 66.1299973, -207.479324, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Dandelion Field"] = CFrame.new(-30.3512802, 1.42874193, 221.074188, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Beginner shop"] = CFrame.new(88.4201584, 7.64259958, 290.393921, -0.172556818, -9.08730158e-08, -0.984999597, 7.36564658e-08, 1, -1.05160375e-07, 0.984999597, -9.06977107e-08, -0.172556818),
	["Mega Memory"] = CFrame.new(-430, 69.7540512, -57, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Extreme Memory"] = CFrame.new(-400, 130, 546, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Pro Shop"] = CFrame.new(164, 80, -165, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Top Shop"] = CFrame.new(-18, 194, -163, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Night Memory"] = CFrame.new(-17, 320, -270, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Memory"] = CFrame.new(137, 80, -93, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["King Bettle"] = CFrame.new(155, 15, 147, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Onett"] = CFrame.new(-8, 254, -520, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Mother Bear"] = CFrame.new(-184, 10, 90, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Polar Bear"] = CFrame.new(-107, 147, -78, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Brown Bear"] = CFrame.new(280, 69, 240, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Spirit Bear"] = CFrame.new(-363, 100, 476, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Science Bear"] = CFrame.new(268, 118, 22, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Tunel Bear"] = CFrame.new(507.3, 5.7, -45.7),
	["Black Bear"] = CFrame.new(-259, 20, 297, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Diamond Mask"] = CFrame.new(-339, 142, -389, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Gummy Mask"] = CFrame.new(270, 25260, -718, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Demon Mask"] = CFrame.new(300, 45, 272, 1, 0, 0, 0, 1, 0, 0, 0, 1),
	["Panda Bear"] = CFrame.new(104.562164, 35.5114594, 47.1055717, 0.998950779, -1.82728266e-09, -0.0457965843, 2.63707722e-09, 1, 1.76220034e-08, 0.0457965843, -1.77242843e-08, 0.998950779),
	["Stick Bug"] = CFrame.new(-130.038483, 50.7233162, 149.707108, -0.715459228, 4.86261627e-08, -0.698654294, -3.16805959e-08, 1, 1.0204235e-07, 0.698654294, 9.51409262e-08, -0.715459228),
	["Wind Shrine"] = CFrame.new(-481.718811, 140.761505, 411.694946, 0, 1, -0, -1, 0, 0, 0, 0, 1),
	["Honey Bee"] = CFrame.new(-387.468506, 100.4101486, -229.54892, 3.23057175e-05, 0.707060337, -0.707153201, -1, 3.23057175e-05, -1.33812428e-05, 1.33812428e-05, 0.707153201, 0.707060337),
	["Petal Shop"] = CFrame.new(-485.175018, 58.4478493, 511.009979, 1, 0, 0, 0, 1, 0, 0, 0, 1),
}
local red = Color3.fromRGB(255,0,0)
local blue = Color3.fromRGB(0, 206, 206)
local baodz = "Dandelion Field"
local keycheck = "Fasd"
if key == "ezgasd2me" then
	keycheck = true
else
	keycheck = false
end
local LQBHub = Instance.new("ScreenGui")
local open = Instance.new("TextButton")
local mainpage = Instance.new("Frame")
local minimize = Instance.new("TextButton")
local home = Instance.new("Frame")
local waypoint = Instance.new("TextButton")
local autofarm = Instance.new("TextButton")
local extras = Instance.new("TextButton")
local page3 = Instance.new("Frame")
local ScrollingFrame = Instance.new("ScrollingFrame")
local autodig = Instance.new("TextButton")
local equipdemon = Instance.new("TextButton")
local equipgummy = Instance.new("TextButton")
local equipdiamond = Instance.new("TextButton")
local KillTunel = Instance.new("TextButton")
local KillCoconut = Instance.new("TextButton")
local KillKing = Instance.new("TextButton")
local Noclip = Instance.new("TextButton")
local KillSnail = Instance.new("TextButton")
local AutoDispenser = Instance.new("TextButton")
local settings = Instance.new("TextButton")
local page2 = Instance.new("Frame")
local menufield = Instance.new("ScrollingFrame")
local Bamboo = Instance.new("TextButton")
local Dandelion = Instance.new("TextButton")
local Mushroom = Instance.new("TextButton")
local Blueflower = Instance.new("TextButton")
local Sunflower = Instance.new("TextButton")
local Spider = Instance.new("TextButton")
local Clover = Instance.new("TextButton")
local Cactus = Instance.new("TextButton")
local Pineapple = Instance.new("TextButton")
local Stump = Instance.new("TextButton")
local Strawberry = Instance.new("TextButton")
local Pinetree = Instance.new("TextButton")
local Rose = Instance.new("TextButton")
local Pumpkin = Instance.new("TextButton")
local Mountain = Instance.new("TextButton")
local Coconut = Instance.new("TextButton")
local Pepper = Instance.new("TextButton")
local fieldtofarm = Instance.new("TextLabel")
local Autofarmtween = Instance.new("TextButton")
local Type = Instance.new("TextLabel")
local Typeautofarm = Instance.new("TextButton")
local BackgroundType = Instance.new("Frame")
local Tween = Instance.new("TextButton")
local Walking = Instance.new("TextButton")
local Autofarmwalk = Instance.new("TextButton")
local page1 = Instance.new("ScrollingFrame")
local Dandelion_2 = Instance.new("TextButton")
local Mushroom_2 = Instance.new("TextButton")
local Clover_2 = Instance.new("TextButton")
local Sunflower_2 = Instance.new("TextButton")
local Spider_2 = Instance.new("TextButton")
local Blueflower_2 = Instance.new("TextButton")
local Bamboo_2 = Instance.new("TextButton")
local Pinetree_2 = Instance.new("TextButton")
local Strawberry_2 = Instance.new("TextButton")
local Cactus_2 = Instance.new("TextButton")
local Rose_2 = Instance.new("TextButton")
local Pumpkin_2 = Instance.new("TextButton")
local Pepper_2 = Instance.new("TextButton")
local Coconut_2 = Instance.new("TextButton")
local Pineapple_2 = Instance.new("TextButton")
local Stump_2 = Instance.new("TextButton")
local Mountain_2 = Instance.new("TextButton")
local BeginnerShop = Instance.new("TextButton")
local ProShop = Instance.new("TextButton")
local TopShop = Instance.new("TextButton")
local MegaMemory = Instance.new("TextButton")
local Memory = Instance.new("TextButton")
local Night = Instance.new("TextButton")
local ExtremeMemory = Instance.new("TextButton")
local GummyMask = Instance.new("TextButton")
local DiamondMask = Instance.new("TextButton")
local DemonMask = Instance.new("TextButton")
local Onett = Instance.new("TextButton")
local BlackBear = Instance.new("TextButton")
local BrownBear = Instance.new("TextButton")
local KingBettle = Instance.new("TextButton")
local SpiritBear = Instance.new("TextButton")
local ScienceBear = Instance.new("TextButton")
local PolarBear = Instance.new("TextButton")
local PandaBear = Instance.new("TextButton")
local MotherBear = Instance.new("TextButton")
local Stick = Instance.new("TextButton")
local Wind = Instance.new("TextButton")
local Petal = Instance.new("TextButton")
local TunelBear = Instance.new("TextButton")
local HoneyBee = Instance.new("TextButton")
local Nothing = Instance.new("TextButton")
local loadingpage = Instance.new("Frame")
local Discord = Instance.new("TextLabel")
local statuskey = Instance.new("TextLabel")
local TextLabel = Instance.new("TextLabel")
local LQBHub_2 = Instance.new("TextLabel")
local ImageLabel = Instance.new("ImageLabel")

--Properties:

LQBHub.Name = "LQB Hub"
LQBHub.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

open.Name = "open"
open.Parent = LQBHub
open.BackgroundColor3 = Color3.fromRGB(0, 255, 127)
open.Position = UDim2.new(0, 0, 0.50788641, 0)
open.Size = UDim2.new(0, 74, 0, 39)
open.Visible = false
open.Font = Enum.Font.SourceSans
open.Text = "Open"
open.TextColor3 = Color3.fromRGB(0, 0, 0)
open.TextSize = 20.000
open.TextWrapped = true

mainpage.Name = "mainpage"
mainpage.Parent = LQBHub
mainpage.Active = true
mainpage.BackgroundColor3 = Color3.fromRGB(236, 193, 156)
mainpage.BackgroundTransparency = 0.250
mainpage.BorderColor3 = Color3.fromRGB(236, 193, 156)
mainpage.Position = UDim2.new(0.117378056, 0, 0.0463412628, 0)
mainpage.Size = UDim2.new(0, 476, 0, 252)
mainpage.Visible = false

minimize.Name = "minimize"
minimize.Parent = mainpage
minimize.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
minimize.BackgroundTransparency = 1.000
minimize.Position = UDim2.new(0.947698772, 0, 0, 0)
minimize.Size = UDim2.new(0, 24, 0, 30)
minimize.Font = Enum.Font.SourceSans
minimize.Text = "-"
minimize.TextColor3 = Color3.fromRGB(0, 0, 0)
minimize.TextSize = 30.000

home.Name = "home"
home.Parent = mainpage
home.BackgroundColor3 = Color3.fromRGB(30, 132, 127)
home.BackgroundTransparency = 0.250
home.BorderColor3 = Color3.fromRGB(255, 255, 255)
home.BorderSizePixel = 0
home.LayoutOrder = 1
home.Position = UDim2.new(-0.00200000009, 0, 0.119999997, 0)
home.Size = UDim2.new(0, 478, 0, 224)

waypoint.Name = "waypoint"
waypoint.Parent = home
waypoint.BackgroundColor3 = Color3.fromRGB(22, 198, 93)
waypoint.BorderColor3 = Color3.fromRGB(0, 0, 0)
waypoint.Position = UDim2.new(0.00199998682, 0, 0.00200000824, 0)
waypoint.Size = UDim2.new(0, 110, 0, 27)
waypoint.Font = Enum.Font.SourceSans
waypoint.Text = "Waypoint"
waypoint.TextColor3 = Color3.fromRGB(0, 0, 0)
waypoint.TextSize = 14.000

autofarm.Name = "autofarm"
autofarm.Parent = home
autofarm.BackgroundColor3 = Color3.fromRGB(22, 198, 93)
autofarm.BorderColor3 = Color3.fromRGB(0, 0, 0)
autofarm.Position = UDim2.new(0.23448953, 0, 0.00200000824, 0)
autofarm.Size = UDim2.new(0, 110, 0, 27)
autofarm.Font = Enum.Font.SourceSans
autofarm.Text = "Auto Farm"
autofarm.TextColor3 = Color3.fromRGB(0, 0, 0)
autofarm.TextSize = 15.000

extras.Name = "extras"
extras.Parent = home
extras.BackgroundColor3 = Color3.fromRGB(22, 198, 93)
extras.BorderColor3 = Color3.fromRGB(0, 0, 0)
extras.Position = UDim2.new(0.464979112, 0, 0.00199999125, 0)
extras.Size = UDim2.new(0, 130, 0, 27)
extras.Font = Enum.Font.SourceSans
extras.Text = "Extras"
extras.TextColor3 = Color3.fromRGB(0, 0, 0)
extras.TextSize = 14.000

page3.Name = "page3"
page3.Parent = home
page3.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
page3.BorderColor3 = Color3.fromRGB(0, 0, 0)
page3.Position = UDim2.new(0.00199998682, 0, 0.122535706, 0)
page3.Size = UDim2.new(0, 475, 0, 229)
page3.Visible = false

ScrollingFrame.Parent = page3
ScrollingFrame.Active = true
ScrollingFrame.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
ScrollingFrame.BackgroundTransparency = 1.000
ScrollingFrame.Position = UDim2.new(-0.00199999125, 0, 0.0203913152, 0)
ScrollingFrame.Size = UDim2.new(0, 476, 0, 225)

autodig.Name = "autodig"
autodig.Parent = ScrollingFrame
autodig.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
autodig.Position = UDim2.new(0.0219999999, 0, 0.0219999999, 0)
autodig.Size = UDim2.new(0, 145, 0, 35)
autodig.Font = Enum.Font.SourceSans
autodig.Text = "Auto Dig"
autodig.TextColor3 = Color3.fromRGB(0, 0, 0)
autodig.TextSize = 14.000

equipdemon.Name = "equipdemon"
equipdemon.Parent = ScrollingFrame
equipdemon.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
equipdemon.Position = UDim2.new(0.325630248, 0, 0.0203300156, 0)
equipdemon.Size = UDim2.new(0, 136, 0, 35)
equipdemon.Font = Enum.Font.SourceSans
equipdemon.Text = "Equip Demon Mask"
equipdemon.TextColor3 = Color3.fromRGB(0, 0, 0)
equipdemon.TextSize = 14.000

equipgummy.Name = "equipgummy"
equipgummy.Parent = ScrollingFrame
equipgummy.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
equipgummy.Position = UDim2.new(0.610243678, 0, 0.0202933364, 0)
equipgummy.Size = UDim2.new(0, 125, 0, 35)
equipgummy.Font = Enum.Font.SourceSans
equipgummy.Text = "Equip Gummy Mask"
equipgummy.TextColor3 = Color3.fromRGB(0, 0, 0)
equipgummy.TextSize = 14.000

equipdiamond.Name = "equipdiamond"
equipdiamond.Parent = ScrollingFrame
equipdiamond.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
equipdiamond.Position = UDim2.new(0.0219075829, 0, 0.0991254076, 0)
equipdiamond.Size = UDim2.new(0, 144, 0, 35)
equipdiamond.Font = Enum.Font.SourceSans
equipdiamond.Text = "Equip Diamond Mask"
equipdiamond.TextColor3 = Color3.fromRGB(0, 0, 0)
equipdiamond.TextSize = 14.000

KillTunel.Name = "Kill Tunel"
KillTunel.Parent = ScrollingFrame
KillTunel.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
KillTunel.Position = UDim2.new(0.324999988, 0, 0.100000001, 0)
KillTunel.Size = UDim2.new(0, 136, 0, 35)
KillTunel.Font = Enum.Font.SourceSans
KillTunel.Text = "Kill Tunel Bear"
KillTunel.TextColor3 = Color3.fromRGB(0, 0, 0)
KillTunel.TextSize = 14.000

KillCoconut.Name = "Kill Coconut"
KillCoconut.Parent = ScrollingFrame
KillCoconut.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
KillCoconut.Position = UDim2.new(0.610243738, 0, 0.10029038, 0)
KillCoconut.Size = UDim2.new(0, 125, 0, 35)
KillCoconut.Font = Enum.Font.SourceSans
KillCoconut.Text = "Kill Coconut Crab"
KillCoconut.TextColor3 = Color3.fromRGB(0, 0, 0)
KillCoconut.TextSize = 14.000

KillKing.Name = "Kill King"
KillKing.Parent = ScrollingFrame
KillKing.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
KillKing.Position = UDim2.new(0.021663826, 0, 0.173111796, 2)
KillKing.Size = UDim2.new(0, 144, 0, 35)
KillKing.Font = Enum.Font.SourceSans
KillKing.Text = "Kill King Bettle"
KillKing.TextColor3 = Color3.fromRGB(0, 0, 0)
KillKing.TextSize = 14.000

Noclip.Name = "Noclip"
Noclip.Parent = ScrollingFrame
Noclip.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
Noclip.Position = UDim2.new(0.324999988, 0, 0.178000003, 0)
Noclip.Size = UDim2.new(0, 135, 0, 35)
Noclip.Font = Enum.Font.SourceSans
Noclip.Text = "Noclip"
Noclip.TextColor3 = Color3.fromRGB(0, 0, 0)
Noclip.TextSize = 14.000

KillSnail.Name = "Kill Snail"
KillSnail.Parent = ScrollingFrame
KillSnail.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
KillSnail.Position = UDim2.new(0.610000014, 0, 0.179000005, 0)
KillSnail.Size = UDim2.new(0, 125, 0, 35)
KillSnail.Font = Enum.Font.SourceSans
KillSnail.Text = "Kill Snail"
KillSnail.TextColor3 = Color3.fromRGB(0, 0, 0)
KillSnail.TextSize = 14.000

AutoDispenser.Name = "Auto Dispenser"
AutoDispenser.Parent = ScrollingFrame
AutoDispenser.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
AutoDispenser.Position = UDim2.new(0.0219999999, 0, 0.252999991, 2)
AutoDispenser.Size = UDim2.new(0, 144, 0, 35)
AutoDispenser.Font = Enum.Font.SourceSans
AutoDispenser.Text = "Auto Dispenser"
AutoDispenser.TextColor3 = Color3.fromRGB(0, 0, 0)
AutoDispenser.TextSize = 14.000

settings.Name = "settings"
settings.Parent = home
settings.BackgroundColor3 = Color3.fromRGB(22, 198, 93)
settings.BorderColor3 = Color3.fromRGB(0, 0, 0)
settings.Position = UDim2.new(0.735146523, 0, 0.00200000824, 0)
settings.Size = UDim2.new(0, 125, 0, 26)
settings.Font = Enum.Font.SourceSans
settings.Text = "Settings"
settings.TextColor3 = Color3.fromRGB(0, 0, 0)
settings.TextSize = 14.000

page2.Name = "page2"
page2.Parent = home
page2.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
page2.BorderColor3 = Color3.fromRGB(0, 0, 0)
page2.Position = UDim2.new(0.00199998682, 0, 0.122535706, 0)
page2.Size = UDim2.new(0, 475, 0, 201)
page2.Visible = false

menufield.Name = "menufield"
menufield.Parent = page2
menufield.Active = true
menufield.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
menufield.Size = UDim2.new(0, 222, 0, 199)

Bamboo.Name = "Bamboo"
Bamboo.Parent = menufield
Bamboo.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Bamboo.BorderColor3 = Color3.fromRGB(27, 42, 53)
Bamboo.Position = UDim2.new(-0.0019999966, 0, 0.284649193, 0)
Bamboo.Size = UDim2.new(0, 210, 0, 23)
Bamboo.Font = Enum.Font.SourceSans
Bamboo.Text = "Bamboo Field"
Bamboo.TextColor3 = Color3.fromRGB(0, 0, 0)
Bamboo.TextSize = 14.000

Dandelion.Name = "Dandelion"
Dandelion.Parent = menufield
Dandelion.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Dandelion.Position = UDim2.new(-0.00199999986, 0, -0.00127638876, 0)
Dandelion.Size = UDim2.new(0, 210, 0, 23)
Dandelion.Font = Enum.Font.SourceSans
Dandelion.Text = "Dandelion Field"
Dandelion.TextColor3 = Color3.fromRGB(0, 0, 0)
Dandelion.TextSize = 14.000

Mushroom.Name = "Mushroom"
Mushroom.Parent = menufield
Mushroom.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Mushroom.Position = UDim2.new(-0.00200000009, 0, 0.0552512631, 0)
Mushroom.Size = UDim2.new(0, 210, 0, 23)
Mushroom.Font = Enum.Font.SourceSans
Mushroom.Text = "Mushroom Field"
Mushroom.TextColor3 = Color3.fromRGB(0, 0, 0)
Mushroom.TextSize = 14.000

Blueflower.Name = "Blueflower"
Blueflower.Parent = menufield
Blueflower.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Blueflower.Position = UDim2.new(-0.00200000033, 0, 0.11205025, 0)
Blueflower.Size = UDim2.new(0, 210, 0, 23)
Blueflower.Font = Enum.Font.SourceSans
Blueflower.Text = "Blue Flower Field"
Blueflower.TextColor3 = Color3.fromRGB(0, 0, 0)
Blueflower.TextSize = 14.000

Sunflower.Name = "Sunflower"
Sunflower.Parent = menufield
Sunflower.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Sunflower.BorderColor3 = Color3.fromRGB(27, 42, 53)
Sunflower.Position = UDim2.new(-0.00210526958, 0, 0.171306357, 0)
Sunflower.Size = UDim2.new(0, 210, 0, 23)
Sunflower.Font = Enum.Font.SourceSans
Sunflower.Text = "Sunflower Field"
Sunflower.TextColor3 = Color3.fromRGB(0, 0, 0)
Sunflower.TextSize = 14.000

Spider.Name = "Spider"
Spider.Parent = menufield
Spider.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Spider.Position = UDim2.new(-0.00200000009, 0, 0.228794008, 0)
Spider.Size = UDim2.new(0, 210, 0, 23)
Spider.Font = Enum.Font.SourceSans
Spider.Text = "Spider Field"
Spider.TextColor3 = Color3.fromRGB(0, 0, 0)
Spider.TextSize = 14.000

Clover.Name = "Clover"
Clover.Parent = menufield
Clover.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Clover.Position = UDim2.new(-0.00199999986, 0, 0.341020107, 0)
Clover.Size = UDim2.new(0, 210, 0, 23)
Clover.Font = Enum.Font.SourceSans
Clover.Text = "Clover Field"
Clover.TextColor3 = Color3.fromRGB(0, 0, 0)
Clover.TextSize = 14.000

Cactus.Name = "Cactus"
Cactus.Parent = menufield
Cactus.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Cactus.Position = UDim2.new(-0.00199999986, 0, 0.398809016, 0)
Cactus.Size = UDim2.new(0, 210, 0, 23)
Cactus.Font = Enum.Font.SourceSans
Cactus.Text = "Cactus Field"
Cactus.TextColor3 = Color3.fromRGB(0, 0, 0)
Cactus.TextSize = 14.000

Pineapple.Name = "Pineapple"
Pineapple.Parent = menufield
Pineapple.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Pineapple.Position = UDim2.new(-8.47550109e-06, 0, 0.455711424, 0)
Pineapple.Size = UDim2.new(0, 210, 0, 23)
Pineapple.Font = Enum.Font.SourceSans
Pineapple.Text = "Pineapple Patch"
Pineapple.TextColor3 = Color3.fromRGB(0, 0, 0)
Pineapple.TextSize = 14.000

Stump.Name = "Stump"
Stump.Parent = menufield
Stump.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Stump.Position = UDim2.new(-0.00199999986, 0, 0.514386952, 0)
Stump.Size = UDim2.new(0, 210, 0, 23)
Stump.Font = Enum.Font.SourceSans
Stump.Text = "Stump Field"
Stump.TextColor3 = Color3.fromRGB(0, 0, 0)
Stump.TextSize = 14.000

Strawberry.Name = "Strawberry"
Strawberry.Parent = menufield
Strawberry.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Strawberry.Position = UDim2.new(-0.00199999986, 0, 0.572075367, 0)
Strawberry.Size = UDim2.new(0, 210, 0, 23)
Strawberry.Font = Enum.Font.SourceSans
Strawberry.Text = "Strawberry Field"
Strawberry.TextColor3 = Color3.fromRGB(0, 0, 0)
Strawberry.TextSize = 14.000

Pinetree.Name = "Pinetree"
Pinetree.Parent = menufield
Pinetree.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Pinetree.Position = UDim2.new(-0.00199999986, 0, 0.629864275, 0)
Pinetree.Size = UDim2.new(0, 210, 0, 23)
Pinetree.Font = Enum.Font.SourceSans
Pinetree.Text = "Pine Tree Forest"
Pinetree.TextColor3 = Color3.fromRGB(0, 0, 0)
Pinetree.TextSize = 14.000

Rose.Name = "Rose"
Rose.Parent = menufield
Rose.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Rose.Position = UDim2.new(-0.00200000009, 0, 0.687150776, 0)
Rose.Size = UDim2.new(0, 210, 0, 23)
Rose.Font = Enum.Font.SourceSans
Rose.Text = "Rose Field"
Rose.TextColor3 = Color3.fromRGB(0, 0, 0)
Rose.TextSize = 14.000

Pumpkin.Name = "Pumpkin"
Pumpkin.Parent = menufield
Pumpkin.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Pumpkin.Position = UDim2.new(-0.00200000009, 0, 0.745000005, 0)
Pumpkin.Size = UDim2.new(0, 210, 0, 23)
Pumpkin.Font = Enum.Font.SourceSans
Pumpkin.Text = "Pumpkin Patch"
Pumpkin.TextColor3 = Color3.fromRGB(0, 0, 0)
Pumpkin.TextSize = 14.000

Mountain.Name = "Mountain"
Mountain.Parent = menufield
Mountain.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Mountain.Position = UDim2.new(-0.00200000009, 0, 0.802728593, 0)
Mountain.Size = UDim2.new(0, 210, 0, 23)
Mountain.Font = Enum.Font.SourceSans
Mountain.Text = "Mountain Top Field"
Mountain.TextColor3 = Color3.fromRGB(0, 0, 0)
Mountain.TextSize = 14.000

Coconut.Name = "Coconut"
Coconut.Parent = menufield
Coconut.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Coconut.Position = UDim2.new(-0.00228018407, 0, 0.858005047, 0)
Coconut.Size = UDim2.new(0, 210, 0, 23)
Coconut.Font = Enum.Font.SourceSans
Coconut.Text = "Coconut Field"
Coconut.TextColor3 = Color3.fromRGB(0, 0, 0)
Coconut.TextSize = 14.000

Pepper.Name = "Pepper"
Pepper.Parent = menufield
Pepper.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Pepper.Position = UDim2.new(-0.00123530626, 0, 0.914646029, 0)
Pepper.Size = UDim2.new(0, 210, 0, 23)
Pepper.Font = Enum.Font.SourceSans
Pepper.Text = "Pepper Patch"
Pepper.TextColor3 = Color3.fromRGB(0, 0, 0)
Pepper.TextSize = 14.000

fieldtofarm.Name = "fieldtofarm"
fieldtofarm.Parent = page2
fieldtofarm.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
fieldtofarm.BackgroundTransparency = 1.000
fieldtofarm.Position = UDim2.new(0.554475963, 0, 0.100302488, 0)
fieldtofarm.Size = UDim2.new(0, 179, 0, 41)
fieldtofarm.Font = Enum.Font.SourceSans
fieldtofarm.Text = "Location"
fieldtofarm.TextColor3 = Color3.fromRGB(0, 0, 0)
fieldtofarm.TextSize = 15.000

Autofarmtween.Name = "Autofarmtween"
Autofarmtween.Parent = page2
Autofarmtween.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
Autofarmtween.Position = UDim2.new(0.514705837, 0, 0.306532651, 0)
Autofarmtween.Size = UDim2.new(0, 217, 0, 23)
Autofarmtween.Font = Enum.Font.SourceSans
Autofarmtween.Text = "Start Auto Farm"
Autofarmtween.TextColor3 = Color3.fromRGB(0, 0, 0)
Autofarmtween.TextSize = 15.000

Type.Name = "Type"
Type.Parent = page2
Type.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Type.BackgroundTransparency = 1.000
Type.Position = UDim2.new(0.46443519, 0, 0.571428597, 0)
Type.Size = UDim2.new(0, 129, 0, 22)
Type.Font = Enum.Font.SourceSans
Type.Text = "Type Auto Farm:"
Type.TextColor3 = Color3.fromRGB(0, 0, 0)
Type.TextSize = 14.000

Typeautofarm.Name = "Typeautofarm"
Typeautofarm.Parent = page2
Typeautofarm.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
Typeautofarm.Position = UDim2.new(0.696842134, 0, 0.572139323, 0)
Typeautofarm.Size = UDim2.new(0, 111, 0, 22)
Typeautofarm.Font = Enum.Font.SourceSans
Typeautofarm.Text = "Tween"
Typeautofarm.TextColor3 = Color3.fromRGB(0, 0, 0)
Typeautofarm.TextSize = 14.000

BackgroundType.Name = "BackgroundType"
BackgroundType.Parent = page2
BackgroundType.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
BackgroundType.Position = UDim2.new(0.696679175, 0, 0.737118006, 0)
BackgroundType.Size = UDim2.new(0, 110, 0, 48)
BackgroundType.Visible = false

Tween.Name = "Tween"
Tween.Parent = BackgroundType
Tween.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
Tween.Position = UDim2.new(0, 0, -1.49011612e-08, 0)
Tween.Size = UDim2.new(0, 110, 0, 22)
Tween.Font = Enum.Font.SourceSans
Tween.Text = "Tween"
Tween.TextColor3 = Color3.fromRGB(0, 0, 0)
Tween.TextSize = 14.000

Walking.Name = "Walking"
Walking.Parent = BackgroundType
Walking.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
Walking.BackgroundTransparency = 1.000
Walking.Position = UDim2.new(0, 0, 0.49999994, 0)
Walking.Size = UDim2.new(0, 110, 0, 22)
Walking.Font = Enum.Font.SourceSans
Walking.Text = "Walking"
Walking.TextColor3 = Color3.fromRGB(0, 0, 0)
Walking.TextSize = 14.000

Autofarmwalk.Name = "Autofarmwalk"
Autofarmwalk.Parent = page2
Autofarmwalk.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
Autofarmwalk.Position = UDim2.new(0.514705837, 0, 0.306532651, 0)
Autofarmwalk.Size = UDim2.new(0, 217, 0, 23)
Autofarmwalk.Visible = false
Autofarmwalk.Font = Enum.Font.SourceSans
Autofarmwalk.Text = "Start Auto Farm"
Autofarmwalk.TextColor3 = Color3.fromRGB(0, 0, 0)
Autofarmwalk.TextSize = 15.000

page1.Name = "page1"
page1.Parent = home
page1.Active = true
page1.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
page1.BorderColor3 = Color3.fromRGB(0, 0, 0)
page1.Position = UDim2.new(0.00199998682, 0, 0.122535706, 0)
page1.Size = UDim2.new(0, 475, 0, 198)
page1.ScrollBarThickness = 3

Dandelion_2.Name = "Dandelion"
Dandelion_2.Parent = page1
Dandelion_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Dandelion_2.Position = UDim2.new(-0.00210526306, 0, -0.000624757027, 0)
Dandelion_2.Size = UDim2.new(0, 161, 0, 32)
Dandelion_2.Font = Enum.Font.SourceSans
Dandelion_2.Text = "Dandelion Field"
Dandelion_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Dandelion_2.TextSize = 14.000

Mushroom_2.Name = "Mushroom"
Mushroom_2.Parent = page1
Mushroom_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Mushroom_2.Position = UDim2.new(0.671578944, 0, -0.00278788875, 0)
Mushroom_2.Size = UDim2.new(0, 161, 0, 32)
Mushroom_2.Font = Enum.Font.SourceSans
Mushroom_2.Text = "Mushroom Field"
Mushroom_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Mushroom_2.TextSize = 14.000

Clover_2.Name = "Clover"
Clover_2.Parent = page1
Clover_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Clover_2.Position = UDim2.new(0.33684209, 0, -0.00062475726, 0)
Clover_2.Size = UDim2.new(0, 161, 0, 32)
Clover_2.Font = Enum.Font.SourceSans
Clover_2.Text = "Clover Field"
Clover_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Clover_2.TextSize = 14.000

Sunflower_2.Name = "Sunflower"
Sunflower_2.Parent = page1
Sunflower_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Sunflower_2.Position = UDim2.new(-0.00210526306, 0, 0.0708038211, 0)
Sunflower_2.Size = UDim2.new(0, 161, 0, 32)
Sunflower_2.Font = Enum.Font.SourceSans
Sunflower_2.Text = "Sunflower Field"
Sunflower_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Sunflower_2.TextSize = 14.000

Spider_2.Name = "Spider"
Spider_2.Parent = page1
Spider_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Spider_2.Position = UDim2.new(0.671578944, 0, 0.0708038211, 0)
Spider_2.Size = UDim2.new(0, 161, 0, 32)
Spider_2.Font = Enum.Font.SourceSans
Spider_2.Text = "Spider Field"
Spider_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Spider_2.TextSize = 14.000

Blueflower_2.Name = "Blueflower"
Blueflower_2.Parent = page1
Blueflower_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Blueflower_2.Position = UDim2.new(0.33684209, 0, 0.0708038211, 0)
Blueflower_2.Size = UDim2.new(0, 161, 0, 32)
Blueflower_2.Font = Enum.Font.SourceSans
Blueflower_2.Text = "Blue Flower Field"
Blueflower_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Blueflower_2.TextSize = 14.000

Bamboo_2.Name = "Bamboo"
Bamboo_2.Parent = page1
Bamboo_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Bamboo_2.Position = UDim2.new(-0.00200000009, 0, 0.142000005, 0)
Bamboo_2.Size = UDim2.new(0, 161, 0, 32)
Bamboo_2.Font = Enum.Font.SourceSans
Bamboo_2.Text = "Bamboo Field"
Bamboo_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Bamboo_2.TextSize = 14.000

Pinetree_2.Name = "Pinetree"
Pinetree_2.Parent = page1
Pinetree_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Pinetree_2.Position = UDim2.new(0.671999991, 0, 0.142000005, 0)
Pinetree_2.Size = UDim2.new(0, 161, 0, 32)
Pinetree_2.Font = Enum.Font.SourceSans
Pinetree_2.Text = "Pine Tree Forest"
Pinetree_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Pinetree_2.TextSize = 14.000

Strawberry_2.Name = "Strawberry"
Strawberry_2.Parent = page1
Strawberry_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Strawberry_2.Position = UDim2.new(0.337000012, 0, 0.142000005, 0)
Strawberry_2.Size = UDim2.new(0, 161, 0, 32)
Strawberry_2.Font = Enum.Font.SourceSans
Strawberry_2.Text = "Strawberry Field"
Strawberry_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Strawberry_2.TextSize = 14.000

Cactus_2.Name = "Cactus"
Cactus_2.Parent = page1
Cactus_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Cactus_2.Position = UDim2.new(-0.00200000009, 0, 0.214000002, 0)
Cactus_2.Size = UDim2.new(0, 161, 0, 32)
Cactus_2.Font = Enum.Font.SourceSans
Cactus_2.Text = "Cactus Field"
Cactus_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Cactus_2.TextSize = 14.000

Rose_2.Name = "Rose"
Rose_2.Parent = page1
Rose_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Rose_2.Position = UDim2.new(0.671999991, 0, 0.214000002, 0)
Rose_2.Size = UDim2.new(0, 161, 0, 32)
Rose_2.Font = Enum.Font.SourceSans
Rose_2.Text = "Rose Field"
Rose_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Rose_2.TextSize = 14.000

Pumpkin_2.Name = "Pumpkin"
Pumpkin_2.Parent = page1
Pumpkin_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Pumpkin_2.Position = UDim2.new(0.337000012, 0, 0.214000002, 0)
Pumpkin_2.Size = UDim2.new(0, 161, 0, 32)
Pumpkin_2.Font = Enum.Font.SourceSans
Pumpkin_2.Text = "Pumpkin Patch"
Pumpkin_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Pumpkin_2.TextSize = 14.000

Pepper_2.Name = "Pepper"
Pepper_2.Parent = page1
Pepper_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Pepper_2.Position = UDim2.new(0.337000012, 0, 0.356857151, 0)
Pepper_2.Size = UDim2.new(0, 161, 0, 32)
Pepper_2.Font = Enum.Font.SourceSans
Pepper_2.Text = "Pepper Patch"
Pepper_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Pepper_2.TextSize = 14.000

Coconut_2.Name = "Coconut"
Coconut_2.Parent = page1
Coconut_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Coconut_2.Position = UDim2.new(-0.041999992, 0, 0.355692297, 0)
Coconut_2.Size = UDim2.new(0, 179, 0, 32)
Coconut_2.Font = Enum.Font.SourceSans
Coconut_2.Text = "      Coconut Field"
Coconut_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Coconut_2.TextSize = 14.000

Pineapple_2.Name = "Pineapple"
Pineapple_2.Parent = page1
Pineapple_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Pineapple_2.Position = UDim2.new(-0.00200000009, 0, 0.284857154, 0)
Pineapple_2.Size = UDim2.new(0, 161, 0, 32)
Pineapple_2.Font = Enum.Font.SourceSans
Pineapple_2.Text = "Pineapple Patch"
Pineapple_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Pineapple_2.TextSize = 14.000

Stump_2.Name = "Stump"
Stump_2.Parent = page1
Stump_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Stump_2.Position = UDim2.new(0.337000012, 0, 0.284857154, 0)
Stump_2.Size = UDim2.new(0, 161, 0, 32)
Stump_2.Font = Enum.Font.SourceSans
Stump_2.Text = "Stump Field"
Stump_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Stump_2.TextSize = 14.000

Mountain_2.Name = "Mountain"
Mountain_2.Parent = page1
Mountain_2.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Mountain_2.Position = UDim2.new(0.678052545, 0, 0.284253299, 0)
Mountain_2.Size = UDim2.new(0, 153, 0, 32)
Mountain_2.Font = Enum.Font.SourceSans
Mountain_2.Text = "Mountain Top Field"
Mountain_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Mountain_2.TextSize = 14.000

BeginnerShop.Name = "Beginner Shop"
BeginnerShop.Parent = page1
BeginnerShop.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
BeginnerShop.Position = UDim2.new(0.677999973, 0, 0.35800001, 0)
BeginnerShop.Size = UDim2.new(0, 161, 0, 31)
BeginnerShop.Font = Enum.Font.SourceSans
BeginnerShop.Text = "Beginner Shop"
BeginnerShop.TextColor3 = Color3.fromRGB(0, 0, 0)
BeginnerShop.TextSize = 14.000

ProShop.Name = "Pro Shop"
ProShop.Parent = page1
ProShop.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
ProShop.Position = UDim2.new(-0.00410529692, 0, 0.429428577, 0)
ProShop.Size = UDim2.new(0, 161, 0, 31)
ProShop.Font = Enum.Font.SourceSans
ProShop.Text = "Pro Shop"
ProShop.TextColor3 = Color3.fromRGB(0, 0, 0)
ProShop.TextSize = 14.000

TopShop.Name = "Top Shop"
TopShop.Parent = page1
TopShop.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
TopShop.Position = UDim2.new(0.336947322, 0, 0.429428577, 0)
TopShop.Size = UDim2.new(0, 161, 0, 31)
TopShop.Font = Enum.Font.SourceSans
TopShop.Text = "Top Shop"
TopShop.TextColor3 = Color3.fromRGB(0, 0, 0)
TopShop.TextSize = 14.000

MegaMemory.Name = "Mega Memory"
MegaMemory.Parent = page1
MegaMemory.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
MegaMemory.Position = UDim2.new(0.677999973, 0, 0.429428577, 0)
MegaMemory.Size = UDim2.new(0, 161, 0, 31)
MegaMemory.Font = Enum.Font.SourceSans
MegaMemory.Text = "Mega Memory"
MegaMemory.TextColor3 = Color3.fromRGB(0, 0, 0)
MegaMemory.TextSize = 14.000

Memory.Name = "Memory"
Memory.Parent = page1
Memory.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Memory.Position = UDim2.new(0.336947322, 0, 0.49862501, 0)
Memory.Size = UDim2.new(0, 161, 0, 31)
Memory.Font = Enum.Font.SourceSans
Memory.Text = "Memory"
Memory.TextColor3 = Color3.fromRGB(0, 0, 0)
Memory.TextSize = 14.000

Night.Name = "Night"
Night.Parent = page1
Night.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Night.Position = UDim2.new(0.677999914, 0, 0.49862501, 0)
Night.Size = UDim2.new(0, 161, 0, 31)
Night.Font = Enum.Font.SourceSans
Night.Text = "Night Memory"
Night.TextColor3 = Color3.fromRGB(0, 0, 0)
Night.TextSize = 14.000

ExtremeMemory.Name = "Extreme Memory"
ExtremeMemory.Parent = page1
ExtremeMemory.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
ExtremeMemory.Position = UDim2.new(-0.00410529692, 0, 0.49862501, 0)
ExtremeMemory.Size = UDim2.new(0, 161, 0, 31)
ExtremeMemory.Font = Enum.Font.SourceSans
ExtremeMemory.Text = "Extreme Memory"
ExtremeMemory.TextColor3 = Color3.fromRGB(0, 0, 0)
ExtremeMemory.TextSize = 14.000

GummyMask.Name = "Gummy Mask"
GummyMask.Parent = page1
GummyMask.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
GummyMask.Position = UDim2.new(0.677999973, 0, 0.567821443, 0)
GummyMask.Size = UDim2.new(0, 161, 0, 31)
GummyMask.Font = Enum.Font.SourceSans
GummyMask.Text = "Gummy Mask"
GummyMask.TextColor3 = Color3.fromRGB(0, 0, 0)
GummyMask.TextSize = 14.000

DiamondMask.Name = "Diamond Mask"
DiamondMask.Parent = page1
DiamondMask.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
DiamondMask.Position = UDim2.new(0.336947322, 0, 0.567821443, 0)
DiamondMask.Size = UDim2.new(0, 161, 0, 31)
DiamondMask.Font = Enum.Font.SourceSans
DiamondMask.Text = "Diamond Mask"
DiamondMask.TextColor3 = Color3.fromRGB(0, 0, 0)
DiamondMask.TextSize = 14.000

DemonMask.Name = "Demon Mask"
DemonMask.Parent = page1
DemonMask.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
DemonMask.Position = UDim2.new(-0.00410529692, 0, 0.567821443, 0)
DemonMask.Size = UDim2.new(0, 161, 0, 31)
DemonMask.Font = Enum.Font.SourceSans
DemonMask.Text = "Demon Mask"
DemonMask.TextColor3 = Color3.fromRGB(0, 0, 0)
DemonMask.TextSize = 14.000

Onett.Name = "Onett"
Onett.Parent = page1
Onett.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Onett.Position = UDim2.new(-0.00410529692, 0, 0.637017846, 0)
Onett.Size = UDim2.new(0, 161, 0, 31)
Onett.Font = Enum.Font.SourceSans
Onett.Text = "Onett"
Onett.TextColor3 = Color3.fromRGB(0, 0, 0)
Onett.TextSize = 14.000

BlackBear.Name = "Black Bear"
BlackBear.Parent = page1
BlackBear.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
BlackBear.Position = UDim2.new(0.336947322, 0, 0.637017846, 0)
BlackBear.Size = UDim2.new(0, 161, 0, 31)
BlackBear.Font = Enum.Font.SourceSans
BlackBear.Text = "Black Bear"
BlackBear.TextColor3 = Color3.fromRGB(0, 0, 0)
BlackBear.TextSize = 14.000

BrownBear.Name = "Brown Bear"
BrownBear.Parent = page1
BrownBear.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
BrownBear.Position = UDim2.new(0.677999914, 0, 0.637017846, 0)
BrownBear.Size = UDim2.new(0, 161, 0, 31)
BrownBear.Font = Enum.Font.SourceSans
BrownBear.Text = "Brown Bear"
BrownBear.TextColor3 = Color3.fromRGB(0, 0, 0)
BrownBear.TextSize = 14.000

KingBettle.Name = "King Bettle"
KingBettle.Parent = page1
KingBettle.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
KingBettle.Position = UDim2.new(0.677999914, 0, 0.777642846, 0)
KingBettle.Size = UDim2.new(0, 161, 0, 31)
KingBettle.Font = Enum.Font.SourceSans
KingBettle.Text = "King Bettle"
KingBettle.TextColor3 = Color3.fromRGB(0, 0, 0)
KingBettle.TextSize = 14.000

SpiritBear.Name = "Spirit Bear"
SpiritBear.Parent = page1
SpiritBear.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
SpiritBear.Position = UDim2.new(0.336947322, 0, 0.777642846, 0)
SpiritBear.Size = UDim2.new(0, 161, 0, 31)
SpiritBear.Font = Enum.Font.SourceSans
SpiritBear.Text = "Spirit Bear"
SpiritBear.TextColor3 = Color3.fromRGB(0, 0, 0)
SpiritBear.TextSize = 14.000

ScienceBear.Name = "Science Bear"
ScienceBear.Parent = page1
ScienceBear.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
ScienceBear.Position = UDim2.new(-0.00410529692, 0, 0.777642846, 0)
ScienceBear.Size = UDim2.new(0, 161, 0, 31)
ScienceBear.Font = Enum.Font.SourceSans
ScienceBear.Text = "Science Bear"
ScienceBear.TextColor3 = Color3.fromRGB(0, 0, 0)
ScienceBear.TextSize = 14.000

PolarBear.Name = "Polar Bear"
PolarBear.Parent = page1
PolarBear.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
PolarBear.Position = UDim2.new(0.677999973, 0, 0.708446443, 0)
PolarBear.Size = UDim2.new(0, 161, 0, 31)
PolarBear.Font = Enum.Font.SourceSans
PolarBear.Text = "Polar Bear"
PolarBear.TextColor3 = Color3.fromRGB(0, 0, 0)
PolarBear.TextSize = 14.000

PandaBear.Name = "Panda Bear"
PandaBear.Parent = page1
PandaBear.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
PandaBear.Position = UDim2.new(0.336947322, 0, 0.708446443, 0)
PandaBear.Size = UDim2.new(0, 161, 0, 31)
PandaBear.Font = Enum.Font.SourceSans
PandaBear.Text = "Panda Bear"
PandaBear.TextColor3 = Color3.fromRGB(0, 0, 0)
PandaBear.TextSize = 14.000

MotherBear.Name = "Mother Bear"
MotherBear.Parent = page1
MotherBear.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
MotherBear.Position = UDim2.new(-0.00410529692, 0, 0.708446443, 0)
MotherBear.Size = UDim2.new(0, 161, 0, 31)
MotherBear.Font = Enum.Font.SourceSans
MotherBear.Text = "Mother Bear"
MotherBear.TextColor3 = Color3.fromRGB(0, 0, 0)
MotherBear.TextSize = 14.000

Stick.Name = "Stick"
Stick.Parent = page1
Stick.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Stick.Position = UDim2.new(-0.00400000019, 0, 0.850000024, 0)
Stick.Size = UDim2.new(0, 161, 0, 31)
Stick.Font = Enum.Font.SourceSans
Stick.Text = "Stick Bug"
Stick.TextColor3 = Color3.fromRGB(0, 0, 0)
Stick.TextSize = 14.000

Wind.Name = "Wind"
Wind.Parent = page1
Wind.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Wind.Position = UDim2.new(0.337052613, 0, 0.850000024, 0)
Wind.Size = UDim2.new(0, 161, 0, 31)
Wind.Font = Enum.Font.SourceSans
Wind.Text = "Wind Shrine"
Wind.TextColor3 = Color3.fromRGB(0, 0, 0)
Wind.TextSize = 14.000

Petal.Name = "Petal"
Petal.Parent = page1
Petal.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Petal.Position = UDim2.new(0.677999973, 0, 0.850000024, 0)
Petal.Size = UDim2.new(0, 161, 0, 31)
Petal.Font = Enum.Font.SourceSans
Petal.Text = "Petal Shop"
Petal.TextColor3 = Color3.fromRGB(0, 0, 0)
Petal.TextSize = 14.000

TunelBear.Name = "Tunel Bear"
TunelBear.Parent = page1
TunelBear.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
TunelBear.Position = UDim2.new(0.337052613, 0, 0.919196427, 0)
TunelBear.Size = UDim2.new(0, 161, 0, 31)
TunelBear.Font = Enum.Font.SourceSans
TunelBear.Text = "Tunel Bear"
TunelBear.TextColor3 = Color3.fromRGB(0, 0, 0)
TunelBear.TextSize = 14.000

HoneyBee.Name = "Honey Bee"
HoneyBee.Parent = page1
HoneyBee.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
HoneyBee.Position = UDim2.new(-0.00400000019, 0, 0.919196427, 0)
HoneyBee.Size = UDim2.new(0, 161, 0, 31)
HoneyBee.Font = Enum.Font.SourceSans
HoneyBee.Text = "Honey Bee"
HoneyBee.TextColor3 = Color3.fromRGB(0, 0, 0)
HoneyBee.TextSize = 14.000

Nothing.Name = "Nothing"
Nothing.Parent = page1
Nothing.BackgroundColor3 = Color3.fromRGB(0, 161, 161)
Nothing.Position = UDim2.new(0.677999973, 0, 0.919196427, 0)
Nothing.Size = UDim2.new(0, 161, 0, 31)
Nothing.Font = Enum.Font.SourceSans
Nothing.Text = "Coming Soon"
Nothing.TextColor3 = Color3.fromRGB(0, 0, 0)
Nothing.TextSize = 14.000

loadingpage.Name = "loadingpage"
loadingpage.Parent = LQBHub
loadingpage.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
loadingpage.BackgroundTransparency = -0.010
loadingpage.Position = UDim2.new(0.328498483, 0, 0.282159537, 0)
loadingpage.Size = UDim2.new(0, 216, 0, 122)

Discord.Name = "Discord"
Discord.Parent = loadingpage
Discord.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
Discord.BackgroundTransparency = 1.000
Discord.Position = UDim2.new(-0.458858043, 0, 0.69198209, 0)
Discord.Size = UDim2.new(0, 414, 0, 50)
Discord.Font = Enum.Font.SourceSans
Discord.Text = "Discord: yanwe111#4860"
Discord.TextColor3 = Color3.fromRGB(0, 0, 0)
Discord.TextSize = 20.000

statuskey.Name = "statuskey"
statuskey.Parent = loadingpage
statuskey.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
statuskey.BackgroundTransparency = 1.000
statuskey.Position = UDim2.new(-0.00211334229, 0, 0.354680181, 0)
statuskey.Size = UDim2.new(0, 216, 0, 50)
statuskey.Font = Enum.Font.SourceSans
statuskey.Text = ""
statuskey.TextColor3 = Color3.fromRGB(0, 0, 0)
statuskey.TextSize = 14.000

TextLabel.Parent = loadingpage
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.Position = UDim2.new(-0.00125616568, 0, 0.358824551, 0)
TextLabel.Size = UDim2.new(0, 216, 0, 50)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = ""
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextSize = 14.000

LQBHub_2.Name = "LQB Hub"
LQBHub_2.Parent = loadingpage
LQBHub_2.BackgroundColor3 = Color3.fromRGB(0, 206, 206)
LQBHub_2.BackgroundTransparency = 1.000
LQBHub_2.Position = UDim2.new(-0.458858043, 0, -0.00107681751, 0)
LQBHub_2.Size = UDim2.new(0, 414, 0, 50)
LQBHub_2.Font = Enum.Font.SourceSans
LQBHub_2.Text = "LQB Hub"
LQBHub_2.TextColor3 = Color3.fromRGB(0, 0, 0)
LQBHub_2.TextSize = 20.000

ImageLabel.Parent = loadingpage
ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel.BackgroundTransparency = 1.000
ImageLabel.Position = UDim2.new(0.164978221, 0, 0.072854057, 0)
ImageLabel.Size = UDim2.new(0, 36, 0, 31)
ImageLabel.Image = "rbxassetid://6247725804"

-- Scripts:

local function OBKQBW_fake_script() -- open.open mainpage 
	local script = Instance.new('LocalScript', open)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Visible = false
		script.Parent.Parent.mainpage.Visible = true
	end)
end
coroutine.wrap(OBKQBW_fake_script)()
local function VCQLTA_fake_script() -- minimize.hide mainpage 
	local script = Instance.new('LocalScript', minimize)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Visible = false
		script.Parent.Parent.Parent.open.Visible = true
	end)
end
coroutine.wrap(VCQLTA_fake_script)()
local function PYYZCFI_fake_script() -- waypoint.LocalScript 
	local script = Instance.new('LocalScript', waypoint)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.page1.Visible = true
		script.Parent.Parent.page2.Visible = false
		script.Parent.Parent.page3.Visible = false
		script.Parent.Parent.page4.Visible = false
	end)
end
coroutine.wrap(PYYZCFI_fake_script)()
local function UYZPMOP_fake_script() -- autofarm.LocalScript 
	local script = Instance.new('LocalScript', autofarm)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.page1.Visible = false
		script.Parent.Parent.page2.Visible = true
		script.Parent.Parent.page3.Visible = false
		script.Parent.Parent.page4.Visible = false
	end)
end
coroutine.wrap(UYZPMOP_fake_script)()
local function GESPUGP_fake_script() -- extras.LocalScript 
	local script = Instance.new('LocalScript', extras)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.page1.Visible = false
		script.Parent.Parent.page2.Visible = false
		script.Parent.Parent.page3.Visible = true
		script.Parent.Parent.page4.Visible = false
	end)
end
coroutine.wrap(GESPUGP_fake_script)()
local function OOGMA_fake_script() -- autodig.LocalScript 
	local script = Instance.new('LocalScript', autodig)

	local ad = false
	script.Parent.MouseButton1Click:Connect(function()
		if ad == false then
			ad = true
			script.Parent.BackgroundColor3 = red
		while ad == true do
			wait(0.5)
			for _,b in pairs(game.Players.LocalPlayer.Character:GetChildren()) do 
				if b:IsA("Tool") then 
					b.ClickEvent:FireServer()
				end
			end
		end
		else
			ad = false
			script.Parent.BackgroundColor3 = blue
		end
	end)
end
coroutine.wrap(OOGMA_fake_script)()
local function VXUXBAF_fake_script() -- equipdemon.LocalScript 
	local script = Instance.new('LocalScript', equipdemon)

	script.Parent.MouseButton1Click:Connect(function()
		local BDZ = "Equip"
		local BDZ_2 = 
			{
				["Mute"] = true, 
				["Type"] = "Demon Mask", 
				["Category"] = "Accessory"
			}
		local Event = game:GetService("ReplicatedStorage").Events.ItemPackageEvent
		Event:InvokeServer(BDZ, BDZ_2)
		print('Equip Demon Mask')
	end)
	
end
coroutine.wrap(VXUXBAF_fake_script)()
local function RIWET_fake_script() -- equipgummy.LocalScript 
	local script = Instance.new('LocalScript', equipgummy)

	script.Parent.MouseButton1Click:Connect(function()
		local BDZ = "Equip"
		local BDZ_2 = 
			{
				["Mute"] = true, 
				["Type"] = "Gummy Mask", 
				["Category"] = "Accessory"
			}
		local Event = game:GetService("ReplicatedStorage").Events.ItemPackageEvent
		Event:InvokeServer(BDZ, BDZ_2)
		print('Equip Gummy Mask')
	end)
	
end
coroutine.wrap(RIWET_fake_script)()
local function DBYBO_fake_script() -- equipdiamond.LocalScript 
	local script = Instance.new('LocalScript', equipdiamond)

	script.Parent.MouseButton1Click:Connect(function()
		local BDZ = "Equip"
		local BDZ_2 = 
			{
				["Mute"] = true, 
				["Type"] = "Diamond Mask", 
				["Category"] = "Accessory"
			}
		local Event = game:GetService("ReplicatedStorage").Events.ItemPackageEvent
		Event:InvokeServer(BDZ, BDZ_2)
		print('Equip Diamond Mask')
	end)
	
end
coroutine.wrap(DBYBO_fake_script)()
local function MBRZQ_fake_script() -- KillTunel.LocalScript 
	local script = Instance.new('LocalScript', KillTunel)

	local killtunel = false
	script.Parent.MouseButton1Click:Connect(function()
		if killtunel == false then
			local HRP = workspace:WaitForChild(game.Players.LocalPlayer.Name).HumanoidRootPart
			HRP.CFrame = wp["Tunel Bear"]
			script.Parent.BackgroundColor3 = red
			killtunel = true 
			noclip = true
			for _,v in pairs(game.workspace.Decorations.TrapTunnel:GetChildren()) do 
				if string.find(v.Name,"") then 
					v:Destroy()
	
				end
			end
			wait(6)
			while killtunel do
				wait()
				for _,v in pairs(game.Workspace.Monsters:GetChildren()) do
					if string.find(v.Name,"Tunnel") then
						game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,20.5,0)
	
					end
				end
			end
		else 
			noclip = false    
			killtunel = false 
			script.Parent.BackgroundColor3 = blue 
		end
	end)
end
coroutine.wrap(MBRZQ_fake_script)()
local function BOLEYWP_fake_script() -- KillCoconut.LocalScript 
	local script = Instance.new('LocalScript', KillCoconut)

	script.Parent.MouseButton1Click:Connect(function()
		if script.Parent.BackgroundColor3 == blue then
		local TweenService = game:GetService("TweenService")
		local players = game.Players.LocalPlayer.Character
		local HRP = players.HumanoidRootPart
		local TI = TweenInfo.new(
				3,
				Enum.EasingStyle.Linear,
				Enum.EasingDirection.Out,
				0,
				false,
				0
			)
		local goals = {
				CFrame = CFrame.new(-301.411224, 112.865395, 474.973236, -0.999229074, 2.88422974e-09, 0.0392589495, 1.78224591e-09, 1, -2.81047221e-08, -0.0392589495, -2.80130763e-08, -0.999229074)
			}
		local tween = TweenService:Create(HRP, TI, goals)
		noclip = true
		script.Parent.BackgroundColor3 = red
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-402.776184, 112.865395, 547.087036, -0.986643791, 6.33653263e-09, 0.162893936, 1.78224591e-09, 1, -2.81047221e-08, -0.162893936, -2.74390271e-08, -0.986643791)
			wait(2)
			tween:Play()
		else
			script.Parent.BackgroundColor3 = blue
			noclip = false
		end	
	end)
end
coroutine.wrap(BOLEYWP_fake_script)()
local function NTDGN_fake_script() -- KillKing.LocalScript 
	local script = Instance.new('LocalScript', KillKing)

	script.Parent.MouseButton1Click:Connect(function()
		if script.Parent.BackgroundColor3 == blue then
			local TweenService = game:GetService("TweenService")
			local players = game.Players.LocalPlayer.Character
			local HRP = players.HumanoidRootPart
			local TI = TweenInfo.new(
				3,
				Enum.EasingStyle.Linear,
				Enum.EasingDirection.Out,
				0,
				false,
				0
			)
			local goals = {
				CFrame = wp["King Bettle Bug"]
			}
			local tween = TweenService:Create(HRP, TI, goals)
			script.Parent.BackgroundColor3 = red 
			noclip = true
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["King Bettle"]
			wait(2)
			tween:Play()
		else
			script.Parent.BackgroundColor3 = blue
			noclip = false 
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["King Bettle"]
		end
	end)
end
coroutine.wrap(NTDGN_fake_script)()
local function XJHA_fake_script() -- Noclip.LocalScript 
	local script = Instance.new('LocalScript', Noclip)

	script.Parent.MouseButton1Click:Connect(function()
		if script.Parent.BackgroundColor3 == blue then
			noclip = true
			script.Parent.BackgroundColor3 = red
		else
			noclip = false
			script.Parent.BackgroundColor3 = blue
		end
	end)
end
coroutine.wrap(XJHA_fake_script)()
local function NBLFIE_fake_script() -- KillSnail.LocalScript 
	local script = Instance.new('LocalScript', KillSnail)

	script.Parent.MouseButton1Click:Connect(function()
		if script.Parent.BackgroundColor3 == blue then
			local TweenService = game:GetService("TweenService")
			local players = game.Players.LocalPlayer.Character
			local HRP = players.HumanoidRootPart
			local TI = TweenInfo.new(
				3,
				Enum.EasingStyle.Linear,
				Enum.EasingDirection.Out,
				0,
				false,
				0
			)
			local goals = {
				CFrame = CFrame.new(422.218964, 122.764984, -177.787811, -0.0653970614, 5.28176187e-08, -0.997859657, 8.36690006e-08, 1, 4.74474788e-08, 0.997859657, -8.03868971e-08, -0.0653970614)
			}
			local tween = TweenService:Create(HRP, TI, goals)
			script.Parent.BackgroundColor3 = red
			noclip = true
			HRP.CFrame = CFrame.new(297.838837, 122.764984, 34.4880829, -0.905914068, -2.33645086e-08, -0.423461318, -2.74339982e-08, 1, 3.51471874e-09, 0.423461318, 1.48012793e-08, -0.905914068) 
			wait(2)
			tween:Play()
		else
			noclip = false
			script.Parent.BackgroundColor3 = blue
		end
	end)
end
coroutine.wrap(NBLFIE_fake_script)()
local function TWUGWBJ_fake_script() -- AutoDispenser.LocalScript 
	local script = Instance.new('LocalScript', AutoDispenser)

	local dispenser = false
	script.Parent.MouseButton1Click:Connect(function()
		if dispenser == false then
		dispenser = true
		script.Parent.BackgroundColor3 = red
			while dispenser do 
				wait(2)
				local claim = "Glue Dispenser"
				local event = game:GetService("ReplicatedStorage").Events.ToyEvent
				event:FireServer(claim)
				local claim = "Wealth Clock"
				local event = game:GetService("ReplicatedStorage").Events.ToyEvent
				event:FireServer(claim)
				local claim = "Coconut Dispenser"
				local event = game:GetService("ReplicatedStorage").Events.ToyEvent
				event:FireServer(claim)
				local claim = "Strawberry Dispenser"
				local event = game:GetService("ReplicatedStorage").Events.ToyEvent
				claim:FireServer(claim)
				local claim = "Treat Dispenser"
				local event = game:GetService("ReplicatedStorage").Events.ToyEvent
				event:FireServer(claim)
				local claim = "Free Ant Pass Dispenser"
				local event = game:GetService("ReplicatedStorage").Events.ToyEvent
				event:FireServer(claim)
				local claim = "Blueberry Dispenser"
				local event = game:GetService("ReplicatedStorage").Events.ToyEvent
				event:FireServer(claim)
				local claim = "Honey Dispenser"
				local event = game:GetService("ReplicatedStorage").Events.ToyEvent
				event:FireServer(claim)
				local claim = "Free Royal Jelly Dispenser"
				local event = game:GetService("ReplicatedStorage").Events.ToyEvent
				event:FireServer(claim)
			end
		else
			dispenser = false
			script.Parent.BackgroundColor3 = blue
		end
	end)
end
coroutine.wrap(TWUGWBJ_fake_script)()
local function LHDR_fake_script() -- settings.LocalScript 
	local script = Instance.new('LocalScript', settings)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.page1.Visible = false
		script.Parent.Parent.page2.Visible = false
		script.Parent.Parent.page3.Visible = false
		script.Parent.Parent.page4.Visible = true
	end)
end
coroutine.wrap(LHDR_fake_script)()
local function BGGGSV_fake_script() -- Bamboo.LocalScript 
	local script = Instance.new('LocalScript', Bamboo)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Bamboo Field"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(BGGGSV_fake_script)()
local function CVCNBE_fake_script() -- Dandelion.LocalScript 
	local script = Instance.new('LocalScript', Dandelion)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Dandelion Field"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(CVCNBE_fake_script)()
local function MZDAXN_fake_script() -- Mushroom.LocalScript 
	local script = Instance.new('LocalScript', Mushroom)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Mushroom Field"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(MZDAXN_fake_script)()
local function DPVYO_fake_script() -- Blueflower.LocalScript 
	local script = Instance.new('LocalScript', Blueflower)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Blue Flower Field"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(DPVYO_fake_script)()
local function VXME_fake_script() -- Sunflower.LocalScript 
	local script = Instance.new('LocalScript', Sunflower)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Sunflower Field"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(VXME_fake_script)()
local function CESPADO_fake_script() -- Spider.LocalScript 
	local script = Instance.new('LocalScript', Spider)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Spider Field"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(CESPADO_fake_script)()
local function FGMDWPF_fake_script() -- Clover.LocalScript 
	local script = Instance.new('LocalScript', Clover)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Clover Field"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(FGMDWPF_fake_script)()
local function LNBH_fake_script() -- Cactus.LocalScript 
	local script = Instance.new('LocalScript', Cactus)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Cactus Field"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(LNBH_fake_script)()
local function SPNO_fake_script() -- Pineapple.LocalScript 
	local script = Instance.new('LocalScript', Pineapple)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Pineapple Patch"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(SPNO_fake_script)()
local function SYRH_fake_script() -- Stump.LocalScript 
	local script = Instance.new('LocalScript', Stump)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Stump Field"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(SYRH_fake_script)()
local function OVOMJCN_fake_script() -- Strawberry.LocalScript 
	local script = Instance.new('LocalScript', Strawberry)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Strawberry Field"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(OVOMJCN_fake_script)()
local function FIZOLNA_fake_script() -- Pinetree.LocalScript 
	local script = Instance.new('LocalScript', Pinetree)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Pine Tree Forest"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(FIZOLNA_fake_script)()
local function UKVDTMF_fake_script() -- Rose.LocalScript 
	local script = Instance.new('LocalScript', Rose)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Rose Field"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(UKVDTMF_fake_script)()
local function UKNNGCP_fake_script() -- Pumpkin.LocalScript 
	local script = Instance.new('LocalScript', Pumpkin)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Pumpkin Patch"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(UKNNGCP_fake_script)()
local function JOLTJAH_fake_script() -- Mountain.LocalScript 
	local script = Instance.new('LocalScript', Mountain)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Mountain Top Field"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(JOLTJAH_fake_script)()
local function BQFXTJ_fake_script() -- Coconut.LocalScript 
	local script = Instance.new('LocalScript', Coconut)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Coconut Field"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(BQFXTJ_fake_script)()
local function NHVQLN_fake_script() -- Pepper.LocalScript 
	local script = Instance.new('LocalScript', Pepper)

	script.Parent.MouseButton1Click:Connect(function()
		baodz = "Pepper Patch"
		script.Parent.Parent.Parent.fieldtofarm.Text = "Field To Farm: "..baodz
	end)
end
coroutine.wrap(NHVQLN_fake_script)()
local function EOTGN_fake_script() -- Autofarmtween.LocalScript 
	local script = Instance.new('LocalScript', Autofarmtween)

	local plr = game.Players.LocalPlayer
	local autofarm = false
	local makehoney = false
	local placespr = false
	local function atf(HRP,FZ)
		local atf1 = coroutine.wrap(function()
			repeat
				local HRP = plr.Character.HumanoidRootPart
				local HRPCF = HRP.CFrame
				local FZ = game.Workspace.FlowerZones[baodz].CFrame
				noclip = true
				local TweenService = game:GetService("TweenService")
				local TI = TweenInfo.new(
					.01,
					Enum.EasingStyle.Linear,
					Enum.EasingDirection.Out,
					0,
					false,
					0
				)
				for k,v in pairs(workspace.Collectibles:GetChildren()) do
					if tostring(v) == tostring(game.Players.LocalPlayer.Name) or tostring(v) == "C" then
						if (v.Position-HRP.Position).magnitude <= 45 then
							local goals = {
								CFrame = CFrame.new(v.Position.x, HRP.Position.y, v.Position.z)
							}
							local tween = TweenService:Create(HRP, TI, goals)
							tween:Play()
							wait(.05)
						end
					end
				end
				wait(1)
				local goals = {
					CFrame = FZ * CFrame.new(0,0,0)
				}
				local tween = TweenService:Create(HRP, TI, goals)
				tween:Play()
				wait(1)
				if placespr == true then
					local sprinkler = {
						["Name"] = "Sprinkler Builder"
					}
					local event = game:GetService("ReplicatedStorage").Events.PlayerActivesCommand
					event:FireServer(sprinkler)
					placespr = false
				end
				wait(.05)
			until not autofarm or makehoney or placespr
		end)
		local atc = coroutine.wrap(function()
			for k,v in pairs(workspace[plr.Name]:GetChildren()) do
				if v.ClassName == "Tool" then
					repeat
						v.ClickEvent:FireServer()
						wait(.1)
					until not autofarm or makehoney
				end
			end
		end)
		atf1()
		atc()
	end
	script.Parent.MouseButton1Down:connect(function()
		if autofarm == true then
			autofarm = false
			placespr = false
			noclip = false
			script.Parent.BackgroundColor3 = blue
			script.Parent.Text = "Start Auto Farm"
		else
			autofarm = true
			placespr = true
			script.Parent.BackgroundColor3 = red
			script.Parent.Text = "Stop Auto Farm"
			local MH = coroutine.wrap(function()
				repeat
					wait()
					for k,v in pairs(workspace[plr.Name]:GetChildren()) do
						if v:FindFirstChild("Display") then
							if v.Display.Gui.ProgressBar.Size == v.Display.Gui.RedBar.Size or v.Display.Gui.ProgressLabel == plr.CoreStats.Pollen.Value.."/"..plr.CoreStats.Pollen.Value or plr.CoreStats.Pollen.Value == plr.CoreStats.Capacity then
								makehoney = true
								wait(3)
								local HRP = plr.Character.HumanoidRootPart
								local HRPCF = HRP.CFrame
								local FZ = game.Workspace.FlowerZones[baodz].CFrame
								game:GetService("Players").LocalPlayer.Character:MoveTo(game:GetService("Players").LocalPlayer.SpawnPos.Value.p)
								wait(3)
								game:GetService("ReplicatedStorage").Events.PlayerHiveCommand:FireServer("ToggleHoneyMaking")
								repeat wait(.1) until game.Players.LocalPlayer.CoreStats.Pollen.Value <= 1
								wait(7)     
								local TweenService = game:GetService("TweenService")
								local TI = TweenInfo.new(
									.01,
									Enum.EasingStyle.Linear,
									Enum.EasingDirection.Out,
									0,
									false,
									0
								)
								local goals = {
									CFrame = FZ * CFrame.new(0,0,0)
								}
								local tween = TweenService:Create(HRP, TI, goals)
								tween:Play()
								wait(1)
								local sprinkler = {
									["Name"] = "Sprinkler Builder"
								}
								local event = game:GetService("ReplicatedStorage").Events.PlayerActivesCommand
								event:FireServer(sprinkler)
								wait(1)
								atf(HRP,FZ)
								makehoney = false
							end
						end
						wait()
					end
					wait(1)
				until not autofarm
			end)
			atf(HRP,FZ)
			MH()	
		end
	end)
end
coroutine.wrap(EOTGN_fake_script)()
local function ZXQZY_fake_script() -- Typeautofarm.LocalScript 
	local script = Instance.new('LocalScript', Typeautofarm)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.BackgroundType.Visible = true
	end)
end
coroutine.wrap(ZXQZY_fake_script)()
local function IRJMJ_fake_script() -- Tween.LocalScript 
	local script = Instance.new('LocalScript', Tween)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Parent.Typeautofarm.Text = script.Parent.Text
		script.Parent.Parent.Visible = false
		script.Parent.Parent.Parent.Autofarmtween.Visible = true
		script.Parent.Parent.Parent.Autofarmwalk.Visible = false
	end)
end
coroutine.wrap(IRJMJ_fake_script)()
local function CDOOJKD_fake_script() -- Walking.LocalScript 
	local script = Instance.new('LocalScript', Walking)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Parent.Typeautofarm.Text = script.Parent.Text
		script.Parent.Parent.Visible = false
		script.Parent.Parent.Parent.Autofarmtween.Visible = false
		script.Parent.Parent.Parent.Autofarmwalk.Visible = true
	end)
end
coroutine.wrap(CDOOJKD_fake_script)()
local function VAQFRDZ_fake_script() -- Autofarmwalk.LocalScript 
	local script = Instance.new('LocalScript', Autofarmwalk)

	local plr1 = game.Players.LocalPlayer
	local autofarm1 = false
	local makehoney1 = false
	local placespr1 = false
	local function atf(HRP1,FZ1)
		local atf1 = coroutine.wrap(function()
			repeat
				local HRP1 = plr1.Character.HumanoidRootPart
				local HRPCF1 = HRP1.CFrame
				local FZ1 = game.Workspace.FlowerZones[baodz].CFrame
				local FZ = game.Workspace.FlowerZones[baodz]
				local FZP = FZ.Position
				local PLC1 = plr1.Character 
				noclip = true
				for k,v in pairs(workspace.Collectibles:GetChildren()) do
					if tostring(v) == tostring(game.Players.LocalPlayer.Name) or tostring(v) == "C" then
						if (v.Position-HRP1.Position).magnitude <= 45 then
							local pos = v.Position
									PLC1.Humanoid:MoveTo(Vector3.new(pos.X, pos.Y, pos.Z))
									PLC1.Humanoid.MoveToFinished:Wait()
							wait(.05)
						end
					end
				end
				noclip = false
				wait(1)
				game.Players.LocalPlayer.Character:MoveTo(Vector3.new(FZP.X,FZP.Y,FZP.Z))
				wait(1)
				if placespr1 == true then
					local sprinkler = {
						["Name"] = "Sprinkler Builder"	
					}
					local event = game:GetService("ReplicatedStorage").Events.PlayerActivesCommand
					event:FireServer(sprinkler)
					placespr1 = false
				end
				wait(1)
				noclip = true
				wait(.05)
			until not autofarm1 or makehoney1 or placespr1
		end)
		local atc = coroutine.wrap(function()
			for k,v in pairs(workspace[plr1.Name]:GetChildren()) do
				if v.ClassName == "Tool" then
					repeat
						v.ClickEvent:FireServer()
						wait(.1)
					until not autofarm1 or makehoney1
				end
			end
		end)
		atf1()
		atc()
	end
	script.Parent.MouseButton1Down:connect(function()
		if autofarm1 == true then
			autofarm1 = false
			placespr1 = false
			noclip = false
			script.Parent.BackgroundColor3 = blue
			script.Parent.Text = "Start Auto Farm"
		else
			autofarm1 = true
			placespr1 = true
			script.Parent.BackgroundColor3 = red
			script.Parent.Text = "Stop Auto Farm"
			local MH = coroutine.wrap(function()
				repeat
					wait()
					for k,v in pairs(workspace[plr1.Name]:GetChildren()) do
						if v:FindFirstChild("Display") then
							if v.Display.Gui.ProgressBar.Size == v.Display.Gui.RedBar.Size or v.Display.Gui.ProgressLabel == plr1.CoreStats.Pollen.Value.."/"..plr1.CoreStats.Pollen.Value or plr1.CoreStats.Pollen.Value == plr1.CoreStats.Capacity then
								makehoney1 = true
								wait(3)
								local HRP1 = plr1.Character.HumanoidRootPart
								local HRPCF1 = HRP1.CFrame
								local FZ1 = game.Workspace.FlowerZones[baodz].CFrame
								local FZ = game.Workspace.FlowerZones[baodz]
								local FZP = FZ.Position
								local PLC1 = plr1.Character 
								game:GetService("Players").LocalPlayer.Character:MoveTo(game:GetService("Players").LocalPlayer.SpawnPos.Value.p)
								wait(3)
								game:GetService("ReplicatedStorage").Events.PlayerHiveCommand:FireServer("ToggleHoneyMaking")
								repeat wait(.1) until game.Players.LocalPlayer.CoreStats.Pollen.Value <= 1
								wait(7)   
								game.Players.LocalPlayer.Character:MoveTo(Vector3.new(FZP.X,FZP.Y,FZP.Z))
								wait(1)
								local sprinkler = {
									["Name"] = "Sprinkler Builder"
								}
								local event = game:GetService("ReplicatedStorage").Events.PlayerActivesCommand
								event:FireServer(sprinkler)
								wait(1)
								atf(HRP1,FZ1)
								makehoney1 = false
							end
						end
						wait()
					end
					wait(1)
				until not autofarm1
			end)
			atf(HRP1,FZ1)
			MH()	
		end
	end)
end
coroutine.wrap(VAQFRDZ_fake_script)()
local function RDNPLJH_fake_script() -- Dandelion_2.LocalScript 
	local script = Instance.new('LocalScript', Dandelion_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Dandelion Field"]
	end)
end
coroutine.wrap(RDNPLJH_fake_script)()
local function SSCB_fake_script() -- Mushroom_2.LocalScript 
	local script = Instance.new('LocalScript', Mushroom_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Mushroom Field"]
	end)
end
coroutine.wrap(SSCB_fake_script)()
local function MWTQ_fake_script() -- Clover_2.LocalScript 
	local script = Instance.new('LocalScript', Clover_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Clover Field"]
	end)
end
coroutine.wrap(MWTQ_fake_script)()
local function ZHSWL_fake_script() -- Sunflower_2.LocalScript 
	local script = Instance.new('LocalScript', Sunflower_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Sunflower Field"]
	end)
end
coroutine.wrap(ZHSWL_fake_script)()
local function EVBB_fake_script() -- Spider_2.LocalScript 
	local script = Instance.new('LocalScript', Spider_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Spider Field"]
	end)
end
coroutine.wrap(EVBB_fake_script)()
local function RYGOA_fake_script() -- Blueflower_2.LocalScript 
	local script = Instance.new('LocalScript', Blueflower_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Blue Flower Field"]
	end)
end
coroutine.wrap(RYGOA_fake_script)()
local function GYIZWL_fake_script() -- Bamboo_2.LocalScript 
	local script = Instance.new('LocalScript', Bamboo_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Bamboo Field"]
	end)
end
coroutine.wrap(GYIZWL_fake_script)()
local function DHCAB_fake_script() -- Pinetree_2.LocalScript 
	local script = Instance.new('LocalScript', Pinetree_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Pine Tree Forest"]
	end)
end
coroutine.wrap(DHCAB_fake_script)()
local function VRIP_fake_script() -- Strawberry_2.LocalScript 
	local script = Instance.new('LocalScript', Strawberry_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Strawberry Field"]
	end)
end
coroutine.wrap(VRIP_fake_script)()
local function YRSBI_fake_script() -- Cactus_2.LocalScript 
	local script = Instance.new('LocalScript', Cactus_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Cactus Field"]
	end)
end
coroutine.wrap(YRSBI_fake_script)()
local function YJYI_fake_script() -- Rose_2.LocalScript 
	local script = Instance.new('LocalScript', Rose_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Rose Field"]
	end)
end
coroutine.wrap(YJYI_fake_script)()
local function IXKAKYY_fake_script() -- Pumpkin_2.LocalScript 
	local script = Instance.new('LocalScript', Pumpkin_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Pumpkin Patch"]
	end)
end
coroutine.wrap(IXKAKYY_fake_script)()
local function MTHFAU_fake_script() -- Pepper_2.LocalScript 
	local script = Instance.new('LocalScript', Pepper_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Pepper Patch"]
	end)
end
coroutine.wrap(MTHFAU_fake_script)()
local function RPZYS_fake_script() -- Coconut_2.LocalScript 
	local script = Instance.new('LocalScript', Coconut_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Coconut Field"]
	end)
end
coroutine.wrap(RPZYS_fake_script)()
local function GEEGZ_fake_script() -- Pineapple_2.LocalScript 
	local script = Instance.new('LocalScript', Pineapple_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Pineapple Patch"]
	end)
end
coroutine.wrap(GEEGZ_fake_script)()
local function XMLQ_fake_script() -- Stump_2.LocalScript 
	local script = Instance.new('LocalScript', Stump_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Stump Field"]
	end)
end
coroutine.wrap(XMLQ_fake_script)()
local function POFX_fake_script() -- Mountain_2.LocalScript 
	local script = Instance.new('LocalScript', Mountain_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Mountain Top Field"]
	end)
end
coroutine.wrap(POFX_fake_script)()
local function HMGFJKY_fake_script() -- BeginnerShop.LocalScript 
	local script = Instance.new('LocalScript', BeginnerShop)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Beginner shop"]
	end)
end
coroutine.wrap(HMGFJKY_fake_script)()
local function YXMKJVL_fake_script() -- ProShop.LocalScript 
	local script = Instance.new('LocalScript', ProShop)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Pro Shop"]
	end)
end
coroutine.wrap(YXMKJVL_fake_script)()
local function DDRE_fake_script() -- TopShop.LocalScript 
	local script = Instance.new('LocalScript', TopShop)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Top Shop"]
	end)
end
coroutine.wrap(DDRE_fake_script)()
local function FLXPAVX_fake_script() -- MegaMemory.LocalScript 
	local script = Instance.new('LocalScript', MegaMemory)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Mega Memory"]
	end)
end
coroutine.wrap(FLXPAVX_fake_script)()
local function PCSZTSO_fake_script() -- Memory.LocalScript 
	local script = Instance.new('LocalScript', Memory)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Memory"]
	end)
end
coroutine.wrap(PCSZTSO_fake_script)()
local function YYZMTY_fake_script() -- Night.LocalScript 
	local script = Instance.new('LocalScript', Night)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Night Memory"]
	end)
end
coroutine.wrap(YYZMTY_fake_script)()
local function HQEP_fake_script() -- ExtremeMemory.LocalScript 
	local script = Instance.new('LocalScript', ExtremeMemory)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Extreme Memory"]
	end)
end
coroutine.wrap(HQEP_fake_script)()
local function QNKLGFA_fake_script() -- GummyMask.LocalScript 
	local script = Instance.new('LocalScript', GummyMask)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Gummy Mask"]
	end)
end
coroutine.wrap(QNKLGFA_fake_script)()
local function KWCOGFL_fake_script() -- DiamondMask.LocalScript 
	local script = Instance.new('LocalScript', DiamondMask)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Diamond Mask"]
	end)
end
coroutine.wrap(KWCOGFL_fake_script)()
local function ARTPY_fake_script() -- DemonMask.LocalScript 
	local script = Instance.new('LocalScript', DemonMask)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Demon Mask"]
	end)
end
coroutine.wrap(ARTPY_fake_script)()
local function BWJB_fake_script() -- Onett.LocalScript 
	local script = Instance.new('LocalScript', Onett)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Onett"]
	end)
end
coroutine.wrap(BWJB_fake_script)()
local function SUIDLGK_fake_script() -- BlackBear.LocalScript 
	local script = Instance.new('LocalScript', BlackBear)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Black Bear"]
	end)
end
coroutine.wrap(SUIDLGK_fake_script)()
local function VICIEHI_fake_script() -- BrownBear.LocalScript 
	local script = Instance.new('LocalScript', BrownBear)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Brown Bear"]
	end)
end
coroutine.wrap(VICIEHI_fake_script)()
local function XIZI_fake_script() -- KingBettle.LocalScript 
	local script = Instance.new('LocalScript', KingBettle)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["King Bettle"]
	end)
end
coroutine.wrap(XIZI_fake_script)()
local function QCRYU_fake_script() -- SpiritBear.LocalScript 
	local script = Instance.new('LocalScript', SpiritBear)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Spirit Bear"]
	end)
end
coroutine.wrap(QCRYU_fake_script)()
local function XGMVAQE_fake_script() -- ScienceBear.LocalScript 
	local script = Instance.new('LocalScript', ScienceBear)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Science Bear"]
	end)
end
coroutine.wrap(XGMVAQE_fake_script)()
local function JYXW_fake_script() -- PolarBear.LocalScript 
	local script = Instance.new('LocalScript', PolarBear)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Polar Bear"]
	end)
end
coroutine.wrap(JYXW_fake_script)()
local function UWJXBPT_fake_script() -- PandaBear.LocalScript 
	local script = Instance.new('LocalScript', PandaBear)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Panda Bear"]
	end)
end
coroutine.wrap(UWJXBPT_fake_script)()
local function MZGSEL_fake_script() -- MotherBear.LocalScript 
	local script = Instance.new('LocalScript', MotherBear)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Mother Bear"]
	end)
end
coroutine.wrap(MZGSEL_fake_script)()
local function PHIRXRE_fake_script() -- Stick.LocalScript 
	local script = Instance.new('LocalScript', Stick)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Stick Bug"]
	end)
end
coroutine.wrap(PHIRXRE_fake_script)()
local function ALOSHLS_fake_script() -- Wind.LocalScript 
	local script = Instance.new('LocalScript', Wind)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Wind Shrine"]
	end)
end
coroutine.wrap(ALOSHLS_fake_script)()
local function QNCJK_fake_script() -- Petal.LocalScript 
	local script = Instance.new('LocalScript', Petal)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Petal Shop"]
	end)
end
coroutine.wrap(QNCJK_fake_script)()
local function THZTJCF_fake_script() -- TunelBear.LocalScript 
	local script = Instance.new('LocalScript', TunelBear)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Tunel Bear"]
	end)
end
coroutine.wrap(THZTJCF_fake_script)()
local function LKWNF_fake_script() -- HoneyBee.LocalScript 
	local script = Instance.new('LocalScript', HoneyBee)

	script.Parent.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = wp["Honey Bee"]
	end)
end
coroutine.wrap(LKWNF_fake_script)()
local function ZUVUE_fake_script() -- TextLabel.LocalScript 
	local script = Instance.new('LocalScript', TextLabel)

	if keycheck == true then
		local w = 0
			for a = 1,3 do
				wait(0.3)
				script.Parent.Parent.statuskey.Text = "Checking key"..string.rep('.',w%3+1)
				w = w + 1
			end
			wait(1)
			script.Parent.Parent.statuskey.Text = "Correct key"
			wait(2)
			script.Parent.Parent.statuskey:Destroy()
			script.Parent.Text = ""
			wait(.1)
			local load = 0
			for d=1,10 do 
				wait(.3)
				script.Parent.Parent.TextLabel.Text = "Loading Place"..string.rep('.',load%3+1)
				load = load + 1
			end
				if game.PlaceId == 1537690962 or game.PlaceId == 4079902982 then
				script.Parent.Parent.TextLabel.Text = "Loading Place: 🎄 Bee Swarm Simulator"
					wait(1)
					script.Parent.Parent:TweenPosition(UDim2.new(0,0,1,0),"InOut","Sine",0.5)
			script.Parent.Parent.Parent.mainpage.Position = UDim2.new(0.117,0,-1,0)
					script.Parent.Parent.Parent.mainpage.Visible = true
					script.Parent.Parent.Parent.mainpage:TweenPosition(UDim2.new(0.117, 0,0.046, 0), "InOut", "Sine", 0.5)
					wait(.1)
					script.Parent.Parent:Destroy()
				else
					script.Parent.Parent.TextLabel.Text = "Wrong Place"
					wait(2)
					script.Parent.Parent.Parent:Destroy()
				end
	else
	  		local n = 0
			for b = 1,3 do
				wait(0.3)
				script.Parent.Parent.statuskey.Text = "Checking key"..string.rep('.',n%3+1)
				n = n + 1
			end
			wait(1)
			script.Parent.Parent.statuskey.Text = "Wrong key. Please Take new key !"
			wait(2)
			script.Parent.Parent.Parent:Destroy()
	end
end
coroutine.wrap(ZUVUE_fake_script)()
local function UDMBYS_fake_script() -- LQBHub_2.LocalScript 
	local script = Instance.new('LocalScript', LQBHub_2)

	local r = { 
		Color3.fromRGB(254, 0, 0);  
		Color3.fromRGB(255, 127, 0); 
		Color3.fromRGB(255, 221, 1); 
		Color3.fromRGB(0, 200, 0);  
		Color3.fromRGB(0, 160, 199); 
		Color3.fromRGB(0, 55, 230);  
		Color3.fromRGB(129, 16, 210)} 
	local info = TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut, 0, false, 0)
	script.Parent.TextColor3 = r[1] 
	i = 1
	while true do
		local tween = game:GetService("TweenService"):Create(script.Parent, info, {
			TextColor3 = r[i]}) 
		tween:Play()
		repeat wait() until tween.Completed
		wait(0.1)
		if i == #r then i = 1 else i = i + 1 end
	end
end
coroutine.wrap(UDMBYS_fake_script)()
