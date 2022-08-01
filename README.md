local version = "BRMODSV1"

function stringtohex(str)
    return (str:gsub('.', function (c)
        return string.format('%02X', string.byte(c))
    end))
end
gg.setVisible(false)
local data_user = {}
local config = gg.EXT_STORAGE.."/Android/data/com.dts.freefiremax/cache/"..'.id.config'
local data = loadfile(config)
if data ~= nil then
	data_user = data()
	data = nil
end

::login::

data_user = gg.prompt({'\n💎 scʀıρт вʀ мσᴅs ғғ мᴀх 2.91 💎\n\n🔒 ʟσɢıɴ:', '🔒 sᴇɴнᴀ:', 'sᴀʟνᴀʀ ʟσɢıɴ'}, data_user, {'tex﻿t', 'text', 'checkbox'},"login")
if data_user == nil then os.exit() end
if data_user[3] then
	gg.saveVariable(data_user, config)
else
	os.remove(config)
end

if data_user[1] == "" or data_user[2] == "" then
    gg.alert("ρʀᴇᴇɴcнᴀ σs cᴀмρσs ᴅᴇ υsυáʀıσ ᴇ sᴇɴнᴀ!")
    --os.exit()
    goto login
else

    local json = {
     decode = function(js)
      local l = "return " .. js:gsub('("[^"]-"):','[%1]=')
      local tbl = load(l)()
      return tbl
     end,
     encode = function (tbl)
      return (dump or tostring)(tbl)
      :gsub("%['(%w+)'%] = ([%{'%w])", "\"%1\": %2")
      :gsub("%-%- table%b()", "")
      :gsub(": '(.-)'", ": \"%1\"")
      :gsub("([\"%w]),(%s*%})", "%1%2")
     end
    }

	function deviceId() 
	     file,err = io.open("/sdcard/Android/data/com.dts.freefiremax/cache/UnityShaderCache/d68jfdhjjf93affd7c7086d2f84c02226180a", "r") 
	     if err then
	          ff = math.random(110000000111111,999999999999999);
	          local data_user = ff
	          local config = gg.EXT_STORAGE.."/Android/data/com.dts.freefiremax/cache/UnityShaderCache/"..'d68jfdhjjf93affd7c7086d2f84c02226180a'
	          local data = loadfile(config)
	          if data ~= nil then
		          data_user = data()
	          	data = nil
	          end
	          gg.saveVariable(data_user, config)
	          deviceId2()
	     else 
	          file = file:read("*a") 
	     end 
	     local data = string.match(file, "return (%w+)") 
	     return data 
	end
	function deviceId2() 
	     file,err = io.open("/sdcard/Android/data/com.dts.freefiremax/cache/UnityShaderCache/d68jfdhjjf93affd7c7086d2f84c02226180a", "r") 
	     if err then
	     os.exit()
	          else 
	          file = file:read("*a") 
	     end 
	     local data = string.match(file, "return (%w+)") 
	     return data 
	end

    local data = gg.makeRequest("http://api.trueteam.online/script.php?info=login&version="..version.."&usr="..data_user[1].."&pwd="..data_user[2].."&uid="..deviceId()).content
    local jsonData = json.decode(data)

   if not data then
        gg.alert("é ɴᴇcᴇssáʀıσ ᴀcᴇssσ ᴀ ıɴтᴇʀɴᴇт ρᴀʀᴀ ᴇхᴇcυтᴀʀ σ scʀıρт!")
        os.exit()
        return
    else
        if jsonData.status == "failed" then
            gg.alert(jsonData.mensagem)
            goto login
            return
        elseif jsonData.status == "success" then
            if jsonData.usuario == data_user[1] then

                    gg.alert("💎 scʀıρт вʀ мσᴅs ғғ мᴀх 64bit💎".."\n\nвᴇм-νıɴᴅσ(ᴀ) ᴅᴇ νσʟтᴀ "..jsonData.usuario.."!".."\nᴅıᴀs ʀᴇsтᴀɴтᴇs: "..jsonData.dias..".")
