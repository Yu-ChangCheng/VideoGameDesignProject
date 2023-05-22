# Solar Sentinel - a single player 3D Mech FPS Game built using Unity Game Engine by Team Trash Pandas

## A "game feel" game where you are a Mech saving your planet from losing its sun.
###To play simply download the Build folder and play on either the MacOS or Windows
The trailer Video: https://youtu.be/x4AXpEoTAnU

###To Download the game, please find it here: https://gtvault-my.sharepoint.com/:f:/g/personal/ycheng345_gatech_edu/EurOD2Q2QMlFo-HWwcI1a2gBU2_BfJ69bBkc70LMG5QmQg?e=yTNRX8


## Team: Trash Pandas
  * Yu-Chang Cheng | ycheng345@gatech.edu | ycheng345
  * Louis Russo | lrusso7@gatech.edu | lrusso7
  * Benjamin Fluharty | bfluharty3@gatech.edu | bfluharty3
  * Benedicto Da Silva | bsilva38@gatech.edu | bsilva38
  * Shane Moro | shane7@gatech.edu | smoro7



How to play (PC):
  * Movement
      *  Move with "WASD" keys 
      *  Look around by moving the mouse
      *  Jump with "SPACE" 
      *  Brake with "LSHIFT" 
  * Combat
      *  Fire projectile with left-click
      *  Engage EMP with "1"
  * Menus/HUD
      *  Pause game with "ESC"
      *  View progress with "TAB"
      *  View map with "M"
      *  Zoom in minimap with "+"
      *  Zoom out minimap with "-"
      
How to play (Xbox Controller):
  * Movement
      *  Move with "LS"
      *  Look around with "RS"
      *  Jump with "A" 
      *  Brake with "B" 
  * Combat
      *  Fire projectile with "RT"
      *  Engage EMP with "RB"
  * Menus/HUD
      *  Pause game with "START"
      *  View progress with "SELECT"
      *  View map with "LB"
      *  Zoom in minimap with "UP ARROW"
      *  Zoom out minimap with "DOWN ARROW"
 
 
Technology Requirements:
  * Game must be implemented in Unity
    * Solar Sentinel was implemented on Unity 2020.3.43f.

  * Game must consist of a 3D world
    * Solar Sentinel takes place in a 3D world laid out on a 1 million m^2 map, filled with varying topography, vegetation, walls, shields, gates and other obstacles. The player experiences time advancing in the 3D world by the sun’s height in the sky and length of shadows (game begins at sunrise as the player character is solar-powered).

  * Game must utilize a character/vehicle controlled by the player with engaging animations that react to the player’s inputs.
    * The player character is a Mech built in Blender with multiple articulated and moving parts. Player mobility is controlled by two propulsion mechanisms. 
    * Most of the time the Mech will be moving on the ground and traction is achieved through the use of four wheel colliders. Players use the keyboard to control the force and direction of movement applied to the wheel colliders which translate into control over the character’s acceleration, turning and breaking. 
    * A secondary propulsion mechanism is the use of jetpacks in the back of the character. They can only be used a few seconds at a time and apply upward force to the Mech allowing it to jump over obstacles. They are activated using the keyboard. 
    * The mech also has a cockpit mounted on a swivel ball that allows it to rotate 360 degrees on the Y axis, currently controlled by the mouse cursor. 
    * Lastly, the Mech has gun turrets mounted on either side of the cockpit that can move up and down, also controlled by the mouse. The player can fire laser projectiles through the character guns using the mouse. The combined cockpit and gun rotations allow the Mech to aim at targets around it. 

  * Game must implement a real-time steering, path planning, and state machine based AI
    * The game uses enemy drones as AI-controlled NPCs.  
    * These drones use a state machine to decide their next action. These states are Idle, Pursue, Engage, and Death. 
    * Changes states based on multiple factors including distance to player and whether projectiles are detected nearby.
    * Movement is limited to a defined NavMesh baked into the terrain.

  * Game must utilize rigid body physics simulation with interactive objects
    * Multiple in game objects react when shot, destroyed, or collided into. 
    * Solar panels move when shot. 
    * Closed doors and shields prevent the player from moving past. 
    * Platforms/terrain prevent the player from falling through the floor. 
    * Crates move when bumped into or shot. 
    * Player, solar panels, and main building falls apart when destroyed. 

  * Game must be a Game Feel game, with rich Game Feel mechanics and a supporting environment
    * Objectives are shown to the player on a GUI menu that can be accessed in game and updates when objectives have been completed. 
    * Game difficulty increases as the game progresses with more obstacles and enemies that the player must interact with. 

  * Game must attempt to provide interesting choices for the player to make during gameplay
    * The player can choose how to engage with enemies via various pickups. 
    * Attack with main weapon. 
    * Use EMP to take out multiple enemies at once. 
    * Collect a shield to engage while protected. 
    * Players can choose to collect the energy pickups as soon as they see them, or they can choose to defer the pickup until after some particular challenge (e.g., after engaging enemy drones) 
    * Players have a choice to take an easy or hard path after disabling the first shield generator. 
    * The easy path leads directly to the second shield generator after killing three drones. 
    * The hard path leads the player towards many enemy drones that must be killed prior to reaching the second shield generator.  Once the enemy drones have been killed the player is rewarded with an EMP pickup and an energy pickup.   

  * Game must include engaging and polished starting/resolving actions, pause in gameplay, configuration, credits, licenses, etc., via GUI menu
    * The title menu has a trailer video and provides an initial setting and entry point to the game. 
    * The player can access the pause game menu to Continue, Restart, Exit, or change Options (Volume, Resolution, FPS, Mini Map). 
    * The player can check the game progress from the mission menu during the game. 
    * Credits scrolling menu are displayed to the player upon completing the game.
    * When the player dies, they are given the option to respawn or go back to the main menu. 


