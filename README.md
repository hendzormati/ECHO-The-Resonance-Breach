# ECHØ: The Resonance Breach

ECHØ is a first-person exploration and horror prototype built with Unreal Engine. The player wakes up in a dark industrial corridor and recovers a handheld resonator. Holding one of its three frequency controls reveals the surrounding environment and produces a distinct sound.

The current playable scene includes the wakeup sequence, movement, resonator pickup, an information display and three emission ranges. The full game and environmental soundscape are still in development.

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

## Assets and licences

Third-party assets retain their respective licences. The table distinguishes assets used in the scene from downloads awaiting integration.

| Resource | Author | Licence | Use |
| --- | --- | --- | --- |
| [Unreal Engine First Person template and mannequin](https://www.unrealengine.com/eula/unreal) | Epic Games | Unreal Engine EULA | Player foundation and animation sources |
| [SICKA Free Environment Pack](https://www.fab.com/listings/2ae68053-14c9-4849-9565-2e1d16a595ba) | SICKA | CC-BY reported at acquisition; exact terms still to confirm | Corridor environment; scene layout, lighting and material instances modified |
| [Free Medieval Assassin Girl](https://www.fab.com/listings/2986b290-90ed-4a0e-a891-cacf442033f9) | Dimentrius3dArtist | CC-BY indicated at download; coverage of the Unreal package still to confirm | Playable and cinematic character; clothing selection, materials, animation retargeting and hand poses modified |
| [Breathing (male)](https://freesound.org/people/dav0r/sounds/346932/) | dav0r | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) | Downloaded; not yet used in gameplay |
| [Forcefield Ambience](https://freesound.org/people/Thimblerig/sounds/467727/) | Thimblerig | CC0 1.0 | Downloaded; not yet used in gameplay |
| [Footsteps on Metal](https://freesound.org/people/IENBA/sounds/698697/) | IENBA | CC0 1.0 | Downloaded; not yet used in gameplay |
| [Dark sci-fi ambient bass synth drone 004](https://freesound.org/people/pryanic/sounds/777039/) | pryanic | CC0 1.0 | Downloaded; not yet used in gameplay |
| [Atmosphere Scifi Bunker Loop Stereo](https://freesound.org/people/Nox_Sound/sounds/817225/) | Nox_Sound | CC0 1.0 | Downloaded; not yet used in gameplay |
| [Wild Cloth Movement for Foley](https://freesound.org/people/CHallSmith/sounds/870604/) | CHallSmith | CC0 1.0 | Downloaded; not yet used in gameplay |
| [Impact Sounds](https://kenney.nl/assets/impact-sounds) and [Interface Sounds](https://kenney.nl/assets/interface-sounds) | Kenney | CC0 1.0 | Downloaded; not yet used in gameplay |
| Resonator model, materials and synthesized emission loops | ECHØ project | Original project assets | Used in the playable scene |

For assets covered by [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), redistribution requires appropriate credit, a link to the licence and an indication of modifications. Licence confirmation remains necessary for the entries marked above before their source assets are published.
