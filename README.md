# AC_Black_Diamond
Anti-cheats for SAMP supports updated versions

You load the filterscript, and you add the following code to your gamemode and can use the new functions
Note that you have a public that checks an unsupported version in anticheat, it is recommended to block them and inform them that they need to update their SAMP version

no open source why? to protect against bypass attempts, afraid of malicious code? This is an amx file, its compiler is not complicated, you can throw the file in hexeditor and see all the functions I use and also the strings (at the end of the file)
At the beginning of his the functions

```cpp


//----------------------------------------------------------
#define KickEx(%0) SetTimerEx("KickP2", 6000, false, "d", %0)
forward KickP2(playerid);
public KickP2(playerid) return Kick(playerid);

#define BanEx(%0) SetTimerEx("BanP2", 6000, false, "d", %0)
forward BanP2(playerid);
public BanP2(playerid) return Ban(playerid);


//Old version anticheat does not support, it is recommended to kick and ask to update the SAMP version
forward OnDetectedOldversion(playerid);
public OnDetectedOldversion(playerid)
{
    printf("oldversion detected %d", playerid);
	SendClientMessage(playerid, 0xFFFF0000, "Update your version and return to the server www.sa-mp.com");
	GameTextForPlayer(playerid, "~r~oldversion", 5000, 3);
	KickEx(playerid);
    return 1;
}
//A cheat similar to autocbug allows you to shoot at a very high speed https://www.blast.hk/threads/20266/
forward OnDetectedImprovedDeagle(playerid);
public OnDetectedImprovedDeagle(playerid)
{
    printf("ImprovedDeagle detected %d", playerid);
	SendClientMessage(playerid, 0xFFFF0000, "Use cheats [ImprovedDeagle.asi] out!");
	GameTextForPlayer(playerid, "~r~Use cheats out!", 5000, 3);
	KickEx(playerid);
    return 1;
}

//It helps you in the bug to be more accurate, and also makes an infinite zoom in the sniper
forward OnDetectedExtraWS(playerid);
public OnDetectedExtraWS(playerid)
{
    printf("ExtraWS detected %d", playerid);
	SendClientMessage(playerid, 0xFFFF0000, "Use cheats [ExtraWS.asi] out!");
	GameTextForPlayer(playerid, "~r~Use cheats out!", 5000, 3);
	KickEx(playerid);
    return 1;
}

//It is recommended to block players using this
forward OnDetecteds0beit(playerid);
public OnDetecteds0beit(playerid)
{
    printf("sobeit detected %d", playerid);
	SendClientMessage(playerid, 0xFFFF0000, "Use cheats [s0beit/cheats] out!");
	GameTextForPlayer(playerid, "~r~Use cheats out!", 5000, 3);
	BanEx(playerid);
    return 1;
}
//use sampfuncs for get api sampinfo cheats..
forward OnDetectedSAMPFUNCS(playerid);
public OnDetectedSAMPFUNCS(playerid)
{
    printf("sampfuncs detected %d", playerid);
	SendClientMessage(playerid, 0xFFFF0000, "Use cheats [SAMPFUNCS.asi] out!");
	GameTextForPlayer(playerid, "~r~Use cheats out!", 5000, 3);
	KickEx(playerid);
    return 1;
}

//use SprintHook.asi auto run fast cheat https://www.blast.hk/threads/20161/
forward OnDetectedSprintHook(playerid);
public OnDetectedSprintHook(playerid)
{
    printf("SprintHook detected %d", playerid);
	SendClientMessage(playerid, 0xFFFF0000, "Use cheats [SprintHook.asi] out!");
	GameTextForPlayer(playerid, "~r~Use cheats out!", 5000, 3);
	KickEx(playerid);
    return 1;
}

//CLEO,modloader,modloader..etc
forward OnDetectedMods(playerid);
public OnDetectedMods(playerid)
{
    printf("mods detected %d", playerid);
	SendClientMessage(playerid, 0xFFFF0000, "Use cheats [cleo.asi/modloader.asi] out!");
	GameTextForPlayer(playerid, "~r~Use cheats out!", 5000, 3);
	KickEx(playerid);
    return 1;
}
//test bypass anticheat 100% need ban
forward OnDetectedbypass(playerid);
public OnDetectedbypass(playerid)
{
    printf("testbypass detected %d", playerid);
	SendClientMessage(playerid, 0xFFFF0000, "Use cheats out!");
	GameTextForPlayer(playerid, "~r~Use cheats out!", 5000, 3);
	BanEx(playerid);
    return 1;
}

//Not wrong at all, very useful for advanced types of silent aim
forward OnDetectedSilentaim(playerid);
public OnDetectedSilentaim(playerid)
{
    printf("silentaim detected %d", playerid);
	SendClientMessage(playerid, 0xFFFF0000, "Use cheats [silentaim] out!");
	GameTextForPlayer(playerid, "~r~Use cheats out!", 5000, 3);
	KickEx(playerid);
    return 1;
}



```
