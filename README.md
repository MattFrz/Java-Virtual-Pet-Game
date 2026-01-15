Note: javadocs are under the directory called "docs". Compiled class files are under "out".

Welcome to EvoPets! This is our (Group 72's) project, which is a GUI game where you can take care of a pet and watch it grow and evolve as you manage all the pet's stats, like happiness, health, energy, and fullness.

This game is built using JavaFX, therefore JavaFX is neccessary to run the game. Here are the comprehensive steps to building, compiling, and running EvoPets on your Windows computer.

1. Install Java JDK (obviously). The game will obviously not work if Java is not installed.
2. Install JavaFX SDK from this website: https://gluonhq.com/products/javafx/. IMPORTANT: the version of JavaFX you install MUST be equal to or less than the version of Java JDK. If it's not, JavaFX may not run properly. For example, if your Java version is 17, you shouldn't download JavaFX v24. When downloading, choose the SDK version (not the jmods version).
3. Extract the downloaded files somewhere on your computer. Make sure you know the path to the JavaFX library. For example, if your javaFX folder is in Program Files under This PC (C:), then your file path is "C:/Program Files/javafx-sdk-24/lib" (assuming version 24 of JavaFX). Don't forget the lib part of the file path.
4. Navigate to the folder where the game is stored in Windows command prompt (using the cd command).
5. Compile the program with a prompt line like this: 

javac --module-path "(PATH TO JAVAFX LIBRARY)" --add-modules javafx.controls,javafx.fxml src/*.java 

Make sure you replace the path with the actual path where you stored the javaFX files (from step 3). Note: if you are in the src folder, then replace the last part with *.java. I'm sure you know the basics of Windows Command Prompt.

6. Run the file by typing something like this:

java --module-path "(PATH TO JAVAFX LIBRARY)" --add-modules javafx.controls,javafx.fxml -cp . Main

Again, replace the path with your actual path to JavaFX library. The main class is called Main. 


The password for parental controls is "CS2212". The C and S are uppercase. The parental controls will not load if you don't type the correct password.

This game has an evolution system, which is our main "additional feature" as per the functional requirements. You gain score when your stats are increased, with the exception of forced sleeping (energy reaching 0). When your score reaches 500 and 1000, you will evolve to level 2 and 3 respectively. When you evolve, the pet will grow to a teen and then an adult, completing your evolution journey!

To use food items, you have to buy them from the kitchen AND use them from the inventory. If you don't use them from the inventory, then your fullness stat won't increase.

When you exit the game, a file will be created in your working directory (the one where Main.class is found) called "TimeInformation.ser". This file contains information for parental controls, including total playtime, average playtime, time controls (for limiting playtime), and more. This is the file subsequent launches will use to restore time information. If you want to reset this information, delete this .ser file.

When you save a game, a file called <PetName>.ser will be created in the working directory. This file contains information for the save file. The program will load the first three of these files in the load game screen. If you want to delete a save file, delete one of these .ser files.

Have fun with EvoPets!

Group 72

