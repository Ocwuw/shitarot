# shitarot
-- unresolved Luraph runtime helper; preserved as a safe stub
local function luraph_runtime1(...)
	return nil
end

-- unresolved Luraph runtime helper; preserved as a safe stub
local function luraph_runtime2(...)
	return nil
end

-- unresolved Luraph runtime helper; preserved as a safe stub
local function luraph_runtime3(...)
	return nil
end

-- unresolved Luraph runtime helper; preserved as a safe stub
local function luraph_runtime4(...)
	return nil
end

-- unresolved Luraph runtime helper; preserved as a safe stub
local function luraph_runtime5(...)
	return nil
end

-- unresolved Luraph runtime helper; preserved as a safe stub
local function luraph_runtime6(...)
	return nil
end

-- unresolved Luraph runtime helper; preserved as a safe stub
local function luraph_runtime7(...)
	return nil
end

-- unresolved Luraph runtime helper; preserved as a safe stub
local function luraph_runtime8(...)
	return nil
end

-- [DARKCODE] Bypassed key check / whitelist
if not game:IsLoaded() then
	pcall(function()
		game.Loaded:Wait()
	end)
end

local shkey = {
	alive = true,
	value = "SHITARO_BYPASS_KEY",
	reason = "KEY_VALID",
	open = function()
		return true
	end,
	stop = function()
		shkey.alive = false
	end,
	bind = function(...) end,
	watch = function() end,
}
getgenv().SHKEY = shkey
getgenv().SCRIPT_KEY = "SHITARO_BYPASS_KEY"
getgenv().JD_IS_PREMIUM = true
getgenv().JD_REASON = "KEY_VALID"

local rig = getgenv().rig

if type(rig) == "table" and type(rig.unload) == "function" then
	pcall(rig.unload)
end

local Players
Players = game:GetService("Players")
local RunService
RunService = game:GetService("RunService")
local ReplicatedStorage
ReplicatedStorage = game:GetService("ReplicatedStorage")
local UserInputService
UserInputService = game:GetService("UserInputService")
local Workspace
Workspace = game:GetService("Workspace")
game:GetService("Stats")
local Lighting
Lighting = game:GetService("Lighting")
local localPlayer
localPlayer = Players.LocalPlayer
local v, v2

