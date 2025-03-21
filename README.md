# retro-link_unity-vr

## Creating a VR project from start
- Followed steps from [Unity's tutorial](https://learn.unity.com/tutorial/create-a-vr-starter-project-from-scratch?uv=2022.3#)

## VR Project Setup
- Below is from Unity's [1.1 - VR Project Setup](https://learn.unity.com/tutorial/vr-project-setup#)

### Build and run on device
If you are using a Quest, follow this step to build the app onto your device. Otherwise, skip this step.  

Since the Quest is a standalone device (meaning it does not need to be connected to a computer), you can build an app and test it directly on the device, disconnected from your computer.  

If you are on a Mac and cannot test your app through the Windows Quest software as in the previous step, this will be the primary way for you to test your app on your headset.  

In order to build your app to the Quest headset, you will need to configure plug-ins for the Android build target.  

1. Install the OpenXR for Android builds:
	- From the top menu, select **Edit > Project Settings**, then select the XR Plug-in Management panel from the sidebar.
	- From the XR Plug-in Management settings, select the **Android** tab, then select **OpenXR** from the list of available Plug-in Providers to install that plug-in. **Note**: You will only have an Android tab if you installed the Android export module.
	- If you don’t see an option for **OpenXR** in the Android tab, first go back to the Desktop tab and select OpenXR there, then return to the Android tab.
2. Resolve warnings by setting up an interaction profile.
	- Click on the new warning or error icon that appears to open the **OpenXR Project Validation** window,
	- If there is an option to **Fix All**, select that to address some of the warnings. 
	- A warning will likely still remain telling you that you need to add an **interaction profile**. Select the **Edit** button to open the OpenXR settings panel.
	- In the **OpenXR** settings, in the **Android** tab, select the **+** button to add the appropriate profile for your device.
	- For models of the Quest, select the **Oculus Touch Controller Profile**, then enable the **Meta Quest Support** feature groups.
	- If any additional errors or warnings appear, click on the error or warning icons to resolve them.
3. Prepare your scene for building: 
	- Make sure the XR Device Simulator in your scene is disabled. If it is enabled, your head tracking will not work.
	- From the top menu, click **File > Build Settings**.
	- Click **Add Open Scenes** to add your scene.
4.  Switch to the Android build platform: 
	- In the **Platform section**, select **Android**.
	- Click **Switch Platform**, and wait for your project to switch to the Android platform.
	- **Note**: Android will only show up as a possible build target if you successfully installed the Android Export Module during installation of the Unity Editor.
5.  Select your device as the build target:
	- Make sure your VR device is turned on and plugged in.
	- Next to the **Run Device** drop-down, click **Refresh**, then select your VR device.  Your device may show up as a device ID or as a device name. 
	- **Note**: If your device does not show up in the list, try putting on the device. It may prompt you to **Allow USB debugging**. If it is still not showing up in the list, try restarting your device, making sure it’s in Developer Mode, or restarting Unity.
6.  Build and run your project on your device:
	- Click **Build and Run**. 
	- When prompted to choose a location, create a new “Builds” folder, then **Save** your project.
	- **Note**: When you build your app for the first time, it may take several minutes to compile. 