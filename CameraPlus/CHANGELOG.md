# v6.0.1 Changes
- Missing folder integrity check when backing up old settings. 

# v6.0.0 Changes
- Supports game version 1.16.3.  
- Change the configuration file from ini and cfg to json file.  
- Optimized some code.  

# v5.2.4 Changes  
- Fixed TurnToeHead offset forgetting to return.  

# v5.2.3 Changes
- I accidentally commented out the VRPointer part.  

# v5.2.2 Changes
- Supports Player Track for new Noodle Extensions.  

# v5.2.1 Changes
- buf fix (It failed to destroy VRPointer internally and was mass-produced every time the profile was loaded.)  
- Re-register code for 1.15.0 and below.  
- Revised the display object  menu and added display / non-display switches for Saber, Notes, and wall frames.  

# v5.2.0 Changes
- Supported game version 1.16.1 (Not compatible with 1.15.0 and earlier. Although it works)  

# v5.1.0 Changes
- Fixed an issue where the camera would fall to the bottom of the ground when Turn To Head was enabled during FPFC Toggle.  
- Fixed an issue where scripts would be reset when crossing scenes without changing Profile when using UnityTimer (Thanks for reporting)  
- Added TurnToHead option and offset to MovementScript.  

# v5.0.0 Changes
- Rebuilt to IPA 4.x specifications.  
- Fixed camera Quad ignoring Depth.
- Added offset to the option to point the camera at the HMD.
- The 360-degree setting value is shared with the third person.

# v4.11.0 Changes
- Added option to follow the 3rd person camera in the direction of the HMD.
- When failing the multiplayer score display, it is displayed in red to make it easier to understand.

# v4.10.0 Changes
- VMCProtocol implementation (Sender uses OSC Jack, Receiver depends on VMCAvatar)  
- Added some numerical restrictions to the camera2 converter(thanks review kinsi)  
- Show the third-person camera when the FPFCToggle is turned back off.
  (Known issue where using the FPFC toggle prevents you from moving to another player's position in multiplayer mode.)
- (Not Fix)Lighter multiplayer related processing.  
- Camera position can now be changed by mouse dragging. (Base cord were given to me by nalululuna.)
- Fixed an issue where profile changes were not made at startup.  

# v4.9.2 Changes
- Fixed an issue where the first-person camera would switch to the third-person camera when switching profiles.  

# v4.9.1 Changes
- In v4.9.0, we changed the timing of the display layer control for the future.  
However, it turned out that it was not working properly in some environments, so we changed it back.  

# v4.9.0 Changes
- Trial implementation of configuration converter to Camera2.
- Fixed a bug in NoodlePlayerTrack when changing RoomAdjust.
- Start implementation of SongScript.
- Fixed a typo in ExampleMovementScript.json. For those who cannot get it to work, delete the saved sample once and the correct file will be generated.

# v4.8.0 Changes
- Fixed the multiplayer status display screen being out of sync again. Functions taken from Camera2
- Add 90/360 degree profiles. Change the way to turn off Smoothcamera.
# v4.7.6 Changes
- Fixed a situation where enabling TransportWall when Bloom is off would only result in translucency. 
  Thanks for sharing the patch, Kinsi55!
# v4.7.5
- Added an option to prevent accidentally grabbing and moving the camera quad.
# v4.7.4
- Fixed the part that fails to get multiplayer lobby position.
- Fixed incorrect positioning of the camera quad in multi-mode.
- 10 player mode support for MultiplayerExtension + BeatTogether
- Fixed the display position of multiplayer status display (name, score and rank).
- Merged features for Custom Notes.
# v4.7.0 for game version 1.13.2
- Function to follow the camera to NoodleExtension's AssignPlayerToTrack (optional, off by default)
- Fixed a possible duplication of camera locations in the multiplayer lobby.
- Fixed an issue where flickering would occur at the start of a song.
  (This was noticeable when used with the "Gotta go fast" mod, and kinsi55 helped me with this.
# v4.6.0
- Since the number of setting items has increased considerably, the UI has been reorganized.
- More options to display name, rank, and score during multiplayer.
- Added profile switching for multiplayer. Currently the profile is the same for lobby and game.
# v4.5.0
- Changed the JSON library from SimpleJSON to JSON.net.
- Add MovementScript selection to the right-click menu
- Add Added FOV control to the MovementScript.
- Add MultiplayCamera
# v4.4.2
- Fixed an issue with the new profile system not saving when there is no profile (thanks to Fefeland for contacting me)
- Fixed an error that was occurring when playing online.
- Multiplayer spectator mode is not currently supported.
- Considering offsetting it due to the fact that the player's position is no longer at the origin.

# v3.1.0 Changes
- New song camera movement script!
   * Same as the old camera movement script, except it gets automatically read from the song directory (if it exists) when a song is played!
   * To use this new script, just right click on the camera in your game window and add a song camera movement script from the `Scripts` menu
   * Mappers, simply add a CameraMovementData.json in the custom song directory, and if the user has a camera with a song movement script attached to it that camera script will be played back when they start the song.

# v3.0.5 Changes
- Switch back to vertical FOV (oops)

# v3.0.3 Changes
- Fixed a bug where some cameras would not be displayed correctly if the width was less than the height
- Now automatically moves old cameraplus.cfg into UserData\CameraPlus if it doesn't already exist

# v3.0.2 Changes
- Automatically fit main camera to canvas
- Added render scale and fit to canvas options in the Layout menu

# v3.0.1 Changes
 - Fix LIV compatibility

# v3.0 Changes
 - Fixed performance issues
 - Added multi-cam support!
    * Right click the game window for a full menu  with the ability to add, remove, and manage your cameras!
 - New CameraMovement script support (created by Emma from the BSMG discord)
    * Allows you to create custom scripted movement paths for third person cameras, to create cool cinematic effects!
