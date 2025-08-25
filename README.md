# Documentation
Documentation
1. Introduction
What is venue4D?
venue4D™ is a real-time in-venue graphics platform built on Unreal Engine 5 that allows live event venues to display high-impact 2D and 3D visuals—like sponsor content, and crowd animations—on LED screens with minimal technical expertise. It combines prebuilt smart templates, a simple trigger interface, and powerful hardware to make professional-grade visuals easy to deploy, customize, and control during live events, all through a subscription-based model that includes ongoing updates and support.
Who is it for?
venue4D™ is designed for sports arenas, stadiums, concert venues, and live event production teams who need professional, dynamic visuals without the complexity of building them from scratch. It’s ideal for teams that want to elevate the fan experience and showcase sponsors with eye-catching displays.


Key benefits
Professional-Grade Graphics Instantly: Deploy stunning 2D and 3D visuals on LED walls without hiring developers.
Easy Customization: Swap logos, colors, text, and sponsor content on most smart templates in seconds through a simple interface.
Live Triggering: Operators can cue animations on scoreboards in real time during events.
Scalable Output: Works seamlessly across any screen size—from a single scoreboard panel to a full-arena wrap.
All-in-One Solution: Hardware, software, and templates are bundled in a subscription package.

How to get support
Documentation: Access guides and tutorials at venue4d.com.
Online chat: Access live chat at venue4D.com or fill out a support form.
E-mail: Send an e-mail to support@emissivelabs.com.
Discord Community: Join our Discord Community for real-time support, product updates, and to connect with our team and other users.
Terms of Service



2. Getting Started
2.1 Downloading Software
Software prerequisites:
Latest version of 7zip
Download base venue4D unreal application and DLC here:	
https://aurora-deployment-1.s3.us-east-2.amazonaws.com/base/Base-EMSV.7z
https://aurora-deployment-1.s3.us-east-2.amazonaws.com/dlc/DLC-EMSV.7z
Custom version of unreal:
https://aurora-deployment-1.s3.us-east-2.amazonaws.com/engine/Engine.7z
Download the latest version of the venue4D application: https://www.dropbox.com/scl/fi/qjr708672z5gjxqu4ql7f/venue4d-win-portable-v2.0.0.zip?rlkey=zjl0qlyoc8gqtqegxecw2hibo&st=e65y5yml&dl=
Extract Base-EMSV.7z to a folder (ex. c:\venue4d)
Extract DLC content folders to the location where base was extracted: \FanFuel_10\DLC
Create a shortcut to FanFuel_10.exe and add the following command line parameters:
FanFuel_10.exe -RCWebControlEnable -MotionDesignRundownServerStart -Venue4DServerStart-MotionDesignPlaybackServerStart="FanFuelPackageGame"
(Optional) For headless with output through decklink, use the following command line parameters: 
 \FanFuel_10.exe -RCWebControlEnable -MotionDesignRundownServerStart -Venue4DServerStart-MotionDesignPlaybackServerStart="FanFuelPackageGame"-log -RenderOffscreen -unattended
(Optional) For headless with output to attached monitors/displays/hdmi/dp, use the following command line parameters:
\FanFuel_10.exe -RCWebControlEnable -MotionDesignRundownServerStart -Venue4DServerStart-MotionDesignPlaybackServerStart="FanFuelPackageGame" -log -NoWindow -unattended
Extract the contents of the venue4D application archive to a folder of your choice.
Copy the data folder from the app to \FanFuel_10\data OR create a symbolic link.  do not do both
(Optional) Instead of copying the data folder, create a Symbolic Link instead.  NOTE: This requires running the terminal as an administrator (search for terminal in the start menu, then right click the terminal icon and select run as administrator).  In the terminal, type the following (replacing the paths as appropriate):
New-Item -Path c:\venue4d\engine\FanFuel_10\data -ItemType SymbolicLink -Value C:\venue4d\app\data
Start the venue4D packaged app with one of the shortcuts that have been created.
Start the venue4D control app
2.2 Syncing your Venue 
Click on Settings (bottom left corner)