Known problem areas:
  * Messy project structure
  * Pausing during ongoing dialog may freeze text as it is being outputted.
  * Colliders between the mech and drones sometimes disagree vaulting one of the objects into the sky.


Manifest of which files authored by each teammate:
Detail who on the team did what
  * Yu-Chang Cheng – Title Menus, Transitions, Mechanics (Pause/Quit), Credits
  * Louis Russo – HUD Design and Integration
  * Benjamin Fluharty – Enemy Development and AI
  * Benedicto Da Silva -  Level Design, Spatial Simulation, Physics
  * Shane Moro – Playable Character


For each team member, list each asset implemented. Make sure to list C# script files individually so we can confirm each team member contributed to code writing
Animations/Drone Idle.anim                                           Main: Benjamin Fluharty
Animations/Enemy Shield Solar Panel/Solar Power Destroyed.anim       Main: Benedicto da Silva
Animations/Enemy Shield Solar Panel/Solar Power Display.controller   Main: Benedicto da Silva
Animations/Enemy Shield Solar Panel/Solar Power Flashing Fast.anim   Main: Benedicto da Silva
Animations/Enemy Shield Solar Panel/Solar Power Flashing Slow.anim   Main: Benedicto da Silva
Animations/PA_DroneExplodeFall_Clip.anim                             Main: Benjamin Fluharty
Animations/PlayerShield/PlayerShieldActive.anim                      Main: Benedicto da Silva
Animations/PlayerShield/PlayerShieldAnimator.controller              Main: Benedicto da Silva
Animations/PlayerShield/PlayerShieldExpired.anim                     Main: Benedicto da Silva
Animations/PlayerShield/PlayerShieldExpiring.anim                    Main: Benedicto da Silva
Animations/PlayerShield/ShieldPickupAnimator.controller              Main: Benedicto da Silva
Animations/PlayerShield/ShieldPickupRotation.anim                    Main: Benedicto da Silva
Animations/PowerPack Animator.controller                             Main: Benedicto da Silva
Animations/PowerPack Rotation.anim                                   Main: Benedicto da Silva
Animations/SmokeAppear.anim                                          Main: Shane Moro
Animations/SmokeDisipate_1.controller                                Main: Shane Moro
Animations/SmokeDisipate_1_Anim.anim                                 Main: Shane Moro
Animations/SmokeDisipate_2.controller                                Main: Shane Moro
Animations/SmokeDisipate_2_Anim.anim                                 Main: Shane Moro
Animations/SmokeDisipate_3.controller                                Main: Shane Moro
Animations/SmokeDisipate_3_Anim.anim                                 Main: Shane Moro
Animations/SmokeMain.controller                                      Main: Shane Moro
AnimatorControllers/Damaged.anim                                     Main: Benjamin Fluharty
AnimatorControllers/Drone.controller                                 Main: Benjamin Fluharty, Contributors: Benedicto da Silva
AnimatorControllers/ShieldGenerator2.controller                      Main: Benjamin Fluharty
Light_Source 1/Beam.mat                                              Main: Yu-Chang Cheng
Light_Source 1/Circle.mat                                            Main: Yu-Chang Cheng
Light_Source 1/Materials/Circle.mat                                  Main: Yu-Chang Cheng
Light_Source 1/Materials/particlelight.mat                           Main: Yu-Chang Cheng
Materials/Black.mat                                                  Main: Shane Moro
Materials/Blue.mat                                                   Main: Shane Moro
Materials/DiminishedEnemyShield.mat                                  Main: Benjamin Fluharty
Materials/DroneMat.mat                                               Main: Benjamin Fluharty
Materials/DroneSpawnerPower.mat                                      Main: Benjamin Fluharty
Materials/EMPMaterial.mat                                            Main: Louis Russo
Materials/EMPRange.mat                                               Main: Louis Russo
Materials/EnemyShield.mat                                            Main: Benedicto da Silva
Materials/GameBlueFlash.mat                                          Main: Louis Russo
Materials/GameBlueIdle.mat                                           Main: Louis Russo
Materials/GameGreenFlash.mat                                         Main: Louis Russo
Materials/GameGreenIdle.mat                                          Main: Louis Russo
Materials/GameRedFlash.mat                                           Main: Louis Russo
Materials/GameRedIdle.mat                                            Main: Louis Russo
Materials/GameYellowFlash.mat                                        Main: Louis Russo
Materials/GameYellowIdle.mat                                         Main: Louis Russo
Materials/Green.mat                                                  Main: Benedicto da Silva, Contributors: Shane Moro
Materials/HeavyLaser.mat                                             Main: Benjamin Fluharty
Materials/Laser.mat                                                  Main: Benjamin Fluharty
Materials/PA_ArchfireTankMat.mat                                     Main: Benjamin Fluharty
Materials/PA_DroneMat.mat                                            Main: Benjamin Fluharty
Materials/PhotovoltaicCell.mat                                       Main: Benedicto da Silva
Materials/PhotovoltaicFrame.mat                                      Main: Benedicto da Silva
Materials/PlayerMapIconColor.mat                                     Main: Louis Russo
Materials/PowerPack.mat                                              Main: Benedicto da Silva
Materials/Red.mat                                                    Main: Louis Russo
Materials/ShieldPickup.mat                                           Main: Benedicto da Silva
Materials/SmokeColor.mat                                             Main: Shane Moro
Materials/Spark.mat                                                  Main: Louis Russo
Materials/Sun.mat                                                    Main: Shane Moro
Materials/SunRay.mat                                                 Main: Shane Moro
MenuUI/Animation/BlinkingPressCtoContinue.anim                       Main: Yu-Chang Cheng
MenuUI/Animation/Congrats msg.controller                             Main: Yu-Chang Cheng
MenuUI/Animation/Health_Icon.controller                              Main: Yu-Chang Cheng
MenuUI/Animation/Heart.anim                                          Main: Yu-Chang Cheng
MenuUI/Animation/MainMenu.controller                                 Main: Yu-Chang Cheng
MenuUI/Animation/MenuUpDown.anim                                     Main: Yu-Chang Cheng
MenuUI/Animation/PopUp.anim                                          Main: Yu-Chang Cheng
MenuUI/Animation/PopUpCongrats.anim                                  Main: Yu-Chang Cheng
MenuUI/Animation/PressAnyKeyToContinue.controller                    Main: Yu-Chang Cheng
MenuUI/Animation/PressCtoContinue.controller                         Main: Yu-Chang Cheng
MenuUI/Animation/PressToContinue.anim                                Main: Yu-Chang Cheng
MenuUI/Animation/RollUpCreditMenu.anim                               Main: Yu-Chang Cheng
MenuUI/Animation/Rollable.controller                                 Main: Yu-Chang Cheng
MenuUI/Animation/ShowedUpMainMenu.anim                               Main: Yu-Chang Cheng
MenuUI/Animation/Title.controller                                    Main: Yu-Chang Cheng
MenuUI/Animation/UICanvas - Credit Scrolling.controller              Main: Yu-Chang Cheng
MenuUI/DifficultyManager.cs                                          Main: Benjamin Fluharty, Contributors: Yu-Chang Cheng
MenuUI/Prefab/Display_Screen.prefab                                  Main: Yu-Chang Cheng
MenuUI/Prefab/OptionMenu.prefab                                      Main: Yu-Chang Cheng, Contributors: Benjamin Fluharty
MenuUI/Prefab/UICanvas - Credit Menu.prefab                          Main: Yu-Chang Cheng
MenuUI/Prefab/UICanvas - Credit Scrolling.prefab                     Main: Yu-Chang Cheng
MenuUI/Prefab/UICanvas - GameOver Menu.prefab                        Main: Yu-Chang Cheng
MenuUI/Prefab/UICanvas - Pause Menu.prefab                           Main: Yu-Chang Cheng
MenuUI/Prefab/UICanvas - Respawn Menu.prefab                         Main: Yu-Chang Cheng
MenuUI/Prefab/UICanvas - TitleMenu.prefab                            Main: Yu-Chang Cheng, Contributors: Benjamin Fluharty
MenuUI/ProjectorController.cs                                        Main: Yu-Chang Cheng, Contributors: Benjamin Fluharty
MenuUI/Respawn.anim                                                  Main: Yu-Chang Cheng, Contributors: Benjamin Fluharty
MenuUI/Scripts/ButtonScript.cs                                       Main: Yu-Chang Cheng, Contributors: Benjamin Fluharty
MenuUI/Scripts/CreditMenuToggle.cs                                   Main: Yu-Chang Cheng, Contributors: Benjamin Fluharty
MenuUI/Scripts/CreditScrollingUpdateText.cs                          Main: Yu-Chang Cheng, Contributors: Benjamin Fluharty
MenuUI/Scripts/PauseMenuToggle.cs                                    Main: Yu-Chang Cheng, Contributors: Benjamin Fluharty
MenuUI/Scripts/RespawnMenuControl.cs                                 Main: Yu-Chang Cheng, Contributors: Benjamin Fluharty
MenuUI/Scripts/RestartMenu.cs                                        Main: Benjamin Fluharty
MenuUI/Set_HUD_UI_per_State.cs                                       Main: Yu-Chang Cheng
MenuUI/StateNameController.cs                                        Main: Yu-Chang Cheng
MenuUI/ToggleGameObject.cs                                           Main: Yu-Chang Cheng
MenuUI/UICanvas - Respwan Menu.controller                            Main: Yu-Chang Cheng, Contributors: Benjamin Fluharty
Mesh/CircleRamp.fbx                                                  Main: Louis Russo
Mesh/Mech_Forest.fbx                                                 Main: Shane Moro
Mesh/smokestack.fbx                                                  Main: Shane Moro
Models/Enemies/Boss Drone.fbx                                        Main: Benjamin Fluharty
Models/Enemies/PA_ArchfireTank.fbx                                   Main: Benjamin Fluharty
Models/Enemies/PA_Drone.fbx                                          Main: Benjamin Fluharty
Physics/Boundary.physicMaterial                                      Main: Benjamin Fluharty
Physics/Drone.physicMaterial                                         Main: Benjamin Fluharty
Physics/Platform.physicMaterial                                      Main: Louis Russo
Prefab/3DEventSound.prefab                                           Main: Benjamin Fluharty
Prefab/BlueThrust.prefab                                             Main: Shane Moro
Prefab/CapacitorDecay.prefab                                         Main: Shane Moro
Prefab/Decorative Elements 1.prefab                                  Main: Benedicto da Silva
Prefab/Decorative Elements 2.prefab                                  Main: Benedicto da Silva
Prefab/DialogTrigger.prefab                                          Main: Louis Russo
Prefab/DroneSpawner.prefab                                           Main: Benjamin Fluharty
Prefab/EMP.prefab                                                    Main: Shane Moro, Contributors: Benjamin Fluharty
Prefab/EMPPickup.prefab                                              Main: Louis Russo
Prefab/EMP_Circle.prefab                                             Main: Shane Moro, Contributors: Benjamin Fluharty
Prefab/EmpRangeMarker.prefab                                         Main: Louis Russo
Prefab/EnemyCapacitorPower.prefab                                    Main: Shane Moro
Prefab/EnemyDoorPower.prefab                                         Main: Shane Moro
Prefab/EnemyShieldPower.prefab                                       Main: Benedicto da Silva
Prefab/EventSound.prefab                                             Main: Benjamin Fluharty
Prefab/GreenThrust.prefab                                            Main: Shane Moro
Prefab/HUD.prefab                                                    Main: Yu-Chang Cheng, Contributors: Louis Russo
Prefab/HeavyDrone.prefab                                             Main: Benjamin Fluharty
Prefab/HeavyLaser.prefab                                             Main: Benjamin Fluharty
Prefab/JetpackThrustColor_B.prefab                                   Main: Shane Moro
Prefab/Laser.prefab                                                  Main: Benedicto da Silva, Contributors: Benjamin Fluharty, Shane Moro
Prefab/LaserDeflection.prefab                                        Main: Benedicto da Silva
Prefab/Mainweapon_OD_Ring.prefab                                     Main: Shane Moro
Prefab/MechDecay.prefab                                              Main: Shane Moro
Prefab/MechWeaponImpact.prefab                                       Main: Shane Moro
Prefab/MechWeaponMain.prefab                                         Main: Shane Moro
Prefab/Mech_Forest.prefab                                            Main: Shane Moro, Contributors: Louis Russo
Prefab/PA_Drone.prefab                                               Main: Benjamin Fluharty Contributors: Benedicto da Silva, Louis Russo
Prefab/PlayerShield.prefab                                           Main: Benedicto da Silva, Contributors: Benjamin Fluharty
Prefab/ProjectorDecay.prefab                                         Main: Shane Moro
Prefab/ProjectorExplosion.prefab                                     Main: Shane Moro
Prefab/Puzzle3.prefab                                                Main: Louis Russo
Prefab/RespawnPortal.prefab                                          Main: Shane Moro
Prefab/ReticleBlue.prefab                                            Main: Shane Moro
Prefab/ShieldCoreDecay.prefab                                        Main: Shane Moro
Prefab/ShieldGenerator1.prefab                                       Main: Benedicto da Silva, Contributors: Louis Russo, Benjamin Fluharty
Prefab/ShieldGenerator2.prefab                                       Main: Benedicto da Silva, Contributors: Louis Russo, Benjamin Fluharty
Prefab/ShieldGenerator3.prefab                                       Main: Benedicto da Silva, Contributors: Louis Russo, Benjamin Fluharty
Prefab/ShieldGenerator4.prefab                                       Main: Louis Russo, Contributors: Benjamin Fluharty
Prefab/ShieldPickup.prefab                                           Main: Benedicto da Silva
Prefab/Smoke.prefab                                                  Main: Shane Moro
Prefab/SolarEnergyGate.prefab                                        Main: Benedicto da Silva, Contributors: Shane Moro
Prefab/SparkParticles.prefab                                         Main: Louis Russo
Prefab/Sun.prefab                                                    Main: Yu-Chang Cheng, Contributors: Shane Moro
Prefab/YellowGlowRing.prefab                                         Main: Shane Moro
Prefab/YellowThrust.prefab                                           Main: Shane Moro
Prefab/light/SparkEffect.prefab                                      Main: Louis Russo
ProjecterUI/Materials/Keyboard.mat                                   Main: Yu-Chang Cheng
ProjecterUI/Materials/KeyboardMap.mat                                Main: Yu-Chang Cheng
Scripts/AppEvents/BlueSquareEvent.cs                                 Main: Louis Russo
Scripts/AppEvents/BoxCollisionEvent.cs                               Main: Benjamin Fluharty
Scripts/AppEvents/CorrectGuessEvent.cs                               Main: Benjamin Fluharty
Scripts/AppEvents/DoorFallEvent.cs                                   Main: Benjamin Fluharty
Scripts/AppEvents/DroneAlertEvent.cs                                 Main: Benjamin Fluharty
Scripts/AppEvents/DroneDeadEvent.cs                                  Main: Benjamin Fluharty
Scripts/AppEvents/DroneHitEvent.cs                                   Main: Benjamin Fluharty
Scripts/AppEvents/DroneLaserEvent.cs                                 Main: Benjamin Fluharty
Scripts/AppEvents/DroneSpawnEvent.cs                                 Main: Benjamin Fluharty
Scripts/AppEvents/EMPEngageEvent.cs                                  Main: Benjamin Fluharty
Scripts/AppEvents/EMPPickupEvent.cs                                  Main: Benjamin Fluharty
Scripts/AppEvents/EnergyPickupEvent.cs                               Main: Benedicto da Silva, Contributors: Benjamin Fluharty
Scripts/AppEvents/EventManager.cs                                    Main: Prof. Jeff Wilson
Scripts/AppEvents/EventSound.cs                                      Main: Benjamin Fluharty
Scripts/AppEvents/EventSound3D.cs                                    Main: Benjamin Fluharty
Scripts/AppEvents/FinalExplosionEvent.cs                             Main: Benjamin Fluharty
Scripts/AppEvents/GreenSquareEvent.cs                                Main: Louis Russo
Scripts/AppEvents/KeyPressEvent.cs                                   Main: Louis Russo
Scripts/AppEvents/LaserImpactEvent.cs                                Main: Benjamin Fluharty
Scripts/AppEvents/MechBrakeEvent.cs                                  Main: Benjamin Fluharty
Scripts/AppEvents/MechHitEvent.cs                                    Main: Benjamin Fluharty
Scripts/AppEvents/MechJumpEvent.cs                                   Main: Benjamin Fluharty
Scripts/AppEvents/MechLandingEvent.cs                                Main: Benjamin Fluharty
Scripts/AppEvents/MechLaserEvent.cs                                  Main: Benjamin Fluharty
Scripts/AppEvents/MinimapMaxResizeEvent.cs                           Main: Louis Russo
Scripts/AppEvents/Puzzle3FailEvent.cs                                Main: Louis Russo
Scripts/AppEvents/RedSquareEvent.cs                                  Main: Louis Russo
Scripts/AppEvents/ShieldActivateEvent.cs                             Main: Louis Russo
Scripts/AppEvents/ShieldDamageEvent.cs                               Main: Benjamin Fluharty
Scripts/AppEvents/ShieldPickupEvent.cs                               Main: Benedicto da Silva, Contributors: Benjamin Fluharty
Scripts/AppEvents/ShieldShutdownEvent.cs                             Main: Benjamin Fluharty
Scripts/AppEvents/SolarPanelEvent.cs                                 Main: Benedicto da Silva
Scripts/AppEvents/SolvePuzzleEvent.cs                                Main: Benjamin Fluharty
Scripts/AppEvents/UIMessageEvent.cs                                  Main: Louis Russo
Scripts/AppEvents/YellowSquareEvent.cs                               Main: Louis Russo
Scripts/Enemies/Drone.cs                                             Main: Benjamin Fluharty, Contributors: Benedicto da Silva, Louis Russo, Yu-Chang Cheng, Shane Moro
Scripts/Enemies/DroneCounter.cs                                      Main: Yu-Chang Cheng
Scripts/Enemies/DronePerception.cs                                   Main: Benjamin Fluharty
Scripts/Enemies/DroneSpawn.cs                                        Main: Benjamin Fluharty
Scripts/Enemies/EnemyManager.cs                                      Main: Benjamin Fluharty
Scripts/Enemies/EnemySolarPanelCell.cs                               Main: Benedicto da Silva
Scripts/Enemies/EnergyBar.cs                                         Main: Benedicto da Silva, Contributors: Benjamin Fluharty
Scripts/Enemies/Laser.cs                                             Main: Benjamin Fluharty, Contributors: Benedicto da Silva
Scripts/Enemies/Shield/EnemySolarPanel.cs                            Main: Benedicto da Silva
Scripts/Enemies/Shield/Puzzle3/BlueSquareControl.cs                  Main: Louis Russo
Scripts/Enemies/Shield/Puzzle3/GreenSquareControl.cs                 Main: Louis Russo
Scripts/Enemies/Shield/Puzzle3/Puzzle3Control.cs                     Main: Louis Russo, Contributors: Benjamin Fluharty
Scripts/Enemies/Shield/Puzzle3/Puzzle3TriggerControl.cs              Main: Louis Russo
Scripts/Enemies/Shield/Puzzle3/RedSquareControl.cs                   Main: Louis Russo
Scripts/Enemies/Shield/Puzzle3/YellowSquareControl.cs                Main: Louis Russo
Scripts/Enemies/Shield/ShieldGenerator1Control.cs                    Main: Louis Russo, Contributors: Benedicto da Silva, Benjamin Fluharty, Yu-Chang Cheng
Scripts/Enemies/Shield/ShieldGenerator2Control.cs                    Main: Benjamin Fluharty, Contributors: Louis Russo, Benedicto da Silva, Yu-Chang Cheng
Scripts/Enemies/Shield/ShieldGenerator3Control.cs                    Main: Louis Russo, Contributors: Benedicto da Silva, Benjamin Fluharty, Yu-Chang Cheng
Scripts/Enemies/Shield/ShieldGenerator4Control.cs                    Main: Louis Russo, Contributors: Shane Moro
Scripts/Enemies/Shield/ShieldGeneratorControl.cs                     Main: Benedicto da Silva, Contributors: Louis Russo
Scripts/Enemies/Shield/ShieldManager.cs                              Main: Benedicto da Silva, Contributors: Louis Russo
Scripts/HUD/Dialog.cs                                                Main: Louis Russo
Scripts/HUD/DialogManager.cs                                         Main: Louis Russo, Contributors: Benjamin Fluharty
Scripts/HUD/DialogReturn.cs                                          Main: Louis Russo
Scripts/HUD/FPSCounter.cs                                            Main: Benedicto da Silva
Scripts/HUD/Minimap.cs                                               Main: Louis Russo, Contributors: Benjamin Fluharty
Scripts/HUD/PlayerMapControl.cs                                      Main: Louis Russo, Contributors: Benjamin Fluharty
Scripts/HUD/ProgressPanel.cs                                         Main: Louis Russo, Contributors: Benedicto da Silva
Scripts/HUD/UIManager.cs                                             Main: Louis Russo, Contributors: Benedicto da Silva, Yu-Chang Cheng, Benjamin Fluharty
Scripts/Pickups/EMPPickup.cs                                         Main: Louis Russo, Contributors: Benedicto da Silva, Benjamin Fluharty
Scripts/Pickups/EnergyPackController.cs                              Main: Benedicto da Silva, Contributors: Louis Russo, Benjamin Fluharty
Scripts/Pickups/IPickup.cs                                           Main: Benedicto da Silva, Contributors: Louis Russo
Scripts/Pickups/PickupAnimation.cs                                   Main: Louis Russo
Scripts/Pickups/PickupManager.cs                                     Main: Benedicto da Silva, Contributors: Louis Russo
Scripts/Pickups/PlayerShieldController.cs                            Main: Benedicto da Silva, Contributors: Benjamin Fluharty
Scripts/Pickups/ShieldPickupController.cs                            Main: Benedicto da Silva, Contributors: Louis Russo, Benjamin Fluharty
Scripts/Player/EMPControl.cs                                         Main: Louis Russo, Contributors: Benjamin Fluharty, Shane Moro
Scripts/Player/EMP_Animation.cs                                      Main: Shane Moro
Scripts/Player/GunController.cs                                      Main: Benjamin Fluharty, Contributors: Shane Moro
Scripts/Player/LaserDeflectionController.cs                          Main: Benedicto da Silva
Scripts/Player/MechDecay.cs                                          Main: Shane Moro
Scripts/Player/MechWeaponMain.cs                                     Main: Shane Moro, Contributors: Benjamin Fluharty
Scripts/Player/MovementController.cs                                 Main: Shane Moro, Contributors: Benjamin Fluharty
Scripts/Player/PlayerAttributes.cs                                   Main: Shane Moro, Contributors: Yu-Chang Cheng, Louis Russo, Benedicto da Silva, Benjamin Fluharty
Scripts/Player/PlayerTraining.cs                                     Main: Louis Russo
Scripts/Player/ReticleScript.cs                                      Main: Shane Moro
Scripts/Player/ThirdPersonCamera.cs                                  Main: Benedicto da Silva
Scripts/Sounds/AudioEventManager.cs                                  Main: Prof. Wilson, Contributors: Benjamin Fluharty, Louis Russo, Benedicto da Silva
Scripts/Training/IntroductionCompleteEvent.cs                        Main: Louis Russo
Scripts/Training/IntroductionEvent.cs                                Main: Louis Russo
Scripts/Training/TrainingCompleteEvent.cs                            Main: Louis Russo
Scripts/Training/TrainingManager.cs                                  Main: Louis Russo
Scripts/Training/TrainingQueryEvent.cs                               Main: Louis Russo
Scripts/Training/TrainingStep.cs                                     Main: Louis Russo
Scripts/Utilities/GameQuitter.cs                                     Main: Benedicto da Silva, Contributors: Yu-Chang Cheng
Scripts/Utilities/GameStarter.cs                                     Main: Benjamin Fluharty, Contributors: Benedicto da Silva, Yu-Chang Cheng
Scripts/Utilities/InputChecker.cs                                    Main: Benjamin Fluharty
Scripts/Utilities/MenuUISound.cs                                     Main: Yu-Chang Cheng, Contributors: Benjamin Fluharty
Scripts/Utilities/OptionMenu.cs                                      Main: Yu-Chang Cheng, Contributors: Benjamin Fluharty
Scripts/Utilities/PauseControl.cs                                    Main: Louis Russo, Contributors: Benjamin Fluharty
Scripts/Utilities/PressAnyKeyToContinue.cs                           Main: Yu-Chang Cheng
Scripts/Utilities/QuaternionUtil.cs                                  Main: Benedicto da Silva
Scripts/Utilities/SettingsMenu.cs                                    Main: Yu-Chang Cheng, Contributors: Benjamin Fluharty
Scripts/Utilities/Starter.cs                                         Main: Yu-Chang Cheng
Scripts/World/BuildingMain.cs                                        Main: Shane Moro, Contributors: Yu-Chang Cheng, Benjamin Fluharty
Scripts/World/ButterflyController.cs                                 Main: Shane Moro
Scripts/World/ButterflyGroupDead_RT.cs                               Main: Shane Moro
Scripts/World/CapacitorSolarPanel.cs                                 Main: Shane Moro
Scripts/World/CheckpointManager.cs                                   Main: Louis Russo, Contributors: Benjamin Fluharty
Scripts/World/ChoiceTrigger1Control.cs                               Main: Louis Russo
Scripts/World/CloudSpawner.cs                                        Main: Yu-Chang Cheng
Scripts/World/CrateCollisionReporter.cs                              Main: Benjamin Fluharty
Scripts/World/DeadPoolDoor.cs                                        Main: Shane Moro
Scripts/World/DeadpoolRender.cs                                      Main: Shane Moro, Contributors: Louis Russo
Scripts/World/DoorSolarPanel.cs                                      Main: Shane Moro, Contributors: Louis Russo
Scripts/World/EasyPathDroneRender.cs                                 Main: Shane Moro
Scripts/World/EndGameRender.cs                                       Main: Shane Moro, Contributors: Louis Russo
Scripts/World/FreshWaterRender.cs                                    Main: Shane Moro, Contributors: Louis Russo
Scripts/World/HardPathRender.cs                                      Main: Shane Moro, Contributors: Louis Russo
Scripts/World/Level2Enemies_RT.cs                                    Main: Shane Moro, Contributors: Louis Russo
Scripts/World/MechWeaponImpact.cs                                    Main: Shane Moro
Scripts/World/PlanetRotation.cs                                      Main: Benedicto da Silva, Contributors: Yu-Chang Cheng, Benjamin Fluharty
Scripts/World/PowerSourceCapacitor.cs                                Main: Shane Moro
Scripts/World/PowerSourceEMP.cs                                      Main: Shane Moro, Contributors: Benjamin Fluharty, Fluharty,
Scripts/World/Puzzle3DoorControl.cs                                  Main: Shane Moro
Scripts/World/RespawnPortal.cs                                       Main: Shane Moro
Scripts/World/Shield4Trigger.cs                                      Main: Louis Russo
Scripts/World/ShieldCoverDoor.cs                                     Main: Shane Moro
Scripts/World/ShieldGen3Door.cs                                      Main: Shane Moro
Scripts/World/ShieldTrigger.cs                                       Main: Benjamin Fluharty
Scripts/World/SmokeCreator.cs                                        Main: Shane Moro
Scripts/World/SmokeMovement.cs                                       Main: Shane Moro
Scripts/World/SunRays.cs                                             Main: Shane Moro, Contributors: Louis Russo, Benjamin Fluharty, Benedicto da Silva
Scripts/World/ToxicPoolRender.cs                                     Main: Shane Moro, Contributors: Louis Russo
Scripts/World/TutorialDoor.cs                                        Main: Shane Moro, Contributors: Benjamin Fluharty
Scripts/World/VegetaionFlowersRender.cs                              Main: Shane Moro
Scripts/World/VegetationGrassRender.cs                               Main: Shane Moro
Scripts/World/finalPowersource.cs                                    Main: Shane Moro


