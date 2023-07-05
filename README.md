# AC_Black_Diamond
Anti-cheats for SAMP supports updated versions

You load the filterscript, and you add the following code to your gamemode and can use the new functions
Note that you have a public that checks an unsupported version in anticheat, it is recommended to block them and inform them that they need to update their SAMP version

Unopened code to protect against bypass attempts, afraid of malicious code? This is an amx file, its compiler is not complicated, you can throw the file in hexeditor and see all the functions I use and also the strings (at the end of the file)
At the beginning of his the functions

```cpp

forward OnDetecteds0beit(playerid);
public OnDetecteds0beit(playerid)
{
    printf("sobeit detected %d", playerid);
    return 1;
}
//use sampfuncs for get api sampinfo cheats..
forward OnDetectedSAMPFUNCS(playerid);
public OnDetectedSAMPFUNCS(playerid)
{
    printf("sampfuncs detected %d", playerid);
    return 1;
}

//use SprintHook.asi auto run fast cheat
forward OnDetectedSprintHook(playerid);
public OnDetectedSprintHook(playerid)
{
    printf("SprintHook detected %d", playerid);
    return 1;
}

//CLEO,modloader,modloader..etc
forward OnDetectedMods(playerid);
public OnDetectedMods(playerid)
{
    printf("mods detected %d", playerid);
    return 1;
}
//test bypass anticheat 100% need ban
forward OnDetectedbypass(playerid);
public OnDetectedbypass(playerid)
{
    printf("testbypass detected %d", playerid);
    return 1;
}

//Old version anticheat does not support, it is recommended to kick and ask to update the SAMP version
forward OnDetectedOldversion(playerid);
public OnDetectedOldversion(playerid)
{
    printf("oldversion detected %d", playerid);
    return 1;
}

forward OnDetectedSlientaim(playerid);
public OnDetectedSlientaim(playerid)
{
    printf("slientaim detected %d", playerid);
    return 1;
}

```
