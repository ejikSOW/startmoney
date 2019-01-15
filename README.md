# startmoney

Server file arma 3 Exile start money for player
1. Create folder in your mission. Example: mpmission/Exile.Altis/Override
2. Upload file ExileServer_object_player_database_insert.sqf in folder
3. create file hpp for override. Example: mpmission/Exile.Altis/override.hpp
4. Add lines to file
ExileServer_object_player_database_insert = "Override\ExileServer_object_player_database_insert.sqf";
5. Open file  mpmission/Exile.Altis/config.cpp
6. Find lines with class CfgExileCustomCode and write him lines
#include "override.hpp"
Example:
class CfgExileCustomCode 
{
	#include "override.hpp"
	/*
		You can overwrite every single file of our code without touching it.
		To do that, add the function name you want to overwrite plus the 
		path to your custom file here. If you wonder how this works, have a
		look at our bootstrap/fn_preInit.sqf function.

		Simply add the following scheme here:

		<Function Name of Exile> = "<New File Name>";

		Example:

		ExileClient_util_fusRoDah = "myaddon\myfunction.sqf";
	*/
};
7. mpmission/Exile.Altis write folder Exile.Altis in pbo
