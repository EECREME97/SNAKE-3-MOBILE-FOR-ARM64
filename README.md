# SNAKE-3-MOBILE-FOR-ARM64
PORT OF THE CLASIC JAVA PHONE GAME SNAKE 3 
Snake III — Native ARM64 Port
A native, high-performance ARM64 reimplementation of Nokia’s 3D reinvention of the classic Snake formula: Snake III (also known as Snake 3D), originally released in 2005.
No emulators. No wrappers. Just pure, compiled-for-ARM64 code slithering through 3D mazes, chasing fruit, and dueling friends over Bluetooth.

https://via.placeholder.com/800x400?text=Replace+with+your+Snake+III+screenshot

📖 About the Game
Snake III is not just another blocky Snake clone. Released by Nokia in November 2005 for Series 40 J2ME feature phones, it took the beloved formula and gave it a third dimension, a living, breathing snake, and a set of game modes that went far beyond “eat and grow.” It shipped pre-installed on phones like the Nokia 3250, and its Bluetooth multiplayer was an unusual and impressive feat for a mobile game of its era.

Kotaku described it as taking “a more living snake approach, rather than the abstract feel” of earlier entries. Instead of a simple line on a flat grid, you were guiding a 3D serpent through actual mazes, with depth, obstacles, and a real sense of space.

This project is a ground-up native ARM64 port of that 2005 classic. It preserves the 3D maze navigation, the three distinct modes, and the local two-player battles, while replacing the J2ME runtime with a lean, native engine built for ARM64 hardware.

🎮 Gameplay Explained
The goal of Snake III is to navigate a three-dimensional maze, consume fruit and bonuses, grow your snake, and either survive as long as possible or outmaneuver a rival in local multiplayer.

Mechanic	How it works
3D Maze Navigation	Unlike the flat grids of Snake and Snake II, Snake III places you inside a three-dimensional labyrinth. You must steer through corridors, around corners, and across depth—not just left and right.
Classic Mode	The pure survival experience: avoid obstacles, eat fruit, and grow as long as you can. The familiar loop, reimagined in 3D.
Adventure Mode	A progression-based mode where you must grow large enough to advance from screen to screen. Each stage demands a different length or performance before you can move on.
Custom Mode	A level editor. Build your own mazes and challenges, then play them. The original game let you edit your own levels, a rare feature for a 2005 mobile title.
Local Multiplayer (Bluetooth)	Two players on separate phones connect via Bluetooth and navigate the same 3D maze simultaneously, competing head-to-head in snake battles.
Obstacles & Bonuses	The mazes are filled with obstacles to avoid and bonus items beyond standard fruit, adding risk and reward to every route.
High Scores	Track your best runs and see how you improve over time.
The three modes give Snake III a surprising amount of longevity for a feature-phone game: a quick arcade fix, a structured campaign, and a creative sandbox—plus the social pull of Bluetooth duels.

⚡ Why a Native ARM64 Port?
This is not an emulator or a compatibility layer. The game logic has been recompiled and optimized to run directly on ARM64 CPUs (Apple Silicon, modern Android devices, ARM64 Linux handhelds, etc.).

What that means for you:

Fluid 3D movement — navigating a 3D maze demands consistent frame pacing; native execution delivers it without the stutter of an emulated J2ME runtime.

Instant directional input — tight turns and quick reactions are essential in Snake III; native input handling removes the lag of a virtual keypad layer.

Local multiplayer, reimagined — the original Bluetooth battles can be replaced with native local networking (or shared-device two-player), depending on your implementation, without emulator networking quirks.

Crisp 3D visuals at any resolution — from a phone screen to a desktop monitor, the mazes and the snake render sharply.

Native save system — high scores, custom levels, and progress are stored locally in a modern, portable format.

Touch, keyboard, and gamepad ready — the directional control scheme translates naturally to any input method.

🕹️ Controls
Action	Touch / Mouse	Keyboard	Gamepad
Move snake	Swipe / on-screen D-pad	Arrow keys / WASD	D-pad / Left stick
Confirm / Select	Tap	Enter	A / Cross
Back / Pause	On-screen button	Esc	B / Circle
Open menu	Tap menu icon	M	Start / Options
(Keyboard shortcuts are remappable in the settings menu.)

🛠️ Building from Source
Prerequisites
A C/C++ toolchain targeting ARM64 (e.g., aarch64-linux-gnu-gcc, Clang with --target=aarch64-linux-gnu, or Xcode for Apple Silicon).

CMake 3.20+ (or your preferred build system).

SDL2 or a comparable native windowing/input library.

(Optional) A networking library if you implement local multiplayer over LAN.

Quick build (Linux ARM64)
bash
git clone https://github.com/yourusername/snake-iii-arm64.git
cd snake-iii-arm64
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make -j$(nproc)
./snake-iii
Cross-compiling for Apple Silicon (macOS)
bash
cmake .. -DCMAKE_OSX_ARCHITECTURES=arm64 -DCMAKE_BUILD_TYPE=Release
make -j$(sysctl -n hw.ncpu)
Note: Replace yourusername with your actual GitHub username. If you use a different build system (Makefile, Meson, etc.), adjust the instructions accordingly.

📦 Downloads
Pre-built binaries are available on the Releases page.

Platform	Architecture	Format
Linux	ARM64	.tar.gz
macOS	Apple Silicon (ARM64)	.app / .dmg
Android	ARM64-v8a	.apk
🙏 Credits
Original Game: Snake III (2005), developed and published by Nokia Oyj. Also known as Snake 3D.

Native ARM64 Port: [Your Name / Your Handle]

Special Thanks: Nokia’s internal game teams for pushing the Snake formula into 3D, and the J2ME preservation community for keeping these titles playable and documented.

This is a fan-made preservation project. It is not affiliated with or endorsed by Nokia or any successor rights holders.

📄 License
The source code of this native port is released under the MIT License.
The original game assets and design remain the property of their respective copyright holders. This project is intended for educational and preservation purposes only.

⭐ Contributing
Found a bug? Want to add a custom-level editor, native LAN multiplayer, or controller remapping?
Pull requests and issue reports are welcome. Please open an issue before submitting large changes.

If this project brought back memories of navigating Nokia’s first 3D snake maze—or battling a friend over Bluetooth—consider giving it a ⭐. It helps more people find the port.