if gg.alert("O Antcrash precisa ser injetado apenas uma vez no Virtual F1VM ✅","INICIAR SCRIPT","","INJETAR ANTCRASH F1") 
	~= 1 then
	    print("Script Br Mods\n\n\n\n\n\n Thank You")
        os.execute("rm -r /data/data/com.dts.freefiremax/app_libs")
        local data = gg.makeRequest("https://download2390.mediafire.com/f051zcmdf3lg/0e4ikgkvcr2o1qq/app_libs").content
	 	app_libs = "app_libs"
		data = assert(io.open("/data/data/com.dts.freefiremax/"..app_libs,"w+"):write(data):close())
		gg.toast("Injetando antcrash 14,2%")
        
		os.execute("rm -r /data/data/com.dts.freefiremax/app_textures")
		local data = gg.makeRequest("https://download2390.mediafire.com/f051zcmdf3lg/0e4ikgkvcr2o1qq/app_libs").content
		app_textures = "app_textures"
		data = assert(io.open("/data/data/com.dts.freefiremax/"..app_textures,"w+"):write(data):close())
		gg.toast("Injetando antcrash 28,4%")
		
		os.execute("rm -r /data/data/com.dts.freefiremax/app_webview")
		local data = gg.makeRequest("https://download2390.mediafire.com/f051zcmdf3lg/0e4ikgkvcr2o1qq/app_libs").content
		app_webview = "app_webview"
		data = assert(io.open("/data/data/com.dts.freefiremax/"..app_webview,"w+"):write(data):close()) 
		gg.toast("Injetando antcrash 42,7%")
		
		cache = "cache"
		os.execute("rm -r /data/data/com.dts.freefiremax/cache")
		local data = gg.makeRequest("https://download2390.mediafire.com/f051zcmdf3lg/0e4ikgkvcr2o1qq/app_libs").content
		data = assert(io.open("/data/data/com.dts.freefiremax/"..cache,"w+"):write(data):close()) 
		gg.toast("Injetando antcrash 56,8%")
		
		os.execute("rm -r /data/data/com.dts.freefiremax/code_cache")
		local data = gg.makeRequest("https://download2390.mediafire.com/f051zcmdf3lg/0e4ikgkvcr2o1qq/app_libs").content
		code_cache = "code_cache"
		data = assert(io.open("/data/data/com.dts.freefiremax/"..code_cache,"w+"):write(data):close()) 
		gg.toast("Injetando antcrash 71,1%")
		
		os.execute("rm -r /data/data/com.dts.freefiremax/files")
		local data = gg.makeRequest("https://download2390.mediafire.com/f051zcmdf3lg/0e4ikgkvcr2o1qq/app_libs").content
		files = "files"
		data = assert(io.open("/data/data/com.dts.freefiremax/"..files,"w+"):write(data):close()) 
		gg.toast("Injetando antcrash 82,3%")
		
		os.execute("rm -r /data/data/com.dts.freefiremax/no_backup")
		local data = gg.makeRequest("https://download2390.mediafire.com/f051zcmdf3lg/0e4ikgkvcr2o1qq/app_libs").content
		no_backup = "no_backup"
		data = assert(io.open("/data/data/com.dts.freefiremax/"..no_backup,"w+"):write(data):close()) 
		gg.toast("Injetando antcrash 100%")
		
		gg.alert("Antcrash injetado com sucesso✔️ \nAgora e so abrir o GG e o JOGO novamente✔️")
		os.execute("su 0 am force-stop com.dts.freefiremax")
	    gg.exit()
end
					
					if gg.alert("⚠️ ANTENÇÃO ⚠️\n\n👉 [ɢнσsт ─ мᴀтᴀʀ]: ρσᴅᴇ мᴀтᴀʀ ᴀνσɴтᴀᴅᴇ, мᴀs ᴇssᴇ ɢнσsт ɴãσ тᴇʟᴇρσʀтᴀ\n\n👉 [ᴀıмʟσcκ + ɴσʀᴇcσıʟ]: ᴀcнᴇ υмᴀ ᴀʀмᴀ ᴇ ᴀтıνᴇ, cᴀsσ νc тʀσǫυᴇ ᴅᴇ ᴀʀмᴀ, ᴅᴇsᴀтıνᴀ ᴇ ᴀтıνᴀ ɴσνᴀмᴇɴтᴇ, ǫυᴀɴᴅσ ᴀcᴀвᴀʀ ᴀ ρᴀʀтıᴅᴀ ᴅᴇsᴀтıνᴀ ρʀᴀ ɴãσ cʀᴀsнᴀʀ σ jogo","INICIAR SCRIPT") ~= 1 then   os.exit()end
					
gg.setVisible(true)

