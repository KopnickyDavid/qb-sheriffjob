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