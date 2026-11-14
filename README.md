# Moon Sweet Moon

A short Moon outpost game for kids aged 7 to 12, made for the 2026 NASA Space Apps Challenge (Junior Astronaut Mission Trainer).

You look after a small Moon base and its crew of three for three shifts. Each shift you read the Sun, share a few batteries between the air room, the farm, the storm shelter and the science lab, then watch what happens. No choice is free: power for the shelter is power the farm and the lab do not get.

## How to play

Open `index.html` in a browser. There is nothing to install and no account.

- **Daily mission:** one mission a day, built from yesterday's Sun (UTC), the same for everyone. Winning lets you pick one upgrade for your base.
- **Practice:** play any saved past day. Practice does not change your base.

The game has a loading page, a home page, a how-to-play page, a My base page and an About the data page.

## NASA data used

**Solar flares: NASA DONKI** (Space Weather Database Of Notifications, Knowledge, Information), run by the Community Coordinated Modeling Center (CCMC) at NASA Goddard.

- Address used: `https://ccmc.gsfc.nasa.gov/DONKI-API/get/FLR?startDate=YYYY-MM-DD&endDate=YYYY-MM-DD`
- 191 flare records from six date ranges in 2026 are saved inside `index.html` (copied on 14 Nov 2026).
- When the game loads it also asks that address for yesterday and the 5 days before. If NASA answers, the daily mission uses those live records. If not, it uses the saved copy and says so on the home page. **The live request has not been tested from a hosted site yet.**
- From each record the game uses the peak time, the size class (C, M or X), the sunspot region number and the place on the Sun.

How the data drives the game:

| In the game | From the NASA record |
|---|---|
| Whether a storm hits a shift, and when | Flare peak time (each shift is 8 hours of that day, UTC) |
| How strong the storm is | Flare class: C is small, M is medium, X is big |
| The "this sunspot fired before" clue | Flares from the same sunspot region in the 5 days before |
| Where the sunspot sits on the Sun picture | The flare's recorded place on the Sun |
| Calm days | Dates in a fetched range with no flare record |

## What is simplified

- In the game every flare brings a storm to the base. In real life only some flares send harmful particles toward the Moon.
- A flare's light arrives in about 8 minutes and the particles come later. The game squeezes that wait into a few seconds.
- The storm chance meter is a game forecast, not data.
- The Sun picture is a drawing. On a day a sunspot did not fire, its place is estimated from the Sun's rotation.
- Batteries, food, science points, crew rules and upgrades are game rules made to teach the trade-off.
- The crew's facts are sample lines that still need checking against NASA sources.

## Still to do

- Spot-check the saved flare records against the NASA address above.
- Test the live NASA request once the game is hosted.
- Show a real photo of the Sun for the mission date.
- Check every crew fact against a NASA source and link it.
