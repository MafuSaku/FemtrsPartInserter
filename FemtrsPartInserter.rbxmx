--[[

███████╗███████╗███╗░░░███╗████████╗██████╗░██╗░██████╗  ██████╗░░█████╗░██████╗░████████╗
██╔════╝██╔════╝████╗░████║╚══██╔══╝██╔══██╗╚█║██╔════╝  ██╔══██╗██╔══██╗██╔══██╗╚══██╔══╝
█████╗░░█████╗░░██╔████╔██║░░░██║░░░██████╔╝░╚╝╚█████╗░  ██████╔╝███████║██████╔╝░░░██║░░░
██╔══╝░░██╔══╝░░██║╚██╔╝██║░░░██║░░░██╔══██╗░░░░╚═══██╗  ██╔═══╝░██╔══██║██╔══██╗░░░██║░░░
██║░░░░░███████╗██║░╚═╝░██║░░░██║░░░██║░░██║░░░██████╔╝  ██║░░░░░██║░░██║██║░░██║░░░██║░░░
╚═╝░░░░░╚══════╝╚═╝░░░░░╚═╝░░░╚═╝░░░╚═╝░░╚═╝░░░╚═════╝░  ╚═╝░░░░░╚═╝░░╚═╝╚═╝░░╚═╝░░░╚═╝░░░

██╗███╗░░██╗░██████╗███████╗██████╗░████████╗███████╗██████╗░
██║████╗░██║██╔════╝██╔════╝██╔══██╗╚══██╔══╝██╔════╝██╔══██╗
██║██╔██╗██║╚█████╗░█████╗░░██████╔╝░░░██║░░░█████╗░░██████╔╝
██║██║╚████║░╚═══██╗██╔══╝░░██╔══██╗░░░██║░░░██╔══╝░░██╔══██╗
██║██║░╚███║██████╔╝███████╗██║░░██║░░░██║░░░███████╗██║░░██║
╚═╝╚═╝░░╚══╝╚═════╝░╚══════╝╚═╝░░╚═╝░░░╚═╝░░░╚══════╝╚═╝░░╚═╝

Description:
This plugin is an open-source plugin where you can insert specific parts onto Roblox Studio to control and make life easier with things already pre-made to your liking and standrd.

GitHub Repository:
https://github.com/mafusaku/FemtrsPartInserter

License:
MIT License (https://opensource.org/licenses/MIT)

]]--

--// Variables
local toolbar = plugin:CreateToolbar("Femtr's Part Inserter") -- Creating Plugin on the toolbar and naming the plugin

local button = toolbar:CreateButton("Create Part","Creates a 2x2 Sized Part","rbxassetid://413369028") -- Button Name, Description, Image (rbxassetid://[ID])
local button2 = toolbar:CreateButton("Create Sphere", "Creates a 2x2 Sized Sphere", "rbxassetid://1108275823")
local button3 = toolbar:CreateButton("Create Wedge", "Creates a 2x2 Sized Wedge", "rbxassetid://427534899")
local button4 = toolbar:CreateButton("Create Corner Wedge", "Creates a 2x2 Sized Corner Wedge", "rbxassetid://427534806")
local button5 = toolbar:CreateButton("Create Cylinder", "Creates a 2x2 Sized Cylinder", "rbxassetid://9086583856")
local button6 = toolbar:CreateButton("Create Mesh Part", "Creates a 2x2 Sized Mesh Part", "rbxassetid://413367093")
local button7 = toolbar:CreateButton("Create Truss Part", "Creates a 2x2 Sized Truss Part", "rbxassetid://9087431519")

local camera = workspace.CurrentCamera -- Defining and getting the camera on workspace (Creator's Camera in Studio)

local ChangeHistoryService = game:GetService("ChangeHistoryService")

--// Running code when the button is pressed
--// Button (Creating Part)
button.Click:Connect(function ()
	
	local part = Instance.new("Part", workspace) -- Creating a new part and placing it into workspace
	part.Anchored = true -- Anchors the part (You want to anchor it so it doesn't fall over it gets knocked when a player or object touches it)
	part.Material = Enum.Material.SmoothPlastic -- Part material
	part.BrickColor = BrickColor.new("Institutional white") -- Changes the part color
	
	part.TopSurface = Enum.SurfaceType.SmoothNoOutlines -- Changing the surface type of the part on the top
	part.BottomSurface = Enum.SurfaceType.SmoothNoOutlines -- Changing the surface type of the part on the bottom
	
	part.Size = Vector3.new(2, 2, 2) -- Changing the part size to whatever is set (Vector3.new(#, #, #))
	
	part.CFrame = camera.CFrame + (camera.CFrame.LookVector * 5) -- Makes it so the part spawns 5 studs away from the Creator's Camera
	part.Orientation = Vector3.new(0, 0, 0) -- Makes it so the part does not rotate weirdly when spawned in
	
	ChangeHistoryService:SetWaypoint("Create Part") -- Makes it so whenever the Creator undos (CTRL+Z) something the previous parts if there's multiple will not be affected
	
end)

--// Button2 (Creating Sphere)
button2.Click:Connect(function ()
	
	local part = Instance.new("Part", workspace)
	part.Anchored = true
	part.Shape = Enum.PartType.Ball
	part.Material = Enum.Material.SmoothPlastic
	part.BrickColor = BrickColor.new("Institutional white")

	part.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	part.BottomSurface = Enum.SurfaceType.SmoothNoOutlines

	part.Size = Vector3.new(2, 2, 2) 

	part.CFrame = camera.CFrame + (camera.CFrame.LookVector * 5)
	part.Orientation = Vector3.new(0, 0, 0)

	ChangeHistoryService:SetWaypoint("Create Sphere")
	
end)

--// Button3 (Creating Wedge)
button3.Click:Connect(function ()

	local part = Instance.new("WedgePart", workspace)
	part.Anchored = true
	part.Material = Enum.Material.SmoothPlastic
	part.BrickColor = BrickColor.new("Institutional white")

	part.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	part.BottomSurface = Enum.SurfaceType.SmoothNoOutlines

	part.Size = Vector3.new(2, 2, 2) 

	part.CFrame = camera.CFrame + (camera.CFrame.LookVector * 5)
	part.Orientation = Vector3.new(0, 0, 0)

	ChangeHistoryService:SetWaypoint("Create Wedge")

end)

--// Button4 (Creating Corner Wedge)
button4.Click:Connect(function ()

	local part = Instance.new("CornerWedgePart", workspace)
	part.Anchored = true
	part.Material = Enum.Material.SmoothPlastic
	part.BrickColor = BrickColor.new("Institutional white")

	part.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	part.BottomSurface = Enum.SurfaceType.SmoothNoOutlines

	part.Size = Vector3.new(2, 2, 2) 

	part.CFrame = camera.CFrame + (camera.CFrame.LookVector * 5)
	part.Orientation = Vector3.new(0, 0, 0)

	ChangeHistoryService:SetWaypoint("Create Corner Wedge")

end)

--// Button 5 (Creating Cylinder)
button5.Click:Connect(function ()

	local part = Instance.new("Part", workspace)
	part.Anchored = true
	part.Shape = Enum.PartType.Cylinder
	part.Material = Enum.Material.SmoothPlastic
	part.BrickColor = BrickColor.new("Institutional white")

	part.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	part.BottomSurface = Enum.SurfaceType.SmoothNoOutlines

	part.Size = Vector3.new(2, 2, 2) 

	part.CFrame = camera.CFrame + (camera.CFrame.LookVector * 5)
	part.Orientation = Vector3.new(0, 0, 0)

	ChangeHistoryService:SetWaypoint("Create Cylinder")

end)

--// Button 6 (Creating Mesh Part)
button6.Click:Connect(function ()

	local part = Instance.new("MeshPart", workspace)
	part.Anchored = true
	part.Material = Enum.Material.SmoothPlastic
	part.BrickColor = BrickColor.new("Institutional white")
	part.TextureID = "rbxassetid://6372755229"

	part.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	part.BottomSurface = Enum.SurfaceType.SmoothNoOutlines

	part.Size = Vector3.new(2, 2, 2) 

	part.CFrame = camera.CFrame + (camera.CFrame.LookVector * 5)
	part.Orientation = Vector3.new(0, 0, 0)

	ChangeHistoryService:SetWaypoint("Create MeshPart")

end)

--// Button 7 (Creating Truss Part)
button7.Click:Connect(function ()

	local part = Instance.new("TrussPart", workspace)
	part.Anchored = true
	part.Material = Enum.Material.SmoothPlastic
	part.BrickColor = BrickColor.new("Institutional white")

	part.TopSurface = Enum.SurfaceType.SmoothNoOutlines
	part.BottomSurface = Enum.SurfaceType.SmoothNoOutlines

	part.Size = Vector3.new(2, 2, 2) 

	part.CFrame = camera.CFrame + (camera.CFrame.LookVector * 5)
	part.Orientation = Vector3.new(0, 0, 0)

	ChangeHistoryService:SetWaypoint("Create TrussPart")

end)