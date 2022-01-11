Pawns And Controllers
=====================

Links
^^^^^

*   `Setting Up Character Movement <https://docs.unrealengine.com/en-US/InteractiveExperiences/HowTo/CharacterMovement/index.html>`_
*   `Posessing Pawns <https://docs.unrealengine.com/en-US/InteractiveExperiences/HowTo/PossessPawns/index.html>`_
*   `Input <https://docs.unrealengine.com/en-US/InteractiveExperiences/Input/index.html>`_
*   `Get / Set Control Rotation <https://www.youtube.com/watch?v=vszgkMwahDA>`_
*   `Static Camera: When you want your pawn to look out of a specific camera <https://docs.unrealengine.com/en-US/InteractiveExperiences/UsingCameras/Blueprints/index.html>`_


Default Camera
^^^^^^^^^^^^^^

Looking at a default player controller you will see the viewport contains a camera. When a Player Controller
posesses a pawn, if no camera on that pawn exists the player controller uses the location / rotation of the pawn
as the default camera location / rotation. In the case of a Character Pawn the camera location is determined by
the pawn location and the ``Base Eye Height`` Settings under the Camera settings in the Character details panel.

Rotating Your Character
^^^^^^^^^^^^^^^^^^^^^^^

In UE4 tutorials, it is common to see that within the Character Pawn, the XAxis input of the mouse is connected to the
``Add Controller Yaw Input`` Function and the YAxis input to the ``Add Controller Pitch Input``. When using these
functions the user will find that they can now rotate the player along the yaw direction (Scanning horizontally) and
the pitch direction (up and down). However if they take a look at the pawn itself they will find that the pawn only
rotates along the Yaw and not the Pitch. This is because by default the pawn has ``Use Controller Rotation Yaw``
set to true and the other rotations are set to False.