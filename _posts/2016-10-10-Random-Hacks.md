Small hacks found along the way... never use safari on your iPhone again, make your keyboard cursor way faster...

##Never use Safari Again
From your iphone

Copy this: `javascript:location.href="googlechrome"+location.href.substring(4);`

* Open Safari, at the bottom of the screen select the "export" button and "Add Bookmark"
  (the actual page you bookmark doesn't matter right now)
* Open Safari bookmarks, (open-book icon at the bottom of the screen)
* Select "edit" from the bottom of the screen
* Find the bookmark you just created
  * Rename it "Open in Chrome" (or whatever)
  * Delete the URL and paste in the code from above

Now when you click a link and your iPhone automatically takes you to safari, all you have to do is select the open-book icon and then select the bookmark you just created and the page will be opened in Chrome.

**Reference for this document**
http://blog.jonabrams.com/post/26099585134/open-in-chrome


##Make your cursor move super faster

Everybody knows that you can get a pretty fast keyboard repeat rate by changing a slider on the Keyboard tab of the Keyboard & Mouse System Preferences panel. But you can make it even faster! In Terminal, run this command:
defaults write NSGlobalDomain KeyRepeat -int 0
Then log out and log in again. The fastest setting obtainable via System Preferences is 2 (lower numbers are faster), so you may also want to try a value of 1 if 0 seems too fast. You can always visit the Keyboard & Mouse System Preferences panel to undo your changes.

**Reference for this document**
http://hints.macworld.com/article.php?story=20090823193018149

You may find that a few applications don't handle extremely fast keyboard input very well, but most will do just fine with it.
