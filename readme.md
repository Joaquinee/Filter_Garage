# Script Filter Garage Pour Serveur Altis Life

Script Filter garagae Pour serveur Altis Life

## Installation Client

Glissez le fichier client dans votre missions.

Dans function.hpp trouver : `class Dialog_Controls` puis ajoutez :
```hpp
class filterGarage {};
```

Dans le fichier **dialog\impound.hpp** ajoutez en  dessous de  : 
```hpp
class MainHideText: Life_RscText {
      idc = 2811;
      text = "$STR_ANOTF_QueryGarage";
      sizeEx = 0.06;
      x = 0.24;
      y = 0.5;
      w = 0.6;
      h = (1 / 15);
};
```
Ce code la : 
```hpp
class Search_veh: Life_RscEdit {
      idc = 2812;
      text = "";
      x = 0.11;
      y = 0.8;
      w = 0.3;
      h = 0.04;
      onKeyUp = "[(_this # 0), 2802, 2803] spawn life_fnc_filterGarage";
};
```
Dans le fichier **dialog\function\fn_impoundMenu.sqf** ajoutez au dessus de  : 
```sqf
ctrlShow[2810,false];
```
Le code suivant : 
```sqf
uiNamespace setVariable ["VehicleList", _vehicles];
```