External Assets
Most code for the FPS display, EventManager, and AudioManager was used from the Milestone Projects.

Clouds
Unity Package: 3LE Low Poly Cloud Pack 
URL: https://assetstore.unity.com/packages/3d/3le-low-poly-cloud-pack-65911 
Author: The Fallout Nerd 
Version: 1.0 - July 05, 2016 

Vegetation
Unity Package: Low Poly Tree Pack 
URL: https://assetstore.unity.com/packages/3d/vegetation/trees/low-poly-tree-pack-57866 
Author: Broken Vector 
Version: 1.3 - July 02, 2018 

Butterflies
Unity Package: Butterfly (Animated)
URL: https://assetstore.unity.com/packages/3d/characters/animals/insects/butterfly-animated-58355
Author: INNOWELL GmbH
Version: 1.0

Various Laser Sounds for Combat and Movement
Unity Package: Free Laser Weapons
URL: https://assetstore.unity.com/packages/audio/sound-fx/weapons/free-laser-weapons-214929
Author: Daniel SoundsGood 
Version 1.0 - April 06, 2022

Ambience and Water Sounds
Unity Package: Nature - Essentials
URL: https://assetstore.unity.com/packages/audio/ambient/nature/nature-essentials-208227
Author: Nox_Sound
Version 1.2 - February 23, 2022