Go to the Venues tab
Click on red “Add a new venue” button in the top right corner
Name Venue (ex: Rocket Arena)

Click your newly created venue

Click on red “add new” button; provide…
Name of engine
Engine type
IP address 
Data path (Location of the "data" folder in the Engine install folder.  This is where team logos, sponsor logos, etc. are all placed.) 
“Use for preview” (Indicates that this is the engine that will be used for generating preview thumbnails)

Click on newly created engine

Click on red “add new” button; provide…
Canvas Name
Input the widths and height (pixels) of your canvas (a single canvas contains multiple displays.
Keep in mind when creating dimensions, the canvas does not need to be completely filled to run. We recommend not filling the entire canvas.

Click on the newly created canvas

Click the red “Add Display” button in the top right corner

Click on the settings icon of the added Display. Provide…
Change name of display (ex: entrance by visitor locker room)
Change width and height (pixels) to match display
Change render scale due to preference (recommended to keep at 100%) 
Custom scale allows for specific percentage scaling. Compared to rounding to the nearest whole number. 
Position X and Y: coordinates for display position on the canvas. 
Does not need to reflect positioning in real life. 
Enter Display Type (ex: ribbon board)

To move a display location you can manually drag and drop into new location and drag bottom left hand corner of display to change size
Video
Repeat steps 9-11 for each display in your arena.






When everything is all set up, hit the back arrow in top left corner

Click the red “Save Engine Configuration” button in the top right corner

Hit the settings tab in the bottom left corner

Your venue will appear under the venues tab 

2.3 Add your Team
Click on Settings in bottom left corner
Go to the “Teams” tab

Click on the red “Create team” button.

Provide…
Name of the team (ex: Miami Heat)
Team Abbreviation (Ex: MIA)
Select Sport 
Select League
Optional: select a default style preset. Only recommended if they have the same logos and colors. (For example Miami University Football and Miami University Basketball)
Click the red “Create Team” button








2.4 Load your Team Logo
Click on Settings in bottom left corner
Click on “SmartChip” tab

Click on red “Select file” button or drop svg file over zone
Need svg file of Team Logo


Primary - Overfill color Selection: 

Click dropper icon
Click on primary color in logo
Or type of color that you want
Repeat this for all Logo Colors
Square vs Variable? (square means width/height of image will be the same, variable preserves the aspect ratio of the input logo)
Click red “generate smart chip” button

Click red “save” button


2.5 Add a new Style Preset
Click on Settings tab in bottom left corner
Click on “Style Presets” tab

Click the red “Create preset” button

Create Style Preset Pop Up
Enter the name of the style (ex: Minnesota Vikings)
Load From Logo vs Manual Override (Best for editing colors)
Sponsor Image
Image Filter
Font
Team Logo
Click the red “Create Preset” button

3. Create a Show
3.1 Add a new Show
On the left hand side of the screen, near shows hit the plus icon on the right

Add Show Panel
Type in Show Name (Ex: April 14th, 2025, Basketball Game vs Baylor)
Select Venue
Select Show Date
Select Sport
Select League
Select Home and Away Teams
Hit red “Add Show” button

3.2 Add a Panel

At the top middle of the screen, hit the add panel button


Enter the name of the panel (Ex: 1st Half Prompts), and hit the red “Add Panel” button

3.3 Add a Prompt
Select a Panel
Hit the add prompt button
Above the thumbnail to the left, select a pack 
Above the thumbnail to the right, select a scene
Select a Prompt Text Preset or add in custom lines

On the “Style” tab, load a team logo or use manual override or both
Add in sponsor image if desired
Image Filter?
Font?
On the “Playout” tab, select a preset or manual
If manual choose loop
If using multiple loops choose how many below selection
Choose Mask

Hit the red “Save” button in the top right corner

Then hit the back arrow in the top left




3.4 Organizing Prompts
To change the location of a prompt
Go to any panel, hover over the prompt you want to move
Drag and drop the prompt in the new desired location (works between panels too in the “All” panel)
To change the location of a panel
On the top of the page, hover over the tab of the panel you would like to move, drag and drop the tab in its new location on the top of the page
If changing panel location in the “All” tab, hover over the panel, drag and drop it in its new location
To change the size of a panel in the “All” tab…
Click on the bottom left hand corner of the panel you would like to rearrange
Drag, and create the height and width of the panel size that you want

Video documenting this

3.5 Run a Prompt
Click on Settings (bottom left corner)

Make sure you are connected to a venue
Go back to the show you created
In the top right corner, hit the run button
Click on the scene you would like to run


To stop the prompt click on the scene thumbnail again

4. Miscellaneous
4.1 Create a New Playout Preset

Go to settings in the bottom left corner

Go to the “Playout Presets” tab on the top of the window
Select the red “create preset” button

Optional: Choose an existing playout preset to build off of (this will not overwrite existing preset)
Enter the name of the new playout preset
Select how many loops the preset should run for
Select Mask Type
Click red “Create Preset” button
4.2 Edit an Existing Playout Preset
Go to settings in the bottom left corner
Go to the “Playout Presets” tab on the top of the window
Click on the preset or select the three dot icon to the far right of the preset you want to edit
Optional: Choose an existing playout preset to build off of (this will not overwrite existing preset)
Change the name of the playout preset
Change the loop count in the preset
Change Mask Type
Click red “Save Preset” button

4.3 Delete an Existing Playout Preset
Go to settings in the bottom left corner
Go to the “Playout Presets” tab on the top of the window

Select the three dot icon to the far right of the preset you want to delete, select delete

4.4 Create a New Prompt Preset 
Go to settings in the bottom left corner

Go to the “Prompt Presets” tab on the top of the window
Select red “create preset” button
Optional: Choose an existing preset to build off of (this will not overwrite existing preset data)
Enter the name of the new prompt text preset (Ex: Make Some Noise )
Line1: Enter a word/slogan max (X) characters (Ex: MAKE)
Line2: Enter a word/slogan max (X) characters (Ex: SOME)
Line3: Enter a word/slogan max (X) characters (Ex: NOISE)
Click red “Save Preset” button
4.5 Edit an Existing Prompt Preset 
Go to settings in the bottom left corner

Go to the “Prompt Presets” tab on the top of the window

Click on the preset or select the three dot icon to the far right of the preset you want to edit 

Optional: Choose an existing preset to build off of (this will not overwrite existing preset data)
Change the name of the new prompt text preset 
Line1: Change the word/slogan max 10 characters (Ex: MAKE)
Line2: Change the word/slogan max 10 characters (Ex: SOME)
Line3: Change the word/slogan max 10 characters (Ex: NOISE)
Click red “Save Preset” button
4.6 Delete an Existing Prompt Preset

Go to settings in the bottom left corner

Go to the “Prompt Presets” tab on the top of the window

Select the three dot icon to the far right of the preset you want to delete, select delete

4.7 Edit an Existing Venues Engine 
Click on Settings (bottom left corner)

Go to the Venues tab
Click on the venue or select the three dot icon to the far right of the venue you want to edit    

To edit an engine select three dot icon to the far right 
Name of engine
Engine type
IP address 
Data path
“Use for preview”
Select red “Update button”

To add a new engine select “add new” button; provide…
Name of engine
Engine type
IP address 
Data path
“Use for preview”
Select red “Add” button
If you created a new engine… click on engine name 
Click on the red “add new” button; provide…
Canvas Name
Input the widths and height of your canvas; 
Keep in mind when creating dimensions, the canvas does not need to be completely filled to run. We recommend not filling the entire canvas.
Click on the newly created canvas
Click the red “Add Display” button in the top right corner
Click on the settings icon of the added Display.
Change name of display (ex: entrance by visitor locker room)
Change width and height to match display
Change render scale due to preference (recommended to keep at 100%) 
Custom scale allows for specific percentage scaling. Compared to rounding to the nearest whole number. 
Position X and Y: coordinates for display position on the canvas. 
Does not need to reflect positioning in real life. 
Enter Display Type (ex: ribbon board)
To move a display location you can manually drag and drop into a new location and drag the bottom left hand corner of the display to change size. Video
Repeat steps 9-11 for each display in your arena.
When everything is all set up, hit the back arrow in top left corner
Click the red “Save Engine Configuration” button in the top right corner
4.8 Delete an Existing Venue
Click on Settings (bottom left corner)
Go to the Venues tab
Click on the three dot icon to the far right of the venue you want to delete, select delete
4.9 Delete an Existing Venues Engine
Click on Settings (bottom left corner)
Go to the Venues tab
Click on the venue name click on the three dot icon to the far right of the venue, select edit
Click on the three dot icon to the far right of the engine you want to delete, select delete

4.10 Edit an Existing Venues Displays 
Click on Settings (bottom left corner)
Go to the Venues tab
Click on the venue or select the three dot icon to the far right of the venue you want to edit
Click on the Engine which has the displays you want to edit
If you want to create a new canvas, click on the red “add new” button; provide…
Canvas Name
Input the widths and height of your canvas; 
Keep in mind when creating dimensions, the canvas does not need to be completely filled to run. We recommend not filling the entire canvas.
If you want to edit an existing canvas size, select the three dot icon to the right of the canvas
Enter the new dimensions of your canvas
To get to displays, click on the canvas you would like to edit
To add a new display, click on the red “Add Display” button in the top right corner
To edit a display, click on the settings icon of the added Display. 
Change name of display (ex: entrance by visitor locker room)
Change width and height to match display
Change render scale due to preference (recommended to keep at 100%) 
Custom scale allows for specific percentage scaling. Compared to rounding to the nearest whole number. 
Position X and Y: coordinates for display position on the canvas. 
Does not need to reflect positioning in real life. 
Enter Display Type (ex: ribbon board)
To move a display location you can manually drag and drop into a new location and drag the bottom left hand corner of the display to change size. Video
Repeat steps 9-11 for each display in your arena.
When everything is all set up, hit the back arrow in top left corner
Click the red “Save Engine Configuration” button in the top right corner
4.11 Delete an Existing Venues Displays
Click on Settings (bottom left corner)
Go to the Venues tab
Click on the venue or select the three dot icon to the far right of the venue you want to edit
Click on the Engine which has the displays you want to edit
If you want to delete an entire canvas, select the three dot icon to the left of the canvas 

If you want to delete individual displays, select the canvas where the displays are
Select the settings icon in the top right of the display 
Select the red “delete display” button
Repeat steps 7 and 8 for as many displays as you want
Hit the back arrow in the top left corner next to the canvas name
Hit the red “Save Engine Configuration” button in the top right corner

4.12 Edit an Existing Team
Click on Settings in bottom left corner
Go to the “Teams” tab
Search for your team by name, sport, league and/or abbreviation 
Click on the three dot icon to the far right of the team you want to edit
Change name of the team (ex: Minnesota Vikings)
Change Team Abbreviation (Ex: MIN)
Change Sport 
Change League
Click the red “Update Team” button

4.13 Delete an Existing Team
Click on Settings in bottom left corner
Go to the “Teams” tab
Search for your team by name, sport, league and/or abbreviation 
Click on the three dot icon to the far right of the team you want to delete, select delete

4.14 Load a Sponsor Logo
Click on Settings in bottom left corner
Click on “SmartChip” tab
Click on red “Select file” button or drop svg file over zone
Select svg file of Sponsor Logo
Primary - Overfill color Selection: 
Click dropper icon
Click on primary color in logo
Or type of color that you want
Repeat this for all Logo Colors
Square vs Variable?
Click red “generate smart chip” button
Click red “save” button
I have no idea where to save it to integrate it into venue4D application
4.15 Edit an Existing Style Preset
Click on Settings tab in bottom left corner
Click on “Style Presets” tab
Click on the style preset you want to edit or the three dot icon to the right of the style preset
Change the name of the style (ex: Vikings Pride Game)
Load From Logo vs Manual Override (Best for editing colors)
Sponsor Image, Image Filter, Font, Team Logo
Click the red “Save Preset” button
4.16 Delete an Existing Style Preset
Click on Settings tab in bottom left corner
Click on “Style Presets” tab
Click on the three dot icon to the right of the style preset, select delete
4.17 Edit an Existing Shows Settings
On the left hand side of the screen, near shows, hover over the show you want to edit and click on the tree dot icon 
Edit Show Name (Ex: April 14th, 2025, Basketball Game vs Baylor)
Edit Venue
Edit Show Date
Edit Sport
Edit League
Edit Home and Away Teams
Hit red “Update Show” button

4.18 Duplicate an Existing Show
On the left hand side of the screen, near shows, hover over the show you want to duplicate and click on the tree dot icon, click “duplicate show”

4.19 Delete an Existing Show
On the left hand side of the screen, near shows, hover over the show you want to duplicate and click on the tree dot icon, click “delete show”


4.20 Generate a Pack into a Show
On the left hand side of the screen, near shows, hover over the show you want to generate a pack into and click on the tree dot icon, click “Generate from Pack”
Select a pack to generate from
Select a scene from the pack
Click red “Generate” button
The show should now have a copy of every prompt preset in the theme of the pack and scene you selected 

4.21 Generate a Sample into a Show
On the left hand side of the screen, near shows, hover over the show you want to generate a pack into and click on the tree dot icon, click “Generate Sample”
I don’t know what this does

4.22 Delete a Panel from a Show
On the left hand side of the screen, under shows, click on the show you want to delete the panel from
At the top middle of the screen, click on the panel you would like to delete
Click on the three dot icon next to the name of the panel, click “Delete”

4.23 Rename a Panel on a Show
On the left hand side of the screen, under shows, click on the show you want to edit the panel from
At the top middle of the screen, click on the panel you would like to edit
Click on the three dot icon next to the name of the panel, click “Rename”
Type in new name and hit the red “Rename” button
4.24 Duplicate a Panel on a Show
On the left hand side of the screen, under shows, click on the show you want to edit the panel from
At the top middle of the screen, click on the panel you would like to edit
Click on the three dot icon next to the name of the panel, click “Duplicate”

4.25 Change the Style on a Panel on a Show
On the left hand side of the screen, under shows, click on the show you want to edit the panel from
At the top middle of the screen, click on the panel you would like to edit
Click on the three dot icon next to the name of the panel, click "Change Style”
Select the style preset you would like to add from the dropdown menu
Click the red “Change” button

4.26 Change the Scene of a Panel on a Show
On the left hand side of the screen, under shows, click on the show you want to edit the panel from
At the top middle of the screen, click on the panel you would like to edit
Click on the three dot icon next to the name of the panel, click "Change Scene”
Select the pack you would like to use
Select the scene you would like to use
Click the red “Change” button

4.27 Delete a Prompt from a Panel/Show
On the left hand side of the screen, under shows, click on the show you want to edit the prompt from
At the top middle of the screen, click on the panel where the prompt is located
Hover over the prompt, and click on the red X button in the right corner
Click the red “delete” button

4.28 Edit a Prompt from a Panel/Show
On the left hand side of the screen, under shows, click on the show you want to edit the prompt from
At the top middle of the screen, click on the panel where the prompt is located
Hover over the prompt, and click on the settings icon in the middle
Edit any of these properties
Above the thumbnail to the left, select a new pack 
Above the thumbnail to the right, select a new scene
Select a new Prompt Text Preset or change custom lines
On the “Style” tab, load a new team logo or use manual override or both
Add in sponsor image if desired
Image Filter?
Font?
On the “Playout” tab
select a preset or manual
If manual choose loop
If using multiple loops choose how many below selection
Choose Mask
Hit the red “Save” button in the top right corner

4.29 Duplicate a Prompt from a Panel/Show
On the left hand side of the screen, under shows, click on the show you want to edit the prompt from
At the top middle of the screen, click on the panel where the prompt is located
Hover over the prompt, and click on the two page icon in the left corner


Things Not Included which I Don't Know

Settings tab: License Information

 
