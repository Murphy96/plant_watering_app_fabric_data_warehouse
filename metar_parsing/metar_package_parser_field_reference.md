##### **METAR PARSER FIELD REFERENCE FOR METAR PACKAGE** 





**CORE OBSERVATION FIELDS**

&#x09;						    

&#x09;		 

|ATTRIBUTE|TYPE|MEANING|ACCESS VALUE|
|-|-|-|-|
|obs.code|str|Original raw METAR|obs.code|
|obs.type|str|METAR/SPECI|obs.type|
|obs.correction|str / None|Correction indicator|obs.correction|
|obs.mod|str|AUTO/COR/etc.|obs.mod|
|obs.station\_id|str|ICAO station|obs.station\_id|
|obs.time|datetime|Observation timestamp|obs.time|
|obs.cycle|int|Hourly observation cycle|obs.cycle|





**WIND** 



|ATTRIBUTE		|OBJECT|MEANING|ACCESS VALUE|
|-|-|-|-|
|obs.wind\_dir|direction (returns degrees by default)|Mean wind direction|obs.wind\_dir.value(), obs.wind\_dir.compass()|
|obs.wind\_speed|speed|Mean wind speed|obs.wind\_speed.value()|
|obs.wind\_gust|speed|Gust speed|obs.wind\_gust.value()|
|obs.wind\_dir\_to|direction (returns degrees by default)|End of variable direction range|obs.wind\_dir\_to.value()|



**VISIBILITY** 



|ATTRIBUTE|OBJECT|MEANING|ACCESS VALUE|
|-|-|-|-|
|obs.vis|distance|Prevailing visibility|obs.vis.value()|
|obs.vis\_dir|direction (returns degrees by default)|Direction associated with visibility|obs.vis\_dir.value(), obs.vis\_dir.compass()|
|obs.max\_vis|distance|Maximum visibility|max\_vis.value()|
|obs.max\_vis\_dir|direction (returns degrees by default)|Direction of maximum visibility|max\_vis\_dir.value(), max\_vis\_dir.compass()|





**TEMPERATURE**



|ATTRIBUTE|OBJECT|MEANING|ACCESS VALUE|
|-|-|-|-|
|obs.temp|Temperature (returns Celsius by default)|Recorded Temperature|obs.temp.value(), obs.temp.value("C"), obs.temp.value("F"), obs.temp.value("K")|
|obs.dewpt|Temperature (returns Celsius by default)|Recorded Dewpoint |obs.dewpt.value(), obs.dewpt.value("C"), obs.dewpt.value("F"), obs.dewpt.value("K")|



**PRESSURE**



|ATTRIBUTE|OBJECT|MEANING|ACCESS VALUE|
|-|-|-|-|
|obs.press|Pressure|Recorded Barometric Pressure |obs.press.value(), units supported: HPA, MB, IN|
|obs.press\_sea\_level|Pressure|Pressure at Sea Level (standard barometric pressure)|obs.press\_sea\_level.value("HPA")|



**WEATHER**



|ATTRIBUTE|TYPE|MEANING|ACCESS VALUE|
|-|-|-|-|
|obs.weather|<br />Tuple: (<br />    intensity,<br />    description,<br />    precipitation,<br />    obscuration,<br />    other<br />)<br />|Current Weather Conditions |Intensity Code Meaning <br />-       Light<br />none    Moderate<br />+       Heavy<br /><br />Proximity Code Meaning<br />none    On station<br />VC      In vicinity (5-10 miles)<br />DSNT    > 10 miles<br /><br />Description <br />BC      Patches<br />BL      Blowing<br />DR      Low drifting<br />FZ      Freezing <br />MI      Shallow<br />PR      Partial <br />SH      Shower(s)<br />TS      Thunderstorm<br /><br />Precipitation Code Meaning<br />DZ	Drizzle<br />RA	Rain<br />SN	Snow<br />SG	Snow grains<br />IC	Ice crystals<br />PL	Ice pellets<br />GR	Hail<br />GS	Small hail / snow pellets<br />UP	Unknown precipitation<br /><br />Obscuration <br />BR      Mist<br />DU      Widespread dust<br />FG      Fog<br />FU      Smoke<br />HZ      Haze<br />PY      Spray <br />SA      Sand<br />VA      Volcanic ash <br /><br />Other <br />DS      Dust storm <br />FC      Funnel cloud(s)<br />PO      Well developed dust/sand whirls<br />SQ      Squalls<br />SS      Sandstorm |
|obs.recent|<br /><br /><br /><br /><br /><br />Tuple: (<br />    intensity,<br />    description,<br />    precipitation,<br />    obscuration,<br />    other<br />)<br /><br />|Recent Weather Conditions (stored separately from Current weather)|Intensity Code Meaning<br />-       Light<br />none    Moderate<br />+       Heavy<br /><br />Proximity Code Meaning<br />none    On station<br />VC      In vicinity (5-10 miles)<br />DSNT    > 10 miles<br /><br />Description<br />BC      Patches<br />BL      Blowing<br />DR      Low drifting<br />FZ      Freezing<br />MI      Shallow<br />PR      Partial<br />SH      Shower(s)<br />TS      Thunderstorm<br /><br />Precipitation Code Meaning<br />DZ	Drizzle<br />RA	Rain<br />SN	Snow<br />SG	Snow grains<br />IC	Ice crystals<br />PL	Ice pellets<br />GR	Hail<br />GS	Small hail / snow pellets<br />UP	Unknown precipitation<br /><br />Obscuration<br />BR      Mist<br />DU      Widespread dust<br />FG      Fog<br />FU      Smoke<br />HZ      Haze<br />PY      Spray<br />SA      Sand<br />VA      Volcanic ash<br /><br />Other<br />DS      Dust storm<br />FC      Funnel cloud(s)<br />PO      Well developed dust/sand whirls<br />SQ      Squalls<br />SS      Sandstorm|











