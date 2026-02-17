Build a single page, client side only application using html5 + js that provides a facility for timing netball games.

The UI should look like as follows:

 - At the top, a bar containing the association logo (to be supplied) and the application title.

 - Then a bar containing a series of buttons:
   - Start
   - Stop
   - Siren
 On the far side of this bar there should be a button with a gear icon, which is used to open the configuration dialog.

 - Then a bar showing the status using a large font.

 - Then a table with the following columns:
   - Round #: Not editable, generated
   - Start Time: Editable - start time of this round
   - Qtr Duration - Editable - How long each quarter of the game is
   - Q1 Break - Editable - How long the break at the end of Q1 is
   - Q2 Break - Editable - How long the break at the end of Q2 is
   - Q3 Break - Editable - How long the break at the end of Q3 is
   - Inter Game Break - Editable - how long the break before the start of the next game is
   - Start Q1
   - End Q1
   - Start Q2
   - End Q2
   - Start Q3
   - End Q3
   - Start Q4
   - End Q5

 Each row should have a "Delete" button, and there should be an "Add" button to add more rows.

A summary of the functionality is as follows:

 - The following columns of the table are to be editable: Start Time, Qtr Duration, Q1 Break, Q2 Break, Q3 Break, Inter Game Break. The remaining columns are to be calculated from those values.

 When the user adds a row, all values are populated from defaults. The game start time is calculated from the end of the previous game.

 The user may edit rows in the table by double clicking the cell they want to edit, entering a new value, then pressing enter. Times are entered in the format hh:mm. Durations are entered in the form of mm:ss, or if just an integer is entered then it is interpreted as minutes.

 If a user edits the start time of a row, then all subsequent rows are recalculated accordingly.

 - While ever the page is running, it shall display the current time in the status bar.
 
 - When the "Start" button is clicked, the timing function is activated. The status bar shall display the amount of time to the next event as per the table - eg. "Round 1 Q1 starts 05:32". Any events in the table which are in the past are ignored.

 - 30 seconds before the beginning of a quarter, the app shall play the audio file "30sec_warning.mp3"

 - At the start of each quarter, the app shall play the audio file "qtr_start.mp3"

 - At the end of each quarter, the app shall play the audio file "qtr_end.mp3"

 - When the "Stop" button is pressed, current time continues to display, but the event processing above stops.

 - When the "Siren" button is pressed, it should prompt the user with "Are you sure you want to sound the siren?". If the user confirms, play the audio file "siren.mp3".
