# Moon Sweet Moon

A short Moon outpost game for kids aged 7 to 12, made for the 2026 NASA Space Apps Challenge (Junior Astronaut Mission Trainer).

**Play it:** https://erikazhouzx-hub.github.io/MoonSweetMoon/

You look after a small Moon outpost and its crew of three for three shifts. Each shift you read the Sun, share a few batteries between the air room, the farm, the storm shelter and the science lab, then watch what happens. No choice is free: power for the shelter is power the farm and the lab do not get.

Every day's mission is built from what the real Sun did yesterday, using NASA's solar flare records.

## Why a Moon outpost needs to watch the Sun

The outpost is on the Moon, and the Sun matters to it in two ways. Solar panels turn sunlight into the power the outpost runs on. The Sun also fires solar storms, and the Moon has no air to block them. So the Sun is both the outpost's power and its danger, and every mission starts by checking what the real Sun did.

## How to play

Open the link above, or open `index.html` in a browser. There is nothing to install and no account.

- **Daily mission:** one mission a day, built from yesterday's Sun (UTC), the same for everyone.
- **Practice:** play any saved past day. Practice does not change your outpost.
- **Try this Sun again:** after any mission, replay the same real day with a new plan. Replays are practice.

The game has a loading page, a home page, a how-to-play page, a My outpost page, a Fun facts page and an About the data page.

## What a child learns

| Idea | Where the game teaches it |
|---|---|
| Power is limited, so every choice costs something | One pile of batteries, four rooms, every shift |
| The Sun is both the outpost's power and its danger | Solar panels make the batteries, and solar flares bring the storms |
| Flares come in sizes, and a bigger one needs more protection | C, M and X storms need 1, 2 or 3 shelter batteries |
| A forecast is a best guess, not a promise | The storm chance is sometimes wrong, and Captain Rae says so |
| Food takes time, so you plan ahead | Lettuce needs 4 growth steps and wilts without power |
| Air comes first | Too little air power hurts the crew straight away |
| Some days cannot be won, and that is not your fault | "A day too strong for any crew" on the results screen |
| These are real things | Real flares, real Sun photos, and a NASA link on every fact and outpost part |

## A new puzzle every day

About 3 real days in 4 have no storm (22 of the last 30 days in the saved data), so a calm day needed something new to solve.

- **Captain's order of the day.** One extra goal, picked from the date, the same for everyone: Early harvest, Big experiment, Think of tomorrow, or Science day. Each one needs a different plan, and each comes with a one-line reason.
- **Fair orders.** The order never depends on the day's storms, so it gives nothing away. We checked every storm pattern and battery order in advance. If the Sun makes an order impossible, the game says so and it does not count against the player.
- **A Moon land to build on.** Finishing the order in a daily mission wins a building: a tall solar mast, a radiation sensor, a space garden, a radio dish, an ice drill, a Moon rover and a Sun telescope. On the home page the player picks the building and taps an empty spot on a picture of their Moon land to build it there, and can move it later. Tapping a building shows a real fact with a link to its NASA page.
- **Days in a row.** The home page counts how many days in a row the player has finished the daily mission.
- **Space pets.** A pet joins the Moon land after the first daily mission, then one more for every 3 days played in a row. The four pets are real species that NASA has studied in space, each with a real fact and a link to its NASA page:

| Pet | Real species | NASA source |
|---|---|---|
| Water bear | Tardigrade, flown to the space station in 2021 (Cell Science-04) | https://www.nasa.gov/humans-in-space/microscopic-superheroes-to-help-protect-astronaut-health-in-space/ |
| Bobtail squid | *Euprymna scolopes*, flown in 2021 (UMAMI) | https://science.nasa.gov/biological-physical/investigations/umami/ |
| Fruit fly | *Drosophila melanogaster* (Fruit Fly Lab) | https://www.nasa.gov/ames/space-biosciences/fruit-fly-lab/ |
| Space mouse | *Mus musculus* (rodent research on the space station) | https://science.nasa.gov/biological-physical/data/osdr/ |

