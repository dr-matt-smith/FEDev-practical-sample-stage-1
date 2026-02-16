[Stage 0 & 1](https://github.com/dr-matt-smith/FEDev-practical-sample-stage-1)
| [Stage 2](https://github.com/dr-matt-smith/FEDev-practical-sample-stage-2)
| [Stage 3](https://github.com/dr-matt-smith/FEDev-practical-sample-stage-3)
| [Stage 4](https://github.com/dr-matt-smith/FEDev-practical-sample-stage-4)
| [Stage 5](https://github.com/dr-matt-smith/FEDev-practical-sample-stage-5)

# FEDev-practical-sample-stage-1

NOTE: A Captioned video work through of this stage has been published at:
- https://go.screenpal.com/watch/cOn2Ywn0F5z

This document summarises the steps I took when creating my solution to the sample FEDev Practial 1, which requires you to document (as Git commit-snapshots) each of the following progressive stages in your website development:

```
Stage 1. Basic HTML structure for 2 pages: “index.html” and “characters.html”
   a. No CSS
   b. No links
   c. No images

Stage 2. Add images

Stage 3. Add nav links

Stage 4. Add CSS, to make the pages look like the provided screenshots
   a. Using CSS style rules in 1 or more “.css” files

Stage 5. Refactor the website as a Svelte(kit) project
   a. Demonstrate reusable Svelte components, such as:
       i. Nav bar
       ii. page footer

Stage 6. Add a third “merchandise” page
   a. Add a link to this page in the nav bar
   b. Style this in a similar style to the other 2 pages
   c. Find images from the web for several merchandise items
   d. Add a form at the bottom of this page asking for:
       i. Name / email address / postal address
       ii. (you do NOT have to write code to process this forms submission)

Stage 7. For an ‘A’ grade illustrate some/all of the following:
   a. Replacing standard CSS rules with TailWindCSS
   b. Populating the merchandise page contents by looping through JSON data
   (rather than hard coded page content)
   c. Publish the site as static pages via GitHub Actions
```


## Stage 0: Setting up project

TO set up I did the following:

1. Created a new Github repo
    - making it **private**
    - adding a README
    - adding a **Node** `.gitognore` (since we know this will become a SvelteKit project)
    - adding `dr-matt-smith` as a collaborator

1. Created a new Celbridge project (you may use whatever editor you wish).

1. I cloned the Github repo to my local computer

1. I copied the Github repo files into my Celbridege folder
    - including the hidden `.git` directory
    - NOTE: It doesn't matter which README file (the Celbrdige one or the Github one) you have, since you'll edit this anyway ...
   
1. I downloaded and unZIPed the practical files from Brightspace, and copied them into the Celbridge project directory


## Stage 1. Basic HTML structure for 2 pages: “index.html” and “characters.html”

I did the following:

1. Created a directory `images` and moved all image files into that directory 
 
1. Create blank HTML files `index.html` and `characters.html`

1. Added a basic HTML skeleton to each file:

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>Rings of Power - (title/characters) page</title>
    </head>
    <body>
    </body>
    <html>
    ```

1. I used the text from the provided `page_content.txt` file to add into the HTML for the `<title>` and body for the home page 
   - so file  (`index.html`) looks like this:
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <title>Rings of power - home page</title>
   </head>
   <body>
   
   <footer>
   The Rings of Power &copy; 2024
   </footer>
   
   </body>
   </html>
   ```

1. I used the text from the provided `page_content.txt` file to add into the HTML for the `<title>` and body for the characters page 
   - I used `<h3>` for the capitalised character names
   - I used `<p>` for the text about each character
   - so file  (`characters.html`) looks like this:
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
   <title>Rings of power - characters page</title>
   </head>
   
   <body>
   
   <h3>GALADRIEL</h3>
   <p>
   Galadriel, an Elf is a key part of the story. We meet her in the Lord of the Rings, when she welcomes the Fellowship to Lothlórien. In The Rings of Power, we meet a younger Galadriel who is a very diﬀerent Galadriel: a fierce warrior who we meet on a mission to find Sauron after her brother died at his hands.
   </p>
   
   <h3>HALBRAND</h3>
   <p>
   After abandoning her ship to continue her mission to locate Sauron, she’s left adrift in the Sundering Seas before a broken boat full of humans rescue her. Among them is Halbrand who develops an uneasy alliance with Galadriel as the pair begin their journey to the island of Numenor.
   </p>
   
   <h3>ELROND</h3>
   <p>
   Elrond, the half-elf and the future leader of Rivendell. We meet younger version of Elrond as a young politician who finds himself kept out of key discussions as he is not yet a lord. However, Elrond is soon tasked with another mission, helping the legendary smith Celebrimbor.
   </p>
   
   <h3>PRINCE DURIN IV</h3>
   <p>
   During the Second Age, Khazad-dûm was the home to the dwarven kingdom, long before it falls into ruin. The kingdome is ruled over by King Durin III, who is supported by his son Prince Durin IV. We meet Durin IV burdened with the responsibility of keeping their kingdom thriving, and protecting it from outsiders.
   </p>
   
   <h3>DISA</h3>
   <p>
   Disa is Durin IV’s wife, who lives with him and their children in Khazad-dûm. Disa is also noted for her beautiful singing voice and fierceness.
   </p>
   
   <h3>ARONDIR</h3>
   <p>
   Arondir is a Silvan Elf soldier stationed in the Southlands, a station set up to keep an eye on the humans of the realm, after they allied with Morgoth during the First Age.
   </p>
   
   <h3>THE STRANGER</h3>
   <p>
   A mysterious character for the moment. Nori spots him after a meteor lands in the woods where she lives. But the tall man doesn’t speak their language and is like no one they’ve ever seen before.
   </p>
   
   <h3>NORI</h3>
   <p>
   Nori is one of the Harfoots, the early predecessors to the Hobbits, who migrate with the seaso
   </p>
   
   <footer>
   The Rings of Power &copy; 2024
   </footer>
   
   </body>
   </html>
   ```
   
1. I then edited the `README.md` file to record that project **Stage 1 - Basic HTML structure (no CSS/no links/no images)** was complete

1. I then followed the usual sequence of actions to create a new snapshot and upload it to Github:
   - add the changed/new files to the stating area
      - `git add .`
   - creatre a new commit-snapshot for the current status of the project
      - `git commit -m "Stage 1 - Basic HTML structure - completed""`
   - upload the new commit-snapshot to Github.com
      - `git push`
