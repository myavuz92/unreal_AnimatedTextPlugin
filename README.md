# unreal_AnimatedTextPlugin

## Support

This plugin currently supports Animated Text Block, Rich Text and CommonUI Text.

![Supports](https://github.com/user-attachments/assets/25a80b35-d356-4bd3-960d-2d69bac37e03)


## Functionality

### AnimateText
Feed a string into the "AnimateText" Event to have it animated.

![AnimateText](https://github.com/user-attachments/assets/aec95dfc-3aa7-484c-96b4-729492898146)


### ChangeSpeed
You can simply change the speed of the creation of the next character by changing the "DelayBetweenCharacters" Value, or adjust the "SpeedChangePerLoop" Value to increase or decrease the speed of the text until hitting the MinSpeed or MaxSpeed.

![ChangeSpeed](https://github.com/user-attachments/assets/eeb03495-d471-4229-b192-c078272e8391)


### DeleteLastCharacter
With this Event you are able to remove the last character. In the current version you can also remove the last character with "-".

![DeleteLastChar](https://github.com/user-attachments/assets/cbe19243-7662-406b-8a10-470b5c01f4d8)

### ClearText

Clear Text is a Event which clears the Text box.


### EventCalled

To call an Event use this syntax "[EventName]". This will return the string and you are able to call whatever you want by using "Switch on String".

![CallEvents](https://github.com/user-attachments/assets/4627a487-22e6-4998-b4a0-7759335aad92)


### AnimationFinished

"AnimationFinished" is a Dispatacher that is being called when the animation stops. There are only two possible outcoes either the loop is finished that means the condition "paused" is false or it was paused with the "PauseText" Event which of course leadst to the condition "paused" being true.

![AnimFinish](https://github.com/user-attachments/assets/b6c6d413-e7c1-47f0-9140-e327b3c422d6)


### PauseText and ContinueText

The Event "PauseText" is pausing the spawning of the characters and the loop which is also callable by using "|". Use the "ContinueText" event to continue. "ContinueText" is only going to work if it has been pause before.

### ForLoopWithBreak_Delayed
The main functionalty comes from the custom "ForLoopWithBreak_Delayed" Macro, which gives the user the ability to create a for each loop with a delay in between that can be skipped with a boolean.

![ForEachLoop](https://github.com/user-attachments/assets/2ed8fb0e-bd31-4deb-b919-96f76892cbc8)

## Example

An example widget is included in the plugin.

## Modify

To modify existing functionalities or create new functionalities modify the "Switch on String". This Switch is only checking the last character and can easily be modified.

![SoS](https://github.com/user-attachments/assets/fd8ae423-a2d6-4313-81c3-553ddab53b3c)


## Exposed Variables

All of the Animated Text Assets have Speed Settings exposed which includes "Delay Between Characters", "Speed change per loop", "Min Speed" and "Max Speed".
I have also expsed two SFX settings exposed. These are "Click SFX" (which is being used when adding a character) and "Delete SFX" (which is being used when deleting a character).
The initial settings depends on which type of Animated Text you are using for example the Animated Rich Text has the TextStyleSet which is a Datatable input.

![ExposedVar](https://github.com/user-attachments/assets/985b9e08-4b22-4e7c-8055-eab7affca87e)


## Limitations

#### Characters which are being used in the "Switch on String" can not be used as Text Characters.

#### Currently only Rich Text is supporting multiple fontsizes or text styles. 
