Hello!
# This are the general instructions!

Wellcome! ;)

# Aera design instructions

## Project description

Aera imagines a fan as an extension of the person speaking. When the user
chooses to enable the microphone, the system listens for speech and looks for
language related to heat. More heat references request a faster breeze across
three speeds: low, medium, and high. When heat-related speech pauses, the fan
gradually slows to a stop. If the user remains quiet, the display offers a
short heat-themed poem. Speaking again returns the interaction to the voice
and fan response.

There is no distance, motion, or room-presence sensing in this design. The
microphone is enabled only through a deliberate user action. The intended
experience is conversational and poetic, not a temperature measurement or a
safety system.

## Current browser prototype

Open [`index.html`](./index.html) in a browser. It provides:

- An optional browser speech-recognition interaction, started by pressing
  **Start listening**.
- A phrase-entry field for testing without a microphone.
- A small, visible keyword list that approximates heat-related language.
  One match selects low, two or three select medium, and four or more select
  high. This is a demonstration rule, not contextual or semantic
  understanding.
- A simulated step-down after heat-related speech stops, followed by a poem
  after a quiet pause. The poem mood can be set to desert or intimate.

The browser prototype does not connect to a Raspberry Pi, read sensors, or
control a real fan. Browser speech-recognition availability and audio
processing depend on the browser and its provider; this project does not
include an API key or a speech-recognition service. A `network` recognition
error means the browser could not reach its speech service; check the internet
connection or try again later. Phrase entry remains available without speech
recognition.

## Future hardware considerations

A real fan implementation is not part of the browser demo. Before connecting
one, select a fan and a manufacturer-approved, motor-rated three-speed
controller explicitly compatible with that exact fan. Verify the controller's
documented, isolated low-voltage interface and have a qualified electrician
select, install, and check mains-side equipment.

The Raspberry Pi must never connect directly to mains power, fan motor
conductors, or speed-select wiring. A generic relay, dimmer, or hobby
MOSFET is not a substitute for a compatible motor-rated controller. Any
physical build needs independent, appropriate power isolation and must be
reviewed by qualified professionals; software and microphone behavior are not
safety controls.


