# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Janice Kim**

Time spent: **1.5** hours spent in total

Link to project: https://glitch.com/edit/#!/zircon-pale-peanut

## Required Functionality

The following **required** functionality is complete:

* [X] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [X] "Start" button toggles between "Start" and "Stop" when clicked. 
* [X] Game buttons each light up and play a sound when clicked. 
* [X] Computer plays back sequence of clues including sound and visual cue for each button
* [X] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [X] User wins the game after guessing a complete pattern
* [X] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [X] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [ ] Buttons use a pitch (frequency) other than the ones in the tutorial
* [ ] More than 4 functional game buttons
* [ ] Playback speeds up on each turn
* [X] Computer picks a different pattern each time the game is played
* [X] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [X] Game has images corresponding to number of lives left (mistakes)

## Video Walkthrough (GIF)
https://i.imgur.com/GnaYN53.gifv

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 
No outside resources used.

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 
A challenge I encountered in creating this submission was connecting the JavaScript function to HTML elements. Intially, I found that the playClueSequence() function was not properly running because when I pressed the start button, the buttons would not light up or make a sound to display the pattern. I tried adding a print statement to the startGame(), which allowed me to see that the playClueSequence() function was not running properly when the user pressed the button. I was also to inspect the page and see that the pattern was not being played. After inspecting the HTML of the buttons and tracing the code ofthe playClueSequence() function, I realized that the buttons were not being animated due to the id names I had given them. I initially named the buttons with the numbers written out, for example buttonOne instead of button1. As a result, the pattern didn't correspond to the id names of the buttons in the HTML file, as the lightButton(btn) function takes in each integer in the pattern array then animates the corresponding button by concatenating the number to the string button, forming the id of the button. I was able to fix this bug by changing the names of the ids of the buttons then correcting the corresponding CSS selectors in the CSS file. From this challenge, I learned the importance of retracing my steps and looking at the details in order to ensure that across files, different id selectors, variables, and names correspond such that the web application works properly.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 
After completing my submission, I have questions on how a leaderboard for the memory game could be created--how can information be stored when a web application refreshes in order to save scores (for example, the number of correct buttons of the pattern). I'm curious to explore how data is stored across different users of the same web application. Another question expanding on this idea of a leaderboard is where this data is stored? How can we keep track of names affiliated with high scores and where does this information go? Is there a separate software necessary that we need to include to store this data? The last question I have is how sequences can continue until the user is unable to remember the pattern. How can we continuously generate a pattern or content for the user as the user is actively playing the game? How can the content of a webpage be dynamic and respond to the user?

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 
If I had more time to work on this project, I would style the elements to reflect an 8-bit game, creating custom SVG graphics so that I could change the color of the buttons easily using CSS selectors. This way, the design of the game would be cohesive and enhance user experience. Another change I would make is adding more sound effects and change the game button sounds to a sequence of multiple tones. For examples, I would add a sound effect when starting the game, when the user either wins or loses, when the user pauses the game, and light background music for when the game has started. Lastly, I would spend some time creating a new feature where the user can store and save a sequence they create to be used as a game sequence for a friend. This would involve perhaps adding a button that would allow the user to "record" a sequence of length 8 by pressing the buttons in order. This ordering could be stored in an array then set as the pattern for the next player. This feature would be super fun, as it would allow the user to create various patterns or even recognizable patterns based on tones!



## Interview Recording URL Link

[My 5-minute Interview Recording](your-link-here)


## License

    Copyright [Janice Kim]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
