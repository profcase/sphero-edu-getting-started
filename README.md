# Sphero Edu - Getting Started

## Links

- [View on GitHub Pages](https://profcase.github.io/sphero-edu-getting-started/)
- [Code Repository](https://github.com/profcase/sphero-edu-getting-started)

## Sphero Edu App

Write programs with blocks or JavaScript.

- [Sphero Edu Website](https://edu.sphero.com/)
- [Sphero Edu Mobile App](https://edu.sphero.com/d)

## Sphero Play App

Control robot with facial expressions & more.

- [Sphero Play Android App](https://play.google.com/store/apps/details?id=com.sphero.spheromini&hl=en_US)
- [Sphero Play iOS App](https://itunes.apple.com/us/app/sphero-play/id1280682522?mt=8)

## Important

- Each Sphero Mini takes ~60 minutes for a full charge.
- Each charge will last ~20-60 minutes.
- The robot charges with USB. You will need your laptop or a brick (not provided).
- You will need a cell phone, with the Sphero Edu App, logged in as an Educator.
- At least 2 robots per instructor are recommended.

## Troubleshooting

If you get a "Session expired" error on login, clear your cache and try again:

- From a Home screen, tap the Arrow icon to display all apps.
- Navigate: Settings &gt; Apps & notifications &gt; App info.
- Tap the Sphero Edu app. Tap Storage. Tap Clear cache.

OR un-install the app from the webstore and re-install it.

## Unboxing Sphero Mini

1. Take off outer plastic bag and discard.
2. Take off outer plastic ring and discard.
3. Take off tape on opposite sides and discard.
4. Take plastic box off paper box.
5. Open paper box.
6. Remove inner white divider and legal guide; discard.
7. Remove and discard tie from USB cord.
8. Keep bag of bowling pins in paper box.
9. Pinch plastic base to remove clear plastic cover.
10. Pry robot off sticky dot base (keep sticky dot on base).
11. Remove clear plastic from around robot; discard plastic.

## Charging Sphero Mini

1. Press gently on centerline of robot, extract robot core.
2. Insert mini USB end into robot core.
3. Insert standard USB end into laptop (or outlet brick, not provided).
4. Lights will come on when charging.
5. Allow about 60 minutes to fully charge.

## After charging

1. Disconnect USB charging cord.
2. Put robot core back into shell and push 2 shell halves together.

## Set Up (First Time)

1. Ensure robot is charged and outer cover is on.
2. Ensure Bluetooth is enabled on phone.
3. Ensure Location is enabled on phone.
4. Open Sphero Edu app.
5. Register your account.
6. Log in to the app.
7. Follow Let's get started for an overview.
8. Create a first program, use default name.
9. Click "start" and allow it to access your location.
10. Select Robot Type "Sphero Mini".
11. Tap nearby robot to connect. Allow Firmware to update.

## Using Sphero

1. Ensure robot is charged and outer cover is on.
2. Ensure Bluetooth and Location is enabled on phone.
3. Log in to Sphero Edu app.
4. To change color or aim the robot: Lower Icon Bar / Last Icon, Far Right
5. To run programs: Lower Icon Bar / Second Icon ("Programs")

## Creating Programs

1. Login to the app.
2. Click Programs / + Create.

Note: If you create a program with blocks, it will show you the JavaScript. If you create in JavaScript, it does not automatically generate a block view. 

## Animal Toss

In the [Animal Toss](https://edu.sphero.com/remixes/370784) game, a group of students toss a Sphero and guess a random animal based on sound. Guessing wrong means you have to act out the animal. The [program](https://edu.sphero.com/remixes/370784) reads accelerometer data, and if the robot feels > 3G, it will play a random animal sound on the instructors mobile app. Animals include: Alligator, Bear, Bird , Cat, Chicken, Cow, Dog, Dolphin, Donkey, Duck, Elephant, Frog, Horse, Horse Gallop, Lion, Monkey, Pig, Rooster, Sea Lion, Sheep, Tiger, Whale.

![Animal Toss Program](https://github.com/profcase/sphero-edu-getting-started/raw/master/AnimalToss.PNG "Animal Toss Program")

## Hello Bearcat!

```JavaScript
async function startProgram() {
  await speak("Hello Bearcat", true);
  setMainLed({ r: 0, g: 103, b: 71 });
  setSpeed(60);
  await delay(2);
  setSpeed(0);
}
```

## Bearcat Square

```JavaScript
async function startProgram() {
  setMainLed({ r: 0, g: 103, b: 71 });
  await speak("Hello Bearcat - I can make a square", true);
  await delay(1);
  for (var _i1 = 0; _i1 < 4; _i1++) {
    setMainLed(getRandomColor());
    await Sound.Game.Coin.play(true);
    await roll((getHeading() + 90), 60, 1);
    await delay(1);
  }
}
```

## Sphero Mini x 30

![Sphero Mini x 30](https://github.com/profcase/sphero-edu-getting-started/raw/master/SpheroEdu30.PNG "Sphero Mini x 30")

## Acknowledgements

Many thanks for the generous support from Northwest Missouri State University.

## Copyright

© 2018 Denise Case, Northwest Missouri State University