Drone Alert Sound
Unity Package: Sci-Fi Alarm SFX
URL: https://assetstore.unity.com/packages/audio/ambient/sci-fi/sci-fi-alarm-sfx-238043 
Author: Sound Works 12
Version 1.0 - December 01, 2022

Drone Model and Materials
Unity Package: SciFi Enemies and Vehicles
URL: https://assetstore.unity.com/packages/3d/characters/robots/scifi-enemies-and-vehicles-15159
Author: Popup Asylum
Version 1 - February 14, 2014

Mech Movement Sounds
Unity Package: Sci-Fi Units Rover
URL: https://assetstore.unity.com/packages/audio/sound-fx/sci-fi-units-rover-193829
Author: Sound Works 12
Version 1.0 - April 27, 2021

Box Collision Sounds
Unity Package: Close Contact
URL: https://assetstore.unity.com/packages/audio/sound-fx/close-contact-220142
Author: Rogue Waves
Version 1.0 - Apr 29, 2022

Several Audio Samples for the Mech, UI, and World Elements
Unity Package: Shapeforms Audio Free Sound Effects
URL: https://assetstore.unity.com/packages/audio/sound-fx/shapeforms-audio-free-sound-effects-183649
Author: Shapeforms
Version 1.1 - April 02, 2021