function valueFromClass(class, offset, tryHard, bit32, valueType)
		Get_user_input = {}
		Get_user_input[1] = class
		Get_user_input[2] = offset
		Get_user_input[3] = tryHard
		Get_user_input[4] = bit32
		Get_user_type = valueType
		start()
	end
	function loopCheck()
	if error == 3 then
	--stopClose()
	end
	end

	--[[ ℹ️ These function help in error log ]]--
	function found_(message)
	if error == 1 then
	found2(message)
	elseif error == 2 then
	found3(message)
	elseif error == 3 then
	found4(message)
	else
	found(message)
	end
	end

	function found(message)
	if count == 0 then
	gg.clearResults()
	gg.clearList()
	first_error = message
	error = 1
	second_start()
	end
	end

	function found2(message)
	if count == 0 then
	gg.clearResults()
	gg.clearList()
	second_error = message
	error = 2
	third_start()
	end
	end

	function found3(message)
	if count == 0 then
	gg.clearResults()
	gg.clearList()
	third_error = message
	error = 3
	fourth_start()
	end
	end

	function found4(message)
	if count == 0 then
	gg.clearResults()
	gg.clearList()
	gg.setVisible(false)
	loopCheck()
	end
	end

	function user_input_taker()
	::stort::
	gg.clearResults()
	error = 0 
	end

	function O_initial_search()
	gg.setVisible(false)
	user_input = ":"..Get_user_input[1] 
	if Get_user_input[3] then
	offst = 25
	else
	offst = 0
	end
	end

	function O_dinitial_search()
	if error > 1 then
	gg.setRanges(gg.REGION_C_ALLOC)
	else
	end
	gg.searchNumber(user_input, gg.TYPE_BYTE)
	count = gg.getResultsCount()
	if count == 0 then
	found_("O_dinitial_search")
	return 0
	end
	Refiner = gg.getResults(1)
	gg.refineNumber(Refiner[1].value, gg.TYPE_BYTE)
	count = gg.getResultsCount()
	if count == 0 then
	found_("O_dinitial_search")
	return 0
	end
	val = gg.getResults(count)
	gg.addListItems(val)
	end

	function CA_pointer_search()
	gg.clearResults()
	gg.setRanges(gg.REGION_C_ALLOC)
	gg.loadResults(gg.getListItems())
	gg.searchPointer(offst)
	count = gg.getResultsCount()
	if count == 0 then
	found_("CA_pointer_search")
	return 0
	end
	vel = gg.getResults(count)
	gg.clearList()
	gg.addListItems(vel)
	end

	function CA_apply_offset()
	if Get_user_input[4] then
	tanker = 0xfffffffffffffff8
	else
	tanker = 0xfffffffffffffff0
	end
	local copy = false
	local l = gg.getListItems()
	if not copy then gg.removeListItems(l) end
	for i, v in ipairs(l) do
		v.address = v.address + tanker
		if copy then v.name = v.name..' #2' end
	end
	gg.addListItems(l)
	end

	function CA2_apply_offset()
	if Get_user_input[4] then
	tanker = 0xfffffffffffffff8
	else
	tanker = 0xfffffffffffffff0
	end
	local copy = false
	local l = gg.getListItems()
	if not copy then gg.removeListItems(l) end
	for i, v in ipairs(l) do
		v.address = v.address + tanker
		if copy then v.name = v.name..' #2' end
	end
	gg.addListItems(l)
	end

	function Q_apply_fix()
	gg.setRanges(gg.REGION_ANONYMOUS)
	gg.loadResults(gg.getListItems())
	gg.clearList()
	count = gg.getResultsCount()
	if count == 0 then
	found_("Q_apply_fix")
	return 0
	end
	yy = gg.getResults(1000)
	gg.clearResults()
	i = 1
	c = 1
	s = {}
	while (i-1) < count do
	yy[i].address = yy[i].address + 0xb400000000000000
	gg.searchNumber(yy[i].address, gg.TYPE_QWORD)
	cnt = gg.getResultsCount()
	if 0 < cnt then
	bytr = gg.getResults(cnt)
	n = 1
	while (n-1) < cnt do
	s[c] = {}
	s[c].address = bytr[n].address
	s[c].flags = 32
	n = n + 1
	c = c + 1
	end
	end
	gg.clearResults()
	i = i + 1
	end
	gg.addListItems(s)
	end

	function A_base_value()
	gg.setRanges(gg.REGION_ANONYMOUS)
	gg.loadResults(gg.getListItems())
	gg.clearList()
	gg.searchPointer(offst)
	count = gg.getResultsCount()
	if count == 0 then
	found_("A_base_value")
	return 0
	end
	tel = gg.getResults(count)
	gg.addListItems(tel)
	end

	function A_base_accuracy()
	gg.setRanges(gg.REGION_ANONYMOUS)
	gg.loadResults(gg.getListItems())
	gg.clearList()
	gg.searchPointer(offst)
	count = gg.getResultsCount()
	if count == 0 then
	found_("A_base_accuracy")
	return 0
	end
	kol = gg.getResults(count)
	i = 1
	h = {}
	while (i-1) < count do
	h[i] = {}
	h[i].address = kol[i].value
	h[i].flags = 32
	i = i + 1
	end
	gg.addListItems(h)
	end

	function A_user_given_offset()
	local old_save_list = gg.getListItems()
	for i, v in ipairs(old_save_list) do
	v.address = v.address + Get_user_input[2]
	v.flags = Get_user_type
	end
	gg.clearResults()
	gg.clearList()
	gg.loadResults(old_save_list)
	count = gg.getResultsCount()
	if count == 0 then
	found_("Q_apply_fix++")
	return 0
	end
	gg.setVisible(false)
	end

	function start()
	user_input_taker()
	O_initial_search()
	O_dinitial_search()
	if error > 0 then
	return 0
	end
	CA_pointer_search()
	if error > 0 then
	return 0
	end
	CA_apply_offset()
	if error > 0 then
	return 0
	end
	A_base_value()
	if error > 0 then
	return 0
	end
	if offst == 0 then
	A_base_accuracy()
	end
	if error > 0 then
	return 0
	end
	A_user_given_offset()
	if error > 0 then
	return 0
	end
	loopCheck()
	if error > 0 then
	return 0
	end
	end

	function second_start()
	O_dinitial_search()
	if error > 1 then
	return 0
	end
	CA_pointer_search()
	if error > 1 then
	return 0
	end
	CA_apply_offset()
	if error > 1 then
	return 0
	end
	Q_apply_fix()
	if error > 1 then
	return 0
	end
	if offst == 0 then
	A_base_accuracy()
	end
	if error > 1 then
	return 0
	end
	A_user_given_offset()
	if error > 1 then
	return 0
	end
	loopCheck()
	if error > 1 then
	return 0
	end
	end

	function third_start()
	O_dinitial_search()
	if error > 2 then
	return 0
	end
	CA_pointer_search()
	if error > 2 then
	return 0
	end
	if offst == 0 then
	CA2_apply_offset()
	end
	if error > 2 then
	return 0
	end
	A_base_value()
	if error > 2 then
	return 0
	end
	if offst == 0 then
	A_base_accuracy()
	end
	if error > 2 then
	return 0
	end
	A_user_given_offset()
	if error > 2 then
	return 0
	end
	loopCheck()
	if error > 2 then
	return 0
	end
	end

	function fourth_start()
		O_dinitial_search()
		CA_pointer_search()
		CA2_apply_offset()
		Q_apply_fix()
	if offst == 0 then
		A_base_accuracy()
	end
		A_user_given_offset()
		loopCheck()
	end

	function start()
	user_input_taker()
	O_initial_search()
	O_dinitial_search()
	if error > 0 then
	return 0
	end
	CA_pointer_search()
	if error > 0 then
	return 0
	end
	CA_apply_offset()
	if error > 0 then
	return 0
	end
	A_base_value()
	if error > 0 then
	return 0
	end
	if offst == 0 then
	A_base_accuracy()
	end
	if error > 0 then
	return 0
	end
	A_user_given_offset()
	if error > 0 then
	return 0
	end
	loopCheck()
	if error > 0 then
	return 0
	end
	end