NASA shares data from space biology studies like these in its Open Science Data Repository (OSDR). In the game the pets roam the Moon land in little air bubbles. That part is for fun: real animals have only flown inside spacecraft. The pets do not change how the game plays.

## Stars: scored on care, and fair on bad days

Stars are for looking after the crew.

| Reward | How to earn it |
|---|---|
| 1 star | Finish the mission |
| 2 stars | Only one astronaut is hurt at the end |
| 3 stars | Everyone is healthy at the end |
| Science star | 3 stars, plus 4 experiments |
| Upgrade card | Win the science star in a daily mission |

- **A blocked storm counts as experiments:** 1 for a small storm, 2 for medium, 3 for big. So protecting the crew also earns science. This is a game rule (see "What is simplified").
- **Upgrade cards** are single-use. The player chooses when to use one, on the battery screen, and it works for that mission only.

**Days when the Sun is too strong.** On some real days there is not enough power to block every storm and still keep the air and the farm going. Even a perfect plan would end with a hurt crew. The game works this out for each day by trying every way to share the batteries. On such a day it says so on the results screen, shows the best that any plan could be sure of, and scores the player against that best plan. The crew still gets hurt, but the player is not punished for something no one could avoid.

How we tested the scoring:

- Of the 50 saved days, 36 can always be finished with everyone healthy. 12 cannot, whatever the plan. 2 depend on the order the batteries arrive in.
- The game's "best plan" maths was checked against a separate checker written in Python: 300 cases (50 days, 6 battery orders each), all matched.
- **Estimate:** a simple scripted player who follows the forecast earns 3 stars on about 70% of days and the science star on about 47%. This is a simulation, not a test with real children, who would likely score lower.

## The forecast and the last-chance move

- **The forecast gives two things each shift:** the storm chance (low, medium or high) and the likely size if a storm comes (small, medium or big). When a storm is coming, the forecast says "high" 3 times in 4 and names the right size 3 times in 4. A size is always shown, so it never gives away whether a storm is coming. The forecast is a game rule, not NASA data.
- **Being ready is cheaper than reacting.** If the shelter is not ready when the Sun flashes, the player gets 10 seconds for a last-chance move. A rushed shelter needs 1 battery more than a ready one (a medium storm needs 2 if ready, 3 if rushed), and the batteries must all come from one room. If that room does not have enough, the storm still gets in.
- **Captain Rae is ground staff.** She works at Mission Control on Earth and sends the Sun report and the order of the day. A radio call to Earth and back takes more than 2 seconds, so in the last-chance move the crew decides alone.
- **The farm needs power every shift in a row.** The crew and Captain Rae remind the player while lettuce is growing.
- **Crew health has one clear scale.** ♥♥ fine, ♥♡ hurt (1 step down), ♡♡ sick (2 steps down). A good shift heals 1 step, so hurt needs 1 good shift and sick needs 2. Each crew member's cost follows the same scale: if Nova is hurt the lettuce needs 1 more growth step (sick: 2 more), if Kai is hurt the outpost gets 1 fewer battery (sick: 2 fewer), and if Juno is hurt or sick she can only heal herself, then heals everyone at once when she is fine.
- **Mission log.** The My outpost page is the history page: it lists every day played, with the stars, the crew's health and whether the order was done.
- **A promised harvest always happens.** The farm goes by Nova's health at the start of the shift, so "Harvest this shift" on the battery screen stays true even if a storm hurts her during that shift. Her injury slows the farm from the next shift.
- **The training mission teaches the last-chance move.** Captain Rae explains out loud that rushing batteries to the shelter costs 1 extra.

## Made for ages 7 to 12

