# Ui Lib

```lua
local library = loadstring(game:HttpGet('https://raw.githubusercontent.com/HoyoGey/CoconutGreen/main/Asset/Ui.lua'))()

local Window = library:CreateWindow("Name", "Version", 10044538000)

local Tab = Window:CreateTab("Scripts")

local sec = Tab:CreateFrame("Page 1")

sec:Button("Button", function()

end)

--sec:Toggle(title <string>,default <boolean>, flag <string>, callback <function>)
local toggle = sec:Toggle("Toggle", false, function(t)
   print(t)
end)

--[[
toggle:Set(state <boolean>)
]]

--sec:Slider(title <string>,default <number>,max <number>,minimum <number>,increment <number>, flag <string>, callback <function>)
local slider = sec:Slider("Slider", 0,25,0,2.5, function(t)
   print(t)
end)

--[[
slider:Set(state <number>)
]]

--sec:Dropdown(title <string>,options <table>,default <string>, flag <string>, callback <function>)
local dropdown = sec:Dropdown("Dropdown", {"a","b","c","d","e"},"", function(t)
   print(t)
end)

--[[
Dropdown:Refresh(options <table>, deletecurrent <boolean>)
Dropdown:Set(option <string>)
]]

--sec:MultiDropdown(title <string>,options <table>,default <table>, flag <string>, callback <function>)
local multidropdown =sec:MultiDropdown("Multi Dropdown", {"a","b","c","d","e"},{"b", "c"}, function(t)
   print(table.concat(t, ", "))
end)

--[[
Dropdown:Refresh(options <table>, deletecurrent <boolean>)
Dropdown:Set(option <table>)
]]

--sec:Colorpicker(title <string>, default <color3>, flag <string>, callback <function>)
sec:Colorpicker("Colorpicker", Color3.fromRGB(255,255,255), function(t)
   print(t)
end)

--sec:Textbox(title <string> ,disappear <boolean>, callback <function>)
sec:Textbox("Textbox", true, function(t)
   print(t)
end)

--sec:Bind(title <string>, default <keycode>, hold <boolean>, flag <string>, callback <function>)
sec:Bind("Hold Bind", Enum.KeyCode.E, true, function(t)
   print(t)
end)

sec:Bind("Normal Bind", Enum.KeyCode.F, false, function()
   print("Bind pressed")
end)

Label = sec:CreateLabel("Label")

--Label:UpdateLabel("New Title")
```
