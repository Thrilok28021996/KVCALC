Packaging Your App for Android

Now that you’ve finished the code for your application, you can share it with others. One great way to do that is to turn your code into an application that can run on your Android phone. To accomplish this, first you’ll need to install a package called buildozer with pip:

$ pip install buildozer

Then, create a new folder and navigate to it in your terminal. Once you’re there, you’ll need to run the following command:

$ buildozer init

This will create a buildozer.spec file that you’ll use to configure your build. For this example, you can edit the first few lines of the spec file as follows:

[app]

# (str) Title of your application
title = KvCalc

# (str) Package name
package.name = kvcalc

# (str) Package domain (needed for android/ios packaging)
package.domain = org.kvcalc

Feel free to browse the rest of the file to see what else you can change.

At this point, you’re almost ready to build your application, but first, you’ll want to install the dependencies for buildozer. Once those are installed, copy your calculator application into your new folder and rename it to main.py. This is required by buildozer. If you don’t have the file named correctly, then the build will fail.

Now you can run the following command:

$ buildozer -v android debug

The build step takes a long time! On my machine, it took 15 to 20 minutes. Depending on your hardware, it may take even longer, so feel free to grab a cup of coffee or go for a run while you wait. Buildozer will download whatever Android SDK pieces it needs during the build process. If everything goes according to plan, then you’ll have a file named something like kvcalc-0.1-debug.apk in your bin folder.

The next step is to connect your Android phone to your computer and copy the apk file to it. Then you can open the file browser on your phone and click on the apk file. Android should ask you if you’d like to install the application. You may see a warning since the app was downloaded from outside Google Play, but you should still be able to install it.

