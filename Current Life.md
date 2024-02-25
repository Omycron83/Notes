# To-Do
1. Lin. Algebra & Analysis Nachholen
2. KI-Paper: Rechnungen beenden
3. BLL & Abitur
4. Go to the gym 3x, Boxing 1-2x a week
5. Talk to people as often as possible, Increase Drip
6. Still get great marks -> Vorarbeiten (+ MA), viel Engagement in Projekten, Viel für Klausuren lernen
# Rythmus
6:45 - 7:10 : Get up, get ready for school
07:10 - 16:20 : Be in school, spend time APAP
16:20 - 17:40 : First Pomodoro (Gym)
17:40 - 18:55 : Second (First) Pomodoro
19:00 - 20:15 : Third (Second) Pomodoro
20:15 - 21:15 : Fourth (Third) Pomodoro
21:20 - 22:35 : Menial Labor/Free Time/Eating (Fourth Pomodoro)
22:35 - 23:00 : Going to bed, reflecting
# Lern-Strategie:
0. **Goals** - Setze dir konkrete, erreichbare Ziele in der Study-Session (u.A. 75% Zeit) + Zeitaufgabe
1. **Survey** - Erstes Lesen, Einordnen, anfängliches Verstehen
2. **Question** - Übungsaufgaben , max. 45 min lösen, Change of setting, 20 min lösen, in Lösung schauen, nochmal lösen
3. **Rephrase** - Informationen/Vorgehen verstehen, dann unabhängig aufschreiben, "Rubber-Duck erklären", Fragen: Warum, Wofür, Mit was verwandt, Wie?
4. **Active Recall** - Flashcards (Anki) , Packe-meinen-Koffer, Abfragen, Erklären
5. **Repetition** - ^ in uniformen / expandierenden Intervallen (1-1-1-1-1) o. (1-2-4-8-16)
## Environment:
- Lofi-Music
- Clear Desk
- Other account
- Obsidian notes
- **Notetaking must be functional, as its procrastination otherwise!** (Conceptual instead of Sequential Note-Taking, in all but final study pages)
## Working through textbooks
0. Preparation: Buch(er) und Kapitel identifizieren, alle Seiten skimmen, Übungsaufgaben anschauen -> Was ist wichtig? Warum machen wir das? Wie integriert sich das?
Abschnittsweise:
1. Durchlesen & Verstehen
2. Rephrase (v.a. Begriffe, Definitionen, Lemmas, Grafiken) & **kurz** notieren (Beweise wie Questions betrachten)
3. Übungsaufgaben machen: 
	1. Wenn Einfach -> Gehe zum nächsten Abschnitt
	2. Wenn noch schwierig -> Gehe zu 1.

## Learning for tests (Uni-Tests, Schul-Klausuren)
0. Themenmaterial skimmen, Themenübersicht erstellen, Beispielaufgaben anschauen
1. Material durchlesen, wiederverstehen
2. Notizen durchgehen, ggf. Konzeptionell anpassen
3. Lernblätter auf Basis von ^ **formulieren**, ggf. Flashcards erstellen
4. Kurzes Auswendiglernen
5. Übungsaufgaben machen:
	1. Wenn einfach: nächste Aufgabe
	2. Wenn schwer: Gehe ggf. zu 1., sonst zu 4.

## In-Class:
- Aktives lernen bevorzugen, "Mitlernen", Konzentriert sein: **"Ich sitze da, dann kann ich auch mein bestes geben"** / Alles ist eine mündliche Prüfung
- Inhaltlich nur relevantes aufschreiben
## After-Class:
- Durchgehen & Verstehen
- Von wichtigem Lernzettel schreiben
- ggf. Vorarbeiten
-> ca. 20-30 min / Fach (das am nächsten Tag ist)/ Nachmittag

## Notizenverwaltung:
- Für Verständnis / "Working-Memory" -> Hefter
- Für Leistungsvorbereitung / Klausur -> Zusammenfassung
- Für Leben -> Obsidian

[1] Dunlosky, J., Rawson, K. A., Marsh, E. J., Nathan, M. J., & Willingham, D. T. (2013). Improving Students’ Learning With Effective Learning Techniques: Promising Directions From Cognitive and Educational Psychology. Psychological Science in the Public Interest, 14(1), 4–58. https://doi.org/10.1177/1529100612453266

# Ernährung:
Proteinquellen:
- Lentils
- Eggs
- Whey-Protein
- Harzer Cheese
Carbs:
- Potatoes

# Fitness:
Routine: Push-Pull-Legs
https://docs.google.com/spreadsheets/d/1-i4IHdH2JQTHpr_2qWCW1ba0myo-ua3qO96Hvm8AGW4/edit?usp=sharing

### Push:
- Chest press 3x 6-9 
- Shoulder press 3x 6-9 
- Machine fly 2x 9-12 
- Seitheben maschine 2x 9-12
- Trizeps maschine 2x 9-12
### Pull:
- Pull ups 3x 6-9
- Pull downs 3x 6-9
- Wide rows 3x 6-9 
- Seated cable rows 3x 6-9 
- Preacher curl maschine 3x 9-12
### Legs:
- Leg press/Squats an smith maschine 3x 6-9 
- Leg extensions 2x 9-12 
- Leg curls 3x 6-9 
- Calf raises 3x 9-12 
- (Abs)


# Current links:
Habitica: https://habitica.com/
Github: https://github.com/Omycron83
Pomodoro: https://pomofocus.io/

# Github:
## Backup files:
Creating a new Git repository locally, syncing it with a remote repository on GitHub, and adding your local files involves a series of steps. Here's a step-by-step guide to help you achieve this:

1. **Create a New Local Git Repository:** Open your terminal or command prompt and navigate to the directory where you want to create your new repository.

    `cd /path/to/your/directory`

   Initialize a new Git repository in this directory.

    `git init`

2. **Create a Repository on GitHub:** Open your web browser and log in to your GitHub account.

Click the '+' icon in the top-right corner and select "New repository".

 Fill in the repository name, description, and other settings as needed.
 
 Click "Create repository".

3. **Link the Local Repository with the GitHub Repository:** On the GitHub repository page, you'll see the repository URL (HTTPS or SSH). Copy this URL.

4. **Add Remote to Your Local Repository:** In your terminal, navigate to your local repository if you're not already there.

    `cd /path/to/your/directory`

 Add the GitHub repository as a remote. Replace `<github-repo-url>` with the URL you copied.

    `git remote add origin <github-repo-url>`

5. **Sync Your Local Repository with GitHub:** Before you add files, it's a good practice to pull any changes that might have occurred on GitHub since you initialized the repository. This prevents conflicts later.

    `git pull origin main`

    Note: If your default branch is named something other than "main," replace it with the correct branch name.

6. **Add and Commit Your Local Files:** Copy or create the files you want to add to your repository into the local directory.

    Use the following commands to stage and commit your files:

    `git add . git commit -m "Initial commit"`

7. **Push Your Local Changes to GitHub:** Now, push your committed changes to GitHub:

    `git push origin main`

Again, replace "main" with your actual branch name if it's different.


Your local files are now added to your GitHub repository. You can continue working on your project, making changes, committing, and pushing them to GitHub using the same Git commands (add, commit, push).

Remember that if you're using two-factor authentication on GitHub, you might need to use a personal access token instead of your GitHub password when pushing changes. This token needs the appropriate permissions for repository access.

## Get files from there to here in reverse