- **Captain Rae**, at Mission Control on Earth, reads the Sun report aloud at the start of the mission, one sentence at a time. Each clue appears as she says it. On later shifts she only gives the storm chance and likely size.
- **The crew talk.** Nova, Kai and Juno step to the centre of the screen after each shift and say what happened and why, with moving mouths and their own voices.
- **Read it to me.** The How to play page can be read aloud.
- **Background music.** The game makes its own soft music with Web Audio, so there is no music file and no licence to check. It goes quieter while a character talks, and a Music button switches it off.
- **Fun facts while loading.** The loading screen shows a "Did you know?" fact and changes it every 9 seconds. Every fact a player has seen is kept on a Fun facts page, newest first, with a link to the NASA page it comes from.
- **A training mission for first-time players.** The first time someone presses Play, Captain Rae walks them through one guided shift: the room to use glows, and the game waits for each move. It uses a made-up storm, says so on screen, and can be skipped.
- **Voice speed, Back and Skip.** A Voice button makes the voices talk at 2x. It does not speed up the game. Skip moves on by one sentence and Back goes to the one before. The buttons disappear when the talking ends.
- **The captain says what you have.** She reads out your meals and experiments, and each number lights up on screen as she says it.
- **Every number is explained.** The battery screen shows where the batteries come from, for example "Solar panels 5, Shadow on the panels −1, = 4 batteries".
- Voices use the device's built-in speech, so there are no audio files and nothing is recorded. The voice sounds different on each device. The Sound button switches it off.

## NASA data used, and why

**1. Solar flares: NASA DONKI** (Space Weather Database Of Notifications, Knowledge, Information), run by the Community Coordinated Modeling Center (CCMC) at NASA Goddard. We use it because it tells us what the real Sun did on a given day, which is what a real crew would have to react to.

- Address used: `https://ccmc.gsfc.nasa.gov/DONKI-API/get/FLR?startDate=YYYY-MM-DD&endDate=YYYY-MM-DD`
- **Live:** when the game loads it asks that address for yesterday and the 5 days before. If NASA answers, the daily mission uses those live records. This works on the hosted site.
- **Saved copy:** 191 flare records from six date ranges in 2026 are saved inside `index.html` (copied on 14 Nov 2026). The game uses them for practice days, and for the daily mission if NASA cannot be reached. It says on the home page which one it is using.
- **Checked:** on 15 Nov 2026 we compared 87 saved records (1 to 5 Feb and 5 to 11 Nov 2026) with NASA's address. All 87 matched.
- From each record the game uses the peak time, the size class (C, M or X), the sunspot region number and the place on the Sun.

How the data drives the game:

| In the game | From the NASA record |
|---|---|
| Whether a storm hits a shift, and when | Flare peak time (each shift is 8 hours of that day, UTC) |
| How strong the storm is, and how many shelter batteries it needs | Flare class: C is small (1), M is medium (2), X is big (3) |
| The "this sunspot fired before" clue | Flares from the same sunspot region in the 5 days before |
| Where the sunspot sits on the Sun picture | The flare's recorded place on the Sun |
| Calm days | Dates in a fetched range with no flare record |
| Whether a day is "too strong for any crew" | Worked out from that day's real storms |

The results screen puts the two side by side: "What really happened on the Sun" (the real flares, with class and time) and "What your plan did".

**2. Sun photos: NASA Solar Dynamics Observatory (SDO)**, AIA 304 images, fetched for the mission date through the Helioviewer API (`https://api.helioviewer.org/v2/takeScreenshot/`). We use them so the player sees the real Sun of that day, not a drawing.

- Each shift shows the real Sun at that shift's time: 04:00, 12:00 or 20:00 UTC.
- The photo is taken in ultraviolet light, which eyes cannot see, so it is coloured red. Bright patches are the busy regions where flares happen.
- A ring marks the sunspot region named in the clue, placed from the position in the DONKI flare record.
- If the photo cannot load, the game shows a drawing instead.

**3. NASA pages behind the facts and rules**