Drone Spawner Materials
Unity Package: Basic Metal Texture Pack 
https://assetstore.unity.com/packages/2d/textures-materials/metals/basic-metal-texture-pack-37402
Author: Joseph Steffensen 
Version 1.0 - April 14, 2016

Sound for Shield Damage
Unity Package: Shooting Sound
https://assetstore.unity.com/packages/audio/sound-fx/shooting-sound-177096
Author: B.G.M 
Version 1.0 - August 20, 2020

Title Menu Music
Unity Package: The Night Sky
URL: https://assetstore.unity.com/packages/audio/music/orchestral/the-night-sky-35720
Author: Olan
Version original - May 07, 2015

Mech Braking Sound Effect
Unity Package: UI - Mechanical (Free Sample Pack)
URL: https://assetstore.unity.com/packages/audio/sound-fx/ui-mechanical-free-sample-pack-148704
Author: InspectorJ Sound Effects
Version 1.0 - June 21, 2019

Game Background Music
Unity Package: Dark Atmospheric FREE TRACK Music Pack | Adaptive Tracks 
URL: https://assetstore.unity.com/packages/audio/music/electronic/dark-atmospheric-free-track-music-pack-adaptive-tracks-244634
Author: Composed Immersion 
Version 1.0 - March 03, 2023