do
	local function fn(arg)
		local request = rawget(getfenv(), "request") or syn and syn.request or http and http.request
		local request2

		if request then
			request2 = request
		else
			request2 = fluxus and fluxus.request
		end

		if not request2 then
			request2 = getgenv and (getgenv().request or getgenv().http_request)
		end

		if not request2 and type(http_request) == "function" then
			request2 = http_request
		end

		if type(request2) ~= "function" then
			request2 = function(opt)
				local ok, res = pcall(game.HttpGet, game, opt.Url)
				if ok and res then
					return { StatusCode = 200, Body = res, Headers = {} }
				end
				return { StatusCode = 500, Body = "" }
			end
		end
		local band = bit32.band
		local bxor = bit32.bxor
		local bnot = bit32.bnot
		local rrotate = bit32.rrotate
		local rshift = bit32.rshift
		local char = string.char
		local byte = string.byte
		local rep = string.rep
		local sub = string.sub
		local concat = table.concat
		local floor = math.floor

		local tbl = {
			1116352408,
			1899447441,
			3049323471,
			3921009573,
			961987163,
			1508970993,
			2453635748,
			2870763221,
			3624381080,
			310598401,
			607225278,
			1426881987,
			1925078388,
			2162078206,
			2614888103,
			3248222580,
			3835390401,
			4022224774,
			264347078,
			604807628,
			770255983,
			1249150122,
			1555081692,
			1996064986,
			2554220882,
			2821834349,
			2952996808,
			3210313671,
			3336571891,
			3584528711,
			113926993,
			338241895,
			666307205,
			773529912,
			1294757372,
			1396182291,
			1695183700,
			1986661051,
			2177026350,
			2456956037,
			2730485921,
			2820302411,
			3259730800,
			3345764771,
			3516065817,
			3600352804,
			4094571909,
			275423344,
			430227734,
			506948616,
			659060556,
			883997877,
			958139571,
			1322822218,
			1537002063,
			1747873779,
			1955562222,
			2024104815,
			2227730452,
			2361852424,
			2428436474,
			2756734187,
			3204031479,
			3329325298,
		}

		local function fn2(arg2)
			local n = #arg2
			local n2 = n * 8 % 4294967296
			local v3 = floor(n * 8 / 4294967296)
			local str = arg2
				.. "\128"
				.. rep("\0", (56 - (n + 1) % 64) % 64)
				.. char(
					floor(v3 / 16777216) % 256,
					floor(v3 / 65536) % 256,
					floor(v3 / 256) % 256,
					v3 % 256,
					floor(n2 / 16777216) % 256,
					floor(n2 / 65536) % 256,
					floor(n2 / 256) % 256,
					n2 % 256
				)
			local create = table.create and table.create(64, 0) or {}
			local n3 = 1779033703
			local n4 = 3144134277
			local n5 = 1013904242
			local n6 = 2773480762
			local n7 = 1359893119
			local n8 = 2600822924
			local n9 = 528734635
			local n10 = 1541459225

			for i = 1, #str, 64 do
				for i2 = 0, 15 do
					local n11 = i + i2 * 4
					create[i2 + 1] = byte(str, n11) * 16777216
						+ byte(str, n11 + 1) * 65536
						+ byte(str, n11 + 2) * 256
						+ byte(str, n11 + 3)
				end

				for i2 = 17, 64 do
					local v4 = create[i2 - 15]
					local v5 = create[i2 - 2]
					create[i2] = (
						create[i2 - 16]
						+ bxor(rrotate(v4, 7), rrotate(v4, 18), rshift(v4, 3))
						+ create[i2 - 7]
						+ bxor(rrotate(v5, 17), rrotate(v5, 19), rshift(v5, 10))
					) % 4294967296
				end

				local v4 = n7
				local v5 = n8
				local v6 = n9
				local v7 = n10
				local v8 = n3
				local v9 = n4
				local v10 = n5
				local v11 = n6

				for i2 = 1, 64 do
					local v12 = tbl[i2]
					local n11 = (
						v7
						+ bxor(rrotate(v4, 6), rrotate(v4, 11), rrotate(v4, 25))
						+ bxor(band(v4, v5), band(bnot(v4), v6))
						+ v12
						+ create[i2]
					) % 4294967296
					local n12 = (v11 + n11) % 4294967296
					local n13 = (
						n11
						+ (
								bxor(rrotate(v8, 2), rrotate(v8, 13), rrotate(v8, 22))
								+ bxor(band(v8, v9), band(v8, v10), band(v9, v10))
							)
							% 4294967296
					) % 4294967296
					v7 = v6
					v11 = v10
					v6 = v5
					v10 = v9
					v5 = v4
					v9 = v8
					v4 = n12
					v8 = n13
				end

				n3 = (n3 + v8) % 4294967296
				n4 = (n4 + v9) % 4294967296
				n5 = (n5 + v10) % 4294967296
				n6 = (n6 + v11) % 4294967296
				n7 = (n7 + v4) % 4294967296
				n8 = (n8 + v5) % 4294967296
				n9 = (n9 + v6) % 4294967296
				n10 = (n10 + v7) % 4294967296
			end

			local function fn3(arg3)
				return char(
					floor(arg3 / 16777216) % 256,
					floor(arg3 / 65536) % 256,
					floor(arg3 / 256) % 256,
					arg3 % 256
				)
			end

			return fn3(n3) .. fn3(n4) .. fn3(n5) .. fn3(n6) .. fn3(n7) .. fn3(n8) .. fn3(n9) .. fn3(n10)
		end

		local function fn3(arg2, arg3)
			local v3

			if #arg2 > 64 then
				v3 = fn2(arg2)
			else
				v3 = arg2
			end

			if #v3 < 64 then
				v3 ..= rep("\0", 64 - #v3)
			end

			local tbl2 = {}
			local tbl3 = {}

			for i = 1, 64 do
				local v4 = byte(v3, i)
				tbl2[i] = char(bxor(v4, 92))
				tbl3[i] = char(bxor(v4, 54))
			end

			return fn2(concat(tbl2) .. fn2(concat(tbl3) .. arg3))
		end

		local function fn4(arg2)
			local tbl2 = {}
			local n = #arg2
			local n2 = 1
			local n3 = 0

			while n2 <= n do
				local v3 = byte(arg2, n2)
				local v4 = byte(arg2, n2 + 1)
				local v5 = byte(arg2, n2 + 2)
				local n4 = v3 * 65536 + (v4 or 0) * 256 + (v5 or 0)
				local n5 = n3 + 1
				tbl2[n5] = sub(
					"ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789-_",
					floor(n4 / 262144) + 1,
					floor(n4 / 262144) + 1
				)
				n3 = n5 + 1
				tbl2[n3] = sub(
					"ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789-_",
					floor(n4 / 4096) % 64 + 1,
					floor(n4 / 4096) % 64 + 1
				)

				if v4 then
					n3 += 1
					tbl2[n3] = sub(
						"ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789-_",
						floor(n4 / 64) % 64 + 1,
						floor(n4 / 64) % 64 + 1
					)
				end

				if v5 then
					n3 += 1
					tbl2[n3] = sub(
						"ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789-_",
						n4 % 64 + 1,
						n4 % 64 + 1
					)
				end

				n2 += 3
			end

			return concat(tbl2)
		end

		local tbl2 = {}

		for i = 1, 64 do
			tbl2[sub("ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/", i, i)] = i - 1
		end

		local function fn5(arg2)
			local str = arg2:gsub("-", "+"):gsub("_", "/"):gsub("[^A-Za-z0-9+/=]", "")
			local str2 = str .. rep("=", (4 - #str % 4) % 4)
			local tbl3 = {}
			local n = 0

			for i = 1, #str2, 4 do
				local n2 = (tbl2[sub(str2, i, i)] or 0) * 262144
					+ (tbl2[sub(str2, i + 1, i + 1)] or 0) * 4096
					+ (tbl2[sub(str2, i + 2, i + 2)] or 0) * 64
					+ (tbl2[sub(str2, i + 3, i + 3)] or 0)
				n += 1
				tbl3[n] = char(floor(n2 / 65536) % 256)

				if sub(str2, i + 2, i + 2) ~= "=" then
					n += 1
					tbl3[n] = char(floor(n2 / 256) % 256)
				end

				if sub(str2, i + 3, i + 3) ~= "=" then
					n += 1
					tbl3[n] = char(n2 % 256)
				end
			end

			return concat(tbl3)
		end

		local function fn6(arg2)
			return (arg2:gsub("..", function(arg3)
				return char(tonumber(arg3, 16))
			end))
		end

		local v3 = fn6("02d417c2bd7b033a00d3c4e9fda43fc56761f68f516cf68a68a6110f2cb99e49")
		local v4 = Random.new(tick() * 1000000 % 2147483647 + os.time())

		local function fn7(arg2)
			local tbl3 = {}

			for i = 1, arg2 do
				tbl3[i] = char(v4:NextInteger(0, 255))
			end

			return concat(tbl3)
		end

		local function fn8(arg2)
			local tbl3 = {}

			for i = 8, 1, -1 do
				tbl3[i] = char(arg2 % 256)
				arg2 = floor(arg2 / 256)
			end

			return concat(tbl3)
		end

		local function fn9(arg2)
			return (
				string.gsub(arg2, "[^%w%-%._~/]", function(arg3)
					return string.format("%%%02X", string.byte(arg3))
				end)
			)
		end

		return (
			(function(arg2, arg3, arg4)
				local v5 = fn7(16)
				local v6 = fn8(os.time())
				local v7 =
					fn4(v5 .. v6 .. fn3(v3, "SHITARO-" .. arg3 .. "-REQ-v1\0" .. arg4 .. "\0" .. v5 .. "\0" .. v6))

				local ok, result = pcall(request2, {
					Url = arg2 .. fn9(arg4),
					Method = "GET",
					Headers = {
						["X-Shitaro-Token"] = v7,
						["User-Agent"] = "Roblox/WinInet",
						Accept = "*/*",
						["Cache-Control"] = "no-cache",
					},
				})

				if ok and type(result) == "table" and result.StatusCode == 200 then
					local body = result.Body
					if
						type(body) == "string"
						and #body > 50
						and not body:find("<!DOCTYPE")
						and not body:find("<html")
					then
						return body
					end
				end

				if type(game.HttpGet) == "function" then
					local ok2, body2 = pcall(game.HttpGet, game, arg2 .. fn9(arg4))
					if
						ok2
						and type(body2) == "string"
						and #body2 > 50
						and not body2:find("<!DOCTYPE")
						and not body2:find("<html")
					then
						return body2
					end
				end

				return nil
			end)("https://shitaro.lol/api/library/", "LIB", arg)
		)
	end

	-- [DARKCODE] Ported to Obsidian UI Library (https://github.com/deividcomsono/Obsidian)
	local ObsidianRepo = "https://raw.githubusercontent.com/deividcomsono/Obsidian/main/"
	local Obsidian = loadstring(game:HttpGet(ObsidianRepo .. "Library.lua"))()

	v = {
		pal = {
			accent = Color3.fromRGB(60, 140, 255),
			accent2 = Color3.fromRGB(40, 100, 200),
		},
	}

	function v.window(opt)
		local Window = Obsidian:CreateWindow({
			Title = opt.name or "shitaro.lol",
			Footer = "build: " .. tostring(opt.build or "beta"),
			NotifySide = "Right",
			ShowCustomCursor = false,
			AutoShow = true,
			Center = true,
		})

		local flags = {}
		local winObj = {
			flags = flags,
			gui = Obsidian.ScreenGui or game:GetService("CoreGui"):FindFirstChild("Obsidian") or Instance.new("Folder"),
			_window = Window,
		}

		function winObj:set_key(k)
			if type(k) == "string" and Enum.KeyCode[k] then
				Obsidian.ToggleKeybind = Enum.KeyCode[k]
			elseif typeof(k) == "EnumItem" then
				Obsidian.ToggleKeybind = k
			end
		end
		winObj:set_key(opt.key or "Z")

		local tabIcons = {
			rage = "crosshair",
			legit = "target",
			["anti aim"] = "shield",
			antiaim = "shield",
			visuals = "eye",
			movement = "wind",
			misc = "sliders",
			config = "settings",
			configs = "settings",
		}

		function winObj:tab(tCfg)
			local tName = tCfg.name or "Tab"
			local icon = tabIcons[tCfg.icon or tName:lower()] or "box"
			local Tab = Window:AddTab(tName, icon)
			local tabObj = { _tab = Tab }

			function tabObj:group(gName, side)
				local isRight = (side and string.lower(side) == "right")
				local Groupbox = isRight and Tab:AddRightGroupbox(gName) or Tab:AddLeftGroupbox(gName)

				if Groupbox and not Groupbox.AddColorPicker then
					function Groupbox:AddColorPicker(Idx, Info)
						local Label =
							self:AddLabel({ Text = Info.Title or Info.Text or tostring(Idx), DoesWrap = false })
						if Label and Label.AddColorPicker then
							return Label:AddColorPicker(Idx, Info)
						end
						return nil
					end
				end

				if Groupbox and not Groupbox.AddKeyPicker then
					function Groupbox:AddKeyPicker(Idx, Info)
						local Label = self:AddLabel({ Text = Info.Text or tostring(Idx), DoesWrap = false })
						if Label and Label.AddKeyPicker then
							return Label:AddKeyPicker(Idx, Info)
						end
						return nil
					end
				end

				local groupObj = { _box = Groupbox }

				function groupObj:toggle(tCfg)
					local flag = tCfg.flag or tCfg.name
					local def = tCfg.default or false
					flags[flag] = def
					local cb = tCfg.on

					local Toggle = Groupbox:AddToggle(flag, {
						Text = tCfg.name or flag,
						Default = def,
						Callback = function(val)
							flags[flag] = val
							if type(cb) == "function" then
								pcall(cb, val)
							end
						end,
					})

					local toggleObj = { _toggle = Toggle }
					local optionsMeta = {}

					optionsMeta.slider = function(self, sCfg)
						groupObj:slider(sCfg)
						return toggleObj
					end

					optionsMeta.toggle = function(self, subTCfg)
						groupObj:toggle(subTCfg)
						return toggleObj
					end

					optionsMeta.dropdown = function(self, dCfg)
						groupObj:dropdown(dCfg)
						return toggleObj
					end

					optionsMeta.colorpicker = function(self, cCfg)
						local cFlag = cCfg.flag or (flag .. ".color")
						local cDef = cCfg.default or Color3.fromRGB(255, 255, 255)
						local cCb = cCfg.on
						flags[cFlag] = setmetatable({ c = cDef }, {
							__index = function(_, k)
								return cDef[k]
							end,
						})

						pcall(function()
							Toggle:AddColorPicker(cFlag, {
								Title = cCfg.name or "Color",
								Default = cDef,
								Callback = function(col)
									flags[cFlag] = setmetatable({ c = col }, {
										__index = function(_, k)
											return col[k]
										end,
									})
									if type(cCb) == "function" then
										pcall(cCb, col)
									end
								end,
							})
						end)
						return toggleObj
					end

					optionsMeta.keyfield = function(self, kCfg)
						local kFlag = kCfg.flag or (flag .. ".key")
						local kDef = kCfg.default or "None"
						local kCb = kCfg.on
						flags[kFlag] = { key = kDef, mode = "Toggle" }

						pcall(function()
							Toggle:AddKeyPicker(kFlag, {
								Default = kDef,
								SyncToggleState = true,
								Mode = "Toggle",
								Text = kCfg.name or flag,
								Callback = function(val)
									flags[kFlag] = { key = tostring(val), mode = "Toggle" }
									if type(kCb) == "function" then
										pcall(kCb, { key = tostring(val) })
									end
								end,
							})
						end)
						return toggleObj
					end

					toggleObj.options = optionsMeta
					return toggleObj
				end

				function groupObj:slider(sCfg)
					local flag = sCfg.flag or sCfg.name
					local def = sCfg.default or sCfg.min or 0
					flags[flag] = def
					local cb = sCfg.on
					local rounding = (sCfg.float and sCfg.float < 1) and 2 or 0

					local Slider = Groupbox:AddSlider(flag, {
						Text = sCfg.name or flag,
						Min = sCfg.min or 0,
						Max = sCfg.max or 100,
						Default = def,
						Rounding = rounding,
						Suffix = sCfg.suffix or "",
						Callback = function(val)
							flags[flag] = val
							if type(cb) == "function" then
								pcall(cb, val)
							end
						end,
					})

					return {
						_slider = Slider,
						get = function(self)
							return flags[flag]
						end,
						set = function(self, val)
							pcall(function()
								Slider:SetValue(val)
							end)
						end,
					}
				end

				function groupObj:dropdown(dCfg)
					local flag = dCfg.flag or dCfg.name
					local def = dCfg.default
					local isMulti = (dCfg.multi == true)
					local cb = dCfg.on

					local function toMultiList(valMap)
						local res = {}
						if type(valMap) == "table" then
							for k, v in pairs(valMap) do
								if v == true then
									table.insert(res, k)
									res[k] = true
								end
							end
						end
						return res
					end

					if isMulti then
						local init = {}
						if type(def) == "table" then
							for _, item in ipairs(def) do
								init[item] = true
							end
						end
						flags[flag] = toMultiList(init)
					else
						flags[flag] = def or (dCfg.options and dCfg.options[1]) or ""
					end

					local Dropdown = Groupbox:AddDropdown(flag, {
						Text = dCfg.name or flag,
						Values = dCfg.options or {},
						Default = def,
						Multi = isMulti,
						Callback = function(val)
							if isMulti then
								flags[flag] = toMultiList(val)
								if type(cb) == "function" then
									pcall(cb, flags[flag])
								end
							else
								flags[flag] = val
								if type(cb) == "function" then
									pcall(cb, val)
								end
							end
						end,
					})

					local ddObj = {
						_dropdown = Dropdown,
						opened = function()
							return false
						end,
						reload = function(self, newOpts)
							pcall(function()
								Dropdown:SetValues(newOpts)
							end)
						end,
						set = function(self, val)
							pcall(function()
								Dropdown:SetValue(val)
							end)
						end,
						get = function(self)
							return flags[flag]
						end,
					}
					return ddObj
				end

				function groupObj:colorpicker(cCfg)
					local flag = cCfg.flag or cCfg.name
					local def = cCfg.default or Color3.fromRGB(255, 255, 255)
					flags[flag] = setmetatable({ c = def }, {
						__index = function(_, k)
							return def[k]
						end,
					})
					local cb = cCfg.on

					local Cp
					pcall(function()
						local Label = Groupbox:AddLabel({ Text = cCfg.name or flag, DoesWrap = false })
						if Label and Label.AddColorPicker then
							Cp = Label:AddColorPicker(flag, {
								Title = cCfg.name or flag,
								Default = def,
								Callback = function(col)
									flags[flag] = setmetatable({ c = col }, {
										__index = function(_, k)
											return col[k]
										end,
									})
									if type(cb) == "function" then
										pcall(cb, col)
									end
								end,
							})
						elseif Groupbox.AddColorPicker then
							Cp = Groupbox:AddColorPicker(flag, {
								Title = cCfg.name or flag,
								Default = def,
								Callback = function(col)
									flags[flag] = setmetatable({ c = col }, {
										__index = function(_, k)
											return col[k]
										end,
									})
									if type(cb) == "function" then
										pcall(cb, col)
									end
								end,
							})
						end
					end)

					return {
						_cp = Cp,
						set = function(self, col)
							pcall(function()
								if Cp and Cp.SetValueRGB then
									Cp:SetValueRGB(col)
								elseif Cp and Cp.SetValue then
									Cp:SetValue(col)
								end
							end)
						end,
						get = function(self)
							return flags[flag]
						end,
					}
				end

				function groupObj:keyfield(kCfg)
					local flag = kCfg.flag or kCfg.name
					local def = kCfg.default or "None"
					local cb = kCfg.on
					flags[flag] = { key = def, mode = "Toggle" }

					local Kp
					pcall(function()
						local Label = Groupbox:AddLabel({ Text = kCfg.name or flag, DoesWrap = false })
						if Label and Label.AddKeyPicker then
							Kp = Label:AddKeyPicker(flag, {
								Default = def,
								SyncToggleState = false,
								Mode = "Toggle",
								Text = kCfg.name or flag,
								Callback = function(val)
									flags[flag] = { key = tostring(val), mode = "Toggle" }
									if type(cb) == "function" then
										pcall(cb, { key = tostring(val) })
									end
								end,
							})
						elseif Groupbox.AddKeyPicker then
							Kp = Groupbox:AddKeyPicker(flag, {
								Default = def,
								SyncToggleState = false,
								Mode = "Toggle",
								Text = kCfg.name or flag,
								Callback = function(val)
									flags[flag] = { key = tostring(val), mode = "Toggle" }
									if type(cb) == "function" then
										pcall(cb, { key = tostring(val) })
									end
								end,
							})
						end
					end)

					return {
						_kp = Kp,
						set = function(self, k)
							pcall(function()
								if Kp and Kp.SetValue then
									Kp:SetValue({ tostring(k), "Toggle" })
								end
							end)
						end,
						get = function(self)
							return flags[flag]
						end,
					}
				end

				function groupObj:textbox(tCfg)
					local flag = tCfg.flag or tCfg.name
					local def = tCfg.default or ""
					flags[flag] = def
					local cur = def

					local Input = Groupbox:AddInput(flag, {
						Text = tCfg.name or flag,
						Default = def,
						Placeholder = tCfg.hint or "",
						Finished = false,
						Callback = function(val)
							cur = val
							flags[flag] = val
						end,
					})

					return {
						_input = Input,
						get = function(self)
							return cur
						end,
						set = function(self, val)
							cur = val
							pcall(function()
								Input:SetValue(val)
							end)
						end,
					}
				end

				function groupObj:button(bCfg)
					return Groupbox:AddButton({
						Text = bCfg.name or "Button",
						Func = function()
							if type(bCfg.on) == "function" then
								pcall(bCfg.on)
							end
						end,
					})
				end

				return groupObj
			end

			tabObj.section = tabObj.group
			return tabObj
		end

		function winObj:watermark(wCfg)
			local wmLabel
			pcall(function()
				if Obsidian.AddDraggableLabel then
					wmLabel = Obsidian:AddDraggableLabel({
						Text = wCfg.title or "shitaro.lol",
					})
					if wmLabel and wmLabel.SetVisible then
						wmLabel:SetVisible(false)
					end
				else
					Obsidian:SetWatermark(wCfg.title or "shitaro.lol")
					Obsidian:SetWatermarkVisibility(false)
				end
			end)
			return {
				toggle = function(self, v)
					pcall(function()
						if wmLabel and wmLabel.SetVisible then
							wmLabel:SetVisible(v == true)
						elseif Obsidian.SetWatermarkVisibility then
							Obsidian:SetWatermarkVisibility(v == true)
						end
					end)
				end,
			}
		end

		function winObj:keylist(kCfg)
			return {
				toggle = function(self, v)
					pcall(function()
						if Obsidian.KeybindFrame then
							Obsidian.KeybindFrame.Visible = (v == true)
						end
					end)
				end,
			}
		end

		local cfgFolder = "shitaro_configs"
		local cfgMem = {}
		local HttpService = game:GetService("HttpService")

		function winObj:configs()
			local list = {}
			if listfiles and isfolder and isfolder(cfgFolder) then
				local ok, files = pcall(listfiles, cfgFolder)
				if ok and type(files) == "table" then
					for _, f in ipairs(files) do
						local name = f:match("([^/\\]+)%.json$")
						if name then
							table.insert(list, name)
						end
					end
				end
			end
			if #list == 0 then
				for k in pairs(cfgMem) do
					table.insert(list, k)
				end
			end
			if #list == 0 then
				table.insert(list, "default")
			end
			return list
		end

		function winObj:save(name)
			if not name or name == "" then
				return false
			end
			local snap = {}
			for k, val in pairs(flags) do
				if typeof(val) == "Color3" then
					snap[k] = { __type = "Color3", r = val
