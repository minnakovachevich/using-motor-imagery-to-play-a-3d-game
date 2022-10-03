# using-motor-imagery-to-play-a-3d-game
<p align="justify">
Final project for my Brain-Computer Interface class. We were supposed to make a 3d game in Unity, and on our final exam we were to train the BCI using a volunteer's EEG signals so they could play the game using only their 'thoughts' and with no interference with the computer (e.g. using a keyboard). It was an honor and a privilege to work this semester with our more than amazing Professor, PhD Jelena Mladenovic. I have learnt so much and I can't wait to be in her other classes in future.  

The 3D game had to have a player whose motion was determined by using two commands, left-right, forward-backwards or up-down. We also had to implement obstacles on the plane, so the player would have a harder time deciding which direction to choose. Lastly, I added coins along the plane so that the player could collect them and increase his/her score based on the amount collected. At the end, the screen would show the player if the game was a win or a lose.

The game can be found in the **Releases** section, as the file was too big to be uploaded directly to the main branch.

In order to control the game using the EEG signals, we needed to add **LSL4Unity** to our game. Then we needed to test the motor imagery example using generic signals from openViBE (classified data from Generic Oscillator). This was done prior to our final exam, where we connected the game to real EEG data from volunteers.

In order to connect the game to real EEG data, and get feedback in the form of player's movement within the game, we had to go through two phases of data refinement: **calibration** and **testing** **phase**.

In the first phase we noted down the volunteer's EEG signals, and trained them. This is a crucial step, because the machine needs to be calibarated according to each individual person's EEG signals. Once we have finished training a student volunteer, we needed to train the spatial filter which allowed for feature extraction, based on which we trained the classifiers into two classes. In this phase, there is no feedback. 

In the next phase, the testing phase, we repeated the entire process, except at the end, the volunteer's EEG signals were assigned their corresponding class, which allowed for feedback. Since in the previous phase we trained the machine to ”recognize” which signal meant which class, in this phase the machine was assigning classes to signals based on parameters set in the previous phase.

At the end, the volunteer managed to play the game using motor imagery with no need to physically interfere with the game (e.g. using a keyboard).
</p>