Various UI Sounds
Unity Package: FREE Casual Game SFX Pack
URL: https://assetstore.unity.com/packages/audio/sound-fx/free-casual-game-sfx-pack-54116
Author: Dustyroom 
Version: 1.0 - March 04, 2019

Terrain Modeling Package
Unity Package: Terrain Toolkit 2017 
URL: https://assetstore.unity.com/packages/tools/terrain/terrain-toolkit-2017-83490 
Author: heparo 
Version: 20210314170000 - April 12, 2021 

Architecture (Building, Doors, Walls) 
Unity Package: Sci-Fi Styled Modular Pack 
Author: karboosx 
URL: https://assetstore.unity.com/packages/3d/environments/sci-fi/sci-fi-styled-modular-pack-82913
Version: 1.1 - November 05, 2018

Moving Vegetation 
Unity Package: Low Poly Wind 
Author: Nicrom 
URL: https://assetstore.unity.com/packages/vfx/shaders/low-poly-wind-182586 
Version: 1.2.0 - February 17, 2021

Trusses (Landing Pad) 
Unity Package: Aluminium truss systems free 
Author: Polistudio 
URL: https://assetstore.unity.com/packages/3d/environments/industrial/aluminium-truss-systems-free-128696 
Version: 1.0 - January 21, 2019

