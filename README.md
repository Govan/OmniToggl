# OmniToggl
A omnifocus plugin to seamlessly start and stop [Toggl](https://track.toggl.com/timer) timers from inside [OmniFocus](https://www.omnigroup.com/omnifocus/)

## What it does


![Example](img/Dec-29-2020-18-58-28.gif)


When you highlight a task or project in OmniFocus and then kick off this automation, a timer will be started with:
- Description as the name of the task or project
- Tags copied over from OmniFocus
- Project used from the task the project is contained in, or the project itself, within OmniFocus. The script will create a new Project if the project doesn't exist in Toggl.
- A tag of `<x>m` where `x` is the duration in minutes, a default of `15m` applies to any item with no duration - I use this as part of my [Huginn](https://github.com/huginn/huginn) setup.

## Requriements
- Omnifocus Pro with Automation activated
- For iOS you need the Omnifocus version > 3.11.2.
- A Toggl Account [Sign up here](https://track.toggl.com/timer)

## How to install on Mac
1. Clone the repo
2. Open the file called `OmniToggl.omnifocusjs` this should open the file in OmniFocus
3. Choose if you would like to install on Mac (to only use locally) or "OmniFocus in iCloud Drive" (to make it available across platforms (including iPhone and iPad)
![Omnifocus Dialog](img/Screenshot-1.png)
4. Choose Automation > Configure in the menu
5. Choose `OmniToggl` in menu and click `Reveal in Finder`
![Omnifocus Dialog](img/Screenshot-3.png)
6. In finder right click on OmniToggl.omnifocusjs and select `Show Package Contents`
![Omnifocus Dialog](img/Screenshot-4.png)
7. Open `Resources/common.js` in your favourite text editor
![Omnifocus Dialog](img/Screenshot-6.png)
8. Replace 'REPLACE_ME' with your toggl API Token that can be found [here](https://track.toggl.com/profile)
9. Replace 'REPLACE_ME_TOO' with your [workspace id](https://developers.track.toggl.com/docs/workspace)
10. Quit and Restart OmniFocus
11. You should now be all set up and can start a timer by clicking on a task and choosing Automation > OmniToggle > Start Timer from the menu.

Note: if anyone knows of a way to store data other then having to edit a file as described then please let me know as it seems it should be easier then this but the documentation is not great.
