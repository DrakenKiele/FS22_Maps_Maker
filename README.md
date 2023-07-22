# FS22_Maps_Maker
I want to create a map generator utility for making maps for Farm Sim 22. 

Notes:
1. I am no expert at anything maybe but being a total organizational nightmare.  As such, I created this Git to help get organized and to, eventually be able to streamline the process of creating maps for Farm Sim 22.
2. I have only been doing this particular work for about two weeks.  Which makes this list a bit weak.  But, as I produce more maps, I hope this will help to be a start of something bigger.
3. I am not the type of person that wants to be up in front of a crowd creating online content.  That is not the goal of this Git.  I just want to note, and to share, what I have figured out so that others may benefit.
4. I have downloaded over 4000 mods for FS 22 and have almost all of them running at once.  When I have errors in my load log, I figure out the cause and pull mods out of the lineup.  Sometimes I am able to fix them myself.  I have offered corrected version of files to a few authors.

Topics I will be covering in this Readme

I. FS22 Map Content Folder Structure
II. The modDesc.xml file.
III. Map size disambiguation.
IV. Creating map textures using Paint.net
V. Where to find "real" help.
VI. The elements of a complete starter map.
VII. Prefabs
VIII. Copy rights and what to do if you want your stuff off my Git.

I. FS22 Map Content Folder Structure.

Background:  The maps in FS22 come in two parts basically,  The MAIN Map I3D file and all of the files that support it.

From this perspective you have the map.i3d which describes the 3d environment and all of the other i3d prefabs that go into it.  And then you have all of the XML files that configure the i3d files.

The basic structure of your project may look something like this: NOTE: Folder names will be ALL CAPS, fileNamesWillBeCamelCase.

Here is what you get if you open the editor, save a new project, and use the Prefab button to get a new map.

DATA- (PNG, DDS, GDM, GRLE files)
PREFABS- (Prefab Folders)
XML- (XML files)
-icon.dds
-map.i3d
-map.i3d.shapes
-map.i3d.terrain.lod.types.cache
-map.i3d.terrain.occluders.cache
-map.i2d.terrain.weights.cache
-map.xml
-overview.dds
-modDesc.xml
-preview.dds
-sounds.i3d
-sounds.i3d.shapes

To keep things orderly, I add a -MAP folder and put all the "map" files in it.  Then, I create a -SOUND folder for the "sounds" files.

DATA- (PNG, DDS, GDM, GRLE files)
PREFABS- (Prefab Folders)
XML- (XML files)
MAP- (map files)
SOUND- (sounds files)
-icon.dds
-overview.dds
-modDesc.xml
-preview.dds

The remaining files are used in FS22 before you even open the map.  So, I keep them out of the folder structure.

II. The modDesc.xml file.

As far as I can tell, this is the jumoping off point for your map.  This is the first place FS22 looks when it begins to open and utilize your map.

---------------------------------------------------------------------------------------------------------------------------------------------------

<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<modDesc descVersion="75">
    <author>Draken Kiele</author>
	
    <version>1.0.0.0</version>
	
    <title>
        <en><yourmapTitle></en>
        <de></de>
    </title>
	
    <description>
        <en><![CDATA[<yourMapDescription]]></en>
        <de></de>
    </description>
	
    <iconFilename>icon.png</iconFilename>
	
    <multiplayer supported="true"/>
	
    <maps>
        <map id="<mapTitle>" className="Mission00" filename="$dataS/scripts/missions/mission00.lua" configFilename="maps/xml/map.xml" defaultVehiclesXMLFilename="maps/xml/vehicles.xml" defaultPlaceablesXMLFilename="maps/xml/placeables.xml" defaultItemsXMLFilename="maps/xml/items.xml">
            <title>
                <en>Callisto 16x Terrafarm</en>
                <de>Callisto 16x Terrafarm</de>
            </title>
            <description>
                <en><yourMapDescriptionExtended></en>
                <de></de>
            </description>
            <iconFilename>preview.png</iconFilename>
        </map>
    </maps>
	
	<storeItems>

  </storeItems>
	
</modDesc>