Water Environments 
Unity Package: LowPoly Water 
Author: Ebru Dogan 
URL: https://assetstore.unity.com/packages/tools/particles-effects/lowpoly-water-107563 
Version: 1.0.0 - January 18, 2018

Shipping Containers 
Unity Package: Megapoly.Art - Containers 
Author: Megapoly Art 
URL: https://assetstore.unity.com/packages/3d/props/megapoly-art-containers-197278 
Version: 1.0 - October 1, 2021

VFX – Mech Weapon, Mech Boosters, Explosions 
Unity Package: Magic Effects FREE 
Author: Hovl Studio 
URL: https://assetstore.unity.com/packages/vfx/particles/spells/magic-effects-bundle-247933 
Version: 1.0 - February 26, 2023

Radioactive Signs
Unity Package: Three signs (ISO 7010) 
Author: Pirate Parrot (www.pirateparrot.net)
URL: https://assetstore.unity.com/packages/3d/props/exterior/three-signs-iso-7010-188492 
Version: 1.0 - November 17, 2021

UI Click Sound
Sound: 157871__orginaljun__arcade-button-1-click-sound.mp3 
URL: https://freesound.org/people/orginaljun/sounds/157871/ 
Author: orginaljun 

Solar Panel Crash Audio Clip
Sound: metallic crash.wav 
URL: https://freesound.org/people/BehanSean/sounds/422438/ 
Author: Behan Sean 

