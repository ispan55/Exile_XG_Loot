# Exile_XG_Loot
Exile_XG_Loot

#INSTALLTION
##Mission
    Go to the mission folder in the download, copy ExileClient_system_process_postInit.sqf and paste it into your mission folder.
    Go inside your missions config.cpp and find
      
      class CfgExileCustomCode 
      {
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
    
  and add:
    
      ExileClient_system_process_postInit = "ExileClient_system_process_postInit.sqf";
  
  So it looks like:
  
    class CfgExileCustomCode 
    {
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
    	ExileClient_system_process_postInit = "ExileClient_system_process_postInit.sqf";
    };
##Server
  Go into the @ExileServer/addons folder located in the download and copy the loot PBO for the version of the addon you want and paste it inside your @ExileServer/addons folder.
  