| Used for | NASA page |
|---|---|
| Sunlight takes about 8 minutes to reach Earth | https://science.nasa.gov/earth/facts/ |
| About 1.3 million Earths fit inside the Sun | https://science.nasa.gov/sun/facts/ |
| Footprints last on the Moon (no wind or rain) | https://science.nasa.gov/solar-system/moon/10-cool-things-nasas-lunar-reconnaissance-orbiter-is-teaching-us-about-the-moon/ |
| Twelve people have walked on the Moon | https://science.nasa.gov/moon/moon-walkers/ |
| A radio signal takes a little over 1 second to reach the Moon | https://www.nasa.gov/wp-content/uploads/2011/08/583093main_earth_calling.pdf |
| Flare classes, and X is 10 times M | https://science.nasa.gov/sun/solar-storms-and-flares/ |
| Lettuce grown and eaten on the space station in 2015 | https://www.nasa.gov/image-article/space-farming-yields-crop-of-benefits-earth/ |
| SDO has watched the Sun since 2010 | https://sdo.gsfc.nasa.gov/mission/ |
| The Moon turns once in about 27 Earth days, and its air cannot be breathed | https://science.nasa.gov/moon/facts/ |
| Orion carries a radiation sensor that can warn the crew to take shelter | https://www.nasa.gov/missions/artemis/artemis-1/artemis-i-radiation-measurements-validate-orion-safety-for-astronauts/ |
| Near the Moon's south pole the Sun stays low and shadows are long | https://www.nasa.gov/reference/moonbase-environment/ |
| Solar panels up to 32 feet tall for the Moon's south pole | https://www.nasa.gov/technology/nasa-industry-to-mature-vertical-solar-array-technologies-for-lunar-surface/ |
| The space station garden is called Veggie | https://blogs.nasa.gov/kennedy/2015/08/11/veggie-success-benefits-journey-to-mars-and-eaters-on-earth/ |
| One lettuce crop on the space station grew for 33 days | https://images.nasa.gov/details/KSC-20150807-PH-NAS01_0008 |
| Frozen water in craters near the Moon's poles | https://spaceplace.nasa.gov/all-about-the-moon/en/ |
| Apollo astronauts drove a Lunar Roving Vehicle | https://science.nasa.gov/moon/exploration/ |
| SDO takes a picture of the Sun every 12 seconds | https://svs.gsfc.nasa.gov/gallery/sdo/ |

## Daily totals (no personal data)

When a player finishes the daily mission, the game sends three things to a small Supabase table: the mission date, the stars earned, and whether the whole crew stayed healthy. It sends no name, no account and nothing about the player.

The game can add a result and read the day's totals ("12 crews have finished today's mission"), but it cannot read single results. The Supabase key in `index.html` is a publishable key, which is made to be visible in a web page. Practice missions send nothing.

## What is simplified

- In the game every flare brings a storm to the outpost. In real life only some flares send harmful particles toward the Moon.
- A flare's light arrives in about 8 minutes and the particles come later. The game squeezes that wait into a few seconds.
- The storm chance and likely size are a game forecast, not data. The extra battery for a rushed shelter is a game rule too.
- "A blocked storm counts as experiments" is a game rule. The real part is that spacecraft carry radiation sensors, and one on Orion can warn the crew to take shelter.
- The battery rule (5 a shift, 1 fewer in shadow, 1 more in bright sun) is a game rule. The real part is that near the Moon's south pole the Sun stays low and long shadows can get in the way of solar power.
- The last-chance move says Earth is too far to ask in time. The real part is the radio delay of a little over 1 second each way. The game does not model the delay beyond that line.
- The ring that marks a sunspot on the photo is placed from the flare record, or estimated from the Sun's rotation on a day the spot did not fire. It is approximate.
- Batteries, meals, experiments, crew health and upgrade cards are game rules made to teach the trade-off. They are small whole numbers a child can count: 3 crew eat 1 meal each per shift, the outpost starts with 6 meals, a lettuce harvest makes 3 meals (one shift of food, so a mission needs exactly one harvest), and 1 lab battery runs 1 experiment. They are not NASA figures.

## Still to do

- Test with real children aged 7 to 12.
- Listen to the voices and the music on a few devices.
- Use a NASA health dataset (OSDR) for the crew health rules, which are game rules today.
