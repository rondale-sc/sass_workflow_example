sass_workflow_example
=====================

This is a small app designed to demonstrate persistent in browser sass editing

# Instructions

Steps `1..7` are setting up Chrome, and should only be performed once.

1. Open Chrome
2. Navigate to 'about:flags'
3. Find and click the "Enable Developer Tools experiments." link
4. Click re-launch at the bottom
5. Open the developer console, then click the Cog (bottom right)
6. Go to "Experiments" 
   - Enable "Sass stylesheet debugging"
7. Go to "General"
   - Enable "Sourcemaps"
   - Enable "Auto-reload CSS upon Sass save"
8. From the terminal run the following commands:
   - `git clone git@github.com:rondale-sc/sass_workflow_example.git` 
   - `cd sass_workflow_example`
   - `ruby example_app.rb` - *This will start the sinatra server*
9. Open another terminal (or tab) and navigate to the `sass_workflow_example` repository (see step 8) and run the following command(s):
  - `sass --watch --sourcemap styles.sass:styles.css` - *Tells Sass to watch for changes to the Sass file and regenerate css whenever it is altered*
10. Return to Chrome and navigate to `http://localhost:4567`
11. Open the Developer Console
	- Inspect the `demo-box` element
	- Command (⌘) + click any css attribute
	- In the column to the left of your SASS file you'll see the file name
	- Right click the filename and select 'Save As'
	- Find and select the location of the file
12. Select any css attribute, modify it and save it.  It will be persisted to the **actual** sass file on disk, and the css reloaded to your browser