Popup Typing Sound Effect
Sound: click-21156.mp3 
URL: https://cdn.pixabay.com/download/audio/2022/02/17/audio_988aaf064c.mp3?filename=click-21156.mp3 

Vehicle Tire Movement 
Author:  b3agz 
URL: https://www.youtube.com/watch?v=QQs9MWLU_tU 

Menu and UI Images
Image: heart.png 
URL: https://download.services.iconscout.com/download?name=heart&download=1&url=https%3A%2F%2Fd1b1fjiwh8olf2.cloudfront.net%2Ficon%2Ffree%2Fpng-512%2F76703.png%3Ftoken%3DeyJhbGciOiJoczI1NiIsImtpZCI6ImRlZmF1bHQifQ__.eyJpc3MiOiJkMWIxZmppd2g4b2xmMi5jbG91ZGZyb250Lm5ldCIsImV4cCI6MTY3OTI3MDQwMCwicSI6bnVsbCwiaWF0IjoxNjc5MDIyNzY0fQ__.ef49ded277eaab3ab0c068632bae1f5424ffa0d91c1451c76ba645f2fa58f721&width=512&height=512 

Image: sci-fi_background.png 
URL: https://i.pinimg.com/736x/b7/87/c9/b787c9a7e233e120a834242f5bfd4046.jpg 

Image: drone_icon.png 
URL: https://download.favpng.com/api_download.php?k=vKzisgqz 

Video/ Sound for Trailer Video: ROYALTY FREE Cinematic Trailer Music Cinematic Trailer Background Music by MUSIC4VIDEO.mp4
URL: https://www.youtube.com/watch?v=knRAM6AHcKI&ab_channel=MusicforVideoLibrary

