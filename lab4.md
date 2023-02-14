# Lab report 3
## Grep command options

> [Source for all options:](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

What grep command should look like: `grep [options] pattern [files]`

Possible oprtions: 

> Pro tip: *use -r option with other oprtions to iterate through all files in a directory recursively*

### **-c**

what is it doing: returns a count of the lines that match a given pattern

why is it useful: if we need to know how many times a given pattern occurs in the file
- example 1:
```
grep -c 'Israel' ./written_2/travel_guides/berlitz1/HistoryJerusalem.txt
11
```
- example 2:
```
grep -c 'Israel' ./written_2/travel_guides/berlitz1/HistoryJapan.txt
0
```
### **-l**

what is it doing: returns list of a filenames that match a given pattern

why is it useful: if we need to know just the filenames where the pattern occurs, or count the files later
- example 1:
```
grep -lr 'frog' ./written_2/
./written_2/non-fiction/OUP/Berk/CH4.txt
./written_2/non-fiction/OUP/Kauffman/ch1.txt
./written_2/non-fiction/OUP/Kauffman/ch8.txt
./written_2/travel_guides/berlitz1/IntroJamaica.txt
./written_2/travel_guides/berlitz1/WhatToJamaica.txt
./written_2/travel_guides/berlitz1/WhereToEgypt.txt
./written_2/travel_guides/berlitz1/WhereToIstanbul.txt
./written_2/travel_guides/berlitz1/WhereToMalaysia.txt
./written_2/travel_guides/berlitz2/Bahamas-History.txt
./written_2/travel_guides/berlitz2/Bermuda-WhereToGo.txt
./written_2/travel_guides/berlitz2/Boston-WhereToGo.txt
./written_2/travel_guides/berlitz2/CstaBlanca-WhereToGo.txt
./written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt
```
- example 2:
```
grep -lr 'fox' ./written_2/
./written_2/non-fiction/OUP/Kauffman/ch9.txt
./written_2/travel_guides/berlitz1/WhereToEgypt.txt
./written_2/travel_guides/berlitz1/WhereToFrance.txt
./written_2/travel_guides/berlitz1/WhereToIsrael.txt
./written_2/travel_guides/berlitz1/WhereToJapan.txt
./written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt
./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
```
### **-h**

what is it doing: returns the matched lines without the filenames

why is it useful: if we need to know the content of lines with the pattern
- example 1:
```
grep -hr 'sushi' ./written_2/
        you or turn it into sushi or sashimi (depending on your degree of faith
        Matsushima is considered one of the country’s three Great
        three of this or eight of that. ) Although you can reach Matsushima in
        Shiogama and take the one-hour boat cruise across Matsushima Bay.
        In the town of Matsushima, visit the pretty Kanrantei
Just north of the Pueblo are the crowded streets and Oriental architecture of L.A.’s Chinatown, while to the south is Little Tokyo,
the cultural center of the Japanese community. The Japanese Village Plaza is a popular shopping spot, with twisting paths lined with
bonsai trees, rock gardens, and sushi bars. Nearby is a monument to the space shuttle Challenger,
including a statue of the Japanese-American astronaut Ellison Onizuka, one of the seven who died in the 1986 disaster.
```
- example 2:
```
grep -hr 'pizza' ./written_2/
         — good pizzas, interesting pasta dishes. Eat out on the tree-shaded
        including pizzas, any time of day. Major credit cards.
        Menorcan, and Spanish cuisine rather than pizza and French fries.
        Bistro for pizza and pasta in Castle Market, Fitzer’s cafés, and the
        Turkish-style pizza parlour, dishing up tasty pide (unleavened bread)
        to spend hours in the restaurants. Naples is where pizza began (the
Across the plaza from Fanueil Hall the three Quincy market buildings fill with crowds of locals and visitors, who come to feast on chowder,
seafood, deli sandwiches, pizza, and an array of ethnic cuisines. They also come to shop at the stalls, the flower market, and the stores,
to watch the street entertainers and to sample the nightlife. One restaurant in particular draws folks — Durgin Park, which offers Yankee cuisine,
communal dining, and tough no-nonsense waitresses. When they were built in 1826, these buildings stood on the waterfront.
Older Bostonians can still recall the stench of rancid meat emanating from them on a hot summer’s day and the gradual decay of the area before
they were restored in the late 1970s.
While in the Marais, take a wander around the old Jewish quarter (or shtetl, as Parisian Jews call it), especially if you are looking for
somewhere unusual to eat. Jews have lived around the rue des Rosiers for centuries, and the rue Ferdinand Duval was known until 1900 as the rue des Juifs.
The other main street, rue des Ecouffes (medieval slang for moneylenders), completes the lively shopping area, with delicatessens,
kosher butchers, and even kosher pizza shops. More recent arrivals from the Jewish communities of North Africa have largely replaced
the Ashkenazim of Eastern Europe, who themselves took the place of the Sephardim who first settled in Paris from Spain in the 13th century.
```
### **-n** 

what is it doing: returns the matched lines and their line numbers

why is it useful: if we need to know what lines *exactly* contain the pattern
- example 1:
```
grep -n 'Israel' ./written_2/travel_guides/berlitz1/HistoryJerusalem.txt
32:        allotted to any of the twelve rival tribes of Israel, David made it the
60:        his death the empire collapsed, and the Israelite kingdom was divided
61:        into two separate, impoverished, often warring nations: Israel, with
68:        Israel and moved southward to besiege Jerusalem. Thanks to King
76:        Israelites were permitted to return to Jerusalem in 539 b.c. The city
229:        Modern Israel
230:        The State of Israel was declared during this difficult
234:        Israeli forces secured a land corridor connecting the city to the
238:        Jerusalem was to be under Israeli control, and East Jerusalem
243:        barbed wire, no Israeli or Jewish pilgrims were allowed to visit the
248:        days the city was completely in Israeli hands, and in two weeks it was
```
- example 2:
```
grep -n 'Osaka' ./written_2/travel_guides/berlitz1/HistoryJapan.txt
100:        (present-day Osaka) and then a little to the east, at Nara, in 710.
277:        Osaka was the biggest Japan had ever seen, requiring a work force of
331:        million in the 18th century), Osaka (400,000), and Nagoya and Kanazawa
344:        bunraku) at Osaka, which was Japan’s cultural capital at a time when
```
