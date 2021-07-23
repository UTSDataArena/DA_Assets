# Data Arena Assets

#### Unreal Engine 4 plugin for the UTS Data Arena
The DA Assets plugin allows easy access to input devices used in the [UTS Data Arena](https://dataarena.net) theatre. Currently classes include access to our 3DConnexion SpaceMouse, and up to 8 trackers in our Optitrack Motion Capture system. Include this plugin in your project to quickly utilise our immersive input interfaces and take your project to the next level.

> 👉 We have locked off support for **Unreal Engine 4.25** projects (as of July 2021). We are currently working on more recent versions of the engine but for now require projects built in **4.25.4** or older.

## 🖲 Currently supported devices

#### 3DConnexion SpaceMouse
Our six degree-of-freedom SpaceMouse is commonly used for wireless navigation of 3D scenes in the Data Arena. The [SpaceMouse](https://3dconnexion.com/uk/product/spacemouse-wireless/) provides high precision translation and rotation movements in X, Y and Z dimensions, as well as two function buttons. Our main use for the SpaceMouse is virtual camera control. The included `SpaceMouseCamera` actor will add a standard [Camera Actor](https://docs.unrealengine.com/4.26/en-US/Basics/Actors/CameraActors/) to your project with pre-defined SpaceMouse axis bindings for steering and access to axis sensitivity and friction control in the details panel. Of course, you aren't limited to camera control and can make use of the SpaceMouse channels however you wish by simply adding the `DA_SpaceMouse` actor to your project.

#### Motion Capture Trackers
The Data Arena has 12-camera Optitrack Motion Capture system installed that can capture infrared marker balls in the theatre. Our main use for this system is to utilise "Rigid Body" *Trackers*. A tracker is a small card of 3 markers points that we can access the position and rotation of in the Data Arena theatre down to a few millimetres. We can support up to 8 trackers that can enable multi-user participation where everyone can have a control device for any purpose. The included `TrackerCursor` class will let you add an on-screen cursor to your project for multi-user interaction with scene objects. A "flip" gesture will let users pickup and drop objects as seen in our [Cozy Living Room](https://dataarena.net/projects/cozy-living-room) project. As with the SpaceMouse, you can make use of Tracker data for any purpose by adding a `DA_Tracker` cursor to your project.


## 👋 Our *Hello World* project
To see this plugin in action, download and run our [DA_HelloWorld](https://github.com/UTSDataArena/DA_HelloWorld) project in Unreal Engine (4.25). This simple project uses the `SpaceMouseCamera` actor to view and navigate the scene, and a `TrackerCursor` actor to pickup, move and drop dynamic objects in the level.

## ⚙️  Installation and usage
1. Download our plugin by either clicking *Code* → *Download ZIP* (above) or cloning this repository if you're familiar with Git.
2. Create a folder called *Plugins* in the base of your project folder and move the entire *DA_Assets* folder here.
> 👉 Github might label your downloaded folder *DA_Assets-master*. Rename it to *DA_Assets* if so.

3. Open your project and confirm the plugin is visible in the [Plugins UI](https://docs.unrealengine.com/4.26/en-US/ProductionPipelines/Plugins/).
4. To access the assets, open the Content Browser and scroll down to DA Assets in the left sidebar. If you can't find it, make sure *Show Plugin Content* is enabled in the *View Options* bottom right.

You're now ready to start experimenting with our assets. The above mentioned `SpaceMouseCamera` and `TrackerCursor` actors can be found in their respective folders. If you wish to utilise the data from our SpaceMouse or Tracker devices in your own way, you can add and reference the `DA_SpaceMouse` and `DA_Tracker` actors in your project from the *DeviceCommunication* folder.

## 💻 Development outside the Data Arena
This plugin is designed to help you utilise our input devices from outside the Data Arena. The `SpaceMouseCamera` and `TrackerCursor` classes have a ***Use VRPN Input*** checkbox accessible in the details panel. Keep this unchecked (off) if you're developing outside the Data Arena. This will tell Unreal Engine to fallback to keyboard input to simulate device input. When you're ready to bring your project to us, we'll enable this setting before packaging to use our real hardware devices in the DA.

> [VRPN](https://github.com/vrpn/vrpn/wiki) is an open-source, network-based interface we use to communicate to our input devices in the Data Arena.

## 🚀 Future development
As of July 2021 we currently support the 3DConnexion SpaceMouse and Optitrack Tracker input systems. Our future developments will include support for PlayStation and PSMove controllers that we already have in the DA, as well as including new actors based off existing integrations that we develop in other project use-cases. As our interfaces are based off VRPN, we can theoretically support any devices listed [here](https://github.com/vrpn/vrpn/wiki/Available-hardware-devices), so feel free to get in touch if you have any hardware you'd like to try in the Data Arena.

## ✉️  Get in touch
For more information take a look at the [UTS Data Arena](https://dataarena.net) website and [get it touch](https://dataarena.net/about#contact) with us about your first Data Arena project. We'd love to hear about what you've got planned with Unreal Engine and how we can help make it happen.
