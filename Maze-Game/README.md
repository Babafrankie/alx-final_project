# 3D Maze
### Creating a 3D maze with raycasting
[Here](https://fnwandibie.wixsite.com/osaze3dmaze) you can go to the deployed site           
[Here](https://medium.com/@fnwandibie/learning-game-development-through-a-maze-game-e0e5d84bb123) you can find a blog I made                
[Here](https://www.linkedin.com/in/osaze-nwandibie/) you can find my Linkedin profile

![textured_1](https://github.com/Babafrankie/alx_3D-Maze_Final-Project)
-----

### Table of Content
* [Purpose](#purpose)
* [Inspiration](#inspiration)
* [Data Flow](#data-flow)
* [Environment](#environment)
* [Installation](#installation)
* [Usage](#usage)
* [To-Do](#to-do)
* [Challenges](#challenges)
* [Contributing](#contributing)
* [Related Projects](#related-projects)
* [Resources](#resources)
* [Authors](#authors)
* [License](#license)
-----

### Purpose
The purpose of these projects extended beyond personal fulfillment. I aimed to showcase my proficiency in graphics programming, particularly with the SDL2 library, and highlight my ability to construct engaging and visually striking environments. Moreover, I wanted to provide a platform for individuals to experience the thrill of navigating through intricate mazes, triggering a sense of nostalgia for those who grew up playing similar games.
-----

### Inspiration
The inspiration for these 3D Maze portfolio projects originated from my fascination with classic video games, particularly those that employed innovative techniques to create immersive environments. Games like Wolfenstein 3D and Doom, which utilized raycasting algorithms, captivated me with their ability to simulate 3D spaces using 2D grids. I wanted to explore and recreate this mesmerizing effect, while simultaneously demonstrating my skills and creativity as a developer.
-----

### Beneficiaries of the Project and Personal Focus:
The 3D Maze portfolio projects cater to a wide range of beneficiaries. Gaming enthusiasts can relish the opportunity to immerse themselves in a nostalgic gaming experience, while aspiring developers can learn from the underlying techniques and gain insights into the implementation of 3D graphics using raycasting. Additionally, recruiters and potential employers can assess my programming abilities and witness my dedication to creating polished and innovative projects.
Throughout the development of these projects, my personal focus revolved around three key aspects:

1. User Experience (UX): I wanted to ensure that the gameplay experience was intuitive, smooth, and visually pleasing. Paying attention to details such as responsive controls, optimized performance, and immersive audio contributed to an enjoyable experience for the players.

2. Code Quality and Modularity: Emphasizing clean and maintainable code was paramount. I aimed to structure the codebase in a modular fashion, allowing for easy expansion and customization. This approach facilitates future enhancements and makes collaboration with other developers more seamless.

3. Visual Appeal: Creating an aesthetically pleasing environment was essential. Attention was given to designing visually striking mazes with varied textures, lighting effects, and atmospheric elements. Balancing performance with graphical fidelity was a constant challenge, requiring careful optimization techniques.
-----

### Data Flow
![maze_architecture](https://miro.medium.com/v2/resize:fit:720/format:webp/1*5IExnwq2013nxkPCTx8_Og.png)
-----

### Environment
This game uses Simple DirectMedia Layer (SDL2) and Raycasting
- [SDL2](https://www.libsdl.org/download-2.0.php) and [SDL2_image](https://www.libsdl.org/projects/SDL_image/) are required to compile and use this program
-----

### Installation
- Clone this repository: `git clone "https://github.com/Babafrankie/alx-final_project/Maze-Game"`
- Access The Maze directory: `cd Maze-Game`
- Compile the files with: `make all`
- Run the maze: `./maze` or `./maze maps/<map_name>`
- Disable textures: `./maze no_tex` or `./maze maps/<map_name> no_tex`

-----

### Usage
This 3D maze uses raycasting to draw the maze walls, utilizing [LodeV's](http://lodev.org/cgtutor/raycasting.html) method of using vectors to calculate ray length. By default the maze uses textures but textures can be disabled on execution.

#### Controls
- `W` or `↑` : move forward
- `S` or `↓` : move backward
- `A` or `←` : rotate camera left
- `D` or `→` : rotate camera right
- `Q` : strafe left
- `E` : strafe right
- `F` : toggle fullscreen
- `ESC` : quit

![textured_3](https://github.com/Babafrankie/Maze-Game/blob/main/screenshots/textured_3.png)

#### Maps
The maps are defined in 2D arrays in text files, which are parsed when passed as an argument to the maze executable. `0` represents open space, all other integers are drawn as walls.

Example:
```
1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1
1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 0 0 0 0 0 2 2 2 2 2 0 0 0 0 3 0 3 0 3 0 0 0 1
1 0 0 0 0 0 2 0 0 0 2 0 0 0 0 0 0 0 0 0 0 0 0 1
1 0 0 0 0 0 2 0 0 0 2 0 0 0 0 3 0 0 0 3 0 0 0 1
1 0 0 0 0 0 2 0 0 0 2 0 0 0 0 0 0 0 0 0 0 0 0 1
1 0 0 0 0 0 2 2 0 2 2 0 0 0 0 3 0 3 0 3 0 0 0 1
1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 4 4 4 4 4 4 4 4 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 4 0 4 0 0 0 0 4 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 4 0 0 0 0 5 0 4 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 4 0 4 0 0 0 0 4 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 4 0 4 4 4 4 4 4 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 4 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 4 4 4 4 4 4 4 4 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1
1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1
```

### To-Do
- Improved map parser
- Better error handling
- More textures
- Enemies / obstacles / objects
- Maze goal that loads next map
- Rain

### Challenges
The most challenging technical issue was something I had not foreseen at all. To my utter surprise, the trickiest part of the whole project was the concept behind ray casting, a technique used in this project to render the maze’s image onto the window. The concept of ray casting involves many high school math geometry principles, which have completely evaporated from my head. As a result of this new finding, I had to alter my plan and spent most of my time reading up on these trigonometric concepts. This left me with less time to build the actual project. However, my understanding of the concepts behind ray casting helped make coding a bit faster, not barring the fact that I had to take time away from my sleep.

### Contributing
For submitting patches and additions, please follow the "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull request** so that I can review your changes

NOTE: Be sure to merge the latest from "upstream" before making a pull request!

-----

### Related Projects
This project is similar to Wolfenstein and Doom

![](https://www.sapphirenation.net/-/media/sites/sapphirenation/articles/2017/09/Wolf-3d-gameplay.jpg)
![](https://cdn.cloudflare.steamstatic.com/steam/apps/2280/ss_04a2879c2d052e9fb4a50380ddb00f660cc19dc3.600x338.jpg?t=1600098964)
-----

### Resources
- [SDL2 API](https://wiki.libsdl.org/CategoryAPI)
- [LazyFoo Beginning Game Programming](http://lazyfoo.net/tutorials/SDL/index.php)
- [Ray-Casting Tutorial For Game Development And Other Purposes by F. Permadi](http://permadi.com/1996/05/ray-casting-tutorial-table-of-contents/)
- [LodeV Raycasting Tutorial](http://lodev.org/cgtutor/raycasting.html)
- [Game Engine Black Book](https://www.amazon.com/Game-Engine-Black-Book-Wolfenstein/dp/1539692876)
-----

### Authors
Osaze Frank Nwandibie - [Github](https://github.com/Babafrankie)

### License
Public Domain. No copy write protection.
