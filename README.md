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
};
7. mpmission/Exile.Altis write folder Exile.Altis in pbo
