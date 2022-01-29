# qb-sheriffjob
 Sheriff job for QBCore 
 <p>
 <b>
I edited policejob for sheriffs and i am planning to add more locales support.
</b>
</p>
<p>
Configured for GABZ paleto sheriff
</p>
<p>
Locales in progress:
SK
CZ
DE
</p>

# License

    QBCore Framework
    Copyright (C) 2021 Joshua Eger

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <https://www.gnu.org/licenses/>

## Dependencies
- [qb-core](https://github.com/qbcore-framework/qb-core) -To implement the job
- [qb-bossmenu](https://github.com/qbcore-framework/qb-bossmenu) - For the boss menu
- [qb-garages](https://github.com/qbcore-framework/qb-garages) - For the vehicle spawner
- [qb-clothing](https://github.com/qbcore-framework/qb-clothing) - For the locker room
- [qb-phone](https://github.com/qbcore-framework/qb-phone) - For the MEOS app and notifications etc.
- [qb-log](https://github.com/qbcore-framework/qb-logs) - For logging certain events
- [qb-menu](https://github.com/qbcore-framework/qb-menu) - For the vehicle menus
- [qb-input](https://github.com/qbcore-framework/qb-input) - For accessing evidence stashes



## Features
- Classical requirements like on duty/off duty, clothing, vehicle, stash etc.
- Citizen ID based armory (Whitelisted)
- Fingerprint test
- Evidence locker (stash)
- Whitelisted vehicles
- Speed radars across the map
- Stormram
- Impounding player vehicle (permanent / for an amount of money)
- Integrated jail system
- Bullet casings
- GSR
- Blood drop
- Evidence bag & Money bag
- Police radar
- Handcuff as an item (Can used via command too. Check Commands section.)
- Emergency services can see each other on map

### Commands
- /spikestrip - Places spike strip on ground.
- /pobject [pion/barier/schotten/tent/light/delete] - Places or deletes an object on/from ground.
- /cuff - Cuffs/Uncuffs nearby player
- /palert [text] - Sends an alert.
- /escort - Escorts nearby plyer.
- /callsign [text] - Sets the player a callsign on database.
- /clearcasings - Clears nearby bullet casings.
- /jail [id] [time] - Sends a player to the jail.
- /unjail [id] - Takes the player out of jail.
- /clearblood - Clears nearby blood drops.
- /seizecash - Seizes nearby player's cash. (Puts in money bag)
- /sc - Puts soft cuff on nearby player.
- /cam [cam] - Shows the selected security cam display.
- /flagplate [plate] [reason] - Flags the vehicle.
- /unflagplate [plate] - Removes the flag of a vehicle.
- /plateinfo [plate] - Displays if a vehicle is marked or not.
- /depot [price] - Depots nearby vehicle. Player can take it after paying the cost.
- /impound - Impounds nearby vehicle permanently.
- /paytow [id] - Makes payment to the tow driver.
- /paylawyer [id] - Makes payment to the lawyer.
- /radar - Toggles the police radar.
- /911 [message] - Sends a report to emergency services.
- /911r [id] - Used to respond the emergency alerts.
- /911a [message] - Sends an anonymous report to emergency services (gives no location).
- /anklet - Places anklet (tracking device) on nearby player.
- /removeanklet [citizenid] - Removes the anklet from player.
- /ebutton - Used to respond an emergency alert.
- /takedrivinglicense - Takes the driving license from nearby player.
- /takedna [id] - Takes a DNA sample from the player.

# qb-core/shared/jobs.lua 
```
['sheriff'] = {
		label = 'Sheriff',
		defaultDuty = true,
		offDutyPay = false,
		grades = {
            ['0'] = {
                name = 'Recruit',
                payment = 50
            },
			['1'] = {
                name = 'Deputy I',
                payment = 75
            },
            ['2'] = {
                name = 'Deputy II',
                payment = 75
            },
            ['3'] = {
                name = 'Deputy III',
                payment = 75
            },
            ['4'] = {
                name = 'Investigator',
                payment = 75
            },
			['5'] = {
                name = 'master investigator',
                payment = 100
            },
			['6'] = {
                name = 'Sergant',
                payment = 125
            },
			['7'] = {
                name = 'lieuitenant',
                payment = 150
            },
            ['8'] = {
                name = 'captain',
                payment = 150
            },
            ['9'] = {
                name = 'chief deputy',
                payment = 150
            },
            ['10'] = {
                name = 'assistant sheriff',
                payment = 150
            },
            ['11'] = {
                name = 'undersheriff',
				isboss = true,
                payment = 150
            },
            ['12'] = {
                name = 'Sheriff',
				isboss = true,
                payment = 150
            },
        },
	},
```
# qb-bossmenu/config.lua
```
    ['sheriff'] = vector3(-433.28, 6006.27, 37.0),
```