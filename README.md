# unreal_AnimatedTextPlugin

## Support

This plugin currently supports Animated Text Block, Rich Text and CommonUI Text.

![Supports](https://github.com/user-attachments/assets/25a80b35-d356-4bd3-960d-2d69bac37e03)


## Functionality

### AnimateText
Enter a string into the "AnimateText" event to animate it, constructing the word letter by letter.

![AnimateText](https://github.com/user-attachments/assets/aec95dfc-3aa7-484c-96b4-729492898146)


### ChangeSpeed
You can easily modify the speed at which the next character appears by adjusting the "DelayBetweenCharacters" value. Additionally, you can change the "SpeedChangePerLoop" value to speed up or slow down the text until it reaches the MinSpeed or MaxSpeed limits.

![ChangeSpeed](https://github.com/user-attachments/assets/eeb03495-d471-4229-b192-c078272e8391)


### DeleteLastCharacter
This event allows you to remove the last character. In the current version, you can also remove it by using the "-" character.

![DeleteLastChar](https://github.com/user-attachments/assets/cbe19243-7662-406b-8a10-470b5c01f4d8)

### ClearText

The Clear Text event clears the text box.


### EventCalled

To invoke an event, use the syntax "[EventName]." This will return the string, allowing you to utilize "Switch on String" to call whatever you need.

![CallEvents](https://github.com/user-attachments/assets/4627a487-22e6-4998-b4a0-7759335aad92)


### AnimationFinished

"AnimationFinished" is a dispatcher that is triggered when the animation stops. There are two possible outcomes: either the loop has completed, indicating that the "paused" condition is false, or the animation was paused using the "PauseText" event, which results in the "paused" condition being true.

![AnimFinish](https://github.com/user-attachments/assets/b6c6d413-e7c1-47f0-9140-e327b3c422d6)


### PauseText and ContinueText

The "PauseText" event pauses the spawning of characters and the loop, which can also be invoked using "|". To resume, use the "ContinueText" event. Note that "ContinueText" will only function if the animation was previously paused.

### ForLoopWithBreak_Delayed
The primary functionality is provided by the custom "ForLoopWithBreak_Delayed" macro, which enables users to create a for-each loop with a delay in between that can be skipped using a boolean value.

![ForEachLoop](https://github.com/user-attachments/assets/2ed8fb0e-bd31-4deb-b919-96f76892cbc8)

## Example

The plugin includes an example widget.

## Modify

To alter existing functionalities or create new ones, adjust the "Switch on String." This switch only checks the last character and can be easily modified.

![SoS](https://github.com/user-attachments/assets/fd8ae423-a2d6-4313-81c3-553ddab53b3c)


## Exposed Variables

All Animated Text Assets feature exposed speed settings, including "Delay Between Characters," "Speed Change per Loop," "Min Speed," and "Max Speed." Additionally, two sound effect settings are available: "Click SFX" (used when adding a character) and "Delete SFX" (used when deleting a character). The initial settings vary depending on the type of Animated Text you are using; for instance, the Animated Rich Text includes a TextStyleSet, which is a DataTable input.

![ExposedVar](https://github.com/user-attachments/assets/985b9e08-4b22-4e7c-8055-eab7affca87e)


## Limitations

#### Characters utilized in the "Switch on String" cannot be used as text characters.

#### Currently, only Rich Text supports multiple font sizes or text styles.
