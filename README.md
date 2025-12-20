--[[
    YetaHub UI Library
    Simple & Lightweight UI Library

    Created by: YetaHub
    License: MIT
]]

--==============================
-- LOAD LIBRARY
--==============================

local library = Coming soon


--==============================
-- CREATE WINDOW
--==============================

local window = library:Window("Window")


--==============================
-- DESTROY WINDOW
--==============================

-- window:Destroy()


--==============================
-- BUTTON
--==============================
-- Name of button, callback

window:Button("Button name", function()
    print("pressed button")
end)


--==============================
-- TOGGLE
--==============================
-- Name, default state, callback

window:Toggle("Example toggle", true, function(bool)
    print(bool) -- true / false
end)


--==============================
-- COLOR PICKER
--==============================
-- Name, default color (true = rainbow), callback

window:ColorPicker("Color Picker", Color3.fromRGB(255, 255, 255), function(color)
    print(color)
end)


--==============================
-- SLIDER
--==============================
-- Name, min value, max value, default value, callback

window:Slider("Example Slider", 0, 100, 20, function(value)
    print(value)
end)


--==============================
-- LABEL
--==============================
-- Text, color (true = rainbow effect)

window:Label("Credits to Intrer#0421", Color3.fromRGB(127, 143, 166))


--==============================
-- INPUT BOX / TEXTBOX
--==============================
-- Name, callback
-- text = input user
-- focuslost = true if user finished typing

window:Box("Walkspeed", function(text, focuslost)
    if focuslost then
        print(text)
    end
end)


--==============================
-- DROPDOWN
--==============================
-- Name, table options, callback

local dropdown = window:Dropdown(
    "Example dropdown",
    {"Button 1", "Button 2", "Third button"},
    function(name)
        print(name)
    end
)


--==============================
-- ADD BUTTON TO DROPDOWN
--==============================

dropdown:Button("New button")


--==============================
-- REMOVE BUTTON FROM DROPDOWN
--==============================
-- Will warn if button doesn't exist

dropdown:Remove("Button")


--==============================
-- KEYBIND (SHOW / HIDE UI)
--==============================
-- Key example: "P"

library:Keybind("P")


--==============================
-- DESTROY UI
--==============================

-- library:Destroy()
