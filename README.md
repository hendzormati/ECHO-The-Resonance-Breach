# ECHØ: The Resonance Breach

ECHØ is a first-person exploration and horror prototype built with Unreal Engine. The player wakes up in a dark industrial corridor and recovers a handheld resonator. Holding one of its three frequency controls reveals the surrounding environment and produces a distinct sound.

The current playable scene includes the wakeup sequence, movement, resonator pickup, an information display and three emission ranges. The scene includes layered industrial ambience, wakeup breathing and cloth foley, varied metal footsteps, landing sounds, resonator control clicks and a spatial sound around the fog. The full game remains in development.

## Requirements

- Windows with Unreal Engine 5.6.1 installed.
- The project content and the character dependencies described below.

## Running the project

1. Download the repository and keep the `ECHO` folder structure intact.
2. Keep the character pack under `ECHO/Content/Medieval_Assassin_Girl` and the adapted assets under `ECHO/Content/ECHO/Characters/Assassin`. Both are used by the playable character. See the licence table before publishing third-party source assets.
3. Open [ECHO/ECHO.uproject](ECHO/ECHO.uproject). If Unreal requests an engine association, select the installed Unreal Engine 5.6 version.
4. Allow the initial shader compilation to finish.
5. Open `/Game/ECHO/Maps/L_01_Wakeup/L_01_Wakeup` if it is not already loaded, then press **Play**. The introduction lasts approximately 16 seconds before player control resumes.

The playable character uses Free Medieval Assassin Girl with separate trousers, boots, sleeves, a vest and hair. Weapons, bags, hood and mask are omitted, and the clothing uses muted fabric materials. The wakeup, locomotion, jump, pickup, carrying and inspection animations have been adapted to this skeleton. The previous Survival Character assets are excluded and are no longer required by the wakeup scene.

Animation work remains in development. Independent crouching, lying down, death, dropping objects and physical button presses are not implemented.

## Controls

| Input | Action |
| --- | --- |
| ZQSD / arrow keys | Move |
| Mouse | Look around |
| Space | Jump |
| Left Shift | Run while held |
| G | Pick up the resonator when prompted |
| I | Open or close the resonator information display |
| Hold L | Low frequency, 5 m range |
| Hold M | Medium frequency, 7 m range |
| Hold H | High frequency, 12 m range |
| Release the frequency key | Stop emission and restore normal visibility |

## Background theme

/Game/ECHO/Audio/Music/SW_ECHO_MainTheme is the shared background theme. It starts during the black screen, fades in as the player wakes up and continues throughout the corridor.

BP_ECHO_ThemePlayer uses the project Game Instance to keep one music player across level changes. Future launch and menu maps can use the same actor without restarting or stacking the theme.


The fog exit is temporarily playable: walking past the corridor edge triggers a fall, a short fade to black, and a restart of the wake-up scene. The next level is not connected yet.

## Optional animation library

The local Game Animation Sample profile replaces idle, eight-direction walking and running, jump start, falling and landing. BP_ECHO_Player loads ABP_ECHO_Advanced from ECHO/Characters/Assassin/Animations/GASP/Runtime through a soft class reference. If that class is unavailable, the original ABP_ECHO_UnarmedCarry remains active. Set UseAdvancedAnimations to false to select the original profile.

The seated wakeup and resonator pickup still use provisional animations. Crouch and traversal clips are available locally but their gameplay is not enabled by this replacement. Throwing, hit reactions, death and weapon handling require additional animation assets and gameplay implementation.

Game Animation Sample was obtained under the [Fab Standard License](https://www.fab.com/eula). Its source assets and retargeted derivatives are excluded from this public repository. They may be incorporated into a packaged game; do not publish a separate reusable animation archive alongside the APK or executable. Local animation backups are private and excluded from Git.

To reproduce the advanced profile on another development PC, obtain [Game Animation Sample](https://www.fab.com/listings/880e319a-a59e-4ed2-b268-b32dac7fa016) for Unreal Engine 5.6. Restore the private Runtime folder with its project dependencies through Unreal's Migrate tool. Without that local profile, the public project uses its original animations.

## Assets and licences

Third-party assets retain their respective licences. The table distinguishes assets used in the scene from downloads awaiting integration.

| Resource | Author | Licence | Use |
| --- | --- | --- | --- |
| [Unreal Engine First Person template and mannequin](https://www.unrealengine.com/eula/unreal) | Epic Games | Unreal Engine EULA | Player foundation and animation sources |
| [SICKA Free Environment Pack](https://www.fab.com/listings/2ae68053-14c9-4849-9565-2e1d16a595ba) | SICKA | CC-BY reported at acquisition; exact terms still to confirm | Corridor environment; scene layout, lighting and material instances modified |
| [Free Medieval Assassin Girl](https://www.fab.com/listings/2986b290-90ed-4a0e-a891-cacf442033f9) | Dimentrius3dArtist | CC-BY indicated at download; coverage of the Unreal package still to confirm | Playable and cinematic character; opaque shirt and layered clothing, materials, animation retargeting and hand poses modified |
| [Breathing (male)](https://freesound.org/people/dav0r/sounds/346932/) | dav0r | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | Wakeup breathing; excerpted and played with adjusted pitch |
| [Forcefield Ambience](https://freesound.org/people/Thimblerig/sounds/467727/) | Thimblerig | CC0 1.0 | Spatial breach ambience, fog entry and texture in the three emission loops; edited and mixed |
| [Footsteps on Metal](https://freesound.org/people/IENBA/sounds/698697/) | IENBA | CC0 1.0 | Six edited metal footstep variants and landing foley |
| [Dark sci-fi ambient bass synth drone 004](https://freesound.org/people/pryanic/sounds/777039/) | pryanic | CC0 1.0 | Shared main theme; stereo excerpt with a loop crossfade and normalized level |
| [Atmosphere Scifi Bunker Loop Stereo](https://freesound.org/people/Nox_Sound/sounds/817225/) | Nox_Sound | CC0 1.0 | Industrial corridor ventilation; edited into a loop |
| [Wild Cloth Movement for Foley](https://freesound.org/people/CHallSmith/sounds/870604/) | CHallSmith | CC0 1.0 | Wakeup, standing, jump and pickup clothing foley; three edited excerpts |
| [Impact Sounds](https://kenney.nl/assets/impact-sounds) and [Interface Sounds](https://kenney.nl/assets/interface-sounds) | Kenney | CC0 1.0 | Downloaded; not yet used in gameplay |
| Resonator model, materials and synthesized emission loops | ECHØ project | Original project assets | Used in the playable scene |
| [Game Animation Sample](https://www.fab.com/listings/880e319a-a59e-4ed2-b268-b32dac7fa016) | Epic Games | [Fab Standard License](https://www.fab.com/eula) | Optional local animation profile; sources and derivatives excluded from public Git |

For assets covered by [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), redistribution requires appropriate credit, a link to the licence and an indication of modifications. Licence confirmation remains necessary for the entries marked above before their source assets are published.