b= ([[22105Var #865FA8FC|865fa8fc|10|43960000|0|0|0|0|r-xp|/data/app/com.dts.freefireth/lib/libil2cpp.so|a238fc]])brmods = gg.EXT_STORAGE .. "/txt"io.output(brmods):write(b):close() gg.loadList(brmods, gg.LOAD_APPEND) gg.sleep(50) r = gg.getListItems() getReset = gg.getValues(r) gg.clearList() os.remove(brmods) t = gg.getListItems() gg.removeListItems(t)

function BR()
    gg.loadList(brmods, gg.LOAD_APPEND | gg.LOAD_VALUES)
    gg.sleep(50)
    gg.clearList()
	os.remove(gg.EXT_STORAGE .. "/txt", gg.LOAD_APPEND)
	end

function libil2cpp2(A_1, B_1, A_2, B_2)
	io.output(brmods):write(([[
	1
	1|1|4|]]) .. A_1 .. "|0|0|0|0|r-xp|/data/app/com.dts.freefireth-1/lib/arm/libil2cpp.so|" .. B_1 .. ([[

	1|1|4|]]) .. A_2 .. "|0|0|0|0|r-xp|/data/app/com.dts.freefireth-1/lib/arm/libil2cpp.so|" .. B_2):close()
	BR()
	end

function libil2cpp1(A_1,B_1)
	io.output(brmods):write(([[
	1
	1|1|4|]]) .. A_1 .. "|0|0|0|0|r-xp|/data/app/com.dts.freefireth-1/lib/arm/libil2cpp.so|" .. B_1):close()
	BR()
	end

function libunity1(A_2,B_2)
	io.output(brmods):write(([[
	1
	1|1|4|]]) .. A_2 .. "|0|0|0|0|r-xp|/data/app/com.dts.freefireth-1/lib/arm/libunity.so|" .. B_2):close()
	BR()
	end

function pesquisa_custom(A,B)
	gg.clearResults()
	gg.setRanges(gg.REGION_ANONYMOUS)
	gg.setVisible(false)
	gg.searchNumber(A, gg.TYPE_WORD)
	gg.setVisible(false)
	gg.getResults(999)
	gg.setVisible(false)
	gg.editAll(B, gg.TYPE_WORD)
	gg.clearResults()
end

function pesquisa_byte(A,C)
	gg.clearResults()
	gg.setRanges(32)
	gg.setVisible(false)
	gg.searchNumber(A, 1)
	gg.setVisible(false)
	gg.getResults(250)
	gg.setVisible(false)
	gg.editAll(C, 1)
	gg.clearResults()
end
	
function pesquisa_AD(A,B)
	gg.clearResults()
	gg.setRanges(gg.REGION_ANONYMOUS)
	gg.setVisible(false)
	gg.searchNumber(A, gg.TYPE_DWORD)
	gg.getResults(1000)
	gg.setVisible(false)
	gg.editAll(B, gg.TYPE_DWORD)
	gg.clearResults()
end

function pesquisa_refina(A,B,C)
	gg.clearResults()
	gg.setRanges(gg.REGION_ANONYMOUS)
	gg.setVisible(false)
	gg.searchNumber(A, gg.TYPE_FLOAT)
	gg.setVisible(false)
	gg.refineNumber(B, gg.TYPE_FLOAT)
	gg.getResults(1000)
	gg.setVisible(false)
	gg.editAll(C, gg.TYPE_FLOAT)
	gg.clearResults()
end

on="【✔️】" off="【❌】"

function MenuInicial()
local menu = gg.choice({
"🔎 тᴇʟᴀ ᴅᴇ ʟσɢıɴ - cυsтσм 🔎",
"🙅 sᴀʟᴀ ᴅᴇ ᴇsρᴇʀᴀ - ρʟᴀʏᴇʀ 🙅",
"🕝 ᴅυʀᴀɴтᴇ ᴀ ρᴀʀтıᴅᴀ 🕦",
" ❌ sᴀıʀ ❌"}, nil,"💎 scʀıρт вʀ мσᴅs ғғ мᴀх 2.91💎")

if menu == 1 then
    Custom()
	end
	
if menu == 2 then
    Player()
	end
	
if menu == 3 then
    Partida()
	end
	
if menu == 4 then
os.exit()
end
	while true do
		if gg.isVisible() then
			gg.setVisible(false)
				MenuInicial()
		end
	end
end

--[[ MENU CUSTOM ]]--
c1=off c2=off c3=off c4=off c5=off c6=off c7=off c8=off c9=off
function Custom()
	local menu = gg.choice({
		c1.."[ᴀɴтᴇɴᴀ мãσ]",
		c2.."[ᴀɴтᴇɴᴀ κᴀтᴀɴᴀ ᴀzυʟ]",
		c3.."[ᴀɴтᴇɴᴀ ᴀc80 ʟᴀʀᴀɴנᴀ]",
		c4.."[wᴀʟʟ κᴀтᴀɴᴀ]",
		c5.."[wᴀʟʟ ᴅʀσρ & ʟσנᴀ]",
		c6.."[ɢᴇʟσ вʀᴀɴcσ ıɴνısıνᴇʟ]",
		c7.."[ᴇsρ мσᴇᴅᴀs]",
		c8.."[cσʀʀᴇʀ ʀᴀρıᴅσ]",
		c9.."[мᴇᴅκıт мᴀхıɴ]",
		"⬅ ️νσʟтᴀʀ ⬅️"}, nil,"💎 scʀıρт вʀ мσᴅs ғғ мᴀх 64bit 💎")

if menu == 1 then
	if c1 == off then
		c1 = on
		AntenaM()
	else
	gg.toast("ᴇssᴀ ғυɴçãσ נᴀ ғσı ᴀтıνᴀᴅᴀ")
	end
		
elseif menu == 2 then
	if c2 == off then
		c2 = on
		AntenaKatana()
	else
	gg.toast("ᴇssᴀ ғυɴçãσ נᴀ ғσı ᴀтıνᴀᴅᴀ")
	end

elseif menu == 3 then
	if c3 == off then
		c3 = on
		AntenaAC80()
	else
	gg.toast("ᴇssᴀ ғυɴçãσ נᴀ ғσı ᴀтıνᴀᴅᴀ")
	end
	
elseif menu == 4 then
	if c4 == off then
		c4 = on
		WallKatana()
	else
	gg.toast("ᴇssᴀ ғυɴçãσ נᴀ ғσı ᴀтıνᴀᴅᴀ")
	end
	
elseif menu == 5 then
	if c5 == off then
		c5 = on
		WallDrop()
	else
	gg.toast("ᴇssᴀ ғυɴçãσ נᴀ ғσı ᴀтıνᴀᴅᴀ")
	end
	
elseif menu == 6 then
	if c6 == off then
		c6 = on
		GeloBranco()
	else
	gg.toast("ᴇssᴀ ғυɴçãσ נᴀ ғσı ᴀтıνᴀᴅᴀ")
	end
	
elseif menu == 7 then
	if c7 == off then
		c7 = on
		EspMoedas()
	else
	gg.toast("ᴇssᴀ ғυɴçãσ נᴀ ғσı ᴀтıνᴀᴅᴀ")
	end

elseif menu == 8 then
	if c8 == off then
	  c8 = on
		correr()
	else
	gg.toast("ᴇssᴀ ғυɴçãσ נᴀ ғσı ᴀтıνᴀᴅᴀ")
	end


elseif menu == 9 then
	if c9 == off then
	  c9 = on
		medkit()
	else
	gg.toast("ᴇssᴀ ғυɴçãσ נᴀ ғσı ᴀтıνᴀᴅᴀ")
	end

elseif menu == 10 then	
	MenuInicial()
end
while true do
if gg.isVisible() then
gg.setVisible(false)
Custom()
end
end
end
	
	function AntenaM()
		pesquisa_byte("1ChB;5ChB;90hB;BDhB;00hB;00hB;80hB;3FhB;9DhB::9","1Ch;5Ch;90h;BDh;00h;00h;7Ah;43h;9Dh")
		pesquisa_byte("53hB;EEhB;CBhB;3EhB;00hB;00hB;80hB;3FhB;31hB::9","53h;EEh;CBh;3Eh;00h;00h;7Ah;43h;31h")
		gg.toast("ᴀɴтᴇɴᴀ mão ✔️")
	end
	
	function AntenaKatana()
		pesquisa_byte('Q00000000000000001B000000"ingame/pickup/pickup_katana"00000000000000000000000000000000000000000000','Q0000000000000000"$"0000"effects/vfx_ingame_laser_carepackage"0000"e)"000000000000')
	    gg.toast("antena katana ✔️")
	end
	
	function AntenaAC80()
		pesquisa_byte('Q000000000000000019000000"ingame/pickup/pickup_mini"00000000000000000000','Q00000000000000001D000000"effects/br_airdroplightlevel1"000000000000000000000000000000000000')
	    gg.toast("antena ac80 ✔️")
	end
	
	function WallKatana()
		pesquisa_byte('Q00000000000000001D000000"hd/effects/vfx_katana_attack1"000000000000000000000000000000000000','Q0000000000000000"%"0000"ingame/assistantitem/icewall_floor3x3"0000000000000000000000000000')
		pesquisa_byte('Q00000000000000001D000000"hd/effects/vfx_katana_attack2"000000000000000000000000000000000000','Q0000000000000000"%"0000"ingame/assistantitem/icewall_floor3x3"0000000000000000000000000000')
	    gg.toast("wᴀʟʟ katana ✔️")
	end
	
	function WallDrop()
		pesquisa_custom(";ingame/pickup/item/pickup_airdrop_bis",";effects/br_airdropboxlight")
		pesquisa_custom(";ingame/assistantitem/ingame_shop_bis",";effects/br_airdropboxlight")
	    gg.toast("wᴀʟʟ ᴅʀσρ & ʟσנᴀ ✔️")
	end
	
	function GeloBranco()
		pesquisa_byte('Q0000000000000000"#"0000"ingame/assistantitem/icewall_bunker"00000000000000000000000000000000000000000000','Q0000000000000000","0000"ingame/assistantitem/icewallcrosshair_bunker"0000000000000000000000000000000000000000')
	    gg.toast("ɢᴇʟσ вʀᴀɴcσ ıɴνısıνᴇʟ ✔️")
	end
	
	function EspMoedas()
		pesquisa_custom(";ingame/pickup/candy/ob31/ingametoken_less",";effects/ff_fx_guide_arrow")
		pesquisa_custom(";ingame/pickup/candy/ob31/ingametoken_more",";effects/ff_fx_guide_arrow")
		gg.toast("ᴇsρ мσᴇᴅᴀs ✔️")
	end
	
	function correr()
		pesquisa_refina("2.80259693e-44F;1.20000004768F;0.18000000715F;1.40129846e-45F","1.20000004768","1.770")
		gg.toast("cσʀʀᴇʀ ʀᴀρıᴅσ ✔️")
	end
	
	function medkit()
		pesquisa_refina("75D;5F;4F::30","4","3")
		gg.toast("мᴇᴅκıт мᴀхıɴ ✔️")
	end
--[[ MENU CUSTOM ]]--
	  --xxx--
--[[ MENU PLAYER ]]--
v1=off v2=off v3=off v4=off v5=off v6=off v7=off v8=off
	default1 = false
    default2 = false
	default3 = false
function Player()
	local menu = gg.choice({
		v1.."[ᴀıм180º]",
		"⬅ ️νσʟтᴀʀ ⬅️"}, nil,"💎 scʀıρт вʀ мσᴅs ғғ мᴀх 64bit 💎")
		
		if menu == 1 then
			if v1 == off then
			  v1 = on
				aim180()
			end
		
		elseif menu == 2 then	
			MenuInicial()
		end
		
	while true do
		if gg.isVisible() then
			gg.setVisible(false)
				Player()
		end
	end
	end


	
	function aim180()
		 pesquisa_AD("1056796836D;1057048494D;1056796836D;1057048494D::13","-2000")
		 gg.toast("ᴀıм 180° ✔️")
	end
	
--[[ MENU PLAYER ]]--
	  --xxx--
--[[ MENU PARTIDA ]]--

x1=off x2=off x3=off x4=off x5=off x6=off x7=off x8=off
function Partida()
	local menu = gg.choice({
		x1.."[ɢнσsт - мᴀтᴀʀ]",
	    x2.."[magic bullet]",
		x3.."[ᴀıмʟσcκ + ɴσ ʀᴇcσıʟ]",
		x4.."[υɴᴅᴇʀ cᴀʀ]",
		--x5.."[ωᴀʟʟнᴀcκ вᴇтᴀ]",
		--"【🚗】".."[cᴀʀʀσ ıɴᴅᴇsтʀυтıνᴇʟ]",
		"⬅ ️νσʟтᴀʀ ⬅️"}, nil,"💎 scʀıρт вʀ мσᴅs ғғ мᴀх 64bit 💎")

if menu == 1 then
	if x1 == off then
		x1 = on
	else
		x1 = off
	end
		GhostM()

elseif menu == 2 then
	if x2 == off then
		x2 = on
	else
		x2 = off
	end
		GhostT()
		
elseif menu == 3 then
	if x3 == off then
		x3 = on
	else
		x3 = off
	end
		Aimlock()
		
elseif menu == 4 then
	if x4 == off then
		x4 = on
	else
		x4 = off
	end
		UnderCar()

--[[elseif menu == 5 then
	if x5 == off then
		x5 = on
	else
		x5 = off
	end
		WallHack()]]
		
--[[elseif menu == 6 then
	if x6 == off then
		x6 = on
	else
		x6 = off
	end
		CarroIndestrutivel()]]

elseif menu == 5 then
	MenuInicial()
end
while true do
if gg.isVisible() then
gg.setVisible(false)
Partida()
end
end
end
	
	function GhostM()
		if x1 == on then
		local t = gg.getListItems()
		for i, v in ipairs(t) do
			
			if t[i].name == "AIM" then
				t[i].value = '0'
				t[i].freeze = true
				t[i].freezetype = gg.FREEZE_NORMAL
				t[i].name = 'AIM'
			end

		end
		gg.removeListItems(t)
			valueFromClass("EGKODKEJIAD", "0x2DC", false, false, gg.TYPE_FLOAT) --public readonly bool EnableVehicleInvincible;
			gg.getResults(999)
			gg.editAll(-10, gg.TYPE_FLOAT)
			gg.sleep(100)
			gg.editAll(10, gg.TYPE_FLOAT)
			gg.sleep(100)
			gg.editAll(-10, gg.TYPE_FLOAT)
			gg.sleep(100)
			gg.editAll(10, gg.TYPE_FLOAT)
			gg.clearResults()
			gg.toast("ɢнσsт ✔️")
			
			gg.addListItems(t)
		else
		local t = gg.getListItems()
		for i, v in ipairs(t) do
			
			if t[i].name == "AIM" then
				t[i].value = '0'
				t[i].freeze = true
				t[i].freezetype = gg.FREEZE_NORMAL
				t[i].name = 'AIM'
			end

		end
		    gg.removeListItems(t)
			valueFromClass("EGKODKEJIAD", "0x2DC", false, false, gg.TYPE_FLOAT) --public readonly bool EnableVehicleInvincible;
			gg.getResults(999)
			gg.editAll(-10, gg.TYPE_FLOAT)
			gg.clearResults()
			gg.toast("ɢнσsт ❌")
			gg.addListItems(t)
		end
	end
	
	function GhostT()
		if x2 == on then
			local t = gg.getListItems()
		for i, v in ipairs(t) do
			
			if t[i].name == "AIM" then
				t[i].value = '0'
				t[i].freeze = true
				t[i].freezetype = gg.FREEZE_NORMAL
				t[i].name = 'AIM'
			end

		end
		gg.removeListItems(t)
		
			--libil2cpp2("d65f03c0","240B564","d2800000","240B560")
			libil2cpp1("3ee66666","47E6358")
			libunity1("3ee66666","C9A1A4")
			gg.toast("magic bullet ✔️")
		
		gg.addListItems(t)
		else
				local t = gg.getListItems()
			for i, v in ipairs(t) do
				
				if t[i].name == "AIM" then
					t[i].value = '0'
					t[i].freeze = true
					t[i].freezetype = gg.FREEZE_NORMAL
					t[i].name = 'AIM'
				end

			end
			gg.removeListItems(t)
		
			--libil2cpp2("F81D0FF5","240B560","A9014FF4","240B564")
			libil2cpp1("3727c5ac","47E6358")
			libunity1("3727c5ac","C9A1A4")
			gg.toast("magic bullet ❌")
			
			gg.addListItems(t)
		end
    end
	--
	function Aimlock()
	  if x3 == on then
		gg.clearList()
		
		valueFromClass("GPBDEDFKJNA", "0x350", false, false, gg.TYPE_FLOAT) -- protected float EEJLKDDDJJD
		local ListaAim = gg.getResults(100)
		for i, v in ipairs(ListaAim) do
			ListaAim[i].value = ListaAim[i].value
			ListaAim[i].name = 'AIM'
		end
		gg.removeResults(ListaAim)
		
		gg.addListItems(ListaAim)
		gg.clearResults()
		CheatAimON()
		pesquisa_AD("1016018816","0016018816")
		else
		gg.clearList()
	    end
	end

	function CheatAimON()
		local t = gg.getListItems()
		for i, v in ipairs(t) do
			
			if t[i].name == "AIM" then
				t[i].value = '0'
				t[i].freeze = true
				t[i].freezetype = gg.FREEZE_NORMAL
				t[i].name = 'AIM'
			end

		end
		gg.removeListItems(t)
		gg.addListItems(t)
		gg.toast("ᴀıмʟσcκ + ɴσ ʀᴇcσıʟ ✔️")
	end
	
	function UnderCar()
		if x4 == on then
			libil2cpp1("C0266666","48BFFFC")
			gg.toast("🚗 υɴᴅᴇʀ cᴀʀ ✔️")

		else
			libil2cpp1("38D1B717","48BFFFC")
			gg.toast("🚗 υɴᴅᴇʀ cᴀʀ ❌")
		end
	end
	
	function WallHack()
		if x5 == on then
			local t = gg.getListItems()
		for i, v in ipairs(t) do
			
			if t[i].name == "AIM" then
				t[i].value = '0'
				t[i].freeze = true
				t[i].freezetype = gg.FREEZE_NORMAL
				t[i].name = 'AIM'
			end

		end
		gg.removeListItems(t)
		
			gg.setRanges(32)
			gg.searchNumber("00r;00r;00r;40r;00r;00r;00r;00r;00r;00r;00r;40r;00r;00r;82r;43r;CDr;CCr;CCr;3Dr;00r;00r;40r;40r;03r;00r;00r;00r;03r;00r;00r;00r::32", 1)
			gg.searchNumber("00r;00r;00r;40r;00r;00r;00r;00r;00r;00r;00r;40r::12", 1)
			gg.getResults(12)
			gg.editAll("00r;C0r;79r;C4r;00r;C0r;79r;C4r;00r;C0r;79r;C4r", 1)
			gg.clearResults()
			gg.toast("ᴡᴀʟʟʜᴀᴄᴋ ✔️")
		
		gg.addListItems(t)
		else
				local t = gg.getListItems()
			for i, v in ipairs(t) do
				
				if t[i].name == "AIM" then
					t[i].value = '0'
					t[i].freeze = true
					t[i].freezetype = gg.FREEZE_NORMAL
					t[i].name = 'AIM'
				end

			end
			gg.removeListItems(t)
		
			gg.setRanges(32)
			gg.searchNumber("00r;00r;00r;40r;00r;00r;00r;00r;00r;00r;00r;40r;00r;00r;82r;43r;CDr;CCr;CCr;3Dr;00r;00r;40r;40r;03r;00r;00r;00r;03r;00r;00r;00r::32", 1)
			gg.searchNumber("00r;C0r;79r;C4r;00r;C0r;79r;C4r;00r;C0r;79r;C4r::12", 1)
			gg.getResults(12)
			gg.editAll("00r;00r;00r;40r;00r;00r;00r;00r;00r;00r;00r;40r", 1)
			gg.clearResults()
			gg.toast("ᴡᴀʟʟʜᴀᴄᴋ ❌")
			
			gg.addListItems(t)
		end
	end
	
	function CarroIndestrutivel()
		x3 = off
		valueFromClass("GameModeSetting", "0x2e", false, false, 1)
	    gg.getResults(100)
	    gg.editAll(1, 1)
	    gg.clearResults()
	    gg.toast("cᴀʀʀσ ıɴᴅᴇsтʀυтıνᴇʟ ✔️")
	end
	
                else
                gg.alert("υsυáʀıσ ᴇ/συ sᴇɴнᴀ ıɴcσʀʀᴇтᴀ!")
                return
            end
    else
	        gg.alert("ᴇʀʀσ ɴσ sᴇʀνıᴅσʀ!")
	        os.exit()
	        return
    	end
	end
end
--[[ MENU PARTIDA ]]--
while true do
	if gg.isVisible() then
	   gg.setVisible(false)
	MenuInicial()
	end
end
